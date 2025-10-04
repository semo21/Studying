# step 1
- [10807 번](https://www.acmicpc.net/problem/10807)
## 난이도
- 브론즈 5
## 핵심
- 1차원 배열 구현

## 풀이
```c++
#include <iostream>

int main(){
    int n, v;
    std::cin >> n;

    int arr[101];
    for(int i = 0; i < n; i++){
        std::cin >> arr[i];
    }

    std::cin >> v;
    int count = 0;
    for(int j = 0; j < n; j++){
        if(arr[j] == v){
            count++;
        }
    }

    std::cout << count << "\n";

    return 0;
}
// 1 <= n <= 100;
// 배열의 최대길이를 미리 선언
// c++배열에서의 nullpt자리를 계산하여 n의 범위 +1하여 설정.
// 입력받은 값을 앞서 입력받은 정수의 개수만큼 탐색.
// 같다면 count 1씩 증가.
#include <iostream>
#include <vector>

int main(){
    int n, v;
    std::cin >> n;

    std::vector<int> arr(n);
    for(int i = 0; i < n; i++){
        std::cin >> arr[i];
    }

    std::cin >> v;

    int count = 0;
    for(int e : arr){
        if(e == v)  count++;
    }

    std::cout << count << "\n";
    return 0;
}
// vector의 가변 크기 배열을 이용한 풀이.
// 배열 길이 선언부만 다름.
```