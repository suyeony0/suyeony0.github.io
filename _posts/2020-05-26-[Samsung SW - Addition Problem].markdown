---
layout: post
title: [Samsung SW - Addition Problem]
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

	﻿[167. [SAMSUNG - SW : Addition Problem]
	- I felt like level 4 problem’s in SAMSUNG SW expert don’t ask brute force. there is always a tricked rule.
	- this problem has trick as well. the key calculation was (b-a) * (n-2) +1.
	- and I had to be careful of data type.
	- see the code.
	#include<stdio.h>
	#include<vector>
	#include<algorithm>
	#include<unordered_set>
	using namespace std;
	
	int main() {
		int T; scanf_s("%d", &T);
	
		long long n, a, b;
		for (int tc = 1; tc <= T; tc++) {
			scanf_s("%lld %lld %lld", &n, &a, &b);
			if((n==1 && a!=b)||a>b) printf("#%d 0\n", tc);
			else if((n==1 && a==b)||n==2 ) printf("#%d 1\n", tc);
			else {
				printf("#%d %lld\n", tc, (b - a) * (n-2)+1);
			}
		}
		return 0;
	}
	
