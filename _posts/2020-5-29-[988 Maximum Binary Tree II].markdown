---
layout: post
title: [988 Maximum Binary Tree II]
date: 2020-5-29
description: txt to markdown
thumbnail: work1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

{% highlight c++ %}
```cpp
	﻿[92. [998] Maximum Binary Tree II – insert the given value into max heap]
	- Algorithm is below.
	> 1. if root is exist and root->val > given value, call the helper function with giving root->right as a parameter.
	> 2. if root is not exist or root->val<=given value, create a new node of given value.
	> 3. Allocate the new node->left = root. And return the node.
	- see the code.
	class Solution {
	public:
	    TreeNode* helper(TreeNode* root, int val){
	        if(root && root->val>val){
	            root->right=helper(root->right,val);
	            return root;
	        }
	        TreeNode* node=new TreeNode(val);
	        node->left=root;
	        return node;
	    }
	    TreeNode* insertIntoMaxTree(TreeNode* root, int val) {
	        return helper(root,val);
	    }
	};
	
```
{% endhighlight %}
