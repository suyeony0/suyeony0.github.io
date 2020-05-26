---
layout: post
title: [1238  Circular Permutation in Binary Representation]
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}
	﻿[91. [1238] Circular Permutation in Binary Representation – return a permutation such that p[i] and p[i+1] differ by only one bit in their binary representation]
	- My algorithm is below.
	> 1. put string “0” and “1” into vector table as a initial values. since n’s least limit is 1.
	> 2. push_back the strings in the vector table in a reverse order.
	> 3. add 0’s for the number of table.size()/2 and add 1’s for the rest.
	> 4. From 1 to n, repeat the algorithm from 2 to 4.
	> 5. reverse all the string in the vector table.
	> 6. covert all the string in the vector table to int. the method is below.
	>>> Notice: usage of stoi
	 int i = std::stoi("01000101", nullptr, 2);
	•	The returned value is the converted int value.
	•	The first argument is the std::string you want to convert.
	•	The second is a size_t * where it'll save the index of the first non digit character.
	•	The third is an int that corresponds to the base that'll be used for conversion..
	> 7. find start position and reconstruct vector to return.
	- refer to the picture I drew.
	 
	- the speed was not good. It was just 9.85% beats.
	class Solution {
	public:
	    void reverseConcatenate(vector<string>& table){
	        for(int i=table.size()-1;i>=0;i--)
	            table.push_back(table[i]);
	    }
	    void addBits(vector<string>& table){
	        for(int i=0;i<table.size()/2;i++)
	            table[i]+='0';
	        for(int i=table.size()/2;i<table.size();i++)
	            table[i]+='1';
	    }
	    void reverseStrings(vector<string>& table){
	        for(int i=0;i<table.size();i++)
	            reverse(table[i].begin(),table[i].end());
	    }
	    vector<int> binaryToInt(vector<string> table){
	        vector<int> answer;
	        for(string s : table)
	            answer.push_back(std::stoi(s,nullptr,2));
	        return answer;
	           
	    }
	    vector<int> circularPermutation(int n, int start) {
	        vector<string> table={"0","1"};
	        for(int i=2;i<=n;i++){
	            reverseConcatenate(table);
	            addBits(table);
	        }
	        reverseStrings(table);
	        vector<int> answer=binaryToInt(table);
	        vector<int>::iterator iter=find(answer.begin(),answer.end(),start);
	        vector<int> res={iter,answer.end()};
	        for(vector<int>::iterator res_iter=answer.begin();res_iter!=iter;res_iter++)
	            res.push_back(*res_iter);
	        return res;
	    }
	};
	
	
{% endraw %}
