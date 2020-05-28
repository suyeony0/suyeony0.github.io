---
layout: post
title: [Samsung SW - Chocolate and Raisin]
date: 2020-5-29
description: txt to markdown
thumbnail: work1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

{% highlight c++ %}
	﻿[157. [SAMSUNG - SW : Chocolate and Raisin]
	- it was D4 problem. I mean it was quite hard to solve.
	- time was the most difficult one to reach the given condition.
	- I used memorization named visit, DFS, and prefix_sum.
	- see the code.
	#include<iostream>
	#include<vector>
	#include<cstring>
	#define min(a,b) a>b? b:a
	using namespace std;
	
	vector<vector<int>> table;
	vector<vector<int>> prefix_sum;
	int n, m;
	int visit[51][51][51][51] = { 0, };
	void prefixSum() {
		prefix_sum[0][0] = table[0][0];
		for (int i = 1; i < n; i++) prefix_sum[i][0] = prefix_sum[i - 1][0] + table[i][0];
		for (int j = 1; j < m; j++) prefix_sum[0][j] = prefix_sum[0][j - 1] + table[0][j];
		for (int i = 1; i < n; i++) {
			for (int j = 1; j < m; j++) {
				prefix_sum[i][j] = prefix_sum[i][j - 1] + prefix_sum[i - 1][j] - prefix_sum[i - 1][j - 1] + table[i][j];
			}
		}
	}
	
	int helper(int tx,int ty,int bx,int by) {
		if (tx == bx && ty == by) return 0;
		else if (visit[tx][ty][bx][by] != -1) return visit[tx][ty][bx][by];
	
		int sum = 0;
		if (tx == 0 && ty == 0) sum = prefix_sum[bx][by];
		else if (tx == 0) sum = prefix_sum[bx][by] - prefix_sum[bx][ty - 1];
		else if (ty == 0) sum = prefix_sum[bx][by] - prefix_sum[tx - 1][by];
		else sum = prefix_sum[bx][by] - prefix_sum[tx - 1][by] - prefix_sum[bx][ty - 1] + prefix_sum[tx - 1][ty - 1];
		
		
		int res = 987654321;
		for (int i = tx ; i < bx; i++) {
			res=min(res,sum+helper(tx, ty, i, by)+ helper(i + 1, ty, bx, by));
		}
		for (int j = ty; j < by; j++) {
			res=min(res,sum+helper(tx, ty, bx, j) + helper(tx, j+1, bx, by));
		}
		visit[tx][ty][bx][by] = res;
		return res;
	}
	
	int main(int argc, char** argv){
		int test_case;
		int T;
		cin >> T;
		for (test_case = 1; test_case <= T; ++test_case) {
			cin >> n; cin >> m;
			memset(visit, -1, sizeof(visit));
			table.assign(n, vector<int>(m));
			prefix_sum.assign(n, vector<int>(m));
			for (int i = 0; i < n; i++) for (int j = 0; j < m; j++) cin >> table[i][j]; //make table
			prefixSum();
			//for (vector<int> row : prefix_sum) {
			//	for (int i : row) cout << i << " ";
			//	cout << endl;
			//}
			cout << "#" << test_case << " ";
			cout << helper(0, 0, n - 1, m - 1) << endl;
			
		}
		return 0;//정상종료시 반드시 0을 리턴해야합니다.
	}
	
	
{% endhighlight %}
