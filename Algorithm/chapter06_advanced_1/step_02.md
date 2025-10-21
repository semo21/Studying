# step 2
- [3003 번](https://www.acmicpc.net/problem/3003)
## 난이도
- 브론즈 5
## 핵심
- 입력된 배열 요소 비교 구현

## 풀이
```c++
#include <iostream>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);

    int a;
    int arr[6] = {1, 1, 2, 2, 2, 8};
    for(int i = 0; i < 6; i ++){
        std::cin >> a;
        std::cout << arr[i] - a << " ";
    }

    return 0;
}

// 필요한 갯수를 배열로 만들어둔 뒤 직접 비교하며 출력

#include <iostream>
#include <array>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);

    constexpr std::array<int, 6> need{1, 1, 2, 2, 2, 8};
    std::array<int, 6> cur{};
    for (int& x : cur) std::cin >> x;

    for (size_t i = 0; i < need.size(); i++){
        if(i) std::cout << ' ';
        std::cout << (need[i] - cur[i]);
    }
    std::cout << '\n';

    return 0;
}
// STL식 문제풀이
// 요소의 값을 constexpr선언으로 고정
// 0 이후 공백이 출력되게 if(i) 조건 사용
```