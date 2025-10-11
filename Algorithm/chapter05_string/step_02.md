# step 2
- [2743 번](https://www.acmicpc.net/problem/2743)
## 난이도
- 브론즈 5
## 핵심
- 문자열, 문자열 길이 출력 구현

## 풀이
```c++
#include <iostream>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);

    std::string str;
    std::cin >> str;
    std::cout << str.length() << "\n";

    return 0;
}

// 배열의 길이를 출력하는 length()함수 사용.
```