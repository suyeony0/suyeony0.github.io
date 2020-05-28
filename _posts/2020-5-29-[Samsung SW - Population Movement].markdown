---
layout: post
title: [Samsung SW - Population Movement]
date: 2020-5-29
description: txt to markdown
thumbnail: food1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

{% highlight c++ %}
```cpp
	﻿[141. [SAMSUNG – SW : Population Movement]]
	- handling visit table and BFS is the point.
	- To avoid time limit exceeded, i need to have a habit using call by reference.
	- see the code.
	#include<iostream>
	#include<fstream>
	#include<vector>
	#include<queue>
	#include<cmath>
	using namespace std;
	int N; int L; int R;
	vector<vector<int>> makeTable() {
		fstream in("C:\\Users\\gjsgu\\Desktop\\Algorithm\\test_case\\test_case_for_population_movement.txt");
		if (in.is_open()) cout << "file is opened." << endl;
		in >> N; in >> L; in >> R;
		vector<vector<int>> table(N, vector<int>(N));
		for (int i = 0; i < N; i++)
			for (int j = 0; j < N; j++)
				in >> table[i][j];
		return table;
	
	}
	vector<vector<int>> makeTable2() {
		cin >> N; cin >> L; cin >> R;
		vector<vector<int>> table(N, vector<int>(N));
		for (int i = 0; i < N; i++)
			for (int j = 0; j < N; j++)
				cin >> table[i][j];
		return table;
	
	}
	
	inline bool isValid(int a, int b) {
		if (abs(a - b) >= L && abs(a - b) <= R) return true;
		return false;
	}
	
	vector<pair<int, int>> makeUnion(vector<vector<int>>& table, vector<vector<bool>>& visit, int x, int y,int& sum) {
		vector<pair<int, int>> unions;
		queue<pair<int, int>> que;
		visit[x][y] = true;
		que.push(make_pair(x, y));
		while (!que.empty()) {
			x = que.front().first; y = que.front().second;
			unions.push_back(make_pair(x, y));
			sum += table[x][y];
			que.pop();
			if (x - 1 >= 0 && !visit[x - 1][y] && isValid(table[x - 1][y], table[x][y])) {
				visit[x - 1][y] = true;
				que.push(make_pair(x - 1, y));
			}
			if (y - 1 >= 0 && !visit[x][y - 1] && isValid(table[x][y - 1], table[x][y])) {
				visit[x][y - 1] = true;
				que.push(make_pair(x, y - 1));
			}
			if (x + 1 < N && !visit[x + 1][y] && isValid(table[x + 1][y], table[x][y])) {
				visit[x + 1][y] = true;
				que.push(make_pair(x + 1, y));
			}
			if (y + 1 < N && !visit[x][y + 1] && isValid(table[x][y + 1], table[x][y])) {
				visit[x][y + 1] = true;
				que.push(make_pair(x, y + 1));
			}
		}
		if (unions.size() == 1) unions.pop_back();
	
		return unions;
	}
	void makeMove(vector<vector<int>>& table, vector<pair<int, vector<pair<int, int>>>>& unions) {
		for (pair<int, vector<pair<int, int>>> row : unions) {
			int people = floor(row.first / row.second.size());
			for (pair<int, int> a : row.second) table[a.first][a.second] = people;
		}
		return;
	}
	
	void printTable(vector<vector<int>> table) {
		for (vector<int> row : table) {
			for (int i : row) cout << i << " ";
			cout << endl;
		}
		cout << endl;
	}
	
	int Move(vector<vector<int>>table) {
		int population_movement = 0;
		while (true) {
			vector<pair<int,vector<pair<int, int>>>> unions;
			vector<vector<bool>> visit(N, vector<bool>(N, false));
			vector<pair<int, int>> temp;
			for (int i = 0; i < N; i++) {
				for (int j = 0; j < N; j++) {
					int x = i; int y = j;
					int sum=0;
					if (!visit[x][y]) {
						temp = makeUnion(table, visit, x, y,sum);
						if (!temp.empty()) unions.push_back(make_pair(sum,temp));
					}
				}
			}
			if (unions.empty()) break;
			else {
				makeMove(table, unions);
				population_movement++;
			}
		}
		return population_movement;
	}
	
	int main() {
		vector<vector<int>> table = makeTable2();
		cout << Move(table);
		return 0;
	}
	
```
{% endhighlight %}
