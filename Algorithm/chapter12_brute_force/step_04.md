# step 4
- [1018 번](https://www.acmicpc.net/problem/1018)

## 난이도
- 실버 3

## 핵심
- 체스판 최적의 해 찾기

## 풀이
```c++
#include <iostream>
#include <vector>
#include <algorithm>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int N, M;
    std::cin >> N >> M;
    std::vector<std::vector<char>> board(N, std::vector<char>(M));
    
    for(int i = 0; i < N; ++i){
        for(int j = 0; j < M; ++j){
            std::cin >> board[i][j];
        }
    }

    int answer = 64;
    for(int sr = 0; sr <= N-8; ++sr){
        for(int sc = 0; sc <= M-8; ++sc){
            int reW = 0;
            int reB = 0;

            char first = board[sr][sc];
            for(int r = 0; r < 8; ++r){
                for(int c = 0; c < 8; ++c){
                    char cur = board[sr+r][sc+c];
                    // 맨 왼쪽 위가 W일 경우를 가정
                    if((r + c) % 2 == 0){
                        if(cur != 'W')  reW++;
                    }else{
                        if(cur != 'B')  reW++;
                    }

                    // 맨 왼쪽 위가 B일 경우를 가정
                    if((r + c) % 2 ==0){
                        if(cur != 'B')  reB++;
                    }else{
                        if(cur != 'W')  reB++;
                    }
                }
            }
            answer = std::min(answer, std::min(reW, reB));
        }
    }
    
    std::cout << answer << '\n';
    return 0;
}

// 올바르게 된 체스판이라면
// 맨 왼쪽이 흰 색일 때, 체스판의 좌표합이 짝수라면 흰색, 홀수라면 검은색
// ex)
// (0, 0) = W, (0, 1) = B, (0, 2) = W...
// (1, 0) = B, (1, 1) = W, (1, 2) = B...
// (2, 0) = W, (2, 1) = B, (2, 2) = W...
// 이것을 이용하여 중첩 반복문에서 8*8크기의 체스판을 탐색
// 맨 왼쪽 위가 W, B일때를 가정하여 각각 수정횟수 탐색
// W, B일 때의 수정횟수를 비교하여 최솟값 구하기
// 나온 최솟값을 전체 최솟값과 비교하여 최솟값 구하기.

#include <iostream>
#include <vector>
#include <algorithm>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int N, M;
    std::cin >> N >> M;
    std::vector<std::vector<char>> board(N, std::vector<char>(M));
    
    for(int i = 0; i < N; ++i){
        for(int j = 0; j < M; ++j){
            std::cin >> board[i][j];
        }
    }

    int answer = 64;
    for(int sr = 0; sr <= N-8; ++sr){
        for(int sc = 0; sc <= M-8; ++sc){
            int re = 0;

            char first = board[sr][sc];
            for(int r = 0; r < 8; ++r){
                for(int c = 0; c < 8; ++c){
                    char cur = board[sr+r][sc+c];
                    if((r + c) % 2 == 0){
                        if(cur != 'W')  re++;
                    }else{
                        if(cur != 'B')  re++;
                    }                    
                }
            }
            answer = std::min(answer, std::min(re, 64 - re));
        }
    }
    
    std::cout << answer << '\n';
    return 0;
}
// 처음 풀이를 단축한 버전
// 체스판은 반복되는 것이 확정.
// 첫 타일이 W인 경우가 틀린 경우라면, 64-reW가 최솟값.
// 첫 타일이 W인 경우가 맞는 경우라면, reW가 최솟값.
// 따라서 첫 풀이에 reW, reB로 나눠진 변수를 re로 통합
// 이후 최솟값을 min(re, 64-re)로 구하기
```