---
layout: post
title: [912 Sort an Array]
date: 2020-5-29
description: txt to markdown
thumbnail: food1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

{% highlight c++ %}

{% raw %}

	﻿[88.  [912] Sort an Array – just sorting an array]
	- I implement merge sort. But the speed was suck! 5.17% beats.
	- so I impelment quick sort as well. But the speed was just 16.25% beats.
	- see the code.
	class Solution {
	public:
	    vector<int> merge(vector<int> nums){
	        if(nums.size()==1) return {nums[0]};
	        vector<int>::iterator mid=next(nums.begin(),nums.size()/2);
	        vector<int> left;
	        vector<int> right;
	        left=merge({nums.begin(),mid});
	        right=merge({mid,nums.end()});
	        vector<int> res;
	        int i=0,j=0;
	        while(i<left.size() && j<right.size()){
	            if(left[i]>right[j]){
	                res.push_back(right[j]);
	                j++;
	                continue;
	            }
	            else{
	                res.push_back(left[i]);
	                i++;
	                continue;
	            }
	        }
	        while(i<left.size()) res.push_back(left[i++]);
	        while(j<right.size()) res.push_back(right[j++]);
	        return res;
	        
	    }
	    void quick(vector<int>& nums, int left, int right){
	        if(left>=right) return;
	        int pivot=left;
	        int i=left+1;
	        int j=right;
	        while(i<j){
	            while(i<j && nums[pivot]>nums[i]) i++;
	            while(i<j && nums[pivot]<nums[j]) j--;
	            if(i>=j) break;
	            int temp=nums[i];
	            nums[i]=nums[j];
	            nums[j]=temp;
	            i++;
	            j--;
	        }
	        if(nums[pivot]>nums[j]){
	            int temp=nums[j];
	            nums[j]=nums[pivot];
	            nums[pivot]=temp;    
	        }
	        quick(nums,left,j-1);
	        quick(nums,j,right);
	    }
	    
	    vector<int> sortArray(vector<int>& nums) {
	        quick(nums,0,nums.size()-1);
	        return nums;
	    }
	};
	
{% endraw %}
{% endhighlight %}

