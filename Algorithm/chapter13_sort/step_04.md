# step 4
- [25305 번](https://www.acmicpc.net/problem/25305)

## 난이도
- 실버 5

## 핵심
- k번째로 큰 수 구하기

## 풀이
```c++
#include <iostream>
#include <vector>
#include <algorithm>

void merge_sort(std::vector<int>& arr, int left, int right);
void merge(std::vector<int>& arr, int left, int mid, int right);

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);

    int N;
    std::cin >> N;
    std::vector<int> arr(N);
    
    for(int i = 0; i < N; ++i)  
        std::cin >> arr[i];
    
    merge_sort(arr, 0, N-1);

    
    for(int e : arr)    
        std::cout << e << '\n';

    return 0;
}

void merge_sort(std::vector<int>& arr, int left, int right){
    if(left >= right)   return;

    int mid = (left + right) / 2;

    merge_sort(arr, left, mid);
    merge_sort(arr, mid+1, right);
    merge(arr, left, mid, right);
}

void merge(std::vector<int>& arr, int left, int mid, int right){
    std::vector<int> temp;

    int i = left;
    int j = mid + 1;
    while(i <= mid && j <= right){
        if(arr[i] <= arr[j]){
            temp.push_back(arr[i++]);
        }else{
            temp.push_back(arr[j++]);
        }
    }

    while(i <= mid) temp.push_back(arr[i++]);
    while(j <= right) temp.push_back(arr[j++]);

    for(int k = 0; k < temp.size(); ++k){
        arr[left + k] = temp[k];
    }
}
// O(n²)의 정렬은 시간초과로 실패
// 따라서 시간이 적게 걸리는 O(n log n)의 병합 정렬이 적합.
```