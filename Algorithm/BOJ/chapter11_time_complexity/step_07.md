# step 7
- [24313 번](https://www.acmicpc.net/problem/24313)

## 난이도
- 실버 5

## 핵심
- 프로그램 수행 시간 분석

## 풀이
```c++
#include <iostream>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int a1, a0, c, n0;
    std::cin >> a1 >> a0 >> c >> n0;

    long long f_n0 = a1 * n0 + a0;
    long long g_n0 = c * n0;

    if (a1 <= c && f_n0 <= g_n0)    
        std::cout << 1 << '\n';
    else    
        std::cout << 0 << '\n';
        
    return 0;
}

// 우선 Big O 정의에서 g(n) = n
// 따라서 식은 f(n) <= c*n
// f(n) = a1*n + a0
// a1*n + a0 <= c*n 을 성립해야함.
// 첫번째로 해당 조건이 항상 성립하기위해선 c*g(n)의 기울기가 더 커야함.
// c와 n은 양의 정수이므로 c*g(n)은 항상 양의 기울기를 가짐. 따라서 c >= a1의 조건을 충족하는게 첫번째 조건.
// 그리고 c >= a1이라면, n0은 g(n)에서 가장 작은 값이므로 n0을 대입했을 때 f(n) <= g(n)이라면 항상 성립
// 따라서 두번째 조건은 g(n0) >= f(n0)
// 두 조건을 동시에 성립한다면 정의를 만족(1), 아니라면 정의를 만족하지 못함(0)
// 핵심 조건: 
// 1. c >= a1
// 2. g(n0) >= f(n0)
```