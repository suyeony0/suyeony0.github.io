---
layout: post
title: [Samsung SW - Tree Jaetech]
data: 2020-05-26
description: txt to markdown
thumbnail: food2.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}
	ï»?142. [SAMSUNG ??SW : Tree Jaetech]]
	- I think, Samsung?™s simulation problem is quite dirty.
	- they present super rigid time limit. 
	- In this time also, I spent so much time to reduce running time.
	- see the code.
	#include<iostream>
	#include<fstream>
	#include<vector>
	#include<algorithm>
	#include<unordered_map>
	using namespace std;
	
	int n, m, k;
	
	int dir[8][2] = { {-1 ,-1},{-1,0},{-1,1},{0,-1},{0,1},{1,-1},{1,0},{1,1} }; // From top-left to bottom-right, 8 directions.
	
	vector<vector<int>> energy;
	vector<vector<vector<int>>> trees;
	vector<vector<int>> table;
	vector<vector<int>> dead;
	void makeInput() {
		ifstream in("C:\\Users\\gjsgu\\Desktop\\Algorithm\\test_case\\test_case_for_tree_jaetech.txt");
		if (in.is_open()) cout << "file is opened." << endl;
		in >> n; in >> m; in >> k;
		table.assign(n, vector<int>(n, 5));
		energy.assign(n, vector<int>(n));
		trees.assign(n, vector<vector<int>>(n));
		for (int i = 0; i < n; i++) {
			for (int j = 0; j < n; j++) {
				in >> energy[i][j];
			}
		}
		int a, b, c;
		for (int i = 0; i < m; i++) {
			in >> a; in >> b; in >> c;
			trees[a - 1][b - 1].push_back(c);
		}
	}
	
	void makeInput2() {
		cin >> n; cin >> m; cin >> k;
		table.assign(n, vector<int>(n, 5));
		energy.assign(n, vector<int>(n));
		trees.assign(n, vector<vector<int>>(n));
		for (int i = 0; i < n; i++) {
			for (int j = 0; j < n; j++) {
				cin >> energy[i][j];
			}
		}
		int a, b, c;
		for (int i = 0; i < m; i++) {
			cin >> a; cin >> b; cin >> c;
			trees[a - 1][b - 1].push_back(c);
		}
	}
	inline bool isValid(int x, int y) {
		if (x >= 0 && x < n && y >= 0 && y < n) return true;
		return false;
	}
	
	void spring_summer() {
		for (int i = 0; i < n; i++) {
			for (int j = 0; j < n; j++) {
				int dead = 0;
				vector<int> temp;
				sort(trees[i][j].begin(), trees[i][j].end());
				for (int k = 0; k < trees[i][j].size(); k++) {
					int age = trees[i][j][k];
					if (table[i][j] < age) { //if there is not enough energy to eat.
						dead += age / 2;
						continue;
					}
					else {
						table[i][j] -= age;
						temp.push_back(trees[i][j][k]+1); // age +1
					}
				}
				table[i][j] += dead; //summer
				trees[i][j].clear();
				for (int qq : temp) trees[i][j].push_back(qq);
			}
			
		}
	}
	
	
	
	void autumn() {
		for (int i = 0; i < n; i++) {
			for (int j = 0; j < n; j++) {
				for (int k = 0; k < trees[i][j].size(); k++) {
					int age = trees[i][j][k];
					if (age % 5 != 0) continue;
					else {
						for (int t = 0; t < 8; t++) {
							int tx = i + dir[t][0]; int ty = j + dir[t][1];
							if (isValid(tx, ty)) {
								trees[tx][ty].push_back(1);
							}
						}
	
					}
				}
			}
			
		}
	}
	
	void winter() {
		for (int i = 0; i < n; i++) {
			for (int j = 0; j < n; j++) {
				table[i][j] += energy[i][j];
			}
		}
	}
	
	int main() {
		makeInput2();
		
		for (int year = 0; year < k; year++) {	
			spring_summer();
			autumn();
			if (year == k - 1) break; // we don't care last winter
			winter();
		}
		int answer = 0;
		for (int i = 0; i < n; i++)
			for (int j = 0; j < n; j++)
				answer += trees[i][j].size();
		cout << answer;
		return 0;
	}
	
	
{% endraw %}
