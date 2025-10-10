# step 8
- [10811 번](https://www.acmicpc.net/problem/10811)
## 난이도
- 브론즈 2
## 핵심
- 1차원 배열, 배열 요소 교환 구현

## 풀이
```c++
#include <iostream>
#include <vector>
#include <numeric>

int main(){
    int n, m;
    std::cin >> n >> m;
    
    std::vector<int> arr(n);
    std::iota(arr.begin(), arr.end(), 1);
    for(int i = 0; i < m; i++){
        int a, b;
        std::cin >> a >> b;

        for(int j = 0; j < (b-a+1)/2; j++){
            int temp = arr[a-1+j];
            arr[a-1+j] = arr[b-1-j];
            arr[b-1-j] = temp;            
        }
    }
    
    for(int e : arr){
        std::cout << e << " ";
    }

    return 0;
}

// 1 <= n, m <= 100
// 가변배열 vector사용
// 배열 요소 초기화에 iota함수 사용.

#include <iostream>
#include <vector>   // vector
#include <numeric>  // iota
#include <algorithm>    // reverse

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);

    int n, m;
    std::cin >> n >> m;

    std::vector<int> arr(n);
    std::iota(arr.begin(), arr.end(), 1);

    while(m--){
        int a, b;
        std::cin >> a >> b;
        std::reverse(arr.begin() + (a-1), arr.begin() + b);
    }
    
    for(int e : arr){
        std::cout << e << " ";
    }

    return 0;
}

// 가독성이 더 좋은 방식
// vector, iota, reverse 사용.
```