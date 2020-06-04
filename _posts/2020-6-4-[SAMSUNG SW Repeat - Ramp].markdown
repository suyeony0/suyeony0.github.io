---
layout: post
title: [SAMSUNG SW Repeat - Ramp]
date: 2020-6-4
description: txt to markdown
thumbnail: city2.jpg
categories: SAMSUNG_SW

# Information for the author block
author : Loui
---

[12. SAMSUNG SW : Ramp]
- it was a simulation problem. but there were lots of edge condition. so I had to be careful.
- when I met higher land than current, I should¡¯ve checked previos lands I passed with how many sequencial plain lands had been. 
- when I met lower land than current, I sholud¡¯ve check post lands I would pass with how moany sequencial plain lands would be.
- I spent 30 minutes.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>

using namespace std;

int N, L;
vector<vector<int>> table;

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	cin >> N >> L;
	table.assign(N, vector<int>(N, 0));
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < N; j++) {
			cin >> table[i][j];
		}
	}

	//algorithm part
	int answer = 0;

	//horizontal
	for (int i = 0; i < N; i++) {
		int prev = table[i][0];
		int seq = 0;
		bool flag = true;
		for (int j = 0; j < N; j++) {
			if (abs(prev - table[i][j]) >= 2) {
				flag = false;
				break; //when the height difference is greater than 1
			} 
			else if (prev == table[i][j]) {
				prev = table[i][j];
				seq += 1;
			}
			else if (prev < table[i][j]) {
				if (seq < L) {
					flag = false;
					break; // when we can't put a ramp
				} 
				prev = table[i][j];
				seq = 1;
				continue;
			}
			else if (prev > table[i][j]) {
				// in this case, we have to check futher shell whether we can put a ramp or not.
				if (j + L > N) { // index out of range
					flag = false; 
					break;
				}
				for (int k = j+1; k < j + L; k++) { //when we can't put a ramp since there is no enough sequence shell.
					if (table[i][j] != table[i][k]) {
						flag = false;
						break;
					}
				}
				if (!flag) break; //for just above "for" syntax
				seq = 0;
				j = j + L - 1;
				prev = table[i][j];
			}
		}
		if (flag) {
			//cout << "i : "<< i << endl;
			answer += 1;
		} 
	}

	//vertical
	for (int j = 0; j < N; j++) {
		int prev = table[0][j];
		int seq = 0;
		bool flag = true;
		for (int i = 0; i < N; i++) {
			if (abs(prev - table[i][j]) >= 2) {
				flag = false;
				break; //when the height difference is greater than 1
			}
			else if (prev == table[i][j]) {
				prev = table[i][j];
				seq += 1;
			}
			else if (prev < table[i][j]) {
				if (seq < L) {
					flag = false;
					break; // when we can't put a ramp
				}
				prev = table[i][j];
				seq = 1;
				continue;
			}
			else if (prev > table[i][j]) {
				// in this case, we have to check futher shell whether we can put a ramp or not.
				if (i + L > N) { // index out of range
					flag = false;
					break;
				}
				for (int k = i + 1; k < i + L; k++) { //when we can't put a ramp since there is no enough sequence shell.
					if (table[i][j] != table[k][j]) {
						flag = false;
						break;
					}
				}
				if (!flag) break; //for just above "for" syntax
				seq = 0;
				i = i + L - 1;
				prev = table[i][j];
			}
		}
		if (flag) {
			//cout << "j : " << j << endl;
			answer += 1;
		} 
	}
	cout << answer;
	return 0;
}

{% endraw %}
```

