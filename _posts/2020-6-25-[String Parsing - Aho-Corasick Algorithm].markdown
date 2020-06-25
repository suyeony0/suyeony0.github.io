---
layout: post
title: [String Parsing - Aho-Corasick Algorithm]
date: 2020-6-25
description: txt to markdown
thumbnail: city2.jpg
categories: Algorithm

# Information for the author block
author : Loui
---


```cpp

{% raw %}

#include<iostream>
#include<queue>
#include<algorithm>

using namespace std;

class Trie {
public: 
	vector<Trie*> go; // let's assume that there are only lower case letters.
	Trie* fail; //this is failure function.

	bool output;

	Trie() {
		go.assign(26, nullptr);
		output = false;
	}
	~Trie() {
		for (int i = 0; i < 26; i++) if (go[i]) delete go[i];
	}
	
	void insert(const char *key) {
		if (*key == '\0') { //when we meet end of string
			output = true;
			return;
		}
		int next = *key - 'a'; //next character's index
		if (!go[next]) { // if we don't have such node
			go[next] = new Trie; //create it
		}
		go[next]->insert(key + 1);
	}

};

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	int N, M;
	string words;
	Trie* root = new Trie;
	cin >> N; //number of string
	for (int i = 0; i < N; i++) {
		cin >> words;
		root->insert(words.c_str); // to use pointer, we have to convert c++ string to c style string.
	}

	//Making Failure function
	queue<Trie*> que;
	root->fail = root;
	que.push(root);
	while (!que.empty()) {
		Trie* cur = que.front();
		que.pop();

		for (int i = 0; i < 26; i++) {
			Trie* next = cur->go[i];
			if (!next) continue; //when next node doesn't exist

			if (cur == root) next->fail = root;
			else {
				Trie* dest = cur->fail;
				// finding a closest ancient to reference failure function.
				while (dest != root && !dest->go[i])
					dest = dest->fail;

				// failure(px) = go(failure(p),x)
				if (dest->go[i]) dest = dest->go[i];
				next->fail = dest;
			}
			// when failure(x)=y, check output(x) include output(y)
			if (next->fail->output) next->output = true;

			que.push(next);
		}
	
	}
	
	// get words to find
	cin >> M; //number of words;
	for (int i = 0; i < M; i++) {
		cin >> words;
		Trie* cur = root;
		bool result = false;
		for (char c : words) {
			int next = c - 'a';
			// if we can't go further, follow failure function.
			while (cur != root && !cur->go[next])
				cur = cur->fail;
			// if there is go[i], move, but if cur is root, it might have no go[next], so we sholud check.
			if (cur->go[i]) cur = cur->go[next];
			// if we find ouput, result is true
			if (cur->output) {
				result = true;
				break;
			}
		}
		if (result) cout << "YES" << endl;
		else cout << "NO" << endl;
	}

	delete root;
}

{% endraw %}
```

