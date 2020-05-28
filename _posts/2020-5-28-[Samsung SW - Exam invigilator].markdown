---
layout: post
title: [Samsung SW - Exam invigilator]
data: 2020-05-26
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}

	﻿[104. [BACKJOON – SAMSUNG SW : Exam Invigilator]]
	- this exam’s trap is the range of number. since tue maximum number of people is 1,000,000 * 1,000,000 and the minimum number of that an invigilator can handle is 1.
	- so we have to use long long (int) for the answer and double for the table having the number of people in a class.
	- see the code.
	#include<iostream>
	#include<fstream>
	#include<vector>
	#include<cmath> // for the function ceil
	
	using namespace std;
	
	pair<vector<double>,int> makeTable() {
		std::ifstream in("C:\\Users\\gjsgu\\Desktop\\Algorithm\\test_case\\test_case_for_exam_invigilator.txt");
		int N;
		if (in.is_open()) {
			cout << "file is opened." << endl;
			in >> N;
		}
		vector<double> table(N, 0);
		int people;
		for (int i = 0; i < N; i++) {
			in >> people;
			table[i] = people;
		}
		int B, C;
		in >> B; in >> C;
		for (int i = 0; i < N; i++) table[i] -= B;
		return make_pair(table, C);
	}
	pair<vector<double>, int> makeTable2() {
		int N;
		cin >> N;
		vector<double> table(N, 0);
		int people;
		for (int i = 0; i < N; i++) {
			cin >> people;
			table[i] = people;
		}
		int B, C;
		cin >> B; cin >> C;
		for (int i = 0; i < N; i++) table[i] -= B;
		return make_pair(table, C);
	}
	
	void printTable(vector<double> table) {
		for (double i : table)
			cout << i << " ";
		cout << endl;
	}
	
	unsigned long long findMinimum(vector<double> table, int C) {
		unsigned long long minimum = table.size();
		for (int i = 0; i < table.size(); i++) {
			if (table[i] <= 0) continue;
			minimum += ceil(table[i] / C);
		}
		return minimum;
	}
	
	int main() {
		//pair<vector<float>,int> input = makeTable();
		pair<vector<double>, int> input = makeTable2();
		vector<double> table = input.first;
		int C = input.second;
		//printTable(table);
		unsigned long long answer=findMinimum(table, C); //since 1,000,000 * 1,000,000 is the maximum number of student and the minimum number of that an invigiltor can handle is 1. 
		cout << answer;
		return 0;
	}
	
	
{% endraw %}
