---
layout: post
title: [SAMSUNG SW Repeat - 2048]
date: 2020-5-28
description: txt to markdown
thumbnail: person1.jpeg
categories: SAMSUNG_SW

# Information for the author block
author : Loui
---

{% raw %}

	[2. SAMSUNG SW ? 2048]
	- this was a simulation problem and it was like just previous problem : ¡°Bids Escape 2¡±. Since we can just tilt the board and can not move each number of shell.
	- I used DFS and I implemented every direction¡¯s move.
	- I spent 28 minutes and 26 seconds.
	- see the code.
	#include<iostream>
	#include<vector>
	#define max(a,b) a>b? a:b
	using namespace std;
	
	
	int N;
	int answer = 0;
	
	void maxValue(vector<vector<int>>& table) {
		for (vector<int> row : table) {
			for (int i : row) answer = max(answer, i);
		}
	}
	
	vector<vector<int>> Move(vector<vector<int>> table,int dir) {
		vector<vector<bool>> visit(N, vector<bool>(N, false));
		switch (dir) {
		case 0: //left
			for (int i = 0; i < N; i++) {
				for (int j = 1; j < N; j++) {
					if (table[i][j] == 0) continue;
					for (int k = j; k >= 1; k--) {
						if (table[i][k - 1] == table[i][k] && visit[i][k - 1] == false) {
							visit[i][k - 1] = true;
							table[i][k - 1] *= 2;
							table[i][k] = 0;
							break;
						}
						else if (table[i][k - 1] == 0) {
							table[i][k - 1] = table[i][k];
							table[i][k] = 0;
						}
						else break;
					}
				}
			}
			break;
		case 1: // right
			for (int i = 0; i < N; i++) {
				for (int j = N - 2; j >= 0; j--) {
					if (table[i][j] == 0) continue;
					for (int k = j; k < N-1; k++) {
						if (table[i][k + 1] == table[i][k] && visit[i][k + 1] == false) {
							visit[i][k + 1] = true;
							table[i][k + 1] *= 2;
							table[i][k] = 0;
							break;
						}
						else if (table[i][k + 1] == 0) {
							table[i][k + 1] = table[i][k];
							table[i][k] = 0;
						}
						else break;
					}
				}
			}
			break;
		case 2: //north
			for (int j = 0; j < N; j++) {
				for (int i = 1; i < N; i++) {
					if (table[i][j] == 0) continue;
					for (int k = i; k >= 1; k--) {
						if (table[k - 1][j] == table[k][j] && visit[k - 1][j] == false) {
							visit[k - 1][j] = true;
							table[k - 1][j] *= 2;
							table[k][j] = 0;
							break;
						}
						else if (table[k - 1][j] == 0) {
							table[k - 1][j] = table[k][j];
							table[k][j] = 0;
						}
						else break;
					}
				}
			}
			break;
		case 3: //south
			for (int j = 0; j < N; j++) {
				for (int i = N - 2; i >= 0; i--) {
					if (table[i][j] == 0) continue;
					for (int k = i; k < N-1; k++) {
						if (table[k + 1][j] == table[k][j] && visit[k + 1][j] == false) {
							visit[k + 1][j] = true;
							table[k + 1][j] *= 2;
							table[k][j] = 0;
							break;
						}
						else if (table[k + 1][j] == 0) {
							table[k + 1][j] = table[k][j];
							table[k][j] = 0;
						}
						else break;
					
					}
				}
			}
			break;
	
		}
		return table;
	}
	
	
	void DFS(vector<vector<int>> table,int cnt) {
		if (cnt == 5) {
			maxValue(table);
			return;
		}
		for (int i = 0; i < 4; i++) 
			DFS(Move(table,i), cnt + 1);
	}
	
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
	
		//get input
		cin >> N;
		vector<vector<int>> table(N, vector<int>(N, 0));
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < N; j++) {
				cin >> table[i][j];
			}
		}
	
		//algorithm part
		DFS(table, 0);
		cout << answer;
		return 0;
	
	}
	
{% endraw %}
