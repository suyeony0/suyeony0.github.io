---
layout: post
title: [KAKAO 2018 - Secret Map]
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

	﻿[139. [Programmers– KAKAO 2018 :Secret Map]]
	- Handling bitset is the main point of this problem.
	- So It was easy for me :)
	- see the code.
	#include <string>
	#include <vector>
	#include<iostream>
	#include<bitset>
	using namespace std;
	
	vector<string> solution(int n, vector<int> arr1, vector<int> arr2) {
	    vector<string> answer;
	    vector<bitset<16>> table;
	    for(int i=0;i<n;i++){
	        bitset<16> a; bitset<16> b;
	        a=arr1[i]; b=arr2[i];
	        table.push_back(a|b);
	    }
	    for(int i=0;i<table.size();i++){
	        string temp="";
	        for(int j=n-1;j>=0;j--){
	            if(table[i][j]==1) temp+="#";
	            else temp+=" ";
	        }
	        answer.push_back(temp);
	    }
	    
	    return answer;
	}
	
