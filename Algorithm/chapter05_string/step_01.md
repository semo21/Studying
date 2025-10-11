# step 1
- [27866 번](https://www.acmicpc.net/problem/27866)
## 난이도
- 브론즈 5
## 핵심
- 문자열, 문자열 요소 접근 구현

## 풀이
```c++
#include <iostream>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int a;
    std::string str;
    std::cin >> str >> a;

    std::cout << str[a-1] << "\n";

    return 0;
}

// sync_with_stdio(false) 실행
// cin.tie(nullptr) 실행
// 문자열을 배열취급하여 인덱스 요소 출력.
```