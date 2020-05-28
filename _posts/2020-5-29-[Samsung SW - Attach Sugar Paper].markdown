---
layout: post
title: [Samsung SW - Attach Sugar Paper]
date: 2020-5-29
description: txt to markdown
thumbnail: city2.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

```cpp
	﻿[172. [SAMSUNG - SW : Attach Sugar Paper]
	- below code is my wrong algorithm. I used BFS to find maximu size of block we can attach with current connected block. but it consider just first max block. so it’s wrong.
	- see the code.
	#include<iostream>
	#include<array>
	#include<queue>
	using namespace std;
	int dir[4][2] = { {-1,0}, {0,-1},{1,0},{0,1} }; // top left bottom right
	
	vector<int> rest = { 5,5,5,5,5,5 };
	int answer = 0;
	int blockSize(array<array<int, 10>, 10>& table, int x, int y) {
		int k=0;
		for (k = 1; k < 5 ; k++) {
			if (x + k >= 10 || y + k >= 10) return k - 1;
			for (int i = x; i <= x + k ; i++) if (table[i][y + k] != 1) return k-1;
			for (int j = y; j < y + k ; j++) if (table[x + k][j] != 1) return k-1;
		}
		if (k == 5) return k - 1;
		return k;
	}
	
	void attach(array<array<int, 10>, 10>& table, int x, int y, int m) {
		table[x][y] = 0;
		for (int k = 1; k <= m; k++) {
			for (int i = x; i <= x + k && x + k < 10 && y + k < 10; i++) table[i][y + k] = 0;
			for (int j = y; j < y + k && y + k < 10 && x + k < 10; j++) table[x + k][j] = 0;
		}
	}
	
	void findBlock(array<array<int,10>,10>& table, int& number_of_one) {
		queue<pair<int, int>> que;
		int sx, sy;
		bool flag = true;
		for (int i = 0; i < 10 && flag; i++) {
			for (int j = 0; j < 10; j++) {
				if (table[i][j] == 1) {
					sx = i; sy = j;
					flag = false;
					break;
				}
			}
		}
		que.push(make_pair(sx,sy));
		//BFS
		int max_block_size = 0; int mx=sx; int my=sy;
		vector<vector<int>> visit(10, vector<int>(10, 0));
		int temp_size = 0;
		while (!que.empty() && max_block_size<5) {
			int x = que.front().first; int y = que.front().second; que.pop();
			if (visit[x][y] == 0) {
				visit[x][y] = 1;
				temp_size = blockSize(table, x, y);
				if (max_block_size < temp_size && rest[temp_size]!=0) {
					max_block_size = temp_size;
					mx = x; my = y;
				}
			}
			for (int i = 0; i < 4; i++) {
				int dx = x+dir[i][0]; int dy = y+dir[i][1];
				if ( dx >= 0 && dy >= 0 && dx < 10 && dy < 10&&visit[dx][dy] == 0 && table[dx][dy] == 1 )
					que.push(make_pair(dx,dy));
			}
		}
		
		if (rest[max_block_size] != 0) {
			cout << "mx, my, size : " << mx << "," << my << "," << max_block_size + 1 << endl;
			attach(table, mx, my, max_block_size);
			number_of_one -= (max_block_size + 1) * (max_block_size + 1);
			answer++;
			rest[max_block_size]--;
		}
		
	}
	
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
		array<array<int, 10>, 10> table;
		// get input
		int number_of_one = 0;
		for (int i = 0; i < 10; i++)
			for (int j = 0; j < 10; j++) {
				cin >> table[i][j];
				if (table[i][j] == 1) number_of_one++;
			}
	
		int loof_count = 0;
		//algorithm part
		while (number_of_one > 0) {
			if (loof_count >= 50) {
				answer = -1;
				break;
			}
			findBlock(table, number_of_one);
			loof_count++;
		}
		cout << answer;
		return 0;
	}
	- this is revised code. I used DFS to check all the possible block I can take with current coordinates.
	- by recording one’s position, I can have terminated DFS loof.
	- see the code.
	#include<iostream>
	#include<array>
	#include<vector>
	#define min(a,b) a>b?b:a
	using namespace std;
	
	array<int, 5 > rest_paper= {5, 5, 5, 5, 5};
	
	int answer = 987654321;
	int number_of_one = 0;
	vector<pair<int, int>> one_pos;
	
	bool attachPaper(array<array<int, 10>, 10>& temp,int x,int y, int k) {
		bool flag = true;
		for (int i = x; i <= k+x&&flag; i++) {
			for (int j = y; j <= k + y; j++) {
				if (temp[i][j] == 0) {
					flag = false;
					break;
				}
				temp[i][j] = 0;
			}
		}
		return flag;
	}
	
	void DFS(array<array<int, 10>, 10> temp,int used_paper,int start,int used_one) {
		if (used_one == number_of_one) {
			answer = min(answer, used_paper);
			return;
		}
		else if (used_one > number_of_one) return;
		if (start >= one_pos.size()) {
			return;
		} 
		int x = one_pos[start].first; int y = one_pos[start].second;
		if (temp[x][y] == 0) {
			DFS(temp, used_paper, start + 1, used_one);
		}
		for (int j = 0; j < 5; j++) {
			if (rest_paper[j] == 0) continue;
			if (x + j >= 10 || y + j >= 10) break;
			rest_paper[j]--;
			array<array<int, 10>, 10> next_table=temp;
			bool flag=attachPaper(next_table, x, y, j);
			used_one += (j + 1) * (j + 1);
			if(flag) DFS(next_table, used_paper+1,start+1,used_one);
			used_one -= (j + 1) * (j + 1);
			rest_paper[j]++;
		}
		
	}
	
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
		array<array<int, 10>, 10> table;
		// get input
		for (int i = 0; i < 10; i++)
			for (int j = 0; j < 10; j++) {
				cin >> table[i][j];
				if (table[i][j] == 1) {
					number_of_one++;
					one_pos.emplace_back(make_pair(i, j));
				}
			}
		// algorithm part
		DFS(table, 0, 0, 0);
		if (answer == 987654321) cout << -1;
		else cout << answer;
		return 0;
	}
	
```
