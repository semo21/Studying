# step 11
- [11718 번](https://www.acmicpc.net/problem/11718)
## 난이도
- 브론즈 3
## 핵심
- 문자열, EOF, 공백문자 입력 구현

## 풀이
```c++
#include <iostream>
#include <string>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    std::string line;
    while(std::getline(std::cin, line)){
        std::cout << line << '\n';
    }    
    return 0;
}

// 끝을 내는 입력이 주어지지 않으므로 EOF처리 필요
// 공백문자를 포함한 입력을 출력해야하므로 getline으로 입력수행
```