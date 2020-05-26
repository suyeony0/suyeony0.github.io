---
layout: post
title: [KAKAO 2019 - Matching Score]
data: 2020-05-26
desciption: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

	﻿[131. [Programmers– KAKAO 2019 :Matching Score]]
	- I hate fucking parsing string!!! there is too many condition to check.
	- I spent almost 4 hour to parse this fucking problem.
	- see the code.
	#include <string>
	#include <vector>
	#include<iostream>
	#include<algorithm>
	#include<sstream>
	#include<map>
	#include<unordered_set>
	#define min(a,b) a>b? b:a
	using namespace std;
	
	map<string, pair<unordered_set<string>,vector<int>>> links; // URL - <{in links},{base,out links,index}>
	vector<string> URL_list;
	vector<string> Lower(vector<string> pages) {
		for (int i = 0; i < pages.size(); i++) {
			std::transform(pages[i].begin(), pages[i].end(), pages[i].begin(), ::tolower);
		}
		return pages;
	}
	string RemoveDelimeter(string s) {
		for (int i = 0; i < s.size(); i++) {
			if ('a' <= s[i] && s[i] <= 'z') continue;
			else s[i] = ' ';
		}
		return s;
	}
	
	vector<int> FindWord(vector<string> pages,string word) {
		vector<int> baseScore(pages.size(),0);
		int i = 0;
		for (string s : pages) {
			s = RemoveDelimeter(s);
			stringstream ss(s);
			string token;
			while (getline(ss, token,' ')){
				if (token == word) baseScore[i]++;
			}
			i++;
		}
		return baseScore;
	}
	void printPage(string s) {
		cout << s << endl;
	}
	void GetURL(vector<string> pages) {
		for (int i = 0; i < pages.size(); i++) {
			string cur_URL = "";
			string now = pages[i];
			while (cur_URL == "") {
				int start = now.find("<meta") + 5;
				now = now.substr(start);
				int last = now.find(">");
				start = now.find("https://");
				if (start > last) continue;
				now = now.substr(start);
				stringstream ss(now);
				string token;
				getline(ss, token, '\"');
				cur_URL = token;
				URL_list.push_back(cur_URL);
				links[cur_URL] = make_pair(unordered_set<string>{}, vector<int>{0, 0, i});
			}
		}
	}
	
	void GetLinks(vector<string> pages) {
		for (int i = 0; i < pages.size(); i++) {
			string now = pages[i];
			string cur_URL = URL_list[i];
			int start = now.find("<body>");
			int last = now.find("</body>");
			now = now.substr(start, last - start + 7); //partition of body tag.
			while(true) {
				start = now.find("<a href");
				if (start == string::npos) break;
				now = now.substr(start);
				start = 0;
				last = now.find(">");
				if (start > last) break;
				start = now.find("https://");
				if (start != string::npos) links[cur_URL].second[1]++; //outer ++
				now = now.substr(start);
				stringstream ss(now);
				string token;
				getline(ss, token, '\"');
				if (links.find(token) != links.end()) links[token].first.insert(cur_URL);
			};
			
			
		}
	}
	
	double GetLinkScore(unordered_set<string> inLinks) {
		unordered_set<string>::iterator iter = inLinks.begin();
		double sum = 0;
		for (; iter != inLinks.end(); iter++) {
			//cout << links[*iter].second[0] << "," << links[*iter].second[1] << endl;
			//cout << "result : " << double(links[*iter].second[0]) / double(links[*iter].second[1]) << endl;
			sum+=double(links[*iter].second[0]) / double(links[*iter].second[1]);
		}
		//cout << sum << endl;
		return sum;
	}
	
	void printLinks() {
		for (auto iter = links.begin(); iter != links.end(); iter++) {
			cout << "URL : " << iter->first << endl;
			cout << " base score : " << iter->second.second[0];
			cout << " out links : " << iter->second.second[1];
			cout << " in links : ";
			for (auto iter2 = iter->second.first.begin(); iter2 != iter->second.first.end(); iter2++) {
				cout << *iter2 << endl;
			}
			cout << endl << endl;;
		}
	}
	
	int solution(string word, vector<string> pages) {
		//for (string s : pages) printPage(s);
		int answer = 0;
		transform(word.begin(), word.end(), word.begin(), ::tolower);
		pages = Lower(pages); // make it lowercase
		vector<int> baseScore=FindWord(pages,word); // get base score
		GetURL(pages);
		GetLinks(pages);
		map<string, pair<unordered_set<string>, vector<int>>>::iterator iter = links.begin();
		for (; iter != links.end(); iter++) iter->second.second[0] = baseScore[iter->second.second[2]];
		//printLinks();
	
		
		vector<pair<int,double>> res(pages.size());//index, sum of score;
		iter = links.begin();
		for (int i = 0; iter != links.end();i++, iter++) {
			res[i] = make_pair(iter->second.second[2], iter->second.second[0] + GetLinkScore(iter->second.first));
		}
		sort(res.begin(), res.end(), [](pair<int, double> a, pair<int, double> b) { return a.second > b.second; });
		double maximum = res[0].second;
		int index=res[0].first;
		for (int i = 0; i < res.size(); i++) {
			if (res[i].second != maximum) break;
			index = min(index, res[i].first);
		}
		
		return index;
	}
	
	int main() {
		/*cout<<solution("blind",{ "<html lang=\"ko\" xml:lang=\"ko\" xmlns=\"http://www.w3.org/1999/xhtml\">\n<head>\n  <meta charset=\"utf-8\">\n  <meta property=\"og:url\" content=\"https://a.com\"/>\n</head>  \n<body>\nBlind Lorem Blind ipsum dolor Blind test sit amet, consectetur adipiscing elit. \n<a href=\"https://b.com\"> Link to b </a>\n</body>\n</html>", "<html lang=\"ko\" xml:lang=\"ko\" xmlns=\"http://www.w3.org/1999/xhtml\">\n<head>\n  <meta charset=\"utf-8\">\n  <meta property=\"og:url\" content=\"https://b.com\"/>\n</head>  \n<body>\nSuspendisse potenti. Vivamus venenatis tellus non turpis bibendum, \n<a href=\"https://a.com\"> Link to a </a>\nblind sed congue urna varius. Suspendisse feugiat nisl ligula, quis malesuada felis hendrerit ut.\n<a href=\"https://c.com\"> Link to c </a>\n</body>\n</html>", "<html lang=\"ko\" xml:lang=\"ko\" xmlns=\"http://www.w3.org/1999/xhtml\">\n<head>\n  <meta charset=\"utf-8\">\n  <meta property=\"og:url\" content=\"https://c.com\"/>\n</head>  \n<body>\nUt condimentum urna at felis sodales rutrum. Sed dapibus cursus diam, non interdum nulla tempor nec. Phasellus rutrum enim at orci consectetu blind\n<a href=\"https://a.com\"> Link to a </a>\n</body>\n</html>" })<<endl;*/
		//cout << solution("Muzi", { "<html lang=\"ko\" xml:lang=\"ko\" xmlns=\"http://www.w3.org/1999/xhtml\">\n<head>\n  <meta charset=\"utf-8\">\n  <meta property=\"og:url\" content=\"https://careers.kakao.com/interview/list\"/>\n</head>  \n<body>\n<a href=\"https://programmers.co.kr/learn/courses/4673\"></a>#!MuziMuzi!)jayg07con&&\n\n</body>\n</html>", "<html lang=\"ko\" xml:lang=\"ko\" xmlns=\"http://www.w3.org/1999/xhtml\">\n<head>\n  <meta charset=\"utf-8\">\n  <meta property=\"og:url\" content=\"https://www.kakaocorp.com\"/>\n</head>  \n<body>\ncon%\tmuzI92apeach&2<a href=\"https://hashcode.co.kr/tos\"></a>\n\n\t^\n</body>\n</html>" })<<endl;
		return 0;
	}
	
