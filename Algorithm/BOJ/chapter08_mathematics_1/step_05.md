# step 5
- [2292 번](https://www.acmicpc.net/problem/2292)
## 난이도
- 브론즈 2
## 핵심
- 입력받은 수 범위 탐색

## 풀이
```c++
#include <iostream>
#include <string>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    long n;
    std::cin >> n;

    long layer = 1;
    long max = 1;

    while(n > max){
        max += 6*layer;
        layer++;
    }
    std::cout << layer << '\n';
    return 0;
}

// 한 겹이 늘어날 때 마다 (6 * 겹의 수)만큼 총 칸의 개수가 증가함.
// 1 + 6*(layer-1) < 결과 <= 1 + 6*(layer)
// 이것을 감지할 수 있는 조건문을 세우는 것이 핵심.
```