---
layout: post
title: [KAKAO 2019 - Candidate Key]
date: 2020-5-29
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% highlight c++ %}
```cpp
	﻿[128. [Programmers– KAKAO 2019 :Candidate Key]]
	- it was fxxkcing difficult for me. Indeed, it was not that difficult. but I spent so much time.
	- since I had to make all the possible combination first. it was okay even though I spent 1 hour or so.
	- But to satisfy minimality, I had to remove duplicate keys, it took a lot of time.
	- HOWEVER!!! the main problem that took so much time was!!!! I’ve read problem in a wrong way…
	- I thought the problem want me to return maximum size of a possible cadidate key. Sadly, it wans’t.
	- I just had to return the number of cadidate keys which is valid….
	- oh my poor hand, brain, time… :(
	- by the way, I used bitset to remove duplicates and BFS to make all the possible combination. when I made BFS, the queue structure was quite complex, since there were quite many condition.
	- see the code.
	#include <string>
	#include <vector>
	#include<iostream>
	#include<queue>
	#include<unordered_set>
	#include<bitset>
	#define max(a,b) a>b ? a : b
	using namespace std;
	int n; int m;
	
	vector<vector<int>> valid;
	vector<vector<int>> all;
	
	
	bool isValid(vector<string> temp) {
		unordered_set<string> check;
		for (int i = 0; i < temp.size(); i++)
			check.insert(temp[i]);
		//cout << "size : " << check.size() << endl;
		if (check.size() == n) return true;
		return false;
	}
	
	void Combination(vector<vector<string>> table) {
		queue<pair<vector<string>,pair<vector<int>,int>>> que;
		for (int i = 0; i < table.size(); i++) {
			que.push(make_pair(table[i], make_pair(vector<int>{ i },i+1)));
		}
	
		while (!que.empty()) {
			vector<string> temp = que.front().first;
			vector<int> indice = que.front().second.first;
			int start = que.front().second.second;
			que.pop();
			
			/*cout << "indice : ";
			for (int i : indice)
				cout << i << " ";
			cout << endl;
			for (string s : temp) 
				cout << s << " ";
			cout << endl;*/
	
			if (isValid(temp)) valid.push_back(indice);
			all.push_back(indice);
	
			for (int i = start; i < m; i++) {
				vector<string> temp_table = temp;
				vector<int> temp_indice = indice;
				for (int j = 0; j < n; j++) {
					temp_table[j] +=" "+ table[i][j];
				}
				temp_indice.push_back(i);
				que.push(make_pair(temp_table, make_pair(temp_indice, i + 1)));
			}
		}
	
	}
	
	void printValid() {
		for (vector<int> row : valid) {
			for (int i : row) {
				cout << i << " ";
			}
			cout << endl;
		}
	}
	void printAll() {
		for (vector<int> row : all) {
			for (int i : row) {
				cout << i << " ";
			}
			cout << endl;
		}
	}
	
	
	void Minimalize() {
		vector<bitset<20>> bits(valid.size());
		for (int i = 0; i < valid.size(); i++) {
			for (int j = 0; j < valid[i].size(); j++) {
				bits[i][valid[i][j]] = 1;
			}
		}
		for (int i = 0; i < bits.size();i++) {
			bitset<20> cur_bit = bits[i];
			for (int j = i + 1; j < bits.size();) {
				bitset<20> temp = cur_bit & bits[j];
				if (temp == cur_bit) {
					valid.erase(next(valid.begin(), j));
					bits.erase(next(bits.begin(), j));
				}
				else j++;
			}
		}
	}
	
	int solution(vector<vector<string>> relation) {
		n = relation.size();
		m = relation[0].size();
		vector<vector<string>> table(m);
		for (int j = 0; j < m; j++) {
			vector<string> temp;
			for (int i = 0; i < n; i++) {
				temp.push_back(relation[i][j]);
			}
			table[j] = temp;
		}
		Combination(table);
		Minimalize();
		int answer = 0;
		return valid.size();
	}
	
	int main() {
		
		return 0;
	}
	
```
{% endhighlight %}
