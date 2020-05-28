---
layout: post
title: [442 Find All Duplicates in an Array]
data: 2020-05-26
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}

	﻿[81. [442] Find All Duplicates in an Array – find numbers which occur twice]
	- If I just have to problem without concerning memory ans time consuming, it is easy.
	- But the point is to use only O(1) memory and O(n) time.
	- Algorithm is below
	> 1. using numbers in array nums as index and negate it. It’s possible since 1<=nums[i]<=n where 0<=i<n.
	> 2. if a number occurs twice, the number’s sign must be + not -.
	class Solution {
	public:
	    vector<int> findDuplicates(vector<int>& nums) {
	        vector<int> answer;
	        for(int i : nums){
	            i=abs(i);
	            nums[i-1]=-nums[i-1];
	            if(nums[i-1]>0) answer.push_back(i);
	        }
	        return answer;
	    }
	};
	
{% endraw %}
