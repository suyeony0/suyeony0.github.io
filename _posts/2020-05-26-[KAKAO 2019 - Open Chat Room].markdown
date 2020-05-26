---
layout: post
title: [KAKAO 2019 - Open Chat Room]
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

	﻿[126. [Programmers– KAKAO 2019 :Open Chat Room]]
	- it was an easy problem, but I needed to handle complex unordered_map structure. it was quite confusing.
	- see the code.
	
	#include <string>
	#include <vector>
	#include <sstream>
	#include <iostream>
	#include<unordered_map>
	using namespace std;
	
	vector<string> res;
	int index = 0;
	unordered_map<string, pair<string, vector<int>>> table;
	void Tokenize(string s) {
		stringstream ss(s);
		string token;
		getline(ss, token, ' '); string in_out = token;
		getline(ss, token, ' '); string uid = token;
		getline(ss, token, ' '); string name = token;
		if (in_out == "Enter") res.push_back("님이 들어왔습니다.");
		else if (in_out == "Leave") res.push_back("님이 나갔습니다.");
	
		if (table[uid].second.empty()) {
			if(in_out=="Enter") table[uid] = make_pair(name, vector<int>{index++});
			else if(in_out=="Change") table[uid] = make_pair(name, vector<int>{});
		} 
		else {
			if (in_out == "Change") table[uid].first = name;
			else if(in_out=="Enter"){
				table[uid].first = name;
				table[uid].second.push_back(index++);
			}
			else {
				table[uid].second.push_back(index++);
			}
		}
	}
	
	vector<string> solution(vector<string> record) {
		vector<string> answer;
		for (string s : record) Tokenize(s);
		answer.assign(index, "");
		for (unordered_map<string, pair<string, vector<int>>>::iterator iter = table.begin(); iter != table.end(); iter++) {
			for (int i : iter->second.second) {
				answer[i] = iter->second.first + res[i];
			}
		}
		for (string s : answer)
			cout << s << endl;
	
		
		return answer;
	}
	
	int main() {
		solution(vector<string>{ "Enter uid1234 Muzi", "Enter uid4567 Prodo","Change uid4567 Ryan", "Leave uid1234", "Enter uid1234 Prodo"  });
		return 0;
	}
	
