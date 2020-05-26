---
layout: post
title: [Samsung SW - Cubing]
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

	﻿[118. [BACKJOON – SAMSUNG SW : Cubing]]
	- it was not a solving algorhthm! I think it was just a time consuming work actually.
	- making cube and make it move following the given rules. was suck!
	- see the code.
	#include<iostream>
	#include<fstream>
	#include<vector>
	
	using namespace std;
	
	
	vector<vector<char>> front;
	vector<vector<char>> back;
	vector<vector<char>> Left;
	vector<vector<char>> Right;
	vector<vector<char>> up;
	vector<vector<char>> down;
	vector<vector<string>> rule;
	int N;
	
	void Input() {
		ifstream in("C:\\Users\\gjsgu\\Desktop\\Algorithm\\test_case\\test_case_for_cubing.txt");
		if (in.is_open()) cout << "file is opened." << endl;
		in >> N;
		int temp;
		string rotate;
		rule.assign(N, vector<string>{});
		for (int i = 0; i < N; i++) {
			in >> temp;
			for (int j = 0; j < temp; j++) {
				in >> rotate;
				rule[i].push_back(rotate);
			}
		}
	}
	
	void Input2() {
		cin >> N;
		int temp;
		string rotate;
		rule.assign(N, vector<string>{});
		for (int i = 0; i < N; i++) {
			cin >> temp;
			for (int j = 0; j < temp; j++) {
				cin >> rotate;
				rule[i].push_back(rotate);
			}
		}
	}
	
	
	void printRule() {
		for (vector<string> row : rule) {
			for (int i = 0; i < row.size(); i++) {
				cout << row[i];
			}
			cout << endl;
		}
	}
	
	void initCube() {
		front = { {'r','r','r'},{'r','r','r'},{'r','r','r'} }; 
		back = { {'o','o','o'},{'o','o','o'},{'o','o','o'} };
		Left = { {'g','g','g'},{'g','g','g'},{'g','g','g'} };
		Right = { {'b','b','b'},{'b','b','b'},{'b','b','b'} };
		up = { {'w','w','w'},{'w','w','w'},{'w','w','w'} };
		//up = { {'1','2','3'},{'4','5','6'},{'7','8','9'} };
		down = { {'y','y','y'},{'y','y','y'},{'y','y','y'} };
		
	}
	
	vector<vector<char>> moveFront(vector<vector<char>> Left, string dir) {
		char temp,temp2,temp3;
		if (dir == "-") {
			temp = Left[0][0]; temp2 = Left[0][1];
			Left[0][0] = Left[0][2]; Left[0][1] = Left[1][2]; Left[0][2] = Left[2][2]; Left[1][2] = Left[2][1]; Left[2][2] = Left[2][0]; Left[2][1] = Left[1][0]; 
			Left[2][0] = temp; Left[1][0] = temp2;
		}
		else {
			temp = Left[0][0]; temp2 = Left[1][0];
			Left[0][0] = Left[2][0]; Left[1][0] = Left[2][1]; Left[2][0] = Left[2][2]; Left[2][1] = Left[1][2]; Left[2][2] = Left[0][2]; Left[1][2] = Left[0][1];
			Left[0][2] = temp; Left[0][1] = temp2;
		}
		return Left;
	}
	void moveSide(char& a, char& b, char& c, char& d, char& e, char& f, char& g, char& h, char& i, char& j, char& l, char& m,string dir) {
		char temp = a, temp2 = b, temp3 = c;
		if (dir == "-") {
			a = d; b = e; c = f; d = g; e = h; f = i; g = j; h = l; i = m; j = temp; l = temp2; m = temp3;
		}
		else {
			a = j; b = l; c = m; j = g; l = h; m = i; g = d; h = e; i = f; d = temp; e = temp2; f = temp3;
			
		}
	}
	
	
	void rotateCube(string side, string dir) {
		char temp, temp2, temp3;
		//cout << "<<"<<side<<">>" << endl;
		if (side == "L") {
			Left = moveFront(Left, dir);
			moveSide(front[0][0], front[1][0], front[2][0], down[0][0], down[1][0], down[2][0], back[0][0], back[1][0], back[2][0], up[0][0], up[1][0], up[2][0], dir);
		}
		else if (side == "R") {
			Right = moveFront(Right, dir);
			moveSide(front[0][2], front[1][2], front[2][2], up[0][2], up[1][2], up[2][2], back[0][2], back[1][2], back[2][2], down[0][2], down[1][2], down[2][2], dir);
		}
		else if (side == "U") {
			up = moveFront(up, dir);
			moveSide(front[0][2], front[0][1], front[0][0], Left[0][2], Left[0][1], Left[0][0], back[2][0], back[2][1], back[2][2], Right[0][2], Right[0][1], Right[0][0],dir);
		}
		else if (side == "D") {
			down = moveFront(down, dir);
			moveSide(front[2][0], front[2][1], front[2][2], Right[2][0], Right[2][1], Right[2][2], back[0][2], back[0][1], back[0][0], Left[2][0], Left[2][1], Left[2][2], dir);
		}
		else if (side == "F") {
			front = moveFront(front, dir);
			moveSide(up[2][0], up[2][1], up[2][2], Right[0][0], Right[1][0], Right[2][0], down[0][2], down[0][1], down[0][0], Left[2][2], Left[1][2], Left[0][2], dir);
		}
		else if (side == "B") {
			back = moveFront(back, dir);
			moveSide(up[0][2], up[0][1], up[0][0], Left[0][0], Left[1][0], Left[2][0], down[2][0], down[2][1], down[2][2], Right[2][2], Right[1][2], Right[0][2], dir);
		}
	}
	
	void printCubeTop() {
		for (vector<char> row : up) {
			for (char c : row) {
				cout << c;
			}
			cout << endl;
		}
	}
	
	void printCube() {
		cout << "up" << endl;
	
		for (vector<char> row : up) {
			for (char c : row) {
				cout << c;
			}
			cout << endl;
		}
		cout << endl;
		cout << "front" << endl;
		for (vector<char> row : front) {
			for (char c : row) {
				cout << c;
			}
			cout << endl;
		}
		cout << endl;
		cout << "Left" << endl;
		for (vector<char> row : Left) {
			for (char c : row) {
				cout << c;
			}
			cout << endl;
		}
		cout << endl;
		cout << "Right" << endl;
		for (vector<char> row : Right) {
			for (char c : row) {
				cout << c;
			}
			cout << endl;
		}	
		cout << endl;
		cout << "back" << endl;
		for (vector<char> row : back) {
			for (char c : row) {
				cout << c;
			}
			cout << endl;
		}
		cout << endl;
		cout << "down" << endl;
		for (vector<char> row : down) {
			for (char c : row) {
				cout << c;
			}
			cout << endl;
		}
	}
	
	void followingRules() {
		string side; string dir;
		for (int i = 0; i < N; i++) {
			initCube();
			for (int j = 0; j < rule[i].size(); j++) {
				side = rule[i][j][0]; dir = rule[i][j][1];
				rotateCube(side, dir);
			}
			printCubeTop();
			//printCube();
		}
	}
	
	
	
	int main() {
		//Input();
		Input2();
		followingRules();
		return 0;
	}
	
