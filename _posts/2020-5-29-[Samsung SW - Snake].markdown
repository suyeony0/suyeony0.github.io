---
layout: post
title: [Samsung SW - Snake]
date: 2020-5-29
description: txt to markdown
thumbnail: breakfast-orange-lemon-oranges-large.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}

	﻿[102. [BACKJOON – SAMSUNG SW : Snake]]
	- I confused due to apple’s corordinate. they gave the corordiantes strating from row 1 and column 1 not 0 and 0.
	- to follow tail, I used queue.
	- I spent 1 hour and 10~20 minutes.
	- see the code.
	#include<iostream>
	#include<fstream>
	#include<vector>
	#include<queue>
	
	using namespace std;
	
	pair<queue<pair<int,char>>,vector<vector<int>>> makeTable() {
		ifstream in("C:\\Users\\gjsgu\\Desktop\\Algorithm\\test_case\\test_case_for_snake.txt");
		int N; int K;
		if (in.is_open()) {
			cout << "file is opened." << endl;
			in >> N; in >> K;
		}
		vector<vector<int>> table(N, vector<int>(N, 0)); // 0 is empty.
		table[0][0] = 2; // 2 is snake's body.
		int row, col;
		for (int i = 0; i < K; i++) {
			in >> row; in >> col;
			table[row-1][col-1] = 1; // 1 is apple.
		}
		int L; // the number of direction change.
		in >> L;
		int sec; char dir;
		queue<pair<int, char>> direction;
		for (int i = 0; i < L; i++) {
			in >> sec; in >> dir;
			direction.push({ sec,dir});
		}
		return make_pair(direction, table);
	}
	pair<queue<pair<int, char>>, vector<vector<int>>> makeTable2() {
		int N; int K;
		cin >> N; cin >> K;
		vector<vector<int>> table(N, vector<int>(N, 0)); // 0 is empty.
		table[0][0] = 2; // 2 is snake's body.
		int row, col;
		for (int i = 0; i < K; i++) {
			cin >> row; cin >> col;
			table[row-1][col-1] = 1; // 1 is apple.
		}
		int L; // the number of direction change.
		cin >> L;
		int sec; char dir;
		queue<pair<int, char>> direction;
		for (int i = 0; i < L; i++) {
			cin >> sec; cin >> dir;
			direction.push({ sec,dir });
		}
		return make_pair(direction, table);
	}
	
	
	void printTable(vector<vector<int>> table) {
		for (vector<int> row : table) {
			for (int i : row) {
				cout << i << " ";
			}
			cout << endl;
		}
	}
	
	int helper(vector<vector<int>>& table, queue<pair<int,char>>& direction) {
		int tx = 0, ty = 0;
		int hx = 0, hy = 0;
		int second = 0;
		vector<vector<int>> dir = { {1,0},{0,-1},{-1,0},{0,1} }; // down left up right
		queue<pair<int, int>> tail;
		tail.push(make_pair(0, 0));
		int cur_dir = 3; //start direction
		direction.push(make_pair(1000, 'L')); //At last time, snake has to move to a wall.
		while (!direction.empty()) {
			int cur_sec = direction.front().first;
			int continue_sec = cur_sec - second;
			char next_dir = direction.front().second;
			direction.pop();
			for (int i = 0; i < continue_sec; i++) {
				second++; // time plused.
				hx += dir[cur_dir][0]; hy += dir[cur_dir][1];
				tail.push(make_pair(hx, hy));
				// if head meets body or wall.
				if (hx < 0 || hx >= table.size() || hy < 0 || hy >= table[0].size()||table[hx][hy] == 2 ) return second;
				// if head meets an apple.
				else if (table[hx][hy] == 1) table[hx][hy] = 2; // notice that even though all the apple is eaten, the game won't be ended.
				
				// if head meets nothing.
				else {//tail has to be moved 1 cell.
					tx = tail.front().first; ty = tail.front().second;
					tail.pop();
					table[tx][ty] = 0;
					table[hx][hy] = 2;
					
				}
				//cout << "hx : " << hx << " hy : " << hy << " tx : " << tx << " ty : " << ty <<" second : "<< second<< endl;
				//printTable(table);
			}
			if (next_dir == 'L') { // turn left
				cur_dir--;
				cur_dir == -1 ? cur_dir = 3 : cur_dir;
			}
			else cur_dir = (cur_dir + 1) % 4; //turn right
			
		}
		return second;
	}
	
	int main() {
		//pair<queue<pair<int, char>>, vector<vector <int >>> input = makeTable();
		pair<queue<pair<int, char>>, vector<vector <int >>> input = makeTable2();
		vector<vector<int>> table = input.second;
		queue<pair<int, char>> direction = input.first;
		
		int answer= helper(table, direction);
		cout << answer;
	
		return 0;
	}
	
{% endhighlight %}
