---
layout: post
title: [Samsung SW - Famous 7 Princesses]
date: 2020-5-29
description: txt to markdown
thumbnail: building1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

```cpp
	﻿[200. [SAMSUNG SW – Famous 7 Princesses]
	- Wow, I have to say it was quite hard and difficult.
	- I thought it was a simulation problem, so if I had used DFS or BFS, I could’ve solved this problem. 
	- but it was a combination problem. since although I used DFS or BFS, I wasn’t able to search like crossroad. 
	- Therefore, I had to choose 7 people first using combination. After that, I had to check the member included at least 4 “S” member and if Yes, I also had to check the people were connected each other.
	- To determine they were connected, I used DFS.
	- see the code.
	#include<iostream>
	#include<vector>
	#include<set>
	using namespace std;
	vector<vector<char>> table(5, vector<char>(5, 0));
	vector<vector<bool>> visit;
	vector<vector<int>> temp_table;
	vector<pair<int, int>> s_pos;
	vector<pair<int, int>> cur_com;
	int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };
	int res = 0;
	int conneceted_size;
	
	void DFS(int x, int y) {
		conneceted_size++;
		for (int i = 0; i < 4; i++) {
			int nx = x + dir[i][0]; int ny = y + dir[i][1];
			if (nx >= 0 && ny >= 0 && nx < 5 && ny < 5 && temp_table[nx][ny] == 1 && visit[nx][ny] == false) {
				visit[nx][ny] = true;
				DFS(nx, ny);
			}
		}
	}
	bool isConnected() {
		conneceted_size = 0;
		temp_table.assign(5, vector<int>(5, 0));
		visit.assign(5, vector<bool>(5, false));
		for (int i = 0; i < 7; i++) temp_table[cur_com[i].first][cur_com[i].second] = 1;
		visit[cur_com[0].first][cur_com[0].second] = true;
		DFS(cur_com[0].first, cur_com[0].second);
		if (conneceted_size == 7) return true;
		return false;
	}
	
	void Combination(int start_x, int start_y, int cnt, int member) {
		if (cnt == 7 ) {
			if (member >= 4) {
				if (isConnected()) res += 1;
				return;
			}
			return;
		}
		for (int i = start_x; i < 5; i++) {
			for (int j = start_y; j < 5; j++) {
				cur_com.emplace_back(make_pair(i, j));
				bool S_member=false;
				if (table[i][j] == 'S') S_member = true;
				if (j == 4) {
					Combination(i + 1, 0, cnt + 1, member + S_member);
					start_y = 0;
				}
				else Combination(i, j + 1, cnt + 1, member + S_member);
				cur_com.pop_back();
			}
		}
	
	
	}
	
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
	
		//get input
		string input;
		for (int i = 0; i < 5; i++) {
			cin >> input;
			for (int j = 0; j < 5; j++) {
				table[i][j] = input[j];
				if (input[j] == 'S') {
					s_pos.emplace_back(make_pair(i, j));
				}
			}
		}
	
		//algorithm part
		Combination(0, 0, 0, 0);
		cout << res;
		return 0;
	}
	
```
