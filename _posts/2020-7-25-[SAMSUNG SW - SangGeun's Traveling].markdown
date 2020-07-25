---
layout: post
title: [SAMSUNG SW - SangGeun's Traveling]
date: 2020-7-25
description: txt to markdown
thumbnail: food1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

﻿[247. SAMSUNG SW – SangGeun’s Traveling]
- I thought it was a DFS problem. But it was not.
- there was a trick that if we can use plains that we already used, we can travel all the city just by using N-1 plain.
- I spent 8 minutes and 40 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<map>

using namespace std;
int T, N, M;

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	cin >> T;

	for (int t = 0; t < T; t++) {
		
		//get input
		cin >> N >> M;
		for (int i = 0; i < M; i++) {
			int s, d;
			cin >> s >> d;
		}
		//algorithm part
		cout << N - 1<<endl;
	}
	return 0;
}

{% endraw %}
```

