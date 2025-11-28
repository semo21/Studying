# step 3
- [19532 번](https://www.acmicpc.net/problem/19532)

## 난이도
- 브론즈 2

## 핵심
- x와 y의 해 구하기

## 풀이
```c++
#include <iostream>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int a, b, c, d, e, f;
    std::cin >> a >> b >> c >> d >> e >> f;

    for(int x = -999; x <= 999; ++x){
        for(int y = -999; y <= 999; ++y){
            int first = (a*x) + (b*y);
            int second = (d*x) + (e*y);
            if(first == c && second == f){
                std::cout << x << ' ' << y << '\n';
            }
        }
    }    
    
    return 0;
}

// 정석적인 브루트 포스 탐색
// 주어진 범위 안을 모두 탐색하여 해 구하기

#include <iostream>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int a, b, c, d, e, f;
    std::cin >> a >> b >> c >> d >> e >> f;
    
    int x = ((c*e)-(b*f))/((a*e)-(b*d));
    int y = ((a*f)-(c*d))/((a*e)-(b*d));
    std::cout << x << ' ' << y << '\n';
    return 0;
}
// x구하기
// ax+by=c, dx+ey=f 에 두 식에 각각 e와 b를 곱하기
// aex+bey=ce, bdx+bey=bf
// (ae-bd)x = ce-bf
// x = (ce-bf)/(ae-bd)
// 
// y구하기
// 두 식에 각각 d와 a를 곱하기
// adx+bdy=cd, adx+aey=af
// (bd-ae)y = (cd-af)
// y = (cd-af)/(bd-ae)
// y = (af-cd)/(ae-bd)
// x = (ce-bf)/(ae-bd)

```