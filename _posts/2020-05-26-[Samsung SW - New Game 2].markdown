---
layout: post
title: {% raw %}[Samsung SW - New Game 2]{% endraw %}
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}
	﻿[149. [SAMSUNG – SW : New Game 2]] 
	- it was a stack handling problem. each shell of 2d array has stack for recoding pieces.
	- see the code.
	#include<iostream>
	#include<fstream>
	#include<vector>
	
	using namespace std;
	
	vector<vector<int>> table;
	vector<vector<vector<int>>> stacks;
	vector<vector<int>> pieces;
	int N, K;
	int dir[4][2] = { {0,1},{0,-1},{-1,0},{1,0} }; //right left up down
	
	void Input() {
		ifstream in("C:\\Users\\gjsgu\\Desktop\\Algorithm\\test_case\\test_case_for_new_game2.txt");
		if (in.is_open()) cout << "file is opened." << endl;
		in >> N; in >> K;
		table.assign(N, vector<int>(N, 0));
		stacks.assign(N, vector<vector<int>>(N, vector<int>(0)));
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < N; j++) {
				in >> table[i][j];
			}
		}
		int a, b, c;
		for (int i = 0; i < K; i++) {
			in >> a; in >> b; in >> c;
			pieces.push_back(vector<int>{a-1, b-1, c-1,i});
			stacks[a - 1][b - 1].push_back(i);
		}
	}
	
	void Input2() {
		cin >> N; cin >> K;
		table.assign(N, vector<int>(N, 0));
		stacks.assign(N, vector<vector<int>>(N, vector<int>(0)));
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < N; j++) {
				cin >> table[i][j];
			}
		}
		int a, b, c;
		for (int i = 0; i < K; i++) {
			cin >> a; cin >> b; cin >> c;
			pieces.push_back(vector<int>{a - 1, b - 1, c - 1, i});
			stacks[a - 1][b - 1].push_back(i);
		}
	}
	
	
	bool isStackedOver4(int x, int y) {
		if (stacks[x][y].size() >= 4) return true;
		return false;
	}
	
	int Game2() {
		int turn = 0;
		while (turn<=1000) {
			turn++;
			bool flag = false;
			//move
			for (int i = 0; i < K; i++) {
				int cur_dir = pieces[i][2]; int x = pieces[i][0]; int y = pieces[i][1];
				//cout << "piece : " << i << " x : " << x << " y : " << y << " dir : "<<cur_dir<<endl;
				int tx = x + dir[cur_dir][0]; int ty = y + dir[cur_dir][1];
				//cout << " tx : " << tx << " ty : " << ty << endl;
				//blue
				if (tx < 0 || ty < 0 || tx >= N || ty >= N || table[tx][ty] == 2) {
					//cout << "blue" << endl;
					if (cur_dir == 0) cur_dir = 1;
					else if (cur_dir == 1) cur_dir = 0;
					else if (cur_dir == 2) cur_dir = 3;
					else cur_dir = 2;
					int nx = x + dir[cur_dir][0]; int ny = y + dir[cur_dir][1];
					pieces[i][2] = cur_dir;
					//double blue
					if (nx < 0 || ny < 0 || nx >= N || ny >= N || table[nx][ny] == 2) continue;
					else { i--; continue; }
				}
				//get index of current stacks;
				int bottom;
				for (bottom = 0; bottom < stacks[x][y].size(); bottom++) if (stacks[x][y][bottom] == i) break;
				// when red
				if (table[tx][ty] == 1) {
					//cout << "red" << endl;
					for (int j = stacks[x][y].size() - 1; j >= bottom; j--) {
						stacks[tx][ty].push_back(stacks[x][y].back());
						pieces[stacks[x][y].back()][0] = tx; pieces[stacks[x][y].back()][1] = ty;
						stacks[x][y].pop_back();
					}
				}
				else {
					//cout << "white" << endl;
					for (int j = bottom; j < stacks[x][y].size(); j++) {
						stacks[tx][ty].push_back(stacks[x][y][j]);
						pieces[stacks[x][y][j]][0] = tx; pieces[stacks[x][y][j]][1] = ty;
					}
					int size = stacks[x][y].size();
					for (int j = bottom; j < size; j++) stacks[x][y].pop_back();
				}
			
				if (isStackedOver4(tx,ty)) { flag = true; break; }
			}
			if (flag) break;
		}
	
		if (turn > 1000) return -1;
		return turn;
	}
	
	int main() {
		Input();
		cout << Game2();
		return 0;
	
	}
	
	
	
	
	
{% endraw %}
