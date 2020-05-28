---
layout: post
title: [Samsung SW - King]
date: 2020-5-29
description: txt to markdown
thumbnail: city2.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

{% highlight c++ %}
```cpp
	﻿
	[187. [SAMSUNG SW – KING]
	- it was an easy simulation problem. I had to just follow given moving order.
	- it has an restriction to move king that after moving king, if there is stone, stone also have to be moved. but this restriction was so easy to implement.
	- see the code.
	#include<iostream>
	#include<array>
	#include<vector>
	#include<map>
	using namespace std;
	array<array<int, 8>, 8> board;
	
	int main() {
	
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
		//get input
		string stone; string king; int N;
		cin >> king >> stone >> N;
		vector<string> orders(N,"");
		for (int i = 0; i < N; i++) cin >> orders[i];
		
		int sy =stone[0] - 'A'; int sx = 8 - (stone[1] - '0');
		int ky = king[0] - 'A'; int kx = 8 - (king[1] - '0' );
		//algorithm part
		map<string, pair<int, int>> direction;
		direction["R"] = make_pair(0, 1); direction["L"] = make_pair(0, -1); direction["B"] = make_pair(1, 0); direction["T"] = make_pair(-1, 0);
		direction["RT"] = make_pair(-1, 1); direction["LT"] = make_pair(-1, -1); direction["RB"] = make_pair(1, 1); direction["LB"] = make_pair(1, -1);
		
		for (string s : orders) {
			int dx = direction[s].first; int dy = direction[s].second; 
			if (sx == dx + kx && sy == dy + ky) {
				if (sx + dx < 0 || sy + dy < 0 || sx + dx >= 8 || sy + dy >= 8 || kx + dx < 0 || ky + dy < 0 || kx + dx >= 8 || ky + dy >= 8) continue;
				else kx = dx + kx; ky = dy + ky; sx = dx + sx; sy = dy + sy;
			}
			else if (kx + dx >= 0 && ky + dy >= 0 && kx + dx < 8 && ky + dy < 8) {
				kx = dx + kx; ky = dy + ky;
			}
		}
		cout << char('A' + ky) << 8 - kx << endl;
		cout << char('A' + sy) << 8 - sx << endl;
		return 0;
	
	}
	
```
{% endhighlight %}
