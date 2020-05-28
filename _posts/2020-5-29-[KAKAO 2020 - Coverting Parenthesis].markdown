---
layout: post
title: [KAKAO 2020 - Coverting Parenthesis]
date: 2020-5-29
description: txt to markdown
thumbnail: food2.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

{% highlight c++ %}
```cpp
	﻿
	[120. [Programmers– KAKAO 2020 : Converting Parenthesis]]
	- this problem’s main point was to follow given rule to make valid parenthesis.
	- but the given rule was quite ambiguous. so referring to example in a detailed fashion was important.
	- be careful when you handle DFS.
	- see the code.
	#include <string>
	#include <vector>
	#include<iostream>
	#include<fstream>
	
	
	using namespace std;
	
	
	string Input() {
		ifstream in("C:\\Users\\gjsgu\\Desktop\\Algorithm\\test_case\\test_case_for_converting_parenthesis.txt");
		if (in.is_open()) cout << "file is opened." << endl;
		string p; in >> p;
		return p;
	}
	
	pair<string, string> splitUV(string p) {
		string u; string v;
		int left = 0; int right = 0;
		int i=0;
		for (i = 0; i < p.size(); i++) {
			u += p[i];
			if (p[i] == '(') left++;
			else if (p[i] == ')') right++;
			if (left == right) break;
		}
		for (int j = i + 1; j < p.size(); j++) v += p[j];
		return make_pair(u, v);
	}
	
	bool isValid(string u) {
		int valid = 0;
		for (char c : u) {
			if (c == '(') valid++;
			else if (c == ')') valid--;
			if (valid < 0) return false;
		}
		return true;
	}
	string reverse(string p) {
		for (int i = 0; i < p.size(); i++) 
			p[i] == '(' ? p[i] = ')' : p[i] = '(';
		return p;
	}
	
	string firstStep(string p) {
		string res;
		if (p.empty()) return "";
		pair<string, string> split = splitUV(p);
		string u = split.first; string v = split.second;
		if (isValid(u)) { res += u; res += firstStep(v);}
		else {
			res += "("+ firstStep(v)+")";
			u.erase(u.begin()); u.erase(next(u.end(),-1));
			u = reverse(u);
			res += u;
		}
		return res;
	}
	
	string solution(string p) {
		string answer = "";
		answer = firstStep(p);
		return answer;
	}
	
	int main() {
		string p= Input();
		cout << solution(p);
		return 0;
	}
	
	
	
	
	
	
```
{% endhighlight %}
