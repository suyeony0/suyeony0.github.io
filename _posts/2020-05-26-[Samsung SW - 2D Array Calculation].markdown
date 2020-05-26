---
layout: post
title: [Samsung SW - 2D Array Calculation]
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

	﻿
	[145. [SAMSUNG – SW :2D Array Calculation]]
	- this was weird. when I used unordered_map, abort occurred at 9% of submission.
	- but after I changed the map to int array with same algorithm, it worked well.
	- what’s wrong with my previous version??? Even, all the test case they gave or in disccusion session was passed with my unordered_map algorithm!
	- see the code.
	#include<iostream>
	#include<fstream>
	#include<vector>
	#include<unordered_map>
	#include<algorithm>
	#define max(a,b) a>b?a:b
	#define min(a,b) a>b?b:a
	#define max_k 101
	using namespace std;
	
	
	int r, c, k;
	vector<vector<int>> table(3,vector<int>(3));
	int time = 0;
	int row = 3, col = 3;
	void Input() {
		ifstream in("C:\\Users\\gjsgu\\Desktop\\Algorithm\\test_case\\test_case_for_2d_array_calculation.txt");
		if (in.is_open()) cout << "file is opened." << endl;
		in >> r; in >> c; in >> k;
		for (int i = 0; i < 3; i++)
			for (int j = 0; j < 3; j++)
				in >> table[i][j];
		
	}
	void Input2() {
		cin >> r; cin >> c; cin >> k;
		for (int i = 0; i < 3; i++)
			for (int j = 0; j < 3; j++)
				cin >> table[i][j];
	
	}
	
	void operR() {
		int max_col = 0;
		vector<vector<pair<int, int>>> temp(row);
		for (int i = 0; i < row; i++) {
			int arr[max_k] = { 0, };
			for (int j = 0; j < col; j++) if (table[i][j] != 0) arr[table[i][j]]++;
			for (int j = 1; j < max_k; j++) if (arr[j] != 0) temp[i].push_back(make_pair(arr[j], j));
			sort(temp[i].begin(), temp[i].end());
			max_col = max(max_col, temp[i].size() * 2);
		}
		col = min(100,max_col);
		table = vector<vector<int>>(row, vector<int>(col,0));
		for (int i = 0; i < row; i++) {
			for (int j = 0; j < temp[i].size() &&j<50; j++) {
				table[i][2*j] = temp[i][j].second;
				table[i][(2*j) + 1] = temp[i][j].first;
			}
		}
	}
	
	void operC() {
		int max_row = 0;
		vector<vector<pair<int,int>>> temp(col);
		for (int j = 0; j < col; j++) {
			int arr[max_k] = { 0, };
			for (int i = 0; i < row; i++) if(table[i][j]!=0) arr[table[i][j]]++;
			for (int i = 1; i < max_k; i++) if (arr[i] != 0) temp[j].push_back(make_pair(arr[i], i));
			sort(temp[j].begin(), temp[j].end());
			max_row = max(max_row, temp[j].size()*2);
		}
		row = min(100,max_row);
		table = vector<vector<int>>(row, vector<int>(col,0));
		for (int j = 0; j < col; j ++) {
			for (int i = 0; i < temp[j].size()&& i< 50; i++) {
				table[2*i][j] = temp[j][i].second;
				table[(2*i)+1][j] = temp[j][i].first;
			}
		}
	}
	void printTable() {
		for (int i = 0; i < row; i++) {
			for (int j = 0; j < col; j++)
				cout << table[i][j] << " ";
			cout << endl;
		}
		cout << endl;
	
	}
	
	
	int calculation() {
		while (time<=100) {
			if (r-1>=0 && c-1>=0 && r-1<row && c-1<col&&table[r - 1][c - 1] == k) return time;
			if (row >= col) operR();
			else operC();
			time++;
		}
		return -1;
	
	}
	
	int main() {
		Input2();
		cout<<calculation();
		return 0;
		
	}
	
