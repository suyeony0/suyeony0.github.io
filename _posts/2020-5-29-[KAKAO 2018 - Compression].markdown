---
layout: post
title: [KAKAO 2018 - Compression]
date: 2020-5-29
description: txt to markdown
thumbnail: city2.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

{% highlight c++ %}

{% raw %}

	﻿[153. [KAKAO – 2018 : Compression]] 
	- For two days from last problem, I had no time to solve algorithm until today.
	- And this problem was quite confusing. Making dictionary was the hardest thing.
	- I made a dictionary for each length of word. After that, from max_length to 1, compare input substring with the dictionary of the substring’s length. 
	- see the code.
	#include <string>
	#include <vector>
	#include <iostream>
	#include<algorithm>
	#include<map>
	#define max(a,b) a>b?a:b
	using namespace std;
	
	vector<int> solution(string msg) {
		vector<int> answer;
		map<int, vector<pair<string, int>>> dict;
		//dict initialized
		dict[1].assign(26, make_pair("", 0));
		for (int i = 0; i < 26; i++) dict[1][i] = make_pair('A' + i, i + 1);
	
		int max_length = 1;
		int start = 0;
		int cur_index = 27;
		bool flag = true;
		while (flag) {
			bool next = true;
			for (int len = max_length; len >= 1 && flag && next; len--) {
				string temp = msg.substr(start, len);
				for (int i = 0; i < dict[len].size(); i++) {
					if (temp == dict[len][i].first) {
						answer.push_back(dict[len][i].second);
						if (start + len < msg.size()) {
							start += len;
							dict[len + 1].push_back(make_pair(temp + msg.substr(start, 1), cur_index));
							max_length = max(max_length, len + 1);
							cur_index++;
							next = false;
							break;
						}
						else {
							flag = false;
							break;
						}
	
					}
				}
	
			}
	
		}
	
	
		return answer;
	}
	
	int main() {
		vector<int> answer;
		answer = solution("TOBEORNOTTOBEORTOBEORNOT");
		//answer = solution("KAKAO");
		for (int i : answer) cout << i << " ";
		return 0;
	}
	
{% endraw %}
{% endhighlight %}

