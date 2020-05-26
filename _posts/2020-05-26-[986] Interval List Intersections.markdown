---
layout: post
title: {% raw %}[986] Interval List Intersections{% endraw %}
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}
	﻿[986] Interval List Intersections – Given two sorted closed interval, return the intersection of these two lists.]
	- At first try, I use map to record interval of two lists into one store with using vector in the map for checking every interval’s end.
	- I think I just need O(total interval of A and B + map.size()). But time limit exceeded occurs.
	class Solution {
	public:
	    vector<vector<int>> intervalIntersection(vector<vector<int>>& A, vector<vector<int>>& B) {
	        map<int,vector<int>> inter;
	        vector<vector<int>> answer;
	        int i;
	        for(vector<int> ele : A){
	            for(i=ele[0];i<ele[1];i++){
	                inter[i]={1,0,0};
	            }
	            inter[i]={1,1,0};
	        }
	        for(vector<int> ele : B){
	            for(i=ele[0];i<=ele[1];i++){
	                if(inter[i].empty()) inter[i]={1,0,0};
	                else inter[i][0]++;
	            }
	            inter[i-1][2]=1;
	        }
	        map<int,vector<int>>::iterator iter=inter.begin();
	        int left=0;
	        for(;iter!=inter.end();iter++){
	            if(iter->second[0]==2){
	                left=iter->first;
	                while(iter->second[0]==2){
	                    if(iter->second[1]==1 || iter->second[2]==1)
	                        break;
	                    else iter++;
	                }
	                answer.push_back({left,iter->first});
	            }
	        }
	        return answer;
	    }
	};
	
	- I guess the reason why the time limit exceed occurs is because I search all the element in each intervals. So I should figure out how to solve this problem by just using left and right limit of each intervals only.
	- the final answer is that if A[i][1] is less than B[j][0], i++, vice versa j++.
	- after that we can find overlapping range by two lists. From there, we just determine which one is left and right limit.
	- see the code.
	class Solution {
	public:
	    vector<vector<int>> intervalIntersection(vector<vector<int>>& A, vector<vector<int>>& B) {
	        vector<vector<int>> answer;
	        for(int i=0, j=0;i<A.size() && j<B.size();){
	            if(A[i][1]<B[j][0]) i++;
	            else if(A[i][0]>B[j][1]) j++;
	            else{
	                answer.push_back({max(A[i][0],B[j][0]),min(A[i][1],B[j][1])});
	                if(A[i][1]<B[j][1]) i++;
	                else j++;
	            }
	        }
	        return answer;
	    }
	};
	
{% endraw %}
