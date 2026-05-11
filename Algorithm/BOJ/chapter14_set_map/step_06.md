# step 06
- [1764 번](https://www.acmicpc.net/problem/1764)

## 난이도
- 실버 4

## 핵심
- 두 조건을 모두 만족하는 값의 집합 구하기

## 풀이
```c++
#include <iostream>
#include <string>
#include <vector>
#include <unordered_set>
#include <algorithm>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int N, M;
    std::cin >> N >> M;
    std::unordered_set<std::string> S;

    // bucket의 refresh를 방지하는 넉넉한 값 할당
    // set의 refresh 비용이 O(N)이기 때문에 꽤 비쌈.
    S.reserve(N * 2);
    for(int i = 0; i < N; ++i){
        std::string name;
        std::cin >> name;
        S.insert(name);
    }

    std::vector<std::string> v;
    v.reserve(std::min(N, M));
    for(int i = 0; i < M; ++i){
        std::string name;
        std::cin >> name;
        if(S.find(name) != S.end()){
            v.push_back(name);
        }        
    }

    std::sort(v.begin(), v.end());

    std::cout << v.size() << '\n';
    for(const std::string& name : v){
        std::cout << name << '\n';
    }
    return 0;
}

// 듣도 못한 사람의 집합을 후에 탐색이 빠른 set로 설정.
// 보도 못한 사람을 set에서 검색하며 중복값 탐색
// 중복값을 vector에 넣고 정렬
// 정렬된 vector를 출력
```