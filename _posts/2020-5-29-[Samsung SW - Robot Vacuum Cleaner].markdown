---
layout: post
title: [Samsung SW - Robot Vacuum Cleaner]
date: 2020-5-29
description: txt to markdown
thumbnail: building1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

{% highlight c++ %}

{% raw %}

	﻿[109. [BACKJOON – SAMSUNG SW : Robot Vacuum Cleaner]]
	- this problem’s hardest point was to determine when cleaning is end.
	- without it, not that hard, just followed given rules.
	- see the code.
	#include<iostream>
	#include<fstream>
	#include<vector>
	using namespace std;
	
	pair<vector<vector<int>>,vector<int>> makeTable() {
		ifstream in("C:\\Users\\gjsgu\\Desktop\\Algorithm\\test_case\\test_case_for_robot_vacuum_cleaner.txt");
		int N, M;
		if (in.is_open()) {
			cout << "file is opened." << endl;
			in >> N; in >> M;
		}
		vector<vector<int>> table(N, vector<int>(M, 0));
		vector<int> pos(3, 0);
		for (int i = 0; i < 3; i++) in >> pos[i];
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < M; j++) {
				in >> table[i][j];
			}
		}
		return make_pair(table,pos);
	}
	
	pair<vector<vector<int>>, vector<int>> makeTable2() {
		int N, M;
		cin >> N; cin >> M;
		vector<vector<int>> table(N, vector<int>(M, 0));
		vector<int> pos(3, 0);
		for (int i = 0; i < 3; i++) cin >> pos[i];
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < M; j++) {
				cin >> table[i][j];
			}
		}
		return make_pair(table, pos);
	}
	
	
	void printTable(vector<vector<int>>& table) {
		for (vector<int> row : table) {
			for (int i : row) {
				cout << i << " ";
			}
			cout << endl;
		}
	}
	int is_end(vector<vector<int>>& table,vector<int>& pos) {
		int x = pos[0]; int y = pos[1];
		vector<vector<int>> dir = { {1,0},{0,-1},{-1,0},{0,1} }; //reverse of north east south west
		if ((x - 1 < 0 || table[x - 1][y])&& (y - 1 < 0 || table[x][y - 1])&& (x + 1 >= table.size() || table[x + 1][y])&& (y + 1 >= table[0].size() || table[x][y + 1])) {
			int cx = x + dir[pos[2]][0]; int cy = y + dir[pos[2]][1];
			if ((cx<0 || cx >= table.size() || cy < 0 || cy >= table[0].size() || table[cx][cy]==1)) return 1;
			return 2;
		}
		return 3;
	}
	
	int cleaning(vector<vector<int>>& table,vector<int>& pos,int count) {
		vector<vector<int>> dir = { {-1,0},{0,1},{1,0},{0,-1} }; // north east south west
		vector<vector<int>> back= { {1,0},{0,-1},{-1,0},{0,1} }; // reverse of north east south west
		int x = pos[0]; int y = pos[1]; int head = pos[2];
		if (table[x][y] == 0) {
			count++;
			table[x][y] = 2;
		}
		int end = is_end(table, pos);
		if (end == 1) return count; //when cleaning is end.
		else if (end == 2) { //when vacuum moves backward.
			pos[0] = x + back[pos[2]][0]; pos[1] = y + back[pos[2]][1];
			return cleaning(table, pos, count);
		}
		int left=head;
		for (int i = 0; i < 4; i++) {
			left - 1 < 0 ? left = 3 : left--;
			int cx = x + dir[left][0]; int cy = y + dir[left][1];
			if (cx>=0 && cx<table.size() && cy>=0 && cy<table[0].size() && table[cx][cy]==0) {
				pos[0] = cx; pos[1] = cy; pos[2] = left;
				return cleaning(table, pos, count);	
			}
		}
		return count;
	}
	
	int main() {
		//pair<vector<vector<int>>,vector<int>> input = makeTable();
		pair<vector<vector<int>>, vector<int>> input = makeTable2();
		cout << cleaning(input.first, input.second,0);
		return 0;
	}
	
{% endraw %}
{% endhighlight %}

