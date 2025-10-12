# step 4
- [11654 번](https://www.acmicpc.net/problem/11654)
## 난이도
- 브론즈 5
## 핵심
- 문자열의 아스키 코드 변환 구현

## 풀이
```c++
#include <iostream>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    char input;
    std::cin >> input;
    std::cout << (int)input << "\n";

    return 0;
}

// 입력값은 알파벳 대/소문자, 숫자0~9 중 하나로 고정
// 입력값을 char형식으로 고정
// 입력값을 int로 형변환하여 출력
```