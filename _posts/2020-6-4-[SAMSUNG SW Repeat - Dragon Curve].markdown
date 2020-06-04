---
layout: post
title: [SAMSUNG SW Repeat - Dragon Curve]
date: 2020-6-4
description: txt to markdown
thumbnail: breakfast-orange-lemon-oranges-large.jpg
categories: SAMSUNG_SW

# Information for the author block
author : Loui
---

﻿[16. SAMSUNG SW : Dragon Curve]
- it was a simulation problem using stack.
- For each round, I had to record previous direction in the stack.
- By increasing generation, from stack.back, rotating the direction and drawing a line in the table is the way to simulate.
- I spent 43 minutes and 12 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>

using namespace std;

int N;
vector<vector<int>> curve; //y x d g 
vector<vector<int>> table(101, vector<int>(101, 0));

int dir[4][2] = { {0,1},{-1,0},{0,-1},{1,0} };



int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	cin >> N;
	curve.assign(N, vector<int>(4, 0));
	for (int i = 0; i < N; i++) {
		cin >> curve[i][0] >> curve[i][1] >> curve[i][2] >> curve[i][3];
	}

	//algorithm part
	for (vector<int> cur_curve : curve) {
		int x = cur_curve[1]; int y = cur_curve[0]; int d = cur_curve[2]; int g = cur_curve[3];
		table[x][y] = 1;
		x = x + dir[d][0]; y = y + dir[d][1];
		table[x][y] = 1;
		if (g >= 1) {
			vector<int> stk;
			stk.emplace_back(d);
			for (int i = 1; i <= g; i++) {
				int _size = stk.size();
				for (int j = _size - 1; j >= 0; j--) {
					int gen = stk[j];
					gen = (gen + 1) % 4;
					x = x + dir[gen][0]; y += dir[gen][1];
					table[x][y] = 1;
					stk.emplace_back(gen);
				}
			}
		}
		
	}
	
	int answer = 0;
	for (int i = 1; i < 101; i++) {
		for (int j = 1; j < 101; j++) {
			if (table[i][j] == 1 && table[i][j - 1] == 1 && table[i - 1][j] == 1 && table[i - 1][j - 1] == 1) answer += 1;
		}
	}
	cout << answer;
	return 0;
	
	
}

{% endraw %}
```

