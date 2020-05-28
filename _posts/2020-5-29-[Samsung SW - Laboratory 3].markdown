---
layout: post
title: [Samsung SW - Laboratory 3]
date: 2020-5-29
description: txt to markdown
thumbnail: breakfast-orange-lemon-oranges-large.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

{% highlight c++ %}
```cpp
	﻿[147. [SAMSUNG – SW : Laboratory 3 ]]
	- huh… so much edge case!
	- I used DFS for permutation of viruses and BFS for contagion.
	- see the code.
	#include<iostream>
	#include<fstream>
	#include<vector>
	#include<queue>
	#include<set>
	using namespace std;
	
	int lab_size, number_of_virus;
	int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} }; // up left down right
	vector<vector<int>> table;
	vector<vector<bool>> visit;
	vector<pair<int, int>> virus;
	vector<pair<int, int>> chosen_virus;
	set<int> min_time;
	void Input() {
		ifstream in("C:\\Users\\gjsgu\\Desktop\\Algorithm\\test_case\\test_case_for_laboratory3.txt");
		if (in.is_open()) cout << "file is opened." << endl;
		in >> lab_size; in >> number_of_virus;
		table.assign(lab_size, vector<int>(lab_size, 0));
		visit.assign(lab_size, vector<bool>(lab_size, 0));
		int temp_input;
		for (int i = 0; i < lab_size; i++) {
			for (int j = 0; j < lab_size; j++) {
				in >> temp_input;
				table[i][j]=temp_input;
				visit[i][j] = temp_input;
				if (temp_input == 2) {
					virus.push_back(make_pair(i, j));
					visit[i][j] = false;
				} 
				
			}
		}
	}
	void Input2() {
		cin >> lab_size; cin >> number_of_virus;
		table.assign(lab_size, vector<int>(lab_size, 0));
		visit.assign(lab_size, vector<bool>(lab_size, 0));
		int temp_input;
		for (int i = 0; i < lab_size; i++) {
			for (int j = 0; j < lab_size; j++) {
				cin >> temp_input;
				table[i][j] = temp_input;
				visit[i][j] = temp_input;
				if (temp_input == 2) {
					virus.push_back(make_pair(i, j));
					visit[i][j] = false;
				}
	
			}
		}
	}
	void printTable(vector<vector<int>>& temp) {
		for (vector<int> row : temp) {
			for (int i : row) cout << i << " ";
			cout << endl;
		}
		cout << endl;
	}
	
	bool isContagious(vector<vector<int>>& temp) {
		for (int i = 0; i < lab_size; i++) 
			for (int j = 0; j < lab_size; j++) if (temp[i][j] == 0) return false;
		//printTable(temp);
		return true;
	}
	
	
	
	int BFS() {
		vector<vector<int>> temp = table;
		vector<vector<bool>> temp_visit=visit;
		queue<pair<int, int>> que;
		queue<pair<int, int>> new_que;
		for (pair<int, int> a : chosen_virus) new_que.push(a);
		//for (pair<int, int> a : chosen_virus) cout << a.first << "," << a.second << endl; cout << endl;
		int time = 0;
		
		while (!new_que.empty()) {
			bool flag = false;
			que = new_que;
			new_que = queue<pair<int, int>>(); // make new_que empty;
			while (!que.empty()) {
				int x = que.front().first; int y = que.front().second;
				que.pop();
				for (int i = 0; i < 4; i++) {
					int tx = x + dir[i][0]; int ty = y + dir[i][1];
					if (tx >= 0 && ty >= 0 && tx < lab_size && ty < lab_size &&  !temp_visit[tx][ty]) {
						if (temp[tx][ty] != 2) flag = true;
						temp_visit[tx][ty] = true; //make visit
						temp[tx][ty] = time+10;
						new_que.push(make_pair(tx, ty));
					}
				}
			}
			if (flag) time++;
			else if (!isContagious(temp)) time++;
		}
		if(isContagious(temp)) return time;
		return 999;//max lab_size is 50 so 999 is enough
	}
	
	
	void Contagion(int count,int start) {
		if (count == number_of_virus) {
			int res = BFS();
			//cout <<"res : "<< res << endl<<endl;
			min_time.insert(res);
			return;
		} 
		for (int i = start; i < virus.size(); i++) {
			int x = virus[i].first; int y = virus[i].second;
			chosen_virus.push_back(make_pair(x, y));
			visit[x][y] = true;
			Contagion(count + 1, i + 1);
			visit[x][y] = false;
			chosen_virus.pop_back();
		}
	
	}
	
	int main() {
		Input2();
		Contagion(0,0);
		int answer= *min_time.begin();
		answer == 999 ? cout<<-1 : cout<<answer;
		return 0;
	}
	
	
```
{% endhighlight %}
