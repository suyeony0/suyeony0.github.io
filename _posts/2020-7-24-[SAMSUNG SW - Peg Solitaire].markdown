---
layout: post
title: [SAMSUNG SW - Peg Solitaire]
date: 2020-7-24
description: txt to markdown
thumbnail: building1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

﻿[245. SAMSUNG SW – Peg Solitaire]
- It was DFS problem for a long time.
- For all the pin, we have to simulate all the possible move.
- I used DFS for backtracking.
- First, record all the pin’s position.
- Second, for each pin, move if possible. and revise the given board.
- Third, return a maximum DFS depth.
- I spent 25 minutes and 55 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<algorithm>
using namespace std;

const int N = 5;
const int M = 9;
const int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };
vector<vector<char>> table;
vector<vector<int>> pins;

int num_pin = 0;
int pin_size;
int answer;
void DFS(int cnt) {

	answer = max(answer, cnt);

	for (int i = 0; i < pin_size; i++) {
		int x = pins[i][0]; int y = pins[i][1];
		if (table[x][y] == '.') continue;
		for (int d = 0; d < 4; d++) {
			int nx = x + dir[d][0]; int ny = y + dir[d][1];
			int nnx = x + dir[d][0] * 2; int nny = y + dir[d][1] * 2;
			if (nnx<0 || nny<0 || nnx>=N || nny>=M) continue;
			if (table[nx][ny] == 'o' && table[nnx][nny] == '.') {
				table[x][y] = '.'; table[nx][ny] = '.'; table[nnx][nny] = 'o';
				pins[i][0] = nnx; pins[i][1] = nny;
				DFS(cnt + 1);
				pins[i][0] = x; pins[i][1] = y;
				table[x][y] = 'o'; table[nx][ny] = 'o'; table[nnx][nny] = '.';
			}
			
		}	
	}
}

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	int T;
	cin >> T;

	for (int t = 0; t < T; t++) {
		num_pin = 0;
		pins.clear();
		pins.shrink_to_fit();
		
		//get input
		table.assign(N, vector<char>(M, 0));
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < M; j++) {
				cin >> table[i][j];
				if (table[i][j] == 'o') {
					num_pin += 1;
					pins.emplace_back(vector<int>{i, j});
				} 
			}
		}
		pin_size = pins.size();
		answer = 0;
		//algorithm part
		DFS(0);
		cout << pin_size - answer <<" "<< answer << endl;
	}
}

{% endraw %}
```

