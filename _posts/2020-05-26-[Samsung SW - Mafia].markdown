---
layout: post
title: {% raw %}[Samsung SW - Mafia]{% endraw %}
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}
	﻿[189. [SAMSUNG SW – Mafia]
	- I felt that I have to read Question more deeply. since I’ve missed a restriction that if rest number of people is even, mafia turn. Otherwise, citizen’s turn.
	- because of that, I spent so much time.
	- I felt one more thing that it’s more effience that just implement max score rather than using sort algorithm in the algorithm header.
	- see the code.
	#include<iostream>
	#include<vector>
	#define max(a,b) a>b?a:b
	#define min(a,b) a>b?b:a
	using namespace std;
	
	//bool end_game = false;
	int N;
	int mafia_pos;
	vector<pair<int, bool>> people; //score and is_dead?
	vector<vector<int>> R;
	int answer = 0;
	
	void DFS(int rest, int night) {
		//if (end_game) return;
		if (people[mafia_pos].second == true || rest <= 1) {
			answer = max(answer, night);
			//if (rest == 1 && people[mafia_pos].second == false) end_game = true;
			return;
		}
		if (rest % 2 == 0) { //mafia time
			for (int i = 0; i < N; i++) {
				if (people[i].second == true || i == mafia_pos) continue;
				people[i].second = true;
				for (int j = 0; j < N; j++) {
					if (people[j].second==true) continue;
					people[j].first += R[i][j];
				}
				DFS(rest - 1, night + 1);
				//if (end_game) return;
				for (int j = 0; j < N; j++) {
					if (people[j].second == true) continue;
					people[j].first -= R[i][j];
				}
				people[i].second = false;
			}
		}
		else { //citizen time
			int max_score = 0;
			int min_index = 987654321;
			for (int i = 0; i < N; i++) {
				if (people[i].second == true) continue;
				if (people[i].first > max_score) {
					max_score = people[i].first;
					min_index = i;
				}
				else if (people[i].first == max_score) {
					min_index = min(min_index, i);
				}
			}
			people[min_index].second = true;
			DFS(rest - 1, night);
			//if (end_game) return;
			people[min_index].second = false;
		}
	}
	
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
		//get input
		cin >> N;
		people.assign(N,pair<int,int>());
		R.assign(N, vector<int>(N, 0));
		int temp_input;
		for (int i = 0; i < N; i++) {
			cin >> temp_input;
			people[i] = make_pair(temp_input, false);
		} 
		for (int i = 0; i < N; i++)
			for (int j = 0; j < N; j++) cin >> R[i][j];
		cin >> mafia_pos;
		
		//algoirithm part
		DFS(N,0);
		cout << answer;
		return 0;
	}
	
{% endraw %}
