# step 3
- [9506 번](https://www.acmicpc.net/problem/9506)
## 난이도
- 브론즈 1
## 핵심
- 조금 더 효율적인 약수 찾기

## 풀이
```c++
#include <iostream>
#include <vector>
#include <algorithm>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
    
    int n;

    while((std::cin >> n) && !(n == -1)){
        std::vector<int> divs{1};
        int sum = 1;

        for(int i = 2; i * i <= n; i++){
            if(n % i == 0){
                int j = n / i;
                divs.push_back(i);
                sum += i;
                if(j != 1){
                    divs.push_back(j);
                    sum += j;
                }
            } 
        }

        std::sort(divs.begin(), divs.end());
        
        if(sum == n){
            std::cout << n << " = ";
            for(size_t i = 0; i < divs.size(); i++){
                if(i)   std::cout << " + ";
                std::cout << divs[i];
            }
            std::cout << '\n';
        }else{
            std::cout << n << " is NOT peerfect." << '\n';
        }
    }
    
    return 0;
}

// n은 약수의 조합임.
// 14= 1*14, 2*7, 7*2, 14*1 처럼 약수의 크기가 n의 제곱근을 넘어가면 이미 나왔던 조합이 반복됨.
// 따라서 첫 반복문에서 약수를 찾을 때, 찾아낸 약수와 n을 약수로 나눈 몫 또한 약수임.
// 그렇기에 첫 반복문의 범위를 i*i로 하여금 n의 제곱근보다 작은 범위에서 실행.
// 그리고 약수를 찾으면 그 몫 또한 저장.
// 다만 진약수(n의 진약수는 n)는 제외.
// 찾아낸 약수를 저장한 vector배열을 정렬하고 출력.
```