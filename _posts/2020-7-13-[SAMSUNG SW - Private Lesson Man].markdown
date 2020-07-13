---
layout: post
title: [SAMSUNG SW - Private Lesson Man]
date: 2020-7-13
description: txt to markdown
thumbnail: work1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

﻿[238. SAMSUNG SW – Private Lesson Man]
- It was a difficult BFS problem.
- A shell has 2 numbers and we can move when a shell has same number with its adjacent shell and the two numbers are adjacent directly.
- I also had to record path to destination. Morever, when we can not arrive destination, we had to return the greatest shell we can reach with the path.
- First, I took input as a 2D array, like given example.
> 1 2 2 4 4 5
>  2 4 5 3 …
- Second, I made a vector “visit” to check a shell we’ve already visit.
- Third, I create a function “ResIndex” that it returns a shell’s number corresponding to the shell’s index.
- Fourth, I create a function “ResPair” that it returns a pair of coordinates which occupy same shell.
- Fifth, I used queue to implemet BFS, the que has current coordinates, count of move, and path.
> Using the coordinates and using ResPair function, we can get the frined’s coordinate and number.
> the two given coordinates, I visited adjancet shells using BFS.
- Sixth, If we can get destinaion, return the count of move and path. if not and que becomes empty, return the greatest number of shell with its path.
- I spent 1 hours and 20 minutes.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<queue>
using namespace std;
int N,M;
vector<vector<int>> table;
vector<bool> visit;
int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };
int destination;
vector<int> max_path;
int cur_max = 0;
int cur_answer = 0;
int answer;
bool flag = false;
//N+(N-1)

inline int ResIndex(int x, int y) {
	int res = 0;
	if (x % 2 == 0) {
		res = (N + N - 1) * (x/2) + 1;
		res += (y / 2);

	}
	else {
		res = N;
		res += (N + N - 1) * (x / 2) + 1;
		res += (y - 1) / 2;
	}
	return res;
}


inline pair<int,int> ResPair(int x, int y) {
	if (x % 2 == 0) {
		if (y % 2 == 0) return make_pair(x, y + 1);
		else return make_pair(x, y - 1);
	}
	else {
		if (y % 2 == 0) return make_pair(x, y - 1);
		else return make_pair(x, y + 1);
	}
}

void PrintTable() {
	cout << endl;
	for (vector<int> row : table) {
		for (int i : row) cout << i << " ";
		cout << endl;
	}
	cout << endl;
}

vector<int> BFS() {
	queue<pair<vector<int>, vector<int>>> que;
	que.push(make_pair(vector<int>{0, 0, 1}, vector<int>{1}));
	max_path = vector<int>{ 1 };
	visit[ResIndex(0, 0)] = true;
	 
	while (!que.empty()) {
		int fx = que.front().first[0]; int fy = que.front().first[1]; int cnt = que.front().first[2];  vector<int> path = que.front().second;
		pair<int, int> cor = ResPair(fx, fy); int lx = cor.first; int ly = cor.second;
		que.pop();
		if (ResIndex(fx, fy) == destination) {
			answer = cnt;
			flag = true;
			return path;
		}
		if (cur_max < ResIndex(fx, fy)) {
			max_path = path;
			cur_max = ResIndex(fx, fy);
			cur_answer = cnt;
		}

		for (int d = 0; d < 4; d++) {
			int nfx = fx + dir[d][0]; int nfy = fy + dir[d][1]; int nlx = lx + dir[d][0]; int nly = ly + dir[d][1];
			if (nfx < 0 || nfy < 0 || nlx < 0 || nly < 0 || nfx>=N || nlx>=N || nfy>=M || nly>=M) continue;
			if (table[nfx][nfy] == table[fx][fy] && visit[ResIndex(nfx, nfy)] == false) {
				path.emplace_back(ResIndex(nfx, nfy));
				visit[ResIndex(nfx, nfy)] = true;
				que.push(make_pair(vector<int>{nfx, nfy, cnt + 1}, path));
				path.pop_back();
			}
			if (table[nlx][nly]==table[lx][ly] && visit[ResIndex(nlx,nly)]==false) {
				path.emplace_back(ResIndex(nlx, nly));
				visit[ResIndex(nlx, nly)] = true;
				que.push(make_pair(vector<int>{nlx, nly, cnt + 1}, path));
				path.pop_back();
			}
		}
	}

	// return max path
	return max_path;
}


int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	cin >> N;
	M = 2 * N;
	table.assign(N, vector<int>( M, -1));
	int a, b;
	for (int i = 0; i < N; i++) {
		if (i % 2 == 0) {
			for (int j = 0; j < M; j+=2) {
				cin >> table[i][j] >> table[i][j + 1];
			}
		}
		else {
			for (int j = 1; j < M - 1; j+=2) {
				cin >> table[i][j] >> table[i][j + 1];
			}
		}
	}

	if (N % 2 == 1) {
		destination = (N + N - 1) * (N / 2) + N;
		visit.assign((N + N - 1) * (N / 2) + N+1, 0);
	} 
	else {
		destination = (N + N - 1) * (N / 2);
		visit.assign((N + N - 1) * (N / 2)+1, 0);
	}

	
	//algorithm part
	vector<int> res = BFS();
	if (flag) {
		cout << answer << endl;
		for (int i : res) cout << i << " ";
	}
	else {
		cout << cur_answer<<endl;
		for (int i : max_path) cout << i << " ";
	}

	return 0;
}

{% endraw %}
```

