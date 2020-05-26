---
layout: post
title: [KAKAO 2019 - Fail Rate]
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

	﻿[127. [Programmers– KAKAO 2019 :Fail Rate]]
	- This problem’s point was to find order of index using fail rate.
	- I used map, since map dose sort automatically.
	- see the code.
	#include <string>
	#include <vector>
	#include<algorithm>
	#include <iostream>
	#include<map>
	
	using namespace std;
	
	vector<int> makeOrder(vector<double>& failure,vector<int> answer) {
		map<double, vector<int>> res;
		for (int i = 1; i < failure.size(); i++) {
			res[failure[i]].push_back(i);
		}
		for (map<double, vector<int>>::reverse_iterator iter = res.rbegin(); iter != res.rend(); iter++) {
			for (int i = 0; i < iter->second.size(); i++) {
				answer.push_back(iter->second[i]);
			}
		}
		return answer;
	}
	
	vector<int> solution(int N, vector<int> stages) {
		
		sort(stages.begin(), stages.end());
		vector<double> failure(N+1); //index starts from 1 not 0.
		double cur_pass = 0;
		int i;
		for (i = stages.size() - 1; i >= 0; i--) {
			if (stages[i] == N + 1) cur_pass++;
			else break;
		}
		double cur_stage = 0;
		for (i; i >= 0;) {
			if (stages[i] == N) {
				cur_stage++;
				if (i == 0) {
					cur_pass += cur_stage;
					failure[N] = cur_stage / cur_pass;
					break;
				}
				i--;
			}
			else {
				cur_pass += cur_stage;
				failure[N] = cur_stage / cur_pass;
				N--;
				cur_stage = 0;
			}
		}
	
	
		vector<int> answer= makeOrder(failure, vector<int>{});
		
		return answer;
	}
	
	int main() {
		solution(5, { 2, 1, 2, 6, 2, 4, 3, 3 });
		return 0;
	}
	
