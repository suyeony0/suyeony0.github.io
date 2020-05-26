---
layout: post
title: [KAKAO 2018 - Sort Timetable]
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

	﻿[155. [KAKAO – 2018 : Sort Filename]] 
	- it was an easy problem, but setting a range of For syntax made a small error. To solve the error, I spent 30 minutes.
	- during revise my algorithm, I made my algorithm worse about time complexity, actually I didn’t need to change set to vector, but I have no idea what’s wrong at the time. 
	- after passing all the test case, it’s quite tiresome returning my alogirhtm to originnal one. 
	- see the code.
	#include <string>
	#include <vector>
	#include <algorithm>
	#include<iostream>
	#include<map>
	#include<set>
	using namespace std;
	
	pair<string,int> getNumber(string s) {
		string head;
		string temp;
		bool flag = true;
		for (int i = 0; i < s.size() && flag; i++) {
			if ('0' <= s[i] && s[i] <= '9') {
				for (int j = i; j <= s.size(); j++) {
					if (j == s.size()) {
						flag = false;
						break;
					}
					else if ('0' <= s[j] && s[j] <= '9') {
						temp += s[j];
					}
					else {
						flag = false;
						break;
					}
				}
			}
			else head += s[i];
		}
		int res = stoi(temp);
		return make_pair(head,res);
	}
	
	vector<string> solution(vector<string> files) {
		vector<string> answer;
		vector<string> temp = files;
		vector<string> name_sort;
		map<string, vector<pair<string,vector<int>>>> map_list;
		//to make lowercase
		for (int i = 0; i < files.size(); i++) {
			transform(temp[i].begin(), temp[i].end(), temp[i].begin(), ::tolower);
			pair<string,int> head_number = getNumber(temp[i]);
			name_sort.push_back(head_number.first);
			//cout << "got name : "<<head_number.first << endl;
			//cout << "got number : " << head_number.second << endl;
			map_list[head_number.first].push_back(make_pair(files[i], vector<int>{i,head_number.second}));
			
		}
		for (map<string, vector<pair<string, vector<int>>>>::iterator iter = map_list.begin(); iter != map_list.end(); iter++) {
			stable_sort(iter->second.begin(), iter->second.end(), [](pair<string, vector<int>> a, pair<string, vector<int>> b) {return a.second[1] < b.second[1]; });
		}
		stable_sort(name_sort.begin(), name_sort.end());
		for (int i = 0; i < name_sort.size(); i++) {
			answer.push_back(map_list[name_sort[i]][0].first);
			map_list[name_sort[i]].erase(map_list[name_sort[i]].begin());
			
		}
		//for (string s : answer)
			//cout << s << " ";
		
	
		return answer;
	}
	
	int main() {
		solution({ "F-5 Freedom Fighter","fa-36", "B-50 Superfortress", "A-10 Thunderbolt II", "F-14 Tomcat" });
		return 0;
	}
	
	
	
	
