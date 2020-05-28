---
layout: post
title: [KAKAO 2018 - Shuttle Bus]
date: 2020-5-29
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% highlight c++ %}
```cpp
	﻿[136. [Programmers– KAKAO 2018 :Shuttle Bus]]
	- handling time is always naughty for me lol :).
	- I changed all the bus schedule to unit of minute. <- is this english right? haha.
	- see the code.
	
	#include <string>
	#include <vector>
	#include <algorithm>
	#include <map>
	#include<iostream>
	using namespace std;
	
	string solution(int n, int t, int m, vector<string> timetable) {
	    string answer = "";
	    int base = 9*60;
	    vector<pair<int,vector<int>>> possible_time;
	    for(int i=0;i<n;i++) possible_time.push_back(make_pair(base+(t*i),vector<int>{0,999999,-1}));
	    vector<bool> full_bus(possible_time.size(),false);
	    
	    vector<int> min_table(timetable.size());
	    for(int i=0; i<timetable.size();i++) min_table[i]=stoi(timetable[i].substr(0,2))*60 + stoi(timetable[i].substr(3,2));
	    sort(min_table.begin(),min_table.end());
	    
	    int start=0;
	    for(int i=0;i<possible_time.size();i++){
	        int bus_time = possible_time[i].first;
	        for(int j=start;j<min_table.size();j++){
	            if(min_table[j]<=bus_time){
	                possible_time[i].second[0]++;
	                possible_time[i].second[1]=min(possible_time[i].second[1],min_table[j]);
	                possible_time[i].second[2]=max(possible_time[i].second[2],min_table[j]);
	                if(possible_time[i].second[0]>=m){ full_bus[i]=true; start=j+1; break; }
	            } 
	            else { start=j; break; }
	        }
	    }
	   
	    int res_time;
	    if(full_bus[n-1]){
	        if(possible_time[n-1].second[2]==possible_time[n-1].second[1]) res_time=possible_time[n-1].second[1]-1;
	        else res_time=possible_time[n-1].second[2]-1;
	    }
	    else{
	        res_time=possible_time[n-1].first;
	    }
	    
	    string hour; string minute;
	    hour=to_string(res_time/60); minute=to_string(res_time%60);
	    if(hour.size()==1) hour="0"+hour; if(minute.size()==1) minute="0"+minute;
	    answer=hour+":"+minute;
	    return answer;
	}
	
```
{% endhighlight %}
