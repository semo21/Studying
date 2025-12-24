# step 01
- [10815 번](https://www.acmicpc.net/problem/10815)

## 난이도
- 실버 5

## 핵심
- 집합에 탐색 요소의 존재 유무 판별

## 풀이
```c++
#include <iostream>
#include <vector>
#include <algorithm>

bool CheckExist(const std::vector<int>& v, int t);

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);

    int N;
    std::cin >> N;
    
    std::vector<int> A(N);
    for(int i = 0; i < N; ++i){
        std::cin >> A[i];
    }

    std::sort(A.begin(), A.end());

    int M;
    std::cin >> M;
    
    std::vector<int> B(M);
    for(int i = 0; i < M; ++i){
        std::cin >> B[i];
    }

    for(int x : B){
        std::cout << (int)CheckExist(A, x) << ' ';
    }
    std::cout << '\n';
    return 0;
}

bool CheckExist(const std::vector<int>& v, int t){
    int left = 0;
    int right = (int)v.size() - 1;
    
    while(left <= right){
        int mid = left + (right - left) / 2;
        
        if(v[mid] == t)    return true;
        else if(v[mid] < t)    left = mid + 1;
        else    right = mid - 1;
    }
    return false;
}

// N <= 500,000 인 자연수
// 받은 정렬을 정렬하여 탐색에 용이하게 만들기
// 나중에 입력받은 배열 B의 값을 정렬된 A에서 이진 탐색 수행
// 있다면 1, 없다면 0 출력
```