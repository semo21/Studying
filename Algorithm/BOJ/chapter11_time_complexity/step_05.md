# step 5
- [24266 번](https://www.acmicpc.net/problem/24266)

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
    
    std::cout << n * n * n << '\n' << 3 << '\n';
    
    return 0;
}

// i, j, k 모두 n번씩 순회 가능
// 따라서 수행횟수는 n * n * n, 최고차항의 차수는 3
```