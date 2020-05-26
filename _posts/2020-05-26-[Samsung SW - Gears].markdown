---
layout: post
title: [Samsung SW - Gears]
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

	﻿[113. [BACKJOON – SAMSUNG SW : Gears ]]
	- I think there are at least 2 method to solve this problem. one is DFS and another one is just to use many if-condintion clause.
	- I chose the latter one.
	- the trap was that before rotate a gear, we have to check the next gear will be rotated or not.
	- see the code.
	#include<iostream>
	#include<fstream>
	#include<vector>
	
	using namespace std;
	
	pair<vector<vector<int>>,vector<vector<int>>> makeTable() {
		ifstream in("C:\\Users\\gjsgu\\Desktop\\Algorithm\\test_case\\test_case_for_gears.txt");
	
		if (in.is_open()) cout << "file is opened." << endl;
	
		vector<vector<int>> table(4,vector<int>(8,0));
		string row;
		for (int i = 0; i < 4; i++) {
			in >> row;
			for (int j = 0; j < row.length(); j++) {
				table[i][j] = row[j]-'0';
			}
		}
		int K;
		in >> K;
		int a; int b;
		vector<vector<int>> rotate(K,vector<int>(2,0));
		for (int i = 0; i < K; i++) {
			in >> a; in >> b;
			rotate[i][0] = a; rotate[i][1] = b;
		}
		return make_pair(table, rotate);
	}
	pair<vector<vector<int>>, vector<vector<int>>> makeTable2() {
		vector<vector<int>> table(4, vector<int>(8, 0));
		string row;
		for (int i = 0; i < 4; i++) {
			cin >> row;
			for (int j = 0; j < row.length(); j++) {
				table[i][j] = row[j] - '0';
			}
		}
		int K;
		cin >> K;
		int a; int b;
		vector<vector<int>> rotate(K, vector<int>(2, 0));
		for (int i = 0; i < K; i++) {
			cin >> a; cin >> b;
			rotate[i][0] = a; rotate[i][1] = b;
		}
		return make_pair(table, rotate);
	}
	
	vector<int> move(vector<int> gear, int dir) {
		if (dir == 1) {
			int temp = gear[7];
			for (int i = gear.size() - 2; i >= 0; i--)
				gear[i + 1] = gear[i];
			gear[0] = temp;
			return gear;
		}
		else {
			int temp = gear[0];
			for (int i = 0; i < gear.size() - 1; i++)
				gear[i] = gear[i + 1];
			gear[7] = temp;
			return gear;
		}	
	}
	void printTable(vector<vector<int>> gears) {
		for (vector<int> row : gears) {
			for (int i : row)
				cout << i << " ";
			cout << endl;
		}
	
	}
	
	int tonado(vector<vector<int>> gears,vector<vector<int>> rotate) {
		// 2 is east, 6 is west.
		int cur_gear; int dir;
		for (int i = 0; i < rotate.size(); i++) {
			cur_gear = rotate[i][0]-1; dir = rotate[i][1];
			gears[cur_gear] = move(gears[cur_gear], dir);
			int temp_dir = dir;
			//to left
			for (int left = cur_gear - 1; left >= 0; left--) {
				if (temp_dir == 1 && gears[left+1][7]!=gears[left][2]) gears[left] = move(gears[left], temp_dir=-1);
				else if(temp_dir==-1 && gears[left+1][5]!=gears[left][2]) gears[left] = move(gears[left], temp_dir=1);
				else break;
			}
			//to right
			temp_dir = dir;
			for (int right = cur_gear + 1; right < gears.size(); right++) {
				if(temp_dir==1 && gears[right-1][3]!=gears[right][6]) gears[right] = move(gears[right], temp_dir=-1);
				else if (temp_dir ==-1 && gears[right - 1][1] != gears[right][6]) gears[right] = move(gears[right], temp_dir = 1);
				else break;
			}
		
		}
		return gears[0][0] + gears[1][0] * 2 + gears[2][0] * 4 + gears[3][0] * 8;
	}
	
	
	
	int main() {
		//pair<vector<vector<int>>, vector<vector<int>>> input = makeTable();
		pair<vector<vector<int>>, vector<vector<int>>> input = makeTable2();
		vector<vector<int>> gears = input.first;
		vector<vector<int>> rotate = input.second;
	
		cout << tonado(gears, rotate);
		return 0;
	}
	
