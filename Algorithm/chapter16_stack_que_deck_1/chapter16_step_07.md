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
// [방법 1] 시뮬레이션 방식 (O(N))
// std::queue를 사용하여 문제의 동작(버림-보냄)을 직접 구현
// 직관적이지만 N과 연산횟수 정비례
```
```c++
#include <iostream>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);

    int N;
    std::cin >> N;

    int L = 1;
    while((L << 1) <= N) L <<= 1;
    int r = N - L;
    if(r == 0)  std::cout << N << '\n';
    else std::cout << 2 * r << '\n';

    return 0;
}
// [방법 2] 수학적 최적화 방식(O(1))
// N장의 카드에서 가장 가까운 2의 거듭제곱(L)을 뺀 나머지(r)을 구함
// r번의 '버리고-보내기' 세트가 끝나는 순간, 큐는 L장(2의 거듭제곱)이 남음
// 남은 카드의 개수가 2의 거듭제곱인 상태에선 가장 마지막에 있는 카드가 승리하는 규칙을 적용
// 따라서 최종 생존 카드는 r번째로 뒤로 보낸 2r이 됨
// 단, N이 2의 거듭제곱인 경우(r=0)엔 정답은 N
```
