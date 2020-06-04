---
layout: post
title: [SAMSUNG SW Repeat - Fishing King]
date: 2020-6-4
description: txt to markdown
thumbnail: city2.jpg
categories: SAMSUNG_SW

# Information for the author block
author : Loui
---

﻿[23. SAMSUNG SW : Fishing King]
- It was a simulation problem. To reach the time limit, I had to use a trick.
- Each shark has their own direcition and speed. Futhermore, the given area is restricted.
- so we can calcluate a shark’s future position int a certain extent.
- like if a shark’s direction is north and speed is “s” then, the shark will be at start position with
opposite direction after (x * 2) move, x is the shark’s row position.
- I spent 1 hour and 5 minutes.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<map>
using namespace std;

int N, M, K; // row col num of shark
vector<vector<vector<int>>> table;
int answer = 0;
int dir[4][2] = { {-1,0},{1,0},{0,1},{0,-1} };


void printTable() {
	cout << endl;
	for (vector<vector<int>> row : table) {
		for (vector<int> i : row) {
			if (i.empty()) cout << "0" << " ";
			else cout << i[2] << " ";
		} 
		cout << endl;
	}
	cout << endl;
}

void GetShark(int y) {
	for (int i = 0; i < N; i++) {
		if (table[i][y].size() != 0) {
			answer += table[i][y][2]; //size
			table[i][y].clear();
			break;
		}
	}
}

void Move(map<pair<int, int>, vector<int>>& stk, int x, int y, int s, int d, int z) {
	
	int os = s;
	while ((d==0&&x*2<s) ||(d==1 &&((N-1-x)*2<s))) {
		if (d == 0) {
			s -= (x*2);
			d = 1;
		}
		else {
			s -= (N - 1 - x) * 2;
			d = 0;
		}
	}
	while ((d == 2 && ((M - 1 - y) * 2) < s) || (d == 3	&& y * 2 < s) ) {
		if (d == 2) {
			s -= (M - 1 - y) * 2;
			d = 3;
		}
		else {
			s -= y * 2;
			d = 2;
		}
	}
	for (int i = 0; i < s; i++) {
		x = x + dir[d][0]; y = y + dir[d][1];
		if (x < 0) {
			d = 1;x = 1;
		}	
		else if (y < 0) {
			d = 2; y = 1;
		}
		else if (x >= N) {
			d = 0; x = N - 2;
		}
		else if (y >= M) {
			d = 3; y = M - 2;
		}
	}
	if (stk.find(make_pair(x, y)) == stk.end()) stk[make_pair(x, y)] = vector<int>{os,d,z};
	else if (stk[make_pair(x, y)][2] >= z) return;
	else stk[make_pair(x, y)] = vector<int>{ os,d,z };
}

void MoveShark() {
	map<pair<int, int>, vector<int>> stk = {};
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < M; j++) {
			if (!table[i][j].empty()) {
				Move(stk, i, j, table[i][j][0], table[i][j][1], table[i][j][2]);
				table[i][j] = vector<int>{};
			}
		}	
	}
	for (map<pair<int, int>, vector<int>>::iterator iter = stk.begin(); iter != stk.end(); iter++) 
		table[iter->first.first][iter->first.second] = vector<int>{ iter->second[0],iter->second[1],iter->second[2] };
}

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	cin >> N >> M >> K;
	table.assign(N, vector<vector<int>>(M, vector<int>()));
	int a, b, c, d, e;
	for (int i = 0; i < K; i++) {
		cin >> a >> b >> c >> d >> e;
		table[a - 1][b - 1] = vector<int>{ c,d-1,e }; //speed direction size
	}

	//algorithm part
	
	for (int j = 0; j < M; j++) {
		GetShark(j);
		//printTable();
		if (j == M - 1) break;
		MoveShark();
		//printTable();
	}
	cout << answer;
	return 0;
}

{% endraw %}
```

