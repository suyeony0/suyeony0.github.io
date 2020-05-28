---
layout: post
title: [BaekJoon - 1697  Hide and Seek]
data: 2020-05-26
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}

	﻿[135. [BaekJoon– 1697 : Hide and Seek]]
	- it was just BFS problem, we just sholud be careful of memory using visit hash.
	- see the code.
	#include<iostream>
	#include<queue>
	#include<unordered_map>
	using namespace std;
	
	int BFS(int n, int k) {
		queue<pair<int, int>> que;
		que.push(make_pair(n, 0));
		//vector<bool> visit(100001,false);
		unordered_map<int, bool> visit;
		while (!que.empty()) {
			int cur_pos = que.front().first;
			int cur_sec = que.front().second;
			visit[cur_pos] = true;
			que.pop();
			if (cur_pos == k) return cur_sec;
			if (cur_pos + 1 <= 100000 && !visit[cur_pos+1]) que.push(make_pair(cur_pos + 1, cur_sec + 1));
			if (cur_pos - 1 >= 0 && !visit[cur_pos-1]) que.push(make_pair(cur_pos - 1, cur_sec + 1));
			if (cur_pos * 2 <= 100000 && !visit[cur_pos*2]) que.push(make_pair(cur_pos * 2, cur_sec + 1));
		}
		return -1;
	}
	
	int main() {
		int n; int k;
		cin >> n; cin >> k;
		cout<<BFS(n, k);
		return 0;
	
	}
	
	
{% endraw %}
