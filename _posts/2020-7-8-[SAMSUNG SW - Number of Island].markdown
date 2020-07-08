---
layout: post
title: [SAMSUNG SW - Number of Island]
date: 2020-7-8
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

﻿[235. SAMSUNG SW – Number of Island]
- It was an easy BFS problem. But they gave me row and columns size oppositely.
- Due to that, I spent little more time.
- the algorithm is that During traveling all the shell of 2D array, if we meet a non-visit ground, start BFS to visit the ground’s island.
- I spent 11 minutes and 45 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<queue>
using namespace std;

int N, M;
vector<vector<int>> table;
vector<vector<int>> visit;
int dir[8][2] = { {-1,0},{-1,-1},{0,-1},{1,-1},{1,0},{1,1},{0,1},{-1,1} };

void BFS(int x,int y, int cnt) {
	queue<vector<int>> que;
	que.push(vector<int>{x, y});
	visit[x][y] = cnt;

	while (!que.empty()) {
		x = que.front()[0]; y = que.front()[1]; que.pop();

		for (int d = 0; d < 8; d++) {
			int nx = x + dir[d][0]; int ny = y + dir[d][1];
			if (nx < 0 || ny < 0 || nx >= N || ny >= M || table[nx][ny] == 0 || visit[nx][ny] == cnt) continue;
			visit[nx][ny] = cnt;
			que.push(vector<int>{nx, ny});
		}
	}
}

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	int cnt = 0;
	do {
		//get input
		cin >> M >> N;
		if (N == 0 && M == 0) break;
		table.assign(N, vector<int>(M, 0));
		visit.assign(N, vector<int>(M, -1));
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < M; j++) {
				cin >> table[i][j];
			}
		}

		//algorithm part
		int num_of_island = 0;
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < M; j++) {
				if (table[i][j] == 1 && visit[i][j] != cnt) {
					BFS(i, j,cnt);
					num_of_island+=1;
				}
			}
		}
		cout << num_of_island << endl;
		cnt += 1;
	} while (true);
	return 0;
}


{% endraw %}
```

