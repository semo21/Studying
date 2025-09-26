# step 4
- [14681번](https://www.acmicpc.net/problem/14681)
## 난이도
- 브론즈 5
## 핵심
- 좌표에 따른 사분면 분류

## 풀이
```c++
#include <iostream>

int main(){
    int x, y;
    std::cin >> x;
    std::cin >> y;

    bool bIsXPlus = (x > 0);
    bool bIsYPlus = (y > 0);

    int quadrant;
    if(bIsXPlus && bIsYPlus){
        quadrant = 1;
    }else if(!bIsXPlus && bIsYPlus){
        quadrant = 2;
    }else if(!bIsXPlus && !bIsYPlus){
        quadrant = 3;
    }else{
        quadrant = 4;
    }

    std::cout << quadrant << std::endl;
    return 0;
}

// -1000 <= x, y <= 1000
// x != 0, y != 0
// x와 y 각 음수/양수 판별
// 경우의 수에 따라 1~4분면으로 구분
// 
```