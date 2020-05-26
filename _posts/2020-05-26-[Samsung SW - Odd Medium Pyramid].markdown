---
layout: post
title: [Samsung SW - Odd Medium Pyramid]
data: 2020-05-26
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}
	﻿[166. [SAMSUNG - SW : Odd Medium Pyramid]
	- run time error occurred. I think there is a trick. it’s not a brute force.
	- see the first code.
	#include<stdio.h>
	#include<vector>
	#include<algorithm>
	using namespace std;
	
	
	int Mid(int a, int b, int c) {
		if ((a > b&& b > c)||(c>b && b>a)) return b;
		else if ((b > a&& a > c)||(c>a && a>b)) return a;
		else return c;
	}
	int main() {
		int T;
		scanf_s("%d", &T);
		int N, X;
		for (int test_case = 1; test_case <= T; test_case++) {
			scanf_s("%d %d", &N,&X);
			bool flag = false;
			vector<int> base(2 * N - 1);
			for (int i = 0; i < base.size(); i++) base[i] = i + 1;
			
			vector<vector<int>> pyramid(N, vector<int>(2 * N - 1, 0));
			do {
				int _size = base.size();
				for (int i = 0; i < base.size(); i++) pyramid[0][i] = base[i];
				for (int level = 1; level < N; level++) {
					for (int i = 2; i < _size; i++) {
						int mid = Mid(pyramid[level-1][i - 2], pyramid[level - 1][i - 1], pyramid[level - 1][i]);
						pyramid[level][i - 2] = mid;
					}
					_size -= 2;
				}
				if (pyramid[N - 1][0] == X) flag = true;
			} while (next_permutation(base.begin(), base.end())&& !flag);
			if (flag) printf("#%d 1\n", test_case);
			else printf("#%d 0\n", test_case);
		}
		return 0;
	}
	
	- so then, what would a trick be?
	- I found the trick! I searched results of when N is 2~5, and I found 1 and 2n-1 value didn’t appear.
	- see the below code.
	#include<stdio.h>
	
	int main() {
		int T;
		scanf_s("%d", &T);
		int N, X;
		for (int test_case = 1; test_case <= T; test_case++) {
			scanf_s("%d %d", &N,&X);
			if (X != 1 && X != (2 * N - 1)) printf("#%d 1\n", test_case);
			else printf("#%d 0\n", test_case);
		}
		return 0;
	}
	
{% endraw %}
