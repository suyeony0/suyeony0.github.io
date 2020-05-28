---
layout: post
title: [1110 Delete Nodes And Return Forest]
date: 2020-5-29
description: txt to markdown
thumbnail: building1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

```cpp
	﻿[75. [1110] Delete Nodes And Return Forest – delete given node, and return roots of every subtrees.]
	- I solved this problme using bottom-up approach.
	- First at all, using postorder search and if a current node has to be deleted, insert their children into answer vector, and come back to parents node, finally delete the node.
	- but the point is how I can handle the original root node, value 1, because of that, I have to use another find function whether the to_delete vector has 1 or not. so it cunsumes pretty much time I think.
	- Tommrow I will revise this algorithm.
	<before tommorow>
	- I changed the algorithm to handle value 1, just adding a boolean variable to check whether the vector to_delete has 1 or not.
	- If to_delete has 1, don't add original root to answer otherwise add it.
	- Final time beats was around 88%.
	class Solution {
	public:
	    bool flag=true; // added
	    TreeNode* helper(TreeNode* root,vector<TreeNode*>& answer, vector<int>& to_delete){
	        if(!root) return nullptr;
	        TreeNode* left=nullptr;
	        TreeNode* right=nullptr;
	        left=helper(root->left,answer,to_delete);
	        right=helper(root->right,answer,to_delete);
	        if(left) root->left=nullptr;
	        if(right) root->right=nullptr;
	        for(int i=0;i<to_delete.size();i++){
	            if(to_delete[i]==root->val){
	                if(root->val==1) flag=false; //added
	                if(root->left) answer.push_back(root->left);
	                if(root->right) answer.push_back(root->right);
	                to_delete.erase(to_delete.begin()+i);
	                return root;
	            }
	        }
	        return nullptr;
	    }
	    vector<TreeNode*> delNodes(TreeNode* root, vector<int>& to_delete) {
	        vector<TreeNode*> answer; 
	        helper(root,answer,to_delete);
	        if(flag) answer.push_back(root); //added
	        return answer;
	    }
	};  
	
```
