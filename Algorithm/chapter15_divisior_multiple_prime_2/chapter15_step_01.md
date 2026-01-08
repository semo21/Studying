# Chapter 15 Step 01
- [1934 번](https://www.acmicpc.net/problem/1934)

## 난이도
- 브론즈 1

## 핵심
- 최소공배수 구하기

## 풀이
```c++
#include <iostream>

long gcd(long a, long b);

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int T;
    std::cin >> T;

    for(int i = 0; i < T; ++i){
        long A, B;
        std::cin >> A >> B;
        long d = gcd(A, B);
        
        std::cout << A * B / d << '\n';
    }

    return 0;
}

long gcd(long a, long b){
    while(b != 0){
        int r = a % b;
        a = b;
        b = r;
    }
    return a;
}
```
- 유클리드 호제법에 기반한 풀이
- gcd는 유클리드 호제법을 구현한 함수
- 유클리드 호제법에 의해 구해진 최대공약수를 d라고 칭함
- 최소공배수는 A * B / d 이므로 그대로 출력