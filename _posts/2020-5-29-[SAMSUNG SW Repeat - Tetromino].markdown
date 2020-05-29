---
layout: post
title: [SAMSUNG SW Repeat - Tetromino]
date: 2020-5-29
description: txt to markdown
thumbnail: work1.jpg
categories: SAMSUNG_SW

# Information for the author block
author : Loui
---

```cpp

{% raw %}

	[6. SAMSUNG SW : Tetromino]
	- it was a simulation problem. but there was lots of manual labor.
	- since I had to implement all the cases of tetromino shape.
	- and for sliding each tetromino, I used quadruple for syntax.
	- I spent 26 minute and 35 seconds.
	- see the code.
	#include<iostream>
	#include<vector>
	#define max(a,b) a>b?a:b
	using namespace std;
	
	vector<vector<int>> table;
	int N, M;
	vector<vector<vector<int>>> tetro = {
		{{1,1,1,1}}, {{1},{1},{1},{1}}, //line
		{{1,1},{1,1}},//square
	
	{{1,0},{1,0},{1,1}},{{0,1},{0,1},{1,1} }, {{1,1},{0,1},{0,1}},{{1,1},{1,0},{1,0}},
	{ {1,1,1},{1,0,0}}, {{1,1,1},{0,0,1}},{{1,0,0} ,{1,1,1}},{ {0,0,1} ,{1,1,1}},
	
	{{1,0},{1,1},{0,1}},{{0,1},{1,1},{1,0}},{{1,1,0},{0,1,1}},{{0,1,1},{1,1,0}},
	{{1,1,1},{0,1,0}},{{0,1,0},{1,1,1}},{{1,0},{1,1},{1,0}},{{0,1},{1,1},{0,1}}
	
	};
	
	
	
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
	
		//get input
		cin >> N >> M;
		table.assign(N, vector<int>(M, 0));
		for (int i = 0; i < N; i++) {
			for (int j = 0; j < M; j++) {
				cin >> table[i][j];
			}
		}
	
		//algorithm part
		int answer = 0;
		for (vector<vector<int>> piece : tetro) {
			int row = piece.size(); int col = piece[0].size();
			for (int x = 0; x + row <= N;x++) {
				for (int y = 0; y + col <= M;y++) {
					int temp = 0;
					for (int i = x; i < x+row; i++) {
						for (int j = y; j < y+col; j++) {
							if (piece[i - x][j - y] == 1) temp += table[i][j];
						}
					}
					answer = max(answer, temp);
				}
			}
		}
		cout << answer;
		return 0;
	
	}
	
	
{% endraw %}
```

