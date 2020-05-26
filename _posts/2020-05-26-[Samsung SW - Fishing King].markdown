---
layout: post
title: [Samsung SW - Fishing King]
data: 2020-05-26
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}
	﻿[146. [SAMSUNG – SW :Fishing King]]
	- I have a so much curiousity of SAMSUNG’s simulation algorithm test cases.
	- this problem also has some weird things.
	- At first, I solved correctly but time limit exceeded occurred. so I change my code with same algorithm but faster, but it didn’t work. what the heck? how come? algorithm was perfectly same and I just chagned container to reduce traversal time.
	- I don’t understand still now.
	- Finally, I used my first submission with more efficient shark move.
	- see the code.
	#include<iostream>
	#include<fstream>
	#include<vector>
	#include<unordered_map>
	#include<algorithm>
	#include<map>
	using namespace std;
	
	int dir[4][2] = { {-1,0},{1,0},{0,1},{0,-1} }; // up, down, right, left
	
	int r, c, m;
	int get_size = 0;
	vector<vector<vector<int>>> table; //speed, direction, size
	map<pair<int, int>, vector<vector<int>>> shark_pos;
	void Input() {
		ifstream in("C:\\Users\\gjsgu\\Desktop\\Algorithm\\test_case\\test_case_for_fishing_king.txt");
		if (in.is_open()) cout << "file is opened." << endl;
		in >> r; in >> c; in >> m;
		table.assign(r, vector<vector<int>>(c));
		int a, b, c, d, e;
		for (int i = 0; i < m; i++) {
			in >> a; in >> b; in >> c; in >> d; in >> e;
			table[a - 1][b - 1] = vector<int>{ c,d - 1,e };
		}
	}
	void Input2() {
		cin >> r; cin >> c; cin >> m;
		table.assign(r, vector<vector<int>>(c));
		int a, b, c, d, e;
		for (int i = 0; i < m; i++) {
			cin >> a; cin >> b; cin >> c; cin >> d; cin >> e;
			table[a - 1][b - 1] = vector<int>{ c,d - 1,e };
		}
	}
	
	
	void GetShark(int col) {
		for (int i = 0; i < r; i++) {
			if (!table[i][col].empty()) {
				get_size += table[i][col][2];
				table[i][col].clear();
				return;
			}
		}
	}
	
	void Moving(int x, int y, int shark_size) {
		int speed = table[x][y][0];
		int cur_dir = table[x][y][1];
		// up, down, right, left ==> 0,1,2,3
		int temp_speed;
		if (cur_dir == 0) temp_speed = speed % ((r - 1) * 2);
		else if (cur_dir == 1) temp_speed = speed % ((r - 1) * 2);
		else if (cur_dir == 2) temp_speed = speed % ((c - 1) * 2);
		else temp_speed = speed % ((c - 1) * 2);
	
		for (int i = 0; i < temp_speed; i++) {
			int tx = x + dir[cur_dir][0]; int ty = y + dir[cur_dir][1];
			if (tx < 0) {
				cur_dir = 1;
				x = 1;
			}
			else if (ty < 0) {
				cur_dir = 2;
				y = 1;
			}
			else if (tx >= r) {
				cur_dir = 0;
				x = r - 2;
			}
			else if (ty >= c) {
				cur_dir = 3;
				y = c - 2;
			}
			else {
				x = tx; y = ty;
			}
		}
		shark_pos[make_pair(x, y)].push_back(vector<int>{speed, cur_dir, shark_size});
	}
	
	void MoveShark() {
		shark_pos.clear();
		for (int i = 0; i < r; i++) {
			for (int j = 0; j < c; j++) {
				if (!table[i][j].empty()) {
					Moving(i, j, table[i][j][2]);
				}
			}
		}
		table = vector<vector<vector<int>>>(r, vector<vector<int>>(c));
		for (map<pair<int, int>, vector<vector<int>>>::iterator iter = shark_pos.begin(); iter != shark_pos.end(); iter++) {
			sort(iter->second.begin(), iter->second.end(), [](vector<int> a, vector<int> b) {return a[2] > b[2]; });
			table[iter->first.first][iter->first.second] = vector<int>{ iter->second[0][0],iter->second[0][1],iter->second[0][2] };
		}
	
	}
	
	void printTable() {
		for (vector<vector<int>> row : table) {
			for (vector<int> srk : row) {
				if (srk.empty()) cout << "(0 0 0)" << " ";
				else cout << "(" << srk[0] << " " << srk[1] << " " << srk[2] << ")" << " ";
			}
			cout << endl;
		}
		cout << endl;
	}
	
	void Fishing() {
		//printTable();
		for (int i = 0; i < c; i++) {
			GetShark(i);
			//cout << "<<get>>" << endl;
			//printTable();
			MoveShark();
			//cout << "<<move>>" << endl;
			//printTable();
		}
	}
	
	int main() {
		Input2();
		Fishing();
		cout << get_size;
		return 0;
	}
	
{% endraw %}
