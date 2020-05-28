---
layout: post
title: [931 Minimum Falling Path Sum]
date: 2020-5-29
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% highlight c++ %}
	﻿[96 [931] Minimum Falling Path Sum – find minimum sum of given rules]
	- At first, I used DFS to consider all the path possible. but time limit exceeded occurred.
	- see the code.
	class Solution {
	public:
	    int helper(vector<vector<int>> A, int i,int j,int sum=0){
	        if(j<0 || j>=A[0].size()) return INT_MAX;
	        int cur=sum+A[i][j];
	        if(i==A.size()-1) return cur;
	        return min(helper(A,i+1,j-1,cur),min(helper(A,i+1,j,cur),helper(A,i+1,j+1,cur)));
	    }
	    int minFallingPathSum(vector<vector<int>>& A) {
	        int minimum=INT_MAX;
	        for(int i=0;i<A[0].size();i++){
	            minimum=min(minimum,helper(A,0,i));
	        }
	        return minimum;
	    }
	};
	- I changed my algorithm to DP.
	- we don’t need to consider previous row after the minimum value of dp[i][j] is allocated.
	- the speed was 99.24 % beats.
	- see the code.
	class Solution {
	public:
	    int minFallingPathSum(vector<vector<int>>& A) {
	        vector<vector<int>> dp(A.size(),vector<int>(A[0].size(),INT_MAX));
	        for(int i=0;i<dp[0].size();i++)
	            dp[0][i]=A[0][i];
	        for(int i=0;i<dp.size()-1;i++){
	            for(int j=0;j<dp[0].size();j++){
	                if(j-1>=0) dp[i+1][j-1]=min(dp[i+1][j-1],dp[i][j]+A[i+1][j-1]);
	                dp[i+1][j]=min(dp[i+1][j],dp[i][j]+A[i+1][j]);
	                if(j+1<dp[0].size()) dp[i+1][j+1]=min(dp[i+1][j+1],dp[i][j]+A[i+1][j+1]);
	            }
	        }
	        return *min_element(dp[dp.size()-1].begin(),dp[dp.size()-1].end());
	    }
	};
	
{% endhighlight %}
