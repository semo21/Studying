# step 6
- [10101 번](https://www.acmicpc.net/problem/10101)
## 난이도
- 브론즈 4
## 핵심
- 각도로 삼각형 판별 및 분류

## 풀이
```c++
#include <iostream>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int tri[3] = {0};
    for(int i = 0; i < 3; i++){        
        std::cin >> tri[i];
    }

    if(tri[0]+tri[1]+tri[2] != 180)  std::cout << "Error" << '\n';
    else if(tri[0] == tri[1] && tri[1] == tri[2])    std::cout << "Equilateral" << '\n';
    else if(tri[0] == tri[1] || tri[0] == tri[2] || tri[1] == tri[2])    std::cout << "Isosceles" << '\n';
    else if(tri[0] != tri[1] && tri[1] != tri[2] && tri[0] != tri[2])   std::cout << "Scalene" << '\n';
    return 0;
}

// 조건별로 분기 구현

#include <iostream>
#include <array>
#include <algorithm>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    std::array<int, 3> tri{};
    for(int &x : tri)  std::cin >> x;
    
    if(tri[0]+tri[1]+tri[2] != 180){
        std::cout << "Error\n";
    }
    else if(tri[0] == tri[1] && tri[1] == tri[2]){
        std::cout << "Equilateral\n";
    }
    else if(tri[0] == tri[1] || tri[0] == tri[2] || tri[1] == tri[2]){
        std::cout << "Isosceles\n";
    }    
    else{
        std::cout << "Scalene\n";
    }
    return 0;
}

// 개선된 버전
```