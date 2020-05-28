---
layout: post
title: [959 Regions Cut By Slashes]
data: 2020-05-26
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}

	﻿[77. [959] Regions Cut By Slashes – return how many distinct regions appear after dividing whole square by /, \]
	- I solved this problem using BFS. But the result was time limit exceeded.
	- 1. make the given array 3 time widen. Because to recognize distinct region, we need at least 3 time wider array.
	- 2. draw given line to divide region.
	- 3. using BFS, paint regions and count hom many regions are.
	
	class Solution {
	public:
	    void helper(vector<vector<int>>& table,queue<pair<int,int>> que){
	        while(!que.empty()){
	            int x=que.front().first;
	            int y=que.front().second;
	            que.pop();
	            table[x][y]=1;
	            if(x && table[x-1][y]==0) que.push(make_pair(x-1,y));
	            if(y && table[x][y-1]==0) que.push(make_pair(x,y-1));
	            if(x!=table.size()-1 && table[x+1][y]==0) que.push(make_pair(x+1,y));
	            if(y!=table[0].size()-1 && table[x][y+1]==0) que.push(make_pair(x,y+1));
	        }
	    }
	    void paintRegion(vector<vector<int>>& table,int& answer){
	        queue<pair<int,int>> que;
	        for(int i=0;i<table.size();i++){
	            for(int j=0;j<table[i].size();j++){
	                if(table[i][j]==0){
	                    que.push(make_pair(i,j));
	                    helper(table,que);
	                    answer++;
	                }
	            }
	        }
	    }
	    int regionsBySlashes(vector<string>& grid) {
	        int N=grid.size()*3;
	        vector<vector<int>> table(N,vector<int>(N,0)); //make table N*3 X N*3
	        for(int i=0;i<grid.size();i++){
	            for(int j=0;j<grid[i].size();j++){
	                if(grid[i][j]=='/'){
	                    table[i*3][3*j+2]=1;
	                    table[i*3+1][3*j+1]=1;
	                    table[i*3+2][3*j]=1;
	                }
	                else if(grid[i][j]=='\\'){
	                    table[i*3][3*j]=1;
	                    table[i*3+1][3*j+1]=1;
	                    table[i*3+2][3*j+2]=1;
	                }
	            }
	        }
	        int answer=0;
	        paintRegion(table,answer);
	        return answer;
	    }
	};
	
	- due to time limit exceeded, I changed my algorithm to DFS.
	
	class Solution {
	public:
	    void paintRegion(vector<vector<int>>& table,int x, int y){
	        if(table[x][y]==0){
	            table[x][y]=1;
	            if(x) paintRegion(table,x-1,y);
	            if(y) paintRegion(table,x,y-1);
	            if(x!=table.size()-1) paintRegion(table,x+1,y);
	            if(y!=table.size()-1) paintRegion(table,x,y+1);
	        } 
	            
	    }
	    int regionsBySlashes(vector<string>& grid) {
	        int N=grid.size()*3;
	        int answer=0;
	        vector<vector<int>> table(N,vector<int>(N,0)); //make table N*3 X N*3
	        for(int i=0;i<grid.size();i++){
	            for(int j=0;j<grid[i].size();j++){
	                if(grid[i][j]=='/'){
	                    table[i*3][3*j+2]=1;
	                    table[i*3+1][3*j+1]=1;
	                    table[i*3+2][3*j]=1;
	                }
	                else if(grid[i][j]=='\\'){
	                    table[i*3][3*j]=1;
	                    table[i*3+1][3*j+1]=1;
	                    table[i*3+2][3*j+2]=1;
	                }
	            }
	        }
	        
	        for(int i=0;i<table.size();i++){
	            for(int j=0;j<table[i].size();j++){
	                if(table[i][j]==0){
	                    paintRegion(table,i,j);
	                    answer++;
	                }
	            }
	        }
	        return answer;
	    }
	};
	
	
	
{% endraw %}
