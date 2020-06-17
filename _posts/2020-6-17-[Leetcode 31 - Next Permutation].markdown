---
layout: post
title: [Leetcode 31 - Next Permutation]
date: 2020-6-17
description: txt to markdown
thumbnail: building1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

﻿[220. Leetcode 31 : Next Permutation]
- it was a quite difficult problem. Since I had to satisfy memory restriction.
- I was able to use only a given vector with extra constant memory.
- Logic is below.
- First, Finding first element from last index in the given vector that is lower than its right elements.
- Second, Finding the smallest element just right after the first element that is greater than the first element.
- Third, Swap the smallest element with the first element.
- Fourth, sort the range, I means, from just right after first element to end of the vector.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#include<algorithm>
#define max(a,b) a>b? a:b
using namespace std;

bool flag = false;
int main() {
	
	vector<int> table = { 6,7,5,3,5,6,2,9,1,2,7,0,9 }; // 1234 1243 1324 1342 1423 1432 
	// we can guess that a next number is always greater than a current number.
	int changed_index = 0;
	int right_index = 0;
	//To check it is last or not.
	int i;
	int after_num = 987654321;
	for ( i = 0; i < table.size()-1; i++) if (table[i] < table[i + 1]) break;
	if (i == table.size()-1) reverse(table.begin(), table.end());
	else { 
		// it must be changed from last index.
		for (int i = table.size()-1; i >= 0; i--) {
			for (int j = i + 1; j < table.size(); j++) {
				if (table[i] < table[j]) {
					changed_index = i;
					flag = true;
					if (table[j] < after_num) {
						after_num = table[j];
						right_index = j;
					}
					//4 1 3 2  // 3 4 1 2 // 2 4 3 1 <<= this one have to occur.
				}
			}
			if (flag) break; // if something is changed by above if syntax, we don't need to go further.
		}
		swap(table[changed_index], table[right_index]);
		sort(table.begin() + 1 + changed_index , table.end());
	}
	for (int i : table) cout << i << " ";
	
	return 0;
}

{% endraw %}
```

