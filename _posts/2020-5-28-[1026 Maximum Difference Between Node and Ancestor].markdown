---
layout: post
title: [1026 Maximum Difference Between Node and Ancestor]
date: 2020-5-28
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}

	﻿[86. [1026] Maximum Difference Between Node and Ancestor – find the greatest difference between an ancestor and decendant]
	- In my algorithm, I should’ve used both DFS and BFS for brute-force.
	- The algorithm is quite vivid. For each node, I check differeces between the current node and its decendants.
	- see the code. the speed was bad. It was just 5.20% beats.
	class Solution {
	public:
	    int DFS(TreeNode* root,int cur_val){
	        if(!root) return 0;
	        return max(abs(root->val-cur_val),max(DFS(root->left,cur_val),DFS(root->right,cur_val)));
	    }
	    
	    int maxAncestorDiff(TreeNode* root) {
	        queue<TreeNode*> que;
	        TreeNode* cur;
	        que.push(root);
	        int answer=0;
	        while(!que.empty()){
	            cur=que.front();
	            que.pop();
	            if(cur->left) que.push(cur->left);
	            if(cur->right) que.push(cur->right);
	            answer=max(answer,max(DFS(cur->left,cur->val),DFS(cur->right,cur->val)));
	        }
	        return answer;
	    }
	};
	
	- In the discussion, there is such a superb approach using 1d vector.
	- The algorithm is below.
	> 1. finding every paht from root to leaf. and push to vector.
	> 2. Then a lefter element is an ancestor of righter element.
	> 3. by using this vector, we can find the maximum difference.
	- This algorithm was just O(n) where n is the number of nodes.
	- Even, we don’t need the 1d vector, we just have to maintain current maximum and minimum value so that when we meet a leaf node, we can use it to calculate a local maximum difference.
	- the speed was 69.22% beats. I reckon it quite fast enough.
	-see the code.
	class Solution {
	public:
	    void DFS(TreeNode* root, int& answer,int maximum,int minimum){
	        maximum=max(maximum,root->val);
	        minimum=min(minimum,root->val);
	        if(!root->left && !root->right){
	            answer=max(answer,maximum-minimum);
	            return;
	        }
	        if(root->left) DFS(root->left,answer,maximum,minimum);
	        if(root->right) DFS(root->right,answer,maximum,minimum);
	    }
	    int maxAncestorDiff(TreeNode* root) {
	        int answer=0;
	        DFS(root,answer,INT_MIN,INT_MAX);
	        return answer;
	    }
	};
	
{% endraw %}
