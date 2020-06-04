---
layout: post
title: [SAMSUNG SW Repeat - Tree Jaetech]
date: 2020-6-4
description: txt to markdown
thumbnail: building1.jpg
categories: SAMSUNG_SW

# Information for the author block
author : Loui
---

﻿[20. SAMSUNG SW : Tree Jaetech]
- it was a simulation problem. there were 4 given rules to simulate : Sping, Summer, Autumn, Winter.
- the time limit was 0.3 seconds. So I thought that it would be hard to reach the time limit. But it was not that matter.
- I used sort() in algorithm header to sort trees with respect to age in a shell.
- In Spring and Summer, if I find a tree that can not eat enough energy, From the tree to end of the list in a shell, I record the trees’ age and remove the trees.
- Autumn was not a big deal, I just had to check index range, and add a tree around a shell.
- I spent 33 minutes.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<algorithm>
using namespace std;

int N, M, K;
vector<vector<int>> energy;
vector<vector<int>> table;
vector<vector<vector<int>>> trees;
int dir[8][2] = { {-1,-1},{-1,0},{-1,1},{0,1},{1,1},{1,0},{1,-1},{0,-1} }; //starts at north west, goes clock-wisely.


void printTable() {
	cout << endl;
	for (vector<vector<int>> row : trees) {
		for (vector<int> i : row) cout << i.size() << " ";
		cout << endl;
	}
	cout << endl;
}

void SpringAndSummer() {
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < N; j++) {
			if (trees[i][j].size() >= 1) {
				int _size = trees[i][j].size();
				int t;
				for (t = 0; t < _size; t++) {
					if (table[i][j] - trees[i][j][t] < 0) break;
					else {
						table[i][j] -= trees[i][j][t];
						trees[i][j][t] += 1;
					}
				}
				for (int e=_size-1; t<=e; e--) {
					table[i][j] += trees[i][j][e] / 2;
					trees[i][j].pop_back();
				} 	
			}
		}
	}
}


void Autumn() {
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < N; j++) {
			if (trees[i][j].size() >= 1) {
				int _size = trees[i][j].size();
				for (int t = 0; t < _size; t++) {
					if (trees[i][j][t] % 5 == 0) {
						for (int d = 0; d < 8; d++) {
							int nx = i + dir[d][0]; int ny = j + dir[d][1];
							if (nx >= 0 && ny >= 0 && nx < N && ny < N) {
								trees[nx][ny].emplace_back(1);
							}
						}
					}
				}
			}
		}
	}

	
}


int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);
	
	//get input
	cin >> N >> M >> K;
	table.assign(N, vector<int>(N, 5));
	energy.assign(N, vector<int>(N, 0));
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < N; j++) {
			cin >> energy[i][j];
		}
	}
	trees.assign(N, vector<vector<int>>(N, vector<int>{}));
	int x, y, z;
	for (int i = 0; i < M; i++) {
		cin >> x >> y >> z;
		trees[x - 1][y - 1].emplace_back(z);
	}
	//algorithm part
	for (int year = 1; year <= K; year++) {
		SpringAndSummer(); Autumn(); 
		if (year != K) {
			for (int i = 0; i < N; i++) {
				for (int j = 0; j < N; j++) {
					sort(trees[i][j].begin(), trees[i][j].end());//sort
					table[i][j] += energy[i][j]; //winter
				}
			}
		} 
	}
	
	int answer = 0;
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < N; j++) {
			answer += trees[i][j].size();
		}
	}
	cout << answer;
	return 0;
	
}

{% endraw %}
```

