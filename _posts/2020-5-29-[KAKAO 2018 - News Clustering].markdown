---
layout: post
title: [KAKAO 2018 - News Clustering]
date: 2020-5-29
description: txt to markdown
thumbnail: building1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

{% highlight c++ %}
```cpp
	﻿[134. [Programmers– KAKAO 2018 :News Clustering]]
	- it was just string parsing and make intersection and union set. so not that hard.
	- see the code.
	
	#include <string>
	#include<iostream>
	#include <algorithm>
	#include<unordered_map>
	#include<unordered_set>
	#define min(a,b) a>b? b:a
	#define max(a,b) a>b? a:b
	using namespace std;
	
	bool isAlpha(char& s){
	    if('a'<= s && s<='z') return true;
	    return false;
	}
	
	unordered_set<string> SplitStr(string s,unordered_map<string,int>& count){
	    unordered_set<string> res;
	    for(int i=1;i<s.size();i++){
	        string temp;
	        if(isAlpha(s[i-1]) && isAlpha(s[i])){
	            temp=s.substr(i-1,2);
	            res.insert(temp);
	            count[temp]++;
	        } 
	    }
	    return res;
	}
	
	int solution(string str1, string str2) {
	    int answer = 0;
	    
	    unordered_map<string,int> s1; unordered_map<string,int> s2;
	    transform(str1.begin(),str1.end(),str1.begin(),::tolower);
	    transform(str2.begin(),str2.end(),str2.begin(),::tolower);
	    unordered_set<string> a=SplitStr(str1,s1); unordered_set<string> b=SplitStr(str2,s2);
	    //find intersection
	    vector<string> inter; 
	    int minimum; 
	    for(unordered_set<string>::iterator iter=a.begin();iter!=a.end();iter++){
	        if(s2.find(*iter)!=s2.end()){
	            minimum=min(s1[*iter],s2[*iter]);
	            for(int j=0;j<minimum;j++) inter.push_back(*iter);
	        }
	    }
	    //find union
	    vector<string> uni;
	    unordered_set<string> temp_set;
	    temp_set.insert(a.begin(),a.end()); temp_set.insert(b.begin(),b.end());
	    int maximum;
	    for(unordered_set<string>::iterator iter=temp_set.begin();iter!=temp_set.end();iter++){
	        if(s1.find(*iter)!=s1.end() && s2.find(*iter)!=s2.end()){
	            maximum=max(s1[*iter],s2[*iter]);
	            for(int j=0;j<maximum;j++) uni.push_back(*iter);
	        }
	        else if(s1.find(*iter)!=s1.end()) for(int j=0;j<s1[*iter];j++) uni.push_back(*iter);
	        else if(s2.find(*iter)!=s2.end()) for(int j=0;j<s2[*iter];j++) uni.push_back(*iter);
	    }
	
	    if(inter.empty() && uni.empty()) return 65536;
	    answer=((double)inter.size()/(double)uni.size())*65536;
	    return answer;
	}
	
```
{% endhighlight %}
