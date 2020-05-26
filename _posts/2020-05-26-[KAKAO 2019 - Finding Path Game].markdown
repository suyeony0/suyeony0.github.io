---
layout: post
title: [KAKAO 2019 - Finding Path Game]
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

	﻿
	[130. [Programmers– KAKAO 2019 :Finding Path Game]]
	- this problem’s point was the way to make tree.
	- I spent 3 hours or so to make tree.
	- I have been stuck since I barely came up with a method to make tree. the given vector sholud be splited before making tree.
	- see the code.
	#include <string>
	#include <vector>
	#include<iostream>
	#include<algorithm>
	#include<queue>
	using namespace std;
	vector<int> preorder;
	vector<int> postorder;
	struct Node {
		int x;
		int y;
		int index;
		Node* left=nullptr;
		Node* right=nullptr;
		Node(int _x, int _y, int _index) {
			x = _x; y = _y; index = _index;
		};
		~Node() {}
	};
	
	pair<vector<pair<vector<int>, int>>, vector<pair<vector<int>, int>>> LRSplit(vector<pair<vector<int>, int>> table,int mid) {
		vector < pair<vector<int>, int>> left;
		vector < pair<vector<int>, int>> right;
		for (int i = 0; i < table.size(); i++) {
			if (table[i].first[0] < mid) left.push_back(table[i]);
			else right.push_back(table[i]);
		}
		return make_pair(left, right);
	}
	
	void makeTree(Node* root,vector<pair<vector<int>,int>> table) {
		table.erase(table.begin());
		if (table.empty()) return;
		pair<vector<pair<vector<int>, int>>, vector<pair<vector<int>, int>>> splited = LRSplit(table, root->x);
		vector < pair<vector<int>, int>> left = splited.first;
		vector < pair<vector<int>, int>> right = splited.second;
		if(!left.empty())root->left = new Node(left[0].first[0], left[0].first[1], left[0].second);
		if(!right.empty())root->right = new Node(right[0].first[0], right[0].first[1], right[0].second);
		if(root->left) makeTree(root->left, left);
		if(root->right) makeTree(root->right, right);
	}
	
	void printTree(vector < pair<vector<int>, int>> tree) {
		for (int i = 0; i < tree.size(); i++) {
			cout << tree[i].first[0] << "," << tree[i].first[1] << " ";
		}
		cout << endl;
	
	}
	void PreOrderSearch(Node* root) {
		if (!root) return;
		preorder.push_back(root->index);
		PreOrderSearch(root->left);
		PreOrderSearch(root->right);
	}
	void PostOrderSearch(Node* root) {
		if (!root) return;
		PostOrderSearch(root->left);
		PostOrderSearch(root->right);
		postorder.push_back(root->index);
	}
	
	void printAnswer(vector<vector<int>>& answer) {
		for (vector<int> row : answer) {
			for (int i : row) {
				cout << i << " ";
			}
			cout << endl;
		}
	}
	
	vector<vector<int>> solution(vector<vector<int>> nodeinfo) {
		vector<vector<int>> answer;
		vector<pair<vector<int>, int>> table;
		for (int i = 0; i < nodeinfo.size(); i++) table.push_back(make_pair(nodeinfo[i], i + 1));
		sort(table.begin(), table.end(), [](pair<vector<int>, int> a, pair<vector<int>, int> b) {return a.first[1] > b.first[1];}); //y first sort
		Node* root = new Node(table[0].first[0], table[0].first[1], table[0].second);
		makeTree(root, table);
		PreOrderSearch(root);
		PostOrderSearch(root);
		answer.push_back(preorder);
		answer.push_back(postorder);
		return answer;
	}
	
	int main() {
		//solution({{5, 3}, {11, 5}, {13, 3}, {3, 5}, {6, 1}, {1, 3}, {8, 6}, {7, 2}, {2, 2}} );
		return 0;
	}
	
