# step 4
- [24265 번](https://www.acmicpc.net/problem/24265)

## 난이도
- 브론즈 3

## 핵심
- 프로그램 수행 시간 분석

## 풀이
```c++
#include <iostream>
#include <algorithm>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    long long n;
    std::cin >> n;
    std::cout << (n * (n-1)) / 2 << '\n' << 2 << '\n';
    return 0;
}

// 코드 1은 이중 반복문으로 실행됨
// 1 <= i <= n-1, i+1 <= j <= n
// j = 2~n(= n-1 회), 3~n(= n-2 회)... j = n~n(1회)
// j는 n의 등차수열의 총합만큼 반복
// 등차수열의 합은 n(n-1)/2
// 따라서 시행횟수는 n(n-1)/2, 시간복잡도는 O(n²)
```