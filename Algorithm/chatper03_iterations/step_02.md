# step 7
- [10950번](https://www.acmicpc.net/problem/10950)
## 난이도
- 브론즈 5
## 핵심
- 반복문, 덧셈, 입출력 구현

## 풀이
```c++
#include <iostream>

int main(){
    int t;    
    std::cin >> t;
    
    for(int i = 0; i < t; i++){
        int a, b;
        std::cin >> a >> b;
        std::cout << a+b << std::endl;
    }

    return 0;
}

// 0 < a, b < 10
// 루프를 t회 실행
// 반복마다 입출력 및 덧셈 구현
```