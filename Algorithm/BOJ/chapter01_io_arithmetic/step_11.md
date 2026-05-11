# step 11
- [11382번](https://www.acmicpc.net/problem/11382)
## 난이도
- 브론즈 5
## 핵심
- 입출력과 덧셈 구현

## 풀이
```c++
#include <iostream>

int main(){
    long a, b, c;
    std::cin >> a >> b >> c;
    std::cout << a+b+c << std::endl;

    return 0;
}

// 10^12 자릿수까지 입력받아야하므로 int가 아닌 long타입을 사용해야 함.
```