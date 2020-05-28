---
layout: post
title: [Samsung SW - Gerrymandering 1]
date: 2020-5-29
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

```cpp
	﻿[182. [SAMSUNG SW – Gerrymandering 1]
	- Checking two districts are connected each other or not was the main point of this problem.
	- To split district, I used permutation – DFS, and to check connection, I used queue.
	- see the code.
	#include<iostream>
	#include<vector>
	#include<unordered_set>
	#include<algorithm>
	#include<climits>
	#include<queue>
	#define min(a,b) a>b? b:a
	using namespace std;
	
	int N;
	vector<vector<int>> table;
	vector<int> people;
	vector<bool> visit;
	int answer = INT_MAX;
	
	void calcul(vector<int>& dis_a, vector<int>& dis_b) {
		int sum_a = 0; int sum_b = 0;
		for (int i : dis_a) sum_a += people[i];
		for (int i : dis_b) sum_b += people[i];
		answer = min(answer, abs(sum_a -sum_b));
	}
	
	bool isValid(vector<int>& dis_a, vector<int>& dis_b) {
		if (dis_a.empty() || dis_b.empty())  return false;
		int size_a = dis_a.size(); int size_b = dis_b.size();
		queue<int> que;
		que.push(dis_a[0]);
		unordered_set<int> res_a; unordered_set<int> res_b;
		vector<bool> visit_a(N, false); vector<bool> visit_b(N, false);
		visit_a[que.front()] = true;
		res_a.insert(que.front());
		while (!que.empty()) {
			int cur_a = que.front(); que.pop();
			for (int i = 0; i < table[cur_a].size(); i++) {
				if (find(dis_a.begin(), dis_a.end(), table[cur_a][i]) != dis_a.end() && visit_a[table[cur_a][i]]==false) {
					visit_a[table[cur_a][i]] = true;
					que.push(table[cur_a][i]);
					res_a.insert(table[cur_a][i]);
				}
			}
		}
		if (res_a.size() != size_a) return false;
		que.push(dis_b[0]);
		visit_b[que.front()] = true;
		res_b.insert(que.front());
		while (!que.empty()) {
			int cur_b = que.front(); que.pop();
			for (int i = 0; i < table[cur_b].size(); i++) {
				if (find(dis_b.begin(), dis_b.end(), table[cur_b][i]) != dis_b.end() && visit_b[table[cur_b][i]] == false) {
					visit_b[table[cur_b][i]] = true;
					que.push(table[cur_b][i]);
					res_b.insert(table[cur_b][i]);
				}
			}
		}
		if (res_b.size() != size_b) return false;
		return true;
	}
	void DFS(vector<int> dis_a,int start) {
		if (start == N-1) return;
		
		for (int i = start; i < N; i++) {
			if (visit[i] == false) {
				vector<int> dis_b;
				visit[i] = true;
				dis_a.emplace_back(i);
				for (int j = 0; j < N; j++) {
					if (find(dis_a.begin(), dis_a.end(), j) == dis_a.end()) {
						dis_b.emplace_back(j);
					}
				}
				if (isValid(dis_a, dis_b)) calcul(dis_a, dis_b);
				DFS(dis_a, start + 1);
				dis_a.pop_back();
				visit[i] = false;
			}
		}
	}
	
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
		//get input
		cin >> N;
		table.assign(N, vector<int>());
		people.assign(N, 0);
		visit.assign(N, false);
		for (int i = 0; i < N; i++) cin >> people[i];
		int edge;
		for (int i = 0; i < N; i++) {
			cin >> edge;
			table[i].assign(edge, 0);
			for (int j = 0; j < edge; j++) {
				int temp_input;
				cin >> temp_input;
				table[i][j] = temp_input - 1;;
			}
		}
		//algorithm part
		DFS(vector<int>{}, 0);
		if (answer == INT_MAX) cout << -1;
		else cout << answer;
		return 0;
	
	}
	
	
```
