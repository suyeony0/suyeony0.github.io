---
layout: post
title: [Samsung SW - Pool]
data: 2020-05-26
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}

	﻿[191. [SAMSUNG SW – Pool]
	- it has been quite long time since I met this kind of a high level problem.
	- it was a simulation problem. but it was hard to make it satisfy all the rule.
	- I started sied of the pool from 1. if I met less value than current considering value, plus 1 to the shell using BFS.
	- that’s meaning is that if we can reach from side with current value, we don’t need to care to fill water.
	- so after that, with traveling all the shell, if we meet less value than current considering value, that is we can’t reach from side. so add 1 to answer value and make the shell plused 1.
	- see the code.
	#include<iostream>
	#include<vector>
	#include <queue>
	#define max(a,b) a>b?a:b
	using namespace std;
	
	int N, M; //<= 50
	vector<vector<int>> table;
	int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };
	int max_wall = 0;
	
	void BFS(int height) {
		queue<pair<int, int>> que;
		que.push(make_pair(0, 0));
		table[0][0] = height;
		while (!que.empty()) {
			int x = que.front().first; int y = que.front().second; que.pop();
			for (int i = 0; i < 4; i++) {
				int nx = x + dir[i][0]; int ny = y + dir[i][1];
				if (nx >= 0 && ny >= 0 && nx <= N + 1 && ny <= M + 1 && table[nx][ny]<height) {
					table[nx][ny] = height;
					que.push(make_pair(nx, ny));
				}
			}
		}
	}
	
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
		int answer = 0;
		//get input
		cin >> N >> M;
		table.assign(N+2, vector<int>(M+2, 0));
		
		string input;
		for (int i = 1; i <= N; i++) {
			cin >> input;
			for (int j = 0; j < M; j++) {
				table[i][j+1] = input[j] - '0';
				max_wall = max(max_wall, input[j]-'0');
			} 
		}
		//algorithm part;
		for (int h = 1; h <= max_wall; h++) {
			BFS(h);
			for (int i = 1; i <= N; i++) {
				for (int j = 1; j <= M; j++) {
					if (table[i][j] < h) {
						answer++;
						table[i][j]++;
					}
				}
			}
		}
		cout << answer;
		return 0;
	}
	
{% endraw %}
