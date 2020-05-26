---
layout: post
title: [Samsung SW - Rotate Array 4]
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}
	﻿[181. [SAMSUNG SW – Rotate Array 4]
	- this was a simulation problem.
	- I had to rotate part of given 2D array clock-wisely, and caclutate minimum value among each row.
	- I was able to choose rotating order to minimize the answer value. I implemented a permutation using DFS.
	- see the code.
	#include<iostream>
	#include<vector>
	#define min(a,b) a>b?b:a
	using namespace std;
	
	int N, M, K;
	int answer = 987654321;
	vector<vector<int>> rotates;
	vector<bool> visit;
	
	vector<vector<int>> rotateTable(vector<vector<int>> temp_table,vector<int> temp_rotate) {
		int r = temp_rotate[0] - 1; int c = temp_rotate[1] - 1; int s = temp_rotate[2];
		int tx = r - s; int ty = c - s; int bx = r + s; int by = c + s;
		//rotating part
		while (tx<bx && ty<by) {
			int start_val = temp_table[tx][ty];
			for (int i = tx; i < bx; i++) temp_table[i][ty] = temp_table[i + 1][ty];
			for (int j = ty; j < by; j++) temp_table[bx][j] = temp_table[bx][j + 1];
			for (int i = bx; i > tx; i--) temp_table[i][by] = temp_table[i - 1][by];
			for (int j = by; j > ty + 1; j--) temp_table[tx][j] = temp_table[tx][j - 1];
			temp_table[tx][ty + 1] = start_val;
			tx++; ty++; bx--; by--;
		}
		return temp_table;
	}
	
	void getMinimum(vector<vector<int>>& temp_table) {
		int minimum = 987654321;
		for (vector<int> row : temp_table) {
			int temp_sum = 0;
			for (int i : row) temp_sum += i;
			minimum = min(minimum, temp_sum);
		}
		answer = min(answer, minimum);
	}
	
	void permutation(vector<vector<int>> temp_table,int start) {
		if (start >= K) {
			getMinimum(temp_table);
			return;
		}
		for (int i = 0; i < K; i++) {
			if (visit[i] == false) {
				visit[i] = true;
				permutation(rotateTable(temp_table, rotates[i]), start + 1);
				visit[i] = false;
			}
		}
	}
	
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
		// get input
		cin >> N >> M >> K;
		vector<vector<int>> table(N, vector<int>(M, 0));
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < M; j++) {
				cin >> table[i][j];
			}
		}
		rotates.assign(K, vector<int>(3, 0));
		visit.assign(K, false);
		for (int i = 0; i < K; i++) cin >> rotates[i][0] >> rotates[i][1] >> rotates[i][2];
	
		//algorithm part
		permutation(table,0);
		cout << answer;
		return 0;
	}
	
{% endraw %}
