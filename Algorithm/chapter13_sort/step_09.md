# step 9
- [1181 번](https://www.acmicpc.net/problem/1181)

## 난이도
- 실버 5

## 핵심
- 단어 순서 정렬

## 풀이
```c++
#include <iostream>
#include <vector>
#include <string>
#include <algorithm>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);

    int N;
    std::cin >> N;

    std::vector<std::string> v;
    v.reserve(N);

    for(int i = 0; i < N; ++i){
        std::string s;
        std::cin >> s;
        v.push_back(s);
    }

    // 정렬: 길이 -> 사전순
    std::sort(v.begin(), v.end(), [](const std::string a, const std::string b){
        if(a.size() != b.size())    return a.size() < b.size();
        return a < b;   // std::string의 비교는 사전순 비교
    });

    // 중복 제가
    v.erase(std::unique(v.begin(), v.end()), v.end());
    
    for(const auto& s : v){
        std::cout << s << '\n';
    }
    return 0;
}
// 
```