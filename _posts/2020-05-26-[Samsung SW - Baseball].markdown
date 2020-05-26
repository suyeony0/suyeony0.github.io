---
layout: post
title: {% raw %}[Samsung SW - Baseball]{% endraw %}
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}
	﻿[173. [SAMSUNG - SW : Baseball]
	- What the heck? I spent 4 hours…
	- I first misunderstood the problem. since they gave me a rule that once I decide an order of players, I can’t change it even if inning is changed. but I thought I have to find optimum score we can get using find all the path we can reach. so I did brute force for every inning. 
	- because of that, I spend quite much time. 
	- second problem was scoring, I tried to make score function iteratively, but it didn’t work well. actually I don’t make sense why it was wrong until now!.
	- so I changed that part a hard code.
	- see the code.
	#include<iostream>
	#include<vector>
	#include<array>
	#include<algorithm>
	#include<map>
	#define max(a,b) a>b?a:b
	using namespace std;
	int N;
	vector<vector<int>> table;
	vector<int> order;
	int answer = 0;
	void printInning(vector<int>& inning) {
		for (int i : inning) cout << i << " ";
		cout << endl;
	}
	
	
	void Game() {
		int cur_player = 0;
		int res = 0;
		for (int i = 0; i < N; i++) {
			array<bool, 4> base = { false,false,false,false };
			int outs = 0;
			vector<int> temp;
			for (int j = 0; j < 8; j++) temp.emplace_back(table[i][order[j]]);
			temp.insert(next(temp.begin(), 3), table[i][0]);
			while (outs < 3) {
				int cur_hit = temp[cur_player];
				if (cur_hit == 0) {
					outs++;
					cur_player = (cur_player + 1) % 9;
					continue;
				}
				else if (cur_hit == 4) {
					for (int c = 3; c >= 1; c--) {
						if (base[c]) res++;
						base[c] = false;
					}
					res++;
				}
				else if (cur_hit == 1) {
					if (base[3]) {
						res++;
						base[3] = false;
					}
					if (base[2]) {
						base[3] = true; base[2] = false;
					}
					if (base[1]) {
						base[2] = true; base[1] = false;
					}
					base[1] = true;
				}
				else if (cur_hit == 2) {
					if (base[3]) {
						res++; base[3] = false;
					}
					if (base[2]) {
						res++; base[2] = false;
					}
					if (base[1]) {
						base[3] = true; base[1] = false;
					}
					base[2] = true;
				}
				else {
					if (base[3]) {
						res++; base[3] = false;
					}
					if (base[2]) {
						res++; base[2] = false;
					}
					if (base[1]) {
						res++; base[1] = false;
					}
					base[3] = true;
				}
				cur_player = (cur_player + 1) % 9;
			}
		}
		answer = max(answer, res);
	}
	
	
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
		//get input
		cin >> N;
		table.assign(N,vector<int>(9));
		
		int input;
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < 9; j++) {
				cin >> table[i][j];
			}
		}
		for (int i = 1; i < 9; i++) order.emplace_back(i);
		//algorithm part
		do {
			Game();
		} while (next_permutation(order.begin(), order.end()));
		cout << answer;
		return 0;
	}
	
{% endraw %}
