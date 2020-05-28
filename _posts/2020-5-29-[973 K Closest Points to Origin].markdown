---
layout: post
title: [973 K Closest Points to Origin]
date: 2020-5-29
description: txt to markdown
thumbnail: food2.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

```cpp

{% raw %}

	﻿[94. [973] K Closest Points to Origin – calculate Euclidean distance of given coordinates and find K CLosets Points to Origin]
	- I used map. key is Euclidean Distance and value is the coordinates.
	- Since there might be same Euclidean Distance but different coordinates. I should’ve used vector<vector<int>> as a value of the map.
	- the speed was 27.42% beats.
	- I found we can use nth_element function that sort the list till given index is sorted.
	- see the code.
	class Solution {
	public:
	    int Euclidean(int x, int y){
	        return pow(x,2)+pow(y,2);
	    }
	    
	    vector<vector<int>> kClosest(vector<vector<int>>& points, int K) {
	        vector<vector<int>> answer;
	        map<int,vector<vector<int>>> table;
	        for(vector<int> cor: points)
	            table[Euclidean(cor[0],cor[1])].push_back({cor[0],cor[1]});
	        int count=0;
	        map<int,vector<vector<int>>>::iterator iter=table.begin();
	        for(int i=0;count<K;i++){
	            for(int j=0;j<iter->second.size();j++){
	                if(count>=K) break;
	                answer.push_back({iter->second[j][0],iter->second[j][1]});
	                count++;
	            }
	            iter++;
	        }
	        return answer;
	    }
	};
	
{% endraw %}
```

