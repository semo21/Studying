# step 8
- [1152 번](https://www.acmicpc.net/problem/1152)
## 난이도
- 브론즈 2
## 핵심
- 문자열 구현

## 풀이
```c++
#include <iostream>
#include <string>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);

    std::string input;
    std::getline(std::cin, input);
    
    int count = 0;
    bool bInWord = false;
    
    for(char e : input){        
        if(e != ' '){
            if(!bInWord){
                count++;
            bInWord = true;
            }            
        }else{
            bInWord = false;
        }
    }
    std::cout << count << '\n';

    return 0;
}

// string 헤더를 명시해주는 편이 좋음.
// 일반적인 컴파일러 구현체들은 iostream에 string이 포함되어 있음. (ex MSVC, GCC, Clang)
// 하지만 아닌 경우도 있기 때문에 string을 명시해주는 편이 범용성 향상에 도움이 됨.
// 메모리 3680 KB / 시간 4 ms
#include <iostream>
#include <string>
#include <sstream>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);

    std::string input;
    std::getline(std::cin, input);

    std::stringstream sStream(input);
    std::string word;
    int count = 0;
    while(sStream >> word)  count ++;
    
    std::cout << count << '\n';

    return 0;
}
// string stream을 이용하여 공백을 구분하는 풀이
// string stream은 공백을 알아서 구분하므로 word에 입력할 때, 공백단위로 구분해줌.
// 따라서 word에 입력할 때 count증가
// 이 풀이는 가독성, 코드 편의성, 범용성면에서 낫지만 비용이 더 많이 듬
// 메모리 5180 KB / 시간 24 ms
```