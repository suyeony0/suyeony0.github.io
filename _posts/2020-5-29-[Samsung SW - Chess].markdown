---
layout: post
title: [Samsung SW - Chess]
date: 2020-5-29
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% highlight c++ %}
```cpp
	﻿#include<iostream>
	#include<vector>
	
	using namespace std;
	
	int N, M,q,k,p;
	vector<vector<int>> table;
	vector<pair<int,int>> queens;
	vector<pair<int,int>> knights;
	int k_dir[8][2] = { {-1,-2},{-2,-1},{-2,1},{-1,2},{1,2},{2,1},{2,-1},{1,-2} };
	int q_dir[8][2] = { {-1,0}, {-1,1},{0,1},{1,1},{1,0},{1,-1},{0,-1},{-1,-1} };
	
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
	
		//get input
		int x, y;
		cin >> N >> M;
		table.assign(N, vector<int>(M, 0));
		cin >> q;
		for (int i = 0; i < q; i++) {
			cin >> x >> y;
			table[x-1][y-1] = 1;
			queens.emplace_back(make_pair(x-1, y-1));
		}
		cin >> k;
		for (int i = 0; i < k; i++) {
			cin >> x >> y;
			table[x-1][y-1] = 1;
			knights.emplace_back(make_pair(x-1, y-1));
		}
		cin >> p;
		for (int i = 0; i < p; i++) {
			cin >> x >> y;
			table[x-1][y-1] = 1;
		}
	
		//algorithm part
		//for queen
		for (int i = 0; i < q; i++) {
			for (int j = 0; j < 8; j++) {
				int move = 1;
				while (true) {
					x = queens[i].first + q_dir[j][0] * move; y = queens[i].second + q_dir[j][1] * move;
					if (x < 0 || y < 0 || x >= N || y >= M || table[x][y] == 1) break;
					table[x][y] = 2;
					move +=1;
				}
			}
		}
	
		//for knight
		for (int i = 0; i < k; i++) {
			for (int j = 0; j < 8; j++) {
				x = knights[i].first + k_dir[j][0]; y = knights[i].second + k_dir[j][1];
				if (x < 0 || y < 0 || x >= N || y >= M || table[x][y] == 1) continue;
				table[x][y] = 2;
			}
		}
		int answer = 0;
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < M; j++) {
				if (table[i][j] == 0) answer++;
			}
		}
		cout << answer;
		return 0;
	
	}
```
{% endhighlight %}
