---
layout: post
title: [SAMSUNG SW - Safety Area]
date: 2020-6-6
description: txt to markdown
thumbnail: breakfast-orange-lemon-oranges-large.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

﻿[208. SAMSUNG SW : Safety Area]
- It was a simulation problem. 
- I used BFS to determine how many safety areas are for each precipitation.
- I spent 11 minutes and 29 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<queue>
#define max(a,b) a>b?a:b
using namespace std;
vector<vector<int>> table;

int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };
int max_height=0;
int N;
int answer = 1;

void BFS(int height) {
	vector<vector<bool>> visit(N, vector<bool>(N, false));
	int res = 0;
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < N; j++) {
			if (table[i][j] > height && visit[i][j]==false) {
				res += 1;
				visit[i][j] = true;
				queue<vector<int>> que;
				que.push(vector<int>{i, j});
				while (!que.empty()) {
					int x = que.front()[0]; int y = que.front()[1]; que.pop();
					for (int d = 0; d < 4; d++) {
						int nx = x + dir[d][0]; int ny = y + dir[d][1];
						if (nx >= 0 && ny >= 0 && nx < N && ny<N && visit[nx][ny] == false && table[nx][ny]>height) {
							visit[nx][ny] = true;
							que.push(vector<int>{nx, ny});
						}
					}
				}
				
			}
		}
	}
	answer = max(answer, res);
}


int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	cin >> N;
	table.assign(N, vector<int>(N, 0));
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < N; j++) {
			cin >> table[i][j];
			max_height = max(max_height, table[i][j]);
		}
	}

	//algorithm part
	for (int i = 1; i < max_height; i++) BFS(i);
	cout << answer;
	return 0;
}

{% endraw %}
```

