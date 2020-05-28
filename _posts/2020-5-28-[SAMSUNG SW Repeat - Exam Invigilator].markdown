---
layout: post
title: [SAMSUNG SW Repeat - Exam Invigilator]
date: 2020-5-28
description: txt to markdown
thumbnail: food1.jpg
categories: SAMSUNG_SW

# Information for the author block
author : Loui
---

```cpp
	[4. SAMSUNG SW : Exam Invigilator]
	- there was a trap that we have to consider data type. since there was no limit of sum of total invigilators.
	- so I set answer`s data type as long long
	- I spent 23 minutes.
	- see the code.
	#include<iostream>
	#include<vector>
	
	using namespace std;
	
	int N, B, C;
	vector<int> table;
	long long answer = 0;
	
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
	
	
		//get input
		cin >> N;
		table.assign(N, 0);
		for (int i = 0; i < N; i++) cin >> table[i];
		cin >> B >> C;
	
		// algorithm part
		answer += N;
		for (int i = 0; i < N; i++) {
			table[i] -= B;
			if (table[i] > 0) {
				long long sub;
				if (table[i] % C >= -0.0001 && table[i] % C<=0.0001) sub = table[i] / C;
				else sub = (long long)(table[i] / C)+1;
				answer += sub;
			}
		}
		cout << answer;
		return 0;
	}
	
```
