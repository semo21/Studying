# Chapter 15 Step 06
- [1929 번](https://www.acmicpc.net/problem/1929)

## 난이도
- 실버 3

## 핵심
- 에라토스테네스의 체 혹은 다른 방법으로 소수 구하기

## 풀이
```c++
#include <iostream>

bool IsPrime(int a);

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int M, N;
    std::cin >> M >> N;

    if(M <= 2){
        std::cout << 2 << '\n';
        M = 3;
    }
    if(N % 2 == 0)  N--;
    if(M % 2 == 0)  M++;
    for(int i = M; i <= N; i += 2){
        if(IsPrime(i)) std::cout << i << '\n';
    }

    return 0;
}

bool IsPrime(int a){
    if(a == 3)    return true;
    if(a % 2 == 0)  return false;
    
    for(int j = 3; j <= a / j; j += 2){
        if(a % j == 0)  return false;
    }

    return true;
}
```
```c++
#include <iostream>
#include <vector>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int M, N;
    std::cin >> M >> N;

    std::vector<bool> isPrime(N + 1, true);
    if(N >= 1)  isPrime[1] = false;

    for(int p = 2; p <= N / p; ++p){
        if(!isPrime[p]) continue;
        for(int x = p * p; x <= N; x +=p ){
            isPrime[x] = false;
        }
    }

    for(int i = M; i <= N; ++i){
        if(isPrime[i])  std::cout << i << '\n';
    }
    return 0;
}
```
- 1번은 step 05 문제와 같은 소수구하기로 풀이
- 2번은 에라토스테네스의 체를 이용하여 풀이
- 1번 메모리: 2020KB, 시간 88ms
- 2번 메모리: 2260KB, 시간 12ms
- 에라토스테네스의 체: 소수의 배수는 소수가 아니다.
- 따라서 `for(int x = p * p; x <= N; x += p)   isPrime[x] = false;`