---
layout: post
title: [Samsung SW - Dragon Curve]
date: 2020-5-29
description: txt to markdown
thumbnail: food2.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

```cpp
	﻿[116. [BACKJOON – SAMSUNG SW : Dragon Curve]]
	- this problem’s main point was the way to make the dragon curve with generation.
	- I used a stack to record previous directions and take it all when new generation was started with rotating the directions 90 degrees.
	- see the code.
	#include<iostream>
	#include<fstream>
	#include<vector>
	
	using namespace std;
	
	int table[101][101] = { 0, };
	int N,X, Y, d, g;
	int direction[4][2] = { {0,1},{-1,0},{0,-1},{1,0} }; // east north west south
	
	vector<vector<int>> makeTable() {
		ifstream in("C:\\Users\\gjsgu\\Desktop\\Algorithm\\test_case\\test_case_for_dragon_curve.txt");
		if (in.is_open()) cout << "file is opened." << endl;
		in >> N;
		vector<vector<int>> curve;
		for (int i = 0; i < N; i++) {
			in >> X >> Y >> d >> g;
			curve.push_back(vector<int>{X, Y, d, g});
		}
		return curve;
	}
	
	vector<vector<int>> makeTable2() {
		cin >> N;
		vector<vector<int>> curve;
		for (int i = 0; i < N; i++) {
			cin >> X >> Y >> d >> g;
			curve.push_back(vector<int>{X, Y, d, g});
		}
		return curve;
	}
	
	
	void printCurve(vector<vector<int>> curve) {
		for (int i = 0; i < curve.size(); i++) {
			for (int j = 0; j < curve[0].size(); j++)
				cout << curve[i][j] << " ";
			cout << endl;
		}
	}
	
	void printTable() {
		for (int i = 0; i < 101; i++) {
			for (int j = 0; j < 101; j++) {
				cout << table[i][j] << " ";
			}
			cout << endl;
		}
	}
	
	pair<vector<int>, vector<int>> Drawing(vector<int> stack, int ex, int ey) {
		vector<int> res = stack;
		for (int i = stack.size() - 1; i >= 0; i--) {
			int dir = (stack[i] + 1) % 4;
			ex += direction[dir][1]; ey += direction[dir][0];
			table[ey][ex] = 1;
			res.push_back(dir);
		}
		return make_pair(res, vector<int>{ex, ey});
	}
	
	void makeDragonCurve(vector<vector<int>> curve) {
		//how to make rotate 90 degree?
		for (vector<int> row : curve) {
			int x = row[0]; int y = row[1]; int dir = row[2]; int generation = row[3];
			int ex = x + direction[dir][1]; int ey = y + direction[dir][0];
			table[y][x] = 1;
			table[ey][ex] = 1;
			vector<int> stack = { dir };
			for (int i = 1; i <= generation; i++) {
				pair<vector<int>, vector<int>> res = Drawing(stack, ex, ey);
				stack = res.first; ex = res.second[0]; ey = res.second[1];
			}
		}
	}
	
	int findAnswer() {
		int sum = 0;
		for (int i = 1; i < 101; i++) {
			for (int j = 1; j < 101; j++) {
				if (table[i][j] && table[i - 1][j] && table[i][j - 1] && table[i - 1][j - 1]) sum++;
			}
		}
		return sum;
	}
	
	int main() {
		//vector<vector<int>> curve = makeTable();
		vector<vector<int>> curve = makeTable2();
		makeDragonCurve(curve);
		cout<<findAnswer();
		return 0;
	}
	
```
