---
layout: post
title: [KAKAO 2020 - Outer Wall Check]
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

	﻿[124. [Programmers– KAKAO 2020 : Outer Wall Check]]
	- I first used DFS to implement a brutr force, but time limit exceeded occurred.
	- see the DFS code.
	#include <string>
	#include <vector>
	#include<iostream>
	#include<climits>
	#define min(a,b) a>b ? b:a
	using namespace std;
	int minimum = INT_MAX;
	
	inline bool isCheckedAll(vector<int> table) {
		if (find(table.begin(), table.end(), 1) == table.end()) return true;
		return false;
	}
	
	vector<int> ChecKWall(vector<int> table,int dist, int start,bool left,int n) {
		if (left) {
			while (dist>=0) {
				table[start] = 0;
				start - 1 < 0 ? start = n - 1 : start--;
				dist--;
			}
		}
		else {
			while (dist>=0) {
				table[start] = 0;
				start = (start + 1) % n;
				dist--;
			}
		}
		return table;
	}
	
	void DFS(vector<int> table,vector<int>weak, vector<int> dist, int n,int count) {
		if (isCheckedAll(table)) { minimum = min(minimum, count); return; }
		else if (dist.empty()) return;
		for (int i = 0; i < weak.size(); i++) {
			int start = weak[i];
			vector<int> temp_weak = weak;
			temp_weak.erase(next(temp_weak.begin(), i));
			for (int j = 0; j < dist.size(); j++) {
				vector<int> temp_dist = dist;
				temp_dist.erase(next(temp_dist.begin(), j));
				DFS(ChecKWall(table, dist[j], start, true, n),temp_weak,temp_dist,n,count+1);
				DFS(ChecKWall(table, dist[j], start, false, n), temp_weak, temp_dist, n, count + 1);
			}
			
		}
		
	}
	
	int solution(int n, vector<int> weak, vector<int> dist) {
		vector<int> table(n,0);
		for (int i = 0; i < weak.size(); i++) table[weak[i]] = 1;
		DFS(table,weak,dist,n,0);
		int answer = minimum;
		return answer==INT_MAX? -1 : answer;
	}
	
	- So I have to change for efficiency.
	- It was not I had expected. It had a lot of complexity.
	- My algorithm is below.
	> 1. choose the number of people we use to check from 1 to dist.size() with decending order.
	> 2. with chosen people, do permutation and check if they can check all the outer wall. If we can, return the number of people as an answer.
	- see the code.
	#include <string>
	#include <vector>
	#include<iostream>
	#include<climits>
	#include<algorithm>
	#define min(a,b) a>b ? b:a
	using namespace std;
	
	inline bool isAllOnes(vector<int> check) {
		if (find(check.begin(), check.end(), 0) == check.end())  return true; 
		return false;
	}
	
	bool isCheckedAll(int people, vector<int>& dist,vector<int> weak,int n) {
		vector<int> chosen = { dist.rbegin(),next(dist.rbegin(),people) };
		do {
			for (int i = 0; i < weak.size(); i++) {
				//cout << "<<people :: " << people << endl;
				int start = i;
				//cout << " weak[start] : " << weak[start] << endl;
				vector<int> check(weak.size(), 0);
				check[start] = 1;
				for (int j = 0; j < chosen.size(); j++) { //start= 10 length = 14 -> 2
					//cout << " cur_start : " << start << endl;
					int length = chosen[j] + weak[start];
					if (length >= n) {
						length %= n;
						int k;
						for (k = start; k < check.size(); k++) check[k] = 1;
						for (k = 0; k < start; k++) {
							if (weak[k] <= length) check[k] = 1;
							else break;
						}
						if (isAllOnes(check)) return true;
						else start = k % weak.size();
					}
					else {
						int k;
						for (k = start; k < weak.size(); k++) {
							if (length >= weak[k]) check[k] = 1;
							else break;
						}
						if (isAllOnes(check)) return true;
						else start = k % weak.size();
					}
				}
			}
		} while (prev_permutation(chosen.begin(), chosen.end()));
		
		return false;
	}
	
	int solution(int n, vector<int> weak, vector<int> dist) {
		vector<int> table(n, 0);
		sort(dist.begin(), dist.end());
		int minimum = INT_MAX;
		for (int i = 0; i < weak.size(); i++) table[weak[i]] = 1;
		// when we need just one person.
		for (int i = 0; i < weak.size(); i++) {
			int length = dist.back() + weak[i];
			if (length >= n) {
				if (i == 0 || (weak[i - 1] <= length % n)) return 1;
			}
			else if (length >= weak.back() && i == 0) return 1;
		}
		// when  we need more than one person.
		for (int people = 2; people <= dist.size(); people++) {
			if (isCheckedAll(people, dist, weak, n)) return people;
		}
		return -1; //when we failed to check all the outer wall even if we used all the people.
	}
	
	int main() {
		//cout<<solution(12, { 1,5,6,10 }, { 1,2,3,4 })<<endl;
		//cout << solution(12, { 1,3,4,9,10 }, { 3,5,7 }) << endl;
		//cout << solution(50, { 1, 5, 10, 12, 22, 25 }, { 4, 3, 2, 1 }) << endl;
		cout << solution(50, { 1, 5, 10, 16, 22, 25 }, { 3,4,6 }) << endl;
		//cout << solution(50, { 1 }, { 6 }) << endl;
		//cout << solution(12, { 1,5 }, { 2,3,7 });
		return 0;
	}
	
