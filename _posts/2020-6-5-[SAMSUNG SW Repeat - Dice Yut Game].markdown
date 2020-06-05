---
layout: post
title: [SAMSUNG SW Repeat - Dice Yut Game]
date: 2020-6-5
description: txt to markdown
thumbnail: food1.jpg
categories: SAMSUNG_SW

# Information for the author block
author : Loui
---

﻿[29. SAMSUNG SW : Dice Yut Game]
- It was a permutation problem with simulation.
- For Yut Game, I had to implement look-up table by myself. It was a manual labour.
- To implement permutation, I used DFS. I hesitated since permutation usually consume lots of computational time. but there was no time limet exceeded.
- In terms of look-up table, I used map<int,vector<int>>, the key is an index of a shell on the board and the value[0] is a score a shell has, value[1:5] is next shell after moving 1~5 shell.
- I spent 45 minutes and 35 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<map>
#define max(a,b) a>b?a:b
using namespace std;

vector<int> order(10,0);
vector<int> horse(4,0);
map<int, vector<int>> table; // index : value , after 1,2,3,4,5
int answer = 0;
vector<bool> visit(33, false);

void InitBoard() {
	//making Yut board
	table[0] = vector<int>{ 0,1,2,3,4,5 }; // start position
	table[1] = vector<int>{ 2,2,3,4,5,6 };
	table[2] = vector<int>{ 4,3,4,5,6,7 };
	table[3] = vector<int>{ 6,4,5,6,7,8 };
	table[4] = vector<int>{ 8,5,6,7,8,9 };
	table[5] = vector<int>{ 10,22,23,24,30,31 }; //first blue circle
	table[6] = vector<int>{ 12,7,8,9,10,11 };
	table[7] = vector<int>{ 14,8,9,10,11,12 };
	table[8] = vector<int>{ 16,9,10,11,12,13 };
	table[9] = vector<int>{ 18,10,11,12,13,14 };
	table[10] = vector<int>{20,25,26,30,31,32};// second blue circle, 28 is just before 40
	table[11] = vector<int>{ 22,12,13,14,15,16 };
	table[12] = vector<int>{ 24,13,14,15,16,17 };
	table[13] = vector<int>{ 26,14,15,16,17,18 };
	table[14] = vector<int>{ 28,15,16,17,18,19 };
	table[15] = vector<int>{30,27,28,29,30,31};// third blue circle
	table[16] = vector<int>{ 32,17,18,19,20,21 };
	table[17] = vector<int>{ 34,18,19,20,21,21 };
	table[18] = vector<int>{ 36,19,20,21,21,21 };
	table[19] = vector<int>{ 38,20,21,21,21,21 };
	table[20] = vector<int>{ 40,21,21,21,21,21 };
	table[21] = vector<int>{ 0,21,21,21,21,21 }; //end position
	table[22] = vector<int>{ 13,23,24,30,31,32 };
	table[23] = vector<int>{ 16,24,30,31,32,20 };
	table[24] = vector<int>{ 19,30,31,32,20,21 };
	table[25] = vector<int>{ 22,26,30,31,32,20 };
	table[26] = vector<int>{ 24,30,31,32,20,21 };
	table[27] = vector<int>{ 28,28,29,30,31,32 };
	table[28] = vector<int>{ 27,29,30,31,32,20 };
	table[29] = vector<int>{ 26,30,31,32,20,21 };
	table[30] = vector<int>{ 25,31,32,20,21,21 };
	table[31] = vector<int>{ 30,32,20,21,21,21 };
	table[32] = vector<int>{ 35,20,21,21,21,21 };
}

void DFS(int cnt, int res) {
	if (cnt == 10 ) {
		answer = max(answer, res);
		return;
	}
	for (int i = 0; i < 4; i++) {
		if (horse[i] == 21) continue;
		int next_shell= table[horse[i]][order[cnt]];
		if (next_shell != 21 && visit[next_shell] == true) continue;
		int temp = horse[i];
		horse[i] = next_shell;
		visit[temp] = false;
		visit[horse[i]] = true;
		DFS(cnt + 1,res+table[next_shell][0]);
		visit[horse[i]] = false;
		visit[temp] = true;
		horse[i] = temp;
	}
}

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);
	
	//get input
	for (int i = 0; i < 10; i++) cin >> order[i];
	InitBoard();
	//algorithm part
	DFS(0,0);
	cout << answer;
	return 0;
}

{% endraw %}
```

