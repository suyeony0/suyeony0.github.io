---
layout: post
title: KMP-Failure Funciton
date: 2020-6-24
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

```cpp

{% raw %}


void FindingFailure() {
	failure.assign(target.size(), 0);
	int j = 0;
	for (int i = 1; i < target.size(); i++) {
		while (j > 0 && target[i] != target[j]) j = failure[j - 1];
		if (target[i] == target[j]) failure[i] = ++j;
	}
}


{% endraw %}
```

