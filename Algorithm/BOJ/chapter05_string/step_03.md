# step 3
- [9086 번](https://www.acmicpc.net/problem/9086)
## 난이도
- 브론즈 5
## 핵심
- 문자열, 문자열 요소 출력 구현

## 풀이
```c++
#include <iostream>

int main(){
    int t;
    std::cin >> t;
    while(t--){
        std::string str;
        std::cin >> str;
        std::cout << str[0] << str[str.length()-1] << "\n";
    }

    return 0;
}

// 배열의 길이를 출력하는 length()함수 사용.
```