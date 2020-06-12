---
layout: post
title: [SAMSUNG SW - Horizontal Vertical Puzzle]
date: 2020-6-12
description: txt to markdown
thumbnail: food2.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

ï»?214. SAMSUNG SW : Horizontal Vertical Puzzle]
- it was a permuation problem.
- At first, I didn?™t understand what the problem required. so I spent 5 minutes or so to understand it.
- I used DFS for permutation.
- To check whether the puzzle table is valid, for each word in the table, I compared it to the given words.
- if it exists, erase it, if not, return false and keep permutating.
- I spent 20 minutes and 49 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<algorithm>
using namespace std;

vector<string> words(6,"");
vector<string> table(3, "");
vector<int> chosen;
vector<bool> visit(6, false);
bool flag = false;

bool isPuzzle() {
	vector<string> chosen_words;
	for (int i = 0; i < 3; i++) {
		table[i] = words[chosen[i]];
		chosen_words.emplace_back(table[i]);
	}
	for (int j = 0; j < 3; j++) {
		string temp = "";
		for (int i = 0; i < 3; i++) {
			temp += table[i][j];
		}
		chosen_words.emplace_back(temp);
	}
	vector<string> temp_words = words;
	for (string cur : chosen_words) {
		if (find(temp_words.begin(), temp_words.end(), cur) != temp_words.end()) {
			temp_words.erase(find(temp_words.begin(), temp_words.end(), cur));
		}
		else return false;
	}
	return true;
}

void Combination(int cnt) {
	if (cnt == 3) {
		if (isPuzzle()) {
			flag = true;
			return;
		}
		return;
	}

	for (int i = 0; i < 6; i++) {
		if (visit[i] == false) {
			visit[i] = true;
			chosen.emplace_back(i);
			Combination(cnt + 1);
			if (flag) return;
			chosen.pop_back();
			visit[i] = false;
		}
	}

}

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	for (int i = 0; i < 6; i++) cin >> words[i];

	//algorithm part
	Combination(0);
	if (!flag) cout << 0;
	else {
		for (string cur : table) {
			cout << cur << endl;
		}
	}
	return 0;

}

{% endraw %}
```

