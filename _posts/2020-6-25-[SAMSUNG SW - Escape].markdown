---
layout: post
title: [SAMSUNG SW - Escape]
date: 2020-6-25
description: txt to markdown
thumbnail: city2.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

﻿[226. SAMSUNG SW – Escape]
- it was an easy simulation problem.
- First, Spreading water.
- Second, Pushing all the possible next position of the hedgehog to a queue from a current position by spending same time.
- Third, During Pushing next position, if the hedgehog meets the destination, print the spending time.
- Fourth, if queue becomes empty without reaching the destination, print ”KAKTUS”.
- I spent 16 minutes and 19 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<queue>
using namespace std;

int N, M;
vector<vector<char>> table;
int sx, sy;
vector<vector<bool>> visit;
queue<vector<int>> que;
vector<vector<int>> water;
bool safe = false;
int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };

void Flood() {
	int _size = water.size();
	for (int i = 0; i < _size; i++) {
		int x = water[i][0]; int y = water[i][1];
		for (int d = 0; d < 4; d++) {
			int nx = x + dir[d][0]; int ny = y + dir[d][1];
			if (nx < 0 || ny < 0 || nx >= N || ny >= M || table[nx][ny]=='*' || table[nx][ny]=='X' || table[nx][ny]=='D') continue;
			table[nx][ny] = '*';
			water.emplace_back(vector<int>{nx,ny});
		}
	}
}

void MoveHedgehog(){
	int cur_time = que.front()[2];

	while (!que.empty()) {
		int x = que.front()[0]; int y = que.front()[1]; int time = que.front()[2];
		if (cur_time != time) break;
		if (table[x][y] == 'D') {
			safe = true;
			return;
		}
		que.pop();

		for (int d = 0; d < 4; d++) {
			int nx = x + dir[d][0]; int ny = y + dir[d][1];
			if (nx < 0 || ny < 0 || nx >= N || ny >= M || table[nx][ny] == '*' || table[nx][ny] == 'X' ||visit[nx][ny]==true) continue;
			visit[nx][ny] = true;
			que.push(vector<int>{nx, ny, time + 1});
		}
	}
	

}

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	cin >> N >> M;
	table.assign(N, vector<char>(M, '.'));
	visit.assign(N, vector<bool>(M, false));
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < M; j++) {
			cin >> table[i][j];
			if (table[i][j] == 'S') {
				sx = i; sy = j;
			}
			if (table[i][j] == '*') water.emplace_back(vector<int>{i, j});

		}
	}

	//algorithm part
	que.push(vector<int>{sx, sy, 0}); // x,y, minutes
	visit[sx][sy] = true;
	while (!que.empty() && !safe) {
		Flood();
		MoveHedgehog();
	}
	if (safe) cout << que.front()[2];
	else cout << "KAKTUS";
	return 0;
}

{% endraw %}
```

