---
layout: post
title: [SAMSUNG SW - Connection]
date: 2020-7-10
description: txt to markdown
thumbnail: city2.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

﻿[237. SAMSUNG SW – Connection]
- It was a BFS problem. But there was restrictions.
- We have to minimize two path without overlapping a line on another line.
- First, using queue, I found A’s minimum path and record the path.
- Second, Considering the recorded path, I found B’s minimum path.
- Third, after swapping A and B, repeating First and Second. Since we have to consider which one have to be first line to find minimum.
- I spent 43 minutes and 31 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<queue>
#define MAX 987654321
using namespace std;

int N, M;
vector<vector<int>> table;

int asx, asy, adx, ady;
int bsx, bsy, bdx, bdy;
int answer = MAX;

int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };

void BFS(int a, int b, int c, int d, int e, int f, int g, int h) {
	
	queue <pair<vector<int>, vector<pair<int,int>>>> que;
	que.push(make_pair(vector<int>{a, b,0}, vector<pair<int,int>>{make_pair(a,b)})); //pair of (current position vector with move count) , (all the shell passed)
	vector<vector<bool>> visit(N,vector<bool>(M,false));
	visit[a][b] = true;
	visit[e][f] = true;
	visit[g][h] = true;
	vector<pair<int, int>> record;
	int a_dis = MAX; int b_dis = MAX;
	while (!que.empty()) {
		int x = que.front().first[0]; int y = que.front().first[1]; int cnt = que.front().first[2]; vector<pair<int, int>> path = que.front().second;
		if (x == c && y == d) {
			record = path;
			a_dis = cnt;
			break;
		}
		que.pop();
		for (int d = 0; d < 4; d++) {
			int nx = x + dir[d][0]; int ny = y + dir[d][1];
			if (nx < 0 || ny < 0 || nx >= N || ny >= M || visit[nx][ny] == true) continue;
			path.emplace_back(make_pair(nx, ny));
			que.push(make_pair(vector<int>{nx, ny, cnt + 1}, path));
			path.pop_back();
			visit[nx][ny] = true;
		}

	}
	


	queue<vector<int>> que2;
	que2.push(vector<int>{e, f, 0});
	visit.assign(N, vector<bool>(M, false));
	for (pair<int, int> row : record) visit[row.first][row.second] = true; 
	visit[e][f] = true;
	visit[a][b] = true;
	visit[c][d] = true;

	while (!que2.empty()) {
		int x = que2.front()[0]; int y = que2.front()[1]; int cnt = que2.front()[2];
		if (x == g && y == h) {
			b_dis = cnt;
			break;
		}
		que2.pop();
		for (int d = 0; d < 4; d++) {
			int nx = x + dir[d][0]; int ny = y + dir[d][1];
			if (nx < 0 || ny < 0 || nx >= N || ny >= M || visit[nx][ny] == true) continue;
			que2.push(vector<int>{nx, ny, cnt + 1});
			visit[nx][ny] = true;
		}

	}
	answer = min(answer, a_dis + b_dis);
	return;

}


int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	cin >> M >> N;
	cin >> asy >> asx >> ady >> adx;
	cin >> bsy >> bsx >> bdy >> bdx;
	N += 1; M += 1;
	table.assign(N, vector<int>(M, 0));

	//algorithm part
	BFS(asx, asy, adx, ady, bsx, bsy, bdx, bdy);
	BFS(bsx, bsy, bdx, bdy, asx, asy, adx, ady);
	if (answer == MAX) cout << "IMPOSSIBLE";
	else cout << answer;
	return 0;

}

{% endraw %}
```

