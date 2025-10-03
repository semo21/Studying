# step 11
- [10952번](https://www.acmicpc.net/problem/10952)
## 난이도
- 브론즈 5
## 핵심
- 반복문, 덧셈, 조건문 구현

## 풀이
```c++
#include <iostream>

int main(){
    int a, b;
    std::cin >> a >> b;
    while(a != 0 && b != 0){
        std::cout << a+b << "\n";
        std::cin >> a >> b;
    }
}
// while 반복문의 조건을 이용한 구현
// if(...)  break; 로 구현 가능
```