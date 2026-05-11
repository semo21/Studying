# step 6
- [10813 번](https://www.acmicpc.net/problem/10813)
## 난이도
- 브론즈 2
## 핵심
- 1차원 배열, 배열 요소 교환 구현

## 풀이
```c++
#include <iostream>

int main(){
    int n, m;
    std::cin >> n >> m;
    int arr[101];
    
    for(int i = 0; i < n; i++){
        arr[i] = i+1;
    }

    for(int j = 0; j < m; j++){
        int a, b, temp;

        std::cin >> a >> b;
        temp = arr[a-1];
        arr[a-1] = arr[b-1];
        arr[b-1] = temp;        
    }

    for(int i = 0; i < n; i++){
        std::cout << arr[i] << " ";
    }
    std::cout << "\n";
    return 0;
}
// 1 <= n, m <= 100
```