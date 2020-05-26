---
layout: post
title: [Samsung SW - Make Bridge 2]
data: 2020-05-26
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}
	﻿[182. [SAMSUNG SW – Making Bridge 2]
	- At first, I used brute force using permutation but it was hard to check all island was connected.
	- see the first code.
	#include<iostream>
	#include<vector>
	#include<unordered_map>
	#include<map>
	#include<set>
	#include<unordered_set>
	#define min(a,b) a>b? b:a
	using namespace std;
	
	int N, M;
	int number_of_island = 0;
	int needed_bridge = 0;
	vector<vector<int>> table;
	int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} }; //tx ty bx by size
	vector<vector<bool>> visit;
	unordered_map<int, vector<int>> map_of_land;
	map<pair<int, int>, int> bridge;
	int answer = 987654321;
	bool isConnected(set<set<int>>& temp_table) {
		unordered_set<int> res;
		for (set<set<int>>::iterator iter = temp_table.begin(); iter != temp_table.end(); iter++) {
			for (set<int>::iterator inner = iter->begin(); inner != iter->end(); inner++) {
				res.insert(*inner);
			}
		}
		if (res.size() == number_of_island) return true;
		return false;
	}
	
	
	void nameDistrict(int x, int y,int name) {
		table[x][y] = name;
		visit[x][y] = true;
		if (map_of_land[name][2] < x) map_of_land[name][2] = x;
		if (map_of_land[name][3] < y) map_of_land[name][3] = y;
		for (int i = 0; i < 4; i++) {
			int nx = x + dir[i][0]; int ny = y + dir[i][1];
			if (nx >= 0 && ny >= 0 && nx < N && ny < M && table[nx][ny] == 1 && visit[nx][ny]==false) {
				map_of_land[name][4]++;
				nameDistrict(nx, ny, name);
			}
		}
	}
	
	void findMinimumBridge() {
	
		//horizontal bridge
		for (int i = 0; i < N; i++) {
			int cur_land = 1;
			int sy = 0;
			for (int j = 0; j < M; j++) {
				if (table[i][j] != 0 && cur_land != table[i][j]) {
					if (j - sy - 1 >= 2 && cur_land!=1) {
						if (bridge.find(make_pair(cur_land, table[i][j])) == bridge.end()) {
							bridge[make_pair(cur_land, table[i][j])] = j - sy - 1;
						}
						else bridge[make_pair(cur_land, table[i][j])] = min(bridge[make_pair(cur_land, table[i][j])], j - sy + 1);
					}
					cur_land = table[i][j];
					sy = j;
				}
				else if (cur_land == table[i][j]) {
					sy = j;
				}
			}
		}
		//vertical bridge
		for (int j = 0; j < M; j++) {
			int cur_land = 1;
			int sx = 0;
			for (int i = 0; i < N; i++) {
				if (table[i][j] != 0 && cur_land != table[i][j]) {
					if (i - sx - 1 >= 2 && cur_land!=1) {
						if (bridge.find(make_pair(cur_land, table[i][j])) == bridge.end()) {
							bridge[make_pair(cur_land, table[i][j])] = i - sx - 1;
						}
						else bridge[make_pair(cur_land, table[i][j])] = min(bridge[make_pair(cur_land, table[i][j])], i - sx + 1);
					}
					cur_land = table[i][j];
					sx = i;
				}
				else if (cur_land == table[i][j]) sx = i;
			}
		}
	}
	
	void Permutation(set<set<int>> temp_table,int start,int sum,map<pair<int,int>,int>::iterator next_iter) {
		if (start >= needed_bridge) {
			if (isConnected(temp_table)) {
				answer = min(answer, sum);
				for (set<set<int>>::iterator iter = temp_table.begin(); iter != temp_table.end(); iter++) {
					for (set<int>::iterator inner = iter->begin(); inner != iter->end(); inner++) {
						cout << *inner << " ";
					}
					cout << ", ";
				}
				cout << endl << "answer : " << answer << endl;
			} 
			return;
		}
		for (map<pair<int, int>, int>::iterator iter = next_iter; iter != bridge.end(); iter++) {
			temp_table.insert(set<int>{iter->first.first,iter->first.second});
			Permutation(temp_table, start + 1, sum + iter->second, next(iter,1));
			temp_table.erase(temp_table.find(set<int>{iter->first.first, iter->first.second}));
		}
	}
	
	void printTable() {
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
		cin >> N >> M;
		table.assign(N, vector<int>(M));
		for (int i = 0; i < N; i++)
			for (int j = 0; j < M; j++) cin >> table[i][j];
		visit.assign(N, vector<bool>(M, false));
	
		//algorithm part
		// 1. counting island and make their name
		// the name start with 2
		
		int name = 2;
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < M; j++) {
				if (table[i][j] == 1) {
					map_of_land[name] = vector<int>{ i,j,i,j,1 };
					number_of_island++;
					nameDistrict(i, j, name++);
				}
			}
		}
		needed_bridge = number_of_island - 1;
		
		cout << endl;
		printTable();
		cout << endl;
		
	
		// 2. making bridge
		findMinimumBridge();
		
		for (map<pair<int, int>, int>::iterator iter = bridge.begin(); iter != bridge.end(); iter++) {
			cout << iter->first.first << " " << iter->first.second << ",";
		}
		cout << endl;
		
		Permutation(set<set<int>>{},0,0,bridge.begin());
		if (answer == 987654321) cout << -1;
		else cout << answer;
		return 0;
	
	}
	
	- so I changed it to Kurskal algorithm.
	- hu.. fucking Kruskal. there are lots of thing to think!
	- I spent 2 hours and half… In this stance, I couldn’t get through the SAMSUNG coding test…
	- I have to push myself up.
	- see the code.
	#include<iostream>
	#include<vector>
	#include<unordered_map>
	#include<map>
	#include<set>
	#include<unordered_set>
	#define min(a,b) a>b? b:a
	using namespace std;
	
	int N, M;
	int number_of_island = 0;
	int needed_bridge = 0;
	vector<vector<int>> table;
	int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} }; //tx ty bx by size
	vector<vector<bool>> visit;
	unordered_map<int, vector<int>> map_of_land;
	map<pair<int, int>, int> bridge;
	unordered_set<int> has_bridge;
	int answer = 987654321;
	
	
	void nameDistrict(int x, int y,int name) {
		table[x][y] = name;
		visit[x][y] = true;
		if (map_of_land[name][2] < x) map_of_land[name][2] = x;
		if (map_of_land[name][3] < y) map_of_land[name][3] = y;
		for (int i = 0; i < 4; i++) {
			int nx = x + dir[i][0]; int ny = y + dir[i][1];
			if (nx >= 0 && ny >= 0 && nx < N && ny < M && table[nx][ny] == 1 && visit[nx][ny]==false) {
				map_of_land[name][4]++;
				nameDistrict(nx, ny, name);
			}
		}
	}
	
	void findMinimumBridge() {
	
		//horizontal bridge
		for (int i = 0; i < N; i++) {
			int cur_land = 1;
			int sy = 0;
			for (int j = 0; j < M; j++) {
				if (table[i][j] != 0 && cur_land != table[i][j]) {
					if (j - sy - 1 >= 2 && cur_land!=1) {
						if (bridge.find(make_pair(cur_land, table[i][j])) == bridge.end()) {
							bridge[make_pair(cur_land, table[i][j])] = j - sy - 1;
						}
						else bridge[make_pair(cur_land, table[i][j])] = min(bridge[make_pair(cur_land, table[i][j])], j - sy - 1);
					}
					cur_land = table[i][j];
					sy = j;
				}
				else if (cur_land == table[i][j]) {
					sy = j;
				}
			}
		}
		//vertical bridge
		for (int j = 0; j < M; j++) {
			int cur_land = 1;
			int sx = 0;
			for (int i = 0; i < N; i++) {
				if (table[i][j] != 0 && cur_land != table[i][j]) {
					if (i - sx - 1 >= 2 && cur_land!=1) {
						if (bridge.find(make_pair(cur_land, table[i][j])) == bridge.end()) {
							bridge[make_pair(cur_land, table[i][j])] = i - sx - 1;
						}
						else bridge[make_pair(cur_land, table[i][j])] = min(bridge[make_pair(cur_land, table[i][j])], i - sx - 1);
					}
					cur_land = table[i][j];
					sx = i;
				}
				else if (cur_land == table[i][j]) sx = i;
			}
		}
	}
	
	int Kruskal(int sum) {
		int cur_size = 1;
		while (cur_size<needed_bridge) {
			int temp_x; int temp_y; int temp_dis = 987654321;
			for (map<pair<int, int>, int>::iterator iter = bridge.begin(); iter != bridge.end(); iter++) {
				if ((has_bridge.find(iter->first.first) != has_bridge.end() || has_bridge.find(iter->first.second) != has_bridge.end()) &&
					!(has_bridge.find(iter->first.first) != has_bridge.end() && has_bridge.find(iter->first.second) != has_bridge.end())) {
					if (iter->second < temp_dis) {
						temp_x = iter->first.first; temp_y = iter->first.second;  temp_dis = iter->second;
					}
				}
			}
			if (temp_dis == 987654321) return -1;
			bridge.erase(bridge.find(make_pair(temp_x, temp_y)));
			//cout << "x : " << temp_x << " y : " << temp_y << " dis : " << temp_dis << endl;
			has_bridge.insert(temp_x); has_bridge.insert(temp_y);
			cur_size++;
			sum += temp_dis;
		}
		/*for (unordered_set<int>::iterator iter = has_bridge.begin(); iter != has_bridge.end(); iter++)
			cout << *iter << " ";
		cout << endl;*/
	
		if (has_bridge.size() != number_of_island) return -1;
		return sum;
	}
	
	
	
	void printTable() {
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
		cin >> N >> M;
		table.assign(N, vector<int>(M));
		for (int i = 0; i < N; i++)
			for (int j = 0; j < M; j++) cin >> table[i][j];
		visit.assign(N, vector<bool>(M, false));
	
		//algorithm part
		// 1. counting island and make their name
		// the name start with 2
		
		int name = 2;
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < M; j++) {
				if (table[i][j] == 1) {
					map_of_land[name] = vector<int>{ i,j,i,j,1 };
					number_of_island++;
					nameDistrict(i, j, name++);
				}
			}
		}
		needed_bridge = number_of_island - 1;
		
		//cout << endl;
		//printTable();
		//cout << endl;
		
	
		// 2. making bridge
		findMinimumBridge();
		
		/*for (map<pair<int, int>, int>::iterator iter = bridge.begin(); iter != bridge.end(); iter++) {
			cout << iter->first.first << " " << iter->first.second << ",";
		}
		cout << endl;*/
		int temp_dis = 987654321;
		int temp_x; int temp_y;
		if (bridge.empty()) {
			cout << -1;
			return 0;
		} 
	
		for (map<pair<int, int>, int>::iterator iter = bridge.begin(); iter != bridge.end(); iter++) {
			if (iter->second < temp_dis) {
				temp_dis = iter->second;
				temp_x = iter->first.first; temp_y = iter->first.second;
			}
		}
		bridge.erase(bridge.find(make_pair(temp_x, temp_y)));
		has_bridge.insert(temp_x); has_bridge.insert(temp_y);
		cout<<Kruskal(temp_dis);
		return 0;
	
	}
	
	
{% endraw %}
