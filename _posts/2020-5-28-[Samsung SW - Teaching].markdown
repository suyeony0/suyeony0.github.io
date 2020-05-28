---
layout: post
title: [Samsung SW - Teaching]
data: 2020-05-26
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}

	﻿[186. [SAMSUNG SW – Teaching]
	- it was a selective permutation problem. all the word in antarctica start with “anta” and end with “tica”. so we teach students at least more than 5 letters. Therefore, if K<=4, return is 0.
	- Otherwise, after teaching ‘a’, ‘c’,’ ‘I’, ‘n’, ‘t’, we have to choose which letters we teach next. I used permutation for this section.
	- see the code.
	#include<iostream>
	#include<vector>
	#define max(a,b) a>b?a:b
	using namespace std;
	int N, K;
	vector<string> table;
	vector<int> rest_letter;
	vector<bool> letters(26, false);
	int answer = 0;
	int rest_size;
	bool isPossibleToRead(string s) {
		for (int i = 4; i < s.size() - 4; i++) if (letters[s[i] - 'a'] == false) return false;
		return true;
	}
	void Permutation(int learned_letter,int start) {
		if (learned_letter >= K) {
			int temp_res = 0;
			for (string s : table) if (isPossibleToRead(s)) temp_res++;
			answer = max(answer, temp_res);
			return;
		}
		for (int i = start; i < rest_size; i++) {
			letters[rest_letter[i]] = true;
			Permutation(learned_letter + 1, i + 1);
			letters[rest_letter[i]] = false;
		}
	}
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
		// get input
		cin >> N >> K;
		if (K <= 4) {
			cout << 0;
			return 0;
		}
		table.assign(N,"");
		for (int i = 0; i < N; i++) cin >> table[i];
		//algorithm part
		letters['a' - 'a'] = true; letters['n' - 'a'] = true; letters['t' - 'a'] = true; letters['c' - 'a'] = true; letters['i' - 'a'] = true;
		for (int i = 0; i < 26; i++) if (letters[i] == false) rest_letter.emplace_back(i);
		rest_size = rest_letter.size();
		Permutation(5,0);
		cout << answer;
		return 0;
	}
	
{% endraw %}
