---
layout: post
title: [Samsung SW - Downhill]
date: 2020-5-29
description: txt to markdown
thumbnail: work1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

```cpp

{% raw %}

	﻿[195. [SAMSUNG SW – Downhill]
	- it was an easy simulation problem. just using memozation is the key to satisfy time limit.
	- see the code.
	#include<iostream>
	#include<vector>
	
	using namespace std;
	int N, M;
	vector<vector<int>> table;
	vector<vector<int>> visit;
	int dir[4][2] = { {-1,0 },{0,-1},{1,0},{0,1} }; // w a s d
	
	
	int DFS(int x, int y){
		//return part
		if (visit[x][y] != -1) return visit[x][y];
		if (x == N - 1 && y == M - 1) return 1;
	
		//DFS part
		int res = 0;
		for (int i = 0; i < 4; i++) {
			int nx = x + dir[i][0]; int ny = y + dir[i][1];
			if (nx >= 0 && ny >= 0 && nx < N && ny < M && table[x][y]>table[nx][ny]) {
				res += DFS(nx, ny);
			}
		}
		visit[x][y] = res;
		return res;
	}
	
	
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
		
		//get input
		cin >> N >> M;
		table.assign(N, vector<int>(M, 0));
		visit.assign(N, vector<int>(M, -1));
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < M; j++) {
				cin >> table[i][j];
			}
		}
	
		//algorithm part
		unsigned int answer = 0;
		answer=DFS(0, 0);
		cout << answer;
		return 0;
	
	}
	
{% endraw %}
```

