---
layout: post
title: [Samsung SW - Moon is being filled up, Let's go!]
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}
	﻿#include<iostream>
	#include<vector>
	#include<unordered_map>
	#include<queue>
	#define min(a,b) a>b?b:a
	using namespace std;
	
	vector<vector<char>> table;
	pair<int, int> start_pos;
	vector<vector<vector<bool>>> visit;
	int N, M;
	int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };
	
	inline bool doWeHaveTheKey(char door, unordered_map<char, bool> has_key) {
		switch (door) {
		case 'A':
			if (has_key.find('a') != has_key.end()) return true;
			return false;
		case 'B':
			if (has_key.find('b') != has_key.end()) return true;
			return false;
		case 'C':
			if (has_key.find('c') != has_key.end()) return true;
			return false;
		case 'D':
			if (has_key.find('d') != has_key.end()) return true;
			return false;
		case 'E':
			if (has_key.find('e') != has_key.end()) return true;
			return false;
		case 'F':
			if (has_key.find('f') != has_key.end()) return true;
			return false;
	
		default:
			break;
		}
	}
	
	int BFS(int x, int y) {
		queue<pair<pair<int, int>, pair<int,int>>> que; //x,y, key,sum
		que.push(make_pair(make_pair(x, y), make_pair(0,0)));
		visit[x][y][0] = true;
	
		while (!que.empty()) {
			x = que.front().first.first; y = que.front().first.second;
			int key = que.front().second.first; int sum = que.front().second.second;
			que.pop();
			if (table[x][y] == '1') return sum;
			for (int i = 0; i < 4; i++) {
				int nx = x + dir[i][0]; int ny = y + dir[i][1];
				int new_key = key;
				if (nx >= 0 && ny >= 0 && nx < N && ny < M) {
					if (table[nx][ny] == '#') continue;
					if ('a' <= table[nx][ny] && table[nx][ny] <= 'f') new_key=(new_key | 1 << table[nx][ny] - 'a');
					if ('A' <= table[nx][ny] && table[nx][ny] <= 'F') {
						if (!(key & (1 << (table[nx][ny] - 'A')))) continue;
					}
					if (visit[nx][ny][new_key]) continue;
					que.push(make_pair(make_pair(nx, ny), make_pair(new_key, sum + 1)));
					visit[nx][ny][new_key] = true;
				}
			}
		}
		return -1;
	}
	
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
	
		//get input
		cin >> N >> M;
		string input;
		table.assign(N, vector<char>(M, 0));
		for (int i = 0; i < N; i++) {
			cin >> input;
			for (int j = 0; j < M; j++) {
				table[i][j] = input[j];
				if (input[j] == '0')  start_pos = make_pair(i, j);
			}
		}
	
		//algorithm part
		int answer = 0;	
		visit.assign(N, vector<vector<bool>>(M, vector<bool>(64, false)));
		visit[start_pos.first][start_pos.second][0] = true;
		answer = BFS(start_pos.first, start_pos.second);
		cout << answer;
		return 0;
	}
	
{% endraw %}
