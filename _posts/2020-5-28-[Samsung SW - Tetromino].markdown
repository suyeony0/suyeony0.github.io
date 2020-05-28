---
layout: post
title: [Samsung SW - Tetromino]
data: 2020-05-26
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}

	﻿[106. [BACKJOON – SAMSUNG SW : Tetromino]]
	- I struggled to implement slinding. I spent 1 hour or so.
	- it was a quite dirty problem, since I had to make all the possible tetromino with my own hands.
	- see the code.
	#include<iostream>
	#include<fstream>
	#include<vector>
	#include<climits>
	#include<queue>
	using namespace std;
	
	vector<vector<int>> makeTable() {
		ifstream in("C:\\Users\\gjsgu\\Desktop\\Algorithm\\test_case\\test_case_for_tetromino.txt");
		int N, M;
		if (in.is_open()) {
			cout << "file is opened." << endl;
			in >> N; in >> M;
		}
		vector<vector<int>> table(N, vector<int>(M, 0));
		for (int i = 0; i < N; i++) 
			for (int j = 0; j < M; j++) in >> table[i][j];
			
		return table;
	}
	
	vector<vector<int>> makeTable2() {
		int N, M;
		cin >> N; cin >> M;
		vector<vector<int>> table(N, vector<int>(M, 0));
		for (int i = 0; i < N; i++)
			for (int j = 0; j < M; j++) cin >> table[i][j];
		return table;
	}
	queue<vector<vector<int>>> makeTetromino() {
		queue<vector<vector<int>>> que;
		que.push(vector<vector<int>>{{1,1,1,1}});
		que.push(vector<vector<int>>{ {1}, { 1 }, { 1 }, {1}});
	
		que.push(vector<vector<int>>{ {1, 1}, { 1,1 }});
	
		que.push(vector<vector<int>>{ {1,0}, { 1,0 }, { 1 ,1}});
		que.push(vector<vector<int>>{ {0, 1}, { 0,1 }, {1,1}});
		que.push(vector<vector<int>>{ {1, 1}, { 1,0 }, { 1,0 }});
		que.push(vector<vector<int>>{ {1, 1}, { 0,1 }, {0,1}});
		que.push(vector<vector<int>>{ {1, 1, 1}, { 0,0,1 }});
		que.push(vector<vector<int>>{ {1, 1, 1}, {1,0,0}});
		que.push(vector<vector<int>>{ {1, 0, 0}, {1,1,1}});
		que.push(vector<vector<int>>{ {0, 0, 1}, {1,1,1}});
	
		que.push(vector<vector<int>>{ {1, 0}, { 1,1 }, {0,1}});
		que.push(vector<vector<int>>{ {0, 1}, { 1,1 }, {1,0}});
		que.push(vector<vector<int>>{ {1, 1, 0}, {0,1,1}});
		que.push(vector<vector<int>>{ {0, 1, 1}, {1,1,0}});
	
		que.push(vector<vector<int>>{ {0, 1, 0}, {1,1,1}});
		que.push(vector<vector<int>>{ {1, 1, 1}, {0,1,0}});
		que.push(vector<vector<int>>{ {0, 1}, { 1,1 }, {0,1}});
		que.push(vector<vector<int>>{ {1, 0}, { 1,1 }, {1,0}});
		return que;
	}
	
	// this function is the key of this problem.
	int slideTetro(vector<vector<int>>& table, vector<vector<int>>& tetro) {
		int sum = 0;
		int maximum = 0;
		// we have to get a window.
		// window size is tetro.size() X tetro[0].size()
		vector<vector<int>> window;
		for (int i = 0; i + tetro.size()<= table.size(); i++) {
			for (int j = 0; j+tetro[0].size()<=table[0].size(); j++) {
				sum = 0;
				//from here, the indice are for window.
				for (int k = i; k < i + tetro.size(); k++) {
					for (int l = j; l < j + tetro[0].size(); l++) {
						if (tetro[k-i][l-j]) sum += table[k][l];
					}
				}
				maximum = max(maximum, sum);
			}
		}
		return maximum;
	}
	
	int findMaximum(vector<vector<int>>& table,queue<vector<vector<int>>>& que) {
		int maximum = 0;
		while (!que.empty()) {
			vector<vector<int>> tetro = que.front();
			que.pop();
			maximum = max(maximum,slideTetro(table,tetro));
		}
		return maximum;
	}
	
	void printTable(vector<vector<int>> table) {
		for (vector<int> row : table) {
			for (int i : row) {
				cout << i << " ";
			}
			cout << endl;
		}
	}
	
	int main() {
		//vector<vector<int>> table = makeTable();
		vector<vector<int>> table = makeTable2();
		queue < vector<vector<int>>> que = makeTetromino();
		cout<<findMaximum(table, que);
		return 0;
	}
	
{% endraw %}
