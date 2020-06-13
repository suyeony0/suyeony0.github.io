---
layout: post
title: [SAMSUNG SW - Postman Han Sang Duck]
date: 2020-6-13
description: txt to markdown
thumbnail: food2.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

﻿[215. SAMSUNG SW : Postman Han Sang Duck]
- At first, I thought it was just a BFS problem.
- But it was a DP Problem. I encounterd a quite difficult one for a long time.
- First, sort the given heights.
- Second, Find a minimum maximum height that Han Sang Duck can delivery all the post.
- Third, Find a maximum minimum height that Han Sang Duck can delivery all the post.
- If we find a valid height, calculate their difference.
- Go back to Second until the right pointer of sorted list reaches the list’s end.
- I spent 1 hours and 22 minutes and 48 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<set>
#define max(a,b) a>b? a:b
#define min(a,b) a>b? b:a
using namespace std;

int N, house;
int px, py;
vector<vector<int>> house_pos;
vector<vector<char>> table;
vector<vector<int>> height;
vector<vector<bool>> visit;
int dir[8][2] = { {-1,0},{-1,-1},{0,-1},{1,-1},{1,0},{1,1},{0,1},{-1,1} }; // start from north, gose by antiClock-wise
set<int> fatigue;
set<int>::iterator s_left;
set<int>::iterator s_right;
void DFS(int x, int y,int min_h, int max_h) {

	
	if (x < 0 || y < 0 || x >= N || y >= N || visit[x][y] || height[x][y]<min_h || height[x][y]>max_h) return;
	visit[x][y] = true;
	for (int d = 0; d < 8; d++)	DFS(x+dir[d][0], y+dir[d][1], min_h, max_h);
	
}

bool isValid() {
	for (vector<int> row : house_pos) if (visit[row[0]][row[1]] == false) return false;
	return true;
}

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	cin >> N;
	table.assign(N, vector<char>(N, 0));
	height.assign(N, vector<int>(N, 0));
	string input;
	for (int i = 0; i < N; i++) {
		cin >> input;
		for (int j = 0; j < N; j++) {
			table[i][j]=input[j];
			if (table[i][j] == 'K') {
				house += 1;
				house_pos.emplace_back(vector<int>{i, j});
			} 
			if (table[i][j] == 'P') {
				px = i; py = j;
			}
		}
	}
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < N; j++) {
			cin >> height[i][j];
			fatigue.insert(height[i][j]);
		}
	}
	s_left = fatigue.begin();
	s_right = fatigue.begin();
	//algorithm part
	int answer = 987654321;
	while (s_right!=fatigue.end()) { 
		while (s_left!=fatigue.end()) {
			visit.assign(N, vector<bool>(N, false));
			DFS(px, py, *s_left, *s_right);
			if (!isValid()) break;
			answer = min(answer, *s_right - *s_left);
			s_left++;
		}
		s_right++;
	}

	cout << answer;
	return 0;
}

{% endraw %}
```

