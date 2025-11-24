# step 8
- [14215 번](https://www.acmicpc.net/problem/14215)

## 난이도
- 브론즈 3

## 핵심
- 가능한 둘레가 긴 삼각형 만들기

## 풀이
```c++
#include <iostream>
#include <algorithm>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int a, b, c, result;
    std::cin >> a >> b >> c;
    
    int maxSide = std::max({a, b, c});
    int sum = a + b + c;
    if(sum - maxSide > maxSide) result = sum;
    else   result = ((sum - maxSide) * 2) - 1;
    
    std::cout << result << '\n';

    return 0;
}

// 삼각형의 구성 조건 중 하나는 가장 긴 변의 길이가 나머지 두변의 합보다 크거나 같지 않은 것.
// 변의 길이는 정수이므로 else의 계산식 내용에서 -1
```