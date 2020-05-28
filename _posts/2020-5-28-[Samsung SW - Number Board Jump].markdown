---
layout: post
title: [Samsung SW - Number Board Jump]
date: 2020-5-28
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}

	﻿[204. [SAMSUNG SW – Number Board Jump]
	- it was just a DFS problem. there was no restriction so easy.
	- see the code.
	#include<iostream>
	#include<vector>
	#include<set>
	#include<string>
	using namespace std;
	
	vector<vector<int>> table(5,vector<int>(5,0));
	set<string> number_set;
	int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };
	
	void DFS(int x, int y, string cur_set,int cnt) {
		if (cnt == 6) {
			number_set.insert(cur_set);
			return;
		}
		for (int i = 0; i < 4; i++) {
			int nx = x + dir[i][0]; int ny = y + dir[i][1];
			if (nx >= 0 && ny >= 0 && nx < 5 && ny < 5) {
				cur_set += table[nx][ny] + '0';
				DFS(nx, ny, cur_set,cnt+1);
				cur_set.pop_back();
			}
		}
	
	}
	
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
	
		//get input
		for (int i = 0; i < 5; i++) {
			for (int j = 0; j < 5; j++) {
				cin >> table[i][j];
			}
		}
		//algorithm part
		for (int i = 0; i < 5; i++) {
			for (int j = 0; j < 5; j++) {
				string cur_set = to_string(table[i][j]) + '0';
				DFS(i, j, cur_set, 1);
				cur_set.pop_back();
			}
		}
	
		cout << number_set.size();
		return 0;
	
	}
	
{% endraw %}
