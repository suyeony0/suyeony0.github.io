---
layout: post
title: [695 Max Area of Island]
date: 2020-5-29
description: txt to markdown
thumbnail: breakfast-orange-lemon-oranges-large.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

{% highlight c++ %}
```cpp
	﻿[99. [695] Max Area of Island] – return a maximum size of island]
	- just use DFS or BFS. Emprically, DFS is faster than BFS.
	- see the code.
	class Solution {
	public:
	    int DFS(vector<vector<int>>& grid,int x, int y,int area){
	        if(!grid[x][y]) return 0;
	        grid[x][y]=0;
	        if(x-1>=0 && grid[x-1][y]) area+=DFS(grid,x-1,y,0);
	        if(y-1>=0 && grid[x][y-1]) area+=DFS(grid,x,y-1,0);
	        if(x+1<grid.size() && grid[x+1][y]) area+=DFS(grid,x+1,y,0);
	        if(y+1<grid[0].size() && grid[x][y+1]) area+=DFS(grid,x,y+1,0);
	        return area+1;
	        
	    }
	    
	    int maxAreaOfIsland(vector<vector<int>>& grid) {
	        int answer=0;
	        int cur;
	        for(int i=0;i<grid.size();i++){
	            for(int j=0;j<grid[0].size();j++){
	                if(grid[i][j]==1){
	                    cur=DFS(grid,i,j,0);
	                    answer=max(answer,cur);
	                }
	                    
	            }
	        }
	        return answer;
	    }
	};
	
```
{% endhighlight %}
