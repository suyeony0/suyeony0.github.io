---
layout: post
title: [KAKAO 2019 Winter Internship - Banned User]
date: 2020-5-29
description: txt to markdown
thumbnail: city2.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

```cpp

{% raw %}

	﻿[177. [KAKAO 2019 – Winter Internship : Banned User]
	- doing permutation was the key point.
	- thanks to time limit was not that restric. I’ve solved easily using DFS – permutation.
	- see the code.
	#include <string>
	#include <vector>
	#include <set>
	#include<iostream>
	using namespace std;
	int answer = 0;
	vector<vector<string>> possible;
	vector<vector<string>> temp_answer;
	set<set<string>> res_answer;
	int ban_size;
	void DFS(vector<string> current_set, int index) {
		if (index >= ban_size) {
			set<string> res;
			for (string tt : current_set) {
				res.insert(tt);
			}
			if (res.size() == ban_size) res_answer.insert(res);
			return;
		}
		for (int i = 0; i < possible[index].size(); i++) {
			current_set.emplace_back(possible[index][i]);
			DFS(current_set, index + 1);
			current_set.pop_back();
		}
	
	}
	
	int solution(vector<string> user_id, vector<string> banned_id) {
		possible.assign(banned_id.size(), vector<string>{});
		for (int j = 0; j < banned_id.size(); j++) {
			string ban = banned_id[j];
			for (string user : user_id) {
				if (ban.size() != user.size()) continue;
				bool flag = true;
				for (int i = 0; i < ban.size(); i++) {
					if (ban[i] == '*' || ban[i] == user[i]) continue;
					if (ban[i] != user[i]) {
						flag = false;
						break;
					}
				}
				if (flag) possible[j].emplace_back(user);
			}
		}
		ban_size = possible.size();
		DFS(vector<string>{}, 0);
		for (set<string> ress : res_answer) {
			if (ress.size() != ban_size) continue;
			answer++;
		}
	
		return answer;
	}
	
{% endraw %}
```

