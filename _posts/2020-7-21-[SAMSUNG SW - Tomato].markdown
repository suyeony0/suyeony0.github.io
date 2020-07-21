---
layout: post
title: [SAMSUNG SW - Tomato]
date: 2020-7-21
description: txt to markdown
thumbnail: food1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

﻿[243. SAMSUNG SW – Tomato]
- It was a simulation problem with 3D matrix.
- Except that a given matrix is 3D, it was a simliar problem I’ve solved till now.
- Just using BFS with 6 directions that are up, down, north, west, south, east, we can solve it easily.
- I used two queues to record new riped tomatos.
- I spent 13 minutes and 13 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<queue>
using namespace std;

int N, M, H;
vector<vector<vector<int>>> table;
int not_tomato = 0;
const int dir[6][3] = { {-1,0,0},{0,-1,0},{0,0,-1},{1,0,0},{0,1,0},{0,0,1} };

queue<vector<int>> BFS(queue<vector<int>> que) {
	queue<vector<int>> res;

	while(!que.empty()) {
		int h = que.front()[0]; int x = que.front()[1]; int y = que.front()[2]; que.pop();

		for (int d = 0; d < 6; d++) {
			int nh = h + dir[d][0]; int nx = x + dir[d][1]; int ny = y + dir[d][2];
			if (nh < 0 || nx < 0 || ny < 0 || nh >= H || nx >= N || ny >= M || table[nh][nx][ny] == 1 || table[nh][nx][ny] == -1) continue;
			table[nh][nx][ny] = 1;
			not_tomato -= 1;
			res.push(vector<int>{nh, nx, ny});
		}
	}
	return res;
}

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	queue<vector<int>> que;
	cin >> M >> N >> H;
	table.assign(H, vector<vector<int>>(N, vector<int>(M, 0)));

	for (int h = H - 1; h >= 0; h--) {
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < M; j++) {
				cin >> table[h][i][j];
				if (table[h][i][j] == 0) not_tomato += 1;
				if (table[h][i][j] == 1) que.push(vector<int>{h, i, j});
			}
		}
	}

	//algorithm part
	int answer = 0;
	while (not_tomato > 0) {
		answer += 1;
		int cur_tomato = not_tomato;
		que = BFS(que);
		if (cur_tomato == not_tomato) {
			cout << -1;
			return 0;
		}
	}
	cout << answer;
	return 0;

{% endraw %}
```

