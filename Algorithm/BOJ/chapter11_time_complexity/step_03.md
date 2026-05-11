# step 3
- [24264 번](https://www.acmicpc.net/problem/24264)

## 난이도
- 브론즈 3

## 핵심
- 프로그램 수행 시간 분석

## 풀이
```c++
#include <iostream>
#include <algorithm>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    long long n;
    std::cin >> n;
    std::cout << (n * n) << '\n' << 2 << '\n';
    return 0;
}

// 예제 알고리즘은 이중 반복문
// 예제 알고리즘의 시간 복잡도는 O(n²)
// 수행 횟수는 n², 최고차항 차수는 2
// 범위가 int보다 커질 수 있으므로 l0ong long 타입으로 선언
```