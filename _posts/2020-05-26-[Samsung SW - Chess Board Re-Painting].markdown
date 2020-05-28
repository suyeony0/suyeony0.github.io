---
layout: post
title: [Samsung SW - Chess Board Re-Painting]
data: 2020-05-26
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}
	﻿[184. [SAMSUNG SW – Chess Board Re-Painting]
	- it was a slicing and brute force problem. but understading the problem is pretty hard. since they took a word “Square”. I’ve been confused whether the “Square” is chess board’s small 1x1 square or 8x8 whole square.
	- except that there was nothing to make me confused.
	- see the code.
	#include<iostream>
	#include<vector>
	#include<array>
	#define min(a,b) a>b?b:a
	using namespace std;
	int N, M;
	vector<vector<char>> table;
	array<array<char, 8>, 8> board;
	
	void Slicing(int x, int y){
		for (int i = x; i < x + 8; i++) {
			for (int j = y; j < y + 8; j++) {
				board[i-x][j-y] = table[i][j];
			}
		}
	}
	int getMinimum() {
		//when start with white
		int white_num = 0;
		for (int i = 0; i < 8; i++) {
			for (int j = 0; j < 8; j++) {
				if ((i + j) % 2 == 0 && board[i][j] == 'B') white_num++;
				if ((i + j) % 2 == 1 && board[i][j] == 'W') white_num++;
			}
		}
		//when start with black
		int black_num = 0;
		for (int i = 0; i < 8; i++) {
			for (int j = 0; j < 8; j++) {
				if ((i + j) % 2 == 0 && board[i][j] == 'W') black_num++;
				if ((i + j) % 2 == 1 && board[i][j] == 'B') black_num++;
			}
		}
		return min(black_num, white_num);
	}
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
		//get input
		cin >> N >> M;
		table.assign(N, vector<char>(M, 0));
		string input;
		for (int i = 0; i < N; i++) {
			cin >> input;
			for (int j = 0; j < M; j++) {
				table[i][j] = input[j];
			}
		}
		//algorithm part
		int answer = 987654321;
		for (int i = 0; i + 7 < N; i++) {
			for (int j = 0; j + 7 < M; j++) {
				Slicing(i, j);
				answer=min(answer,getMinimum());
			}
		}
		cout << answer;
		return 0;
	}
	
{% endraw %}
