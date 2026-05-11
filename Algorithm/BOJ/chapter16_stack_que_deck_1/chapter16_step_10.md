# Chapter 16 Step 10
- [2346 번](https://www.acmicpc.net/problem/2346)

## 난이도
- 실버 3

## 핵심
- 덱 활용

## 풀이
```c++
#include <iostream>
#include <deque>

int main() {
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);

    int N;
    std::cin >> N;

    std::deque<std::pair<int, int>> dq;

    for(int i = 1; i <= N; ++i){
        int x;
        std::cin >> x;
        dq.push_back({i, x});
    }

    while(!dq.empty()){
        auto [idx, move] = dq.front();
        dq.pop_front();

        std::cout << idx << " ";

        if(dq.empty()) break;

        if(move > 0){
            for(int i = 0; i < move - 1; ++i){
                dq.push_back(dq.front());
                dq.pop_front();
            }
        }else{
            for(int i = 0; i < -move; ++i){
                dq.push_front(dq.back());
                dq.pop_back();
            }
        }
    }

    return 0;
}
// 인덱스와 이동값을 가진 pair를 담은 deque로 풀이
```