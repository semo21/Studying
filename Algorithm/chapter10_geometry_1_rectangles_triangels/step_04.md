# step 4
- [15894 번](https://www.acmicpc.net/problem/15894)
## 난이도
- 브론즈 3
## 핵심
- 피라미드 도형 둘레 구하기

## 풀이
```c++
#include <iostream>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    long long n;
    std::cin >> n;
    std::cout << 4*n << '\n';

    return 0;
}

// 4. 8. 12. 16 ... 
// n번째줄 추가 -> K(n) = K(n-1)(기존) -(n-1) + (n+3) = K(n-1) + 4
// 결과적으로 4씩 증가
// 따라서 실선의 크기는 4 * n
```