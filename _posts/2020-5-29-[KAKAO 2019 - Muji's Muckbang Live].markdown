---
layout: post
title: [KAKAO 2019 - Muji's Muckbang Live]
date: 2020-5-29
description: txt to markdown
thumbnail: food1.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}

	﻿[129. [Programmers– KAKAO 2019 :Muji’s Muckbang Live]]
	- this problem has efficiency test as well.
	- as you guess, I passed accuracy tests but not efficiency tests.
	- below code is the code passing accuracy tests.
	#include <string>
	#include <vector>
	#include<iostream>
	#include<algorithm>
	#include<map>
	using namespace std;
	
	vector<int> ReduceNumber(vector<int> food_times,int eat_number) {
		for (long i = 0; i < food_times.size(); i++) {
			if (food_times[i] == 0) continue;
			else food_times[i] -= eat_number;
		}
		return food_times;
	}
	
	void printTable(vector<int> food_times) {
		for (int i : food_times)
			cout << i << " ";
		cout << endl<<endl;
	}
	
	int solution(vector<int> food_times, long long k) {
		int answer = 0;
		int rest_food = food_times.size();
		long long cur_index = 0;
		long long eat_number = 0;
	
	
		map<long long, int> min_table;
		for (int i = 0; i < food_times.size(); i++) min_table[food_times[i]] += 1;
		map<long long, int>::iterator iter = min_table.begin();
	
		long long min_food = iter->first;
		int min_food_size = iter->second;
		long long  accumulated_eat_number = 0;
		//cout << "Begining" << endl;
		//printTable(food_times);
		while (true) {
			if (k >= rest_food) {
				eat_number++;
				k -= rest_food;
				if (eat_number == min_food) {
					accumulated_eat_number += eat_number;
					food_times = ReduceNumber(food_times, eat_number);
					//printTable(food_times);
					rest_food -= min_food_size;
					iter++;
					eat_number = 0;
					if (iter != min_table.end()) {
						min_food = iter->first-accumulated_eat_number;
						//cout << "next min_food : " << min_food << endl;
						min_food_size = iter->second;
					}
					else {
						//cout << "여기 처리" << endl;
						return -1;
					}
				}
			}
			else {
				long long i;
				if(eat_number) food_times=ReduceNumber(food_times, eat_number);
				//cout << "<<Last Traversal>>"<< endl;
				//cout << "	- Remain k : " << k << " - Remain eat_number : " << eat_number << endl;
				//printTable(food_times);
				for (i = 0; i <food_times.size() && k>0; i++) {
					if (food_times[i] == 0) continue;
					else {
						food_times[i]--;
						k--;
					}
				}
				//cout << "!!!Final!!!" << endl;
				//printTable(food_times);
				cur_index = i%food_times.size();
				bool flag = true;
				for (long i = cur_index; i < food_times.size(); i++) if (food_times[i]) { cur_index = i; flag = false; break; }
				if (flag) for (long i = 0; i < food_times.size(); i++) if (food_times[i]) { cur_index = i; flag = false; break; }
				if (flag && i == food_times.size()) return -1;
				break;
			}
		}
		return cur_index+1;
	}
	
	int main() {
		cout<<solution({ 1,2,3},1);
		return 0;
	}
	
	- Let’s find another algorithm to pass efficiency test!
	- I refered to a site to pass the efficiency tests.
	- there are so many geinous…. the point is I don’t need to reduce food’s count. just sort with indice and if Muji can eat a current minimum food, find next food, and so on…
	- see the code.
	#include <string>
	#include <vector>
	#include<iostream>
	#include<algorithm>
	#include<map>
	#include<bitset>
	using namespace std;
	
	int solution(vector<int> foods, long long k) {
		vector<pair<int, int>> food_times;
		for (int i = 0; i < foods.size(); i++) food_times.push_back(make_pair(foods[i], i + 1));
		int fs = foods.size();
		sort(food_times.begin(), food_times.end());
		long long accumulated_min_food=0;
		for (vector<pair<int, int>>::iterator iter = food_times.begin(); iter != food_times.end(); iter++) {
			long long min_food = (long long)(iter->first - accumulated_min_food) * fs;
			if (min_food == 0) {
				fs--;
				continue;
			} 
			else if (min_food <= k) {
				k -= min_food;
				accumulated_min_food = iter->first;
				fs--;
			}
			else {
				k %= fs;
				sort(iter, food_times.end(), [](pair<int, int> a, pair<int, int> b) {return a.second < b.second; });
				return (iter + k)->second;
			}
		}
		return -1;
	}
	
	int main() {
		cout<<solution({10,6,4,3,2,5,15,9,6,5,4,3,2},60);
		return 0;
	}
	
{% endhighlight %}
