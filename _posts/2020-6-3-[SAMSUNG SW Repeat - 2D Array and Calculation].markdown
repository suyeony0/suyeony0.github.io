---
layout: post
title: [SAMSUNG SW Repeat - 2D Array and Calculation]
date: 2020-6-3
description: txt to markdown
thumbnail: food1.jpg
categories: SAMSUNG_SW

# Information for the author block
author : Loui
---

```cpp

{% raw %}

	﻿[22. SAMSUNG SW : 2D Array and Calculation]
	- it was a sorting problem. but it was quite hard.
	- since I had to re allocate 2D array’s size by increasing row or column’s size.
	- in terms of vector, columns size increasing is easy due to emplace or push_back, but row size increasing is not that easy. 
	- I used stable_sort in algorhtm header.
	- I spent 57 minutes and 9 seconds.
	- see the code.
	#include<iostream>
	#include<vector>
	#include<map>
	#include<algorithm>
	#define max(a,b) a>b?a:b
	using namespace std;
	
	int r, c, k;
	vector<vector<int>> table(3, vector<int>(3, 0));
	bool row_turn = true;
	
	void PrintTable() {
			cout << endl;
			for (vector<int> row : table) {
				for (int i : row) cout << i << " ";
				cout << endl;
			}
			cout << endl;
	}
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
	
		//get input
		cin >> r >> c >> k;
		r -= 1; c -= 1;
		for (int i = 0; i < 3; i++) {
			for (int j = 0; j < 3; j++) {
				cin >> table[i][j];
			}
		}
	
		//algorithm part
		int answer = 0;
		int row_size = 3;
		int col_size = 3;
		while (answer <= 101) {
			if (answer > 100) {
				answer = -1;
				break;
			}
			if (row_size>r && col_size >c &&table[r][c] == k) {
				break;
			}
			answer += 1;
			vector<vector<int>> n_table;
			int pre_row_size = row_size;
			int pre_col_size = col_size;
			if (row_turn) {
				vector<vector<pair<int, int>>> order(pre_row_size, vector<pair<int, int>>());
				for (int i = 0; i < pre_row_size; i++) {
					map<int, int> stk;
					for (int j = 0; j < pre_col_size; j++) {
						if (table[i][j] == 0) continue;
						stk[table[i][j]] += 1;
					}
					for (map<int, int>::iterator iter = stk.begin(); iter != stk.end(); iter++)
						order[i].emplace_back(make_pair(iter->first, iter->second));
					stable_sort(order[i].begin(), order[i].end(), [](pair<int, int> a, pair<int, int> b) {return a.second < b.second; });
					col_size = max(col_size, order[i].size() * 2);
				}
				if (col_size > 100) col_size = 100;
				n_table.assign(row_size, vector<int>(col_size, 0));
				for (int i = 0; i < row_size && i<100; i++) {
					for (int j = 0; j < order[i].size() && j<100; j++) {
						n_table[i][j*2] = order[i][j].first;
						n_table[i][(j * 2) + 1] = order[i][j].second;
					}
				}
			}
			else {
				vector<vector<pair<int, int>>> order(pre_col_size, vector<pair<int, int>>());;
				for (int j = 0; j < pre_col_size; j++) {
					map<int, int> stk;
					for (int i = 0; i < pre_row_size; i++) {
						if (table[i][j] == 0) continue;
						stk[table[i][j]] += 1;
					}
					for (map<int, int>::iterator iter = stk.begin(); iter != stk.end(); iter++)
						order[j].emplace_back(make_pair(iter->first, iter->second));
					stable_sort(order[j].begin(), order[j].end(), [](pair<int, int> a, pair<int, int> b) {return a.second < b.second; });
					row_size = max(row_size, order[j].size() * 2);
				}
				if (row_size > 100) row_size = 100;
				n_table.assign(row_size, vector<int>(col_size, 0));
				for (int j = 0; j < col_size && j<100; j++) {
					for (int i = 0; i < order[j].size() && i<100; i++) {
						n_table[i*2][j] = order[j][i].first;
						n_table[(i * 2) + 1][j] = order[j][i].second;
					}
	
				}
			}
			
			table = n_table;
			if (row_size >= col_size) row_turn = true;
			else row_turn = false;
	
			
		}
		cout << answer;
		return 0;
	}
	
{% endraw %}
```

