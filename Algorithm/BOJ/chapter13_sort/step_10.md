# step 10
- [10814 번](https://www.acmicpc.net/problem/10814)

## 난이도
- 실버 5

## 핵심
- 안정 정렬 구현(stable sort)

## 풀이
```c++
#include <iostream>
#include <vector>
#include <string>
#include <algorithm>
#include <utility>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);

    int N;
    std::cin >> N;
    
    std::vector<std::pair<int, std::string>> v;
    v.reserve(N);

    for(int i = 0; i < N; ++i){
        int age;    std::string name;
        std::cin >> age >> name;
        v.push_back({age, name});
    }
    
    std::stable_sort(v.begin(), v.end(), [](const auto& a, const auto& b){
        return a.first < b. first;
    });

    for(const auto&[age, name] : v){
        std::cout << age << ' ' << name << '\n';
    }

    return 0;
}

// 입력순서를 보존하는 안정 정렬을 구현하여 풀이.
// 안정 정렬에서 첫번째 요소(나이)만 비교하고 이후엔 비교하지 않음.
```