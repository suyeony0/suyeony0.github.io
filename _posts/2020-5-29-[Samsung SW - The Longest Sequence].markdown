---
layout: post
title: [Samsung SW - The Longest Sequence]
date: 2020-5-29
description: txt to markdown
thumbnail: food2.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

{% highlight c++ %}
```cpp
	﻿
	[160. [SAMSUNG - SW : The Longest Sequence]
	-At first, I used next_permutation for brute force. but time limit exceeded occurred.
	- see the first code.
	#include<iostream>
	#include<vector>
	#include<algorithm>
	#include<unordered_set>
	#define max(a,b) a>b ? a : b
	using namespace std;
	
	int N;
	// 1 3 5 2 4
	int getLongestSequenceLength(vector<int>& numbers) {
		int res = 0;
		int n_size = numbers.size();
		do {
			for (int i = n_size - 1; i >= 1 && i>res; i--) {
				if (numbers[i] > numbers[i - 1] && numbers[i] % numbers[i - 1] == 0) {
					int temp = 1;
					int j;
					for ( j = i; j >= 1; j--) {
						if (numbers[j] > numbers[j - 1] && numbers[j] % numbers[j - 1] == 0) {
							temp++;
						}
						else break;
					}
					res = max(res, temp);
					i = j+1;
				} 
			}
	
		} while (next_permutation(numbers.begin(), numbers.end()));
		
		return res;
	}
	
	int main(int argc, char** argv)
	{
		int test_case;
		int T;
		cin >> T;
		for (test_case = 1; test_case <= T; ++test_case){
			//get input
			cin >> N;
			vector<int> numbers(N);
			for (int i = 0; i < N; i++) {
				cin >> numbers[i];
			}
			sort(numbers.begin(), numbers.end());
			cout << "#" << test_case << " " << getLongestSequenceLength(numbers) << endl;
		}
		return 0;
	}
	
	- so I change my algorithm to DP.
	- Dp[i] has a number of factor i has in the given vector.
	- the point is that c style array and memset are fatser than STL array and memset. since when I used STL array and vector, time limit exceeded occurred.
	- see the code.
	#include<iostream>
	#include<vector>
	#include<algorithm>
	#include<cstring>
	#define max(a,b) a>b ? a : b
	using namespace std;
	int dp[1000001];
	int numbers[100001];
	int N;
	
	int main(int argc, char** argv)
	{
		
		int test_case;
		int T;
		cin >> T;
		for (test_case = 1; test_case <= T; ++test_case){
			//get input
			memset(dp, 0, sizeof(dp));
			memset(numbers, 0, sizeof(numbers));
			cin >> N;
			for (int i = 0; i < N; i++) {
				cin >> numbers[i];
				dp[numbers[i]] = 1;
			}
			sort(numbers,numbers+N);
			int res = 1;
	
			for (int i = 0; i < N; i++) {
				for (int j = numbers[i] * 2; j <= numbers[N-1]; j += numbers[i]) {
					if (dp[j] > 0) {
						dp[j] = max(dp[j], dp[numbers[i]] + 1);
	
					}
				}
	
			}
			for (int i = 0; i < N; i++)
				res = max(res, dp[numbers[i]]);
	
	
			cout << "#" << test_case << " " << res << endl;
		}
		return 0;
	}
	
	
```
{% endhighlight %}
