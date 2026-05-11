# step 2
- [11005 번](https://www.acmicpc.net/problem/11005)
## 난이도
- 브론즈 1
## 핵심
- 진법 변환

## 풀이
```c++
#include <iostream>
#include <string>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);
   
    long long n;
    int b;
    std::string result;

    std::cin >> n >> b;

    while(n > 0){
        int rem = n % b;
        char c;
        if(rem > 9){
            c = 'A' + rem - 10;
        }else{
            c = '0' + rem;
        }
        result = c + result;
        n /= b;
    }

    std::cout << result << '\n';
    return 0;
}

// 1 <= n <= 1,000,000,000
// 2 <= b <= 36
// b진법이라면 b로 나눈 나머지를 저장해야함
// string으로 출력해야하므로 숫자여도 char형태로 변환
// result에 저장할 때 역순을 방지하기 위해 c + result로 구현
```