---
layout: post
title: [KAKAO 2019 Winter Internship - Stepping Stones]
date: 2020-5-28
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}

	﻿[179. [KAKAO 2019 – Winter Internship : Stepping Stones]
	- this problem also has efficiency test. my first try pass all the accuracy test, but not efficiency test.
	- see my first code.
	#include <string>
	#include <vector>
	#include<iostream>
	using namespace std;
	
	int solution(vector<int> input_stones, int max_interval) {
		int answer = 0;
		vector<pair<int, int>> stones; // pair<value,next_stone>
		stones.emplace_back(make_pair(200000001, 1)); //start position
		for (int i = 0; i < input_stones.size(); i++) stones.emplace_back(make_pair(input_stones[i], i + 2));
		//algorithm part
		while (true) {
			bool stop_flag = false;
			for (int i = 1; i < stones.size(); i++) {
				//when the stone's value is greater than 1
				if (stones[i].first != 0) {
					stones[i].first--;
					if (stones[i].first == 0) {
						int next = stones[i].second;
						for (int j = i - 1; j >= 0; j--) {
							if (stones[j].first != 0) {
								stones[j].second = next;
								break;
							}
							else stones[j].second = next;
						}
					}
				}
				//when the stone's value is 0
				else {
					if (stones[i - 1].second - (i-1) > max_interval) {
						stop_flag = true;
						break;
					}
					i = stones[i - 1].second - 1; // -1 is to make up for 'for' syntax's i++
	
				}
			}
			if (stop_flag) break;
			else answer++;
		}
	
		return answer;
	}
	
	int main() {
		cout << solution({2, 4, 5, 3, 2, 1, 4, 2, 5, 1},3);
		return 0;
	}
	- let’s figure out to pass the efficiency test.
	- I think we don’t need to travel all the stone, since for each person, all the stone’s value is subtracted by 1.
	- if we use binary search, we can solve this problem easily. mid is the value we check for each iteration whether the mid number of people can pass the stepping stones or not.
	- so if mid number of people can pass, take right half, or take left half. 
	- see the code.
	#include <string>
	#include <vector>
	#include<iostream>
	#define MAX_VALUE 200000000
	#define max(a,b) a>b?a:b
	using namespace std;
	int answer = 0;
	bool isPossibleToJump(vector<int>& stones,int mid,int max_interval) {
	
		int cnt = 0;
		for (int i = 0; i < stones.size(); i++) {
			if (stones[i] - (mid-1) <= 0) {
				cnt++;
				if (cnt >= max_interval) return false;
			}
			else cnt = 0;
		}
		return true;
	}
	
	void binarySearch(vector<int>& stones,int left, int right,int max_interval) {
		if (left > right) return;
		int mid = (right + left) / 2;
		bool flag = isPossibleToJump(stones, mid, max_interval);
		
		if (flag) {
			answer = max(answer, mid);
			binarySearch(stones, mid + 1, right, max_interval);
		}
		else {
			binarySearch(stones, left, mid - 1, max_interval);
		}
	
	}
	
	int solution(vector<int> stones, int max_interval) {
		binarySearch(stones, 0, MAX_VALUE, max_interval);
		return answer;
	}
	
	int main() {
		cout << solution({2, 4, 5, 3, 2, 1, 4, 2, 5, 1},3);
		return 0;
	}
	
{% endraw %}
