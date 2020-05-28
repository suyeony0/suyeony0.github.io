---
layout: post
title: [Samsung SW - Brainfuck Interpreter]
date: 2020-5-28
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}

	﻿[174. [SAMSUNG - SW : Brainfuck Interpreter]
	- like the name, it was a fucking interpreter.
	- they gave an ambiguous rule about infinite loop. because of that, I struggled to solve it hard.
	- see the code.
	#include<iostream>
	#include<vector>
	#include<map>
	#define MAX_VALUE 256
	using namespace std;
	
	map<int, int> parenthesis_left;
	map<int, int> parenthesis_right;
	pair<int,int> loop;
	bool flag = false;
	void getPair(string brainfuck) {
		vector<int> temp;
		for (int i = 0; i < brainfuck.size(); i++) {
			if (brainfuck[i] == '[') {
				temp.emplace_back(i);
			}
			else if (brainfuck[i] == ']') {
				parenthesis_left[temp.back()] = i;
				parenthesis_right[i] = temp.back();
				temp.pop_back();
			}
		}
	}
	
	void operate(vector<int>& memory,string& brainfuck,int& order_index,int& pointer,string& input,int& input_index) {
		char order = brainfuck[order_index];
	
		switch (order) {
		case '-':
			memory[pointer] -= 1;
			if (memory[pointer] < 0) memory[pointer] = 255;
			order_index++;
			break;
		case '+':
			memory[pointer] = (memory[pointer] + 1) % 256;
			order_index++;
			break;
		case '<':
			pointer--;
			if (pointer < 0) pointer = memory.size() - 1;
			order_index++;
			break;
		case '>':
			pointer = (pointer + 1) % memory.size();
			order_index++;
			break;
		case '[':
			if (memory[pointer] == 0) {
				order_index = parenthesis_left[order_index];
				break;
			}
			order_index++;
			break;
		case ']':
			loop.first = parenthesis_right[order_index];
			loop.second = order_index;
			if (memory[pointer] != 0) {
				order_index = parenthesis_right[order_index];
				break;
			}
			order_index++;
			break;
		case '.':
			order_index++;
			break;
		case ',':
			int temp_input;
			if (input_index < input.size()) {
				temp_input = (int)input[input_index];
				memory[pointer] = temp_input;
			}
			else memory[pointer] = 255;
			input_index++;
			order_index++;
			break;
		}
	}
	
	
	int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL); cout.tie(NULL);
	
		int t;  cin >> t;
	
		//for each test case
		int m, c, i;
		string brainfuck;
		string input;
		vector<int> memory;
		for (int qq = 0; qq < t; qq++) {
			//get input
			cin >> m >> c >> i>> brainfuck>> input;
			memory.assign(m, 0);
	
			//algoirhtm part
			getPair(brainfuck); //get parenthesis pair
			int order_index = 0;
			int pointer = 0;
			int cnt = 0;
			int input_index = 0;
			flag = true;
			loop = make_pair(-1, -1);
			int max_order_index = 0;
			while (cnt< 50000000) {
				if (order_index>=c) {
					cout << "Terminates" << endl;
					flag = false;
					break;
				}
				operate(memory,brainfuck, order_index,pointer, input,input_index);
				cnt++;
				max_order_index = order_index > max_order_index ? order_index : max_order_index;
			}
			if (flag) {
				cout << "Loops " << parenthesis_right[max_order_index] << " " << max_order_index << endl;
			}
			//map clear
			parenthesis_left.clear();
			parenthesis_right.clear();
		}
	
		return 0;
	}
	
	
{% endraw %}
