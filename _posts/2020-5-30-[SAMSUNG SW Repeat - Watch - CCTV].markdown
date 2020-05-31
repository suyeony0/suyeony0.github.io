---
layout: post
title: [SAMSUNG SW Repeat - Watch - CCTV]
date: 2020-5-30
description: txt to markdown
thumbnail: food1.jpg
categories: SAMSUNG_SW

# Information for the author block
author : Loui
---
 
```cpp

{% raw %}

	[13. SAMSUNG SW : Watch - CCTV]
	- it was a combination problem. Implementing combination was not a big deal but removing blind spots using current cctvs¡¯ direction is quite hard.
	- so I made a function that remove blind spots of given direction with position (x,y)
	- And I gave all the possible direction for each cctv type.
	- I spent 34 minutes and 56 seconds.
	- see the code.
	#include<iostream>
	#include<vector>
	#define min(a,b) a>b? b:a
	using namespace std;
	
	int N, M;
	
	vector<vector<int>> cctv;
	int num_of_cctv;
	int answer = 987654321;
	int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };
	
	
	void blindSpot(vector<vector<int>>& temp_table) {
		int res = 0;
		for (vector<int> row : temp_table) {
			for (int i : row) if (i == 0) res += 1;
		}
		answer = min(answer, res);
	}
	
	vector<vector<int>> Watch(vector<vector<int>> temp_table,int x,int y,vector<int> d) {
	
		for (int i = 0; i < d.size(); i++) {
			int nx = x+dir[d[i]][0]; int ny = y+dir[d[i]][1];
			while (nx >= 0 && ny >= 0 && nx < N && ny < M && temp_table[nx][ny] != 6) {
				if(temp_table[nx][ny]==0) temp_table[nx][ny] = 7;
				nx = nx + dir[d[i]][0]; ny = ny + dir[d[i]][1];
			}
		}
		return temp_table;
	}
	
	
	void DFS(vector<vector<int>> table,int cnt, int start) {
		if (cnt == num_of_cctv) {
			blindSpot(table);
			return;
		}
	
		for (int i = start; i < num_of_cctv; i++) {
			int x = cctv[i][0]; int y = cctv[i][1]; int num = cctv[i][2];
			switch (num){
			case 1:
				for (int j = 0; j < 4; j++) DFS(Watch(table, x, y, vector<int>{j}),cnt+1,i+1);
				break;
			case 2 :
				DFS(Watch(table, x, y, vector<int>{0, 2}), cnt + 1, i + 1);
				DFS(Watch(table, x, y, vector<int>{1, 3}), cnt + 1, i + 1);
				break;
			case 3:
				DFS(Watch(table, x, y, vector<int>{0, 1}), cnt + 1, i + 1);
				DFS(Watch(table, x, y, vector<int>{1, 2}), cnt + 1, i + 1);
				DFS(Watch(table, x, y, vector<int>{2, 3}), cnt + 1, i + 1);
				DFS(Watch(table, x, y, vector<int>{3, 0}), cnt + 1, i + 1);
				break;
			case 4:
				DFS(Watch(table, x, y, vector<int>{0,1,2}), cnt + 1, i + 1);
				DFS(Watch(table, x, y, vector<int>{1,2,3}), cnt + 1, i + 1);
				DFS(Watch(table, x, y, vector<int>{2,3,0}), cnt + 1, i + 1);
				DFS(Watch(table, x, y, vector<int>{3,0,1}), cnt + 1, i + 1);
				break;
			case 5:
				DFS(Watch(table, x, y, vector<int>{0,1,2,3}), cnt + 1, i + 1);
				break;
	
			}
		}
	
	}
	
	
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
	
		//get input
		cin >> N >> M;
		vector<vector<int>> table(N, vector<int>(M, 0));
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < M; j++) {
				cin >> table[i][j];
				if (table[i][j] != 0 && table[i][j] != 6) cctv.emplace_back(vector<int>{i, j, table[i][j]});
			}
		}
	
		//algorithm part
		num_of_cctv = cctv.size();
		DFS(table, 0, 0);
		cout << answer;
		return 0;
	}
	
	
{% endraw %}
```

