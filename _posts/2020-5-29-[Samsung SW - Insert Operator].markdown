---
layout: post
title: [Samsung SW - Insert Operator]
date: 2020-5-29
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% highlight c++ %}
	﻿[110. [BACKJOON – SAMSUNG SW : Insert Operator]]
	- by using next_permutation, we can solve this problem very easily.
	- but there was a trap, the function next_permutation ant in ascending order. 
	- so we have to insert our operators in following order *,+,-,/.
	- cf.) ascii number of each operator is that * : 42, + : 43, - : 45, / : 47.
	- see the code.
	#include<iostream>
	#include<fstream>
	#include<vector>
	#include<algorithm>
	#include<climits>
	
	using namespace std;
	
	pair<vector<int>, vector<int>> makeTable() {
		ifstream in("C:\\Users\\gjsgu\\Desktop\\Algorithm\\test_case\\test_case_for_insert_operator.txt");
		int N;
		if (in.is_open()) {
			cout << "file is opened." << endl;
			in >> N;
		}
		vector<int> table(N, 0);
		vector<int> oper(4, 0);
		for (int i = 0; i < N; i++)
			in >> table[i];
		for (int i = 0; i < 4; i++)
			in >> oper[i];
		return make_pair(table, oper);
	}
	
	pair<vector<int>, vector<int>> makeTable2() {
		
		int N;
		cin >> N;
		vector<int> table(N, 0);
		vector<int> oper(4, 0);
		for (int i = 0; i < N; i++)
			cin >> table[i];
		for (int i = 0; i < 4; i++)
			cin >> oper[i];
		return make_pair(table, oper);
	}
	
	int calculate(vector<int>& table, vector<char> oper) {
		int result = table[0];
		for (int i = 0; i < oper.size(); i++) {
			if (oper[i] == '+') {
				result += table[i + 1];
			}
			else if (oper[i] == '-') {
				result -= table[i + 1];
			}
			else if (oper[i] == '*') {
				result *= table[i + 1];
			}
			else if (oper[i] == '/') {
				result /= table[i + 1];
			}
		}
		return result;
	}
	
	pair<int,int> insertOperator(vector<int>& table, vector<int>& oper) {
		vector<char> opers;
		// to use next_permutation operators have to be inserted with following order : * + - /
		//since next_permutation act as ascending order.
		// c.f ) ascii number of operands are 42, 43, 45, 47 in order.
		for (int i = 0; i < oper[2]; i++) opers.push_back('*');
		for (int i = 0; i < oper[0]; i++) opers.push_back('+');
		for (int i = 0; i < oper[1]; i++) opers.push_back('-');
		for (int i = 0; i < oper[3]; i++) opers.push_back('/');
		int minimum = INT_MAX;
		int maximum = INT_MIN;
		int cur_value;
		do {
			cur_value = calculate(table, opers);
			minimum = min(minimum, cur_value);
			maximum = max(maximum, cur_value);
			
		} while (next_permutation(opers.begin(), opers.end()));
		return make_pair(maximum, minimum);
	}
	
	void printTable(vector<int>& table, vector<int>& oper) {
		for (int i : table)
			cout << i << " ";
		cout << endl;
		for (int i : oper)
			cout << i << " ";
		cout << endl;
	}
	
	int main() {
		//pair<vector<int>, vector<int>> input = makeTable();
		pair<vector<int>, vector<int>> input = makeTable2();
		pair<int,int> answer= insertOperator(input.first,input.second);
		cout << answer.first << endl << answer.second << endl;
	
		
		return 0;
	}
	
{% endhighlight %}
