---
layout: post
title: [SAMSUNG SW Repeat - Snake]
date: 2020-5-28
description: txt to markdown
thumbnail: food2.jpg
categories: SAMSUNG_SW

# Information for the author block
author : Loui
---

`

	[3. SAMSUNG SW ? Snake]
	- it was a simulation problem. there was a trick that the snake have to enlarge the head first and check whether the tail sholud be shrink or not.
	- one more trivial trick is the given apple`s position start with (1,1) not (0,0).
	- see the code.
	#include<iostream>
	#include<vector>
	#include<unordered_map>
	using namespace std;
	
	int N,K,L;
	int cur_dir = 3;
	vector<vector<int>> table;
	unordered_map<int, char> curve;
	int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };
	
	void printTable() {
		for (vector<int> row : table) {
			for (int i : row) cout << i << " ";
			cout << endl;
		}
		cout << endl;
	}
	
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
	
		//get input
		cin >> N>>K;
		table.assign(N, vector<int>(N, 0));
		int x, y;
		table[0][0] = 2;
		for (int i = 0; i < K; i++) {
			cin >> x >> y;
			table[x-1][y-1] = 1;
		}
		cin >> L;
		int l; char c;
		for (int i = 0; i < L; i++) {
			cin >> l >> c;
			curve[l] = c;
		}
	
	
		//algorithm part
		int sec = 0;
		vector<pair<int, int>> snake;
		snake.emplace_back(make_pair(0, 0));
		while(true) {
			sec += 1;
			int hx = snake.back().first + dir[cur_dir][0]; int hy = snake.back().second + dir[cur_dir][1];
			if (hx < 0 || hy < 0 || hx >= N || hy >= N || table[hx][hy] == 2) break;
			else if (table[hx][hy] == 1) {
				table[hx][hy] = 2;
				snake.emplace_back(make_pair(hx, hy));
			}
			else if (table[hx][hy] == 0) {
				table[hx][hy] = 2;
				table[snake.front().first][snake.front().second] = 0;
				snake.erase(snake.begin());
				snake.emplace_back(make_pair(hx, hy));
			}
	
			if (curve.find(sec) != curve.end()) {
				if (curve[sec] == 'L') 	cur_dir = (cur_dir + 1) % 4;
				else {
					cur_dir -= 1;
					if (cur_dir < 0) cur_dir = 3;
				}
			}
	
		}
		cout << sec;
		return 0;
	}
	
`

