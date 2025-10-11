# step 10
- [1546 번](https://www.acmicpc.net/problem/1546)
## 난이도
- 브론즈 1
## 핵심
- 1차원 배열, 배열 요소 비교, 나머지 셈 구현

## 풀이
```c++
#include <iostream>
#include <iomanip>

int main(){
    int n;
    double m, sum, max, result;
    sum = 0;
    std::cin >> n;
    for (int i = 0; i < n; i++){
        std::cin >> m;
        if (i == 0){
            max = m;

        }else{
            if(m > max){
                max = m;
            }
        }
        sum += m;
    }
    result = sum * 100 / max / n;

    std::cout << std::setprecision(3) << result << "\n";

    return 0;
}

// 0 <= n <= 1,000
// 0 <= m <= 100
// 배열을 이용하지 않음
// 입력받는 즉시 점수의 총합에 저장
// 점수의 총합을 과목수만큼 나누고, 이것을 다시 보정식으로 계산

#include <iostream>
#include <iomanip>

int main(){
    int n;
    std::cin >> n;

    double x;
    std::cin >> x;
    double sum = x, max = x;
    
    for(int i = 0; i < n; i++){
        std::cin >> x;
        sum += x;
        if(x > max) max = x;
    }

    double result = (max == 0.0) ? 0.0 : (sum * 100.0) / max / n;
    std::cout << std::setprecision(3) << result << "\n";

    return 0;
}
// 기존 식을 개선시킨 코드.
// 동작 방식은 같음.
```