[202. [SAMSUNG SW ? Making Bridge]
- It was a minimum spanning tree problem.
- when I solved this problem. I thought time limit exceeded might have occurred. but it¡¯s not.
- First, I named all the district respectively.
- Second, for each shell that is one of a district, find minimum path to another district using BFS.
- see the code.
#include<iostream>
#include<vector>
#include<queue>
#include<unordered_set>
#define min(a,b) a>b?b:a
using namespace std;
vector<vector<int>> table;
int dir[4][2] = { {-1,0},{0,-1},{1,0},{0,1} };
int N;
int d_num = 2;
int answer = 987654321;
void makeDistriction() {
	queue<vector<int>> que;
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < N; j++) {
			if (table[i][j] == 1) {
				que.push(vector<int>{i,j});
				table[i][j] = d_num;
				while (!que.empty()) {
					int x = que.front()[0]; int y = que.front()[1];
					que.pop();
					for (int d = 0; d < 4; d++) {
						int nx = x + dir[d][0]; int ny = y + dir[d][1];
						if (nx >= 0 && ny >= 0 && nx < N && ny < N && table[nx][ny] == 1) {
							table[nx][ny] = d_num;
							que.push(vector<int>{nx, ny});
						}
					}
				}
				d_num += 1;
			}
		}
	}
}

void makeBridge() {
	
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < N; j++) {
			if (table[i][j] != 0) {
				queue<vector<int>> que;
				que.push(vector<int>{i, j,0});
				int cur_d = table[i][j];
				vector<vector<bool>> visit(N, vector<bool>(N, false));
				visit[i][j] = true;
				while (!que.empty()) {
					int x = que.front()[0]; int y = que.front()[1]; int dis = que.front()[2]; que.pop();
					if (table[x][y] != 0 && table[x][y]!=cur_d) {
						answer = min(answer, dis-1);
						break;
					}
					for (int d = 0; d < 4; d++) {
						int nx = x + dir[d][0]; int ny = y + dir[d][1];
						if (nx >= 0 && ny >= 0 && nx < N && ny < N && visit[nx][ny] == false && table[nx][ny]!=cur_d) {
							visit[nx][ny] = true;
							que.push(vector<int>{nx, ny, dis + 1});
						}
					}
				}	
			}
		}
	}
}

int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL); cout.tie(NULL);

	//get input
	cin >> N;
	table.assign(N, vector<int>(N, 0));
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < N; j++) {
			cin >> table[i][j];
		}
	}

	//algorithm part
	makeDistriction();
	makeBridge();
	cout << answer;
	return 0;

}

