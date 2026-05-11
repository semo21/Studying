# step 4
- [2903 번](https://www.acmicpc.net/problem/2903)
## 난이도
- 브론즈 3
## 핵심
- 진법 변환

## 풀이
```c++
#include <iostream>
#include <string>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
   
    int n;
    int k = 2;
    std::cin >> n;
    
    while(n--){
        k += k-1;
    }
    
    std::cout << k * k << '\n';
    return 0;
}

// 정사각 형의 각 변 중앙에 점을 추가하는 작업은
// (정사각형의 한 변의 점의 갯수 - 1) 개의 점을 추가하는 것
// 그리고 모든 점의 개수는 (한 변의 점의 갯수)^2이다.
```