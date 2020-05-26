---
layout: post
title: [KAKAO 2018 - Harvet Fest Traffic]
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

	﻿[133. [Programmers– KAKAO 2018 :Harvest Fest Traffic]]
	- time handling is the key of this problem.
	- finding an efficient algorithm for maximum number of traffic during one second was quite hard but not a terrible.
	- but handling time was terrible. First, I handle hour, minute, sec respectively. but I didn’t need that complexity. so I convert all the thing to second. I mean, hour * 3600000, min * 60000, sec* 1000.
	since, they gave second to 3 decimal places.
	- the finding algorithm I mentioned avobe is below
	> 1. take a end time of traffic.
	> 2. add 1 sec.
	> 3. iterate all the traffic and check there is traffic between the duration.
	- see the code. p.s) I didn’t use visual studio for this problem. so there is no color :)
	#include <string>
	#include <vector>
	#include<sstream>
	#include<unordered_map>
	#include<iostream>
	#include<algorithm>
	using namespace std;
	
	
	
	vector<pair<int,int>> Input(vector<string>& lines){
	    vector<pair<int,int>> date(lines.size());
	    for(int i=0;i<lines.size();i++){
	        stringstream ss(lines[i]);
	        string hour; string min; string sec;string process;
	        getline(ss,hour,' ');//remove date
	        getline(ss,hour,':'); getline(ss,min,':'); getline(ss,sec,' '); getline(ss,process,'s');
	        date[i].second=stod(hour)*3600000 + stod(min)*60000 + stod(sec)*1000;
	        date[i].first=date[i].second-stod(process)*1000+1;
	    }
	    return date;
	}
	int findNumber(vector<pair<int,int>> res){
	    vector<int> table(res.size());
	    for(int i=0;i<res.size();i++){
	        int start=res[i].second;
	        int end=res[i].second+999;
	        for(int j=i;j<res.size();j++){
	            if(res[j].second<start || end<res[j].first) continue;
	            table[i]++;
	        }
	    }
	    return *max_element(table.begin(),table.end());
	}
	
	int solution(vector<string> lines) {
	    int answer = 0;
	    vector<pair<int,int>> date;
	    date=Input(lines);
	    answer=findNumber(date);
	    return answer;
	}
	
	
