---
layout: post
title: [SAMSUNG SW Repeat - Gear]
date: 2020-6-4
description: txt to markdown
thumbnail: food2.jpg
categories: SAMSUNG_SW

# Information for the author block
author : Loui
---

[13. SAMSUNG SW : Gear]
- it was a simulation problem. it was easy but I have been stucked due to direction.
- when a gear rotate, another gear has to rotate an opposite direction. I implement it with define command. but there was something wrong.
- afther I revise the define function. it worked well.
- I spent 33 minutes and 33 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#define opposite(a) -a
using namespace std;

int K;
vector<vector<int>> table(4,vector<int>(8,0)); //2 and 6 is edge.
vector<pair<int, int>> order;
vector<bool> visit(4,false);

void Rotate(int i, int dir) {
	int temp;
	if (dir == 1) {
		temp = table[i][7];
		for (int j = 7; j >=1; j--) table[i][j] = table[i][j - 1];
		table[i][0] = temp;
	}
	else {
		temp = table[i][0];
		for (int j = 0; j < 7; j++) table[i][j] = table[i][j + 1];
		table[i][7] = temp;
	}
}

void Play(int i, int dir) {
	if (i == 0) {
		if (table[0][2] != table[1][6] && visit[1] == false) {
			visit[1] = true;
			Play(1, opposite(dir));
			visit[1] = false;
		} 
	}
	else if (i == 3) {
		if (table[3][6] != table[2][2] && visit[2] == false) {
			visit[2] = true;
			Play(2, opposite(dir));
			visit[2] = false;
		} 
	} 
	else {
		if (table[i][6] != table[i - 1][2] && visit[i - 1] == false) {
			visit[i - 1] = true;
			Play(i - 1, opposite(dir));
			visit[i - 1] = false;
		} 
		if (table[i][2] != table[i + 1][6] && visit[i + 1] == false) {
			visit[i + 1] = true;
			Play(i + 1, opposite(dir));
			visit[i + 1] = false;
		} 
	}
	Rotate(i, dir);
}

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	string input;
	for (int i = 0; i < 4; i++) {
		cin >> input;
		for (int j = 0; j < 8; j++) {
			table[i][j]=input[j]-'0';
		}
	}
	cin >> K;
	order.assign(K, pair<int, int>());
	for (int i = 0; i < K; i++) {
		cin >> order[i].first >> order[i].second;
		order[i].first -= 1; //gear number start at 0.
	}

	//algorithm part;
	int answer = 0;
	
	for (pair<int, int> gear : order) {
		visit[gear.first] = true;
		Play(gear.first, gear.second);
		visit[gear.first] = false;
	} 

	for (int i = 0; i < 4; i++) {
		if (table[i][0] == 1) {
			answer += 1 << i;
		}
	}
	cout << answer;
	return 0;
}

{% endraw %}
```

