---
layout: post
title: [SAMSUNG SW - Seven Dwarfs]
date: 2020-6-6
description: txt to markdown
thumbnail: city2.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

﻿[207. SAMSUNG SW : Seven Dwarfs]
- it was a combination problem. I used DFS to implenmt combination.
- this problem was so easy, I just had to check whether sum of chosen dwarfs height is 100 or not after choosing 7 dwarfs.
- I spent 5 minutes.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<algorithm>

using namespace std;
vector<int> table(9, 0);
vector<bool> visit(9, false);
vector<int> chosen;
bool flag = false;

void Combination(int cnt, int start) {
	if (cnt == 7) {
		int sum = 0;
		for (int i : chosen) sum += i;
		if (sum == 100) flag = true;
		return;
	}
	
	for (int i = start; i < 9; i++) {
		if (visit[i]) continue;
		visit[i] = true;
		chosen.emplace_back(table[i]);
		Combination(cnt + 1, i + 1);
		if (flag) return;
		chosen.pop_back();
		visit[i] = false;
	}
}

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	for (int i = 0; i < 9; i++) cin >> table[i];

	//algorithm part
	Combination(0, 0);
	sort(chosen.begin(), chosen.end());
	for (int i : chosen) cout << i <<endl;
	return 0;
}

{% endraw %}
```

