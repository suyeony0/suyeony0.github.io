---
layout: post
title: [Samsung SW - Making Maze]
date: 2020-5-29
description: txt to markdown
thumbnail: work1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

```cpp

{% raw %}

	﻿[194. [SAMSUNG SW – Making Maze]
	- this was a simulation problem with a different start position.
	- if player move over the limit of array, he can’t make a maze.
	- during finishing all the given move, if player have been in the array. it’s a valid maze.
	- so I make 50 x 50 array, and give a different start position for each iteration.
	- see the code.
	#include<iostream>
	#include<vector>
	#define max(a,b) a>b ? a:b
	#define min(a,b) a>b ? b:a
	using namespace std;
	
	int N;
	int dir[4][2] = { {1,0}, {0,-1},{-1,0},{0,1} }; // s w n e
	string input;
	vector<vector<char>> table;
	
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
	
		//get input
		cin >> N>>input;
		bool flag = false;
		int ml, mr, mt, mb;
		for (int i = 0; i < 50; i++) {
			if (flag) break;
			for (int j = 0; j < 50; j++) {
				if (flag) break;
				flag = true;
				table.assign(50, vector<char>(50, '#'));
				// allocate start position
				table[i][j] = '.';
				int cur_x = i; int cur_y = j;
				int cur_dir = 0;
				ml = j; mr = 0; mt = i; mb = 0;
				//take move
				for (int k = 0; k < N; k++) {
					char cur_move = input[k];
					switch (cur_move){
					case 'L':
						cur_dir--;
						if (cur_dir < 0) cur_dir = 3;
						break;
					case 'R':
						cur_dir = (cur_dir+1) % 4;
						break;
					case 'F':
						cur_x = cur_x + dir[cur_dir][0]; cur_y = cur_y + dir[cur_dir][1];
						if (cur_x < 0 || cur_y < 0 || cur_x >= 50 || cur_y >= 50) {
							flag = false;
							break;
						}
						table[cur_x][cur_y] = '.';
						break;
					}
					
					ml = min(ml, cur_y); mr = max(mr, cur_y);
					mt = min(mt, cur_x); mb = max(mb, cur_x);
				}
			}
		}
		for (int i = mt; i <= mb; i++) {
			for (int j = ml; j <= mr; j++) {
				cout << table[i][j];
			}
			cout << endl;
		}
		return 0;
	}
	
	
{% endraw %}
```

