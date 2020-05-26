---
layout: post
title: [969  Pancake Sorting]
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}
	﻿[76. [969] Pancake Sorting – find the order of indexs to reverse the given vector from vector.begin() so that the vector is sorted]
	- the flip begin from A[0]. so we have to sort from A.end() descendantly.
	- at first, we have to find the largest elements that can be found using A.length.
	- then flip from start to the largest elements index so that the largest elements come to first index.
	- and reverse all A so as to put the largest elements to last index. and so on.
	class Solution {
	public:
	    vector<int> pancakeSort(vector<int>& A) {
	        int largest=A.size();
	        vector<int>::iterator last=A.end();
	        vector<int>::iterator cur;
	        vector<int> answer;
	        for(int i=0; i<A.size()-1; i++){
	            cur=find(A.begin(),last,largest);
	            cur++;
	            answer.push_back(distance(A.begin(),cur));
	            answer.push_back(distance(A.begin(),last));
	            reverse(A.begin(),cur);
	            reverse(A.begin(),last);
	            largest--;
	            advance(last,-1);
	        }
	        return answer;
	    }
	};
	
{% endraw %}
