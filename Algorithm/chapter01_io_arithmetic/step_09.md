# step 9
- 10430번 문제
## 난이도
- 브론즈 5
## 핵심
- 나눗셈 나머지 구현

## 풀이
```c++
#include <iostream>

int main(){
    int a, b, c;
    std::cin >> a >> b >> c;
    std::cout << (a+b)%c << std::endl;
    std::cout << ((a%c)+(b%c))%c << std::endl;
    std::cout << (a*b)%c << std::endl;
    std::cout << ((a%c)*(b%c))%c << std::endl;
    return 0;
}
```