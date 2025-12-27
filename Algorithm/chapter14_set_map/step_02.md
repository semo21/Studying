# step 02
- [14425 번](https://www.acmicpc.net/problem/14425)

## 난이도
- 실버 4

## 핵심
- 문자열 저장

## 풀이
```c++
#include <iostream>
#include <unordered_set>
#include <string>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);

    int N, M;
    std::cin >> N >> M;

    std::unordered_set<std::string> S;
    std::string str;

    for(int i = 0; i < N; ++i){
        std::cin >> str;
        S.insert(str);
    }

    int cnt = 0;
    for (int i = 0; i < M; ++i){
        std::cin >> str;
        if(S.find(str) != S.end()){
            ++cnt;
        }
    }

    std::cout << cnt << '\n';
    return 0;
}

// unordered_set을 활용하면 쉽게 풀이가능
// unordered_set은 정렬되지 않고, 중복이 없는 집합
// find를 사용해 해당 문자열이 있는지 탐색
```