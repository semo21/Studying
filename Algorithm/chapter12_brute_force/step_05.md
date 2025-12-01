# step 5
- [1436 번](https://www.acmicpc.net/problem/1436)

## 난이도
- 실버 5

## 핵심
- N번째 해가 나올 때까지 탐색

## 풀이
```c++
#include <iostream>
#include <string>
#include <algorithm>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int N;
    std::cin >> N;
    int i = 665;
    while(N){
        ++i;        
        if(std::to_string(i).find("666") != std::string::npos){
            N--;
        }  
    }

    std::cout << i << '\n';
    return 0;
}

// 모든 수를 탐색
// 수를 to_string하여 "666"을 포함하는지 확인
// N번째 수가 되면 출력
```