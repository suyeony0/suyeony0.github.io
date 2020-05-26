---
layout: post
title: {% raw %}[Samsung SW - Polynomial Calculation]{% endraw %}
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}
	﻿#include<iostream>
	#include<vector>
	
	using namespace std;
	vector<long long> getFn(vector<vector<int>> operand, vector<long long> Xs) {
		vector<long long> res;
		for (const int x : Xs) {
			vector<long long> Fn = { 1,x }; 
			for (vector<int> row : operand) {
				int t = row[0]; int a = row[1]; int b = row[2];
				if (t == 1) {
					Fn.emplace_back((Fn[a]+Fn[b])% 998244353);
				}
				else if (t == 2) {
					Fn.emplace_back((a * Fn[b])% 998244353);
				}
				else if(t==3){
					Fn.emplace_back((Fn[a] * Fn[b])% 998244353);
				}
			}
			res.emplace_back(Fn.back());
		}
		return res;
	}
	int main(int argc, char** argv)
	{
		int test_case;
		int T;
		cin >> T;
		
		
		for (test_case = 1; test_case <= T; ++test_case)
		{
			vector<vector<int>> operand;
			vector<long long> Xs;
			vector<long long> res;
			//get input
			int N; cin >> N;
			int t, a, b;
			for (int i = 2; i <= N; i++) {
				cin >> t >> a >> b;
				operand.emplace_back(vector<int>{t, a, b});
			}
			int M; cin >> M;
			int k;
			for (int i = 0; i < M; i++) {
				cin >> k;
				Xs.emplace_back(k);
			}
			res=getFn(operand,Xs);
			cout << "#" << test_case;
			for (int i=0;i<res.size();i++)
				cout << " " << res[i];
			cout << endl;
		}
		return 0;
	}
{% endraw %}
