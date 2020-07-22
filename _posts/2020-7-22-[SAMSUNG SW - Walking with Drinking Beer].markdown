---
layout: post
title: [SAMSUNG SW - Walking with Drinking Beer]
date: 2020-7-22
description: txt to markdown
thumbnail: work1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

﻿[244. SAMSUNG SW – Walking with Drinking Beer]
- I thought it was a BFS-simulation problem. But it was not.
- Since to solve this problem using BFS, it takes so much time.
- So I changed my algorithm. it was easy.
- First, pushing every beer shop or destination where we can reach with 20 beers from a current position to a queue.
- Second, Using the queue, iterating “First”, and if we can reach destination, return true. or return false.
- I spent 39 minutes and 29 seconds. Because of wrong thought at first.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<queue>
#define ORIGIN 32768

using namespace std;

int N, T;
int sx, sy, dx, dy;
vector<bool> visit;
vector<pair<int, int>> beer;

bool BFS() {
	queue<vector<int>> que;
	que.push(vector<int>{sx, sy});

	while (!que.empty()) {
		int x = que.front()[0]; int y = que.front()[1]; que.pop();
		if (x == dx && y == dy) return true;	
		for (int i = 0; i < N+1; i++) {
			if (visit[i] == true) continue;
			int nx = beer[i].first; int ny = beer[i].second;
			if (abs(x -nx) + abs(y - ny) <= 1000) {
				que.push(vector<int>{nx,ny});
				visit[i] = true;
			} 
		}
	}
	return false;
}


int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	cin >> T;
	for (int test = 0; test < T; test++) {
		
		//get input
		cin >> N;
		cin >> sx >> sy;
		visit.assign(N+1, false);
		beer.assign(N+1, pair<int, int>());
		for (int i = 1; i < N+1; i++) cin >> beer[i].first >> beer[i].second;
		cin >> dx >> dy;
		beer[0].first = dx; beer[0].second = dy;
		//algorithm part
		if (BFS()) cout << "happy" << endl;
		else cout << "sad" << endl;
	}
	return 0;
}

{% endraw %}
```

