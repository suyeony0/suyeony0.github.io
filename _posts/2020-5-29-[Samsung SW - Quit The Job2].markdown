---
layout: post
title: [Samsung SW - Quit The Job2]
date: 2020-5-29
description: txt to markdown
thumbnail: work1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

{% highlight c++ %}
	﻿[183. [SAMSUNG SW – Quit The Job 2]
	- it has been a while since I’ve met DP problem.
	- it was not that ambiguous and complex, but one condition has held my back
	- I started with end like backpropagation, if (i+ table[i].first)> N+1, that is if he can’t finish the counsel, the most efficient way to get paid is to take money[i]=money[i+1].
	- otherwise, max(today pay + next possible counsel pay,money[i+1]) is optimal. since money[i+1] is made as optimal from end of day( the quit day).
	- see the code.
	#include<iostream>
	#include<vector>
	#define max(a,b) a>b? a:b
	using namespace std;
	int N;
	vector<pair<int, int>> table;
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
	
		//get input
		cin >> N;
		table.assign(N+1,pair<int,int>());
		int duration; int pay;
		for (int i = 1; i <= N; i++) {
			cin >> duration >> pay;
			table[i] = make_pair(duration, pay);
		}
	
		//algorithm part
		vector<long long> money(N+2,0);
		int max_money = 0;
		for (int i = N; i >= 1; i--) {
			if (table[i].first + i > N + 1)	money[i] = money[i + 1];
			
			else {
				if (table[i].first + i<= N) money[i] = max(table[i].second + money[table[i].first + i], money[i + 1]);
				else if (i + 1 <= N) money[i] = max(table[i].second, money[i + 1]);
				else money[i] = table[i].second;
			}
		}
		cout << money[1] << endl;
		return 0;
	}
	
{% endhighlight %}
