---
layout: post
title: [SAMSUNG SW - Candy Game]
date: 2020-6-27
description: txt to markdown
thumbnail: food2.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

﻿[227. SAMSUNG SW – Candy Game]
- It was an easy simulation problem.
- Even thought it was easy, I’ve stucked by an edge condition that I had to check the origin array.
- First, swapping 2 elements in a row and checking those columns.
- Seoncd, Swapping 2 elements in a column and checking those rows.
- I spent 32 minutes and 5 seconds by the edge condition.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#define max(a,b) a>b? a:b
using namespace std;

vector<vector<char>> table;
int N;
int answer = 1;

void LongestCandy(bool isRow,int ax1,int ax2) {

	if (isRow) {
		int temp1 = 1; int temp2 = 1;
		char cur1 = table[0][ax1]; char cur2 = table[0][ax2];
		for (int i = 1; i < N; i++) {
			if (table[i][ax1] == cur1) temp1 += 1;
			else {
				answer = max(answer, temp1);
				cur1 = table[i][ax1];
				temp1 = 1;
			}
			if (table[i][ax2] == cur2) temp2 += 1;
			else {
				answer = max(answer, temp2);
				cur2 = table[i][ax2];
				temp2 = 1;
			}
		}

		answer = max(answer, temp1);
		answer = max(answer, temp2);
	}

	else {
		int temp1 = 1; int temp2 = 1;
		char cur1 = table[ax1][0]; char cur2 = table[ax2][0];
		for (int j = 1; j < N; j++) {
			if (table[ax1][j] == cur1) temp1 += 1;
			else {
				answer = max(answer, temp1);
				cur1 = table[ax1][j];
				temp1 = 1;
			}
			if (table[ax2][j] == cur2) temp2 += 1;
			else {
				answer = max(answer, temp2);
				cur2 = table[ax2][j];
				temp2 = 1;
			}
		}
		answer = max(answer, temp1);
		answer = max(answer, temp2);
	}


}


int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	cin >> N;
	table.assign(N, vector<char>(N, ' '));
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < N; j++) {
			cin>>table[i][j];
		}
	}



	//algorithm part
	for (int i = 0; i < N - 1; i++) {
		LongestCandy(false, i, i + 1);
	}
	for (int j = 0; j < N - 1; j++) {
		LongestCandy(true, j, j + 1);

	}

	for (int i = 0; i < N; i++) {
		for (int j = 0; j < N-1; j++) {
			swap(table[i][j], table[i][j + 1]);
			LongestCandy(true, j, j + 1);
			swap(table[i][j], table[i][j + 1]);

			if (i == N - 1) continue;
			swap(table[i][j], table[i + 1][j]);
			LongestCandy(false, i, i + 1);
			swap(table[i][j], table[i + 1][j]);
		}
		if (i == N - 1) break;
		swap(table[i][N -1], table[i + 1][N - 1]);
		LongestCandy(false, i, i + 1);
		swap(table[i][N - 1], table[i + 1][N - 1]);
	}

	cout << answer;
	return 0;
} 


{% endraw %}
```

