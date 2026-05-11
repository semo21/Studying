# step 5
- [11720 번](https://www.acmicpc.net/problem/11720)
## 난이도
- 브론즈 4
## 핵심
- 문자열의 아스키 코드 변환 구현

## 풀이
```c++
#include <iostream>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);

    int n, sum;
    sum = 0;
    std::cin >> n;
    
    std::string input;
    std::cin >> input;

    for(char e : input){
        sum += (e - '0');
    }
    std::cout << sum << "\n";
    return 0;
}

// char 형식은 int 값처럼 연산 가능.
// 하지만 char '0' != 0
// 그러므로 모든 값에서 char '0'의 값만큼 빼서 계산값 보정
```