---
layout: post
title: [Samsung SW - Circle Rotation]
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

	﻿[150. [SAMSUNG – SW : Circle Rotation]] 
	- the trick this problem has is a circle they gave is logically same with 2D array without columns act like circle.
	- so it was just a simulation problem. but like always, SAMSUNG’s problem is not kind to user.
	- there are pretty many ambiguous restrictions.
	- see the code.
	#include<iostream>
	#include<fstream>
	#include<vector>
	#include<queue>
	using namespace std;
	
	int N, M, T;
	vector<vector<int>> order;
	vector<vector<int>> table;
	int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };
	void Input() {
		ifstream in("C:\\Users\\gjsgu\\Desktop\\Algorithm\\test_case\\test_case_for_circle_rotation.txt");
		if (in.is_open()) cout << "file is opened." << endl;
		in >> N; in >> M; in >> T;
		table.assign(N, vector<int>(M));
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < M; j++) {
				in >> table[i][j];
			}
		}
		int a, b, c;
		for (int i = 0; i < T; i++) {
			in >> a; in >> b; in >> c;
			order.push_back(vector<int>{a,b,c});
		}
	}
	void Input2() {
		cin >> N; cin >> M; cin >> T;
		table.assign(N, vector<int>(M));
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < M; j++) {
				cin >> table[i][j];
			}
		}
		int a, b, c;
		for (int i = 0; i < T; i++) {
			cin >> a; cin >> b; cin >> c;
			order.push_back(vector<int>{a, b, c});
		}
	}
	
	
	void Move(int dir,int round,vector<int>& row) {
		int temp;
		round %= row.size();
		if (dir == 0) {
			for (int r = 0; r < round; r++) {
				temp = row.back();
				for (int i = row.size()-1; i >=1; i--) row[i] = row[i - 1];
				row[0] = temp;
			}
		}
		else {
			for (int r = 0; r < round; r++) {
				temp = row[0];
				for (int i = 0; i < row.size() - 1;i++) 
					row[i] = row[i + 1];
				row[row.size() - 1] = temp;
			}
		}
	}
	
	bool isEmpty(vector<pair<int, int>>& left_pos) {
		int count = 0;
		for (int i = 0; i < N;i++) {
			for (int j = 0; j < M; j++) if (table[i][j] != 0) left_pos.push_back(make_pair(i, j));
		}
		if (left_pos.empty()) return true;
		return false;
	}
	
	void printTable() {
		for (vector<int> row : table) {
			for (int i : row) cout << i << " ";
			cout << endl;
		}
		cout << endl;
	}
	
	int Rotate() {
		//cout << "START" << endl;
		//printTable();
		for (vector<int> ord : order) {
			int x = ord[0]; int d = ord[1]; int k = ord[2];
			vector<int> row_index;
			//cout << "order : "<<x<<","<<d<<","<<k << endl;
			for (int i = 1; i * x <= N; i++) { //rotate
				int circle = (i * x)-1;
				row_index.push_back(circle);
				Move(d, k,table[circle]);
				
			}
			//cout << "After Move" << endl;
			//printTable();
			vector<pair<int, int>> left_pos;
			if (!isEmpty(left_pos)) {
				vector<vector<bool>> visit(N, vector<bool>(M, false));
				bool flag = true;
				for (int i = 0; i < N; i++) {
					for (int j = 0; j < M; j++) {
						visit[i][j] = true;
						if (table[i][j] == 0) continue;
						int cur = table[i][j];
						queue<pair<int, int>> que; que.push(make_pair(i, j));
						while (!que.empty()) {
							int x = que.front().first;  int y = que.front().second; que.pop();
							for (int u = 0; u < 4; u++) {
								int tx = x + dir[u][0]; int ty = y + dir[u][1];
								if (ty == M) ty = 0; if (ty == -1) ty = M - 1; //they are in shape of circle.
								if (tx >= 0 && tx < N&& table[tx][ty] == cur && !visit[tx][ty]) {
									visit[tx][ty] = true; que.push(make_pair(tx, ty));
									table[tx][ty] = 0; table[x][y] = 0;
									flag = false;
								}
							}
						}
					}
				}
				if (flag) {
					//cout << "<<flag happend>>" << endl;
					int sum = 0;
					for (vector<int> row : table) {
						for (int i : row) sum += i;
					}
					double average = (double)sum / (double)left_pos.size();
					//cout << "sum : " << sum << " average : " << average << endl;
					for (pair<int, int> a : left_pos) {
						if (table[a.first][a.second] > average) table[a.first][a.second]--;
						else if(table[a.first][a.second] < average)table[a.first][a.second]++;
					}
				}
			}
			//cout << "BFS resulst" << endl;
			//printTable();
		}
		int res = 0;
		for (vector<int> row : table) {
			for (int i : row) res += i;
		}
		return res;
	}
	
	int main() {
		Input2();
		cout << Rotate();
		return 0;
	}
	
	
	
	
