# step 5
- [1157 번](https://www.acmicpc.net/problem/1157)
## 난이도
- 브론즈 1
## 핵심
- 반복문을 통한 출력규칙 구현

## 풀이
```c++
#include <iostream>
#include <string>
#include <cctype>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);

    std::string input;
    std::cin >> input;

    int freq[26] = {0};
    
    for(char c : input){
        char upper = std::toupper(c);
        freq[upper - 'A']++;
    }

    int max = 0;
    char result = '?';
    for(int i = 0; i < 26; i++){
        if(freq[i] > max){
            max = freq[i];
            result = 'A' + i;
        }else if(freq[i] == max){
            result = '?';
        }
    }
    
    std::cout << result << '\n';

    return 0;
}

// cctype 헤더의 함수 toupper(char)사용
// 알파벳의 중복횟수를 기록할 배열을 생성하여 기록
```