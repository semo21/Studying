# step 3
- [10818 번](https://www.acmicpc.net/problem/10818)
## 난이도
- 브론즈 3
## 핵심
- 1차원 배열, 배열 최대/최소 탐색 구현

## 풀이
```c++
#include <iostream>

int main(){
    int n;
    int arr[1000001];
    std::cin >> n;
    
    
    for(int i = 0; i < n; i++){
        std::cin >> arr[i];        
    }
    int max = arr[0]; int min = arr[0];
    
    for(int i = 1; i < n; i++){
        if(arr[i] > max)    max = arr[i];
        if(arr[i] < min)    min = arr[i];
    }
    
    
    std::cout << min << " " << max;
    return 0;
}
// 1 <= n <= 1,000,000
// 배열의 길이를 미리 선언.
// min, max를 배열 첫 요소로 초기화
// 이후 배열을 순환하며 비교 실행

#include <iostream>
#include <vector>

int main(){
    int n;    
    std::cin >> n;
    std::vector<int> arr(n);    
    for(int i = 0; i < n; i++){
        std::cin >> arr[i];        
    }
    int max = arr[0]; int min = arr[0];
    
    for(int i = 1; i < n; i++){
        if(arr[i] > max)    max = arr[i];
        if(arr[i] < min)    min = arr[i];
    }    
    
    std::cout << min << " " << max;
    return 0;
}
// vector를 사용한 배열 풀이
// 배열 선언/ 길이 할당 부분만 다름

#include <iostream>

int main(){
    int n, a;    
    int min, max;
    
    std::cin >> n;

    for(int i = 0; i < n; i++){
        if(i == 0){
            
            std::cin >> a;
            min = a;
            max = a;
        }
        else{
            std::cin >> a;
            if(a > max) max = a;
            if(a < min) min = a;
        }
    } 
    
    std::cout << min << " " << max;
    return 0;
}
// 배열을 이용하지 않는 풀이
// 입력받을 때마다 최대/최소를 비교함
```