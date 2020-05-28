---
layout: post
title: [Samsung SW - Goodbye Finedust!]
date: 2020-5-29
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% highlight c++ %}

	﻿[144. [SAMSUNG – SW : Goodbye Finedust!]]
	- it was a simulation problem, but not DFS and BFS.
	- following given rules not hard, but have to be careful of robot’s position whether robot is at leftside or middle or rightside.
	- see the code.
	#include<iostream>
	#include<fstream>
	#include<vector>
	
	using namespace std;
	
	vector<vector<int>> table;
	vector<pair<int,int>> robot;
	int rtx, rty, rbx, rby;
	int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };
	int r, c, t;
	bool lf=false, rt=false;
	void Input() {
		ifstream in("C:\\Users\\gjsgu\\Desktop\\Algorithm\\test_case\\test_case_for_goodbye_finedust.txt");
		if (in.is_open()) cout << "file is opened." << endl;
		in >> r; in >> c; in >> t;
		table.assign(r, vector<int>(c));
		for (int i = 0; i < r; i++) {
			for (int j = 0; j < c; j++) {
				in >> table[i][j];
				if (table[i][j] == -1) robot.push_back(make_pair(i, j));
			}
		}
		rtx = robot[0].first; rty = robot[0].second;
		rbx = robot[1].first; rby = robot[1].second;
		if (rty == 0) lf = true;
		else if (rty = c - 1) rt = true;
	}
	void Input2() {
		cin >> r; cin >> c; cin >> t;
		table.assign(r, vector<int>(c));
		for (int i = 0; i < r; i++) {
			for (int j = 0; j < c; j++) {
				cin >> table[i][j];
				if (table[i][j] == -1) robot.push_back(make_pair(i, j));
			}
		}
		rtx = robot[0].first; rty = robot[0].second;
		rbx = robot[1].first; rby = robot[1].second;
		if (rty == 0) lf = true;
		else if (rty = c - 1) rt = true;
	}
	
	
	void dustMove() {
		vector<vector<int>> new_dust;
		for (int i = 0; i < r; i++) {
			for (int j = 0; j < c; j++) {
				int x = i; int y = j;
				if (table[x][y] == -1) continue;
				int count = 0;
				if (table[x][y] > 0) {
					for (int i = 0; i < 4; i++) {
						int tx = x + dir[i][0]; int ty = y + dir[i][1];
						if (tx >= 0 && ty >= 0 && tx < r && ty < c && table[tx][ty] != -1) {
							new_dust.push_back(vector<int>{tx, ty, table[x][y]/5});
							count++;
						}
					}
				}
				table[x][y] -= (table[x][y] / 5) * count;
				if (table[x][y] != 0) new_dust.push_back(vector<int>{x, y, table[x][y]});
			}
		}
		table = vector<vector<int>>(r,vector<int>(c));
		table[rtx][rty] = -1; table[rbx][rby] = -1;
		for (vector<int> pos : new_dust) table[pos[0]][pos[1]] += pos[2];
	}
	
	void printTable() {
		for (vector<int> row : table) {
			for (int i : row)
				cout << i << " ";
			cout << endl;
		}
		cout << endl;
	}
	
	void cleanerAct() {
		//top
		for (int j = rty-1; j >= 1; j--) table[rtx][j] = table[rtx][j-1];
		
		if (lf) for (int i = rtx-1; i >= 1; i--) table[i][0] = table[i - 1][0];
		else for (int i = rtx; i >= 1; i--) table[i][0] = table[i-1][0];
	
		for (int j = 0; j < c - 1; j++) table[0][j] = table[0][j + 1];
	
		if(rt) for (int i = 0; i < rtx-1; i++) table[i][c - 1] = table[i + 1][c - 1];
		else for (int i = 0; i < rtx; i++) table[i][c - 1] = table[i + 1][c - 1];
	
		for (int j = c - 1; j > rty; j--) table[rtx][j] = table[rtx][j - 1];
		table[rtx][rty + 1] = 0;
		//bottom
		for (int j = rby - 1; j>= 1; j--) table[rbx][j] = table[rbx][j - 1];
	
		if(lf) for (int i = rbx+1; i < r - 1; i++) table[i][0] = table[i + 1][0];
		else for (int i = rbx; i < r-1; i++) table[i][0] = table[i + 1][0];
	
		for (int j = 0; j < c-1; j++) table[r - 1][j] = table[r - 1][j + 1];
	
		if(rt) for (int i = r - 1; i > rbx+1; i--) table[i][c - 1] = table[i - 1][c - 1];
		else for (int i = r - 1; i > rbx; i--) table[i][c - 1] = table[i - 1][c - 1];
	
		for (int j = c - 1; j > rby; j--) table[rbx][j] = table[rbx][j - 1];
		table[rbx][rby + 1] = 0;
	
	}
	
	int amountFineDust() {
		for (int time = 0; time < t; time++) {
			dustMove();
			cleanerAct();
		}
		int res = 0;
		for (vector<int> row : table)
			for (int j = 0; j < c; j++) if(row[j]!=-1) res += row[j];
		return res;
	}
	
	int main() {
		Input2();
		cout << amountFineDust();
		return 0;
	}
	
	
{% endhighlight %}

