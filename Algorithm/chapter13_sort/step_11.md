# step 11
- [18870 번](https://www.acmicpc.net/problem/18870)

## 난이도
- 실버 2

## 핵심
- 대소관계 비교 정렬

## 풀이
```c++
#include <iostream>
#include <vector>
#include <algorithm>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);

    int N;
    std::cin >> N;
    
    std::vector<int> A(N);
    for(int i = 0; i < N; ++i){
        std::cin >> A[i];
    }

    std::vector<int> B = A;
    std::sort(B.begin(), B.end());
    B.erase(std::unique(B.begin(), B.end()), B.end());

    for(int x : A){
        int idx = std::lower_bound(B.begin(), B.end(), x) - B.begin();
        std::cout << idx << ' ';
    }
    return 0;
}

// N <= 1,000,000 인 자연수(1e6), 시간 제한은 2초
// 1초 = 대략 1e8(10^8)임
// O(N²)정렬은 최악의 경우 N² = 1e12이므로 탈락
// 따라서 O(N log N) 혹은 O(N) 풀이가 적합
//  
// 이 문제는 정렬 + 탐색을 모두 고려해야하는 문제.
// 따라서 정렬은 sort를 사용하지만 그 탐색방법이 관건
// 탐색을 이분 탐색인 lower_bound로 수행
// lower_bound는 iterator 반환이기 때문에 - B.begin()을 수행하여 인덱스 계산
```