---
layout: post
title: [Samsung SW - Baby Shark]
date: 2020-5-28
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}

	﻿[143. [SAMSUNG – SW : Baby Shark]]
	- BFS problem, there is an order of BFS. so I had to sort shells I will visit for each depth.
	- and they gave quite a lot of condition, like time, shark size, eating condition, etc.
	- see the code.
	#include<iostream>
	#include<fstream>
	#include<vector>
	#include<queue>
	#include<algorithm>
	using namespace std;
	
	int n; int sx; int sy;
	vector<vector<int>> table;
	int dir[4][2] = { {-1,0},{0,-1},{0,1},{1,0} };
	void Input() {
		
		ifstream in("C:\\Users\\gjsgu\\Desktop\\Algorithm\\test_case\\test_case_for_baby_shark.txt");
		if (in.is_open()) cout << "file is opened." << endl;
		in >> n;
		table.assign(n, vector<int>(n));
		for (int i = 0; i < n; i++) {
			for (int j = 0; j < n; j++) {
				in >> table[i][j];
				if (table[i][j] == 9) { table[i][j] = 0; sx = i; sy = j; }
			}
		}
	
	}
	
	void Input2() {
	
		cin >> n;
		table.assign(n, vector<int>(n));
		for (int i = 0; i < n; i++) {
			for (int j = 0; j < n; j++) {
				cin >> table[i][j];
				if (table[i][j] == 9) { table[i][j] = 0; sx = i; sy = j; }
			}
		}
	
	}
	
	void printTable() {
		for (vector<int> row : table) {
			for (int i : row)
				cout << i << " ";
			cout << endl;
		}
		cout << endl;
	}
	
	int grownUp() {
		queue<vector<int>> que;
		int total_time = 0;
		int shark_size = 2; //initial shark_size
		int eat_size = 0;
		vector<vector<bool>> visit(n, vector<bool>(n, false));
		que.push(vector<int>{sx, sy, 0});
		while (!que.empty()) {
			int x = que.front()[0]; int y = que.front()[1]; int time = que.front()[2];
			vector<pair<int, int>> order;
			while (!que.empty() && que.front()[2] == time) {
				order.push_back(make_pair(que.front()[0], que.front()[1]));
				que.pop();
			}
			sort(order.begin(), order.end(), [](pair<int, int> a, pair<int, int> b) {return a.second < b.second; });
			sort(order.begin(), order.end());
			for (int i = 0; i < order.size(); i++) {
				int x = order[i].first; int y = order[i].second;
				if (table[x][y] != 0 && table[x][y] < shark_size) { //when it is possible to eat.
					total_time += time;
					eat_size++;
					if (eat_size == shark_size) {
						shark_size++;
						eat_size = 0;
					}
					table[x][y] = 0;
					visit = vector<vector<bool>>(n, vector<bool>(n, false)); //visit re-initialize.
					queue<vector<int>> empty_que;
					que.swap(empty_que); //make the queue empty.
					que.push(vector<int>{x, y, 0});
					visit[x][y] = true;
					break;
				}
				for (int i = 0; i < 4; i++) {
					int tx = x + dir[i][0]; int ty = y + dir[i][1];
					if (tx >= 0 && ty >= 0 && tx < n && ty < n && table[tx][ty] <= shark_size && !visit[tx][ty]) {
						visit[tx][ty] = true;
						que.push(vector<int>{tx, ty, time + 1});
					}
				}
			}
			
		}
		return total_time;
	}
	
	int main() {
		Input2();
		cout << grownUp();
		return 0;
	}
	
	
{% endraw %}
