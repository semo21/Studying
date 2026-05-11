# step 8
- [11651 번](https://www.acmicpc.net/problem/11651)

## 난이도
- 실버 5

## 핵심
- 좌표 정렬, sort의 이해

## 풀이
```c++
#include <iostream>
#include <vector>
#include <algorithm>
#include <utility>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);

    int N;
    std::cin >> N;

    std::vector<std::pair<int, int>> v;
    v.reserve(N);

    for(int i = 0; i < N; ++i){
        int x, y;
        std::cin >> x >> y;
        v.push_back({x, y});        
    }

    std::sort(v.begin(), v.end(), 
    [](const auto& a, const auto& b){
        if(a.second != b.second)
            return a.second < b.second;
        return a.first < b.first;
    });

    for(const auto& [x, y] : v){
        std::cout << x << ' ' << y << '\n';
    }

    return 0;
}
// step07의 11650번 문제와 비슷하지만 y기준 정렬
// 따라서 sort의 3번째 인자로 y 오름차순 설정
// 위 식에선 람다식으로 구현
// a.second < b.second: y가 같지 않다면 작은 값이 먼저 오도록
// a.first < b.first: y가 같다면 x가 작은 값이 먼저 오도록
```