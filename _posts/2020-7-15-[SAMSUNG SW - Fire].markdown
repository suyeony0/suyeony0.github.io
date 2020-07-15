---
layout: post
title: [SAMSUNG SW - Fire]
date: 2020-7-15
description: txt to markdown
thumbnail: breakfast-orange-lemon-oranges-large.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

﻿[239. SAMSUNG SW – Fire]
- It was a simulation problem.
- First, fire has to be spreaded. So I used 2 queue, a queue for recording new position of fire, another queue for implemting BFS.
- Second, person has to move to edge of the building. So I used 2 queue, like above. Since fire speads every second, we have to record current position to move at next second.
- I spent 16 minutes and 14 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<queue>
#define FAIL 987654321
using namespace std;

int N, M, T;
vector<vector<char>> table;
int sx, sy;
queue<pair<int, int>> fire;
queue<vector<int>> person;
const int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };

void MoveFire() {
	queue<pair<int, int>> que = fire;
	fire = queue<pair<int, int>>{};
	while (!que.empty()) {
		int x = que.front().first; int y = que.front().second; que.pop();
		for (int d = 0; d < 4; d++) {
			int nx = x + dir[d][0]; int ny = y + dir[d][1];
			if (nx < 0 || ny < 0 || nx >= N || ny >= M || table[nx][ny] == '#' || table[nx][ny]=='*') continue;
			fire.push(make_pair(nx, ny));
			table[nx][ny] = '*';
		}
	}
}


int BFS() {
	vector<vector<bool>> visit(N, vector<bool>(M, false));
	visit[sx][sy] = true;
	while (!person.empty()) {
		queue<vector<int>> que = person;
		person = queue<vector<int>>{};
		MoveFire();
		while (!que.empty()) {
			int x = que.front()[0]; int y = que.front()[1]; int cnt = que.front()[2]; que.pop();

			if (x == 0 || y == 0 || x == N - 1 || y == M - 1) return cnt;

			for (int d = 0; d < 4; d++) {
				int nx = x + dir[d][0]; int ny = y + dir[d][1];
				if (nx < 0 || ny < 0 || nx >= N || ny >= M || table[nx][ny] == '#' || table[nx][ny] == '*' || visit[nx][ny]==true) continue;
				visit[nx][ny] = true;
				person.push(vector<int>{nx, ny, cnt + 1});
			}
		}
	}
	
	return FAIL;
}

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	
	cin >> T;
	for (int test_case = 0; test_case < T; test_case++) {

		//get input
		cin >> M >> N;
		table.assign(N, vector<char>(M, ' '));
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < M; j++) {
				cin >> table[i][j];
				if (table[i][j] == '@') {
					sx = i; sy = j;
				}
				if (table[i][j] == '*') fire.push(make_pair(i, j));
			}
		}
		person.push(vector<int>{sx, sy, 1});
		//algorithm part

		int answer=BFS();
		if (answer == FAIL) cout << "IMPOSSIBLE"<<endl;
		else cout << answer << endl;

		person = queue<vector<int>>{};
		fire = queue<pair<int, int>>{};
	}
	return 0;
}

{% endraw %}
```

