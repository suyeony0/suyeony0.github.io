---
layout: post
title: [SAMSUNG SW - Move of Knight]
date: 2020-7-20
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

﻿[242. SAMSUNG SW – Move of Knight]
- It was an easy simulation problem.
- Using BFS with a given moving rules of knight, we can solve it very easily.
- I spent 6 minutes and 5 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<queue>
using namespace std;
int N, T;
vector<vector<bool>> table;
const int dir[8][2] = { {-2,-1},{-1,-2},{1,-2},{2,-1},{2,1},{1,2},{-1,2},{-2,1} };
int sx, sy, dx, dy;

int BFS() {
	queue<vector<int>> que;
	que.push(vector<int>{sx, sy, 0});
	table[sx][sy] = true;
	while (!que.empty()) {
		int x = que.front()[0]; int y = que.front()[1]; int cnt = que.front()[2]; que.pop();

		if (x == dx && y == dy) return cnt;

		for (int d = 0; d < 8; d++) {
			int nx = x + dir[d][0]; int ny = y + dir[d][1];
			if (nx < 0 || ny < 0 || nx >= N || ny >= N || table[nx][ny] == true) continue;
			que.push(vector<int>{nx, ny, cnt + 1});
			table[nx][ny] = true;
		}
	}
	return 0;
}

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	
	cin >> T;

	for (int test = 0; test < T; test++) {
		//get input;
		cin >> N;
		table.assign(N, vector<bool>(N, false));
		cin >> sx >> sy >> dx >> dy;
		cout<<BFS()<<endl;
	}
	return 0;
}

{% endraw %}
```

