---
layout: post
title: [SAMSUNG SW Repeat - Laboratory]
date: 2020-6-4
description: txt to markdown
thumbnail: breakfast-orange-lemon-oranges-large.jpg
categories: SAMSUNG_SW

# Information for the author block
author : Loui
---

[8. SAMSUNG SW : Laboratory]
- it was a DFS with permutation problem.
- First, we had to choose 3 empty spaces to create walls to block the viruses. For this, I used permutation like DFS.
- Second, we had to make the viruses contagion their neighbor shells, I used DFS as well.
- Thrid, after contagion, find empty spaces in given 2D array.
- I spent 19 minute. actually, I missed to stop the time watch :)
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#define max(a,b) a>b?a:b
using namespace std;

int N, M;
vector<vector<int>> table;
vector<vector<int>> temp_table;
vector<pair<int, int>> space;
vector<pair<int, int>> virus;
vector<vector<bool>> visit;
int num_of_virus;
int num_of_space;
int answer = 0;

int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };

void safetyArea() {
	int res = 0;
	for (vector<int> row : temp_table) {
		for (int i : row) if (i == 0) res++;
	}
	answer = max(answer, res);
}

void DFS(int x, int y) {
	for (int i = 0; i < 4; i++) {
		int nx = x + dir[i][0]; int ny = y + dir[i][1];
		if (nx >= 0 && ny >= 0 && nx < N && ny < M && visit[nx][ny] == false && temp_table[nx][ny] != 1) {
			visit[nx][ny] = true;
			temp_table[nx][ny] = 2;
			DFS(nx, ny);
		}
	}
}

void permutation(int start,int cnt) {
	if (cnt == 3) {
		temp_table = table;
		visit.assign(N, vector<bool>(M, false));
		for (int i = 0; i < num_of_virus; i++) 
			DFS(virus[i].first,virus[i].second);
		safetyArea();
		return;
	}
	for (int i = start; i < num_of_space; i++) {
		table[space[i].first][space[i].second] = 1;
		permutation(i + 1, cnt + 1);
		table[space[i].first][space[i].second] = 0;
	}
}

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	cin >> N >> M;
	table.assign(N, vector<int>(M, 0));
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < M; j++) {
			cin >> table[i][j];
			if (table[i][j] == 0) space.emplace_back(make_pair(i, j));
			else if (table[i][j] == 2) virus.emplace_back(make_pair(i, j));
		}
	}
	num_of_virus = virus.size();
	num_of_space = space.size();

	//algorithm part
	permutation(0, 0);
	cout << answer;
	return 0;
}

{% endraw %}
```

