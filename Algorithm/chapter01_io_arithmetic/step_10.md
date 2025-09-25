# step 10
- [2588번](https://www.acmicpc.net/problem/2588)
## 난이도
- 브론즈 3
## 핵심
- 입출력과 사칙연산 구현

## 풀이
```c++
#include <iostream>

int main(){
    int a, b;
    std::cin >> a >> b;
    std::cout << a*(b%10) << std::endl;
    std::cout << a*((b%100)/10) << std::endl;
    std::cout << a*(b/100) << std::endl;
    std::cout << a*b << std::endl;

    return 0;
}
```