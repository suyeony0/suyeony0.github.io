---
layout: post
title: [SAMSUNG SW - Mineral]
date: 2020-6-23
description: txt to markdown
thumbnail: food2.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

﻿[224. SAMSUNG SW – Mineral]
- It was a simulation problem with having quite confusing elements.
- They Described the given cave R x C Array. but it was like a wall not ground. 
- I mean, the given array was a standing state. oh.. how can I say? my English is So Sxxk..
- I hope you understand, Let’s take next step.
- First, Thorwing a stick from left to right or right to left in turn. if the stick meets a mineral, remove the mineral.
- Second, Re-clustring the minerals, during checking whether a cluster is on the ground or in the air.
- Third, if a cluster is in the air, we have to drop it down until it meets a different cluster or ground.
- I spent 1 hours and 13 minutes and 2 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<queue>
#define EM 0
#define NEM 9
using namespace std;

int N, M,K;
vector<vector<int>> table;
vector<int> sticks;
int in_the_air = 0;
int num_of_sticks;
int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };


inline int reverseX(int x) { return N - x; }

void Throw(bool left,int height) {
	if (left) {
		for (int j = 0; j < M; j++) {
			if (table[height][j] !=EM) {
				table[height][j] = EM;
				return;
			}
		}
	}
	else {
		for (int j = M - 1; j >= 0; j--) {
			if (table[height][j] != EM) {
				table[height][j] = EM;
				return;
			}
		}
	}
}

void NumberingCluster() {
	int cur_number = 1;
	in_the_air = 0;
	vector<vector<bool>> visit(N, vector<bool>(M, false));
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < M; j++) {
			if (table[i][j] != EM && visit[i][j]==false) {
				bool ground = false;
				queue<vector<int>> que;
				que.push(vector<int>{i, j, cur_number});
				visit[i][j] = true;
				table[i][j] = cur_number;
				while (!que.empty()) {
					int x = que.front()[0]; int y = que.front()[1]; int cur = que.front()[2]; que.pop();
					for (int d = 0; d < 4; d++) {
						int nx = x + dir[d][0]; int ny = y + dir[d][1];
						if ( nx >= N ) { ground = true;	continue; }
						if (nx < 0 || ny < 0 || ny >= M|| visit[nx][ny] || table[nx][ny] == EM) continue;
						visit[nx][ny] = true;
						table[nx][ny] = cur;
						que.push(vector<int>{nx, ny, cur});
					}
				}
				if (!ground) in_the_air = cur_number;
				cur_number++;
			}
		}
	}
}

void DropCluster() {
	bool stop = false;
	while (!stop) {
		for (int i = N - 1; i >= 0; i--) {
			for (int j = 0; j < M; j++) {
				if ((table[i][j] == in_the_air) && (i + 1 >= N || (table[i + 1][j] != EM && table[i + 1][j] != in_the_air))) stop = true;
			}
		}
		if (!stop) {
			for (int i = N - 1; i >= 0; i--) {
				for (int j = 0; j < M; j++) {
					if (table[i][j] == in_the_air) {
						table[i + 1][j] = table[i][j];
						table[i][j] = EM;

					} 
				}
			}
		}
	}
	
}

void PrintTable() {
	for (vector<int> row : table) {
		for (int i : row) {
			if (i != EM) cout << 'x';
			else cout << '.';
		} 
		cout << endl;
	}
}



int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	cin >> N >> M;
	table.assign(N, vector<int>(M, 0));
	string input;
	for (int i = 0; i < N; i++) {
		cin >> input;
		for (int j = 0; j < M; j++) {
			if (input[j] == 'x') table[i][j] = NEM;
			else table[i][j] = EM;
		}
	}
	cin >> K;
	sticks.assign(K,0);
	for (int i = 0; i < K; i++) cin >> sticks[i];
	num_of_sticks = K;
	//algorithm part
	
	
	for (int i = 0; i < K; i += 2) {
		
		
		Throw(true, reverseX(sticks[i])); //remove Mineral from left
		NumberingCluster();
		if (in_the_air != 0) DropCluster();
		//PrintTable();
		//cout << endl;
		
		if (i + 1 < K) { //from right
			Throw(false, reverseX(sticks[i + 1]));
			NumberingCluster();
			if (in_the_air != 0) DropCluster();
			//PrintTable();
			//cout << endl;
		}
		
	}
	PrintTable();
	return 0;

}

{% endraw %}
```

