# step 03
- [7785 번](https://www.acmicpc.net/problem/7785)

## 난이도
- 실버 5

## 핵심
- 탐색 제거 구현

## 풀이
```c++
#include <iostream>
#include <unordered_set>
#include <string>
#include <vector>
#include <algorithm>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);

    int N;
    std::cin >> N;
    
    std::unordered_set<std::string> S;
    std::string str, status;

    for(int i = 0; i < N; ++i){
        std::cin >> str >> status;
        if(status == "enter"){
            S.insert(str);            
        }else if(status == "leave"){
            auto it = S.find(str);
            if(it != S.end()){
                S.erase(it);
            }
        }else{
            std::cout << "Wrong input" << '\n';
        }
    }
    
    std::vector<std::string> v(S.begin(), S.end());
    std::sort(v.begin(), v.end(), std::greater<>());

    for(const std::string& name : v){
        std::cout << name << '\n';
    }
    
    return 0;
}

// 출/퇴근 순서가 무작위이므로 탐색이 빠른 unordered_set 활용
// 입력이 끝나고 vector로 옮겨 정렬 수행
// 사전의 역순으로 출력해야 하므로 역순정렬
```