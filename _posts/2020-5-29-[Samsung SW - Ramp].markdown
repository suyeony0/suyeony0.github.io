---
layout: post
title: [Samsung SW - Ramp]
date: 2020-5-29
description: txt to markdown
thumbnail: work1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

{% highlight c++ %}

{% raw %}

	﻿[112. [BACKJOON – SAMSUNG SW : Ramp]]
	- there was lots of error in this problem. I mean the errors the problem has.
	- this problem didn’t describe exactly. Even having wrong information.
	- I made an algorithm including all the possible case but I didn’t need to actually.
	- However, i didn’t want to spent much time to revise for this problem. I just submited my answer and got marked.
	- see the code.
	#include<iostream>
	#include<fstream>
	#include<vector>
	#include<algorithm>
	using namespace std;
	
	pair<vector<vector<int>>,int> makeTable(){
		ifstream in("C:\\Users\\gjsgu\\Desktop\\Algorithm\\test_case\\test_case_for_ramp.txt");
		int N; int L;
		if (in.is_open()) {
			cout << "file is opened." << endl;
			in >> N; in >> L;
		}
		vector<vector<int>> table(N, vector<int>(N, 0));
		for (int i = 0; i < N; i++) 
			for (int j = 0; j < N; j++)
				in >> table[i][j];
		return make_pair(table,L);
	}
	pair<vector<vector<int>>, int> makeTable2() {
		int N; int L;
		cin >> N; cin >> L;
		vector<vector<int>> table(N, vector<int>(N, 0));
		for (int i = 0; i < N; i++)
			for (int j = 0; j < N; j++)
				cin >> table[i][j];
		return make_pair(table, L);
	}
	
	// we have to consider row first and column first search.
	
	pair<vector<vector<int>>,int> rowSearch(vector<vector<int>> table,int L, vector<vector<int>> visit,int count) {
		int n = table.size();
		vector<int> path;
		for (int i = 0; i < n; i++) {
			int cur_height = table[i][0];
			int length = 1;
			bool flag = false;
			for (int j = 1; j < n; j++) {
				if (table[i][j] == cur_height + 1) { // higher
					if (length >= L) {
						for (int s = 0; s < L; s++) if (visit[i][j - 1 - s] == 1) { flag = true; break; } 
						if (flag) break;
						if (j == n - 1) { count++; path.push_back(i); break; }
						for (int s = 0; s < L; s++) visit[i][j - 1 - s] = 1; 
						length = 1; cur_height++;
						continue;
					}
					else break;
				}
				else if (table[i][j] == cur_height) { // same height
					if (j == n - 1) { count++; path.push_back(i); break; }
					length++;
					continue;
				}
				else if (table[i][j]==cur_height-1) { // lower
					if (n - j < L) break;
					for (int s = j; s < j + L; s++)  if ( visit[i][s] == 1 || table[i][s]!=cur_height-1) { flag = true; break; }
					if (flag) break;
					for (int s = j; s < j + L; s++) visit[i][s] = 1;
					j += L - 1;
					if (j == n - 1) { count++; path.push_back(i); break; }
					length = L;
					cur_height--;
	
				}
				else break;
			}
		}
	
		return make_pair(visit, count);
	}
	
	pair<vector<vector<int>>, int> colSearch(vector<vector<int>> table,int L,vector<vector<int>> visit,int count) {
		int n = table.size();
		vector<int> path;
		for (int j = 0; j < n; j++) {
			int cur_height = table[0][j];
			int length = 1;
			bool flag = false;
			for (int i = 1; i < n; i++) {
				if (table[i][j] == cur_height + 1) { // higher
					if (length >= L) {
						for (int s = 0; s < L; s++) if (visit[i - 1 - s][j] == 1) { flag = true; break; }
						if (flag) break;
						if (i == n - 1) { count++; path.push_back(j); break; }
						for (int s = 0; s < L; s++) visit[i - 1 - s][j] = 1;
						length = 1; cur_height++;
						continue;
					}
					else break;
				}
				else if (table[i][j] == cur_height) { // same height
					if (i == n - 1) { count++; path.push_back(j); break; }
					length++;
					continue;
				}
				else if (table[i][j] == cur_height - 1) { // lower
					if (n - i < L) break;
					for (int s = i; s < i + L; s++)  if (visit[s][j] == 1|| table[s][j] != cur_height - 1) { flag = true; break; }
					if (flag) break;
					for (int s = i; s < i + L; s++) visit[s][j] = 1;
					i += L - 1;
					if (i == n - 1) { count++; path.push_back(j); break; }
					length = L;
					cur_height--;
				}
				else break;
			}
		}
		
		return make_pair(visit, count);
	}
	
	
	int main() {
		//pair<vector<vector<int>>, int> input = makeTable();
		pair<vector<vector<int>>, int> input = makeTable2();
		vector<vector<int>> visit(input.first.size(), vector<int>(input.first.size(), 0));
		pair < vector<vector<int>>, int> row_first = rowSearch(input.first, input.second, visit, 0);
		row_first = colSearch(input.first, input.second, visit, row_first.second);
		cout<<row_first.second;
		return 0;
	}
	
	
	
{% endraw %}
{% endhighlight %}

