# step 05
- [10816 번](https://www.acmicpc.net/problem/10816)

## 난이도
- 실버 4

## 핵심
- 각 카드의 개수 찾기

## 풀이
```c++
#include <iostream>
#include <unordered_map>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int N;
    std::cin >> N;
    
    std::unordered_map<int, int> cnt;
    for(int i = 0; i < N; ++i){
        int x;
        std::cin >> x;
        cnt[x]++;
    }
    
    int M;
    std::cin >> M;
    for(int i = 0; i < M; ++i){
        int x;
        std::cin >> x;
        std::cout << cnt[x] << ' ';
    }

    return 0;
}

// N <= 500,000인 자연수
// map의 key를 카드의 숫자, value를 카드의 개수로 취급
```