---
layout: post
title: [Samsung SW - Ladder Rigging]
date: 2020-5-29
description: txt to markdown
thumbnail: work1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

{% highlight c++ %}

	﻿
	[115. [BACKJOON – SAMSUNG SW : Ladder Rigging]]
	- I spent 5 hour to reach the limit.
	- At first, I used DFS but time limit exceeded occurred.
	- So I changed my algorithm to BFS but it was same!!!
	- so I changed again and make all the thing small and use global variable to reduce the transfer time during calling functions.
	- Finally, I got correct mark. I refered to disccusion.
	#include<iostream>
	#include<fstream>
	#include<vector>
	#include<queue>
	#include<climits>
	using namespace std;
	int answer = INT_MAX;
	int table[31][11];
	int N; int M; int H;
	
	void makeTable() {
		ifstream in("C:\\Users\\gjsgu\\Desktop\\Algorithm\\test_case\\test_case_for_ladder_rigging.txt");
		if (in.is_open()) cout << "file is opened." << endl;
		
		in >> N; in >> M; in >> H;
	
		int a; int b;
		for (int i = 0; i < M; i++) {
			in >> a; in >> b;
			table[a ][b] = 2;// 2 is horizon line.
		}
	}
	
	void makeTable2() {
		cin >> N; cin >> M; cin >> H;
		int a; int b;
		for (int i = 0; i < M; i++) {
			cin >> a; cin >> b;
			table[a ][b] = 2;// 2 is horizon line.
		}
	}
	
	void printTable() {
		for (int i = 0; i < H;i++) {
			for (int j = 0; j < N; j++)
				cout << table[i][j] << " ";
			cout << endl;
		}
	}
	
	inline bool isSameEnd() {
		for (int j = 1; j <=N; j++) {
			int pos = j;
			for (int i = 1; i <= H; i++) {
				if (table[i][pos - 1] == 2) pos -= 1;
				else if (table[i][pos] == 2) pos += 1;
			}
			if (j != pos) return false;
		}
		return true;
	}
	
	void DFS(int count, int start) {
		if(count >= 4) return;
	
		if (isSameEnd()) {
			answer = min(answer, count);
			return;
		} 
	
		for (int i = 1; i <=H; i++) {
			for (int j = start; j < N; j++) {
				if (table[i][j] == 2) continue;
				if (table[i][j - 1] == 2) continue;
				if (table[i][j + 1] == 2) continue;
				table[i][j] = 2;
				DFS( count + 1, j);
				table[i][j] = 0;
			}
		}
	
	}
	
	int main() {
		makeTable2();
		if (isSameEnd()) {
			cout << 0;
			return 0;
		}
		DFS( 0, 1);
		answer== INT_MAX? cout<<-1:cout << answer;
		return 0;
	}
	
{% endhighlight %}

