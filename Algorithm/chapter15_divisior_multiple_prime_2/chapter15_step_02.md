# Chapter 15 Step 02
- [13241 번](https://www.acmicpc.net/problem/13241)

## 난이도
- 실버 5

## 핵심
- 유클리드 호제법을 활용한 최대공약수와 최소공배수 구하기

## 풀이
```c++
#include <iostream>
#include <cstdlib>  // llabs

long long gcd(long long a, long long b);

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    long long A, B;
    std::cin >> A >> B;

    long long d = gcd(A, B);

    std::cout << (A / d) * B << '\n';
    return 0;
}

long long gcd(long long a, long long b){
    a = llabs(a);
    b = llabs(b);
    while(b != 0){
        long long r = a % b;
        a = b;
        b = r;
    }

    return a;
}
```
- 유클리드 호제법을 이용한 최대공약수를 구한 뒤 최소공배수를 구한다.
- 다만, 출력에서 오버플로 방지를 위해 A * B / d의 순서를 바꾸어 A / d * B로 연산한다.
- 추가) 문제는 양수로 주어지지만, 조금 더 안전하게 A, B를 양수로 만들어둔다. (llabs)