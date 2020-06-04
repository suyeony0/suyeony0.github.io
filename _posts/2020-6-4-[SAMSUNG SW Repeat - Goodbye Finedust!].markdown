---
layout: post
title: [SAMSUNG SW Repeat - Goodbye Finedust!]
date: 2020-6-4
description: txt to markdown
thumbnail: breakfast-orange-lemon-oranges-large.jpg
categories: SAMSUNG_SW

# Information for the author block
author : Loui
---

﻿[22. SAMSUNG SW : Goodbye Finedust!]
- it was a weird problem. I will tell you later.
- it was a simulation problem. 
- there was an airconditioner and I had to implement the way that the airconditioner clean air. 
- it was not that hard. but the weird thing occurred.
- as you can see below code. there is a comment block that is an original function Contation I maded.
- and there is anoter Contagion function that has a code of resetting 2D array and reallocate dust value.
- we usually can think that the comment block’s Contagion function would be faster than the other.
- since there is no resetting of 2D array.
- but when I submitted the code. the former one was stucked by time limit exceeded.
- Surpisingly, the latter one passed. what the heck?
- Even now, my brain doesn’t understand why those things happened.
- Because of above reason, I spent quite long time. I spent 53 minutes and 44 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>

using namespace std;

int N, M, T;
int tx, bx;
vector<vector<int>> table;
int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };

/*
void Contagion() {
	vector<vector<int>> stk;
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < M; j++) {
			if (table[i][j] > 0) {
				int res5 = table[i][j] / 5;
				int num_of_contagion = 0;
				for (int d = 0; d < 4; d++) {
					int x = i + dir[d][0]; int y = j + dir[d][1];
					if (x >= 0 && y >= 0 && x < N && y < M && table[x][y] != -1) {
						stk.emplace_back(vector<int>{x, y, res5});
						num_of_contagion += 1;
					}
				}
				table[i][j] -= (res5 * num_of_contagion);
			}
		}
	}
	for (vector<int> row : stk) table[row[0]][row[1]] += row[2];
}
*/

void Contagion() {
	vector<vector<int>> new_dust;
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < M; j++) {
			int x = i; int y = j;
			if (table[x][y] == -1) continue;
			int count = 0;
			if (table[x][y] > 0) {
				for (int i = 0; i < 4; i++) {
					int tx = x + dir[i][0]; int ty = y + dir[i][1];
					if (tx >= 0 && ty >= 0 && tx < N && ty < M && table[tx][ty] != -1) {
						new_dust.push_back(vector<int>{tx, ty, table[x][y] / 5});
						count++;
					}
				}
			}
			table[x][y] -= (table[x][y] / 5) * count;
			if (table[x][y] != 0) new_dust.push_back(vector<int>{x, y, table[x][y]});
		}
	}
	table = vector<vector<int>>(N, vector<int>(M));
	table[tx][0] = -1; table[bx][0] = -1;
	for (vector<int> pos : new_dust) table[pos[0]][pos[1]] += pos[2];
}


void Cleaning() {
	//top - AntiClockWise
	int x = tx; int y = 0;
	for (int i = x-1; i >= 1; i--) table[i][0] = table[i - 1][0];
	for (int j = 0; j < M - 1; j++) table[0][j] = table[0][j + 1];
	for (int i = 0; i <= x - 1; i++) table[i][M - 1] = table[i + 1][M - 1];
	for (int j = M - 1; j >= y + 1; j--) {
		table[x][j] = table[x][j - 1];
	} 
	table[x][y + 1] = 0;
		
	//bottom - ClockWise
	x = bx;
	for (int i = x+1; i < N - 1; i++) table[i][0] = table[i + 1][0];
	for (int j = 0; j < M - 1; j++) table[N - 1][j] = table[N - 1][j + 1];
	for (int i = N - 1; i >= x + 1; i--) table[i][M - 1] = table[i - 1][M - 1];
	for (int j = M - 1; j >= y + 1; j--) table[x][j] = table[x][j - 1];
	table[x][y + 1] = 0;

}

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	cin >> N >> M >> T;
	table.assign(N, vector<int>(M, 0));
	bool flag = true;
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < M; j++) {
			cin >> table[i][j];
		}
	}
	for (int i = 0; i < N; i++) 
		if (table[i][0] == -1) {
		tx = i; bx = i + 1;
		break;
		}

	//algorithm part
	for (int t = 0; t < T; t++) {
		Contagion();
		Cleaning();
	}
	int answer = 2; //Airconditioner's position.
	for (vector<int> row : table) {
		for (int i : row) answer += i;
	}
	cout << answer;
	return 0;
}

{% endraw %}
```

