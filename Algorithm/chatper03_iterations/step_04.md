# step 4
- [25304번](https://www.acmicpc.net/problem/25304)
## 난이도
- 브론즈 4
## 핵심
- 반복문, 덧셈, 입출력, 조건문 구현

## 풀이
```c++
#include <iostream>

int main(){
    int x, n;
    std::cin >> x >> n;

    int total = 0;
    std::string answer = "No";
    for(int i = 0; i < n; i++){
        int a, b;
        std::cin >> a >> b;

        total += (a * b);
    }

    if(total == x){
        answer = "Yes";
    }

    std::cout << answer << std::endl;

    return 0;
}

// 1 <= x <= 1,000,000,000
// 1 <= n <= 100
// 1 <= a <= 1,000,000
// 1 <= b <= 10
// 품목 n회만큼 반복하는 반복문을 구현
// 각 항목의 총 금액인 가격 * 갯수를 total에 더하고 저장
// total과 x를 비교
// 응답의 기본값은 No.
// total과 x가 다르다면 조건문을 거치지 않으므로 No출력
// 맞다면 응답을 Yes로 수정.
```