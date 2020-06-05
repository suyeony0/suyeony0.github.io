---
layout: post
title: [SAMSUNG SW Repeat - Rotating Circle Board]
date: 2020-6-5
description: txt to markdown
thumbnail: building1.jpg
categories: SAMSUNG_SW

# Information for the author block
author : Loui
---

﻿[28. SAMSUNG SW : Rotating Circle Board]
- it was a simulation problem. even thought they gave us a circle board. we can represent it as a 2D array if we check y index’s range.
- To rotate the circle board, I calculated after rotating index first and rearragne the values following the indice.
- To remove adjacent values, I used BFS and visit 2D array.
- I Spent 35 minutes and 19 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<queue>
using namespace std;
int N, M, T;
vector<vector<int>> table;
vector<vector<int>> order;
bool flag = true;
int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };

void PrintTable() {
	cout << endl;
	for (vector<int> row : table) {
		for (int i : row) cout << i << " ";
		cout << endl;
	}
	cout << endl;
}

void Rotate(int i, int d, int k) {
	k = k % M;
	vector<int> temp(M,0);
	vector<int> temp_table = table[i];
	if (d == 0) { //clockwise
		for (int i = 0; i < M; i++) temp[i] = (i+k)%M; 
	}
	else { //anti clock-wise
		int t;
		for (int i = 0; i < M; i++) {
			t = i - k;
			if (t < 0) t = M + t;
			temp[i] = t;
		}
	}
	for (int j = 0; j < M; j++) table[i][temp[j]] = temp_table[j];
}

void Remove() {
	vector<vector<bool>> visit(N,vector<bool>(M,false));
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < M; j++) {
			if (table[i][j] != 0 && visit[i][j] == false) {
				int cur = table[i][j];
				queue<vector<int>> que;
				que.push(vector<int>{i, j});
				visit[i][j] = true;
				while (!que.empty()) {
					int x = que.front()[0]; int y = que.front()[1]; que.pop();
					for (int d = 0; d < 4; d++) {
						int nx = x + dir[d][0]; int ny = y + dir[d][1];
						if (ny >= M) ny = 0; else if (ny < 0) ny = M - 1;
						if (nx >= 0 && nx < N && visit[nx][ny]==false && table[nx][ny]==cur) {
							table[x][y] = 0;
							visit[nx][ny] = true;
							table[nx][ny] = 0;
							flag = false;
							que.push(vector<int>{nx, ny});
						}
					}
				}
			}
		}
	}
}

void Average() {
	int cnt = 0;
	double sum = 0;
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < M; j++) {
			if (table[i][j] == 0) continue;
			cnt += 1;
			sum += table[i][j];
		}
	}
	double average = sum / cnt;
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < M; j++) {
			if (table[i][j] == 0) continue;
			else if (table[i][j] > average) table[i][j] -= 1;
			else if (table[i][j] < average) table[i][j] += 1;
		}
	}
}

bool isEmpty() {
	for (vector<int> row : table) {
		for (int i : row) if (i != 0) return false;
	}
	return true;
}

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	cin >> N >> M >> T;
	table.assign(N, vector<int>(M, 0));
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < M; j++) {
			cin >> table[i][j];
		}
	}
	order.assign(T, vector<int>(3, 0));
	for (int i = 0; i < T; i++) {
		cin >> order[i][0] >> order[i][1] >> order[i][2];
	} 


	//algorithm part
	for (vector<int> row : order) {
		int x = row[0]; int d = row[1]; int k = row[2];
		for (int i = x-1; i < N; i += x) Rotate(i, d, k);
		flag = true;
		if (!isEmpty()) {
			Remove();
			if (flag) Average();
		}
	}

	int answer = 0;
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < M; j++) {
			answer += table[i][j];
		}
	}
	cout << answer;
	return 0;

}

{% endraw %}
```

