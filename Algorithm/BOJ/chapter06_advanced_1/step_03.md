# step 3
- [2444 번](https://www.acmicpc.net/problem/2444)
## 난이도
- 브론즈 3
## 핵심
- 반복문을 통한 출력규칙 구현

## 풀이
```c++
#include <iostream>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);

    int n;
    std::cin >> n;
    for(int i = 1; i <= n; i++){
        for(int j = 1; j <= n-i; j++)    std::cout << ' ';
        for(int j = 1; j <= (2*i)-1; j++)    std::cout << '*';        
        std::cout << '\n';
    }

    for(int i = n - 1; i >= 1; i--){
        for(int j = 1; j <= n - i; j++) std::cout << ' ';
        for(int j = 1; j <= (2*i)-1; j++)   std::cout << '*';
        std::cout << '\n';
    }

    return 0;
}

// 윗쪽 삼각형과 아랫쪽 삼각형 출력을 나눠서 구현
// 별을 찍은 이후엔 공백이 필요없음
```