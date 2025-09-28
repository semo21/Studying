# step 1
- [1330번](https://www.acmicpc.net/problem/1330)
## 난이도
- 브론즈 5
## 핵심
- 비교 조건문 구현

## 풀이
```c++
#include <iostream>

int main(){
    int a, b;
    std::cin >> a >> b;
    std::string op = "";
    if(a>b){
        op = ">";
    }else if(a==b){
        op = "==";
    }else{
        op = "<";
    }
    std::cout << op << std::endl;

    return 0;
}

// -10000 <= A, B <= 10000 의 범위를 가짐.
// 따라서 int형 사용 가능
// A와 B의 크기 비교에 따라 다른 비교연산자를 문자열로 출력.
```