---
layout: post
title: [SAMSUNG SW Repeat - Cubing]
date: 2020-6-1
description: txt to markdown
thumbnail: city2.jpg
categories: SAMSUNG_SW

# Information for the author block
author : Loui
---

```cpp

{% raw %}

	﻿[17. SAMSUNG SW : Cubing]
	- how hard to solve thist problem! there was so many hand-work.
	- it was a simulation problem. but to simulate rotating a cube, I had to give all the index releated with current side of cube and direction.
	- I spent 1 hour and 51 minutes and 39 seconds.
	- see the code.
	#include<iostream>
	#include<vector>
	using namespace std;
	
	int T,N;
	vector<pair<char, char>> rotation;
	
	
	void Rotate(vector<vector<char>>& cur, char dir) {
		char temp;
		if (dir == '+') {
			temp = cur[0][0];
			cur[0][0] = cur[2][0]; cur[2][0] = cur[2][2]; cur[2][2] = cur[0][2]; cur[0][2] = temp;
			temp = cur[0][1];
			cur[0][1] = cur[1][0]; cur[1][0] = cur[2][1]; cur[2][1] = cur[1][2]; cur[1][2] = temp;
			
		}
		else {
			temp = cur[0][0];
			cur[0][0] = cur[0][2]; cur[0][2] = cur[2][2]; cur[2][2] = cur[2][0]; cur[2][0] = temp;
			temp = cur[0][1];
			cur[0][1] = cur[1][2]; cur[1][2] = cur[2][1]; cur[2][1] = cur[1][0]; cur[1][0] = temp;
		}
	}
	
	void subRotate(vector<char*> lst, char dir) {
		char temp1,temp2,temp3;
		if (dir == '+') {
			temp1 = *lst[0]; temp2 = *lst[1]; temp3 = *lst[2];
			*lst[2] = *lst[11]; *lst[1] = *lst[10]; *lst[0] = *lst[9];
			*lst[11] = *lst[8]; *lst[10] = *lst[7]; *lst[9] = *lst[6];
			*lst[8] = *lst[5]; *lst[7] = *lst[4]; *lst[6] = *lst[3];
			*lst[5] = temp3; *lst[4] = temp2; *lst[3] = temp1;
			
			
		}
		else {
			temp1 = *lst[0]; temp2 = *lst[1]; temp3 = *lst[2];
			*lst[0] = *lst[3]; *lst[1] = *lst[4]; *lst[2] = *lst[5];
			*lst[3] = *lst[6]; *lst[4] = *lst[7]; *lst[5] = *lst[8];
			*lst[6] = *lst[9]; *lst[7] = *lst[10]; *lst[8] = *lst[11];
			*lst[9] = temp1; *lst[10] = temp2; *lst[11] = temp3;
			
		}
		return;
	}
	
	
	
	void Play(vector<vector<char>> U, vector<vector<char>> F, vector<vector<char>> B, vector<vector<char>> D, vector<vector<char>> L, vector<vector<char>> R) {
		for (pair<char, char> rot : rotation) {
			switch (rot.first) {
			case 'B' :
				Rotate(B, rot.second); 
				subRotate(vector<char*>{&U[0][2], &U[0][1], &U[0][0], &L[0][0], &L[1][0], &L[2][0], &D[2][0], &D[2][1], &D[2][2], &R[2][2], &R[1][2], &R[0][2]}, rot.second);
				break;
			case 'U':
				Rotate(U, rot.second);
				subRotate(vector<char*>{&B[0][2], & B[0][1], & B[0][0], & R[0][2], & R[0][1], & R[0][0], & F[0][2], & F[0][1], & F[0][0], & L[0][2], & L[0][1], & L[0][0]}, rot.second);
				break;
			case 'F':
				Rotate(F, rot.second);
				subRotate(vector<char*>{&U[2][0], & U[2][1], & U[2][2], & R[0][0], & R[1][0], & R[2][0], & D[0][2], & D[0][1], & D[0][0], & L[2][2], & L[1][2], & L[0][2]}, rot.second);
				break;
			case 'D':
				Rotate(D, rot.second);
				subRotate(vector<char*>{&F[2][0], & F[2][1], & F[2][2], & R[2][0], & R[2][1], & R[2][2], & B[2][0], & B[2][1], & B[2][2], & L[2][0], & L[2][1], & L[2][2]}, rot.second);
				break;
			case 'L':
				Rotate(L, rot.second);
				subRotate(vector<char*>{&U[0][0], & U[1][0], & U[2][0], & F[0][0], & F[1][0], & F[2][0], & D[0][0], & D[1][0], & D[2][0], & B[2][2], & B[1][2], & B[0][2]}, rot.second);
				break;
			case 'R':
				Rotate(R, rot.second);
				subRotate(vector<char*>{&U[2][2], & U[1][2], & U[0][2], & B[0][0], & B[1][0], & B[2][0], & D[2][2], & D[1][2], & D[0][2], & F[2][2], & F[1][2], & F[0][2]}, rot.second);
				break;
			}
		}
		for (vector<char> row : U) {
			for (char c : row) {
				cout << c;
			}
			cout << endl;
		}
	}
	
	
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
		
	
		// cube initialize.
		vector<vector<char>> U = { {'w','w','w'},{'w','w','w'},{'w','w','w'} };
		vector<vector<char>> F = { {'r','r','r'},{'r','r','r'},{'r','r','r'} };
		vector<vector<char>> D = { {'y','y','y'},{'y','y','y'},{'y','y','y'} };
		vector<vector<char>> B = { {'o','o','o'},{'o','o','o'},{'o','o','o'} };
		vector<vector<char>> L = { {'g','g','g'},{'g','g','g'},{'g','g','g'} };
		vector<vector<char>> R = { {'b','b','b'},{'b','b','b'},{'b','b','b'} };
	
		//get number of testcase;
		cin >> T;
		for (int q = 0; q < T; q++) {
			//get input
			cin >> N;
			rotation.assign(N, pair<char, char>());
			for (int i = 0; i < N; i++) cin >> rotation[i].first >> rotation[i].second;
			Play(U, F, B, D, L, R);
		}
		return 0;
	
	}
	
{% endraw %}
```

