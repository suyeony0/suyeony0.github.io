---
layout: post
title: KMP-Algorithm
date: 2020-6-24
description: txt to markdown
thumbnail: city2.jpg
categories: Algorithm

# Information for the author block
author : Loui
---


```cpp

{% raw %}

#include<iostream>
#include<vector>

using namespace std;

vector<int> failure;

string base = "DEWDQSDABDEFDDBBCCDABCDEASD";
string target = "ABCF";

void FindingFailure() {
	failure.assign(target.size(), 0);
	int j = 0;
	for (int i = 1; i < target.size(); i++) {
		while (j > 0 && target[i] != target[j]) j = failure[j - 1];
		if (target[i] == target[j]) failure[i] = ++j;
	}
}

bool KMP() {
	int j = 0;
	for (int i = 0; i < base.size(); i++) {
		while (j > 0 && base[i] != target[j]) j = failure[j - 1];
		if (base[i] == target[j]) {
			if (j == target.size() - 1) {
				return true;
			}
			else j++;
		}
	}
	return false;
}


int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	FindingFailure();
	cout << KMP();
	return 0;
	
	
}

{% endraw %}
```

