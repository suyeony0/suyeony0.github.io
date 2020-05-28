---
layout: post
title: [1123 Lowest Common Ancestor of Deepest Leaves]
date: 2020-5-28
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}

	﻿- find the deepest level from root. If the deepest depth is same, then the root is the answer.
	- if the depth is different. determine which one has deeper depth between left and right child.
	- and doing recursive with the child who has deeper detph.
	
	class Solution {
	public:
	    int helper(TreeNode* root){
	        if(!root) return 0;
	        return 1+max(helper(root->left),helper(root->right));
	    }
	    TreeNode* lcaDeepestLeaves(TreeNode* root) {
	        int left=helper(root->left);
	        int right=helper(root->right);
	        if(left==right) return root;
	        else if(left>right) return lcaDeepestLeaves(root->left);
	        else return lcaDeepestLeaves(root->right);
	    }
	};
{% endraw %}
