---
layout: post
title: [SAMSUNG SW - Virus]
date: 2020-6-11
description: txt to markdown
thumbnail: food2.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

﻿[213. SAMSUNG SW : Virus]
- It was a simulation problem.
- To record graph, I used unordered_map and unorderd_set.
- To travel connected nodes from current node, I used queue.
- I spent 8 minutes and 13 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<unordered_map>
#include<unordered_set>
#include<queue>
using namespace std;
unordered_map<int, unordered_set<int>> table;
unordered_map<int, bool> visit;
int N, K;

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	cin >> N >> K;
	int a, b;
	for (int i = 0; i < K; i++) {
		cin >> a >> b;
		table[a].insert(b);
		table[b].insert(a);
	}

	//algorihtm part
	visit[1] = true;
	queue<int> que;
	que.push(1);
	int answer = 0;
	while (!que.empty()) {
		int cur_com = que.front(); que.pop();
		for (unordered_set<int>::iterator iter = table[cur_com].begin(); iter != table[cur_com].end(); iter++) {
			if (visit[*iter] == false) {
				visit[*iter] = true;
				answer += 1;
				que.push(*iter);
			}
		}
	}
	cout << answer;
	return 0;

}

{% endraw %}
```

