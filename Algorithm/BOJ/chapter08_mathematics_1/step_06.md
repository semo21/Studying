# step 6
- [1193 번](https://www.acmicpc.net/problem/1193)
## 난이도
- 실버 5
## 핵심
- 입력받은 수 범위 탐색

## 풀이
```c++
#include <iostream>
#include <string>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    long long x, num, den;
    std::cin >> x;
    int layer = 1;
    while(x > layer){
        x -= layer;
        layer++;
    }

    if(layer%2 == 1){
        num = layer - x + 1;
        den = x;
    }else{
        num = x;
        den = layer - x + 1;
    }
    
    std::cout << num << '/' << den <<'\n';

    return 0;
}

// 대각선으로 진행하는 분수의 총 개수는 layer가 바뀔 때마다 1씩 늘어남.
// 분모와 분자의 합은 layer+1임
// 분모 또는 분자의 최대값은 layer임.
// 분모가 1 증가하면 분자는 1감소함. 반대도 마찬가지.
// 홀수 layer는 분자>분모 상태에서 시작, 짝수는 분자<분모상태에서 시작
```