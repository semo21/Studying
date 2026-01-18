# Chapter 16 Step 02
- [10773 번](https://www.acmicpc.net/problem/10773)

## 난이도
- 실버 4

## 핵심
- 가장 최근에 작성한 숫자 지우기

## 풀이
```c++
#include <iostream>
#include <stack>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int K;
    std::cin >> K;

    std::stack<int> st;
    while(K--){
        int x;
        std::cin >> x;
        if(x == 0){
            st.pop();
        }else{
            st.push(x);
        }
    }    

    long long t = 0;
    while(!st.empty()){
        t += (long long)st.top();
        st.pop();
    }
    std::cout << t << '\n';
    return 0;
}
```
```c++
#include <iostream>
#include <vector>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);

    int K;
    std::cin >> K;

    long long total = 0;
    std::vector<int> st;
    st.reserve(K);
    while(K--){
        int x;
        std::cin >> x;
        if(x == 0){
            total -= st.back();
            st.pop_back();
        }else{
            st.push_back(x);
            total += x;
        }
    }

    std::cout << total << '\n';
    return 0;
}

```
- stack과 vector를 이용한 풀이.
- 두번째 풀이에선 합산값을 수를 입력받는 동시에 처리
- 따라서 두번째 풀이는 마지막 합산을 위한 추가 순회가 없음