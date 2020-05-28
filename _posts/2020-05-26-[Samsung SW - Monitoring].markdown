---
layout: post
title: [Samsung SW - Monitoring]
data: 2020-05-26
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}
	﻿[114. [BACKJOON – SAMSUNG SW : Monitoring ]]
	- just following rules, removing blind spot is the main point of this problem.
	- DFS is needed.
	- see the code.
	#include<iostream>
	#include<fstream>
	#include<vector>
	#include<climits>
	#include<algorithm>
	using namespace std;
	
	pair<vector<vector<int>>, vector<vector<int>>> makeTable() {
	
		ifstream in("C:\\Users\\gjsgu\\Desktop\\Algorithm\\test_case\\test_case_for_monitoring.txt");
		if (in.is_open()) cout << "file is opened." << endl;
		int N; int M;
		in >> N; in >> M;
		int temp;
		vector<vector<int>> table(N, vector<int>(M, 0));
		vector<vector<int>> camera;
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < M; j++) {
				in >> temp;
				if (1 <= temp && temp <= 5) camera.push_back({ i,j,temp });
				table[i][j] = temp;
			}
		}
		return make_pair(table, camera);
	}
	pair<vector<vector<int>>, vector<vector<int>>> makeTable2() {
		int N; int M;
		cin >> N; cin >> M;
		int temp;
		vector<vector<int>> table(N, vector<int>(M, 0));
		vector<vector<int>> camera;
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < M; j++) {
				cin >> temp;
				if (1 <= temp && temp <= 5) camera.push_back({ i,j,temp });
				table[i][j] = temp;
			}
		}
		return make_pair(table, camera);
	}
	int blindSpot(vector<vector<int>>& table) {
		int spot = 0;
		for (vector<int> row : table)
			for (int i : row)
				if (i == 0) spot++;
		return spot;
	}
	vector<vector<int>> East(vector<vector<int>> table, int x, int y) {
		for (int j = y; j < table[0].size(); j++) {
			if (table[x][j] == 6) break;
			if (table[x][j] == 0) table[x][j] = 9; // 9 is where we can monitor.
		}
		return table;
	}
	vector<vector<int>> West(vector<vector<int>> table, int x, int y) {
		for (int j = y; j >= 0; j--) {
			if (table[x][j] == 6) break;
			if (table[x][j] == 0) table[x][j] = 9; // 9 is where we can monitor.
		}
		return table;
	}
	vector<vector<int>> South(vector<vector<int>> table, int x, int y) {
		for (int i = x; i >= 0; i--) {
			if (table[i][y] == 6) break;
			if (table[i][y] == 0) table[i][y] = 9; // 9 is where we can monitor.
		}
		return table;
	}
	vector<vector<int>> North(vector<vector<int>> table, int x, int y) {
		for (int i = x; i < table.size(); i++) {
			if (table[i][y] == 6) break;
			if (table[i][y] == 0) table[i][y] = 9; // 9 is where we can monitor.
		}
		return table;
	}
	
	vector<vector<vector<int>>> Monitoring(vector<vector<int>> table,int x, int y, int dir) {
		vector<vector<vector<int>>> res_table;
		vector<vector<int>> temp_table;
		switch (dir) {
		case 1:
			// East
			res_table.push_back(East(table, x, y));
			// West
			res_table.push_back(West(table, x, y));
			// North
			res_table.push_back(North(table, x, y));
			// South
			res_table.push_back(South(table, x, y));
			return res_table;
		case 2:
			//horizontal
			temp_table = table;
			temp_table = East(temp_table, x, y);
			temp_table = West(temp_table, x, y);
			res_table.push_back(temp_table);
			//vertical
			temp_table = table;
			temp_table = South(temp_table, x, y);
			temp_table = North(temp_table, x, y);
			res_table.push_back(temp_table);
			return res_table;
		case 3 :
			// North East
			temp_table = table;
			temp_table = North(temp_table, x, y);
			temp_table = East(temp_table, x, y);
			res_table.push_back(temp_table);
			// South East
			temp_table = table;
			temp_table = South(temp_table, x, y);
			temp_table = East(temp_table, x, y);
			res_table.push_back(temp_table);
			// North West
			temp_table = table;
			temp_table = North(temp_table, x, y);
			temp_table = West(temp_table, x, y);
			res_table.push_back(temp_table);
			// South West
			temp_table = table;
			temp_table = South(temp_table, x, y);
			temp_table = West(temp_table, x, y);
			res_table.push_back(temp_table);
			return res_table;
		case 4:
			// without South
			temp_table = table;
			temp_table = West(temp_table, x, y);
			temp_table = North(temp_table, x, y);
			temp_table = East(temp_table, x, y);
			res_table.push_back(temp_table);
			// without West
			temp_table = table;
			temp_table = North(temp_table, x, y);
			temp_table = East(temp_table, x, y);
			temp_table = South(temp_table, x, y);
			res_table.push_back(temp_table);
			// without North
			temp_table = table;
			temp_table = East(temp_table, x, y);
			temp_table = South(temp_table, x, y);
			temp_table = West(temp_table, x, y);
			res_table.push_back(temp_table);
			// without East
			temp_table = table;
			temp_table = South(temp_table, x, y);
			temp_table = West(temp_table, x, y);
			temp_table = North(temp_table, x, y);
			res_table.push_back(temp_table);
			return res_table;
		case 5:
			temp_table = table;
			temp_table = South(temp_table, x, y);
			temp_table = West(temp_table, x, y);
			temp_table = North(temp_table, x, y);
			temp_table = East(temp_table, x, y);
			res_table.push_back(temp_table);
			return res_table;
		}
	}
	
	int DFS(vector<vector<int>> table, vector<vector<int>> camera,int start) {
		if (start == camera.size()) return blindSpot(table);
		int minimum = INT_MAX;
		int x = camera[start][0]; int y = camera[start][1]; int dir = camera[start][2];
		vector < vector<vector<int>>> res_table = Monitoring(table, x, y, dir);
		for (int i = 0; i < res_table.size(); i++) 	minimum=min(minimum,DFS(res_table[i], camera, start + 1));
		return minimum;
	}
	
	
	int main() {
		//pair<vector<vector<int>>, vector<vector<int>>> input = makeTable();
		pair<vector<vector<int>>, vector<vector<int>>> input = makeTable2();
		vector<vector<int>> table = input.first;
		vector<vector<int>> camera = input.second;
		cout << DFS(table, camera,0);
		return 0;
	}
	
	
{% endraw %}
