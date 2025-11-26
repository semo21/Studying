# step 6
- [24267 번](https://www.acmicpc.net/problem/24267)

## 난이도
- 브론즈 2

## 핵심
- 프로그램 수행 시간 분석

## 풀이
```c++
#include <iostream>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    long long n;
    std::cin >> n;

    std::cout << n * (n-1) * (n-2) / 6 << '\n' << 3 << '\n';
        
    return 0;
}

// i, j, k는 서로 같은 수가 될 수 없음
// 따라서 i, j, k를 1 ~ n까지의 범위에 해당하는 3개의 수를 뽑는 조합을 구하는 문제.
// 수행 횟수는 따라서 C(n, 3)이 됨.
// 수행 횟수는 n * (n-1) * (n-2) / 3 * 2 * 1, 최고차항의 차수는 3
```