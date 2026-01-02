# step 07
- [1269 번](https://www.acmicpc.net/problem/1269)

## 난이도
- 실버 4

## 핵심
- 차집합 구하기

## 풀이
```c++
#include <iostream>
#include <unordered_set>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int A, B;
    std::cin >> A >> B;

    std::unordered_set<int> S;
    for(int i = 0; i < A; ++i){
        int x;
        std::cin >> x;
        S.insert(x);
    }

    int common = 0;
    for(int i = 0; i < B; ++i){
        int x;
        std::cin >> x;
        if(S.find(x) != S.end())    common++;
    }

    std::cout << (A + B - 2 * common) << '\n';

    return 0;
}

// A차집합의 개수 = A - (A, B 교집합 개수)
// B차집합의 개수 = B - (A, B 교집합 개수)
// 따라서 (A개수 + B개수 - (2 * 교집합 개수))
// 그러므로 처음 입력받은 A만 저장
// 이후 입력받는 B의 요소들은 탐색하며 교집합 개수를 찾는데만 사용
```