---
layout: post
title: [Samsung SW - Sewoon will do tomorrow]
date: 2020-5-29
description: txt to markdown
thumbnail: food1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

{% highlight c++ %}
```cpp
	﻿[161. [SAMSUNG - SW : Sewoon will do tomorrow]
	- I used DP to check whether there is ovelapped day, but runtime error occurred. I couldn’t find the reason, so I changed my algorithm to easier way.
	- see the first code.
	#include<iostream>
	#include<vector>
	#include<cstring>
	#include<unordered_map>
	#include<climits>
	#define min(a,b) a>b?b:a
	using namespace std;
	
	int getLastDay(vector<pair<int, int>>& table) {
		unordered_map<int, bool> dp;
		int min_day = INT_MAX;
		int t,d;
		for (pair<int, int> row : table) {
			t = row.first; d = row.second;
			int start = (d - t) + 1;
			min_day = min(min_day, start);
			int rest_day = 0;
			for (int i = start; i <= d; i++) {	
				if (dp.count(i)) rest_day++;
				dp[i]=true;
			}
			int j = start;
			while (rest_day > 0) {
				if (!dp.count(j)) {
					dp[j] = true;
					rest_day--;
				}
				j--;
			}
			min_day = min(min_day, j+1);
		}
		return min_day - 1;
	}
	
	int main(int argc, char** argv){
		ios_base::sync_with_stdio(0);
		std::cin.tie(NULL);
		std::cout.tie(NULL);
		int test_case;
		int T,N;
		cin >> T;
		for (test_case = 1; test_case <= T; ++test_case){
			cin >> N;
			vector<pair<int, int>> table(N, make_pair(0, 0));
			int t,d;
			for (int i = 0; i < N; i++) {
				cin >> t >> d;
				table[i] = make_pair(t, d);
			}
			cout << "#" << test_case << " " << getLastDay(table) << endl;
		}
		return 0;//정상종료시 반드시 0을 리턴해야합니다.
	}
	
	- the revised algorithm is based on sorting alogirhtm. after sorting, if there is overlapped day, just moving current homework forward.
	- since we took sort, we don’t need to care a case that several days are overlapped.
	#include<iostream>
	#include<vector>
	#include<cstring>
	#include<climits>
	#include<algorithm>
	#define min(a,b) a>b?b:a
	using namespace std;
	
	int getLastDay(vector<pair<int, int>>& table) {
		int t,d;
		int start_day = table.back().second - table.back().first + 1;
		table.pop_back();
		while(!table.empty()) {
			int te = table.back().second; int ts = te- table.back().first+1;
			table.pop_back();
			if (te >= start_day) {
				start_day = ts - (te - start_day+1);
			}
			else start_day = ts;
		}
		return start_day - 1;
	}
	
	int main(int argc, char** argv){
		ios_base::sync_with_stdio(0);
		std::cin.tie(NULL);
		std::cout.tie(NULL);
		int test_case;
		int T,N;
		cin >> T;
		for (test_case = 1; test_case <= T; ++test_case){
			cin >> N;
			vector<pair<int, int>> table(N, make_pair(0, 0));
			int t,d;
			for (int i = 0; i < N; i++) {
				cin >> t >> d;
				table[i] = make_pair(t, d);
			}
			sort(table.begin(), table.end(), [](pair<int, int> a, pair<int, int> b) {return a.second < b.second; });
			cout << "#" << test_case << " " << getLastDay(table) << endl;
		}
		return 0;//정상종료시 반드시 0을 리턴해야합니다.
	}
	
```
{% endhighlight %}
