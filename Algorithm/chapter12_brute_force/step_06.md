# step 6
- [2839 번](https://www.acmicpc.net/problem/2839)

## 난이도
- 실버 4

## 핵심
- 수학 혹은 브루트 포스 풀이

## 풀이
```c++
#include <iostream>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int N;
    std::cin >> N;

    int bags = 0;
    for(int i = N/5; i >= 0; --i){
        if((N-(5*i))%3==0){
            bags = i + (N-(5*i))/3;
            break;
        }
    }

    if(!bags)   bags = -1;
    std::cout << bags << '\n';
    return 0;
}

// 브루트 포스 풀이
// 5로 채울 수 있는 만큼 구하고
// 그 나머지가 3으로 나누어 떨어진다면 해
// 5로 최대한 많이 채워야하므로 i = N/5부터 --i하며 역순으로 내려감
// N >=3 이므로 bags가 0이라면 해가 없으므로 bags = -1
// 정리된 bags를 출력

#include <iostream>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    


    return 0;
}
// 5x + 3y = N
// 3y = -5x + N
// y = -5x/3 + N/3
// y = 0 일때 x > 0, 5x < N, x < N / 5
// x = 0 일때 y > 0, N > 3

```