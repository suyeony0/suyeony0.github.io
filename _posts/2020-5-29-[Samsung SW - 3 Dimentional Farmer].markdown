---
layout: post
title: [Samsung SW - 3 Dimentional Farmer]
date: 2020-5-29
description: txt to markdown
thumbnail: food1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

{% highlight c++ %}

	﻿[164. [SAMSUNG - SW : 3 Dimentional Farmer]
	- I did brute force at first, but time was problem, so I made binary search tree, but same problem 
	occurred. I think I should’ve balanced binary search tree.
	- see the first code.
	#include<iostream>
	#include<vector>
	#include<unordered_map>
	#define min(a,b) a>b?b:a
	
	using namespace std;
	
	class Node {
	public:
		int value;
		Node* left = nullptr;
		Node* right = nullptr;
		Node(int val) :value(val) {}
	
		void insert(int val) {
			if (val <= value) {
				if (left) left->insert(val);
				else left = new Node(val);
			}
			else {
				if (right) right->insert(val);
				else right = new Node(val);
			}
		}
		int find(int val,int min_dis) {
			min_dis = min(min_dis, abs(val - value));
			if(val==value) return 0;
			else if (val < value) {
				if (left) return left->find(val, min_dis);
				else return min_dis;
			}
			else {
				if (right) return right->find(val, min_dis);
				else return min_dis;
			}
		}
	};
	
	int main(int argc, char** argv){
		ios_base::sync_with_stdio(false);
		cin.tie(NULL);
		cout.tie(NULL);
		int test_case;
		int T;
		cin >> T;
		int N, M,c1,c2;
		for (test_case = 1; test_case <= T; ++test_case){
			cin >> N >> M;
			cin >>c1 >> c2;
			int x_distance = abs(c1 - c2);
			int rt; cin >> rt;
			Node* root = new Node(rt);
			int input;
			for (int i = 1; i < N; i++) {
				cin >> input;
				root->insert(input);
			}	
			int res;
			int cnt = 0;
			int minimum = 987654321;
			for (int i = 0; i < M; i++) {
				cin >> input;
				res = root->find(input,987654321);
				if (x_distance + res < minimum) {
					cnt = 1;
					minimum = x_distance + res;
				}
				else if (x_distance + res == minimum) cnt++;
			}
			cout << "#" << test_case << " " << minimum << " " << cnt << endl;
			
			
		}
		return 0;
	}
	- instead of it, I sorted cows’ coordinates and took binary search to get nearest distance
	- but it corrected just 22 test case, but there are 5 more test case. I don’t know why it was wrong!
	- see the second code.
	#include<iostream>
	#include<vector>
	#include<algorithm>
	#include<climits>
	#include<unordered_map>
	#define min(a,b) a>b?b:a
	
	using namespace std;
	
	int N, M, c1, c2;
	int bin_search(const int val,vector<int>& cows){
		long long left = 0, right = (long long)N - 1, mid=(left + right) / 2;
		if (cows.front() > val) return abs(cows.front() - val);
		else if (cows.back() < val) return abs(val-cows.back());
	
		while (left <= right) {
			mid = (left + right) / 2;
			if (cows[mid] == val) return 0;
			else if (cows[mid] > val) right = mid - 1;
			else left = mid + 1;
			
		}
		if (cows[mid] < val) return min(abs(cows[mid] - val), abs(cows[mid + 1] - val));
		else return min(abs(cows[mid] - val), abs(cows[mid - 1] - val));
	
	}
	int main(int argc, char** argv){
		ios_base::sync_with_stdio(false);
		cin.tie(NULL);
		cout.tie(NULL);
		int test_case;
		int T;
		cin >> T;
		for (test_case = 1; test_case <= T; ++test_case){
			cin >> N >> M;
			cin >>c1 >> c2;
			unordered_map<long long, int> cnt;
			long long x_distance = abs(c1 - c2);
			vector<int> cows(N);
			for (int i = 0; i < N; i++) cin >> cows[i];
			sort(cows.begin(), cows.end());
			long long input;
			long long minimum = INT_MAX;
			long long res;
			for (int i = 0; i < M; i++) {
				cin >> input;
				res=bin_search(input,cows);
				int distance = x_distance + res;
				minimum = min(minimum, distance);
				cnt[distance]++;
			}
			cout << "#" << test_case << " " << minimum << " " << cnt[minimum] << endl;
			cnt.clear();
			cows.clear();
			
		}
		return 0;
	}
	- so I changed the return value of binary search to index from distance.
	- but 3 test case weren’t solved. fuck!
	- see the third code.
	#include<iostream>
	#include<vector>
	#include<algorithm>
	#include<climits>
	#include<unordered_map>
	#define min(a,b) a>b?b:a
	
	using namespace std;
	
	int N, M, c1, c2;
	int bin_search(const int val,vector<int>& cows){
		int left = 0, right = N - 1, mid=(left + right) / 2;
		if (cows.front() > val) return 0;
		else if (cows.back() < val) return N - 1;
	
		while (left <= right) {
			mid = (left + right) / 2;
			if (cows[mid] == val) return mid;
			else if (cows[mid] > val) right = mid - 1;
			else left = mid + 1;
			
		}
		if (cows[mid] < val) mid++;
		return mid;
	
	}
	int main(int argc, char** argv){
		ios_base::sync_with_stdio(false);
		cin.tie(NULL);
		cout.tie(NULL);
		int test_case;
		int T;
		cin >> T;
		for (test_case = 1; test_case <= T; ++test_case){
			cin >> N >> M;
			cin >>c1 >> c2;
			int x_distance = abs(c1 - c2);
			vector<int> cows(N);
			for (int i = 0; i < N; i++) cin >> cows[i];
			sort(cows.begin(), cows.end());
			int horse;
			int minimum = INT_MAX;
			int idx;
			int cnt = 0;
			for (int i = 0; i < M; i++) {
				cin >> horse;
				idx =bin_search(horse,cows);
				if (0 <= idx && idx < N) {
					int cow = cows[idx];
					int distance = abs(cow - horse);
					if (minimum > distance) {
						cnt = 1;
						minimum = distance;
					}
					else if (minimum == distance) cnt++;
				}
				if (0 <= idx && idx < N && cows[idx] != horse) {
					int cow = cows[idx - 1];
					int distance =abs(cow - horse);
					if (minimum > distance) {
						cnt = 1;
						minimum = distance;
					}
					else if (minimum == distance) cnt++;
				}
			}
			cout << "#" << test_case << " " << minimum+x_distance << " " << cnt << endl;
			
		}
		return 0;
	}
	- I gave up.. I refer to a discussion.
	- I think it is almost same and there is no different of time complexity. why it works but my one doesn’t?
	- the below code is from there.
	#include <iostream>
	#include <cstdio>
	#include <string>
	#include <vector>
	#include <algorithm>
	#include <cmath>
	#include <string.h>
	
	using namespace std;
	
	int TC = 1;
	int N, M, C1, C2, H;
	
	int C[500000];
	
	int bSearch(int s, int e) {
		if (s > e) return e;
		int m = (s + e) / 2;
		if (C[m] < H) return bSearch(m + 1, e);
		else if (C[m] == H) return m;
		else return bSearch(s, m - 1);
	}
	
	int main() {
		scanf("%d", &TC);
		for (int tc = 1; tc <= TC; tc++) {
			scanf("%d %d %d %d", &N, &M, &C1, &C2);
			int DX = C1 > C2 ? C1 - C2 : C2 - C1;
	
			for (int i = 0; i < N; i++)
				scanf("%d", &C[i]);
	
			sort(C, C + N);
			int idx = 0, d, mind = 0x7fffffff;
			int cnt = 0;
			for (int i = 0; i < M; i++) {
				scanf("%d", &H);
				idx = bSearch(0, N - 1);
				for (int j = idx; j >= 0; j--) {
					d = C[j] - H;
					if (d < 0) d = -d;
					if (d < mind) {
						mind = d;
						cnt = 1;
					}
					else if (d == mind)
						cnt++;
					else break;
				}
	
				for (int j = idx + 1; j < N; j++) {
					d = C[j] - H;
					if (d < 0) d = -d;
					if (d < mind) {
						mind = d;
						cnt = 1;
					}
					else if (d == mind)
						cnt++;
					else break;
				}
			}
	
			printf("#%d %d %d\n", tc, DX + mind, cnt);
		}
	
		return 0;
	}
	- temp record
	#include<iostream>
	#include<vector>
	#include<algorithm>
	#include<climits>
	#define min(a,b) a>b?b:a
	
	using namespace std;
	int input;
	int N, M, c1, c2;
	vector<int> cows;
	int bSearch(int s, int e) {
		if (s > e) return e;
		int m = (s + e) / 2;
		if (cows[m] < input) return bSearch(m + 1, e);
		else if (cows[m] == input) return m;
		else return bSearch(s, m - 1);
	}
	
	int main(int argc, char** argv) {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL);
		cout.tie(NULL);
		int test_case;
		int T;
		cin >> T;
		for (test_case = 1; test_case <= T; ++test_case) {
			cin >> N; cin>> M;
			cin >> c1; cin>> c2;
			int x_distance = abs(c1 - c2);
			cows.assign(N,0);
			for (int i = 0; i < N; i++) cin >> cows[i];
			sort(cows.begin(), cows.end());
			int idx = 0, d, mind = 0x7fffffff;
			int cnt = 0;
	
			for (int i = 0; i < M; i++) {
				cin >> input;
				idx = bSearch(0,N-1);
				for (int j = idx; j >= 0; j--) {
					d = cows[j] - input;
					if (d < 0) d = -d;
					if (d < mind) {
						mind = d;
						cnt = 1;
					}
					else if (d == mind)
						cnt++;
					else break;
				}
	
				for (int j = idx + 1; j < N; j++) {
					d = cows[j] - input;
					if (d < 0) d = -d;
					if (d < mind) {
						mind = d;
						cnt = 1;
					}
					else if (d == mind)
						cnt++;
					else break;
				}
	
			}
			cout << "#" << test_case << " " << mind+x_distance << " " << cnt << endl;
	
		}
		return 0;
	}
	
{% endhighlight %}

