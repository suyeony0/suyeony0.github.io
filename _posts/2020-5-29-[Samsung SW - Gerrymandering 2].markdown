---
layout: post
title: [Samsung SW - Gerrymandering 2]
date: 2020-5-29
description: txt to markdown
thumbnail: breakfast-orange-lemon-oranges-large.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

```cpp

{% raw %}

	﻿#include<iostream>
	#include<fstream>
	#include<vector>
	#include<algorithm>
	
	#define min(a,b) a>b?b:a
	using namespace std;
	int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };
	vector<vector<int>> table;
	int N;
	
	void Input() {
		ifstream in("C:\\Users\\gjsgu\\Desktop\\Algorithm\\test_case\\test_case_for_gerrymandering.txt");
		if (in.is_open()) cout << "file is opened." << endl;
		in >> N;
		table.assign(N+1, vector<int>(N+1));
		for (int i = 1; i <= N; i++) {
			for (int j = 1; j <= N; j++) {
				in >> table[i][j];
			}
		}
	}
	
	void Input2() {
		cin >> N;
		table.assign(N+1, vector<int>(N+1));
		for (int i = 1; i <= N; i++) {
			for (int j = 1; j <= N; j++) {
				cin >> table[i][j];
			}
		}
	
	}
	
	
	void printTable(vector<vector<int>>& temp_table) {
		for (vector<int> row : temp_table) {
			for (int i : row) {
				cout << i << " ";
			}
			cout << endl;
		}
		cout << endl;
	}
	
	
	void makeDistrict(vector<vector<int>>& temp, int x, int y, int d1, int d2) {
	
		// 1
		for (int i = 0; i < x + d1; i++) {
			for (int j = 0; j <= y; j++) {
				if (temp[i][j] == 10) { temp[i][j] = 5; break; }
				temp[i][j] = 1;
			}
		}
		// 2
		for (int i = 0; i < x + d2+1; i++) {
			for (int j = N; j > y; j--) {
				if (temp[i][j] == 10) { temp[i][j] = 5; break; }
				temp[i][j] = 2;
			}
		}	
		//3
		for (int i = x + d1; i <= N; i++) {
			for (int j = 0; j < y - d1 + d2; j++) {
				if (temp[i][j] == 10) { temp[i][j] = 5; break; }
				temp[i][j] = 3;
			}
		}
		//4
		for (int i = x + d2+1; i <= N; i++) {
			for (int j = N; j >= y - d1 + d2; j--) {
				if (temp[i][j] == 10) { temp[i][j] = 5; break; }
				temp[i][j] = 4;
			}
		}
		
	}
	
	int drawLine(int x,int y,int d1,int d2) {
		vector<vector<int>> temp(N+1, vector<int>(N+1, 5));
		vector<int> exist(5, false);
		//top left
		for (int i = 0; i <= d1; i++) temp[x+i][y-i] = 10;
		//top right
		for (int i = 0; i <= d2; i++) temp[x + i][y + i] = 10;
		//bottom left
		for (int i = 0; i <= d2; i++) temp[x + d1 + i][y - d1 + i] = 10;
		//bottom right
		for (int i = 0; i <= d1; i++) temp[x + d2 + i][y + d2 - i] = 10;
		
		makeDistrict(temp, x, y, d1, d2);
		/*//count
		for (int i = 1; i <= N; i++) {
			for (int j = 1; j <= N; j++) {
				exist[temp[i][j] - 1]++;
			}
		}
		for (int i : exist) if (i == 0) return 999999;
	
		//isConnected?
		for (int i = 1; i <= N; i++) {
			for (int j = 1; j <= N; j++) {
				int cx = i; int cy = j;
				if (exist[temp[cx][cy] - 1] == 1) continue;
				bool connected = false;
				for (int k = 0; k < 4; k++) {
					int tx = cx + dir[k][0]; int ty = cy + dir[k][1];
					if (tx >= 1 && ty >= 1 && tx <= N && ty <= N && temp[tx][ty] == temp[cx][cy]) connected = true; 
				}
				if (!connected) return 999999;
			}
		}*/
		vector<int> people = { 0,0,0,0,0 };
		//cout << x << "," << y << " : " << d1 << "," << d2 << endl;
		//printTable(temp);
		for (int i = 1; i <= N; i++) {
			for (int j = 1; j <= N; j++) {
				people[temp[i][j] - 1]+=table[i][j];
			}
		}
		
		
		
		
		return (*max_element(people.begin(), people.end())) - (*min_element(people.begin(), people.end()));
	
	}
	
	bool isValidToMakeLine(int x,int y,int d1,int d2) {
	
	
		if (x + d1 > N || y - d1 < 1) return false;
		if (x + d2 > N || y + d2 > N) return false;
		if (x + d1 + d2 > N || y - d1 + d2 > N) return false;
		if (x + d2 + d1 > N || y + d2 - d1 < 1) return false;
	
		return true;
	
	}
	
	int Gerrymandering() {
		//(i< i+d1+d2 && i+d1+d2<N) && (j-d1>=0 && j+d2<N)
		int answer = 9999999;
		for (int i = 1; i < N; i++) { //x
			for (int j = 2; j < N ; j++) { //y
				int d1 = 1, d2 = 1;
				for (d1=1; d1<=j; d1++) { //d1
					for (d2 = 1; d2<=N-j; d2++) {
						if(isValidToMakeLine(i,j,d1,d2)) answer = min(answer, drawLine(i, j, d1, d2));
					}
				}
				
			}
		
		}
		return answer;
	}
	
	
	int main() {
		Input2();
		cout << Gerrymandering();
		return 0;
	}
	
	
	
	
{% endraw %}
```

