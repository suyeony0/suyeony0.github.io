---
layout: post
title: [1219 Path with Maximum Gold]
date: 2020-5-29
description: txt to markdown
thumbnail: food1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

```cpp

{% raw %}

	﻿[84. [1219] Path with Maximum Gold – find a path to get maximum gold]
	- I used DFS to solve this problem. the algorithm is quite intutive. I think the explanation is not needed. just cafeful to use visit array.
	- but time limit exceeded occurred.
	- see the code.
	class Solution {
	public:
	    int DFS(vector<vector<int>> grid,int x,int y,vector<vector<int>> visit){
	        visit[x][y]=1;
	        int cur_gold=grid[x][y];
	        vector<int> max_gold;
	        if(x && grid[x-1][y]&& !visit[x-1][y]) max_gold.push_back(DFS(grid,x-1,y,visit));
	        if(y && grid[x][y-1]&&!visit[x][y-1]) max_gold.push_back(DFS(grid,x,y-1,visit));
	        if(x+1<grid.size() && grid[x+1][y]&&!visit[x+1][y] ) max_gold.push_back(DFS(grid,x+1,y,visit));
	        if(y+1<grid[0].size() && grid[x][y+1]&&!visit[x][y+1]) max_gold.push_back(DFS(grid,x,y+1,visit));
	        return cur_gold+ (max_gold.empty()? 0:*max_element(max_gold.begin(),max_gold.end()));
	    }
	    
	    int getMaximumGold(vector<vector<int>>& grid) {
	        int answer=0;
	        vector<vector<int>> visit(grid.size(),vector<int>(grid[0].size(),0));
	        for(int i=0;i<grid.size();i++)
	            for(int j=0;j<grid[i].size();j++)
	                if(grid[i][j])
	                    answer=max(answer,DFS(grid,i,j,visit));
	        return answer;
	    }
	};
	
	- I thought the time limit exceeded happened due to max_gold vector and visit vector. so I remove these.
	- First, I changed max_gold vector to int and just compare all the possible DFS. Because putting a value into vector and finding maximum value from that vector need quite long time I think.
	- Second, I remove visit vector and just use the condition which is, if a cell has 0 golds, then we don’t need to visit the cell. so whenever I visit a cell, I changed the value to 0 like I collected the gold. After all the visiting to neighbor cells, I returned the amount of gold to the cell.
	- Finally, I got speed 96.09% beats :).
	- see the code.
	class Solution {
	public:
	    int DFS(vector<vector<int>>& grid,int x,int y){
	        int cur_gold=grid[x][y];
	        grid[x][y]=0;
	        int max_gold=0;
	        if(x && grid[x-1][y]) max_gold=max(max_gold,DFS(grid,x-1,y));
	        if(y && grid[x][y-1]) max_gold=max(max_gold,DFS(grid,x,y-1));
	        if(x+1<grid.size() && grid[x+1][y]) max_gold=max(max_gold,DFS(grid,x+1,y));
	        if(y+1<grid[0].size() && grid[x][y+1]) max_gold=max(max_gold,DFS(grid,x,y+1));
	        grid[x][y]=cur_gold;
	        return cur_gold+ max_gold;
	    }
	    int getMaximumGold(vector<vector<int>>& grid) {
	        int answer=0;
	        for(int i=0;i<grid.size();i++)
	            for(int j=0;j<grid[i].size();j++)
	                if(grid[i][j])
	                    answer=max(answer,DFS(grid,i,j));
	        return answer;
	    }
	};
	
{% endraw %}
```

