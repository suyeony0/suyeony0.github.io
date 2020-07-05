---
layout: post
title: [SAMSUNG SW - Magic Star]
date: 2020-7-5
description: txt to markdown
thumbnail: work1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

﻿[232. SAMSUNG SW – Magic Star]
- It was a permutation problem. Thanks to this problem, I used DFS for a long time.
- First, I had to record empty position of magic star and had to find missing numbers.
- Second, For each empty position, I’ve inserted a possible value in turn with lexicographical order.
- I’ve forgot to check spending time. But I guess almost 40 minutes or so.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>

using namespace std;

vector<vector<int>> table(5, vector<int>(9, -1));
vector<bool> alpha(12, 0);
vector<int> need_number;
vector<pair<int, int>> pos;
vector<bool> visit;
bool found = false;
int empty_size = 0;

bool IsMagicStar() {

	int sum = 0;
	for (int i = 0, j = 4; i < 4; i++, j--) sum += table[i][j]+1;
	if (sum != 26) return false;
	
	sum = 0;
	for (int i = 0, j = 4; i < 4; i++, j++) sum += table[i][j]+1;
	if (sum != 26) return false;
	
	sum = 0;
	for (int j = 1; j < 9; j += 2) sum += table[1][j]+1;
	if (sum != 26) return false;

	sum = 0;
	for (int j = 1; j < 9; j += 2) sum += table[3][j]+1;
	if (sum != 26) return false;

	sum = 0;
	for (int i = 4, j = 4; i > 0; i--, j--) sum += table[i][j]+1;
	if (sum != 26) return false;

	sum = 0;
	for (int i = 4, j = 4; i > 0; i--, j++) sum += table[i][j]+1;
	if (sum != 26) return false;

	return true;
	
}

void DFS(int insert_pos, int cnt) {
	if (cnt == empty_size) {
		if (IsMagicStar()) {
			found = true;
		} 
		return;
	}

	int x = pos[insert_pos].first; int y = pos[insert_pos].second;
	for (int i = 0; i < empty_size; i++) {
		if (visit[i] == true) continue;
		table[x][y] = need_number[i];
		visit[i] = true;
		DFS(insert_pos+1, cnt + 1);
		if (found) return;
		visit[i] = false;
		table[x][y] = -1;
	}
}

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	string input;
	for (int i = 0; i < 5; i++) {
		cin >> input;
		for (int j = 0; j < 9; j++) {
			if (input[j] == 'x') pos.emplace_back(make_pair(i, j));
			else if ('A' <= input[j] && input[j] <= 'L') {
				table[i][j] = input[j] - 'A';
				alpha[input[j] - 'A'] = true;
			} 
		}
	}
	empty_size = pos.size();
	for (int i = 0; i < 12; i++) if (alpha[i] == false) need_number.emplace_back(i);
	visit.assign(need_number.size(), false);
	//algorithm part
	DFS(0, 0);
	for (int i = 0; i < 5; i++) {
		for (int j = 0; j < 9; j++) {
			if (table[i][j] != -1) cout << char(table[i][j] + 'A');
			else cout << '.';
		}
		cout << endl;
	}
}

{% endraw %}
```

