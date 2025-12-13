# step 7
- [11650 번](https://www.acmicpc.net/problem/11650)

## 난이도
- 실버 5

## 핵심
- 좌표 정렬

## 풀이
```c++
#include <iostream>
#include <vector>
#include <algorithm>    // sort
#include <utility>      // pair

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);

    int N;
    std::cin >> N;

    std::vector<std::pair<int, int>> v;
    v.reserve(N);   // N개만큼 담을 용량 확보

    for(int i = 0; i < N; ++i){
        int x, y;
        std::cin >> x >> y;
        v.push_back({x, y});
    }

    // std::pair는 기본 비교가 (first, then second)라서
    // x 오름차순, x가 같으면 y 오름차순 정렬이 됨
    std::sort(v.begin(), v.end());

    for(const auto& [x, y] : v){
        std::cout << x << ' ' << y << '\n';
    }

    return 0;
}
// N이 최대 100,000이라 O(N²) 정렬은 시간초과
// O(N log N) 정렬인 std::sort 사용
// 좌표 2개를 묶기 위해 std::pair<int, int> 사용
// pair의 기본 정렬 기준은 first -> second(사전순 비교)
// sort함수를 이용하여 정렬
// 이후 pair의 값을 읽고 출력
```