---
layout: post
title: [951  Flip Equivalent Binary Trees]
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}
	﻿[when we choose any node and swap left and right subtrees, we call it a flip operation. 
	 Write a function whether two given trees are flip equivalent.]
	- no matter a tree is filped or not, its children have to be same or just changed the order.
	- So we can just compare every possible situation – Greedy using DFS.
	
	class Solution {
	public:
	    bool flag=true;
	    void helper(TreeNode* root1,TreeNode* root2){
	        if(!root1->left && !root1->right && !root2->left && !root2->right)
	            return;
	        if(root1->left && root2->left && root1->left->val == root2->left->val)
	            helper(root1->left,root2->left); 
	        else if(root1->left && root2->right && root1->left->val==root2->right->val)    
	            helper(root1->left,root2->right);
	        else if(root1->left){
	            flag=false;
	            return;
	        }
	        if(!flag) return;
	        else if(root1->right && root2->left && root1->right->val==root2->left->val)    
	            helper(root1->right,root2->left);
	        
	        else if(root1->right && root2->right && root1->right->val==root2->right->val)
	            helper(root1->right,root2->right);
	        else if(root1->right){
	            cout<<"flag"<<endl;
	            flag=false;
	        } 
	        
	    }
	    bool flipEquiv(TreeNode* root1, TreeNode* root2) {
	        if(!root1 && !root2) return true;
	        if((root1 && !root2) ||(!root1 && root2)) return false;
	        helper(root1,root2);
	        return flag;
	    }
	};
	
{% endraw %}
