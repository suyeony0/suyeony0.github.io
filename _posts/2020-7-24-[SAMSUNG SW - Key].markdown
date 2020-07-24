---
layout: post
title: [SAMSUNG SW - Key]
date: 2020-7-24
description: txt to markdown
thumbnail: breakfast-orange-lemon-oranges-large.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

﻿[246. SAMSUNG SW – Key]
- WOW, it was a quite difficult traveling problem. Since I had to renew keys I had currently.
- I used BFS and if I got a new key, I push the key to key-table(map hash table).
- After BFS, if key-table’s size was increased, I re-tried the BFS with new keys.
- the code was quite dirty, because I made it just adding anything that I needed at the time.
- Morever, there was hidden edge conditions. To catch those things, I spent much time.
- I spent 49 minutes and 17 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<map>
#include<queue>
#define max(a,b) a>b ? a:b
using namespace std;


const int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };
int N, M;
vector<vector<char>> table;
map<char, bool> keys;
vector<pair<int, int>> possible_entrance;
int answer = 0;
vector<vector<bool>> visit_key;

void BFS(int sx, int sy, vector<pair<char, pair<int, int>>> given_key) {
	queue<vector<int>> que;
	vector<vector<bool>> visit(N, vector<bool>(M, false));
	que.push(vector<int>{sx, sy});
	visit[sx][sy] = true;
	vector<pair<char, pair<int, int>>> new_keys = given_key;
	int n_key_size = new_keys.size();
	int m_cnt=0;
	while (!que.empty()) {
		int x = que.front()[0]; int y = que.front()[1];que.pop();

		if (table[x][y] == '$' && visit_key[x][y] == false) {
			visit_key[x][y] = true;
			answer += 1;
		} 

		for (int d = 0; d < 4; d++) {
			int nx = x + dir[d][0]; int ny = y + dir[d][1];
			if (nx < 0 || ny < 0 || nx >= N || ny >= M || table[nx][ny] == '*' || visit[nx][ny] == true) continue;
			if (('A' <= table[nx][ny] && table[nx][ny] <= 'Z') && keys.find(tolower(table[nx][ny])) == keys.end()) continue;
			
			else if (('A' <= table[nx][ny] && table[nx][ny] <= 'Z') && keys.find(tolower(table[nx][ny])) != keys.end()) {
				que.push(vector<int>{nx, ny});
				visit[nx][ny] = true;
			}
			else if (('a' <= table[nx][ny] && table[nx][ny] <= 'z')) {
				if (keys.find(table[nx][ny]) == keys.end()) {
					new_keys.emplace_back(make_pair(table[nx][ny], make_pair(nx, ny)));
					keys[tolower(table[nx][ny])] = true;
				}
				que.push(vector<int>{nx, ny});
				visit[nx][ny] = true;
			}
			else {
				que.push(vector<int>{nx, ny});
				visit[nx][ny] = true;
			}

		}
	}

	if (n_key_size != new_keys.size()) BFS(new_keys[n_key_size].second.first, new_keys[n_key_size].second.second, new_keys);
		
		
	
	return;
}

vector<pair<int, int>> Entrance() {
	vector<pair<int, int>> possible_entrance;
	for (int i = 0; i < N; i++) {
		if (table[i][0] == '.' || table[i][0] == '$' || keys.find(tolower(table[i][0])) != keys.end()) possible_entrance.emplace_back(make_pair(i, 0));

		if (table[i][M - 1] == '.' || table[i][M - 1] == '$' || keys.find(tolower(table[i][M - 1])) != keys.end())
			possible_entrance.emplace_back(make_pair(i, M - 1));
	}
	for (int j = 0; j < M; j++) {
		if (table[0][j] == '.' || table[0][j] == '$' || keys.find(tolower(table[0][j])) != keys.end()) possible_entrance.emplace_back(make_pair(0, j));

		if (table[N - 1][j] == '.' || table[N - 1][j] == '$' || keys.find(tolower(table[N - 1][j])) != keys.end()) possible_entrance.emplace_back(make_pair(N - 1, j));

	}
	return possible_entrance;
}

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);
	int T;
	cin >> T;

	for (int t = 0; t < T; t++) {
		answer = 0;
		keys.clear();
		possible_entrance.clear();
		//get input
		cin >> N >> M;
		table.assign(N, vector<char>(M, 0));
		visit_key.assign(N, vector<bool>(M, false));
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < M; j++) {
				cin >> table[i][j];
			}
		}
		string input_key;
		cin >> input_key;
		if(input_key[0]!='0') for (int i = 0; i < input_key.size(); i++) keys[input_key[i]] = true;

		possible_entrance = Entrance();

		int n_key_size = keys.size();

		//algorithm part
		do {
			n_key_size = keys.size();
			for (int ent = 0; ent < possible_entrance.size(); ent++) 
				BFS(possible_entrance[ent].first, possible_entrance[ent].second, vector<pair<char, pair<int, int>>>{});
			possible_entrance = Entrance();
		} while (n_key_size != keys.size());
		cout << answer << endl;
	}
	return 0;
}

{% endraw %}
```

