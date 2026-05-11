# Chapter 16 Step 03
- [9012 번](https://www.acmicpc.net/problem/9012)

## 난이도
- 실버 4

## 핵심
- 주어진 문자열 판단

## 풀이
```c++
#include <iostream>
#include <string>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int T;
    std::cin >> T;
    
    for(int i = 0; i < T; ++i){
        std::string str;
        std::cin >> str;

        int ps = 0;
        for(char c : str){
            if(c == '(')    ++ps;
            else if(c == ')')   --ps;

            if(ps < 0)  break;
            
        }
        if(ps == 0) std::cout << "YES" << '\n';
        else    std::cout << "NO" << '\n';
    }

    return 0;
}
```
```c++
#include <iostream>
#include <string>
#include <stack>

int main(){

    int T;
    std::cin >> T;

    while(T--){
        std::string str;
        std::cin >> str;

        std::stack<char> stack;
        bool bVPS = true;
        for(char c : str){
            if(c == '('){
                stack.push(c);
            }    
            else if(c == ')'){
                if(stack.empty()){
                    bVPS = false;
                    break;
                }   
                stack.pop();
            }
        }
        if(!stack.empty())  bVPS = false;
        std::cout << (bVPS ? "YES\n" : "NO\n");
    }

    return 0;
}
```
- stack이 없는 풀이와 stack으로 푸는 풀이
- )(는 두 괄호, '(', ')'의 수가 동일하지만 VPS가 될 수 없음을 생각
- 따라서 '('로 시작해서 ')'로 끝나는 문자열을 찾아야 함
- 그렇기 때문에 '('는 1 또는 push, ')'는 -1 또는 pop으로 구분
- 만약 판단변수(ps, stack)가 0 미만 혹은 empty()에서 ')'입력이 된다면 NO조건 충족하여 break
- stack에선 break 이후에 남은 문자열이 있을 수 있으니 if(!stack.empty()) bVPS = false를 통해 한번 더 처리해줌
- 마지막에 if(stack.empty())    cout << "YES\n"; 는 `())(`같은 곳에서 YES출력이 될 수 있기 때문