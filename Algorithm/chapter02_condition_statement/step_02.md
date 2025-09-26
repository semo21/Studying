# step 2
- [9498번](https://www.acmicpc.net/problem/9498)
## 난이도
- 브론즈 5
## 핵심
- 조건별 다른 출력값 구현

## 풀이
```c++
#include <iostream>

int main(){
    int a;
    std::cin >> a;
    std::string grade = "";
    if(a >= 90){
        grade = "A";
    }else if(a >= 80){
        grade = "B";
    }else if(a >= 70){
        grade = "C";
    }else if(a >= 60){
        grade = "D";
    }else{
        grade = "F";
    }
    std::cout << grade << std::endl;
    return 0;
}

// 0 <= a <= 100
// 점수에 따른 등급 분류
// 분류에 맞는 조건 설정 후 Grade 변경
```