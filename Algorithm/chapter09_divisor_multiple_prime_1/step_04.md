# step 4
- [1978 번](https://www.acmicpc.net/problem/1978)
## 난이도
- 브론즈 2
## 핵심
- 소수 탐색 구현

## 풀이
```c++
#include <iostream>
#include <vector>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int n;    
    std::cin >> n;
    std::vector<int> nums(n);
    for(int i = 0; i < n; i++){
        std::cin >> nums[i];
    }

    int result = 0;
    for(int e : nums){
        if(e == 1)  continue;

        bool bIsPrime = true;
        int i = 2;
        while(bIsPrime){
            if(e % i == 0 && e != i){
                bIsPrime = false;
            }    
            else if(e % i == 0 && e == i){
                result++;
                break;
            }
            else{
                i++;
            }    
        }
    }
    
    std::cout << result << '\n';
    
    return 0;
}

// 초기 풀이
// 입력받은 수보다 작은 수를 모두 탐색하며 bool상태를 이용한 소수확인
```

```c++
#include <iostream>
#include <vector>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int n;    
    std::cin >> n;
    std::vector<int> nums(n);
    for(int i = 0; i < n; i++)  std::cin >> nums[i];
    
    int result = 0;
    for(int x : nums){
        if(x < 2)   continue;

        bool bPrime = true;
        for(int d = 2; d * d <= x; d++){
            if(x % d == 0)  { bPrime = false; break; }
        }
        if(bPrime)  result++;
    }    
    
    std::cout << result << '\n';
    
    return 0;
}

// 개선된 풀이
// 약수의 존재는 주어진 수 x의 제곱근보다 커지면 진약수(x의 진약수 = x)를 제외하면 없음
// 따라서 약수의 존재 탐색을 x의 제곱근까지만 탐색
// 탐색과정에서 약수가 존재한다면 bPrime을 false로 변환하여 탐색 중지 후 다음 수로 넘어감
```
