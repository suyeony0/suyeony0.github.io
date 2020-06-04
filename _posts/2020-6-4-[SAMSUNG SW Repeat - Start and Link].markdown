---
layout: post
title: [SAMSUNG SW Repeat - Start and Link]
date: 2020-6-4
description: txt to markdown
thumbnail: work1.jpg
categories: SAMSUNG_SW

# Information for the author block
author : Loui
---

[11. SAMSUNG SW : Start and Link]
- it was a combination problem. so when I used next_permutation, time limit exceeded occurred.
- I implemented Combination using DFS.
- I spent 20 minutes.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<algorithm>
#define min(a,b) a>b?b:a
using namespace std;

int N;
vector<vector<int>> table;
vector<int> players;
vector<int> team_a;
vector<int> team_b;
vector<bool> visit;
int answer = 987654321;

void Calculate() {
	int score_a = 0;
	int score_b = 0;
	

	for (int i = 0; i < N / 2; i++) {
		for (int j = i + 1; j < N / 2; j++) {
			score_a += table[team_a[i]][team_a[j]] + table[team_a[j]][team_a[i]];
			score_b += table[team_b[i]][team_b[j]] + table[team_b[j]][team_b[i]];
		}
	}
	
	answer = min(answer, abs(score_a - score_b));
	
}


void DFS(int cnt,int start) {
	if (cnt == (N / 2)) {
		for (int i = 0; i < N; i++) if (visit[i] == false) team_b.emplace_back(i);
		Calculate();
		team_b.clear();
		return;
	}

	for (int i = start; i < N; i++) {
		if (visit[i] == false) {
			visit[i] = true;
			team_a.emplace_back(i);
			DFS(cnt + 1, i + 1);
			team_a.pop_back();
			visit[i] = false;
		}
	}
}

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	cin >> N;
	table.assign(N, vector<int>(N, 0));
	visit.assign(N, false);
	for (int i = 0; i < N; i++) {
		players.emplace_back(i);
		for (int j = 0; j < N; j++) {
			cin >> table[i][j];
		}
	}

	//algorithm part
	DFS(0, 0);
	cout << answer;
	return 0;
}


{% endraw %}
```

