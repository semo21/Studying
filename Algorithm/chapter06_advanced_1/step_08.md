# step 8
- [25206 번](https://www.acmicpc.net/problem/25206)
## 난이도
- 실버 5
## 핵심
- 문자열 구분에 따른 분기 설정, 사칙연산, 반복문 구현

## 풀이
```c++
#include <iostream>
#include <string>
#include <sstream>

int main(){
    std::ios::sync_with_stdio(false);
    std::cin.tie(nullptr);

    
    double total = 0;
    int n = 20;
    double avg = 0;
    double mAvg = 0;

    for(int i = 0; i < 20; i++){
        std::string line;
        std::getline(std::cin, line);

        std::stringstream ss(line);

        std::string subject;
        double credit;
        std::string grade;

        double mul = 0;

        ss >> subject >> credit >> grade;

        if(grade == "P")    continue;
       
        total += credit;

        if(grade == "A+")   mul = 4.5;
        else if(grade == "A0")  mul = 4.0;
        else if(grade == "B+")  mul = 3.5;
        else if(grade == "B0")  mul = 3.0;
        else if(grade == "C+")  mul = 2.5;
        else if(grade == "C0")  mul = 2.0;
        else if(grade == "D+")  mul = 1.5;
        else if(grade == "D0")  mul = 1.0;
        else if(grade == "F")   mul = 0;

        mAvg += credit * mul;
        
    }
    

    std::cout << mAvg / total<< '\n';
    return 0;
}

// 전공평점 = (학점 * 과목평점) / 학점의 총합
// 학점은 주어지지만, 과목평점의 분기는 직접 나눠야함
// P에 대한 건너뛰는 분기 설정
// 한 줄에 제공되는 공백문자 구분은 stringstream을 이용하여 해결
```