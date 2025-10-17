# step 9
- [2908 번](https://www.acmicpc.net/problem/2908)
## 난이도
- 브론즈 2
## 핵심
- 문자열 구현

## 풀이
```c++
#include <iostream>
#include <string>
#include <algorithm>

int main(){
    std::string a, b;
    std::cin >> a >> b;
    
    std::reverse(a.begin(), a.end());
    std::reverse(b.begin(), b.end());
    
    int rA = std::stoi(a);
    int rB = std::stoi(b);

    std::cout << std::max(rA, rB) << '\n';
    return 0;
}

// algorithm 헤더를 사용한 간단한 풀이.

#include <iostream>

int main(){
    int a, b;
    std::cin >> a >> b;

    auto reverseNum = [](int x){
        int r = 0;
        while (x > 0){
            r = r * 10 + (x % 10);
            x /= 10;
        }
        return r;
    };

    a = reverseNum(a);
    b = reverseNum(b);
    
    std::cout << (a > b ? a : b) << '\n';
    
    return 0;
}

// 람다식을 이용한 자리 바꾸기와 출력 구현
```