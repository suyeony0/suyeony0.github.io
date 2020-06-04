---
layout: post
title: [SAMSUNG SW Repeat - Gerraymandering 3]
date: 2020-6-4
description: txt to markdown
thumbnail: breakfast-orange-lemon-oranges-large.jpg
categories: SAMSUNG_SW

# Information for the author block
author : Loui
---

﻿[26. SAMSUNG SW : Gerrymandering 3]
- It was a simulation problem. Actuaaly it was a classification problem.
- I can have divided the given area to 5 district and find minimum difference between a maximum population district and a minimum population district
- it was quite hard to find the way to divide the area. I tried lots of things. Finally, I found an easy way.
- First, drawing boundaries for 4 diagonal shape of district 5.
- Second, for each district, if we meet district 5, stop allocating number to a shell.
- I spent 1 hour and 27 minutes and 47 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<algorithm>
#define max(a,b) a>b?a:b
#define min(a,b) a>b?b:a
using namespace std;

int N;
vector<vector<int>> table;
vector<vector<int>> dis;
int answer = 987654321;

void printTable() {
	cout << endl;
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < N; j++) {
			cout << dis[i][j] << " ";
		}
		cout << endl;
	}
}

void Gerrymandering(int x, int y, int d1, int d2) {
	if (!(d1 >= 1 && d2 >= 1 && 1 <= x + 1 && x + 1 < x + 1 + d1 + d2 && x + 1 + d1 + d2 <= N && 1 <= y + 1 - d1 && y + 1 - d1 < y + 1 && y + 1 < y + 1 + d2 && y + 1 + d2 <= N)) return;

	for (int i = x, j = y; i <= x + d1 && j >= y - d1; i++,j--) {
		dis[i][j] = 5;
	}

	for (int i = x, j = y; i <= x + d2 && j <= y + d2; i++,j++) {
		dis[i][j] = 5;
	}

	for (int i = x + d1, j = y - d1; i <= x + d1 + d2 && j <= y - d1 + d2; i++,j++) {
		dis[i][j] = 5;
	}

	for (int i = x + d2, j = y + d2; i <= x + d1 + d2 && j >= y + d2 - d1; i++, j--) {
		dis[i][j] = 5;
	}

	for (int i = 0; i < x + d1; i++) {
		for (int j = 0; j < y+1; j++) {
			if (dis[i][j] == 5) break;
			dis[i][j] = 1;
		}
	}
	for (int i = 0; i < x + d2+1; i++) {
		for (int j = N - 1; j >= y+1; j--) {
			if (dis[i][j] == 5) break;
			dis[i][j] = 2;
		}
	}
	for (int i = x + d1; i < N; i++) {
		for (int j = 0; j < y - d1 + d2; j++) {
			if (dis[i][j] == 5) break;
			dis[i][j] = 3;
		}
	}

	for (int i = x + d2+1; i < N; i++) {
		for (int j = N - 1; j >= y - d1 + d2; j--) {
			if (dis[i][j] == 5) break;
			dis[i][j] = 4;
		}
	}

	
	
	vector<int> sum(6,0);
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < N; j++) {
			sum[dis[i][j]] += table[i][j];
		}
	}
	sum[0] += sum[5];
	sum.pop_back();
	sort(sum.begin(), sum.end());
	answer = min(answer, sum[4] - sum[0]);



}


int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	cin >> N;
	table.assign(N, vector<int>(N, 0));
	
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < N; j++) {
			cin >> table[i][j];
		}
	}

	//algorithm part
	for (int x = 0; x <= N - 3; x++) {
		for (int y = 1; y <= N - 2; y++) {
			for (int d1 = 1; x+d1<=N-2 && y-d1>=0; d1++) {
				for (int d2 = 1; x + d2 <= N - 2 && y + d2 <= N - 1; d2++) {
					dis.assign(N, vector<int>(N, 0));
					Gerrymandering(x, y, d1, d2);
				}
			}
		}
	}
	cout << answer;
	return 0;
}

{% endraw %}
```

