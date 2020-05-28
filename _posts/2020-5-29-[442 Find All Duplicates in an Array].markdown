---
layout: post
title: [442 Find All Duplicates in an Array]
date: 2020-5-29
description: txt to markdown
thumbnail: building1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

{% highlight c++ %}

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
	
{% endhighlight %}

