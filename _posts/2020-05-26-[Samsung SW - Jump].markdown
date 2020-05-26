---
layout: post
title: [Samsung SW - Jump]
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

	﻿[198. [SAMSUNG SW – Jump]
	- Recently, I’ve been solving lots of simulation problem. so this problem was easy for me.
	- I used DFS since I had to find all the path to end position and for that DFS using memozation is the easiest way, I think.
	- a precaution is the answer can be 2^63 – 1. so I used unsigned long long data type.
	- see the code.
	#include<iostream>
	#include<vector>
	
	using namespace std;
	
	int dir[2][2] = { {1,0},{0,1} };
	vector<vector<int>> table;
	vector<vector<unsigned long long>> memo;
	vector<vector<bool>> visit;
	int N;
	
	unsigned long long DFS(int x, int y) {
		if (x == N - 1 && y == N - 1) return 1;
		if (memo[x][y] != -1) return memo[x][y];
		if (table[x][y] == 0) return 0;
	
		unsigned long long res = 0;
		for (int i = 0; i < 2; i++) {
			int nx = x + (dir[i][0]*table[x][y]); int ny = y + (dir[i][1]*table[x][y]);
			if (nx >= 0 && ny >= 0 && nx < N && ny < N&&visit[nx][ny]==false) {
				visit[nx][ny] = true;
				res+=DFS(nx, ny);
				visit[nx][ny] = false;
			}
		}
		memo[x][y] = res;
		return res;
	}
	
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
	
		//get input
		cin >> N;
		table.assign(N, vector<int>(N, 0));
		visit.assign(N, vector<bool>(N, false));
		memo.assign(N, vector<unsigned long long>(N, -1));
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < N; j++) {
				cin >> table[i][j];
			}
		}
	
		//algorithm part;
		visit[0][0] = true;
		unsigned long long answer = DFS(0,0);
		cout << answer;
		return 0;
	
	}
	
