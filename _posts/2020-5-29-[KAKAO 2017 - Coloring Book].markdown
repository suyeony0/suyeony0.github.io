---
layout: post
title: [KAKAO 2017 - Coloring Book]
date: 2020-5-29
description: txt to markdown
thumbnail: food2.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

{% highlight c++ %}
```cpp
	﻿[180. [KAKAO 2017 : Coloring Book]
	- this was a simulation problem. I solved using BFS.
	- it’s quite long time since I used BFS lastly. so It took much more time.
	- see the code.
	#include <vector>
	#include<queue>
	#include<iostream>
	#define max(a,b) a>b?a:b
	using namespace std;
	
	
	int N, M;
	
	int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} }; // north west south east
	
	
	
	int BFS(int _x, int _y, vector<vector<int>>& table, vector<vector<bool>>& visit) {
		int cur_size = 0;
		int color = table[_x][_y];
		queue<pair<int, int>> que;
		que.push(make_pair(_x, _y));
		visit[_x][_y] = true;
		while (!que.empty()) {
			int x = que.front().first; int y = que.front().second;
			que.pop();
			cur_size++;
			for (int i = 0; i < 4; i++) {
				int nx = x + dir[i][0]; int ny = y + dir[i][1];
				if (nx >= 0 && ny >= 0 && nx < N && ny < M && visit[nx][ny] == false && table[nx][ny] == color) {
					que.push(make_pair(nx, ny));
					visit[nx][ny] = true;
				}
			}
			
		}
		return cur_size;
	}
	
	vector<int> solution(int row_size, int col_size, vector<vector<int>> picture) {
		N = row_size; M = col_size;
		vector<vector<bool>> visit(N, vector<bool>(M, false));
		int area = 0;
		int max_size = 0;
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < M; j++) {
				if (visit[i][j] == false && picture[i][j] != 0) {
					area++;
					int cur_size=BFS(i, j, picture,visit);
					max_size = max(max_size, cur_size);
				}
			}
		}
	
		vector<int> answer(2);
		answer[0] = area;
		answer[1] = max_size;
		cout << answer[0] << "," << answer[1] << endl;
		return answer;
	}
	
	int main() {
	
		return 0;
	}
	
```
{% endhighlight %}
