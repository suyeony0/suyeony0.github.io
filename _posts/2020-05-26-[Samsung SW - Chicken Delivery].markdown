---
layout: post
title: [Samsung SW - Chicken Delivery]
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

	﻿[117. [BACKJOON – SAMSUNG SW : Chicken Delivery]]
	- DFS was needed to choose which chicken house will be alive.
	- BFS was a significant problem, since when I used queue for BFS, time limit exceeded occurred.
	- so I throw the fxxking queue out and using vector to recored which chicken houses were chosen.
	- From the chosen chicken house, calculated distance between all the houses.
	- see the code.
	#include<iostream>
	#include<fstream>
	#include<vector>
	#include<climits>
	#include<queue>
	#define min(a,b) a>b ? b:a
	using namespace std;
	
	vector<vector<int>> table;
	vector<vector<int>> chicken;
	vector<vector<int>> house;
	vector<int> chosen;
	int N; int M;
	
	void makeTable() {
		ifstream in("C:\\Users\\gjsgu\\Desktop\\Algorithm\\test_case\\test_case_for_chicken_delivery.txt");
		if (in.is_open()) cout << "file is opened." << endl;
		in >> N>>M;
		int temp;
		for (int i = 0; i < N; i++) {
			table.push_back(vector<int>(N, 0));
			for (int j = 0; j < N; j++) {
				in >> temp;
				if (temp == 2) { chicken.push_back({ i,j });  continue;}
				if (temp == 1) house.push_back({ i,j });
				table[i][j] = 1;
			}
		}
		
	}
	
	void makeTable2() {
		cin >> N >> M;
		int temp;
		for (int i = 0; i < N; i++) {
			table.push_back(vector<int>(N, 0));
			for (int j = 0; j < N; j++) {
				cin >> temp;
				if (temp == 2) { chicken.push_back({ i,j });  continue; }
				if (temp == 1) house.push_back({ i,j });
				table[i][j] = 1;
			}
		}
	}
	
	
	int BFS() {
		int distance = 0;
		for (int k = 0; k < house.size(); k++) {
			int hx = house[k][0]; int hy = house[k][1];
			int minimum = INT_MAX;
			for (int i = 0; i < chosen.size(); i++) {
				int a = chosen[i];
				minimum = min(minimum, abs(hx - chicken[a][0]) + abs(hy - chicken[a][1]));
			}
			distance += minimum;
		}
		return distance;
	}
	
	
	int DFS(int start,int count) {
		if (count >= M) {
			return BFS();
		}
		int minimum = INT_MAX;
		for (int i = start; i < chicken.size(); i++) {
			int x = chicken[i][0]; int y = chicken[i][1];
			chosen.push_back(i);
			table[x][y] = 2;
			minimum=min(minimum,DFS(i + 1,count+1));
			table[x][y] = 0;
			chosen.pop_back();
		}
		return minimum;
	}
	
	int main() {
		//makeTable();
		makeTable2();
		cout << DFS(0,0);
		return 0;
	}
	
	
	
	
