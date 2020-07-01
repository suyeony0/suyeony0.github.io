---
layout: post
title: [SAMSUNG SW - Bakery]
date: 2020-7-1
description: txt to markdown
thumbnail: work1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

﻿[228. SAMSUNG SW – Bakery]
- It was a simulation problem. it looks quite difficult. But it’s not.
- Since we can’t put a pipe if a shell already has another pipe.
- But we don’t need to care of it. using greedy search, we can get our answer.
- Because, if we check up-right first, we can travel all the shell.
- First, Using DFS, finding a path from column 0 to columns M-1.
- Second, for all the row, repeating First.
- I spent 51 minutes and 46 seconds due to the above trick.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>

#define max(a,b) a>b?a:b
using namespace std;
int N, M;
vector<vector<char>> table;
vector<vector<bool>> visit;
int dir[3][2] = { {-1,1} ,{0,1},{1,1} };
int answer = 0;
int sum = 0;
bool flag = false;
void DFS(int x, int y) {
	if (y == M - 1) {
		answer += 1;
		flag = true;
		return;
	}

	for (int d = 0; d < 3; d++) {
		int nx = x+ dir[d][0]; int ny = y+dir[d][1];
		if (nx < 0 || nx >= N || visit[nx][ny] == true || table[nx][ny]=='x') continue;
		visit[nx][ny] = true;
		DFS(nx, ny);
		if (flag) return;
	}
}

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	cin >> N >> M;
	table.assign(N, vector<char>(M, 0));
	visit.assign(N, vector<bool>(M, false));
	string input;
	for (int i = 0; i < N; i++) {
		cin >> input;
		for (int j = 0; j < M; j++) {
			table[i][j]=input[j];
		}
	}

	//algorithm part
	
	for (int i = 0; i < N; i++) {
		visit[i][0] = true;
		flag = false;
		DFS(i, 0);
	} 
	cout << answer;
	return 0;
}


{% endraw %}
```

