# step 2
- [2587 번](https://www.acmicpc.net/problem/2587)

## 난이도
- 브론즈 2

## 핵심
- 5개 수의 평균과 중앙값 구하기

## 풀이
```c++
#include <iostream>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int sum = 0;
    int arr[5];
    for(int i = 0; i < 5; ++i)  {
        std::cin >> arr[i];
        sum += arr[i];
    }
    int avg = sum / 5;

    for(int i = 1; i < 5; ++i){
        int key = arr[i];
        int j = i - 1;
        
        while(j >= 0 && (arr[j] > key)){
            arr[j+1] = arr[j];
            --j;
        }
        arr[j+1] = key;
    }

    std::cout << avg << '\n' << arr[2] << '\n';
    return 0;
}
// 삽입 정렬 풀이
```