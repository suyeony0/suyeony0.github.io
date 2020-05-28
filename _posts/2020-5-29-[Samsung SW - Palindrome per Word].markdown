---
layout: post
title: [Samsung SW - Palindrome per Word]
date: 2020-5-29
description: txt to markdown
thumbnail: breakfast-orange-lemon-oranges-large.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

{% highlight c++ %}

{% raw %}

	﻿[165. [SAMSUNG - SW : Palindrome per Word]
	- I used DFS and memorization, but time limit exceeded occurred.
	- For each k, I count how many valid palindrome per word string appear.
	- see the firse code.
	#include<iostream>
	#include<vector>
	using namespace std;
	
	
	string str;
	int s_size;
	vector<vector<int>> visit;
	int DFS(const int k,const int s,const int e,int count) {
		if (visit[k][s] != -1) {
			return visit[k][s];
		}
		int answer = 0;
		if (k <= 1) {
			visit[k][s] = 1;
			return 1;
		}
		else if (k == 2) {
			if (str.substr(s, (e - s) / 2 + 1) == str.substr(e - (e - s) / 2 + 1, (e - s) / 2)) {
				visit[k][s] = 1;
				return 1;
			} 
			return 0;
		}
		for (int i = 1; (s_size - count) - k + 2 - (2 * i) >= 0; i++) {
			if (str.substr(s, i) == str.substr(e - i+1, i)) {
				answer+=DFS(k-2, s + i,e-i,count+(2*i));
				
			}
			else continue;
		}
		visit[k][s] = answer;
		return answer;
	}
	
	int splitString() {
		int k = 1;
		int answer = 0;
		bool odd=false; if (s_size % 2) odd = true;
		while (k <= s_size) {
			if (k % 2 == 0 && odd) {
				k++;
				continue;
			}
			answer+=DFS(k,0,s_size-1,0);
			k++;
		}
		return answer;
	
	}
	
	int main(int argc, char** argv){
		ios_base::sync_with_stdio(false);
		cin.tie(NULL);
		cout.tie(NULL);
		int test_case;
		int T;
		
		cin >> T;
		
		for (test_case = 1; test_case <= T; ++test_case){
			cin >> str;
			s_size = str.size();
			visit.assign(s_size+1, vector<int>(s_size/2+1, -1));
			cout << "#" << test_case << " " << splitString() << endl;
	
		}
		return 0;
	}
	- I refered to discussions to revise my algorithm.
	- Honestly, I didn’t understand the below code well.
	#include <iostream>
	#include <string.h>
	#include <algorithm>
	#include <vector>
	using namespace std;
	#define SMAX 10001
	#define MOD 1000000007
	int TC;
	
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL);
		cout.tie(NULL);
	
	
		cin >> TC;
		for (int tt = 0; tt < TC; tt++) {
			char input[SMAX];
			cin >> input;
			int cnt = 0;
			while (input[cnt])
			{
				cnt++;
			}
			int count[SMAX] = { 1, };
	
			for (int i = 0; i < cnt / 2; i++) {
				// case 0 one character is center
				int ls = i;
				int le = i;
	
				int rs = cnt - le - 1;
				int re = cnt - ls - 1;
	
				while (ls >= 0 && le <= (cnt - 1) / 2 && input[ls] == input[rs] && input[le] == input[re]) {
					count[le + 1] = (count[le + 1] + count[ls]) % MOD;
					ls--;
					le++;
					rs--;
					re++;
				}
	
				// case 1 two characters are center
				ls = i;
				le = i + 1;
	
				rs = cnt - le - 1;
				re = cnt - ls - 1;
	
				while (ls >= 0 && le <= (cnt - 1) / 2 && input[ls] == input[rs] && input[le] == input[re]) {
					count[le + 1] = (count[le + 1] + count[ls]) % MOD;
					ls--;
					le++;
					rs--;
					re++;
				}
	
			}
			int all = 0;
			for (int i = 0; i < cnt / 2 + 1; i++) {
				all = (all + count[i]) % MOD;
			}
			cout << "#" << tt + 1 << " " << all << endl;
		}
	
		return 0;
	}
	
{% endraw %}
{% endhighlight %}

