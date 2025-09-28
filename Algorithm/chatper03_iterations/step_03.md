# step 7
- [8393번](https://www.acmicpc.net/problem/8393)
## 난이도
- 브론즈 5
## 핵심
- 반복문, 덧셈, 입출력 구현

## 풀이
```c++
#include <iostream>

int main(){
    int n;
    int result = 0;
    std::cin >> n;
    for (int i = 0; i < n; i++){
        result += i+1;
    }
    std::cout << result << std::endl;
    return 0;
}

// 1 <= n <= 10000
// n회 실행하는 반복문에서 1부터 n까지의 합 출력
// 등차수열 합 공식인 n((2*base)+(n-1)*diff))/2 로 풀이도 가능.
// std::cout << n*(1+n)/2 << std::endl;
```