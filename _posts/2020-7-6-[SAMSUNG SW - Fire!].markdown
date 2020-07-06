---
layout: post
title: [SAMSUNG SW - Fire!]
date: 2020-7-6
description: txt to markdown
thumbnail: breakfast-orange-lemon-oranges-large.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

﻿[233. SAMSUNG SW – Fire!]
- It was a simulation problem.
- They gave an ambiguous condition that there is no mention which is first between person and fire.
- First, I moved person first but it was wrong. so I swap the order.
- For person’s move, I used double while syntax. Since after moving 1 shell, fire has to be spreaded.
- For Fire’s move, I used two queue to remember currently spreaded fires.
- I spent 32 minutes and 2 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<queue>
#define FAIL 987654321
using namespace std;

int N, M;
vector<vector<char>> table;
int sx, sy;
const int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };
vector<vector<bool>> visit;
vector<vector<bool>> fire_visit;
queue<vector<int>> fire_que;

void PrintTable() {
	cout << endl;
	for (vector<char> row : table) {
		for (char c : row) cout << c << " ";
		cout << endl;
	}
	cout << endl;
}

void MoveFire() {
	queue<vector<int>> NQ = fire_que;
	fire_que = queue<vector<int>>{};
	while (!NQ.empty()) {
		int x = NQ.front()[0]; int y = NQ.front()[1]; NQ.pop();
		if (fire_visit[x][y]==false) {
			fire_visit[x][y] = true;
			for (int d = 0; d < 4; d++) {
				int nx = x + dir[d][0]; int ny = y + dir[d][1];
				if (nx < 0 || ny < 0 || nx >= N || ny >= M || table[nx][ny] == '#') continue;
				table[nx][ny] = 'F';
				fire_que.push(vector<int>{nx, ny});
			}
		}
	}
}

int MovePerson() {
	queue<vector<int>> que;
	que.push(vector<int>{sx, sy, 1});
	
	visit[sx][sy] = true;

	while (!que.empty()) {
		MoveFire();
		int cur_cnt = que.front()[2];
		while (!que.empty()) {
			int x = que.front()[0]; int y = que.front()[1]; int cnt = que.front()[2];
			if (x == 0 || y == 0 || x == N - 1 || y == M - 1) return cnt;
			if (cur_cnt != cnt) break;
			que.pop();

			for (int d = 0; d < 4; d++) {
				int nx = x + dir[d][0]; int ny = y + dir[d][1];
				if (nx < 0 || ny < 0 || nx >= N || ny >= M || table[nx][ny] == '#'|| table[nx][ny]=='F' || visit[nx][ny]) continue;
				visit[nx][ny] = true;
				que.push(vector<int>{nx, ny, cnt + 1});
			}
		}
	}
	return FAIL;
}



int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	cin >> N >> M;
	table.assign(N, vector<char>(M, 0));
	fire_visit.assign(N, vector<bool>(M, false));
	visit.assign(N, vector<bool>(M, false));
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < M; j++) {
			cin >> table[i][j];
			if (table[i][j] == 'J') {
				sx = i; sy = j;
			}
			else if (table[i][j] == 'F') {
				fire_que.push(vector<int>{i, j});
			} 
		}
	}
	
	int answer=MovePerson();
	if (answer == FAIL) cout << "IMPOSSIBLE ";
	else cout << answer;
	return 0;
}


{% endraw %}
```

