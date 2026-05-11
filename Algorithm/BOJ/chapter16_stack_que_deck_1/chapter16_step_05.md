# Chapter 16 Step 05
- [12789 번](https://www.acmicpc.net/problem/12789)

## 난이도
- 실버 3

## 핵심
- 오름차순으로 요소 빼내기

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
    int need = 1;
    for(int i = 0; i < N; ++i){
        int x;
        std::cin >> x;

        if(x == need){
            ++need;
        }else{
            if(!st.empty() && st.top() < x){                
                break;
            }
            st.push(x);
        }

        while(!st.empty() && (st.top() == need)){
            st.pop();
            ++need;
        }
    }

    std::cout << (need == N + 1 ? "Nice\n" : "Sad\n");

    return 0;
}
```
- need라는 요구되는 번호를 선언하고 시작
- 조건에 충족하는 수를 입력받으면 다음 번호로 ++
- 입력받은 번호에 대한 판단이 끝났다면 while문을 통해 stack에 저장된 것들을 꺼내며 판단
- `if(!st.empty() && st.top() < x){ break; }` 분기는 Nice가 성립될 수 없는 조건이기에 추가