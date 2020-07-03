---
layout: post
title: [SAMSUNG SW - Lake of Swan]
date: 2020-7-3
description: txt to markdown
thumbnail: work1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

[230. SAMSUNG SW – Lake of Swan]
- it was a BFS problem. But it has a rigid time limit.
- My first trial was to use naïve BFS. But I’ve stuck by time.
- Second trial was binary search. For that, I’ve preprocessed how many day will be needed to melt each ice. Then, I used binary search to find minimum day that was needed to meet two swans. But I’ve stuck by time and some test-cases were not passed.
- Third trial was using four queue. For each round, I’ve recorded possible swan’s positions and possible ice that can be melt.
- Then, for those position, I pushed adjacent shells that can be next position of a swan and ice can be melt at next round.
- I spent 1 hours and 43 minutes and 26 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<queue>
#define EM 0
#define ICE 987654321
using namespace std;

int N, M;
queue<vector<int>> waterQ;
queue<vector<int>> swanQ;
vector<vector<int>> table;
vector<vector<bool>> visit;
vector<pair<int,int>> swan; //sx sy, dx dy
int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };
int sx, sy, dx, dy;


void PrintTable() {
	cout << endl;
	for (vector<int> row : table) {
		for (int c : row) cout << c << " ";
		cout << endl;
	}
	cout << endl;
}

void MeltingPreprocessing() {
	queue<vector<int>> water = waterQ;
	waterQ = queue<vector<int>>{};
	while (!water.empty()) {
		int x = water.front()[0]; int y = water.front()[1]; water.pop();
		for (int d = 0; d < 4; d++) {
			int nx = x + dir[d][0]; int ny = y + dir[d][1];
			if (nx < 0 || ny < 0 || nx >= N || ny >= M) continue;
			if (table[nx][ny] == ICE) {
				table[nx][ny] = EM;
				waterQ.push(vector<int>{nx, ny});
			}
		}
	}
}

bool Travel() {
	queue<vector<int>> que=swanQ;
	swanQ = queue<vector<int>>{};
	visit[que.front()[0]][que.front()[1]] = true;
	while (!que.empty()) {
		int x = que.front()[0]; int y = que.front()[1]; que.pop();
		for (int d = 0; d < 4; d++) {
			int nx = x + dir[d][0]; int ny = y + dir[d][1];
			if (nx < 0 || ny < 0 || nx >= N || ny >= M || visit[nx][ny]==true) continue;
			if (table[nx][ny]==ICE) {
				swanQ.push(vector<int>{nx, ny});
				visit[nx][ny] = true;
				continue;
			}
			if (nx == dx && ny == dy) return true;
			visit[nx][ny] = true;
			que.push(vector<int>{nx, ny});
		}
	}
	return false;
}

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	cin >> N >> M;
	table.assign(N, vector<int>(M,EM));
	visit.assign(N, vector<bool>(M, false));
	string input;
	for (int i = 0; i < N; i++) {
		cin >> input;
		for (int j = 0; j < M; j++) {
			if (input[j] == '.') {
				table[i][j] = EM;
				waterQ.push(vector<int>{i, j});
			} 
			else if (input[j] == 'L') {
				swan.emplace_back(make_pair(i, j));
				waterQ.push(vector<int>{i, j});
				table[i][j] = EM;
			}
			else table[i][j] = ICE;
		}
	}
	sx = swan[0].first; sy = swan[0].second;
	dx = swan[1].first; dy = swan[1].second;
	//algorithm part
	
	
	
	swanQ.push(vector<int>{sx, sy});
	int answer = 0;
	while (!Travel()) {
		answer += 1;
		MeltingPreprocessing();
	}
	cout << answer;
	return 0;

}


{% endraw %}
```

