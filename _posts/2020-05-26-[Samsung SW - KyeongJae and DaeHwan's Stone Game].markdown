---
layout: post
title: [Samsung SW - KyeongJae and DaeHwan's Stone Game]
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}
	﻿[168. [SAMSUNG - SW : KyeonJae and DaeHwan’s Stone Game]
	- we can’t use DFS for this problem due to time complexity.
	- so we must find a rule, the rule was if abs(r-b)<2 then, DH win, otherwise KyeongJae win.
	- I drew multiple example to find why the logic works well, but honeslty, I wasn’t able to undertand mathmatically.
	- see the code.
	#include<stdio.h>
	#include<cmath>
	using namespace std;
	
	int main() {
		int T; scanf_s("%d", &T);
	
		long long r, b;
		for (int tc = 1; tc <= T; tc++) {
			scanf_s("%lld %lld", &r, &b);
			if (abs(r-b) < 2) printf("#%d DH\n", tc);
			else printf("#%d KJ\n", tc);
		}
		return 0;
	}
	
{% endraw %}
