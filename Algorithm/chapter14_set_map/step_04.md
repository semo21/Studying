# step 04
- [1620 번](https://www.acmicpc.net/problem/1620)

## 난이도
- 실버 4

## 핵심
- 맵을 사용하여 이름과 수를 연결짓기

## 풀이
```c++
#include <bits/stdc++.h>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int N, M;
    std::cin >> N >> M;
    
    std::vector<std::string> numToName(N+1);
    std::unordered_map<std::string, int> nameToNum;

    for(int i = 1; i <= N; ++i){
        std::cin >> numToName[i];
        nameToNum[numToName[i]] = i;
    }

    while(M--){
        std::string input;
        std::cin >> input;

        if(std::isdigit(input[0])){
            int idx = std::stoi(input);
            std::cout << numToName[idx] << '\n';
        }else{
            std::cout << nameToNum[input] << '\n';
        }
    }
    return 0;
}

// key-value 관계를 표현하는 map을 사용하여 풀이
// 첫번째 글자가 숫자가 아니라면 이름이므로 그에 따라 출력 분기 구현
```