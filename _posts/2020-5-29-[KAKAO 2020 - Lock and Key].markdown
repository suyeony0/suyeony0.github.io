---
layout: post
title: [KAKAO 2020 - Lock and Key]
date: 2020-5-29
description: txt to markdown
thumbnail: breakfast-orange-lemon-oranges-large.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

{% highlight c++ %}
```cpp
	﻿[121. [Programmers– KAKAO 2020 : Lock and Key]]
	- implementing slicing using C++ is quite hard for me.
	- I made slicing to determine whether the given key is valid or not. 
	- see the code.
	#include <string>
	#include <vector>
	#include<iostream>
	
	using namespace std;
	
	
	vector<vector<int>> makeTable(int k,int l,vector<vector<int>> lock) {
		vector<vector<int>> table(k * 2 - 2 + l, vector<int>(k * 2 - 2 + l, 2));
		for (int i = k - 1; i < k - 1 + l; i++) {
			for (int j = k - 1; j < k - 1 + l; j++) {
				table[i][j] = lock[i - (k - 1)][j - (k - 1)];
			}
		}
		return table;
	}
	
	vector<vector<int>> rotateKey(vector<vector<int>> key) {
		int k = key.size();
		vector<vector<int>> res(k, vector<int>(k));
		for (int i = 0; i < k; i++) {
			for (int j = 0; j < k; j++) {
				res[i][j] = key[k-j-1][i];
			}
		}
		return res;
	}
	
	void printKey(vector<vector<int>> key) {
		for (vector<int> row : key) {
			for (int i : row) {
				cout << i << " ";
			}
			cout << endl;
		}
		cout << endl;
	}
	void printTable(vector<vector<int>> table) {
		for (vector<int> row : table) {
			for (int i : row) {
				cout << i << " ";
			}
			cout << endl;
		}
		cout << endl;
	}
	bool isValid(vector<vector<int>> key, vector<vector<int>> table,vector<vector<int>> lock){
		int k = key.size(); int t = table.size();
		for (int i = 0; i < t-k+1; i++) {
			for (int j = 0; j < t-k+1; j++) {
				vector<vector<int>> temp_lock = table;
				bool flag = true;
				for (int a = 0; a < k; a++) {
					for (int b = 0; b < k; b++) {
						if (table[i + a][j + b] == 2) { temp_lock[i+a][j+b] = 1; continue; }
						else if ((table[i + a][j + b] == 0 && key[a][b] == 1) || (table[i + a][j + b] == 1 && key[a][b] == 0)) {
							temp_lock[i+a][j+b] = 1;
							continue;
						} 
						else { flag = false; break;}
					}
				}
				if (flag) {
					bool flag2 = true;
					for (int i = k - 1; i < t - k + 1;i++) {
						for (int j = k - 1; j < t - k + 1; j++) {
							if (temp_lock[i][j] == 0) { flag2 = false; break; }
						}
					}
					if (flag2) {
						return true;
					} 
				} 
			}
		}
		return false;
	}
	
	bool solution(vector<vector<int>> key, vector<vector<int>> lock) {
		bool answer = true;
		int k = key.size(); int l = lock.size();
		vector<vector<int>> table = makeTable(k, l,lock);
		//rotate the given key at most 3 times.
		if (isValid(key, table,lock)) return true;
		for (int i = 0; i < 3; i++) {
			key=rotateKey(key);
			if (isValid(key, table,lock)) return true;
		}
		return false;
	}
	
	int main() {
		vector<vector<int>> key = { {0,0},{1,0} };
		vector<vector<int>> lock = { {0,0},{0,0} };
		cout<<solution(key, lock);
		return 0;
	}
	
	
```
{% endhighlight %}
