# step 6
- [1427 번](https://www.acmicpc.net/problem/1427)

## 난이도
- 실버 5

## 핵심
- 주어진 수 정렬

## 풀이
```c++
#include <iostream>
#include <string>
#include <vector>
#include <algorithm>

void merge_sort(std::vector<int>& arr, int left, int right);
void merge(std::vector<int>& arr, int left, int mid, int right);
void bubble_sort(std::vector<int>& arr);
void insertion_sort(std::vector<int>& arr);
void selection_sort(std::vector<int>& arr);

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);

    std::string N;
    std::cin >> N;

    std::vector<int> arr(N.size());
    for(size_t i = 0; i < N.size(); ++i){
        arr[i] = N[i] - '0';
    }
    
    merge_sort(arr, 0, N.size() - 1);
    bubble_sort(arr);
    insertion_sort(arr);
    selection_sort(arr);

    for(int i : arr){
        std::cout << i;
    }
    return 0;
}

void merge_sort(std::vector<int>& arr, int left, int right){
    if(left >= right)   return;

    int mid = (left + right) / 2;

    merge_sort(arr, left, mid);
    merge_sort(arr, mid + 1, right);
    merge(arr, left, mid, right);
}

void merge(std::vector<int>& arr, int left, int mid, int right){
    std::vector<int> temp;

    int i = left;
    int j = mid + 1;
    while(i <= mid && j <= right){
        if(arr[i] >= arr[j]){
            temp.push_back(arr[i++]);
        }else{
            temp.push_back(arr[j++]);
        }
    }

    while(i <= mid) temp.push_back(arr[i++]);
    while(j <= right)   temp.push_back(arr[j++]);

    for(size_t k = 0; k < temp.size(); ++k){
        arr[left + k] = temp[k];
    }
}

void bubble_sort(std::vector<int>& arr){
    int length = arr.size();

    for(int i = 0; i < length-1; ++i){
        for(int j = 0; j < length-1-i; ++j){
            if(arr[j] < arr[j+1]){
                int temp = arr[j+1];
                arr[j+1] = arr[j];
                arr[j] = temp;
            }
        }
    }
}

void insertion_sort(std::vector<int>& arr){
    int length = arr.size();

    for(int i = 0; i < length; ++i){
        int key = arr[i];
        int j = i - 1;
        
        while(j >= 0 && arr[j] < key){
            arr[j+1] = arr[j];
            --j;
        }
        arr[j+1] = key;
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
// 받은 수를 string으로 저장
// 정렬이 가능하도록 int 배열로 치환
// 치환 과정에서 ascii값으로 나오지 않도록 '0'을 뺄셈
// 병합, 버블, 삽입, 선택 정렬로 풀이.
```