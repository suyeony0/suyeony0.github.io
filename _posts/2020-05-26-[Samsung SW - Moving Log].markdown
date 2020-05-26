---
layout: post
title: [Samsung SW - Moving Log]
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}
	﻿[199. [SAMSUNG SW – Moving Log]
	- this was a simulation problem to find the shortest path to move a log.
	- the log’s size is 3, I mean horizontally. so there was a few restriction. but those was okay.
	- I used BFS and visit array. but problem occurred when I got input.
	- I misread input format. After changing the way to get input. it worked properly.
	- see the code.
	#include<iostream>
	#include<vector>
	#include<queue>
	using namespace std;
	vector<vector<char>> table;
	int N;
	vector<int> start_pos(6, 0); //log's start position
	vector<int> end_pos(6, 0); //log's end position
	vector<vector<vector<bool>>> visit;
	bool horizon;
	int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };
	
	
	int BFS() {
		queue<vector<int>> que;//log's position , move count, horizon
		que.push(vector<int>{start_pos[0], start_pos[1], start_pos[2], start_pos[3], start_pos[4], start_pos[5], 0,horizon});
		visit[start_pos[2]][start_pos[3]][horizon] = true;
		while (!que.empty()) {
			int sx = que.front()[0]; int sy = que.front()[1]; int mx = que.front()[2]; int my = que.front()[3]; int ex = que.front()[4]; int ey = que.front()[5];
			int cnt = que.front()[6]; horizon = que.front()[7];
			//cout << sx << "," << sy << "," << mx << "," << my << "," << ex << "," << ey << "=="<<cnt<<endl;
			if (sx == end_pos[0] && sy == end_pos[1] && mx == end_pos[2] && my == end_pos[3] && ex == end_pos[4] && ey == end_pos[5]) return cnt;
			
			que.pop();
			//move
			for (int i = 0; i < 4; i++) {
				int nsx = sx + dir[i][0]; int nsy = sy + dir[i][1]; int nmx = mx + dir[i][0]; int nmy = my + dir[i][1]; int nex = ex + dir[i][0]; int ney = ey + dir[i][1];
				if (nsx >= 0 && nsy >= 0 && nex < N && ney < N && table[nsx][nsy] != '1' && table[nmx][nmy] != '1' && table[nex][ney] != '1' && visit[nmx][nmy][horizon] == false) {
					visit[nmx][nmy][horizon] = true;
					que.push(vector<int>{nsx, nsy, nmx, nmy, nex, ney, cnt + 1, horizon});
				}
			}
	
			//rotate
			if (horizon) {
				int nsx = mx - 1; int nex = mx + 1; int nsy = my; int ney = my;
				if (nsx >= 0 && nex < N && table[sx - 1][sy] != '1' && table[mx - 1][my] != '1' && table[ex - 1][ey] != '1' &&
					table[sx + 1][sy] != '1' && table[mx + 1][my] != '1' && table[ex + 1][ey] != '1' && visit[mx][my][false] == false) {
					visit[mx][my][false] = true;
					que.push(vector<int>{nsx, nsy, mx, my, nex, ney, cnt + 1, false});
				}
			}
			else {
				int nsx = mx; int nex = mx; int nsy = my - 1; int ney = my + 1;
				if (nsy >= 0 && ney < N && table[sx][sy - 1] != '1' && table[mx][my - 1] != '1' && table[ex][ey - 1] != '1'
					&& table[sx][sy + 1] != '1' && table[mx][my + 1] != '1' && table[ex][ey + 1] != '1' && visit[mx][my][true] == false) {
					visit[mx][my][true] = true;
					que.push(vector<int>{nsx, nsy, mx, my, nex, ney, cnt + 1, true});
				}
			}	
		}
		return 0;
	}
	
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
	
		//get input;
		cin >> N;
		table.assign(N, vector<char>(N, 0));
		visit.assign(N, vector<vector<bool>>(N, vector<bool>(2,false))); //horizon, vertical for log's middle position
		bool flag_start = true;
		bool flag_end = true;
		string input;
		for (int i = 0; i < N; i++ ) {
			cin >> input;
			for (int j = 0; j < N; j++) {
				table[i][j] = input[j];
				//start position
				if (flag_start && input[j] == 'B') {
					flag_start = false;
					if (j + 1 < N && input[j+1] == 'B') {
						horizon = true;
						start_pos[0] = start_pos[2] = start_pos[4] = i;
						start_pos[1] = j; start_pos[3] = j + 1; start_pos[5] = j + 2;
					}
					else {
						start_pos[0] = i; start_pos[2] = i + 1; start_pos[4] = i+2;
						start_pos[1] = start_pos[3] = start_pos[5] = j;
						horizon = false;
					}
				}
				//end position
				if (flag_end && input[j] == 'E') {
					flag_end = false;
					if (j + 1 < N && input[j+1] == 'E') {
						end_pos[0] = end_pos[2] = end_pos[4] = i;
						end_pos[1] = j; end_pos[3] = j + 1; end_pos[5] = j + 2;
					}
					else {
						end_pos[0] = i; end_pos[2] = i + 1; end_pos[4] = i + 2;
						end_pos[1] = end_pos[3] = end_pos[5] = j;
					}
				}
			}
		}
	
		//algorithm part
		int answer=BFS();
		cout << answer;
		return 0;
	
	
	}
	
	
{% endraw %}
