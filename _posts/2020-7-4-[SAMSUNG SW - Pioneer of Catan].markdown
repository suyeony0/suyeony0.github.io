---
layout: post
title: [SAMSUNG SW - Pioneer of Catan]
date: 2020-7-4
description: txt to markdown
thumbnail: food1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

﻿[231. SAMSUNG SW – Pioneer of Catan]
- It was a difficult simulation problem. Since a shell has 6 neighbours.
- So implement 6 neighbout was the key of this problem.
- The second difficult thing was the way to dertermine next position.
- There are 6 possible next position. Let’s say current position is (x,y). Then possible next positions are (x-1,y+1), (x-2,y), (x-1,y-1), (x+1,y-1), (x+2,y), (x+1,y+1).
- To determine a next position, I drew some example. From the example, I’ve found a such rule.
- First round, we have to move above coordinates with {1,0,1,1,1,1} time respectively.
- Second round, {2,1,2,2,2,2}. Third round, {3,2,3,3,3,3} and so on.
- Finding next number was not that difficult. I just had to find minimum number that has minimum frequency.
- In addition, determining 2D array size was one of the key. If I took too small size, run time error occurred. But if I took too big size, I’ve stuck by memory limitation.
- Finally I found an adequate size that was 600 x 300.
- I spent 1 hours or so.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>

using namespace std;

vector<vector<int>> table;

int C,N;
int sx, sy;
const int dir[6][2] = { {-1,1},{-2,0},{-1,-1},{1,-1},{2,0},{1,1} };
vector<int> count_num; // To count number of apearance of each number.
vector<int> num_of_move;

int FindNextNumber(int x, int y) {
	vector<bool> visit(6,false); // index 0 won't be used.
	for (int d = 0; d < 6; d++) { //to check adjacent numbers
		int nx = x + dir[d][0]; int ny = y + dir[d][1];
		if (nx < 0 || ny < 0 || nx >= 600 || ny >= 300) continue;
		visit[table[nx][ny]] = true;
	}

	vector<int> will_check;
	for (int i = 1; i < 6; i++) if (visit[i] == false) will_check.emplace_back(i);

	int min_num = count_num[will_check[0]];
	int min_index = will_check[0];
	for (int i = 1; i < will_check.size(); i++) {
		if (min_num > count_num[will_check[i]]) {
			min_index = will_check[i];
			min_num = count_num[will_check[i]];
		} 
	}
	count_num[min_index] += 1;
	return min_index;
}

int Travel(int x,int y) {
	int cur_round = 1;
	table[x][y] = 1;
	int idx = 0;
	while (true) {
		for (int d = 0; d < 6; d++) {
			for (int move_num = 0; move_num < num_of_move[d]+idx; move_num++) {
				cur_round += 1;
				x = x + dir[d][0]; y = y + dir[d][1];
				table[x][y]=FindNextNumber(x,y);
				if (cur_round == N) return table[x][y];
			}
		}
		idx += 1;
	}

}

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	cin >> C;

	//algorithm part

	for (int t = 0; t < C; t++) {
		cin >> N;
		if (N == 1) cout << 1 << endl;
		else {
			table.assign(600, vector<int>(300, 0));
			num_of_move = { 1,0,1,1,1,1 };
			count_num = { 0,1,0,0,0,0 };
			sx = 300, sy = 150;
			int answer = Travel(sx, sy);
			cout << answer << endl;
		}
	}
	return 0;
}

{% endraw %}
```

