---
layout: post
title: [406] Queue Reconstruction by Height
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

	﻿[89. [406] Queue Reconstruction by Height – standing people by given a height rule]
	- a person have a height and a number which represents the number of person who have a height higher than or equal to the person. by using it, we have sort the given array.
	- this problem was quite difficult. Algorithm didn’t happen in my brain.
	- Algorithm is below.
	> 1. sorting max-height people as a subarray.
	> 2. using the value k that each person has as an index, inserting every person to answer vector.
	> 3. repeating from 1, until the given array people is empty.
	- the speed was 11.52% beats.
	- see the code.
	class Solution {
	public:
	    vector<vector<int>> MaxSubarray(int cur_max_value,vector<vector<int>>& people){
	        vector<vector<int>> cur_max;
	        vector<vector<int>>::iterator iter=next(people.end(),-1);
	        for(;iter!=next(people.begin(),-1);iter--){
	                if(cur_max_value!=iter[0][0]){
	                    iter++;
	                    break;
	                }
	        }
	        if(iter==next(people.begin(),-1)) iter=people.begin();
	        cur_max={iter,people.end()};
	        people.erase(iter,people.end());
	        sort(cur_max.begin(),cur_max.end());
	        return cur_max;
	    }
	    vector<vector<int>> reconstructQueue(vector<vector<int>>& people) {
	        if(people.empty()) return {};
	        sort(people.begin(),people.end());
	        vector<vector<int>> cur_max;
	        vector<vector<int>> answer;
	        int cur_max_value=people[people.size()-1][0];    
	        answer=MaxSubarray(cur_max_value,people);
	        while(!people.empty()){
	            cur_max_value=people[people.size()-1][0];    
	            cur_max=MaxSubarray(cur_max_value,people);
	            for(vector<int> person : cur_max)
	                answer.insert(next(answer.begin(),person[1]),person);
	            cout<<endl;
	        }
	        return answer;
	    }
	};
	
	
