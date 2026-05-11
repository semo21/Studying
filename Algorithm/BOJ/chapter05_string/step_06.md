# step 6
- [10809 번](https://www.acmicpc.net/problem/10809)
## 난이도
- 브론즈 2
## 핵심
- 문자열 구현

## 풀이
```c++
#include <iostream>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);

    std::string input;
    std::cin >> input;
    int arr[26] = {0};
    for(int& e : arr){
        e = -1;
    }
    
    for(int i = 0; i < input.length(); i++){
        char l = input[i];
        if(arr[l-'a'] == -1){
            arr[l-'a'] = i;
        }        
    }
    
    for(int e : arr){
        std::cout << e << " ";
    }
    std::cout << "\n";
    return 0;
}

// 알파벳의 인덱스를 저장할 arr생성.
// arr의 요소를 포인터를 사용하여 -1로 모두 초기화
// 반복문 실행하며 문자열의 요소별로 분기 실행
// a의 인덱스는 0, z의 인덱스는 25이므로 해당 알파벳의 최초 인덱스를 저장
// 중복 실행된 수는 arr의 요소값이 -1이 아님
// 따라서 이미 초기화 되었다면 실행하지 않음
```