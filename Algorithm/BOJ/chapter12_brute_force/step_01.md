# step 1
- [2798 번](https://www.acmicpc.net/problem/2798)

## 난이도
- 브론즈 2

## 핵심
- 3장의 카드를 고르는 모든 경우 구하기

## 풀이
```c++
#include <iostream>
#include <vector>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int N, M;
    std::cin >> N >> M;

    std::vector<int> cards(N);
    for(int i = 0; i < N; ++i){
        std::cin >> cards[i];
    }

    int result = 0;
    for(int i = 0; i < N; ++i){
        for(int j = i+1; j < N; ++j){
            for(int k = j+1; k < N; ++k){
                int sum = cards[i] + cards[j] + cards[k];
                if(sum <= M && sum > result)    result = sum;
            }
        }
    }

    std::cout << result << '\n';
    return 0;
}

// Brute Force 알고리즘 사용
// Brute Force 알고리즘이란, 가능한 모든 경우의 수를 탐색하는 알고리즘
// 나의 표현으론 가장 투박하고 정직하게 탐색하는 알고리즘
// 조합(Combination) 문제이므로
// 3중 반복문에서 i, j, k 범위를 서로 겹치지 않게 설정
// 이후 나온 수가 M보다 작으며 기존의 result보다 크다면 조건 만족
// 모든 반복문 수행 후 M보다 작은 수 중 가장 큰 result가 결과
```