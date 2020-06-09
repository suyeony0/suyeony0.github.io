---
layout: post
title: [SAMSUNG SW - Get District]
date: 2020-6-9
description: txt to markdown
thumbnail: food1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

﻿[211. SAMSUNG SW : Get District]
- It was a BFS problem.
- except for converting given corrodisantes, thers was nothing special.
- I spent 20 minutes and 57 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<algorithm>
#include<queue>
using namespace std;
int N, M, K;
vector<vector<bool>> table;
vector<int> dis;
int answer = 0;
int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };


void DrawBox(int lx,int ly,int rx,int ry) {
	for (int i = rx; i <= lx; i++) {
		for (int j = ly; j <= ry; j++) {
			table[i][j] = true;
		}
	}
}

void BFS(int x, int y) {
	int res = 1;
	queue<vector<int>> que;
	que.push(vector<int>{x, y});
	table[x][y] = true;

	while (!que.empty()) {
		x = que.front()[0]; y = que.front()[1]; que.pop();
		for (int d = 0; d < 4; d++) {
			int nx = x + dir[d][0]; int ny = y + dir[d][1];
			if (nx >= 0 && ny >= 0 && nx < N && ny < M && table[nx][ny] == false) {
				table[nx][ny] = true;
				res +=1;
				que.push(vector<int>{nx, ny});
			}
		}
	}
	dis.emplace_back(res);
}


int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	cin >> N >> M >> K;
	table.assign(N, vector<bool>(M, false));
	int lx, ly, rx, ry;
	for (int i = 0; i < K; i++) {
		cin >> ly >> lx >> ry >> rx;
		lx = N - lx-1; rx = N - rx;
		ry -= 1;
		DrawBox(lx, ly, rx, ry);
	}

	//algorithm part
	
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < M; j++) {
			if (table[i][j] == false) {
				answer += 1;
				BFS(i,j);
			}
		}
	}
	sort(dis.begin(), dis.end());
	cout << answer << endl;
	for (int i : dis) cout << i << " ";
	return 0;

}


{% endraw %}
```

