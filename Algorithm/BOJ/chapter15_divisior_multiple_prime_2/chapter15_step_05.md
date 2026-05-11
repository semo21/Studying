# Chapter 15 Step 05
- [4134 번](https://www.acmicpc.net/problem/4134)

## 난이도
- 실버 4

## 핵심
- √N까지만 나눠서 소수를 판별하기

## 풀이
```c++
#include <iostream>

bool IsPrime(long long x);

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int T;
    std::cin >> T;

    for(int i = 0; i < T; ++i){
        long long n;
        std::cin >> n;
        if (n <= 2){
            std::cout << 2 << '\n';
            continue;
        }else if(n == 3)  {
            std::cout << 3 << '\n';
            continue;
        }

        if (n % 2 == 0) n++;
        while(!IsPrime(n))   n += 2;
        std::cout << n << '\n';
    }

    return 0;
}

bool IsPrime(long long x){
    for(long long i = 3; i <= x / i; i += 2){
        if(x % i == 0)  return false;
    }
    return true;
}
```
- n보다 같거나 큰 소수 중 가장 작은 수 구하기
- n = 0 ~ 2라면 답은 2, n = 3이라면 답은 3
- 2를 제외한 모든 수는 소수가 아님 -> if(n % 2 == 0) n++;처리
- 이후 소수 탐색에서 짝수는 볼 필요 없으므로 n += 2 반복하며 탐색
- 소수판별 함수에서도 약수가 짝수이면 소수가 아니므로(2 제외) i += 2하며 진행 