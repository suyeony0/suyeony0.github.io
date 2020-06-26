---
layout: post
title: [SAMSUNG SW - Ant]
date: 2020-6-24
description: txt to markdown
thumbnail: building1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

[225. SAMSUNG SW – Ant]
- It was an easy simulation problem.
- Just using double nested for syntax, we could solve it.
- First, Getting input of a first group of ants and Rerversing it.
- Second, Appending a second group of ants to the reversed first group.
- Third, from index=0 to N1+N2-1, if we meet different direction when we compare [i] vs [i+1], swap the two ants only if [i]’s direction is right.
- I spent 19 minutes and 38 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<algorithm>
using namespace std;

int N1, N2,T;
vector<pair<char, int>> ants;

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	cin >> N1 >> N2;
	ants.assign(N1,pair<char,int>(0,3)); // 3 is right 1 is left
	int i = 0;d
	for (i = 0; i < N1; i++) cin >> ants[i].first;
	reverse(ants.begin(), ants.end());
	ants.resize(N1+N2);
	int j = i;
	for (int i = 0; i < N2; i++,j++) {
		cin >> ants[j].first;
		ants[j].second = 1;
	}
	cin >> T;
	//algorithm part
	for (int time = 0; time < T; time++) {
		for (int i = 0; i < N1 + N2-1; i++) {
			if (ants[i].second != ants[i + 1].second && ants[i].second==3) {
				swap(ants[i], ants[i + 1]);
				i += 1;
			}
		}
	}
	for (pair<char, int> row : ants) cout << row.first;
	return 0;
}

{% endraw %}
```

