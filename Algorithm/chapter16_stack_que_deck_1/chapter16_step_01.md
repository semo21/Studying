# Chapter 16 Step 01
- [28278 번](https://www.acmicpc.net/problem/28278)

## 난이도
- 실버 4

## 핵심
- 스택의 개념 이해

## 풀이
```c++
#include <iostream>
#include <stack>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int N;
    std::cin >> N;

    std::stack<int> st;
    while(N--){
        int cmd;
        std::cin >> cmd;

        if(cmd == 1){
            int x;
            std::cin >> x;

            st.push(x);
        }else if(cmd == 2){
            if(st.empty()){
                  std::cout << -1 << '\n';
            }
            else{
                std::cout << st.top() << '\n';
                st.pop();
            }
        }else if(cmd == 3){
            std::cout << st.size() << '\n';
        }else if(cmd == 4){
            std::cout << (st.empty() ? 1 : 0) << '\n';
        }else if(cmd == 5){
            if(st.empty())  std::cout << -1 << '\n';
            else    std::cout << st.top() << '\n';
        }
    }

    return 0;
}
```
```c++
#include <iostream>
#include <vector>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);

    int N;
    std::cin >> N;

    std::vector<int> st;
    st.reserve(N);

    while(N--){
        int cmd;
        std::cin >> cmd;

        if(cmd == 1){
            int x;
            std::cin >> x;
            st.push_back(x);
        }else if(cmd == 2){
            if(st.empty()){
                std::cout << -1 << '\n';
            }else{
                std::cout << st.back() << '\n';
                st.pop_back();
            }
        }else if(cmd == 3){
            std::cout << st.size() << '\n';
        }else if(cmd == 4){
            std::cout << (st.empty() ? 1 : 0) << '\n';
        }else if(cmd == 5){
            if(st.empty())  std::cout << -1 << '\n';
            else    std::cout << st.back() << '\n';
        }
    }
    return 0;
}
```
- stack을 이용한 풀이와 vector를 이용한 풀이.
- 기본적인 기능 구현만 하면 완료