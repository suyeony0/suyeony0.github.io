---
layout: post
title: [Samsung SW - Rolling Dice]
date: 2020-5-29
description: txt to markdown
thumbnail: work1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

{% highlight c++ %}

{% raw %}

	﻿[104. [BACKJOON – SAMSUNG SW : Rolling Dice]]
	- I spent less than 1 hour. it was not that hard to solve.
	- see the code.
	#include<iostream>
	#include<fstream>
	#include<vector>
	
	using namespace std;
	
	pair<vector<vector<int>>,vector<int>> makeTable(int& x, int& y) {
		ifstream in("C:\\Users\\gjsgu\\Desktop\\Algorithm\\test_case\\test_case_for_rolling_dice.txt");
		int N, M, K;
		if (in.is_open()) {
			cout << "file is opened." << endl;
			in >> N; in >> M; in >> x; in >> y; in >> K;
		}
		vector<vector<int>> table(N,vector<int>(M,0));
		vector<int> order(K, 0);
		for (int i = 0; i < N; i++) 
			for (int j = 0; j < M; j++) in >> table[i][j];
		for (int i = 0; i < K; i++) in >> order[i];
		return make_pair(table, order);
	}
	
	pair<vector<vector<int>>, vector<int>> makeTable2(int& x, int& y) {
		int N, M, K;
		cin >> N; cin >> M; cin >> x; cin >> y; cin >> K;
		vector<vector<int>> table(N, vector<int>(M, 0));
		vector<int> order(K, 0);
		for (int i = 0; i < N; i++)
			for (int j = 0; j < M; j++) cin >> table[i][j];
		for (int i = 0; i < K; i++) cin >> order[i];
		return make_pair(table, order);
	}
	void printTable(vector<vector<int>> table) {
		for (vector<int> row : table) {
			for (int i : row)
				cout << i << " ";
			cout << endl;
		}
	}
	
	bool moveTheDice(int a, int b,int& x, int& y,int size_x, int size_y){
		if (x + a < 0 || x + a >= size_x || y + b < 0 || y + b >= size_y) return false;
		x = x + a; y = y + b;
		return true;
	}
	void rollTheDice(vector<vector<int>>& dice,int dir) {
		int temp;
		switch (dir) {
		case 1: // east
			temp = dice[1][2]; dice[1][2] = dice[1][1]; dice[1][1] = dice[1][0]; dice[1][0] = dice[3][1]; dice[3][1] = temp;
			break;
		case 2: // west
			temp = dice[1][0]; dice[1][0] = dice[1][1]; dice[1][1] = dice[1][2]; dice[1][2] = dice[3][1]; dice[3][1] = temp;
			break;
		case 3: // north
			temp = dice[0][1]; dice[0][1] = dice[1][1]; dice[1][1] = dice[2][1]; dice[2][1] = dice[3][1]; dice[3][1] = temp;
			break;
		case 4: // south
			temp = dice[3][1]; dice[3][1] = dice[2][1]; dice[2][1] = dice[1][1]; dice[1][1] = dice[0][1]; dice[0][1] = temp;
			break;
		}
	}
	
	void paintTheDice(vector<vector<int>>& table, vector<vector<int>>& dice,int x, int y) {
		if (!table[x][y]) {
			table[x][y] = dice[3][1]; // dice[3][1] is bottom.
			return;
		}
		dice[3][1] = table[x][y];
		table[x][y] = 0;
		return;
	}
	
	void followingOrder(vector<vector<int>>& table, vector<int> order, vector<vector<int>> dice,int& x,int& y) {
		int dir[4][2] = { {0,1},{0,-1},{-1,0},{1,0} }; //east west north south
		for (int i = 0; i < order.size(); i++) {
			if (!moveTheDice(dir[order[i] - 1][0], dir[order[i] - 1][1], x, y, table.size(), table[0].size())) continue;
			//cout << " x :" << x << " y : " << y << endl;
			rollTheDice(dice,order[i]);
			paintTheDice(table,dice,x,y);
			cout << dice[1][1] << endl;
		}
	}
	
	
	
	int main() {
		int x, y;
		//pair<vector<vector<int>>,vector<int>> input = makeTable(x,y);
		pair<vector<vector<int>>, vector<int>> input = makeTable2(x,y);
		vector<vector<int>> table = input.first;
		vector<int> order = input.second;
		vector<vector<int>> dice(4, vector < int>(3,0));
		followingOrder(table,order,dice,x,y);
		return 0;
	}
	
	
{% endraw %}
{% endhighlight %}

