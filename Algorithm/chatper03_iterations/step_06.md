# step 6
- [15552번](https://www.acmicpc.net/problem/15552)
## 난이도
- 브론즈 4
## 핵심
- 반복문, 입출력 구현

## 풀이
```c++
#include <iostream>

int main(){
    int t;
    std::cin.tie(NULL);
    std::ios::sync_with_stdio(false);
    std::cin >> t;

    for(int i = 0; i < t; i++){
        int a, b;
        std::cin >> a >> b;
        std::cout << a+b << "\n";
    }

    return 0;
}

// 0 <= t <= 1,000,000
// 1 <= a, b <= 1,000
// 반복문 실행 속도 향상을 위한 cin.tie(NULL)과 sync_with_stdio(false)설정 
// std::endl 대신 개행문자 "\n"사용.
```