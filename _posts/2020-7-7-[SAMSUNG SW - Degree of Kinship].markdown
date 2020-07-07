---
layout: post
title: [SAMSUNG SW - Degree of Kinship]
date: 2020-7-7
description: txt to markdown
thumbnail: building1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

﻿[234. SAMSUNG SW – Degree of Kinship]
- It was a travelling problem composed of tree structure.
- I used unorderd_map to represent edges between nodes.
- First, Recording a given node’s parent.
- Second, for two node we need to find their degree of kinship, making vectors to record their parent.
- Third, Finding a closest same parent.
- I spent 19 minutes and 58 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<array>
#include<unordered_map>
using namespace std;

int N, S, D,M;
unordered_map<int, int> parent;

void PrintTable(vector<int>& left, vector<int>& right) {
	cout << endl;
	for (int i : left) cout << i << " ";
	cout << endl;
	for (int i : right) cout << i << " ";
	cout << endl;
}

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);
	
	//get input
	cin >> N>>S>>D>>M;
	int x, y;
	for (int i = 0; i < M; i++) {
		cin >> x >> y;
		parent[y] = x;
	}

	//algorithm part
	vector<int> left, right;
	left.emplace_back(S); right.emplace_back(D);
	while (parent[S] != 0) {
		left.emplace_back(parent[S]);
		S = parent[S];
	} 
	while (parent[D] != 0) {
		right.emplace_back(parent[D]);
		D = parent[D];
	} 
	int answer = -1;
	for (int i = 0; i < right.size(); i++) {
		for (int j = 0; j < left.size(); j++) {
			if (right[i] == left[j]) {
				answer = i + j;
				break;
			}
		}
		if (answer != -1) break;
	}
	cout << answer;
	return 0;

}

{% endraw %}
```

