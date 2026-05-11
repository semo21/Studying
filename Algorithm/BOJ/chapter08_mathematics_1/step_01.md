# step 1
- [2745 번](https://www.acmicpc.net/problem/2745)
## 난이도
- 브론즈 2
## 핵심
- 진법 변환

## 풀이
```c++
#include <iostream>
#include <string>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);

    std::string s;
    int b;
    std::cin >> s >> b;    
    long result = 0;
    for(char c : s){
        int v;
        if ('0' <= c && c <= '9'){
            v = c - '0';
        }else{
            v = c - 'A' + 10;
        }
        result = result * b + v;
    }

    std::cout << result << '\n';
    return 0;
}

// 핵심은 result에 반복문을 통한 해당 자리의 진법변환을 할 때마다 b만큼 곱해주는 것.
// 235(10진법) = 2*(10^2) + 3*(10^1) + 5*(10^0)
// 221(3진법) = 2*(3^2) + 2*(3^1) + 1*(3^0)
// 따라서 앞자리부터 계산하므로 b만큼 곱해주면 자연스럽게 자리에 맞게 곱해짐.
// 그리고 result는 시작할 때 0이므로 제일 처음의 result*b는 자연스레 0이 됨.
// 이후 연산부터 result*(b^n)으로 계산됨. 따라서 자연스럽게 마지막 자리는 v가 된다.
```