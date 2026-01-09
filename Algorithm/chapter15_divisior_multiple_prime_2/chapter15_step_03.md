# Chapter 15 Step 03
- [1735 번](https://www.acmicpc.net/problem/1735)

## 난이도
- 실버 3

## 핵심
- 분수의 덧셈 후 약분 구현

## 풀이
```c++
#include <iostream>
#include <cstdlib>

long long gcd(long long a, long long b);

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    long long A1, B1, A2, B2;
    std::cin >> A1 >> B1 >> A2 >> B2;

    long long A = (A1 * B2) + (A2 * B1);
    long long B = B1 * B2;

    long long D = gcd(A, B);    
    std::cout << A / D << ' ' << B / D << '\n';
    return 0;
}

long long gcd(long long a, long long b){
    a = std::abs(a);
    b = std::abs(b);
    while(b != 0){
        long long r = a % b;
        a = b;
        b = r;
    }

    return a;
}
```
- 유클리드 호제법을 이용한 최대공약수 구하기
- 오버플로 방지를 위한 long long 타입