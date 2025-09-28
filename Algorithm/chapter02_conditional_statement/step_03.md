# step 3
- [2753번](https://www.acmicpc.net/problem/2753)
## 난이도
- 브론즈 5
## 핵심
- 사칙연산 후 조건에 따른 분기 구현

## 풀이
```c++
#include <iostream>

int main(){
    int a;
    std::cin >> a;
    bool bIsLeap = false;
    if(a%400 == 0){
        bIsLeap = true;
    }else if(a % 4 == 0 && a % 100 != 0){
        bIsLeap = true;
    }else{
        bIsLeap = false;
    }
    std::cout << (int)bIsLeap << std::endl;

    return 0;
}

// 1 <= a <= 4000
// 조건문들은 삼항 연산자로 작성 가능
// bool bIsLeap = (a & 400 == 0) || (a % 4 == 0 && a % 100 != 0);
```