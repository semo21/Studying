# Chapter 16 Step 06
- [18258 번](https://www.acmicpc.net/problem/18258)

## 난이도
- 실버 4

## 핵심
- 큐의 개념

## 풀이
```c++
#include <iostream>
#include <string>
#include <queue>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int N;
    std::cin >> N;

    std::queue<int> q;
    while(N--){
        std::string cmd;
        std::cin >> cmd;

        if(cmd == "push"){
            int x;
            std::cin >> x;

            q.push(x);
        }else if(cmd == "pop"){
            if(q.empty())   std::cout << -1 << '\n';
            else{
                std::cout << q.front() << '\n';
                q.pop();
            }                   
        }else if(cmd == "size"){
            std::cout << q.size() << '\n';
        }else if(cmd == "empty"){
            std::cout << (q.empty() ? 1 : 0) << '\n';
        }else if(cmd == "front"){
            std::cout << (q.empty() ? -1 : q.front()) << '\n';
        }else if(cmd == "back"){
            std::cout << (q.empty() ? -1 : q.back()) << '\n';
        }
    }

    return 0;
}
```
- queue의 기본적인 기능 구현