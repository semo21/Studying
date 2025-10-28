# step 2
- [2566 번](https://www.acmicpc.net/problem/2566)
## 난이도
- 브론즈 3 
## 핵심
- 2차원 배열 최댓값 탐색, 인덱스 탐색 구현

## 풀이
```c++
#include <iostream>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);

    int arr[9][9];
    int max = -1;
    int rowIdx = 0; 
    int colIdx = 0;

    for(int i = 0; i < 9; i++){
        for(int j = 0; j < 9; j++){
            std::cin >> arr[i][j];
            if(arr[i][j] > max){
                max = arr[i][j];
                rowIdx = i+1;
                colIdx = j+1;
            }
        }
    }

    std::cout << max << '\n' << rowIdx << ' ' << colIdx << '\n';

    return 0;
}

// 인덱스도 구해야하므로 range-based로 작성
```