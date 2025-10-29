# step 3
- [10798 번](https://www.acmicpc.net/problem/10798)
## 난이도
- 브론즈 1
## 핵심
- 2차원 배열 길이 구분 분기 구현

## 풀이
```c++
#include <iostream>
#include <vector>
#include <string>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);

    std::vector<std::string> row(5);
    
    for(size_t i = 0; i < 5; i++){
        std::cin >> row[i];
    }

    for(size_t c = 0; c < 15; c++){
        for(size_t r = 0; r < 5; r++){
            if(c < row[r].size()){
                std::cout << row[r][c];
            }
        }
    }

    return 0;
}

// 가변 배열 vector로 풀이
// 입력 string으로 주어지므로 string타입으로 설정
// 요소배열마다 길이가 다를 수도 있으므로 배열의 길이를 넘는 인덱스는 무시
```