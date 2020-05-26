---
layout: post
title: [Samsung SW - Castle Defence]
data: 2020-05-26
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}
	﻿[171. [SAMSUNG - SW : Castle Defence]
	- it was also a simulation problem.
	- there was a limitation of way to kill an enemy by an archer. because of that, it was quite confused.
	- the limitation was that an archer can kill a leftmost enemy with the shortest distance from oneself. the leftmost was the key of this problem.
	- without above issue, there was nothing to consider hard.
	- I used DFS to choose archers’ position
	- see the code.
	#include<iostream>
	#include<vector>
	#include<set>
	#define MAX_VALUE 987654321
	#define max(a,b) a>b?a:b
	#define min(a,b) a>b?b:a
	using namespace std;
	
	int N, M, D;
	vector<vector<int>> table;
	vector<int> archers;
	int answer = 0;
	int max_enemy;
	bool isEmpty(vector<vector<int>>& temp) {
		for (vector<int> row : temp)
			for (int i : row) if (i == 1) return false;
		return true;
	}
	
	void printTable(vector<vector<int>>& temp) {
		for (vector<int> row : temp) {
			for (int i : row) cout << i << " ";
			cout << endl;
		}
		cout << endl;
	}
	
	void moveEnemy(vector<vector<int>>& temp) {
		//Enemies come down to the castles.
		for (int i = N - 1; i >= 1; i--) {
			for (int j = 0; j < M; j++) {
				temp[i][j] = temp[i - 1][j];
			}
		}
		for (int j = 0; j < M; j++) temp[0][j] = 0;
	
	}
	
	int PlayGame() {
		vector<vector<int>> temp = table;
		int archer_x = N;
		int res = 0;
		while (!isEmpty(temp)) {
			vector<pair<int, int>> temp_remove(3, make_pair(MAX_VALUE, MAX_VALUE));
			set<pair<int, int>> remove;
			int fst_dis = MAX_VALUE; int sec_dis = MAX_VALUE; int thr_dis = MAX_VALUE;
			for (int i = N - 1; i >= 0 && (abs(i-archer_x)<=D); i--) {
				for (int j = 0; j < M; j++) {
					if (temp[i][j] == 1) {
						int a = (abs(i - archer_x) + abs(j - archers[0])); 
						int b = (abs(i - archer_x) + abs(j - archers[1])); 
						int c = (abs(i - archer_x) + abs(j - archers[2]));
						//cout<<"f,s,t : " << fst_dis << "," << sec_dis << "," << thr_dis << endl;
						//cout << "a,b,c :" << a << "," << b << "," << c << endl;
						if ( a <= D && fst_dis>=a) {
							if (fst_dis == a) {
								if (temp_remove[0].second > j) temp_remove[0] = make_pair(i, j);
							}
							else {
								fst_dis = a;
								temp_remove[0] = make_pair(i, j);
							}
						}
						if ( b <= D && sec_dis >= b) {
							if (sec_dis == b) {
								if (temp_remove[1].second > j) temp_remove[1] = make_pair(i, j);
							}
							else {
								sec_dis = b;
								temp_remove[1] = make_pair(i, j);
							}
						}
						if ( c <= D && thr_dis >= c) {
							if (thr_dis == c) {
								if (temp_remove[2].second > j) temp_remove[2] = make_pair(i, j);
							}
							else {
								thr_dis = c;
								temp_remove[2] = make_pair(i, j);
							}
						}
					}
				}
			}
			for (pair<int, int> temp_re : temp_remove) if(temp_re.first!=MAX_VALUE) remove.insert(temp_re);
			res += remove.size();
			//cout << "before killing" << endl;
			//printTable(temp);
			for (pair<int, int> removed_enemy : remove) {
				temp[removed_enemy.first][removed_enemy.second] = 0;
			}
			//cout << "after killing" << endl;
			//printTable(temp);
			moveEnemy(temp);
		}
		return res;
	}
	
	void DFS(int start, int count) {
		if (count == 3) {
			answer=max(answer,PlayGame());
			return;
		}
		// if we got all the enemy by an archers' position, we don't need to do further.
		for (int i = start; i < M && max_enemy!=answer; i++) {
			archers.emplace_back(i);
			DFS(i + 1, count + 1);
			archers.pop_back();
		}
	}
	
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
		//get input
		cin >> N>> M>> D;	
		table.assign(N, vector<int>(M));
		int input;
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < M; j++) {
				cin >> input;
				table[i][j] = input;
				if (input == 1) max_enemy++;
			}
		}
		//algorithm part
		if (isEmpty(table)) cout << 0;
		else {
			DFS(0, 0);
			cout << answer;
		}
		return 0;
	}
	
	
	
{% endraw %}
