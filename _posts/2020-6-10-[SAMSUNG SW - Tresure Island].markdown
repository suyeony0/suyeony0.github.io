---
layout: post
title: [SAMSUNG SW - Tresure Island]
date: 2020-6-10
description: txt to markdown
thumbnail: breakfast-orange-lemon-oranges-large.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

﻿[212. SAMSUNG SW : Tresure Island]
- It was a BFS problem. 
- For all the land, I had to search maximum distance from a current shell using BFS.
- I spent 7 minutes and 21 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<queue>
#define max(a,b) a>b?a:b
using namespace std;
vector<vector<char>> table;
int N, M;
int answer = 0;
int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };

int BFS(int x, int y) {
	queue<vector<int>> que;
	que.push(vector<int>{x, y, 0});
	vector<vector<bool>> visit(N, vector<bool>(M, false));
	visit[x][y] = true;
	int res = 0;
	while (!que.empty()) {
		x = que.front()[0]; y = que.front()[1]; int cnt = que.front()[2];
		que.pop();
		res = max(res, cnt);
		for (int d = 0; d < 4; d++) {
			int nx = x + dir[d][0]; int ny = y + dir[d][1];
			if (nx >= 0 && ny >= 0 && nx < N && ny < M && visit[nx][ny] == false && table[nx][ny] == 'L') {
				visit[nx][ny] = true;
				que.push(vector<int>{nx, ny, cnt + 1});
			}
		}
	}
	return res;
}

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);
	
	//get input
	cin >> N >> M;
	table.assign(N, vector<char>(M, 0));
	string input;
	for (int i = 0; i < N; i++) {
		cin >> input;
		for (int j = 0; j < M; j++) {
			table[i][j] = input[j];
		}
	}

	//algorithm part
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < M; j++) {
			if (table[i][j] == 'L') {
				answer=max(answer,BFS(i, j));
			} 
		}
	}
	cout << answer;
	return 0;
}

{% endraw %}
```

