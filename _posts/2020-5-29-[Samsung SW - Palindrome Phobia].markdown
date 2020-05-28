---
layout: post
title: [Samsung SW - Palindrome Phobia]
date: 2020-5-29
description: txt to markdown
thumbnail: breakfast-orange-lemon-oranges-large.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

{% highlight c++ %}

	﻿#include<iostream>
	#include<algorithm>
	#include<climits>
	using namespace std;
	
	bool isPalindrome(string& s) {
		int i = 0, j = s.size() - 1;
		while (i < j) {
			if (s[i] != s[j]) return false;
			i++; j--;
		}
		return true;
	}
	
	bool hasPalindrome(string& s) {
		int cur_size = 2;
		int s_size = s.size();
		string temp;
		while (cur_size <= s_size) {
			for (int i = 0; i + cur_size <= s_size; i++) {
				temp = s.substr(i, cur_size);
				if (isPalindrome(temp)) return true;
			}
			cur_size++;
		}
		return false;
	}
	
	int main(int argc, char** argv){
		int test_case;
		int T;
		ios_base::sync_with_stdio(0);
		std::cin.tie(NULL);
		std::cout.tie(NULL);
	
		cin >> T;
		string s;
		for (test_case = 1; test_case <= T; ++test_case){
			cin >> s;
			int a=0, b=0, c=0;
			int minimum = INT_MAX, maximum = INT_MIN;
			for (char cha : s) {
				if (cha == 'a')  a++;
				else if (cha == 'b') b++;
				else c++;
			}
			minimum = min(a, min(b, c)); maximum = max(a, max(b, c));
			if (maximum - minimum > 1) cout << "#" << test_case << " NO" << endl;
			else cout << "#" << test_case << " YES" << endl;
	
		}
		return 0;
	}
	
{% endhighlight %}

