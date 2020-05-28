---
layout: post
title: [KAKAO 2019 Winter Internship - Claw Crane Game]
date: 2020-5-29
description: txt to markdown
thumbnail: building1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}

	﻿[175. [KAKAO 2019 – Winter Internship : Claw Crane Game]
	- this was so easy. I think I don’t need comment for this problem.
	- see the code.
	#include <string>
	#include <vector>
	#include<iostream>
	
	using namespace std;
	
	int solution(vector<vector<int>> board, vector<int> moves) {
		int answer = 0;
		//find top
		vector<int> tops(board[0].size(), 0);
		for (int j = 0; j < board[0].size(); j++) {
			for (int i = 0; i < board.size(); i++) {
				if (board[i][j] != 0) {
					tops[j] = i;
					break;
				}
			}
		}
	
		vector<int> stk;
		for (int index : moves) {
			if (tops[index - 1] >= board.size()) continue;
			int cur_char = board[tops[index - 1]][index - 1];
			tops[index - 1]++;
			if (!stk.empty() && stk.back() == cur_char) {
				answer += 2;
				stk.pop_back();
			}
			else {
				stk.push_back(cur_char);
			}
			//[1,5,3,5,1,2,1,4]
		}
	
		return answer;
	}
	
	int main() {
	
		return 0;
		
	}
	
	
{% endhighlight %}
