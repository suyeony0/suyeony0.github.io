---
layout: post
title: [46] Permutations
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

	﻿[100. [46] Permutations – find all the possible permutation]
	- The function next_permutation return true if there is next permutation, and revise given vector to next 
	permutation. but the function can’t handle negative value.
	- So I used DFS. Actually, it’s not such a DFS, but I think it is :).
	- Algorithm is below.
	> 1. from 0 to nums.size(), input the value into new vector
	> 2. remove the value, and repeat from 1.
	> 3. if all the value in the given vector nums is removed, push the vector cur into answer vector
	- The speed was 61.80% beats.
	- see the code.
	class Solution {
	public:
	    void dfs(vector<int> nums,vector<vector<int>>& answer,vector<int> cur,int start){
	        nums.erase(next(nums.begin(),start));
	        if(nums.size()==0){
	            answer.push_back(cur);
	            return;
	        }
	        
	        for(int i=0;i<nums.size();i++){
	            vector<int> temp=cur;
	            temp.push_back(nums[i]);
	            dfs(nums,answer,temp,i);
	        }
	    }
	    vector<vector<int>> permute(vector<int>& nums) {
	vector<vector<int>> answer;
	        for(int i=0;i<nums.size();i++){
	            vector<int> cur;
	            cur.push_back(nums[i]);
	            dfs(nums,answer,cur,i);
	        }
	        return answer;
	    }
	};
	
	
