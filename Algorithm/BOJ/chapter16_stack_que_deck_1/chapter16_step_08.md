# Chapter 16 Step 08
- [11866 번](https://www.acmicpc.net/problem/11866)

## 난이도
- 실버 4

## 핵심
- 큐를 사용하여 동작 구현. 요세푸스 순열

## 풀이
```c++
#include <iostream>
#include <queue>

int main() {
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);

    int N, K;
    std::cin >> N >> K;

    std::queue<int> q;
    for (int i = 1; i <= N; i++) {
        q.push(i);
    }

    std::cout << "<";
    while (!q.empty()) {
        for (int i = 0; i < K - 1; i++) {
            q.push(q.front());
            q.pop();
        }

        std::cout << q.front();
        q.pop();

        if (!q.empty()) {
            std::cout << ", ";
        }
    }
    std::cout << ">\n";

    return 0;
}
// std::queue를 사용하여 문제의 동작(버림-보냄)을 직접 구현
```