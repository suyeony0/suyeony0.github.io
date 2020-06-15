---
layout: post
title: [SAMSUNG SW - Cheeze 2]
date: 2020-6-15
description: txt to markdown
thumbnail: building1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

﻿[217. SAMSUNG SW : Cheeze 2]
- It was a simulation problem like a just previous problem.
- it required more conditions. Without those things, they were almost same.
- I spent 12 minutes and 33 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<queue>

using namespace std;

int N, M;
vector<vector<short>> table;
vector<vector<bool>> air;
int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };

void AirVisit() {
	air.assign(N, vector<bool>(M, false));
	queue<vector<int>> que;
	que.push(vector<int>{0, 0});
	air[0][0] = true;
	while (!que.empty()) {
		int x = que.front()[0]; int y = que.front()[1]; que.pop();

		for (int d = 0; d < 4; d++) {
			int nx = x + dir[d][0]; int ny = y + dir[d][1];
			if (nx >= 0 && ny >= 0 && nx < N && ny < M && table[nx][ny] == 0 && air[nx][ny] == false) {
				air[nx][ny] = true;
				que.push(vector<int>{nx, ny});
			}
		}
	}
}

void Melting() {
	vector<pair<int, int>> stk;
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < M; j++) {
			if (table[i][j] == 1) {
				int num_of_air = 0;
				for (int d = 0; d < 4; d++) {
					int nx = i + dir[d][0]; int ny = j + dir[d][1];
					if (nx >= 0 && ny >= 0 && nx < N && ny < M && table[nx][ny] == 0 && air[nx][ny] == true) num_of_air += 1;
				}
				if (num_of_air >= 2) stk.emplace_back(make_pair(i, j));
			}
		}
	}
	
	for (pair<int, int> row : stk) {
		table[row.first][row.second] = 0;
	}
}

bool isEmpty() {
	for (vector<short> row : table) {
		for (short c : row) if (c != 0) return false;
	}
	return true;
}

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	cin >> N >> M;
	table.assign(N, vector<short>(M, false));
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < M; j++) {
			cin >> table[i][j];
		}
	}

	//algorithm part
	int sec = 0;
	while (!isEmpty()) {
		AirVisit();
		Melting();
		sec += 1;
	}
	cout << sec;
	return 0;

}

{% endraw %}
```

