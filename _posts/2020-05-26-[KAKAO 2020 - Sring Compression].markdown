---
layout: post
title: [KAKAO 2020 - Sring Compression]
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

	﻿[119. [Programmers– KAKAO 2020 : String Compression]]
	- we need to be careful when we handle how many substring occurred.
	- I used std::to_string to convert int to string.
	- see the code.
	#include<iostream>
	#include<fstream>
	#include<vector>
	#include<string>
	#define min(a,b) a>b? b:a
	using namespace std;
	string s;
	
	void Input() {
		ifstream in("C:\\Users\\gjsgu\\Desktop\\Algorithm\\test_case\\test_case_for_string_compression.txt");
		if (in.is_open()) cout << "file is opened." << endl;
		in >> s;
	}
	
	int solution(string s) {
		int answer = s.size();
		
		for (int cur_size = 1; cur_size < s.size()/2+1; cur_size++) {
			vector<string> res = { s.substr(0,cur_size) };
			vector<int> num = { 1 };
			string temp;
			int i;
			for (i = cur_size; i + cur_size <= s.size(); i += cur_size) {
				temp = s.substr(i, cur_size);
				if (res.back() == temp) { num[num.size() - 1]++; continue; }
				res.push_back(temp);
				num.push_back(1);
			}
			string compression;
			for (int j = 0; j < res.size(); j++) {
				if (num[j] == 1) compression += res[j];
				else {
					compression += to_string(num[j]);
					compression += res[j];
				}
			}
			for (; i < s.size(); i++)
				compression += s[i];
			answer = min(answer, compression.length());
		}
		return answer;
	}
	
	int main() {
		Input();
		cout << solution(s);
		return 0;
	}
	
