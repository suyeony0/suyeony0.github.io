---
layout: post
title: [SAMSUNG SW Repeat - Bids Escape 2]
date: 2020-5-28
description: txt to markdown
thumbnail: breakfast-orange-lemon-oranges-large.jpg
categories: SAMSUNG_SW

# Information for the author block
author : Loui
---

```cpp
	[1. SAMSUNG SW : Bids Escape 2]
	- I spent 1 hour and half for this problem again!
	- it was hard to match the restriction for me.
	- see the code.
	#include<iostream>
	#include<vector>
	#include<queue>
	using namespace std;
	
	int N, M;
	vector<vector<char>> table;
	bool visit[12][12][12][12];
	int rx, ry, bx, by, ex, ey;
	int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };
	
	int BFS() {
		queue<vector<int>> que;
		que.push(vector<int>{rx, ry, bx, by,0});
		visit[rx][ry][bx][by] = true;
		while (!que.empty()) {
			rx = que.front()[0]; ry = que.front()[1]; bx = que.front()[2]; by = que.front()[3]; int cnt = que.front()[4];
			que.pop();
			if (cnt > 10) continue;
			for (int i = 0; i < 4; i++) {
				int nrx = rx; int nry = ry; int nbx = bx; int nby = by;
				bool flag = false;
				bool flag2 = false;
	
				while (nbx >= 0 && nby >= 0 && nbx < N && nby < M && table[nbx][nby] != '#') {
					nbx += dir[i][0]; nby += dir[i][1];
					if (nbx == ex && nby == ey) {
						flag2 = true;
						break;
					}
				}
				if (flag2) continue;
				if (table[nbx][nby] == '#') {
					nbx -= dir[i][0]; nby -= dir[i][1];
				}
	
				while (nrx>=0 && nry>=0 && nrx<N && nry<M && table[nrx][nry] != '#') {
					nrx += dir[i][0]; nry += dir[i][1];
					if (nrx == ex && nry == ey) {
						flag = true;
						break;
					}
				}
				if (flag && cnt < 10) return cnt + 1;
				if (table[nrx][nry] == '#') {
					nrx -= dir[i][0]; nry -= dir[i][1];
				} 
	
				if (nrx == nbx && nry == nby) {
					if (i == 0) {
						if (rx < bx) {
							nbx++;
						}
						else {
							nrx++;
						}
					}
					else if (i == 1) {
						if (ry < by) {
							nby++;
						}
						else {
							nry++;
						}
					}
					else if (i == 2) {
						if (rx > bx) {
							nbx--;
						}
						else {
							nrx--;
						}
					}
					else if (i == 3) {
						if (ry > by) {
							nby--;
						}
						else {
							nry--;
						}
					}
				}
				 
				if (visit[nrx][nry][nbx][nby] == false) {
					visit[nrx][nry][nbx][nby] = true;
					que.push(vector<int>{nrx, nry, nbx, nby, cnt + 1});
				}
			}
		
		}
		return -1;
	}
	
	
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
	
		//get input
		cin >> N >> M;
		table.assign(N, vector<char>(M, 0));
		string input;
		for (int i = 0; i < N; i++) {
			cin >> input;
			for (int j = 0; j < M; j++) {
				table[i][j] = input[j];
				if (input[j] == 'R') {
					rx = i; ry = j;
				}
				if (input[j] == 'B') {
					bx = i; by = j;
				}
				if (input[j] == 'O') {
					ex = i; ey = j;
				}
	
			}
		}
		
	
	
		//algorithm part;
		int answer = BFS();
		cout << answer;
		return 0;
	
	}
	
```
