# step 5
- [2884번](https://www.acmicpc.net/problem/2884)
## 난이도
- 브론즈 3
## 핵심
- 시간 계산(24시간, 분 단위 순환)

## 풀이
```c++
#include <iostream>

int main(){
    int a, b;
    std::cin >> a >> b;

    if(b-45 < 0){
        a -= 1;
        b += 15;
        if(a < 0){
            a = 23; 
        }
    }else{
        b -= 45;
    }
    std::cout << a << " " << b << std::endl;

    return 0;
}

// 0 <= a <= 24, 0 <= b <= 59
// 분이 45보다 작다면:
// 60을 더해 보정한 뒤, 시간에서 1을 뺀다.
// 시간이 0보다 작아진다면:
// 23시로 되돌린다.(이전 날로 취급하지만, 문제에선 날짜는 출력하지 않음)
```