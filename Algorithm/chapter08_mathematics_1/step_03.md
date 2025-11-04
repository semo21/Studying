# step 3
- [2720 번](https://www.acmicpc.net/problem/2720)
## 난이도
- 브론즈 3
## 핵심
- 진법 변환

## 풀이
```c++
#include <iostream>
#include <string>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
   
    int t, c;
    std::cin >> t;
    while(t--){        
        std::cin >> c;

        std::cout << c / 25 << ' ';  c%=25;
        std::cout << c / 10 << ' ';  c%=10;
        std::cout << c / 5 << ' ';   c%=5;
        std::cout << c << '\n';
    }
    return 0;
}

// 각 동전의 가치만큼 셈을 바로 출력하며 나머지 값을 정리
```