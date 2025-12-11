# step 4
- [10989 번](https://www.acmicpc.net/problem/10989)

## 난이도
- 브론즈 1

## 핵심
- 카운팅 정렬 사용

## 풀이
```c++
#include <iostream>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);

    int arr[10001] = {0};
    int N, x;
    std::cin >> N;
    for(int i = 0; i < N; ++i){
        std::cin >> x;
        arr[x]++;
    }

    for(int i = 1; i <= 10000; ++i){
        while(arr[i]--) {
            std::cout << i << '\n';
        }
    }

    return 0;
}

// 병합 정렬은 메모리초과로 사용불가
// 설명에 나와있던 카운팅정렬을 활용
// 카운팅 정렬의 시간복잡도는 O(N + k)
// k의 범위는 1 ~ 10000이므로 해당 수를 인덱스삼아 중복 횟수를 저장
// 배열을 순회하며 중복된만큼 출력
```