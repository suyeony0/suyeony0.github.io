---
layout: post
title: [SAMSUNG SW Repeat - Quit The Job]
date: 2020-6-4
description: txt to markdown
thumbnail: city2.jpg
categories: SAMSUNG_SW

# Information for the author block
author : Loui
---

[7. SAMSUNG SW : Quit The Job]
- it was a dp problem. the trick is that starting with the last day, get greater value between (acummulated valud of nextday of current day) and (current day + next possible counsel day).
- the logic is that we could take current maximum(dp[i+1]) value without counseling today or take next possible counseling day¡¯s pay with counseling today(table[i]+dp[next_possible_day]).
- I spent 8 minutes and 25 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#define max(a,b) a>b?a:b
using namespace std;

int N;
vector<pair<int, int>> table;

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	cin >> N;
	table.assign(N+1, pair<int, int>());
	for (int i = 0; i < N; i++) {
		cin >> table[i].first >> table[i].second;
	}

	//algorithm part
	vector<int> dp(N + 1, 0);
	
	for (int i = N - 1; i >= 0; i--) {
		if (table[i].first + i > N) dp[i] = dp[i + 1];
		else dp[i] = max(dp[i + 1], table[i].second + dp[i + table[i].first]);	
		
	}
	cout << dp[0];
	return 0;
}


{% endraw %}
```

