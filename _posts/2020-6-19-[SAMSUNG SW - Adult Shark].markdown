---
layout: post
title: [SAMSUNG SW - Adult Shark]
date: 2020-6-19
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

﻿[222. SAMSUNG SW – Adult Shark]
- It was a same problem with what I’ve solved at SAMSUNG Codingtest 2020.
- it was a simulation problem with direction priorities.
- First, I made priority 3D array as a look up table.
- Second, Finding an adjacent empty shell of a shark.
- Third, If so, push the shark to temprorary vector. if not, finding an adjacent shell that has the shark’s pheromone.
- In terms of the temporary vector, if more than 2 shark have been located a certain shell, remove greater number of shark.
- Fourth, Reduce pheromone.
- Actually, I spent 1 hours and 6 minutes at the real test. Now, 49 minutes and 5 seconds.
- But I think the logic is slightly different with what I’ve done at the real test.
- so I’m quite nervous now.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>

using namespace std;

int N, M, K;
vector<vector<pair<int,int>>> table; //shark_number , remain time of pheromone
vector<vector<vector<int>>> prior; // shark_number -> current_direction -> next_direction's priority
vector<vector<int>> shark; // x, y, direction
int dir[4][2] = { {-1,0},{1,0},{0,-1},{0,1} };
vector<bool> visit;

void SharkMove() {
	vector<vector<int>> stk;
	for (int i = 0; i < M;i++) {
		if (visit[i] == true) continue;
		int x = shark[i][0]; int y = shark[i][1]; int cur_d = shark[i][2];
		bool flag = false;
		//finding empty shell
		for (int d = 0; d < 4; d++) {
			int nx = x + dir[prior[i][cur_d][d]][0]; int ny = y + dir[prior[i][cur_d][d]][1];
			if (nx >= 0 && ny >= 0 && nx < N && ny < N && table[nx][ny].first == 0) { //is it empty shell?
				stk.emplace_back(vector<int>{nx, ny, i+1}); //x ,y, shark_number
				flag = true;
				shark[i][0] = nx; shark[i][1] = ny; shark[i][2] = prior[i][cur_d][d];
				break;
			}
		}
		//move to their own shell
		if (flag) continue;
		for (int d = 0; d < 4; d++) {
			int nx = x + dir[prior[i][cur_d][d]][0]; int ny = y + dir[prior[i][cur_d][d]][1];
			if (nx >= 0 && ny >= 0 && nx < N && ny < N && table[nx][ny].first == i+1) { // is it my shell?
				shark[i][0] = nx; shark[i][1] = ny; shark[i][2] = prior[i][cur_d][d];
				table[nx][ny].second = K; //reset pheromone
				break;
			}
		}
	}

	//determining empty shell
	for (vector<int> row : stk) {
		int x = row[0]; int y = row[1]; int number = row[2];
		if (table[x][y].first == 0) {
			table[x][y].first = number;
			table[x][y].second = K; //set phoeromon
		}
		else {
			if (table[x][y].first < number) {
				visit[number - 1] = true;
				continue;
			} 
			visit[table[x][y].first - 1] = true;
			table[x][y].first = number;
			table[x][y].second = K; //set phoeromon
		}
	}
}

void Remove() {
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < N; j++) {
			if (table[i][j].first != 0 && table[i][j].second == 0) table[i][j].first = 0;
			else if (table[i][j].first != 0) {
				table[i][j].second -= 1;
			}
			
		}
	}
}

bool isOnlyOneAlive() {
	if (visit[0] == false) {
		for (int i = 1; i < M; i++) {
			if (visit[i] == false) return false;
		}
		return true;
	}
	return false;
}

void PrintTable() {
	cout << endl;
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < N; j++) {
			cout << table[i][j].second << " ";
		}
		cout << endl;
	}
	cout << endl;
}

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	cin >> N >> M >> K;
	table.assign(N, vector<pair<int,int>>(N,pair<int,int>(0,0)));
	shark.assign(M, vector<int>(3,0));
	visit.assign(M, false);
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < N; j++) {
			cin >> table[i][j].first;
			if (table[i][j].first != 0) {
				shark[table[i][j].first-1][0] = i;
				shark[table[i][j].first-1][1] = j;
				table[i][j].second = K; //Pheromone time.
			}
		}
	}
	for (int i = 0; i < M; i++) {
		cin >> shark[i][2];
		shark[i][2] -= 1;
	}
	prior.assign(M, vector<vector<int>>(4, vector<int>(4, 0)));
	int input;
	for (int i = 0; i < M; i++) {
		for (int j = 0; j < 4; j++) {
			for (int k = 0; k < 4; k++) {
				cin >> input;
				prior[i][j][k]=input-1; // dir starts at 0.

			}
		}
	}

	//algorithm part
	int answer = 0;
	while (!isOnlyOneAlive() && answer<=1000) {
		Remove();
		SharkMove();
		answer += 1;
	}
	if (answer >= 1001) answer = -1;
	cout << answer;
	return 0;

}

{% endraw %}
```

