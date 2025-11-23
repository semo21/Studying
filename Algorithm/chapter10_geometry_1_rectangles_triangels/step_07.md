# step 6
- [5073 번](https://www.acmicpc.net/problem/5073)
## 난이도
- 브론즈 3
## 핵심
- 변의 길이로 삼각형을 판별 및 분류

## 풀이
```c++
#include <iostream>
#include <algorithm>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int a, b, c;    
    while(true){
        std::cin >> a >> b >> c;
        if(a == 0 && b == 0 && c == 0)  break;

        int maxSide = std::max({a, b, c});
        int sum = a + b + c;

        if (sum - maxSide <= maxSide){
            std::cout << "Invalid\n";
            continue;
        }

        if(a == b && b== c)
            std::cout << "Equilateral\n";
        else if(a == b || b == c || a == c)
            std::cout << "Isosceles\n";
        else
            std::cout << "Scalene\n";
    }

    return 0;
}

// algorithm 헤더의 max함수를 사용하여 입력받은 값 중 최댓값 탐색
// 가장 긴 변이 입력받은 값의 총합의 절반 이상이라면 Invalid
```