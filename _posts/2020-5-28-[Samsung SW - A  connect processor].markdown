---
layout: post
title: [Samsung SW - A  connect processor]
date: 2020-5-28
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}

	﻿[98. [Samsung SW – A : connect processor]]
	- I spent almost 5 hours for debugging…
	- see the code.
	#include<iostream>
	#include<vector>
	#include<climits>
	
	using namespace std;
	
	vector<vector<int>> drawTable(int cur_size, vector<pair<int, int>>& position,int& chips) {
		vector<vector<int>> table(cur_size, vector<int>(cur_size, 0));
		int c;
		for (int i = 0; i < cur_size; i++) {
			for (int j = 0; j < cur_size;) {
				cin >> c;
				if (c == 0 || c == 1) {
					table[i][j] = c;
					if ((i == 0 || j == 0 || i == cur_size - 1 || j == cur_size - 1) && c==1) {
						chips++;
					}
					else if (c == 1) {
						position.push_back(make_pair(i, j));
					}
					j++;
						
	
				}
			}
		}
		return table;
	}
	
	void printTable(vector<vector<int>> table) {
		int cur_size = table.size();
		for (int i = 0; i < cur_size; i++) {
			for (int j = 0; j < table[i].size(); j++) {
				cout << table[i][j];
			}
			cout << endl;
		}
	}
	
	vector<int> DFS(vector<vector<int>> table, vector<pair<int, int>>& position, int connect,int check, int lines,int numChips,int cur_size) {
	
		if (check ==numChips) {
			return { connect,lines };
		}
		bool flag = false;
		vector<vector<int>> temp = table;
		int x = position[check].first;
		int y = position[check].second;
		vector<int> res = { 0,100 };
		vector<int> cur = { 0,100 };
		//north
		for (int i = x - 1; i >= -1; i--) {
			if (i < 0) {
				flag = true;
				
				res = DFS(temp, position, connect + 1, check+1,lines + x, numChips, cur_size);
				if (cur[0] < res[0]) {
					cur = res;
				}
				else if (cur[0] == res[0] && cur[1] > res[1])
					cur = res;
				break;
			}
			if (temp[i][y] == 0) temp[i][y] = 1;
			else break;
		}
		temp = table;
		//south
		for (int i = x + 1; i <= cur_size; i++) {
			if (i >= cur_size) {
				flag = true;
				
				res = DFS(temp, position, connect + 1, check+1, lines + cur_size - (x+1 ), numChips, cur_size);
				if (cur[0] < res[0]) {
					cur = res;
				}
				else if (cur[0] == res[0] && cur[1] > res[1]) 
						cur = res;
					
					
				break;
			}
			if (temp[i][y] == 0) temp[i][y] = 1;
			else break;
		}
		temp = table;
		//east
		for (int i = y + 1; i <= cur_size; i++) {
			if (i >= cur_size) {
				flag = true;
				
				res = DFS(temp, position, connect + 1, check + 1, lines + cur_size - (y+1), numChips, cur_size);
				if (cur[0] < res[0]) {
					cur = res;
				}
				else if (cur[0] == res[0] && cur[1] > res[1])
					cur = res;
					
				break;
			}
			if (temp[x][i] == 0) temp[x][i] = 1;
			else break;
		}
		temp = table;
		//west
		for (int i = y - 1; i >= -1; i--) {
			if (i < 0) {
				flag = true;
				
				res = DFS(temp, position, connect + 1, check + 1, lines + y, numChips, cur_size);
				if (cur[0] < res[0]) {
					cur = res;
				}
				else if (cur[0] == res[0] && cur[1] > res[1])
					cur = res;
					
				break;
			}
			if (temp[x][i] == 0) temp[x][i] = 1;
			else break;
		}
		
	
		if (!flag) {
			cur = DFS(temp, position, connect, check + 1, lines,  numChips, cur_size);
		}
		return { cur[0],cur[1] };
	
	}
	
	int main(int argc, char** argv) {
		int test_case;
		int T;
		cin >> T;
		int cur_size;
		string cur_row;
		int chips=0;
		vector<int> answer;
		for (test_case = 1; test_case <= T; ++test_case) {
			cin >> cur_size;
			vector<pair<int, int>> position;
			chips = 0;
			vector<vector<int>> table = drawTable(cur_size, position,chips);
			//printTable(table);
			answer = DFS(table, position, chips, 0,0,cur_size-chips, cur_size);
			cout << "#" << test_case << " " << answer[1] << endl;
		}
		return 0;//정상종료시 반드시 0을 리턴해야합니다.
	}	
	
{% endraw %}
