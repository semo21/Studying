# step 1
- [24263 번](https://www.acmicpc.net/problem/24263)

## 난이도
- 브론즈 4

## 핵심
- 프로그램 수행 시간 분석

## 풀이
```c++
#include <iostream>
#include <algorithm>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int n;
    std::cin >> n;
    std::cout << n << '\n' << 1 << '\n';
    return 0;
}

// 주어진 알고리즘은 반복문을 순회.
// 따라서 시간 복잡도는 O(n), 즉 1차
// 주어진 n만큼 순회하며 최고차항의 차수가 1
// 따라서 n과 1을 출력
```