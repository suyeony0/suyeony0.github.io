---
layout: post
title: {% raw %}[429] N-ary Tree Level Order Traversal{% endraw %}
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}
	﻿
	[90. [429] N-ary Tree Level Order Traversal – split given tree based on levels]
	- I think there are two method to solve the problem. one is to use two queues, the other is to use only one queue and to count how many nodes we have to consider in a level 
	- I chose a second algorithm.
	- Algorithm is below.
	> 1. For each iteration, memorize how many children are there at a certain level. Then we can use the number as a next level’s the number of nodes.
	> 2. And for each iteration, if we met NULL, skip it. otherwise put the node’s children into the queue.
	> 3. repeating from 1. until queue becomes empty.
	- the speed was 52.03% beats.
	-see the code. notice that I added the Node class since it’s not the usual form of normal Node Class.
	/*
	// Definition for a Node.
	class Node {
	public:
	    int val;
	    vector<Node*> children;
	
	    Node() {}
	
	    Node(int _val) {
	        val = _val;
	    }
	
	    Node(int _val, vector<Node*> _children) {
	        val = _val;
	        children = _children;
	    }
	};
	*/
	class Solution {
	public:
	    void levelOrder(Node* root,queue<Node*>& que,vector<int>& cur_level){
	        if(!root) return;
	        for(Node* i : root->children){
	            que.push(i);
	            cur_level.push_back(i->val);
	        }
	    }
	    vector<vector<int>> levelOrder(Node* root) {
	        if(!root) return {};
	        queue<Node*> que;
	        vector<vector<int>> answer;
	        vector<int> cur_level;
	        que.push(root);
	        Node* cur;
	        int need=1;
	        answer.push_back({{root->val}});
	        while(!que.empty()){
	            for(int count=0;count<need;count++){
	                cur=que.front();
	                que.pop();
	                levelOrder(cur,que,cur_level);
	            }
	            if(!cur_level.empty()) answer.push_back(cur_level);
	            need=cur_level.size();
	            cur_level.clear();
	        }
	        return answer;
	    }
	};
	
	
{% endraw %}
