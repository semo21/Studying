# Chapter 15 Step 07
- [4948 번](https://www.acmicpc.net/problem/4948)

## 난이도
- 실버 2

## 핵심
- 입력받은 범위의 소수 개수 구하기

## 풀이
```c++
#include <iostream>
#include <vector>
#include <algorithm>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    std::vector<int> ns;    
    while(true){
        int n;
        std::cin >> n;
        if(!std::cin)    return 0;
        if(n == 0)  break;
        ns.push_back(n);
    }
    if(ns.empty())  return 0;

    int maxN = 2 * (*max_element(ns.begin(), ns.end()));

    std::vector<bool> isPrime(maxN + 1, true);
    isPrime[0] = isPrime[1] = false;

    for(int i = 2; 1LL * i * i <= maxN; ++i){
        if(!isPrime[i]) continue;
        for(int j = i * i; j <= maxN; j += i){
            isPrime[j] = false;
        }
    }
    
    std::vector<int> pref(maxN + 1, 0);
    for(int i = 1; i <= maxN; ++i){
        pref[i] = pref[i - 1] + (isPrime[i] ? 1 : 0);
    }

    for(int n : ns){
        std::cout << pref[2 * n] - pref[n] << '\n';
    }

    return 0;
}
```
- 에라스토테네스의 체를 저장하여 n부터 2n까지의 소수의 개수를 구할 수 있음
- pref[2n](=2n까지의 소수의 개수) - pref[n](=n까지의 소수의 개수) = n~2n까지의 소수의 개수이기 때문
- 우선 모든 입력을 다 받고 나서 연산을 진행함
- 입력받은 수 중 가장 큰 수를 알아야 체의 크기(maxN+1)를 정할 수 있기 때문