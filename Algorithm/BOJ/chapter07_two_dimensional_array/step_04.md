# step 4
- [2563 번](https://www.acmicpc.net/problem/2563)
## 난이도
- 실버 5
## 핵심
- 2차원 배열을 이용한 도형 넓이 구현

## 풀이
```c++
#include <iostream>
#include <vector>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);

    std::vector<std::vector<int>> matrix(100, std::vector<int>(100, 0));
    int result = 0;

    int n;    
    std::cin >> n;    
    for(int i = 0; i < n; i++){
        int x, y;
        std:: cin >> x >> y;
        for(int j = x; j < x+10; j++){
            for(int k = y; k < y+10; k++){
                if(matrix[j][k] == 0){
                    matrix[j][k] = 1;
                    result++;
                }
            }
        }
    }

    std::cout << result << '\n';
    return 0;
}

// 100 * 100크기의 2차원 배열을 생성하고 모든 요소를 0으로 초기화
// 이후 10 * 10 크기의 색종이 위치로 주어진 곳을 1로 변경하며 result(총 넓이)++
// 만약 이미 matrix의 해당 위치가 이미 1이라면 겹치는 부분이므로 무시
```