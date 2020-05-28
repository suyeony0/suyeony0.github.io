---
layout: post
title: [1043 Partition Array for Maximum Sum]
date: 2020-5-29
description: txt to markdown
thumbnail: building1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

{% highlight c++ %}
	﻿[83. [1043] Partition Array for Maximum Sum – partition the given array into subarrays of length  at most given K. each subarray’s value will be changed the greatest value in the subarrays. return the largest sum of the given arrays after partitioning]
	- what the heck? this problem is not a midium level. I think!, Yes, I may not good at DP problem :).
	- Anyway, I tried to solve this problem 2d DP.
	- row is index, col is the size of partition.
	- Algorithm is just >> dp[i][j] = max(dp[i-j]…dp[i-1]) + max(A[i-j+1]….A[i])*j).
	 
	- But tiem limit exceeded occurred.
	- see the code.
	class Solution {
	public:
	    void printDP(vector<vector<int>> dp){
	        for(int i=0;i<dp.size();i++){
	            for(int j=0;j<dp[i].size();j++){
	                cout<<dp[i][j]<<" ";
	            }
	            cout<<endl;
	        }
	    }
	    void initializeDP(vector<int> A, int K, vector<vector<int>>& dp){
	        //vector initialized
	        for(int i=0;i<A.size();i++)
	            dp[i][0]=A[i]; //when K=1;
	        //initialize DP's diagonal.
	        for(int i=1,j=1;i<K;i++,j++){
	            dp[i][j]=*std::max_element(A.begin(),next(A.begin(),i+1))*(j+1);
	        }
	        //initialize DP's upper triangle.
	        for(int i=0;i<K;i++){
	            for(int j=i+1;j<K;j++){
	                dp[i][j]=dp[i][j-1];
	            }
	        }
	    }
	    int dpMAX(vector<vector<int>>& dp,vector<int> A, int K, int i, int j){
	        int res=INT_MIN;
	        int prev;
	        int max_ele=INT_MIN;
	        for(int a=i-(j+1);a<i;a++){
	            prev=dp[a][j]; // a = 1
	            for(int b=a+1;b<=i;b++){
	                max_ele=max(max_ele,A[b]);
	            }
	            res=max(res,prev+max_ele*(i-a));
	            max_ele=INT_MIN;
	        }
	        return res;
	    }
	    
	    int maxSumAfterPartitioning(vector<int>& A, int K) {
	        if(K==1){
	            return accumulate(A.begin(),A.end(),0);
	        }
	        vector<vector<int>> dp(A.size(),vector<int>(K,0));
	        initializeDP(A,K,dp);
	        for(int j=1;j<K;j++){
	            for(int i=j+1;i<A.size();i++){
	                dp[i][j]=dpMAX(dp,A,K,i,j);
	            }
	        }
	        printDP(dp);
	        return dp[A.size()-1][K-1];
	    }
	};
	- I happened to recognize that I don’t need the 2d DP, since I don’t use previous j(which is 1…K-1) array in the 2d DP. I needed just dp[i][K].
	- so I revised my algorithm to an 1d DP.
	- speed was 11.42% beats. I know is quite slow, but I’m happy I could solve this problem :).
	- see the code.
	class Solution {
	public:
	    void initializeDP(vector<int> A, int K, vector<int>& dp){
	        int max_ele=INT_MIN;
	        for(int i=0;i<K;i++)
	            dp[i]=*max_element(A.begin(),next(A.begin(),i+1))*(i+1);
	    }
	    int dpMAX(vector<int>& dp,vector<int> A,int i,int K){
	        int res=INT_MIN;
	        int prev;
	        int max_ele=INT_MIN;
	        for(int a=i-K;a<i;a++){
	            prev=dp[a];
	            for(int b=a+1;b<=i;b++){
	                max_ele=max(max_ele,A[b]);
	            }
	            res=max(res,prev+max_ele*(i-a));
	            max_ele=INT_MIN;
	        }
	        return res;
	    }         
	    int maxSumAfterPartitioning(vector<int>& A, int K) {
	        if(K==1){
	            return accumulate(A.begin(),A.end(),0);
	        }
	        vector<int> dp(A.size(),0);
	        initializeDP(A,K,dp);
	        for(int i=K;i<A.size();i++){
	            dp[i]=dpMAX(dp,A,i,K);
	        }
	        return dp[A.size()-1];
	    }
	};
	
{% endhighlight %}
