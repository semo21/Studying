# Chapter 16 Step 04
- [4949 번](https://www.acmicpc.net/problem/4949)

## 난이도
- 실버 4

## 핵심
- 주어진 문자열 판단

## 풀이
```c++
#include <iostream>
#include <string>
#include <stack>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    while(true){
        std::string line;
        std::getline(std::cin, line);
        if(line == ".")   break;
        
        std::stack<char> st;
        bool bValid = true;
        for(char c : line){
            if(c == '(' || c == '['){
                st.push(c);
            }else if(c == ')'){
                if(st.empty() || st.top() != '('){
                    bValid = false;
                    break;
                }
                st.pop();
            }else if(c == ']'){
                if(st.empty() || st.top() != '['){
                    bValid = false;
                    break;
                }
                st.pop();
            }
        }

        if(!st.empty()) bValid = false;
        std::cout << (bValid ? "yes\n" : "no\n");
    }

    return 0;
}
```
- getline()으로 입력을 받아야 함 -> 공백도 포함한 입력이기때문
- 조건에 맞는 분기 설정
- 처리되지 않은 `(`나 `[`가 있다면 추가로 false로 설정