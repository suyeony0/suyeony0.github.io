---
layout: post
title: [SAMSUNG SW - Gas Pipe]
date: 2020-6-18
description: txt to markdown
thumbnail: food1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

﻿[221. SAMSUNG SW – Gas Pipe]
- It has been such a long time I’ve met a time limit exceed.
- It was a simulation problem. I’ve struggle to reach the time limit.
- Checking whether all the pipe is used consumed lots of computational time.
- So I chagend the logic just to find a possible condition to put a pipe of a certain shape.
- First, Finding the stolen shell.
- Second, Checking a possible pipe to put the shell.
- I spent 2 hours and 40 minutes and 20 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>

using namespace std;

int N, M;
vector<vector<char>> table;

int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };
char answer;
int nx, ny,d;
void FindStartPosition(int& sx, int& sy) {
	//find start direction
	
	for (d = 0; d < 4; d++) {
		nx = sx + dir[d][0]; ny = sy + dir[d][1];
		if (nx >= 0 && ny >= 0 && nx < N && ny < M && table[nx][ny] != '.') {
			if (nx == sx) { //horizontal
				if (table[nx][ny] == '-' || table[nx][ny] == '+') break;
				else if (ny < sy && (table[nx][ny] == '1' || table[nx][ny] == '2')) break;
				else if (ny > sy && (table[nx][ny] == '2' || table[nx][ny] == '3')) break;
			}
			else { //vertical
				if (table[nx][ny] == '|' || table[nx][ny] == '+') break;
				else if (nx < sx && (table[nx][ny] == '1' || table[nx][ny] == '4')) break;
				else if (nx > sx && (table[nx][ny] == '2' || table[nx][ny] == '3')) break;
			}
		}
	}
	sx = nx; sy = ny;
}

void Move() {
	
	while (table[nx][ny] != 'Z' && table[nx][ny] != '.') {
		switch (table[nx][ny]) {
		case '-':
			if (d == 1) ny -= 1;
			else if (d == 3) ny += 1;
			else return;
			break;
		case '|':
			if (d == 0) nx -= 1;
			else if (d == 2) nx += 1;
			else return;
			break;
		case '+':
			if (d == 0) nx -= 1;
			else if (d == 2) nx += 1;
			else if (d == 1) ny -= 1;
			else if (d == 3) ny += 1;
			else return;
			break;
		case '1':
			if (d == 1) {
				nx += 1;
				d = 2;
			}
			else if (d == 0) {
				ny += 1;
				d = 3;
			}
			else return;
			break;
		case '2':
			if (d == 2) {
				ny += 1;
				d = 3;
			}
			else if (d == 1) {
				nx -= 1;
				d = 0;
			}
			else return;
			break;
		case '3':
			if (d == 3) {
				nx -= 1;
				d = 0;
			}
			else if (d == 2) {
				ny -= 1;
				d = 1;
			}
			else return;
			break;
		case '4':
			if (d == 3) {
				nx += 1;
				d = 2;
			}
			else if (d == 0) {
				ny -= 1;
				d = 1;
			}
			else return;
			break;
		}
	}
}


void FindPipe() {
	vector<bool> around(4, false);
	int x = nx; int y = ny;
	for (int d = 0; d < 4; d++) {
		nx = x + dir[d][0]; ny = y + dir[d][1];
		if (nx >= 0 && ny >= 0 && nx < N && ny < M && table[nx][ny] != '.') {
			if (d == 0 && (table[nx][ny] == '|' || table[nx][ny] == '+' || table[nx][ny] == '1' || table[nx][ny] == '4')) around[d] = true;
			else if(d==2 && (table[nx][ny] == '|' || table[nx][ny] == '+' || table[nx][ny] == '2' || table[nx][ny] == '3')) around[d] = true;
			else if (d == 1 && (table[nx][ny] == '-' || table[nx][ny] == '+' || table[nx][ny] == '1' || table[nx][ny] == '2')) around[d] = true;
			else if (d == 3 && (table[nx][ny] == '-' || table[nx][ny] == '+' || table[nx][ny] == '3' || table[nx][ny] == '4')) around[d] = true;
		}
	}
	if (around[0] && around[1] && around[2] && around[3]) answer = '+';
	else if (around[0] && around[1]) answer = '3';
	else if (around[0] && around[3]) answer = '2';
	else if (around[2] && around[1]) answer = '4';
	else if (around[2] && around[3]) answer = '1';
	else if (around[0] && around[2]) answer = '|';
	else if (around[1] && around[3]) answer = '-';
}



int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	cin >> N >> M;
	table.assign(N, vector<char>(M, 0));
	int sx, sy, dx, dy;
	string input;
	for (int i = 0; i < N; i++) {
		cin >> input;
		for (int j = 0; j < M; j++) {
			table[i][j] = input[j];
			if (table[i][j] == 'M') {
				sx = i; sy = j;
			}
			if (table[i][j] == 'Z') {
				dx = i; dy = j;
			}
		}
	}

	//algorithm part

	int csx, csy;
	FindStartPosition(sx, sy);
	Move();
	csx = nx; csy = ny;
	FindPipe();
	cout << csx + 1 << " " << csy + 1 << " " << answer << endl;
	return 0;

}

{% endraw %}
```

