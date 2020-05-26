---
layout: post
title: [739] Daily Temperatures
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

	﻿[93. [739] Daily Temperatures – determine how many days we have to wait so that a temperatur is wamer than today.]
	- Algorithm is below.
	> 1. make stack and push the last element in the given vector T as a pair with count 0 : (T[i],0)
	> 2. For i where t.end-2 to 0, if stack’s top is less than T[i], pop and accumulate count.
	> 3. if stack is empty, put the T[i] with 0. otherwise put the t[i] with count and put the count into answer[i]
	- see the code.
	class Solution {
	public:
	    vector<int> dailyTemperatures(vector<int>& T) {
	        stack<pair<int,int>> stk;
	        vector<int> answer(T.size(),0);
	        stk.push(make_pair(T.back(),0));
	        
	        for(int i=T.size()-2;i>=0;i--){
	            int count=1;
	            while(!stk.empty() && stk.top().first<=T[i]){
	                count+=stk.top().second;
	                stk.pop();
	            }
	            if(stk.empty()){
	                stk.push(make_pair(T[i],0));
	            }
	            else{
	                stk.push(make_pair(T[i],count));
	                answer[i]=count;
	            }
	            
	        }
	        return answer;
	    }
	};
	
