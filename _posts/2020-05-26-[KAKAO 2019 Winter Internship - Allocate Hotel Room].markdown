---
layout: post
title: [KAKAO 2019 Winter Internship - Allocate Hotel Room]
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}
	﻿[178. [KAKAO 2019 – Winter Internship : Allocate Hotel Room]
	- this problem has efficiency test. the key was the union-find structure.
	- but without knowing union-find structure, we colud solve it. I’ve solved this problem using recursion with unorderd_map.
	- the map has pair as a value, the first of the pair is prev, the second is next. but I think now, I just need the second. so we just have to make unordered_map<int,int> structure.
	- if map[input_room] is empty, then we just push the room number into answer vector.
	- if the map is not empty, then give the map[input_room].second to next recursion until we find empty room. after that, we revise each key’s second to new next room.
	- it’s hard to describe in written language. just see the code.
	#include <string>
	#include <vector>
	#include <unordered_map>
	using namespace std;
	unordered_map<long long, pair<long long, long long>> next_room;
	vector<long long> answer;
	void recursion(long long wanted_room) {
		if (next_room.find(wanted_room) == next_room.end()) {
			answer.emplace_back(wanted_room);
			next_room[wanted_room].first = 0;
			next_room[wanted_room].second = wanted_room + 1;
			return;
		}
		else {
			recursion(next_room[wanted_room].second);
			long long next = next_room[next_room[wanted_room].second].second;
			next_room[wanted_room].second = next;
			return;
		}
	}
	
	vector<long long> solution(long long k, vector<long long> room_number) {
		for (long long wanted_room : room_number) {
			recursion(wanted_room);
		}
		return answer;
	}
	
{% endraw %}
