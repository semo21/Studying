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

    int n;
    std::cin >> n;

    int count = 0;

    while(n--){
        std::string s;
        std::cin >> s;
        
        bool arr[26] = {false};
        char prev = 0;
        bool bIsOk = true;
        
        for(char c : s){
            if(c != prev){
                if(arr[c - 'a']){
                    bIsOk = false;
                    break;
                }
                arr[c - 'a'] = true;
                prev = c;
            }
        }

        if(bIsOk)   count++;
    }

    std::cout << count << '\n';
    return 0;
}

// bool과 prev 변수를 사용하여 상태를 판단.
// 포인트는 이전 단어와 다른 글자인데 arr에선 이미 true인 경우를 찾아내는 것.
```