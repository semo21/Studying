# Chapter 16 Step 07
- [2164 번](https://www.acmicpc.net/problem/2164)

## 난이도
- 실버 4

## 핵심
- 큐를 사용하여 동작 구현

## 풀이
```c++
#include <iostream>
#include <queue>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int N;
    std::cin >> N;

    std::queue<int> q;
    for(int i = 0; i < N; ++i){
        q.push(i+1);
    }
    while(q.size() > 1){
        q.pop();
        q.push(q.front());
        q.pop();
    }

    std::cout << q.front() << '\n';
    return 0;
}
```
```c++
#include <iostream>
#include <queue>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);

    int N;
    std::cin >> N;

    int L = 1;
    while((L << 1) <= N) L <<= 1;
    
    if(N == L)  std::cout << N << '\n';
    else std::cout << 2 * (N - L) << '\n';

    return 0;
}
```
