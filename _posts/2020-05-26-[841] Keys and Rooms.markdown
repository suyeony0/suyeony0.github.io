---
layout: post
title: [841] Keys and Rooms
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}
	﻿[87. [841] Keys and Rooms – each room has a list of keys to enter rooms. return true if it is possible to enter every room]
	- Algorithm is below.
	> 1. when I enter a room, inserting every key into queue and recording all the key into can_visit. Finally, removing all the key in the room.
	> 2. pop a key from the queue, if I already visited the key’s room, continue. otherwise repeat from 1.
	> 3. when queue is empty, checking whether the given the number of rooms is same to can_visit.
	- the speed was 68.01% beats.
	- see the code.
	class Solution {
	public:
	    bool canVisitAllRooms(vector<vector<int>>& rooms) {
	        unordered_set<int> can_visit;
	        queue<int> que;
	        int cur_room;
	        can_visit.insert(0);
	        for(int i : rooms[0]){
	            que.push(i);
	            can_visit.insert(i);
	        }
	        rooms[0].clear();
	        while(!que.empty()){
	            cur_room=que.front();
	            que.pop();
	            if(rooms[cur_room].empty()) continue;
	            for(int i : rooms[cur_room]){
	                que.push(i);
	                can_visit.insert(i);
	            }
	            rooms[cur_room].clear();
	        }
	        return rooms.size()==can_visit.size();
	    }
	};
	
{% endraw %}
