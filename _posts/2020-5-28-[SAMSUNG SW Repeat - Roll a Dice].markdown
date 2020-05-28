---
layout: post
title: [SAMSUNG SW Repeat - Roll a Dice]
date: 2020-5-28
description: txt to markdown
thumbnail: city2.jpg
categories: SAMSUNG_SW

# Information for the author block
author : Loui
---

{% raw %}

	[5. SAMSUNG SW ? Roll a Dice]
	- it was a simulation problem. implementing Dice was quite tricky. In my case, I made 4 x 3 array to represent the dice.
	- they gave us number of order to move the dice, but the diretions started with 1 not 0, so there was a small confusing.
	- I spent 22 minutes.
	- see the code.
	#include<iostream>
	#include<vector>
	
	using namespace std;
	
	int N, M,x,y,K;
	vector<vector<int>> table;
	vector<vector<int>> dice = { {0,0,0},{0,0,0},{0,0,0},{0,0,0} };
	vector<int> roll;
	int dir[4][2] = { {0,1},{0,-1},{-1,0},{1,0} }; // d a w s
	
	
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
	
		//get input
		cin >> N >> M>>x>>y>>K;
		table.assign(N, vector<int>(M, 0));
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < M; j++) {
				cin >> table[i][j];
			}
		}
		roll.assign(K, 0);
		for (int i = 0; i < K; i++) cin >> roll[i];
		
		//algorithm part
		for (int round = 0; round < K; round++) {
			int cur_dir = roll[round]-1;
			x = x + dir[cur_dir][0]; y = y + dir[cur_dir][1];
			if (x < 0 || y < 0 || x >= N || y >= M) {
				x -= dir[cur_dir][0]; y -= dir[cur_dir][1];
				continue;
			}
	
			//roll the dice
			int temp;
			switch (cur_dir){
			case 0://east
				temp = dice[1][0];
				dice[1][0] = dice[3][1];
				dice[3][1] = dice[1][2];
				dice[1][2] = dice[1][1];
				dice[1][1] = temp;
				break;
			case 1://west
				temp = dice[1][2];
				dice[1][2] = dice[3][1];
				dice[3][1] = dice[1][0];
				dice[1][0] = dice[1][1];
				dice[1][1] = temp;
				break;
			case 2://north
				temp = dice[0][1];
				dice[0][1] = dice[1][1];
				dice[1][1] = dice[2][1];
				dice[2][1] = dice[3][1];
				dice[3][1] = temp;
				break;
			case 3://south
				temp = dice[3][1];
				dice[3][1] = dice[2][1];
				dice[2][1] = dice[1][1];
				dice[1][1] = dice[0][1];
				dice[0][1] = temp;
				break;
			}
			if (table[x][y] == 0) table[x][y] = dice[3][1];
			else {
				dice[3][1] = table[x][y];
				table[x][y] = 0;
			}
			cout << dice[1][1]<<endl;
		}
		return 0;
	}
	
{% endraw %}
