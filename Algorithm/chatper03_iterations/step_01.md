# step 7
- [2739번](https://www.acmicpc.net/problem/2739)
## 난이도
- 브론즈 5
## 핵심
- 반복문, 곱셈, 입출력 구현

## 풀이
```c++
#include <iostream>

int main(){
    int a;
    std::cin >> a;
    for(int i = 0; i < 9; i++){
        std::cout << a << " * " << i+1 << " = " << a*(i+1) <<std::endl;
    }

    return 0;
}

// 1 <= a <= 9
// 구구단구현이므로 반복문의 루프는 9회로 설정
```