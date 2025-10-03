# step 8
- [11022번](https://www.acmicpc.net/problem/11022)
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
        std::cout << "Case #" << i+1 << ": " 
        << a << " + " << b << " = " 
        << a+b << std::endl;
    }

    return 0;
}

// 0 < a,b < 10
```