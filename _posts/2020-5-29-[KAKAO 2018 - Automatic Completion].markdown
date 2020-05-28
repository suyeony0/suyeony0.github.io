---
layout: post
title: [KAKAO 2018 - Automatic Completion]
date: 2020-5-29
description: txt to markdown
thumbnail: breakfast-orange-lemon-oranges-large.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

```cpp
	﻿[154. [KAKAO – 2018 : Automatic Completion]] 
	- it was a string parisng problem. so I used Trie tree to make dictionary.
	- when I insert a string into the dictionary, I recorded how many word can be parsed from the node with a name has_word.
	- the concept was easy, but making Trie tree was quite naughty :).
	- see the code.
	#include <string>
	#include <vector>
	#include<iostream>
	using namespace std;
	
	class Trie {
	public:
		vector<Trie*> dict; // a : 0 - z : 25
		bool terminal = false;
		int has_word = 0;
		Trie() {
			dict.assign(26, nullptr);
		}
		~Trie() {
			for (Trie* remove : dict) if (remove != nullptr) remove = nullptr;
		}
		void insert(const char* c) {
			if (*c == '\0') {
				//has_word++;
				terminal = true;
				return;
			}
			int index = *c - 'a';
			
			if (dict[index] == nullptr) dict[index] = new Trie();
			dict[index]->has_word++;
			dict[index]->insert(c + 1);
	
		}
		bool find(const char* c) {
			if (terminal && *c == '\0') return true;
			else if (*c == '\0') return false;
			int index = *c - 'a';
			if (dict[index] != nullptr) {
				return dict[index]->find(c + 1);
			}
			else return false;
	
		}
		int length(const char* c,int count) {
			if (has_word == 1) return count;
			else if (has_word > 1 && *c == '\0') return count;
			int index = *c - 'a';
			return dict[index]->length(c + 1, count + 1);
		}
	};
	
	
	int solution(vector<string> words) {
		int answer = 0;
		Trie* dict = new Trie();
		//make dictionary
		for (string s : words) {
			const char* c = s.c_str(); // to make string to const char*, we can use string::str.c_str();
			dict->insert(c);
		}
		
		for (string s : words) {
			const char* c = s.c_str();
			int temp = dict->length(c, 0);
			//cout << "length : "<<temp << endl;
			answer += temp;
		}
			
		
		return answer;
	}
	
	int main() {
		cout<<solution(vector<string>{ "abc", "def", "ghi", "jklm" });
		return 0;
	}
	
	
```
