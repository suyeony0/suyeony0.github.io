---
layout: post
title: [Samsung SW - Dice Yut Play]
date: 2020-5-29
description: txt to markdown
thumbnail: food2.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

```cpp
	﻿[151. [SAMSUNG – SW : Dice Yut Play]] 
	- this was the last problem of SAMSUNG SW in Baekjoon. But sadly, my algorithm didn’t work well. so I refered to below URL.
	https://eine.tistory.com/entry/%EB%B0%B1%EC%A4%80-17825%EB%B2%88-%EC%A3%BC%EC%82%AC%EC%9C%84-%EC%9C%B7%EB%86%80%EC%9D%B4-%EB%AC%B8%EC%A0%9C-%ED%92%80%EC%9D%B4
	- In my case, I made all the node of the board and did brute force, but answer was wrong.
	- so I took the above URL’s code. he used bit mask for permutation that made using DFS in my case. so genius…
	- Futhermore, he made lookup table. I’ve never thought that I could make it as a look up table! I learned a lot from the URL.
	- see the code.
	#include<iostream>
	#include<vector>
	#define max(a,b) a>b?a:b
	using namespace std;
	#define endl '\n'
	typedef long long ll;
	typedef pair<int, int> pii;
	int dice[10];
	#define END 32
	
	//이동 규칙이 복잡할 수 있으므로 Look-up 테이블을 만들어서 사용한다.
	//jump[index][0] = 해당 판 점수
	//jump[index][1~5] => 주사위 해당 수가 나오면 이동하는 양
	int jump[33][6] = {
		{0,1,2,3,4,5}, //0번자리
		{2,2,3,4,5,9}, //1번자리
		{4,3,4,5,9,10}, //2번자리
		{6,4,5,9,10,11}, //3번자리
		{8,5,9,10,11,12},//4번자리
		{10,6,7,8,20,29},//5번자리
		{13,7,8,20,29,30}, //6번자리
		{16,8,20,29,30,31}, //7번자리
		{19,20,29,30,31,32}, //8번자리
		{12,10,11,12,13,14}, //9번자리
		{14,11,12,13,14,15}, //10번자리
		{16,12,13,14,15,16}, //11번자리
		{18,13,14,15,16,17}, //12번자리
		{20,18,19,20,29,30}, //13번자리
		{22,15,16,17,24,25}, //14번자리
		{24,16,17,24,25,26}, //15번자리
		{26,17,24,25,26,27}, //16번자리
		{28,24,25,26,27,28}, //17번자리
		{22,19,20,29,30,31}, //18번자리
		{24,20,29,30,31,32}, //19번자리
		{25,29,30,31,32,32}, //20번자리
		{26,20,29,30,31,32}, //21번자리
		{27,21,20,29,30,31}, //22번자리
		{28,22,21,20,29,30}, //23번자리
		{30,23,22,21,20,29}, //24번자리
		{32,26,27,28,31,32}, //25번자리
		{34,27,28,31,32,32}, //26번자리
		{36,28,31,32,32,32}, //27번자리
		{38,31,32,32,32,32}, //28번자리
		{30,30,31,32,32,32}, //29번자리
		{35,31,32,32,32,32}, //30번자리
		{40,32,32,32,32,32}, //31번자리
		{0,32,32,32,32,32} //32번자리
	};
	int ans=0;
	void check(int bit) {
		int score = 0;
		vector<int>occupation(35);
		vector<int> pos(4);
		occupation[0] = 4;
	
		for (int turn = 0; turn < 10; turn++) {
			//이번에 옮길 말
			int horse = (bit >> (turn * 2)) & 0x3;
			//cout << horse << endl;
			//이동하는 거리
			int move = dice[turn];
	
			//현재 위치
			int& current_pos = pos[horse];
	
			//이동할 위치
			int next_pos = jump[current_pos][move];
	
			//이번 이동으로 얻을 점수
			int get_score = jump[next_pos][0];
	
			//처음이나 끝 위치가 아닌데 말이 겹치는 경우
			if (occupation[next_pos] > 0 && next_pos && next_pos != END) {
				//불가능한 이동
				return;
			}
			else {
				score += get_score;
				occupation[next_pos]++;
				occupation[current_pos]--;
				current_pos = next_pos;
			}
		}
		ans = max(ans, score);
	}
	int main() {
		for (int i = 0; i < 10; i++)
			cin >> dice[i];
		for (int bit = 0; bit < (1 << 20); bit++) {
			check(bit);
		}
		cout << ans << endl;
	
	}
	
	
	
	
```
