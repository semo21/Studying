# step 7
- [2480번](https://www.acmicpc.net/problem/2480)
## 난이도
- 브론즈 4
## 핵심
- 사칙연산 분기별 수행

## 풀이
```c++
#include <iostream>

int main(){
    int a, b, c;
    std::cin >> a >> b >> c;

    int result;
    if(a==b && b==c){
        result = 10000 + (1000*a);
    }else if(a==b || a==c){
        result = 1000 + (100*a);
    }else if(b==c){
        result = 1000 + (100*b);
    }else{        
        int max = a;
        if(b > max) max = b;
        if(c > max) max = c;
        
        result = 100*max;
    }
    std::cout << result << std::endl;
    return 0;
}

// 두 수가 같은 경우를 [a와 b, a와 c], [b와 c] 비교로 통합
// 각기 다른 수 일 경우, 반복문이 아닌 조건문으로 최대값을 가려냄.
// if조건문을 사용하여 빠짐없이 최대값을 탐색하도록 설계.
```