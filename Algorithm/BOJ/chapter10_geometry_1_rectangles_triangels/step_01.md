# step 1
- [27323 번](https://www.acmicpc.net/problem/27323)
## 난이도
- 브론즈 5
## 핵심
- 도형의 넓이 구하기

## 풀이
```c++
#include <iostream>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int a, b;
    std::cin >> a;
    std::cin >> b;

    std::cout << a * b << '\n';

    return 0;
}

// 주어진 변의 길이를 서로 곱해 넓이 구하기
```