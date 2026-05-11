# step 8
- [3052 번](https://www.acmicpc.net/problem/3052)
## 난이도
- 브론즈 2
## 핵심
- 1차원 배열, 배열 요소 비교, 나머지 셈 구현

## 풀이
```c++
#include <iostream>

int main(){
    int count = 0;
    bool seen[42] = {false};
    
    for(int i = 0; i < 10; i++){
        int n; 
        std::cin >> n;
        if(seen[n%42] == false){
            seen[n%42] = true;
            count++;
        }
    }
    std::cout << count << "\n";
    return 0;
}
// 0 <= n <= 1000
// 입력횟수 10 고정
// 크기 42의 배열을 선언하여 풀이.
```