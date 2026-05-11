# Chapter 16 Step 09
- [28279 번](https://www.acmicpc.net/problem/28279)

## 난이도
- 실버 4

## 핵심
- 덱 활용

## 풀이
```c++
#include <iostream>
#include <deque>

int main() {
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);

    int N;
    std::cin >> N;

    std::deque<int> dq;
    for(int i = 0; i < N; ++i){
        int cmd;
        std::cin >> cmd;
        
        switch(cmd){
            case 1:{
                int x;
                std::cin >> x;
                dq.push_front(x);
                break;
            }                
            case 2:{
                int x;
                std::cin >> x;
                dq.push_back(x);
                break;
            }
            case 3:{
                if(dq.empty())  std::cout << -1 << '\n';
                else {
                    std::cout << dq.front() << '\n';
                    dq.pop_front();
                }
                break;
            }
            case 4:{
                if(dq.empty())  std::cout << -1 << '\n';
                else{
                    std::cout << dq.back() << '\n';
                    dq.pop_back();
                }
                break;
            }
            case 5:{
                std::cout << dq.size() << '\n';
                break;
            }
            case 6:{
                std::cout << dq.empty() << '\n';
                break;
            }
            case 7:{
                if(dq.empty())  std::cout << -1 << '\n';
                else            std::cout << dq.front() << '\n';
                break;
            }
            case 8:{
                if(dq.empty())  std::cout << -1 << '\n';
                else            std::cout << dq.back() << '\n';\
                break;
            }            
        }
    }

    return 0;
}
// switch와 deque를 이용하여 풀이
```