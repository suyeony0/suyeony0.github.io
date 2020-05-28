---
layout: post
title: [Samsung SW - Quit The Job]
date: 2020-5-28
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}

	﻿[107. [BACKJOON – SAMSUNG SW : Quit The Job]]
	- it was dp problem. I made dp from the last day.
	- dp[i] has the maximum money we can earn after ith day.
	- the point is that where dp[i], we don’t need to choose ith day if it couldn’t make maximum money.
	- dp has table.size()+1 memory, since I started table.size()-1 index and it’s possible we can’t consult at the last day.
	- see the code.
	#include<iostream>
	#include<fstream>
	#include<vector>
	#include<algorithm>
	using namespace std;
	
	vector<vector<int>> makeTable() {
		std::ifstream in("C:\\Users\\gjsgu\\Desktop\\Algorithm\\test_case\\test_case_for_quit_the_job.txt");
		int N;
		if (in.is_open()) {
			cout << "file is opened." << endl;
			in >> N;
		}
		vector<vector<int>> table(N, vector<int>(2, 0));
		for (int i = 0; i < N; i++) {
			in >> table[i][0]; in >> table[i][1];
		}
		return table;
	}
	vector<vector<int>> makeTable2() {
		int N;
		cin >> N;
		vector<vector<int>> table(N, vector<int>(2, 0));
		for (int i = 0; i < N; i++) {
			cin >> table[i][0]; cin >> table[i][1];
		}
		return table;
	}
	
	void printTable(vector<vector<int>> table) {
		for (vector<int> row : table) {
			for (int i : row) {
				cout << i << " ";
			}
			cout << endl;
		}
	}
	
	int findMaximum(vector<vector<int>>& table) {
		int last_day = table.size();
		int cur_max = 0;
		vector<int> dp(last_day+1, 0); // dp is the maximum money we can earn after ith day. whether choosing ith day or not doesn't matter.
		for (int i = last_day - 1; i >= 0; i--) {
			// if a consulting continues over the last day, just take dp[i+1]
			if (table[i][0] - 1 + i >= last_day) {
				dp[i] = dp[i + 1];
				continue;
			} 
			// if not, take maximum between current day's money + dp of next possible day and just dp[i+1]
			dp[i] = max(table[i][1] + dp[i + table[i][0]], dp[i+1]);
			//cout << "dp[" << i << "] : " << dp[i] << endl;
		}
		return dp[0];
	}
	
	int main() {
		//vector<vector<int>> table=makeTable();
		vector<vector<int>> table = makeTable2();
		cout << findMaximum(table);
		return 0;
	}
	
{% endraw %}
