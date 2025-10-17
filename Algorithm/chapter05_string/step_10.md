# step 9
- [5622 번](https://www.acmicpc.net/problem/5622)
## 난이도
- 브론즈 2
## 핵심
- 문자열 구현

## 풀이
```c++
#include <iostream>
#include <string>

int main(){
    std::string input;
    std::cin >> input;
    int result = 0;
    for(char e : input){
        if((e-'A') >=16 && (e-'A') <= 19){
            result += 7 + 3;
        }else if((e-'A') >= 23){
            result += 9 + 3;
        }else{
            result += (e-'A')/3 + 3;
        }
    }

    std::cout << result << '\n';
    return 0;
}

// 
```