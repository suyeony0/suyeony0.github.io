---
layout: post
title: [KAKAO 2018 - The Song Just Before]
date: 2020-5-28
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}

	﻿[152. [KAKAO – 2018 : The Song Just Before]] 
	- WOW! I have barely solved this problem. At first, I used vector to record notes of a song, but in that case, it would be harder to check whether my song is in there than using string.
	- so I changed algorithm. I spent 2 hours or so, I think.
	- see the code.
	#include <string>
	#include<iostream>
	#include <vector>
	#include <sstream>
	#include<algorithm>
	#define min(a,b) a>b ? b:a
	using namespace std;
	
	string songToInt(string song) {
		//cout<<song<<endl;
		string res;
		bool sharp = false;
		for (int i = song.size() - 1; i >= 0; i--) {
			if (song[i] == '#') sharp = true;
			else {
				switch (song[i]) {
				case 'C':
					if (sharp) res += 'C';
					else res += 'c';
					break;
				case 'D':
					if (sharp) res += 'D';
					else res += 'd';
					break;
				case 'E':
					res += 'e';
					break;
				case 'F':
					if (sharp) res += 'F';
					else res += 'f';
					break;
				case 'G':
					if (sharp) res += 'G';
					else res += 'g';
					break;
				case 'A':
					if (sharp) res += 'A';
					else res += 'a';
					break;
				case 'B':
					res += 'b';
					break;
				}
				sharp = false;
			}
		}
		
		//for (int i : res) cout << i << " ";
		//cout << endl;
		reverse(res.begin(), res.end());
		//for (int i : res) cout << i << " ";
		//cout << endl;
	
		return res;
	
	}
	
	bool hasMySong(string a, string b) {
		int i = 0, j = 0;
		bool flag = false;
		int start = 0;
		while (i<a.size()) {
			if (j >= b.size()) {
				flag = true;
				break;
			}
			if (a[i] == b[j]) {
				i++; j++;
			}
			else {
				start++;
				i = start; j = 0;
			}
	
		}
		return flag;
	}
	
	string solution(string m, vector<string> musicinfos) {
		string answer = "";
		// make list
		vector<pair<vector<int>, pair<string, string>>> list; //pair<vector{start,end,length},pair<name,{song : 1,2,12,3...}}>>
		for (int i = 0; i < musicinfos.size(); i++) {
			stringstream ss(musicinfos[i]);
			string start; string end; string name; string song;
			getline(ss, start, ','); getline(ss, end, ','); getline(ss, name, ','); getline(ss, song, '\n');
			string s_time = ""; s_time += start[0]; s_time += start[1];
			string s_temp = ""; s_temp += start[3]; s_temp += start[4];
			int s_input = stoi(s_time) * 60 + stoi(s_temp);
			string e_time = ""; e_time += end[0]; e_time += end[1];
			string e_temp = ""; e_temp += end[3]; e_temp += end[4];
			int e_input = stoi(e_time) * 60 + stoi(e_temp);
			string temp = songToInt(song);
			int play_time = e_input - s_input;
			int temp_size = temp.size();
			if (play_time > temp_size) for (int i = temp_size; i < play_time; i++) temp+=temp[i % temp_size];
			else if (play_time < temp_size) temp = { temp.begin(),next(temp.begin(),play_time) };
			list.push_back(make_pair(vector<int>{s_input, e_input, e_input - s_input - 1, i},
				make_pair(name, temp)));
		}
		
		string my_song = songToInt(m);
		vector<pair<string, vector<int>>> find_list;
		for (int i = 0; i < list.size(); i++) {
			if (list[i].second.second.find(my_song)!=string::npos) {
				find_list.push_back(make_pair(list[i].second.first, vector<int>{list[i].first[3], list[i].first[2]}));
			}
		}
	
		if (find_list.empty()) answer = "(None)";
		else {
			sort(find_list.begin(), find_list.end(), [](pair<string, vector<int>> a, pair<string, vector<int>> b) { return a.second[1] > b.second[1]; });
			vector<pair<string, vector<int>>> temp;	
			int cur = find_list[0].second[1];
			for (int i = 0; i < find_list.size(); i++) {
				if (find_list[i].second[1] == cur) temp.push_back(find_list[i]);
				else break;
			}
			sort(temp.begin(), temp.end(), [](pair<string, vector<int>> a, pair<string, vector<int>> b) { return a.second[0] < b.second[0]; });
			answer = temp[0].first;
		}
	
		return answer;
	}
	
	int main() {
		cout<<solution("ABC", { "12:00,12:14,HELLO,C#DEFGAB","13:00,13:05,WORLD,ABCDEF"});
		return 0;
	}
	
{% endraw %}
