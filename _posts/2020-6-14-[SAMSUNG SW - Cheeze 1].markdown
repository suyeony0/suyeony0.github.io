---
layout: post
title: [SAMSUNG SW - Cheeze 1]
date: 2020-6-14
description: txt to markdown
thumbnail: work1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

[216. SAMSUNG SW : Cheeze 1]
- It was a simulation problem.
- Before make cheeze melt, I should determine shells that are adjacent to air.
- To do that, I used BFS.
- After that, for each shell, I checked whether it is cheeze and the shell is adjacent to air.
- if so, I pushed its x,y corrdinates to a stk. Finally, remove the shells.
- During Above operation, I also counted how many cheeze shells left.
- I spent 14 minutes and 19 seconds.
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
int num_of_cheeze = 0;

void AirVisit() {
	air.assign(N, vector<bool>(M, false));
	queue<vector<int>> que;
	que.push(vector<int>{0, 0});
	air[0][0] = true;
	while (!que.empty()) {
		int x = que.front()[0]; int y = que.front()[1]; que.pop();
		for (int d = 0; d < 4; d++) {
			int nx = x + dir[d][0]; int ny = y + dir[d][1];
			if (nx >= 0 && ny >= 0 && nx < N && ny < M && table[nx][ny] == 0 && air[nx][ny]==false) {
				air[nx][ny] = true;
				que.push(vector<int>{nx, ny});
			}
		}
	}
}

void Melting() {
	vector<pair<int, int>> stk;
	num_of_cheeze = 0;
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < M; j++) {
			if (table[i][j] == 1) {
				num_of_cheeze += 1;
				for (int d = 0; d < 4; d++) {
					int nx = i + dir[d][0]; int ny = j + dir[d][1];
					if (nx >= 0 && ny >= 0 && nx < N && ny < M && air[nx][ny] == true) {
						stk.emplace_back(make_pair(i, j));
						break;
					}
				}
			}
		}
	}
	for (pair<int, int> row : stk) {
		table[row.first][row.second] = 0;
	}
}

void PrintTable() {
	cout << endl;
	for (vector<short> row : table) {
		for (short i : row) cout << i << " ";
		cout << endl;
	}
	cout << endl;
}

bool isEmpty() {
	for (vector<short> row : table) {
		for (short i : row) if (i != 0) return false;
	}
	return true;
}

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	cin >> N >> M;
	table.assign(N, vector<short>(M, 0));
	
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < M; j++) {
			cin >> table[i][j];
		}
	}

	//algorithm part
	int sec = 0;
	while (true) {
		AirVisit();
		Melting();
		sec += 1;
		if (isEmpty()) break;
	}
	cout << sec << endl;
	cout << num_of_cheeze << endl;
	return 0;
}	


{% endraw %}
```

