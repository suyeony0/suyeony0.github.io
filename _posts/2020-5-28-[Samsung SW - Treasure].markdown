---
layout: post
title: [Samsung SW - Treasure]
date: 2020-5-28
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}

	﻿[185. [SAMSUNG SW – Treasure]
	- this problem had a trick that if we use next_permutation, time limit exceeded occur.
	- so we have to find an algorithm but the algorithm was not that hard.
	- we should just mulitply a’s minimum value with b’s maximum value for each round.
	- see the code.
	#include<iostream>
	#include<vector>
	#include<algorithm>
	
	using namespace std;
	
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
	
		//get input
		int N; cin >> N;
		vector<int> table_a(N);
		vector<int> table_b(N);
		for (int i = 0; i < N; i++) cin >> table_a[i];
		for (int i = 0; i < N; i++) cin >> table_b[i];
		sort(table_a.begin(), table_a.end());
		sort(table_b.begin(), table_b.end(), [](int a, int b) { return a > b; });
		//algorithm part
		int i = 0;
		int answer = 0;
		while (i<N) {
			answer += table_a[i] * table_b[i];
			i++;
		}
		cout << answer;
		return 0;
	}
	
	
{% endraw %}
