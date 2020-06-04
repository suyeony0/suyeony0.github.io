---
layout: post
title: [SAMSUNG SW Repeat - New Game 2]
date: 2020-6-4
description: txt to markdown
thumbnail: work1.jpg
categories: SAMSUNG_SW

# Information for the author block
author : Loui
---

﻿[27. SAMSUNG SW : New Game 2]
- It was a simulation problem. there were 3 colored shell : white, blue, red.
- Basic rule is if a horse move and a next shell has a horse, then the moving horse will be placed above the next shell’s horse.
- In case of white, a horse move to the shell with horses above itself.
- In case of blue or chess board, a horse move to opposite direction. if the opposite shell is also blue or out of chess board, stop.
- In  case of red, a horse move to the shell with horses above itself with reversed order.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<algorithm>

using namespace std;

int N, K;
vector<vector<int>> table;
vector<vector<vector<int>>> stk;
vector<vector<int>> horse; // order, x,y,dir
int dir[4][2] = { {0,1},{0,-1},{-1,0},{1,0} }; // r l n s


int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	cin >> N >> K;
	table.assign(N, vector<int>(N, 0));
	stk.assign(N, vector<vector<int>>(N, vector<int>()));
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < N; j++) {
			cin >> table[i][j];
		}
	}
	int q, w, e;
	horse.assign(K, vector<int>(3, 0));
	for (int i = 0; i < K; i++) {
		cin >>q>>w>>e;
		horse[i][0] = q-1; horse[i][1] = w-1; horse[i][2] = e - 1;
		stk[q-1][w-1].emplace_back(i);	
	}
	
	//algorithm part
	int answer = 0;
	bool flag = false;
	while (!flag) {
		if (answer > 1000) {
			answer = -1;
			break;
		}
		answer += 1;
		for (int i = 0; i < K; i++) {
			int x = horse[i][0]; int y = horse[i][1]; int d = horse[i][2];
			int nx = x + dir[d][0]; int ny = y + dir[d][1];

			if (nx < 0 || ny < 0 || nx >= N || ny >= N || table[nx][ny] == 2) { //blue or out of range
				if (d == 0) d = 1;
				else if (d == 1) d = 0;
				else if (d == 2) d = 3;
				else if (d == 3) d = 2;
				nx = x + dir[d][0]; ny = y + dir[d][1];
				horse[i][2] = d;
				if (nx < 0 || ny < 0 || nx >= N || ny >= N || table[nx][ny] == 2) {
					continue;
				}
			}
			if (table[nx][ny] == 0) {
				vector<int> temp;
				for (int j = stk[x][y].size() - 1; j >= 0; j--) {
					horse[stk[x][y][j]][0] = nx; horse[stk[x][y][j]][1] = ny;
					temp.emplace_back(stk[x][y][j]);
					if (stk[x][y][j] == i) break;
				}
				for (int j = temp.size() - 1; j >= 0; j--) {
					stk[nx][ny].emplace_back(temp[j]);
					stk[x][y].pop_back();
				} 
			}

			else if (table[nx][ny] == 1) {
				for (int j = stk[x][y].size() - 1; j >= 0; j--) {
					horse[stk[x][y][j]][0] = nx; horse[stk[x][y][j]][1] = ny;
					stk[nx][ny].emplace_back(stk[x][y][j]);
					if (stk[x][y][j] == i) break;
					stk[x][y].pop_back();
				}
				stk[x][y].pop_back();
			}
			if (stk[nx][ny].size() >= 4) {
				flag = true;
				break;
			}
		}
	}

	cout << answer;
	return 0;
}

{% endraw %}
```

