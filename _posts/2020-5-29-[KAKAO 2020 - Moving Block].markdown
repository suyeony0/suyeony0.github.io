---
layout: post
title: [KAKAO 2020 - Moving Block]
date: 2020-5-29
description: txt to markdown
thumbnail: city2.jpg
categories: Algorithm

# Information for the author block
author : Loui
---

{% raw %}

	﻿[125. [Programmers– KAKAO 2020 : Moving Block]]
	- At first, I used DFS to implement brute force, but I failed lots of test case and time limit exceeded occurred.
	- see the code.
	#include <string>
	#include <vector>
	#include<iostream>
	#include<climits>
	#define min(a,b) a>b ? b:a
	using namespace std;
	int minimum = INT_MAX;
	typedef struct cell {
		bool wall=false;
		bool right = false;
		bool down = false;
	
	}cell;
	
	void printTable(vector<vector<int>> table) {
		for (vector<int> row : table) {
			for (int i : row) {
				cout << i << " ";
			}
			cout << endl;
		}
	}
	
	void DFS(vector<vector<int>> board, vector<vector<cell>> visit, int bs, int x, int y, bool isRight, int count) {
		// initialize
		int rx; int ry;
		if (isRight) { rx = x; ry = y + 1; visit[x][y].right = true; }
		else { rx = x + 1; ry = y; visit[x][y].down = true; }
		//cout << "x : " << x << " y : " << y <<" Right : "<<isRight<< endl;
		// check arriving
		if (rx == bs - 1 && ry == bs - 1) { minimum = min(minimum, count); return; }
		// DFS
		//cout << " x : " << x << " y : " << y <<" rx : "<<rx<<" ry : "<<ry<< " Right : "<<isRight<<" count : "<<count<< endl;
		// isRight
		if (isRight) {
			//cout << "right" << endl;
			//move
			//right
			if (ry + 1 < bs && board[rx][ry + 1] == 0 && visit[rx][ry].right == false) { DFS(board, visit, bs, rx, ry, true, count + 1); }
			//down
			if (x + 1 < bs && board[x + 1][y] == 0 && board[rx + 1][ry] == 0 && visit[x + 1][y].right == false) { DFS(board, visit, bs, x + 1, y, true, count + 1); }
			//left 
			if (y - 1 >= 0 && board[x][y-1] == 0 && visit[x][y-1].right == false) { DFS(board, visit, bs, x, y-1, true, count + 1); }
			//up
			if (x - 1 >= 0 && board[x - 1][y] == 0 && board[rx - 1][y] == 0 && visit[x - 1][y].right == false) { DFS(board, visit, bs, x - 1, y, true, count + 1); }
	
			//rotate
			//left axis - clockwise
			//cout << "1" << endl;
			if (rx < bs && ry < bs &&x+1<bs&& board[rx+1][ry] == 0&& board[x+1][y]==0 && visit[x][y].down == false) { DFS(board, visit, bs, x, y, false, count + 1); }
			//left axis - anticlockwise
			//cout << "2" << endl;
			if (rx < bs && ry << bs && x - 1 >= 0 && board[rx - 1][ry] == 0 && board[x - 1][y] == 0 && visit[x - 1][y].down == false) { DFS(board, visit, bs, x - 1, y, false, count + 1); }
			//right axis - clockwise
			//cout << "3" << endl;
			if (x - 1 >= 0 && board[x - 1][y] == 0 && board[rx - 1][ry] == 0 && visit[rx - 1][ry].down == false) { DFS(board, visit, bs, rx - 1, ry, false, count + 1); }
			//right axis - anticlockwise
			//cout << "4" << endl;
			if (x + 1 < bs && board[x + 1][y] == 0 && board[rx + 1][rx] == 0 && visit[rx][ry].down == false) { DFS(board, visit, bs, rx, ry, false, count + 1); }
		}
		// is Down
		else {
			//cout << "down" << endl;
			//move
			//right
			if (y + 1 < bs && board[x][y + 1] == 0 && board[rx][ry + 1] == 0 && visit[x][y + 1].down == false) { DFS(board,visit,bs,x,y+1,false,count+1); }
			//down
			if (rx + 1 < bs && board[rx + 1][y] == 0 && visit[rx][rx].down == false) { DFS(board, visit, bs, rx, ry, false, count + 1); }
			//left
			if (y - 1 >= 0 && board[x][y - 1] == 0 && board[rx][ry - 1] == 0 && visit[x][y - 1].down == false) { DFS(board, visit, bs, x, y - 1, false, count + 1); }
			//up
			if (x - 1 >= 0 && board[x - 1][y] == 0 && visit[x - 1][y].down == false) { DFS(board, visit, bs, x - 1, y, false, count + 1); }
	
			//rotate
			//top axis - clockwise
			//cout << "5" << endl;
			if (y - 1 >= 0 && board[x][y - 1] == 0 && board[rx][ry - 1] == 0 && visit[x][y - 1].right == false) { DFS(board, visit, bs, x , y-1, true, count + 1); }
			//top axis - anticlockwise
			//cout << "6" << endl;
			if (y + 1 < bs && board[x][y+1] == 0 && board[rx][ry + 1] == 0 && visit[x][y].right == false) { DFS(board, visit, bs, x, y, true, count + 1); }
			//bottom axis - clockwise
			//cout << "7" << endl;
			if (y + 1 < bs && board[x][y + 1] == 0 && board[rx][ry + 1] == 0 && visit[rx][ry].right == false) { DFS(board, visit, bs, rx, ry, true, count + 1); }
			//bottom axis - anticlockwise
			//cout << "8" << endl;
			if (y - 1 >= 0 && board[x][y - 1] == 0 && board[rx][ry - 1] == 0 && visit[rx][ry - 1].right == false) { DFS(board, visit, bs, rx, ry - 1, true, count + 1); }
		}
	}
	
	int solution(vector<vector<int>> board) {
		int answer = 0;
		int bs = board.size();
		vector<vector<cell>> visit(bs,vector<cell>(bs));
		for (int i = 0; i < bs; i++) {
			for (int j = 0; j < bs; j++) {
				if (board[i][j] == 1) visit[i][j].wall = true;
			}
		}
		//printTable(board);
		//cout << endl;
		DFS(board, visit, bs,0,0,true,0);
		answer = minimum;
		return answer;
	}
	
	int main() {
		cout << solution({ {0, 0, 0, 1, 1}, {0, 0, 0, 1, 0}, {0, 1, 0, 1, 1}, {1, 1, 0, 0, 1}, {0, 0, 0, 0, 0} });
		return 0;
	}
	
	- so I had to change the algorithm to BFS and revise some codes but time limit exceeded occurred also.
	- below is the BFS code I used.
	
	int BFS(vector<vector<int>> board, vector<vector<cell>> visit, int bs, int x, int y, bool isRight) {
		queue < pair<vector<vector<cell>>, vector<int>>> que;
		int count = 0;
		int rx, ry;
		que.push(make_pair(visit, vector<int>{x, y, isRight, count}));
		while (!que.empty()) {
			visit = que.front().first;
			vector<int> front = que.front().second;
			x = front[0]; y = front[1]; isRight = front[2]; count = front[3];
			que.pop();
			if (isRight) { rx = x; ry = y + 1; visit[x][y].right = true; }
			else { rx = x + 1; ry = y; visit[x][y].down = true; }
			if (rx == bs - 1 && ry == bs - 1) return count;
			
			if (isRight) {
				//move
				//right
				if (ry + 1 < bs && board[rx][ry + 1] == 0 && visit[rx][ry].right == false) 
				{ que.push(make_pair(visit,vector<int>{ rx, ry, true, count + 1 })); }
				//down
				if (x + 1 < bs && board[x + 1][y] == 0 && board[rx + 1][ry] == 0 && visit[x + 1][y].right == false) 
				{ que.push(make_pair(visit, vector<int>{ x+1, y, true, count + 1 })); }
				//left 
				if (y - 1 >= 0 && board[x][y - 1] == 0 && visit[x][y - 1].right == false) 
				{ que.push(make_pair(visit, vector<int>{ x, y-1, true, count + 1 })); }
				//up
				if (x - 1 >= 0 && board[x - 1][y] == 0 && board[rx - 1][y] == 0 && visit[x - 1][y].right == false) 
				{ que.push(make_pair(visit, vector<int>{ x-1, y, true, count + 1 })); }
	
				//rotate
				//left axis - clockwise
				if (x+1<bs && board[rx + 1][ry] == 0 && board[x + 1][y] == 0 && visit[x][y].down == false) 
				{ que.push(make_pair(visit, vector<int>{ x, y, false, count + 1 })); }
				//left axis - anticlockwise
				if (x - 1 >= 0 && board[rx - 1][ry] == 0 && board[x - 1][y] == 0 && visit[x - 1][y].down == false) 
				{que.push(make_pair(visit, vector<int>{ x-1, y, false, count + 1 }));	}
				//right axis - clockwise
				if (x - 1 >= 0 && board[x - 1][y] == 0 && board[rx - 1][ry] == 0 && visit[rx - 1][ry].down == false) 
				{ que.push(make_pair(visit, vector<int>{ rx-1, ry, false, count + 1 }));	}
				//right axis - anticlockwise
				if (x + 1 < bs && board[x + 1][y] == 0 && board[rx + 1][ry] == 0 && visit[rx][ry].down == false) 
				{ que.push(make_pair(visit, vector<int>{ rx, ry, false, count + 1 }));}
			}
			else {
				//move
				//right
				if (y + 1 < bs && board[x][y + 1] == 0 && board[rx][ry + 1] == 0 && visit[x][y + 1].down == false) 
				{ que.push(make_pair(visit, vector<int>{ x, y+1, false, count + 1 })); }
				//down
				if (rx + 1 < bs && board[rx + 1][y] == 0 && visit[rx][ry].down == false)
				{ que.push(make_pair(visit, vector<int>{ rx, ry, false, count + 1 })); }
				//left
				if (y - 1 >= 0 && board[x][y - 1] == 0 && board[rx][ry - 1] == 0 && visit[x][y - 1].down == false) 
				{ que.push(make_pair(visit, vector<int>{ x, y-1, false, count + 1 })); }
				//up
				if (x - 1 >= 0 && board[x - 1][y] == 0 && visit[x - 1][y].down == false) 
				{ que.push(make_pair(visit, vector<int>{ x-1, y, false, count + 1 }));  }
	
				//rotate
				//top axis - clockwise
				if (y - 1 >= 0 && board[x][y - 1] == 0 && board[rx][ry - 1] == 0 && visit[x][y - 1].right == false) 
				{ que.push(make_pair(visit, vector<int>{ x, y-1, true, count + 1 })); }
				//top axis - anticlockwise
				if (y + 1 < bs && board[x][y + 1] == 0 && board[rx][ry + 1] == 0 && visit[x][y].right == false) 
				{ que.push(make_pair(visit, vector<int>{ x, y, true, count + 1 }));  }
				//bottom axis - clockwise
				if (y + 1 < bs && board[x][y + 1] == 0 && board[rx][ry + 1] == 0 && visit[rx][ry].right == false) 
				{ que.push(make_pair(visit, vector<int>{ rx, ry, true, count + 1 }));  }
				//bottom axis - anticlockwise
				if (y - 1 >= 0 && board[x][y - 1] == 0 && board[rx][ry - 1] == 0 && visit[rx][ry - 1].right == false)
				{ que.push(make_pair(visit, vector<int>{ rx, ry-1, true, count + 1 }));  }
			}
		}
		return 0;
	}
	
	- so I made NewBFS, I got all test cases’ mark but, time limit exceeded occurred at tc 13, 14.
	- see the NewBFS code.
	
	int NewBFS(vector<vector<cell>> visit) {
		int bs = visit.size();
		queue<vector<int>> que;
		que.push(vector<int>{0, 0, 1,0});//x,y, isRIght;
		while ( !que.empty()) {
			int x = que.front()[0]; int y = que.front()[1]; bool isRight = que.front()[2]; int count = que.front()[3];
			que.pop();
			if (isRight && x == bs - 1 && y + 1 == bs - 1) return count;
			else if (x + 1 == bs - 1 && y == bs - 1) return count;
			isRight ? visit[x][y].right = false : visit[x][y].down = false;
	
			if (isRight) {
				//move
				if (y + 2 < bs && visit[x][y + 1].right&& visit[x][y+2].wall) que.push(vector<int>{x, y + 1, true, count + 1});
				if (y-1>=0 && visit[x][y-1].right && visit[x][y-1].wall) que.push( vector<int>{x, y -1, true, count + 1});
				if(x+1<bs && visit[x+1][y].wall && visit[x+1][y+1].wall && visit[x+1][y].right) que.push(vector<int>{x+1, y, true, count + 1});
				if(x-1>=0 && visit[x-1][y].wall && visit[x-1][y+1].wall && visit[x-1][y].right) que.push(vector<int>{x-1, y, true, count + 1});
				//rotate
				if (x + 1 < bs &&  visit[x + 1][y].wall &&  visit[x + 1][y + 1].wall ) {
					if( visit[x][y].down) que.push( vector<int>{x, y, false, count + 1});
					if( visit[x][y + 1].down) que.push(vector<int>{x, y+1, false, count + 1});
				} 
				if (x - 1 >= 0 &&  visit[x - 1][y].wall &&  visit[x - 1][y + 1].wall ) {
					if( visit[x - 1][y].down) que.push( vector<int>{x - 1, y, false, count + 1});
					if( visit[x - 1][y + 1].down) que.push(vector<int>{x - 1, y + 1, false, count + 1});
				} 
			}
			else {
				//move
				if(y+1<bs &&  visit[x][y+1].wall &&  visit[x+1][y+1].wall &&  visit[x][y+1].down) que.push(vector<int>{x, y+1, false, count + 1});
				if(y-1>=0 &&  visit[x][y-1].wall &&  visit[x+1][y-1].wall &&  visit[x][y-1].down) que.push(vector<int>{x, y-1, false, count + 1});
				if(x+2<bs &&  visit[x+2][y].wall &&  visit[x+1][y].down) que.push(vector<int>{x+1, y, false, count + 1});
				if(x-1>=0 &&  visit[x-1][y].wall &&  visit[x-1][y].down) que.push(vector<int>{x-1, y, false, count + 1});
				//rotate
				if (y + 1 < bs &&  visit[x][y + 1].wall &&  visit[x + 1][y + 1].wall) {
					if( visit[x][y].right) que.push( vector<int>{x, y, true, count + 1});
					if( visit[x+1][y].right) que.push( vector<int>{x+1, y, true, count + 1});
				}
				if (y - 1 >= 0 &&  visit[x][y - 1].wall &&  visit[x + 1][y - 1].wall) {
					if( visit[x][y-1].right) que.push(vector<int>{x, y-1, true, count + 1});
					if( visit[x+1][y-1].right) que.push(vector<int>{x+1, y-1, true, count + 1});
				}
			}
		}
		return 0;
	}
	
	- I resolved the time limit exceeded at tc 13,14 by changing the location of allocating visit state.
	- before I changed it, I allocate visit state when I poped the queue.front().
	- but I changed it before I pushed a state into queue.
	- see the code.
	#include <string>
	#include <vector>
	#include<iostream>
	#include<queue>
	using namespace std;
	typedef struct cell {
		bool wall = true;
		bool right = true;
		bool down = true;
	
	}cell;
	
	void printTable(vector<vector<int>> table) {
		for (vector<int> row : table) {
			for (int i : row) {
				cout << i << " ";
			}
			cout << endl;
		}
	}
	
	int NewBFS(vector<vector<cell>> visit) {
		int bs = visit.size();
		queue<vector<int>> que;
		que.push(vector<int>{0, 0, 1,0});//x,y, isRIght;
		while ( !que.empty()) {
			int x = que.front()[0]; int y = que.front()[1]; bool isRight = que.front()[2]; int count = que.front()[3];
			que.pop();
			if (isRight && x == bs - 1 && y + 1 == bs - 1) return count;
			else if (x + 1 == bs - 1 && y == bs - 1) return count;
	
			if (isRight) {
				//move
				if (y + 2 < bs && visit[x][y + 1].right && visit[x][y + 2].wall) {
					visit[x][y+1].right = false;
					que.push(vector<int>{x, y + 1, true, count + 1});
				} 
				if (y - 1 >= 0 && visit[x][y - 1].right && visit[x][y - 1].wall) {
					visit[x][y -1].right = false;
					que.push(vector<int>{x, y - 1, true, count + 1});
				} 
				if (x + 1 < bs && visit[x + 1][y].wall && visit[x + 1][y + 1].wall && visit[x + 1][y].right) {
					visit[x+1][y].right = false;
					que.push(vector<int>{x + 1, y, true, count + 1});
				} 
				if (x - 1 >= 0 && visit[x - 1][y].wall && visit[x - 1][y + 1].wall && visit[x - 1][y].right) {
					visit[x -1][y].right = false;
					que.push(vector<int>{x - 1, y, true, count + 1});
				}
					
				
				//rotate
				if (x + 1 < bs &&  visit[x + 1][y].wall &&  visit[x + 1][y + 1].wall ) {
					if (visit[x][y].down) {
						visit[x][y].down = false;
						que.push(vector<int>{x, y, false, count + 1});
					} 
					if (visit[x][y + 1].down) {
						visit[x][y+1].down = false;
						que.push(vector<int>{x, y + 1, false, count + 1});
					}
				} 
				if (x - 1 >= 0 &&  visit[x - 1][y].wall &&  visit[x - 1][y + 1].wall ) {
					if (visit[x - 1][y].down) {
						visit[x-1][y].down = false;
						que.push(vector<int>{x - 1, y, false, count + 1});
					} 
					if (visit[x - 1][y + 1].down) {
						visit[x - 1][y+1].down = false;
						que.push(vector<int>{x - 1, y + 1, false, count + 1});
					} 
				} 
			}
			else {
				//move
				if (y + 1 < bs && visit[x][y + 1].wall && visit[x + 1][y + 1].wall && visit[x][y + 1].down) {
					visit[x][y + 1].down = false;
					que.push(vector<int>{x, y + 1, false, count + 1});
				} 
				if (y - 1 >= 0 && visit[x][y - 1].wall && visit[x + 1][y - 1].wall && visit[x][y - 1].down) {
					visit[x][y - 1].down = false;
					que.push(vector<int>{x, y - 1, false, count + 1});
				} 
				if (x + 2 < bs && visit[x + 2][y].wall && visit[x + 1][y].down) {
					visit[x+1][y].down = false;
					que.push(vector<int>{x + 1, y, false, count + 1});
				} 
				if (x - 1 >= 0 && visit[x - 1][y].wall && visit[x - 1][y].down) {
					visit[x -1][y].down = false;
					que.push(vector<int>{x - 1, y, false, count + 1});
				} 
				//rotate
				if (y + 1 < bs &&  visit[x][y + 1].wall &&  visit[x + 1][y + 1].wall) {
					if (visit[x][y].right) {
						visit[x ][y].right = false;
						que.push(vector<int>{x, y, true, count + 1});
					} 
					if (visit[x + 1][y].right) {
						visit[x+1][y].right = false;
						que.push(vector<int>{x + 1, y, true, count + 1});
					} 
				}
				if (y - 1 >= 0 &&  visit[x][y - 1].wall &&  visit[x + 1][y - 1].wall) {
					if (visit[x][y - 1].right) {
						visit[x ][y-1].right = false;
						que.push(vector<int>{x, y - 1, true, count + 1});
					} 
					if (visit[x + 1][y - 1].right) {
						visit[x+1][y - 1].right = false;
						que.push(vector<int>{x + 1, y - 1, true, count + 1});
					} 
				}
			}
		}
		return 0;
	}
	
	int solution(vector<vector<int>> board) {
		int answer = 0;
		int bs = board.size();
		vector<vector<cell>> visit(bs,vector<cell>(bs));
		for (int i = 0; i < bs; i++) {
			for (int j = 0; j < bs; j++) {
				if (board[i][j] == 1) visit[i][j].wall = false;
			}
		}
		answer = NewBFS(visit);
		return answer;
	}
	
	int main() {
	
		return 0;
	}
	
{% endhighlight %}
