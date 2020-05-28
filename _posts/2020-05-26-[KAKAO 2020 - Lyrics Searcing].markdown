---
layout: post
title: [KAKAO 2020 - Lyrics Searcing]
data: 2020-05-26
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}
	﻿[122. [Programmers– KAKAO 2020 : Lyrics Searcing]]
	- I had solved correctly, but time limit exceeded occurred. so I had to change my algorithm for efficiency.
	- below code is before changing the code.
	#include <string>
	#include <vector>
	#include<iostream>
	#include<fstream>
	#include<unordered_map>
	
	using namespace std;
	
	pair<vector<string>, vector<string>> Input() {
		vector<string> words; vector<string> queries;
		ifstream in("C:\\Users\\gjsgu\\Desktop\\Algorithm\\test_case\\test_case_for_lyrics_searching.txt");
		if (in.is_open()) cout << "file is opened." << endl;
		int N;
		in >> N;
		string temp;
		for (int i = 0; i < N; i++) { in >> temp; words.push_back(temp); }
		while (!in.eof()) { in >> temp; queries.push_back(temp); }
		return make_pair(words, queries);
	}
	
	void printInput(vector<string> input) {
		for (string s : input)
			cout << s << " ";
		cout << endl;
	}
	void printAnswer(vector<int> answer) {
		for (int i : answer)
			cout << i << " ";
		cout << endl;
	}
	
	int numOfValidString(vector<string> words, string quer) {
		if (words.empty()) return 0;
		int i;
		int num = 0;
		int size = words[0].size();
		if (quer[0] == '?') {
			for (i = 0; i < quer.size(); i++) if (quer[i] != '?') break;
			int first = i;
			int distance = size - first;
			for (int j = 0; j < words.size(); j++) {
				if (words[j].substr(first, distance) == quer.substr(first, distance)) num++;
			}
		}
		else{
			for(i=quer.size()-1; i>=0;i--) if (quer[i] != '?') break;
			int last = i;
			for (int j = 0; j < words.size(); j++) {
				if (words[j].substr(0, last + 1) == quer.substr(0, last + 1)) num++;
			}
		}
		return num;
	}
	
	vector<int> solution(vector<string> words, vector<string> queries) {
		vector<int> answer;
		unordered_map<int, vector<string>> length;
		for (int i = 0; i < words.size(); i++) length[words[i].size()].push_back(words[i]);
		for (int i = 0; i < queries.size(); i++) answer.push_back(numOfValidString(length[queries[i].size()],queries[i]));
		return answer;
	}
	int main() {
		pair<vector<string>, vector<string>> input = Input();
		vector<string> words = input.first;
		vector<string> queries = input.second;
		solution(words, queries);
		return 0;
	}
	
	-  I had to use trie structure to get marked at efficiency test.
	- trie structure is often used when we handle string search.
	- trie acts like a dictionary. so it has functions like insert, find.
	- see the below code. I spent almost 4~5 hours.
	#include <string>
	#include <vector>
	#include<iostream>
	#include<fstream>
	#include<unordered_map>
	using namespace std;
	
	pair<vector<string>, vector<string>> Input() {
		vector<string> words; vector<string> queries;
		ifstream in("C:\\Users\\gjsgu\\Desktop\\Algorithm\\test_case\\test_case_for_lyrics_searching.txt");
		if (in.is_open()) cout << "file is opened." << endl;
		int N;
		in >> N; 
		string temp;
		for (int i = 0; i < N; i++) { in >> temp; words.push_back(temp); }
		while (!in.eof()) { in >> temp; queries.push_back(temp); }
		return make_pair(words, queries);
	}
	
	void printInput(vector<string> input) {
		for (string s : input)
			cout << s << " ";
		cout << endl;
	}
	void printAnswer(vector<int> answer) {
		for (int i : answer)
			cout << i << " ";
		cout << endl;
	}
	// we have to use trie tree to record words and reversed words.
	// we consider trie structure as a dictionary.
	class Trie {
	
	private:
		Trie* children[26];
		bool terminal;
		unordered_map<int, int> length;
	public:
		Trie() {
			fill(children, children + 26, nullptr);
			this->terminal = false;
		}
		~Trie() {
			for (int i = 0; i < 26; i++) if(children[i]!=NULL) delete children[i];
		}
	
		void insert(const char* s,int size) {
			if (*s =='\0') {
				terminal = true;
				return;
			}
			length[size] += 1;
			if (children[*s - 'a'] == NULL)
				children[*s - 'a'] = new Trie;
			children[*s - 'a']->insert(s+1, size);
		}
	
		int find(const char* s,int size) {
			if (*s == '\0') return terminal;
			int count = 0;
			if (*s == '?') count += length[size];
			else {
				if (children[*s - 'a'] == NULL) return 0;
				count=children[*s - 'a']->find(s+1, size);
			}
			return count;
		}
	};
	
	
	vector<int> solution(vector<string> words, vector<string> queries) {
		vector<int> answer;
		Trie* prefix = new Trie;
		Trie* suffix = new Trie;
		int match;
		for (int i = 0; i < words.size(); i++) {
			prefix->insert(&words[i][0], words[i].size());
			string temp = { words[i].rbegin(),words[i].rend() };
			suffix->insert(&temp[0], temp.size());
		}
		for (int i = 0; i < queries.size(); i++) {
			if (queries[i][0] == '?') {
				string temp = { queries[i].rbegin(), queries[i].rend() };
				answer.push_back(suffix->find(&temp[0], temp.size()));
			}
			else answer.push_back(prefix->find(&queries[i][0], queries[i].size()));
		}
		return answer;
	}
	int main() {
		pair<vector<string>, vector<string>> input = Input();
		vector<string> words = input.first;
		vector<string> queries = input.second;
		printAnswer(solution(words, queries));
		
		return 0;
	}
	
	
{% endraw %}
