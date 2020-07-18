---
layout: post
title: [SAMSUNG SW - Laser Commuication]
date: 2020-7-18
description: txt to markdown
thumbnail: food2.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

﻿[241. SAMSUNG SW – Laser Communication]
- It was a difficult simulation problem for a long time.
- Since I had to remember all the possible number of mirror a shell can have.
- At first, I tried to approach just using BFS. But It was not that easy.
- So I started to check all the shell’s possible mirror number. 
- I worried since given memory size may be not enough to remember queue’s elements.
- But I had no choice without it. 
- I spent 1 hours and 30 minutes and 12 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<queue>
using namespace std;
int N, M;
vector<vector<char>> table;
vector<pair<int, int>> start;
int answer = 987654321;
const int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };
void BFS() {
	queue<vector<int>> que;
	vector<vector<int>> visit(N, vector<int>(M, 987654321));

	//for initial direction
	for (int d = 0; d < 4; d++) {
		que.push(vector<int>{start[0].first,start[0].second,0, d});
	}
	visit[start[0].first][start[0].second] = true;

	while (!que.empty()) {
		int x = que.front()[0]; int y = que.front()[1]; int cnt = que.front()[2]; int hori = que.front()[3]; que.pop();

		for (int d = 0; d < 4; d++) {
			int nx = x + dir[d][0]; int ny = y + dir[d][1]; int cur_cnt = cnt;
			if (nx < 0 || ny < 0 || nx >= N || ny >= M || table[nx][ny] == '*') continue;
			if (hori != d) cur_cnt += 1;

			if (visit[nx][ny] >= cur_cnt) {
				visit[nx][ny] = cur_cnt;
				que.push(vector<int>{nx, ny, cur_cnt, d});
			}
		}
	}
	answer = visit[start[1].first][start[1].second];
}


int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	cin >> M >> N;
	table.assign(N, vector<char>(M, 0));
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < M; j++) {
			cin >> table[i][j];
			if (table[i][j] == 'C') {
				start.emplace_back(make_pair(i, j));
			}
		}
	}

	//algorithm part
	BFS();
	cout << answer;
	return 0;
}

{% endraw %}
```

