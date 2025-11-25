# step 1
- [24262 번](https://www.acmicpc.net/problem/24262)

## 난이도
- 브론즈 5

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
    std::cout << 1 << '\n' << 0 << '\n';
    return 0;
}

// 주어진 알고리즘은 반복을 하지 않고 단 한번만 수행
// 단 한번만 수행하는 알고리즘의 시간 복잡도 최고차항의 차수는 0, 즉 복잡도는 상수
// 시행횟수는 1회, 시간복잡도는 O(1)
// 1번 수행, 상수 항이므로 1과 0을 출력
```