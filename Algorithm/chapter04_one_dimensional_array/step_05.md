# step 5
- [10810 번](https://www.acmicpc.net/problem/10810)
## 난이도
- 브론즈 3
## 핵심
- 1차원 배열, 배열 요소 삽입/변경 구현

## 풀이
```c++
#include <iostream>
#include <vector>

int main(){
    int n, m;
    int a, b, c;
    std::cin >> n >> m;

    std::vector<int> arr(n);
    for(int i = 0; i < m; i++){
        std::cin >> a >> b >> c;
            
        for(int j = a-1; j < b-1; j++){
            arr[j] = c;
        }
    }

    for(int e : arr){
        std::cout << e << " ";
    }
    std::cout << "\n";
    return 0;
}
// 1 <= n, m <= 100
// 주머니의 크기(배열크기)는 n
// a부터 b까지의 주머니에 c를 넣기
// 이 과정을 m회 반복
```