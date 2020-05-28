---
layout: post
title: [KAKAO 2018 - Dart Game]
date: 2020-5-29
description: txt to markdown
thumbnail: city2.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

{% highlight c++ %}
```cpp
	﻿[140. [Programmers– KAKAO 2018 :Dart Game]]
	- String parsing and caculate using given rule is the way to solve this problem.
	- parsing part was pretty naughty. since I had to check all the index of the string. but given string was short. So I could follow where an index is and there was no time issue either.
	- see the code.
	#include <string>
	#include<vector>
	#include<cmath>
	#include<iostream>
	using namespace std;
	
	int solution(string dartResult) {
	    vector<string> res;
	    string temp="";
	    //string parsing to make vector
	    for(int i=0;i<dartResult.size();i++){
	        if('0'<=dartResult[i] && dartResult[i]<='9'){
	            temp+=dartResult[i];    
	        }
	        else{
	            temp+=dartResult[i];
	            if(dartResult[i+1]=='*' || dartResult[i+1]=='#'){
	                i++;
	                temp+=dartResult[i];
	            } 
	            res.push_back(temp);
	            temp="";
	        }
	    }
	    //split the score record
	    vector<pair<int,vector<char>>> score(3);
	    for(int i=0;i<res.size();i++){
	        string score_part="";
	        int j=0;
	        for(j=0;j<res[i].size();j++){
	            if('0'<=res[i][j] && res[i][j]<='9'){
	                score_part+=res[i][j];
	            }
	            else break;
	        }
	        score[i].first=stoi(score_part);
	        score[i].second.push_back(res[i][j]);
	        if(res[i].back()=='*' || res[i].back()=='#') score[i].second.push_back(res[i].back());
	    }
	    //let's caculate
	    vector<int> table(3);
	    for(int i=0;i<score.size();i++){
	        if(score[i].second[0]=='S') table[i]=score[i].first;
	        else if(score[i].second[0]=='D') table[i]=pow(score[i].first,2);
	        else if(score[i].second[0]=='T') table[i]=pow(score[i].first,3);
	    }
	    //option
	    for(int i=0;i<score.size();i++){
	        if(score[i].second.size()==1) continue;
	        if(score[i].second[1]=='#') table[i]*=-1;
	        else{
	            if(i==0) table[i]*=2;
	            else{
	                table[i-1]*=2;
	                table[i]*=2;
	            }
	        }
	    }
	    int answer = 0;
	    for(int i=0;i<table.size();i++)
	        answer+=table[i];
	    
	    return answer;
	}
	
```
{% endhighlight %}
