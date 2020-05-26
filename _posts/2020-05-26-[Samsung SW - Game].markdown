---
layout: post
title: [Samsung SW - Game]
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}
	﻿[190. [SAMSUNG SW – Game]
	- It was a typical simulation problem. but tricks were there.
	- First trick was we had to use memorization to avoid time limit abort.
	- Second trick was how to handle an infinite loop, I avoided infinite loop by recording all the path I passed earlier current shell. and then if next shell is in the record. It will be infinite.
	- I implemeted this using DFS.
	- see the code.
	#include<iostream>
	#include<vector>
	#include<set>
	#define max(a,b) a>b?a:b
	using namespace std;
	
	int N, M; //row_size, col_size
	vector<vector<char>> table;
	int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} }; // w a s d
	int answer = 0;
	set<pair<int, int>> visit;
	vector<vector<int>> shell_visit;
	bool flag = false;
	int DFS(int x, int y,int cnt) {
		if (shell_visit[x][y] != -1) {
			return cnt+shell_visit[x][y];
		}
		int move_num = table[x][y] - '0';
		int max_move = 1;
		for (int i = 0; i < 4; i++) {
			int nx = x + (dir[i][0] * move_num); int ny = y + (dir[i][1] * move_num);
			if (visit.find(make_pair(nx, ny)) != visit.end()) { // infinite loop
				flag = true;
				return 0;
			}
			visit.insert(make_pair(nx, ny));
			if (nx >= 0 && ny >= 0 && nx < N && ny < M && table[nx][ny] != 'H') {
				max_move = max(max_move, DFS(nx,ny,cnt+1)-cnt);
			}
			visit.erase(visit.find(make_pair(nx, ny)));
		}
		shell_visit[x][y] = max_move;
		return cnt+max_move;
	}
	
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
		//get input
		cin >> N >> M;
		table.assign(N, vector<char>(M, 0));
		shell_visit.assign(N, vector<int>(M, -1));
		string input_string;
		for (int i = 0; i < N; i++) {
			cin >> input_string;
			for (int j = 0; j < M; j++) table[i][j] = input_string[j];
		}
		//algorithm part
		answer=DFS(0, 0, 0);
		visit.insert(make_pair(0, 0));
		if (flag) cout << -1;
		else cout << answer;
		return 0;
	}
	
{% endraw %}
