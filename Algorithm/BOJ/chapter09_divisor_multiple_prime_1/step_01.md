# step 1
- [5086 번](https://www.acmicpc.net/problem/5086)
## 난이도
- 브론즈 3
## 핵심
- 반복문 조건부 설정, 배수와 약수 구분 구현

## 풀이
```c++
#include <iostream>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int a, b;
    
    while((std::cin >> a >> b) && !(a == 0 && b == 0)){
        if(b % a == 0){
            std::cout << "factor" << '\n';
        }else if(a % b == 0){
            std::cout << "multiple" << '\n';
        }else{
            std::cout << "neither" << '\n';
        }
    }
    return 0;
}

// while 조건부에서 입력을 받으며 바로 0 0 입력인지 판단
// 이후 코드는 문제에서 주어진대로 작성
```