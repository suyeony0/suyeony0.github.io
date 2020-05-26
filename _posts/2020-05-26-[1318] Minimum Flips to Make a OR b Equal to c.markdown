---
layout: post
title: {% raw %}[1318] Minimum Flips to Make a OR b Equal to c{% endraw %}
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}
	﻿[94. [1318] Minimum Flips to Make a OR b Equal to c – return how many filps we need to make a OR b == c]
	- Algorithm is below.
	> 1. given a,b and c, convert these to bitset.
	> 2. if C[i]==1 and A[i]==0 and B[i]==0, then filp++;
	> 3. if C[i]==0 and A[i]==1 ,flip++ ,or B[i]==1, filp++; where 0<= i < log2(max(a,b,c)) +1
	- the speed was 100% beats.
	-see the code.
	class Solution {
	public:
	    int minFlips(int a, int b, int c) {
	        bitset<30> A(a);
	        bitset<30> B(b);
	        bitset<30> C(c);
	        int maximum=max(a,(max(b,c)));
	        int max_count=log2(maximum)+1;
	        int flip=0;
	        for(int i=0;i<max_count;i++){
	            if(C[i] && !A[i] && !B[i]){
	                flip++;
	            }
	            else if(!C[i]){
	                if(A[i]) flip++;
	                if(B[i]) flip++;
	            }
	        }
	        return flip;
	    }
	};
	
{% endraw %}
