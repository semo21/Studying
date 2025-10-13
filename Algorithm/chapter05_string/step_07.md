# step 7
- [2675 번](https://www.acmicpc.net/problem/2675)
## 난이도
- 브론즈 2
## 핵심
- 문자열 구현

## 풀이
```c++
#include <iostream>
#include <string>

int main(){
    int t;
    std::cin >> t;
    for(int i = 0; i < t; i++){
        int a;
        std::string input;
        std::cin >> a >> input;
        for(char e : input) std::cout << std::string(a, e);
        std::cout << "\n";
    }
    return 0;
}

// string 헤더를 명시해주는 편이 좋음.
```