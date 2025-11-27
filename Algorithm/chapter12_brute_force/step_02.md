# step 2
- [2231 번](https://www.acmicpc.net/problem/2231)

## 난이도
- 브론즈 2

## 핵심
- N의 생성자를 구하는 모든 경우 구하기

## 풀이
```c++
#include <iostream>


int numDigits(int n){
    int a = 0;
    while(true){
        ++a;
        n /= 10;
        if(n == 0)   break;
    }

    return a;
}

int digit_sum(int n){
    int sum = 0;
    while(n > 0){
        sum += (n % 10);
        n /= 10;
    }
    return sum;
}

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int N;
    std::cin >> N;
    int M = 0;
    int a = numDigits(N);
    int begin = N - (9 * a) < 1 ? 1 : N - (9 * a);
    int end = N + (9 * a);

    for(int i = begin; i <= end; ++i){
        if(i + digit_sum(i) == N)   {
            M = i;
            break;
        }
    }
    
    std::cout << M << '\n';
    return 0;
}


// 생성자의 범위는
// N - (N의 자릿수 * 9) <= M <= N + (N의 자릿수 * 9)
// N - (N의 자릿수 * 9)가 음수가 된다면 1로 보정
// 위 범위에서 탐색하여 가장 작은 생성자 찾기
// 만약 없다면 0 출력
```