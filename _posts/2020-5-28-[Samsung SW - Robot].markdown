---
layout: post
title: [Samsung SW - Robot]
date: 2020-5-28
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}

	﻿[197. [SAMSUNG SW – Robot]
	- It was a simulation problem with some restriction.
	- we have to maintain 3D boolean visit array to check whether we visit the shell with a certain direction.
	- by maintaining visit array, we don’t need to turn the robot 180 degree at one time. it’s the key point.
	- In this kind of simulation problem, memozation is always the hardest point to implement and to come up with.
	- I used BFS using queue.
	- see the code.
	#include<iostream>
	#include<vector>
	#include<queue>
	#include<cmath>
	using namespace std;
	
	int N, M;
	vector<vector<int>> table;
	vector<vector<vector<bool>>> visit;
	vector<int> start_pos(3);
	vector<int> end_pos(3);
	int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };//wasd
	vector<int> rotation = { -1,1 }; //left right back
	
	vector<pair<int, int>> afterPos(int x, int y, int d) {
		vector<pair<int, int>> res;
		for (int i = 1; i <= 3; i++) {
			int nx = x + (dir[d][0] * i); int ny = y + (dir[d][1] * i);
			if (nx < 0 || ny < 0 || nx >= N || ny >= M || table[nx][ny] != 0 ) return res;
			res.emplace_back(make_pair(nx, ny));
		}
		return res;
	}
	
	inline int dirChange(int d) {
		if (d == 1) return 3;
		else if (d == 2) return 1;
		else if (d == 3) return 2;
		else if (d == 4) return 0;
	}
	
	int BFS() {
		queue<vector<int>> que;
		que.push(vector<int>{start_pos[0]-1, start_pos[1]-1, start_pos[2], 0});
		visit[start_pos[0] - 1][start_pos[1] - 1][start_pos[2]] = true;
		int answer = 987654321;
		while (!que.empty()) {
			int x = que.front()[0];  int y = que.front()[1]; int d = que.front()[2]; int sum = que.front()[3];
			//cout << " x : " << x << " y : " << y << " dir : " << d << " sum : " << sum << endl;
			que.pop();
			if (x == end_pos[0] - 1 && y == end_pos[1] - 1 && d == end_pos[2]) {
				answer = min(answer, sum);
				continue;
			}
			for (int r : rotation) {
				int nd = d + r;
				if (nd < 0) nd = 3;
				else if (nd == 4) nd = 0;
				if (visit[x][y][nd] == false) {
					visit[x][y][nd] = true;
					que.push(vector<int>{x, y, nd, sum + abs(r)});
				} 
			}
			
			vector<pair<int, int>> temp = afterPos(x, y, d);
			for (pair<int, int> res : temp) {
				if (visit[res.first][res.second][d] == false) {
					visit[res.first][res.second][d] = true;
					que.push(vector<int>{res.first, res.second, d, sum + 1});
				} 
			}
		}
		return answer;
	}
	
	
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
	
		//get input
		cin >> N >> M;
		table.assign(N, vector<int>(M, 0));
		visit.assign(N, vector<vector<bool>>(M,vector<bool>(4,false)));
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < M; j++) {
				cin >> table[i][j];
			}
		}
		cin >> start_pos[0] >> start_pos[1] >> start_pos[2];
		cin >> end_pos[0] >> end_pos[1] >> end_pos[2];
	
		//algorithm part
		start_pos[2] = dirChange(start_pos[2]);
		end_pos[2] = dirChange(end_pos[2]);
	
		int answer=BFS();
		cout << answer;
		return 0;
	}
	
	
	
	
{% endraw %}
