---
layout: post
title: [SAMSUNG SW - Water Bottle]
date: 2020-6-6
description: txt to markdown
thumbnail: city2.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

﻿[206. SAMSUNG SW : Water Bottle]
- it was a simulation problem with BFS.
- But at first, I had no idea how to solve this problem.
- the key was just to implement pouring water from one to another.
- I used BFS to record current bottles’ water volume and visit 3d array to check whether current bottles’ volume is already checked or not.
- I spent 26 minutes and 14 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<set>
#include<queue>
using namespace std;
vector<int> bottle(3, 0);
vector<int> water(3, 0);
bool visit[200][200][200];
set<int> answer;

inline bool isValid(int a,int b,int c) {
	if (visit[a][b][c]) return false;
	return true;
}

inline bool isFull(int i,int c,int n) {
	if ((bottle[i] - c) - n < 0) return true;
	return false;
}

void BFS() {
	queue<vector<int>> que;
	que.push(vector<int>{0, 0, water[2]});
	visit[0][0][water[2]] = true;
	answer.insert(water[2]);
	while (!que.empty()) {
		int a = que.front()[0]; int b = que.front()[1]; int c = que.front()[2];
		que.pop();
		int na, nb, nc;
		if (a == 0) answer.insert(c);
		if (a != 0) {
			if (isFull(1,b,a)) {
				na = a - (bottle[1] - b);
				nb = bottle[1];
			}
			else {
				na = 0;
				nb = a + b;
			}
			if (visit[na][nb][c] == false) {
				visit[na][nb][c] = true;
				que.push(vector<int>{na, nb, c});
			}
			if (isFull(2, c, a)) {
				na = a - (bottle[2] - c);
				nc = bottle[2];
			}
			else{
				na = 0;
				nc = a + c;
			}
			if (visit[na][b][nc] == false) {
				visit[na][b][nc] = true;
				que.push(vector<int>{na, b, nc});
			}

		}
		if (b != 0) {
			if (isFull(0, a, b)) {
				nb = b - (bottle[0] - a);
				na = bottle[0];
			}
			else {
				nb = 0;
				na = a + b;
			}
			if (visit[na][nb][c] == false) {
				visit[na][nb][c] = true;
				que.push(vector<int>{na, nb, c});
			}
			if (isFull(2, c, b)) {
				nb = b - (bottle[2] - c);
				nc = bottle[2];
			}
			else {
				nb = 0;
				nc = b + c;
			}
			if (visit[a][nb][nc] == false) {
				visit[a][nb][nc] = true;
				que.push(vector<int>{a, nb, nc});
			}

		
		}
		if (c != 0) {
			if (isFull(0, a, c)) {
				nc = c - (bottle[0] - a);
				na = bottle[0];
			}
			else {
				nc = 0;
				na = a + c;
			}
			if (visit[na][b][nc] == false) {
				visit[na][b][nc] = true;
				que.push(vector<int>{na, b, nc});
			}
			if (isFull(1, b, c)) {
				nc = c - (bottle[1] - b);
				nb = bottle[1];
			}
			else {
				nc = 0;
				nb = b + c;
			}
			if (visit[a][nb][nc] == false) {
				visit[a][nb][nc] = true;
				que.push(vector<int>{a, nb, nc});
			}
		}
	}

}


int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input;
	cin >> bottle[0] >> bottle[1] >> bottle[2];
	water[2] = bottle[2];

	//algorithm part
	BFS();
	for (set<int>::iterator iter = answer.begin(); iter != answer.end(); iter++)
		cout << *iter << " ";
	return 0;

}



{% endraw %}
```

