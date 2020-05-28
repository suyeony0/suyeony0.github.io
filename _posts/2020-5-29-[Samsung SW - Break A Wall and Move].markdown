---
layout: post
title: [Samsung SW - Break A Wall and Move]
date: 2020-5-29
description: txt to markdown
thumbnail: food2.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

```cpp
	﻿[203. [SAMSUNG SW – Break A Wall and Move]
	- It was a simulation problem to find the shortest path from start to end position.
	- I used DFS first, but I failed since there is no insurance that a path I found is minimum path when we use DFS.
	- so I changed it to BFS and solved it.
	- see the code.
	#include<iostream>
	#include<vector>
	#include<queue>
	#define min(a,b) a>b?b:a
	using namespace std;
	
	int N, M;
	vector<vector<int>> table;
	vector<vector<vector<bool>>> visit;
	int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };
	bool flag = false;
	int BFS() {
		queue<vector<int>> que;
		que.push(vector<int>{0, 0, 1,1});
		visit[0][0][1] = true;
		while (!que.empty()) {
			int x = que.front()[0]; int y = que.front()[1]; int punch = que.front()[2]; int sum = que.front()[3];
			if (x == N - 1 && y == M - 1) return sum;
			que.pop();
			for (int i = 0; i < 4; i++) {
				int nx = x + dir[i][0]; int ny = y + dir[i][1];
				if (nx >= 0 && ny >= 0 && nx < N && ny < M) {
					if (table[nx][ny] == 1) {
						if (punch && visit[nx][ny][0]==false) {
							visit[nx][ny][0] = true;
							que.push(vector<int>{nx, ny, 0,sum+1});
						}
						else continue;
					}
					else if(visit[nx][ny][punch] == false) {
						visit[nx][ny][punch] = true;
						que.push(vector<int>{nx, ny, punch,sum+1});
					}
				}
			}
		}
		return -1;
	}
	
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
	
		//get input
		cin >> N >> M;
		table.assign(N, vector<int>(M, 0));
		visit.assign(N, vector<vector<bool>>(M, vector<bool>(2, false)));
		string input;
		for (int i = 0; i < N; i++) {
			cin >> input;
			for (int j = 0; j < M; j++) {
				table[i][j] = input[j] - '0';
			}
		}
	
		//algorithm part
		int answer=BFS();
		cout << answer;
		return 0;
	
	}
	
	
```
