# step 5
- [2581 번](https://www.acmicpc.net/problem/2581)
## 난이도
- 브론즈 2
## 핵심
- 소수 탐색 구현

## 풀이
```c++
#include <iostream>
#include <vector>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int m, n, sum, min;
    std::cin >> m;
    std::cin >> n;
    sum = 0; min = -1;

    for(int i = m; i <= n; i++){
        if(i < 2)   continue;

        bool bPrime = true;
        for(int j = 2; j * j <= i; j++){
            if(i % j == 0) { bPrime = false; break; }
        }
        if(bPrime) {
            sum+=i;             
            if(min == -1) min = i;
        }
    }

    if(min == -1)  {
        std::cout << -1 << '\n';
    }
    else {
        std::cout << sum << '\n';
        std::cout << min << '\n';
    }
    return 0;
}

// 주어진 수(i)의 제곱근보다 큰 약수는 없으므로 j의 범위를 i의 제곱근을 넘지 않도록 설정
// 탐색하여 소수가 맞다면 합계(sum)에 추가
// 만약 최솟값이 설정되지 않은 상태라면(min=-1, 주어진 수는 자연수이므로 -1보다 큼) 최소값 설정
// 마지막에 소수가 한 번도 탐색되지 않음을 감지했다면(min=-1) -1출력
// 소수가 탐색되었다면 합계와 최솟값 출력
```