# step 10
- [2439번](https://www.acmicpc.net/problem/2439)
## 난이도
- 브론즈 4
## 핵심
- 반복문, 입출력 구현

## 풀이
```c++
#include <iostream>

int main(){
    int n;
    std::cin >> n;
    
    for(int i = 1; i <= n; i++){
        std::cout << std::string(n-i,' ')
        << std::string(i, '*')
        << "\n";
    }
    std::cout << "\n";
    return 0;
}

// 또는
#include <iostream>

int main(){
    int n;
    std::cin >> n;
    
    for(int i = 1; i <= n; i++){
        std::cout << std::string(n-i,' ')
        << std::string(i, '*')
        << "\n";
    }
    std::cout << "\n";
    return 0;
}

// 1 <= n <= 100
// 중첩 반복문 or string으로 구현
```