# step 1
- [2738 번](https://www.acmicpc.net/problem/2738)
## 난이도
- 브론즈 3 
## 핵심
- 2차원 배열 요소의 덧셈 구현

## 풀이
```c++
#include <iostream>
#include <vector>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);

    int n, m;
    std::cin >> n >> m;
    
    std::vector<std::vector<int>> A(n, std::vector<int>(m));

    for(int i = 0; i < n; i++){
        for(int j = 0; j < m; j++){
            int a;
            std::cin >> a;
            
            A[i][j] = a;
        }
    }

    for(int i = 0; i < n; i++){
        for(int j = 0; j < m; j++){
            int a;
            std::cin >> a;
            
            A[i][j] += a;
        }
    }

    for(std::vector<int> arr : A){
        for(int e : arr){
            std::cout << e << " ";
        }
        std::cout << '\n';
    }
    return 0;
}

// 가변하는 배열의 크기 구현을 위해 vector사용
// 2차원 배열 B의 요소들은 A의 모든 대응하는 요소에 덧셈
// 따라서 B를 만들지않고 입력받으며 A에 직접 덧셈을 수행
// 출력은 2차원 배열인만큼 중첩반복문을 통하여 실행
```