---
layout: post
title: [SAMSUNG SW - Juvenile Shark]
date: 2020-6-16
description: txt to markdown
thumbnail: work1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

﻿[219. SAMSUNG SW : Juvenile Shark]
- It was a simulation problem.
- I thought it was easy, actually until now. but I’ve trapped by something so I took so much time.
- the trap was syncronizing fish’s position with table.
- I had used fish’s position vector as global variable. So the program didn’t work well.
- To find this trap, I spent so much time :(
- I didn’t’ used BFS. Because of that, I think I devoured much time
- I spent 2 hours and half or so.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<array>
#include<algorithm>
#define max(a,b) a>b?a:b

using namespace std;

array<array <int, 2>, 8> dir = { { {-1,0},{-1,-1},{0,-1},{1,-1},{1,0},{1,1},{0,1},{-1,1} } };
vector<bool> visit(16,false);


int answer = 0;

void PrintTable(vector<vector<int>>& table) {
	cout << endl;
	for (vector<int> row : table) {
		for (int i : row) cout << i+1 << " ";
		cout << endl;
	}
	cout << endl;
}

void FishSwap(vector<vector<int>>& table, vector<vector<int>>& fish, int a, int b) {
	int ax = fish[a][2]; int ay = fish[a][3]; int bx = fish[b][2]; int by = fish[b][3];
	fish[a][2] = bx; fish[a][3] = by; fish[b][2] = ax; fish[b][3] = ay;
	table[ax][ay] = b; table[bx][by] = a;
}

void MoveFish(vector<vector<int>>& table,vector<vector<int>>& fish, int sx, int sy) {
	for (int f = 0; f < 16; f++) {
		if (visit[f] == true) continue;
		int x = fish[f][2]; int y = fish[f][3]; int d = fish[f][1];
		int rotate_num = 0;
		while (rotate_num<8) {
			int nx = x + dir[d][0]; int ny = y + dir[d][1];
			if (nx < 0 || ny < 0 || nx >= 4 || ny >= 4 || (sx == nx && sy == ny)) {
				d = (d + 1) % 8;
				rotate_num += 1;
				continue;
			}
			else {
				FishSwap(table,fish, f, table[nx][ny]);
				fish[f][1] = d;
				break;
			}
			
		}
		
	}
}

void MoveShark(vector<vector<int>> table,vector<vector<int>> fish,int sx, int sy, int sd, int sum,int cnt ) {
	MoveFish(table,fish,sx,sy);
	int nx = sx + dir[sd][0]; int ny = sy + dir[sd][1];
	while (nx >= 0 && ny >= 0 && nx < 4 && ny < 4 ) {
		if (visit[table[nx][ny]] == false) {
			visit[table[nx][ny]] = true;
			MoveShark(table, fish, nx, ny, fish[table[nx][ny]][1], sum + table[nx][ny] + 1, cnt + 1);
			visit[table[nx][ny]] = false;
		}
		nx = nx + dir[sd][0]; ny = ny + dir[sd][1];
	}
	answer = max(answer, sum);
}


int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);
	
	//get input
	vector<vector<int>> table(4, vector<int>(4, 0));
	vector<vector<int>> fish(16, vector<int>(4, 0));
	for (int i = 0; i < 4; i++) {
		for (int j = 0; j < 4; j++) {
			cin >> fish[4 * i + j][0] >> fish[4 * i + j][1];
			fish[4 * i + j][0] -= 1;
			fish[4 * i + j][1] -= 1; //dir index starts at 0.
			fish[4 * i + j][2] = i; fish[4 * i + j][3] = j; //x y position
			table[i][j] = fish[4 * i + j][0];
		}
	}
	visit[fish[0][0]] = true;
	
	//algorithm part
	int sx = 0; int sy = 0;
	int sd;	int sum = 0;
	sd = fish[0][1]; sum = fish[0][0] + 1;
	sort(fish.begin(), fish.end()); //sort by number
	MoveShark(table,fish,sx,sy,sd,sum,0);
	cout << answer;
	return 0;
}


{% endraw %}
```

