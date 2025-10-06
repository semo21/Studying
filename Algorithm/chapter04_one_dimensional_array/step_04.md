# step 4
- [2562 번](https://www.acmicpc.net/problem/2562)
## 난이도
- 브론즈 3
## 핵심
- 1차원 배열, 배열 최대값 탐색 구현

## 풀이
```c++
#include <iostream>

int main(){
    int max, idx;
    int arr[101];

    for(int i = 0; i < 9; i++){
        std::cin >> arr[i];
    }

    max = arr[0];
    idx = 1;
    for(int j = 1; j < 9; j++){
        if(arr[j] > max){
            max = arr[j];
            idx = j+1;
        }
    }   
    std::cout << max << "\n" << idx << "\n";
    
    return 0;
}
// 1 <= n <= 100
// 배열의 길이는 9로 고정
// 요소를 배열에 저장
// 이후 각 요소 최대, 위치 비교 탐색

#include <iostream>

int main(){
    int a, max, idx;

    for(int i = 0; i < 9; i++){
        std::cin >> a;
        if(i == 0){
            max = a;
            idx = i+1;
        }
        else{
            if(a > max){
                max = a;
                idx = i+1;
            }
        }        
    }

    std::cout << max << "\n" << idx << "\n";
    
    return 0;
}
// 배열 생성 없이 바로 비교하는 방법
```