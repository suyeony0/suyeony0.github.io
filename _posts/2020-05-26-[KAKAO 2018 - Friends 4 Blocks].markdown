---
layout: post
title: {% raw %}[KAKAO 2018 - Friends 4 Blocks]{% endraw %}
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}
	﻿
	[137. [Programmers– KAKAO 2018 :Friends 4 Blocks]]
	- it was a slicing problem. 
	- but the fucking confusing between m and n, I spend quite much time shit!
	- From now, I’m gonna use height and length for m and n to prevent such a confusing situation.
	- p.s) unordered_set looks not able to handle pair<int,int>. so I changed it to set.
	- see the code.
	#include <string>
	#include <vector>
	#include<iostream>
	#include<set>
	using namespace std;
	
	vector<vector<char>> makeTable(int m,int n, vector<string> board){
	    vector<vector<char>> table(m,vector<char>(n));
	    for(int i=0;i<m;i++)
	        for(int j=0;j<n;j++)
	            table[i][j]=board[i][j];
	    
	    return table;
	}
	set<pair<int,int>> findBlock(int m,int n, vector<vector<char>>& table){
	    set<pair<int,int>> remove;
	    for(int i=1;i<m;i++){
	        for(int j=1;j<n;j++){ //slice
	            char c=table[i][j];
	            if(c==0) continue;
	            bool flag=true;
	            for(int a=i-1;a<=i;a++){
	                for(int b=j-1;b<=j;b++){
	                    if(table[a][b]!=c){
	                        flag=false;
	                        break;
	                    }
	                }
	                if(!flag) break;
	            }
	            if(flag){
	                for(int a=i-1;a<=i;a++){
	                    for(int b=j-1;b<=j;b++){
	                        remove.insert(make_pair(a,b));
	                    }
	                }
	            }
	            
	        }
	    }
	    return remove;
	}
	
	vector<vector<char>> newTable(int m, int n,vector<vector<char>> table){
	    for(int j=0;j<n;j++){
	        //bool flag=true;
	        for(int i =m-1;i>=0;i--){
	            if(table[i][j]!=0) continue;
	            for(int a=i-1;a>=0;a--){
	                //if(a==0) flag=false;
	                if(table[a][j]==0) continue;
	                else{
	                    table[i][j]=table[a][j];
	                    table[a][j]=0;
	                    break;
	                }
	            }
	            //if(!flag) break;
	        }
	    }
	    return table;
	}
	
	int Game(int m,int n, vector<vector<char>> table){
	    set<pair<int,int>> remove_index;
	    int count=0;
	    while(true){
	        //find block
	        remove_index=findBlock(m,n,table);
	        if(remove_index.empty()) break;
	        count+=remove_index.size();
	        //remove block
	        for(set<pair<int,int>>::iterator iter=remove_index.begin();iter!=remove_index.end();iter++){
	            int x=iter->first; int y = iter->second;
	            table[x][y]=0;
	        }
	        //make new table;
	        table=newTable(m,n,table);
	    }
	    return count;
	}
	
	
	
	int solution(int m, int n, vector<string> board) {
	    int answer = 0;
	    vector<vector<char>> table=makeTable(m,n,board);
	    answer=Game(m,n,table);
	    return answer;
	}
	
	
{% endraw %}
