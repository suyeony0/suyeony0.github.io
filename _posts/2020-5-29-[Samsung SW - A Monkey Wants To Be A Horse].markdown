---
layout: post
title: [Samsung SW - A Monkey Wants To Be A Horse]
date: 2020-5-29
description: txt to markdown
thumbnail: food2.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}

	﻿[196. [SAMSUNG SW – A Monkey Wants To Be A Horse]
	- I tried to solve this problem using DFS and DP, but I failed. since there was K value that is the number of the monkey can move like the horse.
	- see the first code.
	#include<iostream>
	#include<vector>
	#define min(a,b) a>b? b:a
	using namespace std;
	
	vector<vector<int>> table;
	vector<vector<vector<int>>>visit;
	vector<vector<bool>> shell_visit;
	int K, N, M;
	int k_dir[8][2] = { {-1,-2},{-2,-1}, {-2,1},{-1,2},{1,2},{2,1},{2,-1},{1,-2} }; //left top start and clock-wise move.
	int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };//w a s d
	
	int DFS(int x,int y,int cnt) {
		if (visit[x][y][K] != -1) return visit[x][y][K];
		if (x == N - 1 && y == M - 1) return 0;
		
		if (x == 0 && y == 1) {
			cout << "K : "<< K << endl;
		} 
		
		int nx, ny;
		int res = 987654321;
		
		//Knight Move
		if (K > 0) {
			for (int i = 0; i < 8; i++) {
				nx = x + k_dir[i][0]; ny = y + k_dir[i][1];
				if (nx >= 0 && ny >= 0 && nx < N && ny < M && table[nx][ny] != 1 && shell_visit[nx][ny]==false) {
					shell_visit[nx][ny] = true;
					K -= 1;
					res= min(res,DFS(nx, ny,cnt+1)+1);
					K += 1;
					shell_visit[nx][ny] = false;
				}
			}
		}
	
		//Normal Move
		for (int i = 0; i < 4; i++) {
			nx = x + dir[i][0]; ny = y + dir[i][1];
			if (nx >= 0 && ny >= 0 && nx < N && ny < M && table[nx][ny] != 1 && shell_visit[nx][ny] == false) {
				shell_visit[nx][ny] = true;
				res = min(res, DFS(nx, ny, cnt + 1)+1);
				shell_visit[nx][ny] = false;
			}
		}
		if (K > 0)	visit[x][y][1] = res;
		else visit[x][y][0] = res;
		return res;
	}
	
	
	int main(){
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
	
		//get input
		cin >> K >> M >> N;
		table.assign(N, vector<int>(M, 0));
		shell_visit.assign(N, vector<bool>(M, false));
		visit.assign(N, vector<vector<int>>(M,vector<int>(K+1,-1)));
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < M; j++) {
				cin >> table[i][j];
			}
		}
	
		//algorithm part
		shell_visit[0][0] = true;
		int answer = 987654321;
		answer=DFS(0,0,0);
		if (answer == 987654321) cout << -1;
		else cout << answer;
		/*for (int i = 0; i < N; i++) {
			for (int j = 0; j < M; j++) {
				cout << endl << "i : " << i << " j :" << j << "   ";
				cout << visit[i][j][0] << " , " << visit[i][j][1] << endl;
			}
		}*/
		return 0;
	}
	
	- so I changed it to BFS.
	- BFS also has Memozation. I mean Dp. the reason why we can’t use DP in DFS but BFS is that when we use DP in DFS, a shell can be reached along different ways. so even if the shell’s k value is same, there is a probablity that it has a different res value.
	- Therefore, even if we visit a shell with a certain K value. we have to re-check the shell. so the visit array is useless.
	- However, BFS always find a shortest path from current shell. so there is no possible way to reach a certain shell with different path. so we can use DP.
	- see the code.
	#include<iostream>
	#include<vector>
	#include<queue>
	#define min(a,b) a>b? b:a
	using namespace std;
	
	vector<vector<int>> table;
	vector<vector<vector<bool>>>visit;
	vector<vector<bool>> shell_visit;
	int K, N, M;
	int k_dir[8][2] = { {-1,-2},{-2,-1}, {-2,1},{-1,2},{1,2},{2,1},{2,-1},{1,-2} }; //left top start and clock-wise move.
	int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };//w a s d
	
	int BFS(int x,int y, int k) {
		queue<vector<int>> que;
		que.push(vector<int>{x, y, 0,0});
		visit[x][y][0] = true;
		int res = 987654321;
		while (!que.empty()) {
			x = que.front()[0]; y = que.front()[1]; k = que.front()[2]; int sum = que.front()[3];
			que.pop();
	
			if (x == N - 1 && y == M - 1) {
				return sum;
			}
			if (K>k) {
				for (int i = 0; i < 8; i++) {
					int nx = x + k_dir[i][0]; int ny = y + k_dir[i][1];
					if (nx >= 0 && ny >= 0 && nx < N && ny < M && table[nx][ny] != 1 && visit[nx][ny][k+1] == false) {
						visit[nx][ny][k + 1] = true;
						que.push(vector<int>{nx, ny, k + 1, sum + 1});
					}
				}
			}
			for (int i = 0; i < 4; i++) {
				int nx = x + dir[i][0]; int ny = y + dir[i][1];
				if (nx >= 0 && ny >= 0 && nx < N && ny < M && table[nx][ny] != 1 && visit[nx][ny][k] == false) {
					visit[nx][ny][k] = true;
					que.push(vector<int>{nx, ny, k, sum + 1});
				}
			}
		}
	
	
		if (res == 987654321) return -1;
		return res;
	}
	
	
	int main(){
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
	
		//get input
		cin >> K >> M >> N;
		table.assign(N, vector<int>(M, 0));
		visit.assign(N, vector<vector<bool>>(M, vector<bool>(K + 1, false)));
		shell_visit.assign(N, vector<bool>(M, false));
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < M; j++) {
				cin >> table[i][j];
			}
		}
	
		//algorithm part
		shell_visit[0][0] = true;
		int answer = 987654321;
		answer=BFS(0,0,K);
		cout << answer;
		return 0;
	}
	
{% endhighlight %}
