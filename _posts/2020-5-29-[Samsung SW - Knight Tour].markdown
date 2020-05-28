---
layout: post
title: [Samsung SW - Knight Tour]
date: 2020-5-29
description: txt to markdown
thumbnail: food1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

{% highlight c++ %}

{% raw %}

	﻿[193. [SAMSUNG SW – Knight Tour]
	- this problem was so easy for me. I just had to check the condition is possible or not.
	- I record possible end position using first postion and for each iteration, I checked a current position can be reached from previous position. that’s it.
	- once input ended. I checked all the shell is visited for sure.
	- Lastly, if end position is possible position to jump to start position, return true. Otherwise, return false.
	- see the code.
	#include<iostream>
	#include<vector>
	#include<map>
	using namespace std;
	
	vector<vector<bool>> table(6, vector<bool>(6, false));
	map<pair<int, int>, bool> end_pos;
	int dir[8][2] = { {-2,-1},{-1,-2},{-2,1},{-1,2},{2,-1},{1,-2},{2,1},{1,2} };
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
		//make end_pos
		string input;
		cin >> input;
		int col = input[0] - 'A'; int row = 6 - (input[1] - '0');
		table[row][col] = true;
		for (int i = 0; i < 8; i++) {
			int nx = row + dir[i][0]; int ny = col + dir[i][1];
			if (nx >= 0 && ny >= 0 && nx < 6 && ny < 6) {
				end_pos[make_pair(nx, ny)] = true;
			}
		}
		//get input and algorithm part
		int prev_row = row; int prev_col = col;
		for (int i = 0; i < 35; i++) {
			cin >> input;
			int col = input[0] - 'A'; int row = 6 - (input[1] - '0');
			bool flag = false;
			//to check whether the Knight can jump to current position from pre-position.
			for (int j = 0; j < 8; j++) {
				int nx = prev_row + dir[j][0]; int ny = prev_col + dir[j][1];
				if (nx >= 0 && ny >= 0 && nx < 6 && ny < 6 && nx == row && ny == col) {
					flag = true;
					break;
				} 
			}
			if (!flag || table[row][col]) { //if the Knight can not be current position or already visit current position, it's not valid.
				cout << "Invalid";
				return 0;
			}
			else {
				table[row][col] = true;
			}
			prev_row = row; prev_col = col;
		}
		// to check all the shell is visited.
		for (int i = 0; i < 6; i++) {
			for (int j = 0; j < 6; j++) {
				if (table[i][j] == false) {
					cout << "Invalid";
					return 0;
				}
			}
		}
		//to check whether the Knight can jump to start postion from last position
		col = input[0] - 'A'; row = 6 - (input[1] - '0');
		if (end_pos.find(make_pair(row, col)) != end_pos.end()) {	
			cout << "Valid";
			return 0;
		}
		else cout << "Invalid";
		return 0;
	
	}
	
{% endraw %}
{% endhighlight %}

