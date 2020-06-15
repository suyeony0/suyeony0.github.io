---
layout: post
title: [SAMSUNG SW - Monomino Domino]
date: 2020-6-15
description: txt to markdown
thumbnail: person1.jpeg
categories: Algorithm

# Information for the author block
author : Loui
---

[218. SAMSUNG SW : Monomino Domino]
- WOW. I’ve suddenly encountered a <span style="color:red">super strong enemy</span>  for a long time.
- It was a simulation problem.
- To tell you a trap in this problem, 2 x 1 or 1 x 2 “BLOCK”
- they move together, but one of a 1 x 1 block in 2 x 1 or 1 x 2 block can be removed respectively.
- In those case, I had to revise their friend block to themselves.
- I used two 10 x 4 table, so I had to re-allocate blue table’s corrodinates.
- When I remove a row, I had to revise their friend block as I mentioned above.
- I spent 3 hours ans 8 minutes and 13 seconds.
- see the code.

```cpp

{% raw %}

#include<iostream>
#include<vector>
#define EM 999 // empty
using namespace std;

int N;
vector<vector<vector<int>>> blue(10,vector<vector<int>>(4, vector<int>(2,EM)));
vector<vector<vector<int>>> green(10, vector<vector<int>>(4, vector<int>(2,EM)));
vector<vector<int>> order;
int answer = 0;
int num_shell = 0;


void PutAndMove(int t, int x, int y) {
	int i;
	if (t == 1) {
		//green
		for (i = 2; i < 11; i++) if (i >= 10 || green[i][y][0]!=EM) break;
		green[i - 1][y][0] = i - 1; green[i - 1][y][1] = y;

		//blue
		for (i = 2; i < 11; i++) if (i >= 10 || blue[i][x][0]!=EM) break;
		blue[i-1][x][0] = i-1; blue[i - 1][x][1] = x;
	}
	else if (t == 2) {
		//green
		for (i = 2; i < 11; i++) if (i >= 10 || green[i][y][0] != EM || green[i][y + 1][0] != EM) break;
		green[i-1][y][0] = i-1; green[i - 1][y][1] = y+1;
		green[i - 1][y + 1][0] = i-1; green[i - 1][y + 1][1] = y;

		//blue
		for (i = 2; i < 11; i++) if (i+1 >= 10 ||(i+1<10 && blue[i+1][x][0] != EM)) break;
		blue[i-1][x][0] = i; blue[i - 1][x][1] = x;	blue[i][x][0] = i-1; blue[i][x][1]=x;
	}
	else if(t==3){
		//green
		for (i = 2; i < 11; i++) if (i+1 >= 10 ||(i+1<10 && green[i+1][y][0] != EM)) break;
		green[i-1][y][0] = i; green[i - 1][y][1] = y; 
		green[i][y][0] = i-1; green[i][y][1] = y;

		//blue
		for (i = 2; i < 11; i++) if (i >= 10 || blue[i][x][0] != EM || blue[i][x+1][0] != EM) break;
		blue[i-1][x][0] = i-1;	blue[i - 1][x][1] =x+1; 
		blue[i-1][x+1][0] = i-1; blue[i - 1][x + 1][1] = x;
	}
}

void RemoveRow() {
	for (int i = 6; i < 10; i++) {
		int g_num = 0; int b_num = 0;
		for (int j = 0; j < 4; j++) {
			if (green[i][j][0] != EM) g_num += 1;
			if (blue[i][j][0] != EM) b_num += 1;
		} 
		if (g_num == 4) {
			answer += 1;
			for (int j = 0; j < 4; j++) { //remove friend
				if (green[i][j][0] < 10 && green[i][j][1] < 4) {
					green[green[i][j][0]][green[i][j][1]][0] = green[i][j][0];
					green[green[i][j][0]][green[i][j][1]][1] = green[i][j][1];
				}
				green[i][j][0] = EM; green[i][j][1] == EM;
			}
		}
		if (b_num == 4) {
			answer += 1;
			for (int j = 0; j < 4; j++) { //remove friend
				if (blue[i][j][0] < 10 && blue[i][j][1] < 4) {
					blue[blue[i][j][0]][blue[i][j][1]][0] = blue[i][j][0];
					blue[blue[i][j][0]][blue[i][j][1]][1] = blue[i][j][1];
				}
				blue[i][j][0] = EM; blue[i][j][1] = EM;
			}
		}
	}
}

void MoveDown() {
	for (int i = 8; i >= 4; i--) {
		for (int j = 0; j < 4; j++) {
			if (green[i][j][0]!=EM) {
				int g_empty = 0;
				if (green[i][j][0] == i && green[i][j][1] == j) { //has no friend
					for (int k = i + 1; k < 10; k++) {
						if (green[k][j][0]==EM) g_empty += 1;
						else break;
					}
					green[i][j][0] = EM; green[i][j][1] = EM;
					green[i + g_empty][j][0] = i + g_empty;
					green[i + g_empty][j][1] = j;
				}
				else { //has friend
					int fx = green[i][j][0]; int fy = green[i][j][1];
					if (i != fx) { //vertical friend
						int nx = i > fx ? i : fx;
						for (int k = nx + 1; k < 10; k++) {
							if (green[k][j][0] == EM) g_empty += 1;
							else break;
						}
						if (g_empty >= 1) {
							green[i][j][0] = EM; green[i][j][1] = EM;
							green[fx][fy][0] = EM; green[fx][fy][1] = EM;
							green[nx + g_empty][j][0] = nx + g_empty - 1;
							green[nx + g_empty][j][1] = j;
							green[nx + g_empty - 1][j][0] = nx + g_empty;
							green[nx + g_empty - 1][j][1] = j;
						}
						
					}
					else { //horizon friend
						for (int k = i + 1; k < 10; k++) {
							if (green[k][j][0]!=EM || green[k][fy][0]!=EM) break;
							g_empty += 1;
						}
						if (g_empty >= 1) {
							green[i][j][0] = EM; green[i][j][1] = EM;
							green[i][fy][0] = EM; green[i][fy][1] = EM;
							green[i + g_empty][j][0] = i + g_empty;
							green[i + g_empty][j][1] = fy;
							green[i + g_empty][fy][0] = i + g_empty;
							green[i + g_empty][fy][1] = j;
						}
						
					}
				}
			}
			if (blue[i][j][0]!=EM) {
				int b_empty = 0;
				if (blue[i][j][0] == i && blue[i][j][1] == j) { //has no friend
					for (int k = i + 1; k < 10; k++) {
						if (blue[k][j][0]==EM) b_empty += 1;
						else break;
					}
					blue[i][j][0] = EM; blue[i][j][1] = EM;
					blue[i + b_empty][j][0] = i + b_empty;
					blue[i + b_empty][j][1] = j;
				}
				else { //has friend
					int fx = blue[i][j][0]; int fy = blue[i][j][1];
					if (i != fx) { //vertical friend
						int nx = i > fx ? i : fx;
						for (int k = nx + 1; k < 10; k++) {
							if (blue[k][j][0]==EM) b_empty += 1;
							else break;
						}
						if (b_empty >= 1) {
							blue[i][j][0] = EM; blue[i][j][1] = EM;
							blue[fx][fy][0] = EM; blue[fx][fy][1] = EM;
							blue[nx + b_empty][j][0] = nx + b_empty - 1;
							blue[nx + b_empty][j][1] = j;
							blue[nx + b_empty - 1][j][0] = nx + b_empty;
							blue[nx + b_empty - 1][j][1] = j;
						}
						
					}
					else { //horizon friend
						for (int k = i + 1; k < 10; k++) {
							if (blue[k][j][0]!=EM || blue[k][fy][0]!=EM) break;
							b_empty += 1;
						}
						if (b_empty >= 1) {
							blue[i][j][0] = EM; blue[i][j][1] = EM;
							blue[i][fy][0] = EM; blue[i][fy][0] = EM;
							blue[i + b_empty][j][0] = i + b_empty;
							blue[i + b_empty][j][1] = fy;
							blue[i + b_empty][fy][0] = i + b_empty;
							blue[i + b_empty][fy][1] = j;	
						}
						
					}
				}
			}
			
		}
	}
}

void Border() {
	int b_num = 0; int g_num = 0;
	for (int i = 4; i <= 5; i++) {
		for (int j = 0; j < 4; j++) {
			if (green[i][j][0]!=EM) {
				g_num += 1;
				break;
			} 
		}
		for (int j = 0; j < 4; j++) {
			if (blue[i][j][0]!=EM) {
				b_num += 1;
				break;
			}
		}
	}
	if (g_num >= 1) {
		for (int i = 9; i >= 10 - g_num; i--) {
			for (int j = 0; j < 4; j++) {
				if (green[i][j][0] != EM) {
					if (green[i][j][0] < 10 && green[i][j][1] < 4) {
						green[green[i][j][0]][green[i][j][1]][0] = green[i][j][0];
						green[green[i][j][0]][green[i][j][1]][1] = green[i][j][1];
					}
					
				}
				green[i][j][0] = EM; green[i][j][1] = EM;
			}
		}
	}
	if (b_num >= 1) {
		for (int i = 9; i >= 10 - b_num; i--) {
			for (int j = 0; j < 4; j++) {
				if (blue[i][j][0] != EM) {
					if (blue[i][j][0] < 10 && blue[i][j][1] < 4) {
						blue[blue[i][j][0]][blue[i][j][1]][0] = blue[i][j][0];
						blue[blue[i][j][0]][blue[i][j][1]][1] = blue[i][j][1];
					}
					
				}
				blue[i][j][0] = EM; blue[i][j][1] = EM;
			}
		}
	}


}

void getScore() {
	for (int i = 4; i < 10; i++) {
		for (int j = 0; j < 4; j++) {
			if (green[i][j][0]!=EM) num_shell += 1;
			if (blue[i][j][0]!=EM) num_shell += 1;
		}
	}
}

void PrintTable() {
	cout << "### GREEN ###" << endl;
	for (vector<vector<int>> row : green) {
		for (vector<int> i : row) {
			if (i[0] == EM) cout << "0" << " ";
			else cout << "1" << " ";
		}
		cout << endl;
	}
	cout << endl;

	cout << "### BLUE ###" << endl;
	for (vector<vector<int>> row : blue) {
		for (vector<int> i : row) {
			if (i[0] == EM) cout << "0" << " ";
			else cout << "1" << " ";
		}
		cout << endl;
	}
	cout << endl;
}

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	cin >> N;
	order.assign(N, vector<int>(3, 0));
	for (int i = 0; i < N; i++) {
		cin >> order[i][0] >> order[i][1] >> order[i][2];
	}

	//algorithm part
	int sec = 0;
	for (vector<int> row : order) {
		int t = row[0]; int x = row[1]; int y = row[2];
		PutAndMove(t, x, y);
		RemoveRow();
		MoveDown();
		Border();
		MoveDown();
		RemoveRow();
		MoveDown();
		
	}
	getScore();
	cout << answer << endl;
	cout << num_shell << endl;
	return 0;
}

{% endraw %}
```

