---
layout: post
title: [Samsung SW - Diamond]
date: 2020-5-29
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

```cpp

{% raw %}

	﻿[158. [SAMSUNG - SW : Diamond]
	  I’ve misunderstood. but it wasn’t only me. so it’s SAMSUNG’s problem haha.
	- using set and map, I made an algorithm easily. there was no DFS, DP, etc, but just caculation.
	- see the code.
	#include<iostream>
	#include<unordered_map>
	#include<set>
	#define Min(a,b) a>b?b:a
	#define Max(a,b) a>b?a:b
	
	using namespace std;
	int N, K;
	unordered_map<int, int> diamond;
	set<int> diamond_size;
	int maximum = 0;
	// K=3
	// 1 2 3 5 5 5 5 8 9 9 9 10 15
	void helper(set<int>::iterator start) {
		int cur_size = *start;
		maximum = Max(maximum, diamond[cur_size]);
		int res = diamond[cur_size];
		for (set<int>::iterator size_iter = next(start,1); size_iter != diamond_size.end(); size_iter++) {
			int carry = 987654321;
			int key_size = *size_iter;
			if (cur_size + K <key_size) break;
			res += diamond[key_size];
		}
		maximum = Max(maximum, res);
	}
	
	int main(int argc, char** argv){
		int test_case;
		int T;
		
		cin >> T;
		int input;
		
		for (test_case = 1; test_case <= T; ++test_case){
			//get input
			cin >> N >> K;
			diamond.clear();
			diamond_size.clear();
			maximum = 0;
			for (int i = 0; i < N; i++) {
				cin >> input; diamond[input]++;
				diamond_size.insert(input);
			}
			//print out
			for (set<int>::iterator size_iter = diamond_size.begin(); size_iter != diamond_size.end(); size_iter++) {
				//cout << *size_iter << " ";
				helper(size_iter);
			
			}
			cout << "#" << test_case << " ";
			cout << maximum << endl;
		}
		return 0;
	}
	
{% endraw %}
```

