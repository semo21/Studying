# step 6
- [11653 번](https://www.acmicpc.net/problem/11653)
## 난이도
- 브론즈 1
## 핵심
- 소인수분해 구현

## 풀이
```c++
#include <iostream>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int n;
    int i = 2;
    std::cin >> n;
    while(n>1){
        if(n%i == 0){
            std::cout << i << '\n';
            n /= i;
        }else{
            i++;
        }
    }

    return 0;
}
// 아래와 위 풀이는 모두 메모리는 동일하지만 시간 차이가 있음
// 위 풀이는 시간 24ms
// 단순히 매 수를 탐색하며 약수인 것들을 출력

#include <iostream>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int n;    
    std::cin >> n;
    
    for(int i = 2; i * i <= n; i++){
        while(n % i == 0){
            std::cout << i << '\n';
            n /= i;
        }
    }
    if(n > 1) std::cout << n << '\n';

    return 0;
}
// 위 풀이는 시간 0ms
// 진약수를 제외한 약수는 제곱근의 크기보다 작다는 사실을 활용
// 따라서 n의 제곱근까지만 약수탐색
// 이후 n이 1보다 큰 소수라면 출력하는 조건문 작성
```