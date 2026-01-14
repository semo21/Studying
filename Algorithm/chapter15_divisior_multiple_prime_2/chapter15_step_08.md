# Chapter 15 Step 08
- [17103 번](https://www.acmicpc.net/problem/17103)

## 난이도
- 실버 2

## 핵심
- 골드바흐 파티션의 개수 구하기

## 풀이
```c++
#include <iostream>
#include <vector>
#include <algorithm>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int T;
    std::cin >> T;

    std::vector<int> queries(T);
    int maxN = 0;
    for(int i = 0; i < T; ++i){            
        std::cin >> queries[i];
        maxN = std::max(maxN, queries[i]);        
    }

    std::vector<bool> isPrime(maxN + 1, true);
    isPrime[0] = isPrime[1] = false;
    
    for(int p = 2; 1LL * p * p <= maxN; ++p){
        if(!isPrime[p]) continue;
        for(int x = 1LL * p * p; x <= maxN; x += p){
            isPrime[x] = false;
        }
    }

    for(int n : queries){
        int cnt = 0;
        for(int p = 2; i <= n / 2; ++p){
            if(isPrime[p] && isPrime[n-p]) ++cnt;
        }
        std::cout << cnt << '\n';
    }    

    return 0;
}
```
- 에라토스테네스의 체로 소수탐색을 용이하게 만든 후 풀이 진행
- 4 이상의 짝수는 소수의 합으로 구성(같은 소수 2개도 해당. ex) 2 + 2 = 4
- 따라서 주어진 수의 절반까지만 소수탐색.
- 주어진 수 n은 소수 p와 n-p의 합으로 이루어짐
- isPrime[p] 와 isPrime[n-p]를 충족한다면 골드바흐 파티션이므로 cnt++