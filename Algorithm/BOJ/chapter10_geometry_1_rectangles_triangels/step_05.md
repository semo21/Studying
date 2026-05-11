# step 5
- [9063	번](https://www.acmicpc.net/problem/9063)
## 난이도
- 브론즈 3
## 핵심
- 점을 모두 포함하는 최소크기 직사각형 구현

## 풀이
```c++
#include <iostream>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int N, minX, maxX, minY, maxY;
    std::cin >> N;

    for(int i = 0; i < N; i++){
        int x, y;
        std::cin >> x >> y;
        if(i == 0){
            minX = x; maxX = x;
            minY = y; maxY = y;
        }

        if(x < minX)    minX = x;
        if(x > maxX)    maxX = x;
        if(y < minY)    minY = y;
        if(y > maxY)    maxY = y;        
    }

    std::cout << (maxX - minX) * (maxY - minY) << '\n';

    return 0;
}

// 첫 입력에 minX, maxX, minY, maxY를 초기화
// 이후 min, max를 비교하며 갱신


#include <iostream>
#include <algorithm>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int N, minX, maxX, minY, maxY;
    std::cin >> N;

    int x, y;
    std::cin >> x >> y;
    minX = x; maxX = x;
    minY = y; maxY = y;    
    
    for(int i = 1; i < N; i++){
        std::cin >> x >> y;

        minX = std::min(minX, x);
        maxX = std::max(maxX, x);

        minY = std::min(minY, y);
        maxY = std::max(maxY, y);      
    }

    long long w = static_cast<long long>(maxX - minX);
    long long h = static_cast<long long>(maxY - minY);
    std::cout << w * h << '\n';

    return 0;
}

// 가독성과 형식 디테일을 조금 더 개선한 버전
```