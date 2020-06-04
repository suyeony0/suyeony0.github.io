---
layout: post
title: [SAMSUNG SW Repeat - Laboratory 3]
date: 2020-6-4
description: txt to markdown
thumbnail: building1.jpg
categories: SAMSUNG_SW

# Information for the author block
author : Loui
---

﻿[25. SAMSUNG SW : Laboratory 3]
- It was a simulation problem. I chose viruses using DFS-Combination and simulated it using BFS.
- but there was an edge condition that what we should do if we met an unactivated virus.
- In the case, we had to check whether all the shell has a virus even if we don’t pass the virus.
- I spent 41 minutes and 55 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<queue>
#define min(a,b) a>b?b:a
#define max(a,b) a>b?a:b
using namespace std;
int N, M;
vector<vector<int>> table;
vector<vector<bool>> visit; 
vector<pair<int, int>> virus;
vector<pair<int, int>> chosen;
int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };
int num_of_virus = 0;
int answer = 987654321;


bool isValid(vector<vector<int>>& temp_table) {
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < N; j++) {
			if (temp_table[i][j] == 0) return false;
		}
	}
	return true;
}

int BFS() {
	vector<vector<bool>> temp_visit = visit;
	vector<vector<int>> temp_table = table;
	queue<vector<int>> que;
	for (pair<int, int> cur : chosen) que.push(vector<int>{cur.first, cur.second, 0});
	int res = 0;
	while (!que.empty()) {
		int x = que.front()[0]; int y = que.front()[1]; int sec = que.front()[2]; //int index = que.front()[3];
		que.pop();
		for (int i = 0; i < 4; i++) {
			int nx = x + dir[i][0]; int ny = y + dir[i][1];
			if (nx >= 0 && ny >= 0 && nx < N && ny < N && temp_table[nx][ny] !=1 && temp_visit[nx][ny] == false) {
				temp_visit[nx][ny] = true;
				if (temp_table[nx][ny] == 1000 && isValid(temp_table)) 
					return res;
				temp_table[nx][ny] = 2;
				que.push(vector<int>{nx, ny, sec + 1});
				res = max(res, sec + 1);
			}
		}
	}
	if (isValid(temp_table)) return res;
	return 987654321;
}


void Combination(int cnt, int start) {
	if (cnt == M) {
		int res = BFS();
		answer=min(res,answer);
		return;
	}

	for (int i = start; i < num_of_virus; i++) {
		int x = virus[i].first; int y = virus[i].second;
		chosen.emplace_back(make_pair(x, y));
		visit[x][y] = true;
		table[x][y] = 2;
		Combination(cnt + 1, i + 1);
		table[x][y] = 1000;
		visit[x][y] = false;
		chosen.pop_back();
	}

}

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	cin >> N >> M;
	table.assign(N, vector<int>(N, 0));
	visit.assign(N, vector<bool>(N, false));
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < N; j++) {
			cin >> table[i][j];
			if (table[i][j] == 2) {
				table[i][j] = 1000;
				virus.emplace_back(make_pair(i, j));
			} 
		}
	}
	num_of_virus = virus.size();
	//algorithm part
	Combination(0,0);
	if (answer == 987654321) cout << -1;
	else cout << answer;
	return 0;

}


{% endraw %}
```

