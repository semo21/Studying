# step 5
- [25314번](https://www.acmicpc.net/problem/25314)
## 난이도
- 브론즈 5
## 핵심
- 반복문, 나눗셈 구현

## 풀이
```c++
#include <iostream>

int main(){
    int n;
    std::cin >> n;

    for (int i = 0; i < (n/4); i++){
        std::cout << "long ";
    }
    std::cout << "int" << std::endl; 

    return 0;
}

// 4 <= n <= 1000; n은 4의 배수
// n은 4의배수이므로 n/4만큼 "long "을 출력 후 마지막에 "int" 출력.
```