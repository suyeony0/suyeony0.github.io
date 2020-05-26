---
layout: post
title: [791  Custom Sort String]
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}
	﻿[80. [791] Custom Sort String – given sorted array S in a custm way, sort array T so that it is sorted like array S]
	  Intuition is below
	> 1. count each letter in the array T into an unordered_map count.
	> 2. For a character C from S.begin to S.end, if the map count has the character of S, add it to answer as many as count[C]
	> 3. concatenat all the rest charater in the map count.
	class Solution {
	public:
	    string customSortString(string S, string T) {
	        unordered_map<char,int> count;
	        for(char c : T)
	            count[c]++;
	        string answer;
	        for(char c : S){
	            if(count.find(c)!=count.end()){
	                while(count[c]>0){
	                    answer+=c;
	                    count[c]--;
	                }
	            }
	        }
	        unordered_map<char,int>::iterator iter=count.begin();
	        for(;iter!=count.end();iter++){
	            while(iter->second>0){
	                answer+=iter->first;
	                iter->second--;
	            }
	        }
	        return answer;
	    }
	};
	
{% endraw %}
