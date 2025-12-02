# step 1
- [2750 번](https://www.acmicpc.net/problem/2750)

## 난이도
- 브론즈 2

## 핵심
- 정렬 알고리즘 구현

## 풀이
```c++
#include <iostream>
#include <vector>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int N;
    std::cin >> N;
    std::vector<int> arr(N);
    for(int i = 0; i < N; ++i)  std::cin >> arr[i];

    for(int i = 0; i < N-1; ++i){
        for(int j = 0; j < N-1-i; ++j){
            if(arr[j] > arr[j+1]){
                int temp = arr[j];
                arr[j] = arr[j+1];
                arr[j+1] = temp;
            }
        }
    }
    for(int e : arr){
        std::cout << e << '\n';
    }
    return 0;
}
// 버블 정렬

#include <iostream>
#include <vector>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);

    int N;
    std::cin >> N;
    std::vector<int> arr(N);
    for(int i = 0; i < N; ++i)  std::cin >> arr[i];

    for(int i = 1; i < N; ++i){
        int key = arr[i];
        int j = i - 1;

        while(j >= 0 && (arr[j] > key)){
            arr[j+1] = arr[j];
            --j;
        }
        arr[j+1] = key;
    }
    
    for(int e : arr){
        std::cout << e << '\n';
    }
    return 0;
}
// 삽입 정렬
```