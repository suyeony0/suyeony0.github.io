---
layout: post
title: [SAMSUNG SW Repeat - Embed Operator]
date: 2020-5-30
description: txt to markdown
thumbnail: breakfast-orange-lemon-oranges-large.jpg
categories: SAMSUNG_SW

# Information for the author block
author : Loui
---

```cpp

{% raw %}

	[10. SAMSUNG SW : Embed Operator]
	- it was a permutation problem. I used DFS for permutation, but in this case, I could use next_permutation.
	- if I had used next_permutation, I would have been faster than now. since visit vector and DFS stack would have not been needed.
	- I spent 20 minutes.
	- see the code.
	#include<iostream>
	#include<vector>
	#define max(a,b) a>b? a:b
	#define min(a,b) a>b? b:a
	using namespace std;
	
	int N;
	vector<int> opers(4, 0);
	vector<int> number;
	
	vector<char> oper_list;
	vector<char> cur_oper;
	vector<bool> visit;
	int maximum = -1000000001;
	int minimum = 1000000001;
	
	void initOperList(int i, char c) {
		for (int j = 0; j < opers[i]; j++) 
			oper_list.emplace_back(c);
	}
	
	void Calculate() {
		int temp = number[0];
		for (int i = 1; i < N; i++) {
			if (cur_oper[i - 1] == '+') {
				temp+= number[i];
			}
			else if (cur_oper[i - 1] == '-') {
				temp -= number[i];
			}
			else if (cur_oper[i - 1] == '*') {
				temp *= number[i];
			}
			else {
				temp /= number[i];
			}
		}
		maximum = max(maximum, temp);
		minimum = min(minimum, temp);
	}
	
	void DFS(int cnt) {
		if (cnt == N - 1) {
			Calculate();
			return;
		}
	
		for (int i = 0; i < oper_list.size(); i++) {
			if (visit[i] == false) {
				visit[i] = true;
				cur_oper.emplace_back(oper_list[i]);
				DFS(cnt + 1);
				cur_oper.pop_back();
				visit[i] = false;
			}
		}
	}
	
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
	
		//get input
		cin >> N;
		number.assign(N, 0);
		visit.assign(N - 1, false);
		for (int i = 0; i < N; i++) cin >> number[i];
		for (int i = 0; i < 4; i++) cin >> opers[i];
	
		//algorithm part
		initOperList(0, '+'); initOperList(1, '-'); initOperList(2, '*'); initOperList(3, '/');
		DFS(0);
		cout << maximum << endl;
		cout << minimum << endl;
		return 0;
		
	
	}
	
{% endraw %}
```

