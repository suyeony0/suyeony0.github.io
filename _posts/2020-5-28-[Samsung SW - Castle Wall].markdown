---
layout: post
title: [Samsung SW - Castle Wall]
data: 2020-05-26
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}

	﻿[205. [SAMSUNG SW – Castle Wall]
	- this was so hard. they gave walls of the castle using numeric value, actually binary value!
	- so reaching the given condition was so hard.
	- I used BFS, and bit operation.
	- see the code.
	#include<iostream>
	#include<vector>
	#include<queue>
	#define max(a,b) a>b?a:b
	using namespace std;
	
	vector<vector<int>> table;
	int N, M;
	int dir[4][2] = { {0,-1} ,{-1,0},{0,1},{1,0} };
	vector<vector<bool>> visit;
	
	
	int BFS(int x, int y) {
		visit[x][y] = true;
		queue<vector<int>> que;
		que.push(vector<int>{x, y});
		int room_size = 1;
		while (!que.empty()) {
			x = que.front()[0]; y = que.front()[1];
			que.pop();
			int wall = 1;
			for (int i = 0; i < 4; i++) {
				int nx = x + dir[i][0]; int ny = y + dir[i][1];
				if ((table[x][y] & wall)!=wall) {
					if (nx >= 0 && ny >= 0 && nx < N && ny < M && visit[nx][ny] == false) {
						visit[nx][ny] = true;
						que.push(vector<int>{nx, ny});
						room_size += 1;
					}
				}
				wall*=2;
			}		
		}
		return room_size;
	}
	
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
	
		//get input
		cin >> M >> N;
		table.assign(N, vector<int>(M, 0));
		visit.assign(N, vector<bool>(M, false));
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < M; j++) {
				cin >> table[i][j];
			}
		}
		//algorithm part
		int num_of_rooms = 0;
		int max_size = 0;
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < M; j++) {
				if (visit[i][j] == false) {
					int temp = BFS(i,j);
					max_size = max(max_size, temp);
					num_of_rooms += 1;
				}
			}
		}
		
		int max_size2 = 0;
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < M; j++) {
				for (int k = 1; k <= 8; k *= 2) {
					if ((table[i][j]&k)==k) {
						visit.assign(N, vector<bool>(M, false));
						table[i][j] -= k;
						int temp = BFS(i, j);
						max_size2 = max(max_size2, temp);
						table[i][j] += k;
					}
				}
			}
		}
		cout << num_of_rooms << endl;
		cout << max_size << endl;
		cout << max_size2 << endl;
		
		return 0;
	}
	
	
{% endraw %}
