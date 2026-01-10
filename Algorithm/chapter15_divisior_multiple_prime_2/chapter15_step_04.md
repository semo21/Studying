# Chapter 15 Step 04
- [2485 번](https://www.acmicpc.net/problem/2485)

## 난이도
- 실버 4

## 핵심
- 주어진 수의 배열을 등차수열로 만드는 수 찾기

## 풀이
```c++
#include <iostream>
#include <vector>
#include <cstdlib>

long long gcd_ll(long long a, long long b){
    a = std::abs(a);
    b = std::abs(b);
    while(b != 0){
        long long r = a % b;
        a = b;
        b = r;
    }
    return a;
}

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int N;
    std::cin >> N;
    
    std::vector<long long> x(N);
    for(int i = 0; i < N; ++i){
        std::cin >> x[i];
    }

    long long g = 0;
    for(int i = 0; i < N - 1; ++i){
        long long gap = x[i + 1] - x[i];
        g = gcd_ll(g, gap);
    }

    long long result = 0;
    for(int i = 0; i < N - 1; ++i){
        long long gap = x[i+1] - x[i];
        result += (gap / g) - 1;
    }

    std::cout << result << '\n';

    return 0;
}
```
- O(N)의 풀이를 적용
- 벡터에 가로수 위치를 모두 담기
- 가로수 사이의 거리(gap)를 모두 탐색하며 최대공약수 탐색(g)
- 다시 가로수 사이의 거리(gap)에서 최대공약(g)수로 필요한 나무 수 구하기
- 필요한 개수는 `구간의 길이 / 공차(최대공약수) - 1 ((gap / g) - 1)` 임