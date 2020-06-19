---
layout: post
title: [SAMSUNG SW - Start Taxi]
date: 2020-6-19
description: txt to markdown
thumbnail: breakfast-orange-lemon-oranges-large.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

﻿[223. SAMSUNG SW – Start Taxi]
- What a dirty problem!!!
- Because of one edge condition, I spent so much time.
- The edge condition is that a shell can be both of starting point and destination.
- It was one of the problem that I’ve solved at SAMSUNG codingtest 2020.
- I thought I had solved well, but I changed my mind to that I might have been wrong after resolving this problem.
- First, Finding a closest passanger. For that, I record people whom the taxi can reach with spending same fuel.
- Second, Determining a passanger from the record people.
- Third, Bring the person to a destination.
- While moving taxi, if fuel becomes 0, stop the algorithm.
- I spent 2 hours and 41 minutes and 31 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<queue>
#include<set>
#include<map>
using namespace std;

int N, M, K;
vector<vector<int>> table;
map<pair<int,int>,pair<int,int>> people; // sx,sy dx,dy
int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };
int tx, ty;
vector<vector<bool>> visit;
vector<vector<bool>> done_person;
int fuel;
int finish_num = 0;
bool stop = true;
void BFS() {
	visit.assign(N, vector<bool>(N, false));
	queue<vector<int>> que;
	que.push(vector<int>{tx, ty, fuel}); //tx, ty, fuel
	visit[tx][ty] = true;
	set<vector<int>> stk;
	stop = true;
	int cur_fuel;
	//find a closest passanger
	while (!que.empty()) {
		cur_fuel = que.front()[2];
		while (!que.empty()) {
			int x = que.front()[0]; int y = que.front()[1]; fuel = que.front()[2];
			if (cur_fuel != fuel) break; 
			que.pop();
			if (done_person[x][y]==false && people.find(make_pair(x, y))!=people.end()) {
				stk.insert(vector<int>{x, y});
				stop = false;
			}
			if (!stop) continue;
			for (int d = 0; d < 4; d++) {
				int nx = x + dir[d][0]; int ny = y + dir[d][1];
				if (nx < 0 || ny < 0 || nx >= N || ny >= N) continue;
				if (table[nx][ny] ==0 && visit[nx][ny] == false) {
					visit[nx][ny] = true;
					que.push(vector<int>{nx, ny, fuel - 1});
				}
			}
		}
		if (!stop) break;
	}
	if (stop) return;

	//determining passanger
	vector<int> temp = *stk.begin();
	tx = temp[0]; ty = temp[1]; fuel = cur_fuel;
	int dx = people[make_pair(tx, ty)].first;  int dy = people[make_pair(tx, ty)].second;

	//bring him to destination.
	stop = true;
	que = queue<vector<int>>{};
	visit.assign(N, vector<bool>(N, false));
	visit[tx][ty] = true;
	que.push(vector<int>{tx, ty, fuel, 0});
	while (!que.empty()) {
		int x = que.front()[0]; int y = que.front()[1]; fuel = que.front()[2]; int cnt = que.front()[3];
		if (x == dx && y == dy) {
			done_person[tx][ty] = true;
			tx = x; ty = y;
			fuel += cnt * 2;
			finish_num += 1;
			stop = false;
			return; 
		}
		que.pop();
		if (fuel == 0) continue;

		for (int d = 0; d < 4; d++) {
			int nx = x + dir[d][0]; int ny = y + dir[d][1];
			if (nx < 0 || ny < 0 || nx >= N || ny >= N) continue;
			if (table[nx][ny] ==0 && visit[nx][ny] == false) {
				visit[nx][ny] = true;
				que.push(vector<int>{nx, ny, fuel - 1, cnt + 1});
			}
		}
	}


}




int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);
	//get input
	cin >> N >> M >> K;
	table.assign(N, vector<int>(N,0));
	done_person.assign(N, vector<bool>(N,false));
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < N; j++) {
			cin >> table[i][j];
		}
	}
	cin >> tx >> ty;
	tx -= 1; ty -= 1;
	int a, b, c, d;
	for (int i = 0; i < M; i++) {
		cin >> a >> b >> c >> d;
		a -= 1; b -= 1; c -= 1; d -= 1;
		people[make_pair(a, b)] = make_pair(c, d);
	}
	fuel = K;
	//algorithm part;	
	while (finish_num <M) {
		BFS();
		if (stop) {
			fuel = -1;
			break;
		}
		//cout << fuel << endl;
	}
	cout << fuel;
	return 0;
}


{% endraw %}
```

