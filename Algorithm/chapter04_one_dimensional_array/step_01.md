# step 12
- [10951번](https://www.acmicpc.net/problem/10951)
## 난이도
- 브론즈 5
## 핵심
- 반복문, 덧셈, 조건문, EOF 구현

## 풀이
```c++
#include <iostream>

int main(){
    int a, b;
    while(std::cin >> a >> b){        
        std::cout << a+b << "\n";
    }
}
// 0 < a, b < 10
// End of File 구현이 핵심.
// 입력스트림의 끝에서 종료를 구현.
```