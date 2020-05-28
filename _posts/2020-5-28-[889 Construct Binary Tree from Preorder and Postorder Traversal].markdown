---
layout: post
title: [889 Construct Binary Tree from Preorder and Postorder Traversal]
data: 2020-05-26
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}

	﻿[79 [889] Construct Binary Tree from Preorder and Postorder Traversal – make a binary tree using the given pre and postorder traversals]
	- My first algorithm is that the right next node of current node in preoder traversal is root’s left child and the left next node of current node in post traversal is root’s right child.
	- But it’s wrong.
	- So I tried a divivde and conquer approach.
	- What a difficult problem! I spent almost 4 hours for this heck!
	- The key point is divide each traversal respectively.
	- And if after making left child, mid+1==postr, then just have to return root.
	
	class Solution {
	public:
	    unordered_map<int,int> table;
	    TreeNode* helper(vector<int>& pre, vector<int>& post,int prel,int prer,int postl, int postr){
	        TreeNode* root=new TreeNode(pre[prel]);
	        if(prel==prer) return root;
	        int mid=table[pre[prel+1]];
	        int length=mid-postl;
	        root->left=helper(pre,post,prel+1,prel+length+1,postl,postl+length);
	        if(mid+1==postr) return root;
	        root->right=helper(pre,post,prel+length+2,prer,mid+1,postr-1);
	        return root;
	    }
	    TreeNode* constructFromPrePost(vector<int>& pre, vector<int>& post) {
	        for(int i=0;i<post.size();i++) table[post[i]]=i;
	        TreeNode* root=helper(pre,post,0,pre.size()-1,0,post.size()-1);
	        return root;
	    }
	};
	
{% endraw %}
