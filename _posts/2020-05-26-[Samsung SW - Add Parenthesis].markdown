---
layout: post
title: [Samsung SW - Add Parenthesis]
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}
	﻿[169. [SAMSUNG - SW : Add Parenthesis]
	- wow… I spent 4 hours and half…
	- I misunderstood the problem. I thought I had to consider all the possible pair of parenthesis without limitation of operator a parenthesis can have.
	- but each parenthesis can has only one operator.
	- From there, I started to revise my algorithm. but wow… I think since I don’t solve this kind of brute force or DFS problem nowdays, it took so much time.
	- see the code.
	#include<iostream>
	#include<string>
	#define max(a,b) a>b?a:b
	using namespace std;
	
	string s;
	int s_size;
	int N;
	int answer=-987654321;
	inline int calcul(const int a, const int b, const char c) {
		if (c == '+') return a + b;
		else if (c == '-') return a - b;
		else return a * b;
	}
	void DFS(const int idx,int sum) {
		if (idx >= N) {
			answer = max(answer, sum);
			return;
		} 
		//choose current operator
		int cur_choose = calcul(s[idx - 1]-'0', s[idx + 1] - '0', s[idx]);
		if (idx > 1) cur_choose = calcul(sum,cur_choose , s[idx - 2]);
		if (idx + 4 < N - 1) {
			DFS(idx + 4, cur_choose);
		}
		else if (idx + 2 < N - 1) {	
			DFS(idx + 4, calcul(cur_choose, s[idx + 3] - '0', s[idx + 2]));
		}
		else DFS(idx + 4, cur_choose);
	
		//otherwise
		int not_choose = 0;
		if(idx>1) not_choose = calcul(sum, s[idx - 1] - '0', s[idx - 2]);
		if (idx > 1 && idx+2<N-1) DFS(idx + 2, not_choose);
		else if (idx > 1) DFS(idx+2,calcul(not_choose, s[idx + 1] - '0', s[idx]));
		else if (idx <= 1 && N>3) DFS(idx + 2, s[0] - '0');
		
	}
	
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
		cin >> N;
		cin >> s;
		if (N == 1) cout << s[0] - '0';
		else {
			DFS(1, 0);
			cout << answer;
		} 
		return 0;
	}
	
	
	
{% endraw %}
