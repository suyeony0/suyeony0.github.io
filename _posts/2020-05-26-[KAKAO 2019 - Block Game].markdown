---
layout: post
title: [KAKAO 2019 - Block Game]
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

	﻿[132. [Programmers– KAKAO 2019 :Block Game]]
	- Even though it was level 4 problem, it was easy for me.
	- I was happy it was not a fucking string parsing :)
	- the reason why this problem was easy is there is no time limitation. so I can use some functions roughly and repeatedly.
	- see the code.
	#include <string>
	#include <vector>
	#include<iostream>
	#include<map>
	#define min(a,b) a>b ? b:a
	#define max(a,b) a>b ? a:b
	using namespace std;
	int res = 0;
	
	void printTable(vector<vector<int>>& table) {
		for (vector<int> row : table) {
			for (int i : row)
				cout << i << " ";
			cout << endl;
		}
		cout << endl;
	}
	
	bool isRectangular(vector<vector<int>>& table,int tx,int ty,int bx,int by,int block) {
		if (bx == tx && by == ty) return false;
		//cout << "변환 전 : " << block << endl;
		//cout << tx << ty << " , " << bx << by << endl;
		//printTable(table);
		vector<vector<int>> temp = table;
		for (int i = tx; i <= bx; i++) {
			for (int j = ty; j <= by; j++) {
				if (block != temp[i][j]) {
					//cout << i << "," << j << ","<<temp[i][j] << endl;
					return false;
				} 
				temp[i][j] = 0;
			}
		}
		//cout << "변환 후 : "<<block << endl;
		//printTable(temp);
		table = temp;
		res++;
		return true;
	}
	
	void SetInformation(vector<vector<int>> board, int bs, vector<int>& top,vector<int>& height,map<int,int>& blocks_top) {
		for (int i = bs - 1; i >= 0; i--) {
			for (int j = 0; j < bs; j++) {
				if (board[i][j] == 0) continue;
				blocks_top[board[i][j]] = i;
				top[j] = board[i][j];
				height[j] = i;
			}
		}
	}
	
	void getLimit(int& tx, int& ty, int& bx, int& by, int block,vector<vector<int>>& table) {
		for (int i = 0; i < table.size(); i++) {
			for (int j = 0; j < table[i].size(); j++) {
				if (table[i][j] == block) {
					tx = min(tx, i); ty = min(ty, j); bx = max(bx, i); by = max(by, j);
				}
			}
		}
	}
	
	int solution(vector<vector<int>> board) {
		int answer = 0;
		int bs = board.size();
		vector<int> top(bs, 0); //a columns top block
		vector<int> height(bs, 0); // a columns top height
		map<int, int> blocks_top; // block number - the block's top height;
		SetInformation(board, bs, top, height,blocks_top);
	
		for (map<int, int>::iterator iter = blocks_top.begin(); iter != blocks_top.end();) {
			int tx=999, ty=999, bx=-1, by=-1;
			int cur_block = iter->first;
			vector<vector<int>> cur_table = board;
			
			for (int j = 0; j < bs; j++) {
				if (top[j] == cur_block && height[j] > iter->second) {
					for (int i = height[j] - 1; i >= iter->second; i--) {
						cur_table[i][j] = cur_block;
					}
				}
			}
			getLimit(tx, ty, bx, by, cur_block, cur_table); // get the block's boundary
			if (isRectangular(cur_table, tx, ty, bx, by, cur_block)) { //check if the block is rectangular
				board = cur_table;
				blocks_top.erase(cur_block); //if it is rectangular, remove that blcok from the board.
				SetInformation(board, bs, top, height, blocks_top); //reset the information.
				iter = blocks_top.begin();
			}
			else iter++;
		}
		return res;
	}
	int main() {
		
		return 0;
	}
	
