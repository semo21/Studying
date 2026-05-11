# step 9
- [2438번](https://www.acmicpc.net/problem/2438)
## 난이도
- 브론즈 5
## 핵심
- 반복문, 입출력 구현

## 풀이
```c++
#include <iostream>

int main(){
    int n;
    std::cin >> n;
    
    for(int i = 0;i < n; i++){
        for (int j = 0; j < i+1; j++){
            std::cout << "*";
        }
        std::cout << "\n";
    }

    return 0;
}

// 1<= n <= 100
// j+1까지 반복하여 *출력 반복
// i반복 마지막 개행문자로 줄바꿈
```