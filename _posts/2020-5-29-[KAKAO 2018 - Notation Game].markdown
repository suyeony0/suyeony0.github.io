---
layout: post
title: [KAKAO 2018 - Notation Game]
date: 2020-5-29
description: txt to markdown
thumbnail: food2.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}

	﻿[156. [KAKAO – 2018 : Notation Game]]
	- this was final problem of KAKAO. By solving this problem, I’ve solved all the KAKAO coding test problem and part of SAMSUNG SW :)
	- the way to make string for given notation is the key point of this problem. 
	- I made whole string first, actually the string was over calculated, but time limit was okay.
	- After that, just finding Muzi’s turn, that was all.
	- see the code.
	#include <string>
	#include <vector>
	#include<algorithm>
	#include<iostream>
	using namespace std;
	
	string solution(int n, int t, int m, int p) {
	    string answer = "";
	    string alpha="0123456789ABCDEF";
	    string total_string="0";
	    for(int i=1;i<t*m;i++){
	        string temp="";
	        int number=i;
	        while(number>0){
	            int res=number%n;
	            number=number/n;
	            temp+=alpha[res];
	        }
	        reverse(temp.begin(),temp.end());
	        total_string+=temp;
	    }
	    int count=0;
	    for(int i=p-1;i<total_string.size();i+=m){
	        if(count>=t) break;
	        answer+=total_string[i];
	        count++;
	    }
	    return answer;
	}
	
{% endhighlight %}
