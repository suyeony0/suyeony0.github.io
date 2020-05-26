---
layout: post
title: [Samsung SW - LAB]
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}
	﻿	[108. [BACKJOON – SAMSUNG SW : LAB]]
	- At first, I tried brute force. But it took so much time so I sholud’ve changed the algorithm
	- the brute force algorithm is below.
	#include<iostream>
	#include<fstream>
	#include<vector>
	#include<cmath>
	#include<queue>
	using namespace std;
	
	pair<vector<vector<int>>,queue<vector<int>>> makeTable() {
		ifstream in("C:\\Users\\gjsgu\\Desktop\\Algorithm\\test_case\\test_case_for_LAB.txt");
		int N, M;
		if (in.is_open()) {
			cout << "file is opened." << endl;
			in >> N; in >> M;
		}
		int temp;
		vector<vector<int>> table(N, vector<int>(M, 0));
		queue<vector<int>> que;
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < M; j++) {
				in >> table[i][j];
				if (table[i][j] == 2) que.push(vector<int>{ {i, j}});
				
			}
		}
		return make_pair(table,que);
	}
	pair<vector<vector<int>>, queue<vector<int>>> makeTable2() {
		
		int N, M;
		cin >> N; cin >> M;
		int temp;
		vector<vector<int>> table(N, vector<int>(M, 0));
		queue<vector<int>> que;
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < M; j++) {
				cin >> table[i][j];
				if (table[i][j] == 2) que.push(vector<int>{ {i, j}});
	
			}
		}
		return make_pair(table, que);
	}
	
	void printTable(vector<vector<int>>& table) {
		for (vector<int> row : table) {
			for (int i : row) {
				cout << i << " ";
			}
			cout << endl;
		}
	}
	void BFS(vector<vector<int>>& table,vector<int> virus) {
		queue<vector<int>> que;
		que.push(virus);
		while (!que.empty()) {
			int x = que.front()[0]; int y = que.front()[1];
			que.pop();
			if (x - 1 >= 0 && table[x - 1][y] == 0) {
				table[x - 1][y] = 2;
				que.push(vector<int>{x - 1, y});
			}
			if (y - 1 >= 0 && table[x][y - 1] == 0) {
				table[x][y - 1] = 2;
				que.push(vector<int>{ x,y - 1 });
			}
			if (x + 1 < table.size() && table[x + 1][y] == 0) {
				table[x + 1][y] = 2;
				que.push(vector<int>{x + 1, y});
			}
			if (y + 1 < table.size() && table[x][y + 1] == 0) {
				table[x][y + 1] = 2;
				que.push(vector<int>{x, y + 1});
			}
		}
	}
	
	int safetyArea(vector<vector<int>> table,queue<vector<int>> que) {
		while (!que.empty()) {
			BFS(table, que.front());
			que.pop();
		}
		int sum = 0;
		for (vector<int> row : table) {
			for (int i : row) {
				i == 0 ? sum++ : 0;
			}
		}
		return sum;
	}
	
	int DFS(vector<vector<int>> table,queue<vector<int>> que,int depth) {
		if (depth == 3) {
			return safetyArea(table,que);
		}
		int maximum = 0;
		for (int i = 0; i < table.size(); i++) {
			for (int j = 0; j < table[0].size(); j++) {
				if (table[i][j] != 0) continue;
				table[i][j] = 1;
				maximum=max(maximum,DFS(table, que, depth + 1));
				table[i][j] = 0;
			}
		}
		return maximum;
	}
	
	int main() {
		pair<vector<vector<int>>,queue<vector<int>>> input = makeTable();
		//pair<vector<vector<int>>, queue<vector<int>>> input = makeTable2();
		cout << DFS(input.first,input.second,0);
		return 0;
	}
	
	- Now, I have to find another solution.
	- But most people solve this problem as brute force. so I changed DFS to BFS.
	- I have no idea why it’s wrong! at 11%, failure occurs.
	- see the code.
	#include<iostream>
	#include<fstream>
	#include<vector>
	#include<cmath>
	#include<queue>
	using namespace std;
	
	pair<vector<vector<int>>,queue<vector<int>>> makeTable(vector<vector<int>>& empty) {
		ifstream in("C:\\Users\\gjsgu\\Desktop\\Algorithm\\test_case\\test_case_for_LAB.txt");
		int N, M;
		if (in.is_open()) {
			cout << "file is opened." << endl;
			in >> N; in >> M;
		}
		int temp;
		vector<vector<int>> table(N, vector<int>(M, 0));
		queue<vector<int>> que;
		
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < M; j++) {
				in >> table[i][j];
				if (table[i][j] == 2) que.push(vector<int>{ {i, j}});
				else if (table[i][j] == 0) empty.push_back({i,j});
				
			}
		}
		return make_pair(table,que);
	}
	pair<vector<vector<int>>, queue<vector<int>>> makeTable2(vector<vector<int>> & empty) {
		
		int N, M;
		cin >> N; cin >> M;
		int temp;
		vector<vector<int>> table(N, vector<int>(M, 0));
		queue<vector<int>> que;
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < M; j++) {
				cin >> table[i][j];
				if (table[i][j] == 2) que.push(vector<int>{ {i, j}});
				else if (table[i][j] == 0) empty.push_back({ i,j });
	
			}
		}
		return make_pair(table, que);
	}
	
	void printTable(vector<vector<int>>& table) {
		for (vector<int> row : table) {
			for (int i : row) {
				cout << i << " ";
			}
			cout << endl;
		}
	}
	
	
	int safetyArea(vector<vector<int>> & table) {
		int sum = 0;
		for (vector<int> row : table) {
			for (int i : row) {
				if (i == 0) sum++;
			}
		}
		return sum;
	}
	int contagion(vector<vector<int>> table,queue<vector<int>> que) {
		while (!que.empty()) {
			int x = que.front()[0]; int y = que.front()[1];
			que.pop();
			if (x - 1 >= 0 && table[x - 1][y] == 0) {
				table[x - 1][y] = 2;
				que.push(vector<int>{x - 1, y});
			}
			if (y - 1 >= 0 && table[x][y - 1] == 0) {
				table[x][y - 1] = 2;
				que.push(vector<int>{ x,y - 1 });
			}
			if (x + 1 < table.size() && table[x + 1][y] == 0) {
				table[x + 1][y] = 2;
				que.push(vector<int>{x + 1, y});
			}
			if (y + 1 < table.size() && table[x][y + 1] == 0) {
				table[x][y + 1] = 2;
				que.push(vector<int>{x, y + 1});
			}
		}
		return safetyArea(table);
	}
	
	int BFS(vector<vector<int>> table, queue<vector<int>> que, vector<vector<int>> empty) {
		int maximum = 0;
		int depth = 0;
		for (int i = 0; i < empty.size()-2; i++) {
			table[empty[i][0]][empty[i][1]] = 3;
			for (int j = i+1; j < empty.size()-1; j++) {
				table[empty[j][0]][empty[j][1]] = 3;
				for (int k = j+1; k < empty.size(); k++) {
					table[empty[k][0]][empty[k][1]] = 3;
					maximum=max(maximum,contagion(table, que));
					table[empty[k][0]][empty[k][1]] = 0;
				}
				table[empty[j][0]][empty[j][1]] = 0;
			}
			table[empty[i][0]][empty[i][1]] = 0;
		}
		return maximum;
	}
	
	int main() {
		vector<vector<int>> empty;
		pair<vector<vector<int>>,queue<vector<int>>> input = makeTable(empty);
		//pair<vector<vector<int>>, queue<vector<int>>> input = makeTable2(empty);
		//printTable(input.first);
		cout << BFS(input.first, input.second, empty);
		return 0;
	}
	
	- Finally, I found the error.
	- when I compare the range in the function contagion. I compare y index with table.size() not table[0].size().
	- due to [0], I took almost 3 hours. what the fxxk!
	- see the final code.
	#include<iostream>
	#include<fstream>
	#include<vector>
	#include<cmath>
	#include<queue>
	using namespace std;
	
	pair<vector<vector<int>>, vector<vector<int>>> makeTable(vector<vector<int>>& empty, queue<vector<int>>& que) {
		ifstream in("C:\\Users\\gjsgu\\Desktop\\Algorithm\\test_case\\test_case_for_LAB.txt");
		int N, M;
		if (in.is_open()) {
			cout << "file is opened." << endl;
			in >> N; in >> M;
		}
		int temp;
		vector<vector<int>> table(N, vector<int>(M, 0));
		vector<vector<int>> visit(N, vector<int>(M, 0));
		
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < M; j++) {
				in >> table[i][j];
				if (table[i][j] == 2) {
					que.push(vector<int>{ {i, j}});
					//visit[i][j] = 1;
				} 
				else if (table[i][j] == 0) empty.push_back({i,j});
				
			}
		}
		return make_pair(table, visit);
	}
	pair<vector<vector<int>>, vector<vector<int>>> makeTable2(vector<vector<int>> & empty, queue<vector<int>>& que) {
		
		int N, M;
		cin >> N; cin >> M;
		int temp;
		vector<vector<int>> table(N, vector<int>(M, 0));
		vector<vector<int>> visit(N, vector<int>(M, 0));
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < M; j++) {
				cin >> table[i][j];
				if (table[i][j] == 2) {
					que.push(vector<int>{ {i, j}});
					//visit[i][j] = 1;
				} 
				else if (table[i][j] == 0) empty.push_back({ i,j });
	
			}
		}
		return make_pair(table, visit);
	}
	
	void printTable(vector<vector<int>>& table) {
		for (vector<int> row : table) {
			for (int i : row) {
				cout << i << " ";
			}
			cout << endl;
		}
	}
	
	
	int safetyArea(vector<vector<int>> & table) {
		int sum = 0;
		for (vector<int> row : table) {
			for (int i : row) {
				if (i == 0) sum++;
			}
		}
		return sum;
	}
	
	
	int contagion(vector<vector<int>> table,queue<vector<int>> que, vector<vector<int>> visit) {
		while (!que.empty()) {
			int x = que.front()[0]; int y = que.front()[1];
			que.pop();
			if (visit[x][y] == 1) continue;
			visit[x][y] = 1;
			if (x - 1 >= 0 && table[x - 1][y] == 0) {
				table[x - 1][y] = 2;
	
				que.push(vector<int>{x - 1, y});
			}
			if (y - 1 >= 0 && table[x][y - 1] == 0) {
				table[x][y - 1] = 2;
	
				que.push(vector<int>{ x,y - 1 });
			}
			if (x + 1 < table.size() && table[x + 1][y] == 0) {
				table[x + 1][y] = 2;
	
				que.push(vector<int>{x + 1, y});
			}
			if (y + 1 < table[0].size() && table[x][y + 1] == 0) {
				table[x][y + 1] = 2;
	
				que.push(vector<int>{x, y + 1});
			}
		}
		return safetyArea(table);
	}
	
	
	int BFS(vector<vector<int>> table, queue<vector<int>> que, vector<vector<int>> empty,vector<vector<int>> visit) {
		int maximum = 0;
		int depth = 0;
		for (int i = 0; i < empty.size()-2; i++) {
			table[empty[i][0]][empty[i][1]] = 3;
			for (int j = i+1; j < empty.size()-1; j++) {
				table[empty[j][0]][empty[j][1]] = 3;
				for (int k = j+1; k < empty.size(); k++) {
					table[empty[k][0]][empty[k][1]] = 3;
					maximum=max(maximum,contagion(table, que,visit));
					table[empty[k][0]][empty[k][1]] = 0;
				}
				table[empty[j][0]][empty[j][1]] = 0;
			}
			table[empty[i][0]][empty[i][1]] = 0;
		}
		return maximum;
	}
	
	
	
	int main() {
		vector<vector<int>> empty;
		queue<vector<int>> que;
		//pair<vector<vector<int>>,vector<vector<int>>> input = makeTable(empty,que);
		pair<vector<vector<int>>, vector<vector<int>>> input = makeTable2(empty,que);
		//printTable(input.first);
		cout << BFS(input.first, que, empty,input.second);
		return 0;
	}
	
{% endraw %}
