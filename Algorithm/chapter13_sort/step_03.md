# step 2
- [25305 번](https://www.acmicpc.net/problem/25305)

## 난이도
- 브론즈 2

## 핵심
- k번째로 큰 수 구하기

## 풀이
```c++
#include <iostream>
#include <vector>
#include <algorithm>

void insertion_sort(std::vector<int>& arr);
void bubble_sort(std::vector<int>& arr);
void selection_sort(std::vector<int>& arr);

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);

    int N, k;
    std::cin >> N >> k;
    std::vector<int> arr(N);
    for(int i = 0; i < N; ++i)  std::cin >> arr[i];
        
    // insertion_sort(arr);
    // bubble_sort(arr);
    // selection_sort(arr);

    std::cout << arr[k-1] << '\n';
    return 0;
}

void insertion_sort(std::vector<int>& arr){
    int length = arr.size();

    for(int i = 1; i < length; ++i){
        int key = arr[i];
        int j = i - 1;

        while(j >= 0 && arr[j] < key){
            arr[j+1] = arr[j];
            --j;
        }
        arr[j+1] = key;
    }    
}

void bubble_sort(std::vector<int>& arr){
    int length = arr.size();

    for(int i = 0; i < length-1; ++i){
        for(int j = 0; j < length-i-1; ++j){
            if(arr[j] > arr[j+1]){
                int temp = arr[j];
                arr[j] = arr[j+1];
                arr[j+1] = temp;
            }
        }
    }
}

void selection_sort(std::vector<int>& arr){
    int length = arr.size();

    for(int i = 0; i < length-1; ++i){
        int maxIdx = i;
        for(int j = i+1; j < length; ++j){
            if(arr[j] > arr[maxIdx]){
                maxIdx = j;
            }
        }
        std::swap(arr[i], arr[maxIdx]);
    }
}
// 
```