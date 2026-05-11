# step 2
- [2501 번](https://www.acmicpc.net/problem/2501)
## 난이도
- 브론즈 3
## 핵심
- 약수 찾기

## 풀이
```c++
#include <iostream>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int n, k, i, j;

    std::cin >> n >> k;
    i = 1; j = 0;
    while(i <= n){
        if(n % i == 0)  j++;            
        
        if(j == k){
                std::cout << i << '\n';
                break;
            }
        i++;
    }
    if(j < k)  std::cout << 0 << '\n';
    
    return 0;
}

// 입력 받은 수보다 작은 수를 연산하며 약수를 탐색(i)
// 약수를 탐색할 때마다 현재 약수가 몇번째 약수인지 기록(j)
// k번째 약수라면(j==k) 현재 약수(i)출력.
// 루프가 끝나고 약수의 개수가 k보다 작다면 0 출력
```