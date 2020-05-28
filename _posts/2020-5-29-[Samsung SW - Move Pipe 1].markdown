---
layout: post
title: [Samsung SW - Move Pipe 1]
date: 2020-5-29
description: txt to markdown
thumbnail: food2.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}

	﻿[170. [SAMSUNG - SW : Move Pipe 1]
	- it was a simulation problem. given possible directions to move, I had to move the pipe to (N,N).
	- I used DFS and memorization using visit vector.
	- see the code. 
	#include<iostream>
	#include<vector>
	using namespace std;
	
	int N;
	vector<vector<int>> table(17,vector<int>(17,0));
	vector<vector<vector<int>>> visit(17,vector<vector<int>>(17, vector<int>(3,-1)));
	/*
	void printTable(int lx,int ly,int rx,int ry) {
		vector<vector<int>> temp = table;
		temp[lx][ly] = 2; temp[rx][ry] = 2;
		for (vector<int> row : temp) {
			for (int i : row) cout << i << " ";
			cout << endl;
		}
		cout << endl;
	}
	*/
	
	int MovePipe(int lx, int ly, int rx, int ry,bool hori, bool verti) {
		int answer = 0;
		if (rx==N-1 && ry==N-1) {
			return 1;
		}
		int temp;
		
		if (hori) {
			if (visit[lx][ly][0] == -1) {
				//to horizon
				visit[lx][ly][0] = 0;
				if (ry+1<N && table[rx][ry + 1] != 1) {
					temp = MovePipe(lx, ly + 1, rx, ry + 1, true, false);
					visit[lx][ly][0] += temp;
					answer += temp;
				}
				//to diagonal
				if (rx+1<N && ry+1< N&&table[rx][ry + 1] != 1 && table[rx + 1][ry] != 1 && table[rx + 1][ry + 1] != 1) {
					temp = MovePipe(lx, ly + 1, rx + 1, ry + 1, false, false);
					visit[lx][ly][0] += temp;
					answer += temp;
				}
			}
			else {
				answer += visit[lx][ly][0];
			} 
	
		}
		else if (verti) {
			if (visit[lx][ly][1] == -1) {
				visit[lx][ly][1] = 0;
				//to vertical
				if (rx+1<N && table[rx + 1][ry] != 1) {
					temp = MovePipe(lx + 1, ly, rx + 1, ry, false, true);
					visit[lx][ly][1] += temp;
					answer += temp;
				}
				//to diagonal
				if (rx+1<N && ry+1< N &&table[rx + 1][ry] != 1 && table[rx + 1][ry + 1] != 1 && table[rx][ry + 1] != 1) {
					temp = MovePipe(lx + 1, ly, rx + 1, ry + 1, false, false);
					visit[lx][ly][1] += temp;
					answer += temp;
				}
			}
			else {
				answer += visit[lx][ly][1];
			} 
		
		}
		else {
			if (visit[lx][ly][2] == -1) {
				visit[lx][ly][2] = 0;
				//to horizon
				if (ry+1<N &&table[rx][ry + 1] != 1) {
					temp = MovePipe(lx + 1, ly + 1, rx, ry + 1, true, false);
					visit[lx][ly][2] += temp;
					answer += temp;
				}
				//to diagonal
				if (rx+1<N && ry+1<N && table[rx + 1][ry] != 1 && table[rx + 1][ry + 1] != 1 && table[rx][ry + 1] != 1) {
					temp = MovePipe(lx + 1, ly + 1, rx + 1, ry + 1, false, false);
					visit[lx][ly][2] += temp;
					answer += temp;
				}
				//to vertical
				if (rx+1<N && table[rx + 1][ry] != 1) {
					temp = MovePipe(lx + 1, ly + 1, rx + 1, ry, false, true);
					visit[lx][ly][2] += temp;
					answer+=temp;
				}
			}
			else {
				answer += visit[lx][ly][2];
			}
		
		}
		return answer;
	}
	
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
		//get input
		cin >> N;
		for (int i = 0; i < N; i++)
			for (int j = 0; j < N; j++) cin >> table[i][j];
		bool hori, verti; //if both are false, then dir is diagonal.
		//algorithm part
		if (table[N - 1][N - 1] == 1) cout << 0;
		else cout<<MovePipe(0,0,0,1,true, false);
	
		return 0;
	}
	
{% endhighlight %}
