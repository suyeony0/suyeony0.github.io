---
layout: post
title: [SAMSUNG SW - Start Link]
date: 2020-7-9
description: txt to markdown
thumbnail: city2.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

﻿[236. SAMSUNG SW – Start Link]
- It was a BFS problem.
- Just using queue, pushing current floor + U or – D floor to the queue.
- If we meet the target floor, return the number of move.
- I spent 8 minutes and 22 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<queue>
#include<unordered_map>
#define FAIL -1
using namespace std;

int F, S, G, U, D;

int Queueing() {
	queue<vector<int>> que;
	que.push(vector<int>{S, 0}); // start pos , number of needed move.
	unordered_map<int, bool> visit;
	visit[S] = true;

	while (!que.empty()) {
		int cur = que.front()[0]; int cnt = que.front()[1]; que.pop();
		if (cur == G) return cnt;
		if (visit[cur + U] == false && cur+U<=F) {
			visit[cur + U] = true;
			que.push(vector<int>{cur + U, cnt + 1});
		} 
		if (visit[cur - D] == false && cur-D>=1) {
			visit[cur - D] = true;
			que.push(vector<int>{cur - D, cnt + 1});
		} 

	}
	return -1;
}

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	cin >> F >> S >> G >> U >> D;

	//algorithm part
	int answer=Queueing();
	if (answer == FAIL) cout << "use the stairs";
	else cout << answer;
	return 0;
}

{% endraw %}
```

