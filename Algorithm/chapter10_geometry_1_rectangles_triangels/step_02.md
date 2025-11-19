# step 2
- [1085 번](https://www.acmicpc.net/problem/1085)
## 난이도
- 브론즈 3
## 핵심
- 직사각형과 점의 최소 거리 구하기

## 풀이
```c++
#include <iostream>
#include <algorithm>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int x, y, w, h;

    std::cin >> x >> y >> w >> h;

    int minX = std::min(x, w-x);
    int minY = std::min(y, h-y);
    std::cout << std::min(minX, minY) << '\n';

    return 0;
}

// algorithm 헤더의 최솟값을 구하는 함수인 min을 사용하여 풀이
```