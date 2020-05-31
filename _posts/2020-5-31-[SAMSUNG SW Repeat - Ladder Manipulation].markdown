---
layout: post
title: [SAMSUNG SW Repeat - Ladder Manipulation]
date: 2020-5-31
description: txt to markdown
thumbnail: work1.jpg
categories: SAMSUNG_SW

# Information for the author block
author : Loui
---

```cpp

{% raw %}

	﻿[14. SAMSUNG SW : Ladder Manipulation]
	- it was a combination and simulation problem. combination was the main point.
	- I used visit array first to determine a lane currently consider is a valid place to put a ladder. but time limit exceeded occurred.
	- so I removed the visit array and just used given table.
	- by the way, I implemented combination part using DFS. there was a restriction of maximum number we had to choose and when it is less than the maximum number, I also had to check simulation.
	- see the code.
	#include<iostream>
	#include<vector>
	#define min(a,b) a>b?b:a
	using namespace std;
	
	int N, M, H;
	vector<vector<int>> table;
	//vector<vector<vector<bool>>> visit;
	vector<pair<int, int>> space;
	int num_of_space;
	int answer = 10;
	bool Simulation() {
		
		for (int j = 0; j < M; j++) {
			int x = 0; int y = j; int px = 0; int py = j;
			while (x < N) {
				if (y - 1 >= 0 && table[x][y - 1] == 2) y -= 1;
				else if (table[x][y] == 2) y += 1;
				x += 1;
			}
			if (j != y) return false;
		}
		return true;
	}
	
	
	void Permutation(int cnt, int start) {
		if (cnt == 4) return;
		if (Simulation()) {
			answer = min(answer, cnt);
			return;
		}
		for (int i = 0; i < N; i++) {
			for (int j = start; j < M-1; j++) {
				if (table[i][j] == 2) continue;
				if (j - 1 >= 0 && table[i][j - 1] == 2) continue;
				if (j + 1 < M && table[i][j + 1] == 2) continue;
				table[i][j] = 2;
				Permutation(cnt + 1, j);
				table[i][j] = 0;
			}
		}
	
	
	}
	
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
	
		//get input
		cin >> M >> H >> N; // M is row, N is col, H is number of given horizon line.
		table.assign(N, vector<int>(M, 0));
		int x, y;
		for (int i = 0; i < H; i++) {
			cin >> x >> y;
			x -= 1; y -= 1;
			table[x][y] = 2;
		}
	
		//algorithm part
		
		Permutation(0, 0);
		if (answer == 10) cout << -1;
		else cout << answer;
		return 0;
	}
	
	
{% endraw %}
```

