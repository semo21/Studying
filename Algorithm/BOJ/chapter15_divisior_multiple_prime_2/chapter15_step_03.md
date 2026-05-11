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

    long long g = gcd(B1, B2);
    long long lcm = (B1 / g) * B2;

    long long num = A1 * (B2 / g) + A2 * (B1 / g);
    long long den = lcm;

    long long d = gcd(num, den);
    std::cout << num / d << ' ' << den / d << '\n';
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
- 수가 너무 커지는것을 방지하기 위한 g와 lcm으로 약분을 하며 연산 수행
- 이후 마지막에 합쳐진 수를 다시 약분 수행