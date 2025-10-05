# step 2
- [10871 번](https://www.acmicpc.net/problem/10871)
## 난이도
- 브론즈 5
## 핵심
- 1차원 배열 구현

## 풀이
```c++
#include <iostream>

int main(){
    int n, x;
    std::cin >> n >> x;

    int arr[10001];
    for(int i = 0; i < n; i++){
        std::cin >> arr[i];
    }
        
    for (int j = 0; j < n; j++){
        if(arr[j] < x)   std::cout << arr[j] << " ";
    }
    
    return 0;
}
// 1 <= n, x <= 10,000
// 배열 길이 미리 선언
// 배열의 요소를 미리 입력받은 개수만큼 탐색하며 비교

#include <iostream>
#include <vector>

int main(){
    int n, x;
    std::cin >> n >> x;

    std::vector<int> arr(n);
    for(int i = 0; i < n; i++){
        std::cin >> arr[i];
    }
        
    for (int e : arr){
        if(e < x) std::cout << e << " ";
    }    
    
    return 0;
}
// 가변적인 배열 길이를 사용하여 풀이
```