# Chapter 15 Step 09
- [13909 번](https://www.acmicpc.net/problem/13909)

## 난이도
- 실버 5

## 핵심
- 약수의 개수 구하기

## 풀이
```c++
#include <iostream>
#include <cmath>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int N;
    std::cin >> N;

    std::cout << (int)std::sqrt(N) << '\n';

    return 0;
}
```
- 1을 포함한 약수의 개수가 짝수라면 창문이 닫힘
- 약수의 개수가 홀수라면 창문이 열림
- 약수의 개수가 홀수인 것은 완전 제곱수(ex. 36, 49, 144 ...)
- 약수의 개수를 구하는 공식은 약수를 소인수분해 했을 때
- (p1^a)(p2^b)(p3^c)...일 때 (a+1)(b+1)(c+1) = 약수의 개수
- ex) 144 = 2^4 * 3^2이므로 (4+1)(2+1) = 15
- 결론: N의 제곱근 이하의 자연수 중 가장 큰 수 = 열린 창문의 수