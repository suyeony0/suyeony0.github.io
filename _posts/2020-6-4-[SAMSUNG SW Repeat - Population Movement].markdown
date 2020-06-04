---
layout: post
title: [SAMSUNG SW Repeat - Population Movement]
date: 2020-6-4
description: txt to markdown
thumbnail: food2.jpg
categories: SAMSUNG_SW

# Information for the author block
author : Loui
---

﻿[19. SAMSUNG SW : Population Movement]
- it was a BFS problem. To determine unions, I used BFS, and record each country in a vector.
- After determining a union, using vecter that has countries, I allocated population to all the country in the union evenly.
- And if there was a change, I set bool flag == false so as to continue.
- I spent 20 minutes.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<queue>
using namespace std;

int N,L,R;
vector<vector<int>> table;
vector<vector<bool>> visit;
int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };
bool flag;


void BFS(int x, int y) {
	queue<vector<int>> que;
	int sum = table[x][y];
	int cnt = 1;
	vector<pair<int, int>> uni;
	que.push(vector<int>{x, y}); //x y cnt
	visit[x][y] = true;
	uni.emplace_back(make_pair(x, y));
	while (!que.empty()) {
		x = que.front()[0]; y = que.front()[1]; que.pop();
		for (int i = 0; i < 4; i++) {
			int nx = x + dir[i][0]; int ny = y + dir[i][1];
			if (nx >= 0 && ny >= 0 && nx < N && ny < N && visit[nx][ny] == false && L<=abs(table[x][y] - table[nx][ny]) && abs(table[x][y] - table[nx][ny]) <= R) {
				visit[nx][ny] = true;
				que.push(vector<int>{nx,ny});
				uni.emplace_back(make_pair(nx, ny));
				cnt += 1;
				sum += table[nx][ny];
			}
		}
	}
	int res = sum / cnt;
	if (cnt >= 2) flag = false;
	for (pair<int, int> shell : uni) {
		table[shell.first][shell.second] = res;
	}
}

void printTable() {
	cout << endl;
	for (vector<int> row : table) {
		for (int i : row) cout << i << " ";
		cout << endl;
	}
	cout << endl;
}

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	cin >> N>>L>>R;
	table.assign(N, vector<int>(N, 0));
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < N; j++) {
			cin >> table[i][j];
		}
	}

	//algorithm part
	int answer = 0;
	
	while (true) {
		flag = true;
		visit.assign(N, vector<bool>(N, 0));
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < N; j++) {
				if (visit[i][j] == false) {
					BFS(i,j);
				}
			}
		}
		//printTable();
		if (flag) break;
		answer += 1;
	}
	cout << answer;
	return 0;
	

}

{% endraw %}
```

