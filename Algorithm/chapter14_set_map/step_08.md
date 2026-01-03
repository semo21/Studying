# step 08
- [11478 번](https://www.acmicpc.net/problem/11478)

## 난이도
- 실버 3

## 핵심
- 집합을 활용한 중복제거 

## 풀이
```c++
#include <iostream>
#include <set>
#include <string>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    std::string s;
    std::cin >> s;

    std::set<std::string> st;

    int  n = (int)s.size();
    for(int i = 0; i < n; ++i){
        std::string cur;
        cur.reserve(n - i);
        for(int j = i; j < n; ++j){
            cur.push_back(s[j]);
            st.insert(cur);
        }
    }

    std::cout << st.size() << '\n';

    return 0;
}

// Set는 중복되는 요소가 없음
// 따라서 모든 부분집합을 set에 저장하면 중복제거가 가능함
// Set에 모두 저장한 후에 Set의 크기를 구하여 풀이
// Set의 크기는 서로 다른 부분집합의 개수이기 때문에 풀이가능
```