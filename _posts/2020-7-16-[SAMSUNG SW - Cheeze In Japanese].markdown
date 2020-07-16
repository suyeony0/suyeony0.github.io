---
layout: post
title: [SAMSUNG SW - Cheeze In Japanese]
date: 2020-7-16
description: txt to markdown
thumbnail: food2.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

﻿[240. SAMSUNG SW – チーズ]
- It was a simulation problem. But it was written in japanese.
- So I guessed the problem using input and output.
- In my interpretation, we have to find minimum path from start position to destinations.
- The number of destination can be 9 at most. And we have to reach with ascending order.
- I spent 12 minutes and 4 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<queue>
#include<string>
using namespace std;

int N, M, T;
vector<vector<char>> table;
vector<vector<int>> visit;
const int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };

int sx, sy;
int answer=0;
void BFS(int bfs_cnt, int target) {
	queue<vector<int>> que;
	que.push(vector<int>{sx, sy, 0});
	visit[sx][sy] = bfs_cnt;
	while (!que.empty()) {
		int x = que.front()[0]; int y = que.front()[1]; int cnt = que.front()[2]; que.pop();
		if (table[x][y]-'0' == target) {
			answer += cnt;
			sx = x; sy = y;
			return;
		}
		
		for (int d = 0; d < 4; d++) {
			int nx = x + dir[d][0]; int ny = y + dir[d][1];
			if (nx < 0 || ny < 0 || nx >= N || ny >= M || table[nx][ny] == 'X' || visit[nx][ny] == bfs_cnt) continue;
			que.push(vector<int>{nx, ny, cnt + 1});
			visit[nx][ny] = bfs_cnt;
		}
	}
}


int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	cin >> N >> M >> T;
	table.assign(N, vector<char>(M, 0));
	visit.assign(N, vector<int>(M, -1));
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < M; j++) {
			cin >> table[i][j];
			if (table[i][j] == 'S') {
				sx = i; sy = j;
			}
		}
	}

	//algorithm part
	int target = 1;
	while (target <= T) {
		BFS(target, target);
		target += 1;
	}
	cout << answer;
	return 0;

}

{% endraw %}
```

