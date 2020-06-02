---
layout: post
title: [SAMSUNG SW Repeat - Baby Shark]
date: 2020-6-2
description: txt to markdown
thumbnail: person1.jpeg
categories: SAMSUNG_SW

# Information for the author block
author : Loui
---

```cpp

{% raw %}

	﻿[20. SAMSUNG SW : Baby Shark]
	- it was a simulation problem. but a trick was the way the shark moves.
	- since if there were several prey that the shark can reach in same second, shark eats the highest prey and if their height is same, then eats the leftmost prey.
	- To solve this trick, I had to record preys that the shark can reach in same seconds.
	- I used BFS, and set to get highest with leftmost prey with O(1) time. Notice that insert a value into a set take O(log n) time.
	- I spent 1 hour and 11 minutes and 3 seconds.
	- see the code.
	#include<iostream>
	#include<vector>
	#include<queue>
	#include<set>
	using namespace std;
	
	int N;
	vector<vector<int>> table;
	vector<vector<bool>> visit;
	int bx, by;
	int dir[4][2] = { {-1,0},{0,-1},{0,1},{1,0} };
	
	void printTable() {
		cout << endl;
		for (vector<int> row : table) {
			for (int i : row) cout << i << " ";
			cout << endl;
		}
	}
	
	
	/*
	printTable();
					cout << "x : " << nx << " y : " << ny << endl;
					cout << "size : " << _size + 1 << " sec : " << sec + 1 << endl;
	*/
	
	int BFS() {
		queue<vector<int>> que;
		que.push(vector<int>{bx, by, 2,0}); // x y size sec
		visit[bx][by] = true;
		int eat = 0;
		int last_sec = 0;
		
		while (!que.empty()) {
			int sec = que.front()[3];
			set<pair<int, int>> fish = {};
			int _size = que.front()[2];
			while (!que.empty()) {
				int x = que.front()[0]; int y = que.front()[1]; int prev_sec = que.front()[3];
				if (sec != prev_sec) break;
				que.pop();
				for (int i = 0; i < 4; i++) {
					int nx = x + dir[i][0]; int ny = y + dir[i][1];
					if (nx >= 0 && ny >= 0 && nx < N && ny < N && visit[nx][ny] == false && table[nx][ny] <= _size) {
						if (table[nx][ny] != 0 && table[nx][ny] < _size) {
							fish.insert(make_pair(nx, ny));
						}
						else {
							visit[nx][ny] = true;
							que.push(vector<int>{nx, ny, _size, sec + 1});
						}
					}
				}
			}
			if (fish.size() > 0) {
				last_sec = sec+1;
				set<pair<int, int>>::iterator iter = fish.begin();
				int nx = iter->first; int ny = iter->second;
				table[nx][ny] = 0;
				eat += 1;
				visit.assign(N, vector<bool>(N, false));
				table[nx][ny] = 0;
				visit[nx][ny] = true;
				que = queue<vector<int>>{};
	
				if (eat == _size) {
					que.push(vector<int>{nx, ny, _size + 1, sec + 1});
					eat = 0;
					
				} 
				else {
					que.push(vector<int>{nx, ny, _size, sec + 1});
				
				} 
				
			}
			
		}
		return last_sec;
	
	}
	
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
	
		//get input
		cin >> N;
		table.assign(N, vector<int>(N, 0));
		visit.assign(N, vector<bool>(N, 0));
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < N; j++) {
				cin >> table[i][j];
				if (table[i][j] == 9) {
					bx = i; by = j;
					table[i][j] = 0;
				}
			}
		}
	
		//algorithm part
		int answer = BFS();
		cout << answer;
		return 0;
	
	}
	
{% endraw %}
```

