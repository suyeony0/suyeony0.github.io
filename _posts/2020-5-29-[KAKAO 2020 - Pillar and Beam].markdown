---
layout: post
title: [KAKAO 2020 - Pillar and Beam]
date: 2020-5-29
description: txt to markdown
thumbnail: city2.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}

	﻿[123. [Programmers– KAKAO 2020 : Pillar and Beam]]
	- it was a quite dirty and time spending work.
	- I had to implement all the possible condition by given rules.
	- see the code.
	#include <string>
	#include <vector>
	#include<iostream>
	#define pillar 0
	#define beam 1
	using namespace std;
	
	inline int toY(int y, int n) { return n - y - 1; }
	
	void printTable(vector<vector<vector<int>>>& table, int n) {
		for (int i = 0; i < n; i++) {
			for (int j = 0; j < n; j++) {
				cout << table[i][j][pillar] << "," << table[i][j][beam] << " ";
			}
			cout << endl;
		}
	}
	void printAnswer(vector<vector<int>>& answer) {
		for (vector<int> row : answer) {
			for (int i : row) {
				cout << i << " ";
			}
			cout << endl;
		}
	
	}
	void Create(vector<vector<vector<int>>>& table, int x, int y, bool isBeam,int n) {
		if (!isBeam) { //when it is a pillar.
			if(y==n-1) table[y][x][pillar] = 1;
			else if(table[y][x][beam]) table[y][x][pillar] = 1;
			else if(x-1>=0 && table[y][x-1][beam]) table[y][x][pillar] = 1;
			else if(table[y+1][x][pillar]) table[y][x][pillar] = 1;
				
		}
		else { // when it is a beam.
			if(y+1<n && table[y+1][x][pillar]) table[y][x][beam] = 1;
			else if (x + 1 < n && y + 1 < n && table[y + 1][x + 1][pillar]) table[y][x][beam] = 1;
			else if (x-1>=0 && table[y][x-1][beam] && x+1<n && table[y][x+1][beam]) table[y][x][beam] = 1;
		}
	}
	
	void Delete(vector<vector<vector<int>>>& table, int x, int y, bool isBeam,int n) {
		if (!isBeam) {
			if (y - 1 >= 0 && table[y - 1][x][pillar] && table[y - 1][x][beam] == 0 && (x - 1 <0 || table[y - 1][x - 1][beam] == 0)) return;
			else if (y - 1 >= 0 && table[y - 1][x][beam] && (x + 1 >= n || table[y][x + 1][pillar] == 0) && ((x+1>=n || table[y - 1][x + 1][beam] == 0) || (x - 1 < 0 || table[y - 1][x - 1][beam] == 0))) return;
			else if (y - 1 >= 0 && x - 1 >= 0 && table[y - 1][x - 1][beam] && table[y][x - 1][pillar] == 0 && ((x - 2 < 0 || table[y - 1][x - 2][beam] == 0) || (table[y - 1][x][beam] == 0))) return;
			else table[y][x][pillar] = 0;
		}
		else {
			if (table[y][x][pillar] && (x - 1 < 0 || table[y][x - 1][beam] == 0) && table[y + 1][x][pillar] == 0) return;
			else if ((x + 1 < n && table[y][x + 1][pillar]) && table[y + 1][x + 1][pillar] == 0 && table[y][x + 1][beam] == 0) return;
			else if ((x - 1 >= 0 && table[y][x - 1][beam] == 1) && table[y + 1][x - 1][pillar] == 0 && table[y + 1][x][pillar] == 0) return;
			else if((x+1<n && table[y][x+1][beam]==1) && table[y+1][x+1][pillar]==0 && (x+2>=n || table[y+1][x+2][pillar]==0 )) return;
			else table[y][x][beam] = 0;
		}
	}
	
	
	
	vector<vector<int>> solution(int n, vector<vector<int>> build_frame) {
		vector<vector<int>> answer;
		// notice that the table's row is y not x. And the origin is bottom-left not top-left.
		vector<vector<vector<int>>> table(n, vector<vector<int>>(n, vector<int>(2, 0)));
		// make table
		for (int i = 0; i < build_frame.size(); i++) {
			int x = build_frame[i][0]; int y = toY(build_frame[i][1],n); bool isBeam = build_frame[i][2]; bool create = build_frame[i][3];
			create ? Create(table, x, y, isBeam,n) : Delete(table, x, y, isBeam,n);
		}
		printTable(table, n);
		// make answer
		for (int j = 0; j < n; j++) {
			for (int i = n-1; i>=0; i--) {
				if (table[i][j][pillar]) answer.push_back({ j,toY(i,n),0 });
				if (table[i][j][beam]) answer.push_back({ j,toY(i,n),1 });
			}
		}
		printAnswer(answer);
	
		return answer;
	} 
	
	int main() {
		
		solution(6, input);
		return 0;
	}
	
{% endhighlight %}
