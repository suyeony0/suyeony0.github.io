---
layout: post
title: {% raw %}[Samsung SW - Z]{% endraw %}
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}
	﻿[188. [SAMSUNG SW – Z]
	- it was a binary search problem. Actually, it was a quaternary search.
	- we can divide whole square to 4 district, top_left, top_right, bottom_left and bottom_right.
	- and each value follows below rule.
	> top_left = top_left, top_right = top_left + 4^(n-1), 
	> bottom_left = top_left + 2 * 4^(n-1), bottom_right = top_left + 3 * 4^(n-1)
	- Downsizing the square for each round, we re-determine which district has (r,c).
	- if N==1 or top_left +1 ==top_right, then end of while.
	- see the code.
	#include<iostream>
	#include<cmath>
	using namespace std;
	int N, r, c;
	long long top_left, top_right, bottom_left, bottom_right;
	void resizing() {
		if (r < pow(2, N - 1) && c < pow(2, N - 1)) { //top_left
		}  
		else if (r < pow(2, N - 1) && c >= pow(2, N - 1)) {//top_right
			top_left = top_right;
			c -= pow(2, N - 1);
		}  
		
		else if (r >= pow(2, N - 1) && c < pow(2, N - 1)) {//bottom_left
			top_left = bottom_left;
			r -= pow(2, N - 1);
		}  
		else {//bottom_right
			top_left = bottom_right;
			c -= pow(2, N - 1);
			r -= pow(2, N - 1);
		}  
		N--;
		top_right = top_left + pow(4, N - 1);
		bottom_left= top_left + 2*pow(4, N - 1);
		bottom_right = top_left + 3 * pow(4, N - 1);
	}
	
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
		//get input
		cin >> N >> r >> c;
	
		//algorithm part
		// tr = 4^(n-1) + top_left, bl = 2 * 4^(n-1) + top_left , br = 3 * 4^(n-1) + top_left , 
		top_left = 0, top_right = pow(4,N-1), bottom_left = 2 * pow(4, N-1), bottom_right = 3 * pow(4, N-1); //default number
		while (N>1) {
			resizing();
		}
		if (r == 0 && c == 0) cout << top_left;
		else if (r == 0 && c == 1) cout << top_right;
		else if (r == 1 && c == 0) cout << bottom_left;
		else cout << bottom_right;
		return 0;
	}
	
{% endraw %}
