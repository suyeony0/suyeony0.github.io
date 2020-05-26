---
layout: post
title: [KAKAO 2019 Winter Internship - Tuple]
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

	﻿[176. [KAKAO 2019 – Winter Internship : Tuple]
	- just testing that I know the use of vector and find algorithm.
	- string parsing was the key point. 
	- see the code.
	#include <string>
	#include <vector>
	#include<unordered_set>
	#include <algorithm>
	using namespace std;
	
	vector<int> solution(string s) {
		vector<int> answer;
		vector<vector<int>> res(501);
		int max_size = 0;
		//solution("{{2},{2,1},{2,1,3},{2,1,3,4}}");
		for (int i = 2; i < s.size() - 1; i++) {
			if (s[i] == '{' || s[i] == ',') continue;
			string temp = "";
			int input;
			vector<int> temp_res;
			int j;
			for (j = i; j < s.size() - 1 ; j++) {
				if (s[j] == ',' || s[j]=='}') {
					input = stoi(temp);
					temp_res.emplace_back(input);
					temp = "";
					if (s[j] == '}') break;
				}
				else {
					temp += s[j];
				}
			}
			max_size = temp_res.size() > max_size ? temp_res.size() : max_size;
			res[temp_res.size()] = temp_res;
			i = j;
		}
		vector<int> make_tuple;
		make_tuple.emplace_back(res[1][0]);
		for (int i = 2; i <= max_size; i++) {
			for (int j = 0; j < res[i].size(); j++) {
				if (find(make_tuple.begin(), make_tuple.end(), res[i][j]) == make_tuple.end()) {
					make_tuple.emplace_back(res[i][j]);
					break;
				}
				else continue;
			}
		}
	
		return make_tuple;
	}
	
	int main() {
	
		return 0;
	}
	
	
