---
layout: post
title: [1130 Minimum Cost Tree From Leaf Values]
date: 2020-5-29
description: txt to markdown
thumbnail: city2.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

```cpp

{% raw %}

	﻿[78. [1130] Minimum Cost Tree From Leaf Values – find minimum sum of non-leaf node using the given leaves.]
	- Atually, this problem was super difficult for me. First at all, I thought I sholud have construted a real tree. But it’s quite insane jobs.
	- so I tried to make dp but it was not that easy. Finally, I refered to discussion.
	- O(N^2) algorithm is below.
	> 1. find minimum leaf of the array : val1
	> 2. find min(the leaf’s left, the leaf’s right) : val2
	> 3. answer+= val1 * val2
	> 4. remove val1 and repeat from 1st.
	class Solution {
	public:
	    int mctFromLeafValues(vector<int>& arr) {
	        int answer=0;
	        int minimum;
	        int second;
	        while(arr.size()>1){
	            minimum=min_element(arr.begin(),arr.end())-arr.begin(); //minimum value's index
	            if(minimum==0) second=1;
	            else if(minimum==arr.size()-1) second=minimum-1;
	            else{
	                if(arr[minimum+1]>arr[minimum-1]) second=minimum-1;
	                else second=minimum+1;
	            }
	            answer+=arr[minimum]*arr[second];
	            arr.erase(arr.begin()+minimum);
	            if(minimum>second) minimum--;
	        }
	        return answer;
	    }
	};
	
	- Now I’m trying to understand O(N^3) solution that uses dp.
	- The dp solusion from discussion is below.
	Approach 1 (DP)
	In the image the root, their left subtree contains indexes [0-3] and their right subtree cointains indexes [4-5]. Then their value will be max(arr[0-3])* max(arr[4-5]).
	In general:
	dp(left, right )= min( max(arr[left .. i] ) * max(arr[i+1 .. right]) + dp(left,i) +dp(i+1,right) ) where i go from left to right-1
	class Solution {
	public:
	    int memo[41][41];
	    int maxi[41][41];
	    
	    int dp(int left,int right){
	        if(left==right)return 0; //leaf node
	        if(memo[left][right]!=-1)return memo[left][right];
	        
	        int ans = 1<<30;
	        
	        for(int i=left;i<right;i++)
	            ans= min(ans, maxi[left][i] * maxi[i+1][right] + dp(left,i) + dp(i+1,right) );
	        
	        memo[left][right]=ans;
	        return ans;
	    }
	    
	    int mctFromLeafValues(vector<int>& arr) {
	        memset(memo,-1,sizeof(memo));
	        for(int i=0;i<arr.size();i++){
	            maxi[i][i] = arr[i];
	            for(int j=i+1;j<arr.size();j++)
	                maxi[i][j] = max(maxi[i][j-1], arr[j]);
	        }
	        
	        return dp(0,arr.size()-1);
	    }
	};
	
{% endraw %}
```

