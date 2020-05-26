---
layout: post
title: [Samsung SW - Marbles]
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

	﻿[101. [BACKJOON – SAMSUNG SW : Marbles]]
	- I spent 6 hours…
	- At first, I used DFS but some test case was not solved.
	> I think I solved rightly, but my print method might have been wrong…
	- So I refered to a blog and used BFS
	- see the code.
	#include<iostream>
	#include<vector>
	#include<algorithm>
	#include<climits>
	#include<fstream>
	#include<queue>
	
	using namespace std;
	
	vector<vector<int>> direction = { {0,-1},{0,1},{-1,0},{1,0} };//left right up dwon
	int visit[10][10][10][10];
	
	vector<vector<char>> makeTable2(vector<int>& position) {
		std::ifstream in("C:\\Users\\gjsgu\\Desktop\\Algorithm\\test_case.txt");
		string row;
		int N;
		int M;
		if (in.is_open()) {
			in >> N;
			in >> M;
		}
		vector<vector<char>> table(N+2, vector<char>(M+2, '#'));
		for (int i = 0; i < N; i++) {
			in >> row;
			for (int j = 0; j < M; j++) {
				if (row[j] == 'R') {
					position[0] = i;
					position[1] = j;
				}
				if (row[j] == 'B') {
					position[2] = i;
					position[3] = j;
				}
				if (row[j] == 'O') {
					position[4] = i;
					position[5] = j;
				}
				table[i][j] = row[j];
			}
		}
		return table;
	}
	
	vector<vector<char>> makeTable(vector<int>& position) {
		string row;
		int N;
		int M;
		cin >> N;
		cin >> M;
		vector<vector<char>> table(N+2, vector<char>(M+2, '#'));
		for (int i = 0; i < N; i++) {
			cin >> row;
			for (int j = 0; j < M; j++) {
				if (row[j] == 'R') {
					position[0] = i;
					position[1] = j;
				}
				if (row[j] == 'B') {
					position[2] = i;
					position[3] = j;
				}
				if (row[j] == 'O') {
					position[4] = i;
					position[5] = j;
				}
				table[i][j] = row[j];
			}
		}
		return table;
	}
	void printTable(vector<vector<char>>& table) {
		cout << endl;
		for (vector<char> row : table) {
			for (char c : row) {
				cout << c;
			}
			cout << endl;
		} 
	}
	
	void moveTo(vector<vector<char>>& table,int& x, int& y, int k) {
		while (true) {
			x += direction[k][0]; y += direction[k][1];
			//cout << " x : " << x << " y : " << y << endl;
			if (table[x][y] == '#') {
				x -= direction[k][0]; y -= direction[k][1];
				break;
			}
			else if (table[x][y] == 'O') break;
		}
	}
	
	
	int BFS(vector<vector<char>>& table,int a,int b,int c, int d,int e,int f) {
		int count=0;
		queue<vector<int>> que;
		que.push({ a,b,c,d,0 });
		visit[a][b][c][d] = 1;
		while (!que.empty()) {
			vector<int> cur = que.front(); que.pop();
			a = cur[0]; b = cur[1]; c = cur[2]; d = cur[3]; count = cur[4];
			//cout << a << " " << b << " " << c << " " << d << endl;
			if (count > 10) break; // when the depth is over 10
			if (a == e && b == f) return count; // when red ball is placed at th hole.
			//ball move
			for (int i = 0; i < 4; i++) {
				int rx = a; int ry = b; int bx = c; int by = d;
				moveTo(table,rx, ry, i);
				moveTo(table,bx, by, i);
				if (bx == e && by == f) continue;
				if (rx == bx && ry == by) { //if they are overlapped.
					switch (i){
					case 0: //left
						b < d ? by++ : ry++;
						break;
					case 1: //right
						d < b ? by-- : ry--;
						break;
					case 2: //up
						a < c ? bx++ : rx++;
						break;
					case 3: //down
						c < a ? bx-- : rx--;
						break;
					}
				}
				if (!visit[rx][ry][bx][by]) {
					//cout << "input que : " << rx << " "<< ry << " " << bx << " " << by << endl;
					que.push({ rx,ry,bx,by,count + 1 });
					visit[rx][ry][bx][by] = 1;
				}
			}
		}
		return -1;
	}
	
	int main() {
		int answer=-1;
		vector<int> position(6,0);
		vector<vector<char>> table = makeTable(position);
		//vector<vector<char>> table = makeTable2(position);
		visit[position[0]][position[1]][position[2]][position[3]] = 1;
		//printTable(table);
		answer = BFS(table, position[0], position[1], position[2], position[3],position[4],position[5]);
		printf("%d", answer);
		return 0;
	}
	
