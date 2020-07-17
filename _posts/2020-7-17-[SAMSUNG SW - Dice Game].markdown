---
layout: post
title: [SAMSUNG SW - Dice Game]
date: 2020-7-17
description: txt to markdown
thumbnail: breakfast-orange-lemon-oranges-large.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

﻿[240. SAMSUNG SW – Dice Game]
- It was an easy simulation problem.
- they gave us a board and numbers from rolled dice.
- we just should simulate the game
- First, move as much as a number from rolled dice.
- Second, move again as much as a number on the board.
- Iterating first and second, when we arrive N(destination) or over N, return how many move we took.
- I spent 15 minutes and 13 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>

using namespace std;

int N, M;
vector<int> table;
vector<int> dice;

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	cin >> N >> M;
	table.assign(N, 0);
	dice.assign(M, 0);
	for (int i = 0; i < N; i++) cin >> table[i];
	for (int i = 0; i < M; i++) cin >> dice[i];

	//algorithm part
	int j = 0;
	int cur = 0;
	while (j < M) {
		if (cur+dice[j]>=N-1 || cur + dice[j] + table[cur + dice[j]] >= N-1) {
			cout << j+1;
			return 0;
		}
		cur += dice[j] + table[cur + dice[j]];
		j += 1;
	}
	return 0;
}

{% endraw %}
```

