---
layout: post
title: [SAMSUNG SW - Sheep]
date: 2020-7-2
description: txt to markdown
thumbnail: city2.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

﻿[229. SAMSUNG SW – Sheep]
- it was an easy simultaion problem.
- Using BFS we can solve it easily.
- First, traveling all the shell, if we meet non-visit shell, start BFS from the shell.
- Second, During BFS, count sheeps and wolfs in the area.
- Thrid, if number of sheep is greater than wolf, subtract number of wolf from sum_of wolf or Vice versa.
- I spent 11 minutes and 52 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<queue>

using namespace std;
int N, M;
vector<vector<char>> table;
vector<vector<bool>> visit;
int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };
int sum_of_wolf = 0;
int sum_of_sheep = 0;

void BFS(int x, int y){
	queue<vector<int>> que;
	int num_of_sheep = 0; int num_of_wolf = 0;
	if (table[x][y] == 'v') num_of_wolf += 1;
	else if (table[x][y] == 'o') num_of_sheep += 1;
	que.push(vector<int>{x, y});
	visit[x][y] = true;
	while (!que.empty()) {
		x = que.front()[0]; y = que.front()[1]; que.pop();
		for (int d = 0; d < 4; d++) {
			int nx = x + dir[d][0]; int ny = y+ dir[d][1];
			if (nx < 0 || ny < 0 || nx >= N || ny >= M || table[nx][ny] == '#' || visit[nx][ny]==true) continue;
			visit[nx][ny] = true;
			if (table[nx][ny] == 'v') num_of_wolf += 1;
			else if (table[nx][ny] == 'o') num_of_sheep += 1; 
			que.push(vector<int>{nx, ny});
		}
	}
	if (num_of_sheep > num_of_wolf) sum_of_wolf -= num_of_wolf;
	else sum_of_sheep -= num_of_sheep;
}

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	cin >> N >> M;
	table.assign(N, vector<char>(M, 0));
	visit.assign(N, vector<bool>(M, false));
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < M; j++) {
			cin >> table[i][j];
			if (table[i][j] == 'v') sum_of_wolf += 1;
			else if (table[i][j] == 'o') sum_of_sheep += 1;
		}
	}

	//algorithm part
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < M; j++) {
			if (table[i][j] != '#' && visit[i][j] == false) {
				BFS(i, j);
			}
		}
	}
	cout << sum_of_sheep << " " << sum_of_wolf;
	return 0;

}

{% endraw %}
```

