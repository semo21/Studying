# step 6
- [2941 번](https://www.acmicpc.net/problem/2941)
## 난이도
- 실버 5
## 핵심
- 반복문을 통한 문자열 요소 검증

## 풀이
```c++
#include <iostream>
#include <string>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);

    std::string s;
    std::cin >> s;
    int count = 0;
    
    int i = (int)s.length()-1;
    while(i >= 0){
        if(i >= 2 && s[i] == '=' && s[i-1] == 'z' && s[i-2] == 'd'){
            count++;
            i-=3;
        }else if(i >= 1 && s[i] == 'j'){
            count++;
            if(s[i-1] == 'n' || s[i-1] == 'l'){
                i-=2;
            }  
            else{
                i--;
            }    
        }else if(i >= 1){
            if(s[i] == '-' || s[i] == '='){
                i-=2;
            }else{
                i--;
            }
            count++;
        }else{
            count++;
            i--;
        }
    }

    std::cout << count << '\n';
    return 0;
}

// -, =가 포함되면 무조건 크로아티아 알파벳.
// 조건이 복잡한 것부터 먼저 처리.
// 분기를 잘 나누어야 함. 
```