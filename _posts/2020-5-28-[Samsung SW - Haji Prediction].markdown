---
layout: post
title: [Samsung SW - Haji Prediction]
date: 2020-5-28
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}

	﻿[162. [SAMSUNG - SW : Haji Prediction]
	- they gave an algorithm and I should dertermine whethere the algorithm would end or not.
	- so I recorded numbers appeared during algorithm and if recorded number appear again, break the while syntax and return false.
	- but a problem was data type, N could be given up to 10^14. so I used data type LONG LONG, but I needed unsigned long long actually.
	- see the code.
	#include<iostream>
	#include<unordered_map>
	#include<cmath>
	using namespace std;
	
	int main(int argc, char** argv){
		//what is haji in here by the way?
		ios_base::sync_with_stdio(0);
		std::cin.tie(NULL);
		std::cout.tie(NULL);
	
		int test_case;
		int T;
		
		cin >> T;
		unsigned long long N;
		for (test_case = 1; test_case <= T; ++test_case){
			cin >> N;
			bool flag=true;
			unordered_map<unsigned long long, bool> stop;
			while (N > 1) {
				if (stop.count(N)) {
					flag = false;
					break;
				}
				else stop[N] = true;
				if (N % 2 == 0) N = N / 2;
				else N = 3 * N + 3;
				cout << N << endl;
			}
			if (flag) cout << "#" << test_case << " YES" << endl;
			else cout << "#" << test_case << " NO" << endl;
		}
		return 0;
	}
	
{% endraw %}
