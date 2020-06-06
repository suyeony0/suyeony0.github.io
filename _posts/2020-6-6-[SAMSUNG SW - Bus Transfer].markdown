---
layout: post
title: [SAMSUNG SW - Bus Transfer]
date: 2020-6-6
description: txt to markdown
thumbnail: breakfast-orange-lemon-oranges-large.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

﻿[209. SAMSUNG SW : Bus Transfer]
- It was a simulation problem. it was so hard for me.
- I used DFS to find path to destination. but memory limit exceeded.
- see the first code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<map>
#include<set>
#define min(a,b) a>b? b:a
using namespace std;

vector<bool> visit;
vector<vector<int>> shell_visit;
int sx, sy, dx, dy;
int N, M, K;
map<pair<int, int>, set<int>> table;
vector<vector<short>> bus; //number, x1, y1, x2, y2 ,dir , if dir==1 , then vertical
int answer;
inline int Y(int y) {
	return N - y;
}

int DFS(int x, int y) {
	if (x == dx && y == dy) {
		return 0;
	}
	if (shell_visit[y][x] != -1) return shell_visit[y][x];
	
	

	int res = 987654321;
	for (int b : table[make_pair(y,x)]) {
		if (visit[b]) continue;
		visit[b] = true;
		//cout << x << " , " << y <<" : "<<b<< endl;
		
		int x1 = bus[b][1]; int y1 = bus[b][2]; int x2 = bus[b][3]; int y2 = bus[b][4]; int d = bus[b][5];
		if (d) { //vertical
			if (y1 > y2) {
				for (int j = y2; j <= y1; j++) {
					if(!table[make_pair(j,x1)].empty()) res = min(res, DFS(x1, j) + 1);
				}
			}
			else {
				for (int j = y1; j <= y2; j++) {
					if (!table[make_pair(j, x1)].empty()) res = min(res, DFS(x1, j) + 1);
				}
			}
		}
		else { //horizon
			if (x1 > x2) {
				for (int j = x2; j <= x1; j++) {
					if (!table[make_pair(y1, j)].empty()) res=min(res,DFS(j, y1)+1);
				}
			}
			else{
				for (int j = x1; j <= x2; j++) {
					if (!table[make_pair(y1, j)].empty()) res = min(res, DFS(j, y1) + 1);
				}
			}
		}
		visit[b] = false;
		
	}
	shell_visit[y][x] = res;
	return res;
}


int main() {
	ios_base::sync_with_stdio(false);
	cout.tie(NULL); cout.tie(NULL);

	//get input
	cin >> M >> N >> K;
	shell_visit.assign(N, vector<int>(M, -1));
	bus.assign(K, vector<short>(6,0));
	visit.assign(K, false);
	int b;
	int x1, x2, y1, y2;
	for (int i = 0; i < K; i++) {
		cin >> b;
		for (int j = 1; j < 5; j++) {
			cin >> bus[b-1][j];
			//bus[b-1][j] -= 1;
		}
		bus[b - 1][1] -= 1; bus[b - 1][3] -= 1;
		bus[b - 1][2] = Y(bus[b - 1][2]);
		bus[b - 1][4] = Y(bus[b - 1][4]);
		int temp;
		x1 = bus[b - 1][1]; y1 = bus[b - 1][2]; x2 = bus[b - 1][3]; y2 = bus[b - 1][4];
		if (x1==x2) { // vertical
			bus[b - 1][5] = 1;
			if (y1 > y2) {
				for (int j = y2; j <= y1; j++) table[make_pair(j,x1)].insert(b-1);
			}
			else {
				for (int j = y1; j <= y2; j++) table[make_pair(j, x1)].insert(b - 1);
			}
		}
		else { //horizon
			bus[b - 1][5] = 0;
			if (x1 > x2) {
				for (int j = x2; j <= x1; j++) table[make_pair(y1, j)].insert(b - 1);
			}
			else {
				for (int j = x1; j <= x2; j++) table[make_pair(y1, j)].insert(b - 1);
			}
		}
	}
	cin >> sx >> sy >> dx >> dy;
	sx--;  dx--; 
	sy = Y(sy); dy = Y(dy);

	/*cout << endl;
	for (int i = 0; i < K; i++) {
		for (int j = 0; j < bus[i].size();j++) cout << bus[i][j] << " ";
		cout << endl;
	}
	cout << endl;*/
	//algorithm part
	answer=DFS(sx,sy);
	cout << answer;
	return 0;

}
- so I searched and find a way.
- the indice ranges are so wide. so I wasn’t able to use 2D array. 
- Using BFS, finding a bus I can transfer. the below code is from google.
- I Spent 1 hour and 41 minutes and 38 seconds.
- see the code.
#include <iostream>
#include <queue>
using namespace std;

struct info {
	int x1;
	int y1;
	int x2;
	int y2;
	bool is_in(const int& x, const int& y)const {
		return (x >= x1 && x <= x2 && y >= y1 && y <= y2);
	}
	bool is_in(const info& a)const {
		return (a.x1 <= x2 && a.x2 >= x1 && a.y1 <= y2 && a.y2 >= y1);
	}

};
void swap(int& a, int& b) {
	int tmp = a;
	a = b;
	b = tmp;
}
int visited[5001];
info bus[5001];
int M, N, K;
int sx, sy, dx, dy;
queue<int> q;
int bfs() {
	for (int i = 0; i < K; i++) {
		if (bus[i].is_in(sx, sy)) {
			q.push(i);
			visited[i] = 1;
		}
	}
	while (!q.empty()) {
		int idx = q.front();
		if (bus[idx].is_in(dx, dy)) {
			return visited[idx];
		}
		q.pop();
		for (int i = 0; i < K; i++) {
			if (visited[i]) continue;
			if (bus[idx].is_in(bus[i])) {
				visited[i] = visited[idx] + 1;
				q.push(i);
			}
		}
	}
}
int main() {
	ios::sync_with_stdio(false);
	cin.tie(0);
	cin >> M >> N >> K;
	for (int i = 0; i < K; i++) {
		int num, x1, y1, x2, y2;
		cin >> num >> x1 >> y1 >> x2 >> y2;

		if (y1 > y2) swap(y1, y2);
		if (x1 > x2) swap(x1, x2);
		bus[i] = { x1,y1,x2,y2 };
	}
	cin >> sx >> sy >> dx >> dy;
	cout << bfs() << "\n";
	return 0;
}

{% endraw %}
```

