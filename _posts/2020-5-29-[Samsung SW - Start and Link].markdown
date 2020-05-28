---
layout: post
title: [Samsung SW - Start and Link]
date: 2020-5-29
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% highlight c++ %}
```cpp
	﻿
	[111. [BACKJOON – SAMSUNG SW : Start and Link]]
	- at first, I solved using next_permuation but time limit exceeded occurred.
	- so I changed the algorithm to DFS, but it was same.
	- code below is DFS.
	#include<iostream>
	#include<fstream>
	#include<climits>
	#include<vector>
	#include<algorithm>
	#include<unordered_map>
	using namespace std;
	
	unordered_map<string, int> visit;
	
	vector<vector<int>> makeTable() {
		ifstream in("C:\\Users\\gjsgu\\Desktop\\Algorithm\\test_case\\test_case_for_start_and_link.txt");
		int N;
		if (in.is_open()) {
			cout << "file is opened." << endl;
			in >> N;
		}
		vector<vector<int>> table(N, vector<int>(N, 0));
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < N; j++) {
				in >> table[i][j];
			}
		}
		return table;
	}
	
	vector<vector<int>> makeTable2() {
		int N;
		cin >> N;
		
		vector<vector<int>> table(N, vector<int>(N, 0));
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < N; j++) {
				cin >> table[i][j];
			}
		}
		return table;
	}
	void printTeam(vector<int>& team) {
		for (int i : team)
			cout << i << " ";
		cout << endl;
	}
	
	
	int statDifference(vector<vector<int>>& table,vector<int>& red,vector<int>& blue,int middle,string reds) {
		int red_sum = 0; int blue_sum = 0;
		string blues;
		for (int i : blue)
			blues += i+ '0';
		if (visit[blues]) {
			return INT_MAX;
		} 
		visit[reds] = 1;
		for (int i = 0; i < middle; i++) {
			for (int j = 0; j < middle; j++) {
				red_sum += table[red[i]-1][red[j]-1];
				blue_sum += table[blue[i]-1][blue[j]-1];
			}
		}
		
		return abs(red_sum - blue_sum);
	}
	
	int DFS(vector<vector<int>>& table,vector<int> red, vector<int> blue,int middle,string reds) {
		if (red.size() == middle) return statDifference(table,red,blue,middle,reds);
		int minimum = INT_MAX;
		for (int i = 0; i < blue.size(); i++) {
			vector<int> red_temp = red;
			vector<int> blue_temp = blue;
			red_temp.push_back(blue[i]);
			reds += blue[i] + '0';
			blue_temp.erase(next(blue_temp.begin(), i));
			minimum=min(minimum,DFS(table, red_temp, blue_temp, middle,reds));
		}
		return minimum;
	}
	// 1 2 3 4 5 6
	//1 2 4
	// 3 5 6
	
	int makeTeam(vector<vector<int>>& table) {
		vector<int> member;
		int minimum = INT_MAX;
		int middle = table.size() / 2;
		
		for (int i = 0; i < table.size(); i++)
			member.push_back(i + 1);
		return DFS(table, {}, member, middle,"");
	}
	
	int main() {
		//vector<vector<int>> table = makeTable();
		vector<vector<int>> table = makeTable2();
		cout<<makeTeam(table);
		return 0;
	}
	
	- I should’ve revised the code.
	- At first, we don’t need to check all the possible red team.
	- Since if red team has player 1,2, and 3, then blue must have 4,5, and 6.
	- And instead of moving a player from one to another, just select players to be red team.
	- see the code.
	#include<iostream>
	#include<fstream>
	#include<climits>
	#include<vector>
	#include<algorithm>
	#include<unordered_map>
	using namespace std;
	
	vector<vector<int>> makeTable() {
		ifstream in("C:\\Users\\gjsgu\\Desktop\\Algorithm\\test_case\\test_case_for_start_and_link.txt");
		int N;
		if (in.is_open()) {
			cout << "file is opened." << endl;
			in >> N;
		}
		vector<vector<int>> table(N, vector<int>(N, 0));
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < N; j++) {
				in >> table[i][j];
			}
		}
		return table;
	}
	
	vector<vector<int>> makeTable2() {
		int N;
		cin >> N;
	
		vector<vector<int>> table(N, vector<int>(N, 0));
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < N; j++) {
				cin >> table[i][j];
			}
		}
		return table;
	}
	void printTeam(vector<int>& team) {
		for (int i : team)
			cout << i << " ";
		cout << endl;
	}
	
	
	int statDifference(vector<vector<int>>& table,vector<bool>& visit, int middle) {
		vector<int> red; vector<int> blue;
		//In here, make team
		for (int i = 0; i < visit.size(); i++) {
			visit[i] ? red.push_back(i) : blue.push_back(i);
		}
		int red_sum = 0; int blue_sum = 0;
		for (int i = 0; i < red.size(); i++) {
			for (int j = 0; j < red.size(); j++) {
				red_sum += table[red[i]][red[j]];
				blue_sum += table[blue[i]][blue[j]];
			}
		}
		return abs(red_sum - blue_sum);
	}
	int DFS(vector<vector<int>>& table,vector<bool> visit,int count,int middle,int next) {
		if (count == middle) return statDifference(table,visit,middle);
		int minimum = INT_MAX;
		// instead of making red and blue vectors and moving player one to another, just select players to be red team.
		for (int i = next; i < visit.size(); i++) {
			visit[i] = true;
			minimum=min(minimum,DFS(table, visit, count + 1, middle,i+1));
			visit[i] = false;
		}
		return minimum;
	}
	
	int makeTeam(vector<vector<int>>& table) {
		vector<int> member;
		vector<bool> visit(table.size(),false);
		int minimum = INT_MAX;
		int middle = table.size() / 2;
		// we don't neet to check all the possible red team
		// since if red choose 1,2,3, blue must choose 4,5,6 and vice verse.
		// that is the case of that red choose 4,5,6 isn't needed.
		for (int i = 0; i < middle; i++) { 
			visit[i] = true;
			minimum = min(minimum, DFS(table, visit, 1, middle, i + 1));
			visit[i] = false;
		}
		return minimum;
	}
	
	//1 2 3 4 5 6
	//6 5 4 3 2 1
	
	int main() {
		//vector<vector<int>> table = makeTable();
		vector<vector<int>> table = makeTable2();
		cout << makeTeam(table);
		return 0;
	}
	
	
```
{% endhighlight %}
