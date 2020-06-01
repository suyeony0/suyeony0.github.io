---
layout: post
title: [SAMSUNG SW Repeat - Chicken Delivery]
date: 2020-6-1
description: txt to markdown
thumbnail: food2.jpg
categories: SAMSUNG_SW

# Information for the author block
author : Loui
---

```cpp

{% raw %}

	﻿[16. SAMSUNG SW : Chicken Delivery]
	- this was a combination problem. but the key is the way to caclulate distance between each house and the closest chicken house.
	- I implemented Combination using DFS.
	- At first, I used BFS to find minimum distance to chicken house for each house. but time limit exceeded occurred.
	- the key was that we know chicken houses’ positions and houses’ positions. so we don’t need to implement BFS but just calculate minimum distance among all the chicken houses with a house.
	- I spent 42 minutes and 32 seconds.
	- see the code.
	#include<iostream>
	#include<vector>
	#include<queue>
	#include<array>
	#define min(a,b) a>b?b:a
	using namespace std;
	
	int N, M;
	array<array<int, 50>, 50> table = {0,};
	vector<pair<int, int>> chicken;
	vector<pair<int, int>> house;
	vector<pair<int, int>> chosen;
	int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };
	int answer = 987654321;
	int num_of_chicken;
	int BFS() {
		int res = 0;
		for (pair<int, int> h : house) {
			int hx = h.first; int hy = h.second;
			int minimum = 987654321;
			for (pair<int, int> c : chosen) minimum = min(minimum, abs(hx - c.first) + abs(hy - c.second));
			res += minimum;
		}
		return res;
	}
	
	void Combination(int cnt, int start) {
		if (cnt == M) {
			answer=min(answer,BFS());
			return;
		}
	
		for (int i = start; i < num_of_chicken; i++) {
			chosen.emplace_back(make_pair(chicken[i].first,chicken[i].second));
			Combination(cnt + 1, i + 1);
			chosen.pop_back();
		}
	}
	
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
	
		//get input
		cin >> N >> M;
		//table.assign(N, vector<int>(N, 0));
		int input;
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < N;j++) {
				cin >> input;
				if (input == 2) chicken.emplace_back(make_pair(i, j));
				else if (input == 1) {
					house.emplace_back(make_pair(i, j));
				}
			}	
		}
		num_of_chicken = chicken.size();
		//algorithm part
		Combination(0, 0);
		cout << answer;
		return 0;
	}
	
{% endraw %}
```

