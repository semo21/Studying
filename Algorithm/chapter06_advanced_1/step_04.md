# step 4
- [10988 번](https://www.acmicpc.net/problem/10988)
## 난이도
- 브론즈 3
## 핵심
- 반복문을 통한 출력규칙 구현

## 풀이
```c++
#include <iostream>
#include <string>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);

    std::string input;
    std::cin >> input;
    
    bool bIsPalindrome = true;
    for(size_t i = 0; i < input.length()/2; i++){
        if(input[i] != input[input.length()-i-1]){
            bIsPalindrome = false;
            break;
        }  
    }

    std::cout << (int)bIsPalindrome << '\n';

    return 0;
}

// 팰린드롬은 문자의 순서를 뒤집어도 같은 단어임 (ex. 기러기, 토마토)
// 그러므로 문자열의 길이 / 2 만큼 순환하는 반복문을 실행
// 시작, 끝으로부터의 요소를 비교.
// 기본값은 true, 틀리면 false 후 반복문 중지
// 반복문의 횟수 i 타입은 size_t.
// string.length()는 size_t(unsigned int)를 반환하기 때문에 타입 일치시켜줘야함.
```