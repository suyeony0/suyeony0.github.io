---
layout: post
title: [SAMSUNG SW Repeat - Robot Vaccum]
date: 2020-6-4
description: txt to markdown
thumbnail: breakfast-orange-lemon-oranges-large.jpg
categories: SAMSUNG_SW

# Information for the author block
author : Loui
---

[9. SAMSUNG SW : Robot Vaccum]
- this was a simulation problem. I just had to follow given rule.
- there was no trick. so it was easy.
- I sepnt 20 minutes and 31 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>

using namespace std;

int N, M,x,y,d;
vector<vector<int>> table;

int dir[4][2] = { {-1,0},{0,1},{1,0},{0,-1} };

int answer = 0;

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	cin >> N >> M;
	cin >> x >> y >> d;
	table.assign(N, vector<int>(M, 0));
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < M; j++) {
			cin >> table[i][j];
		}
	}

	//algorithm part
	while(true) {
		
		
		if (table[x][y] == 0) {
			answer += 1;
			table[x][y] = 2;
		} 
		


		bool flag = false;

		for (int rotate = 0; rotate < 4; rotate++) {
			d -= 1; if (d < 0) d = 3;
			int nx = x + dir[d][0]; int ny = y + dir[d][1];
			if (nx>=0 && ny>=0 && nx<N && ny<M && table[nx][ny] == 0) {
				x = nx; y = ny;
				flag = true;
				break;
			}
		}
		if (flag) continue;
		else {
			x -= dir[d][0]; y -= dir[d][1];
			if (x < 0 || y < 0 || x >= N || y >= M || table[x][y]==1) break;
		}
	}
	cout << answer;
	return 0;
}

{% endraw %}
```

