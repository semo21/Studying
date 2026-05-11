# step 7
- [5597 번](https://www.acmicpc.net/problem/5597)
## 난이도
- 브론즈 3
## 핵심
- 1차원 배열, 배열 탐색 구현

## 풀이
```c++
#include <iostream>

int main(){
    int arr[30] = {0};

    for(int i = 0; i < 28; i++){
        int n;
        std::cin >> n;
        arr[n-1] = 1;
    }

    for(int j = 0; j < 30; j++){
        if(arr[j] == 0) std::cout << j+1 << "\n";
    }
    return 0;
}
// 배열 길이 30 고정
// 제출한 학생 수 28 고정
```