---
layout: post
title: [1343 Number of Sub-arrays of Size K and Average Greater than or Equal to Threshold]
date: 2020-5-29
description: txt to markdown
thumbnail: city2.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

{% highlight c++ %}

{% raw %}

	﻿[82. [1343] Number of Sub-arrays of Size K and Average Greater than or Equal to Threshold – find the number of sub-array of size K that has an average greater than or equal to given threshold]
	- Algorithm is below
	> 1. From first of the given array, add K-1 elements. => cur_sum
	> 2. iteratively, make cur_sum has K elements. if K’s average is valid about the given condition. then add 1 to answer
	> subtract arr[i-k+1] from cur_sum and add arr[[i] to cur]sum and repeat the algorithm from 2.
	class Solution {
	public:
	    int numOfSubarrays(vector<int>& arr, int k, int threshold) {
	        int cur_sum=0;
	        int answer=0;
	        for(int i=0;i<k-1;i++)
	            cur_sum+=arr[i];
	        for(int i=k-1;i<arr.size();i++){
	            cur_sum+=arr[i];
	            if(cur_sum/k >= threshold) answer++;
	            cur_sum-=arr[i-k+1];
	        }
	        return answer;
	    }
	};
	
{% endraw %}
{% endhighlight %}

