# Chapter 1

- 컴퓨터가 유일하게 인식할 수 있는 언어는 [<span style="color: #44B444">기계어</span>]이다.
- 기계어는 단 두개의 기호인 0과 1을 사용한다. 이 기호를 [<span style="color: #44B444">비트</span>]라고 한다.
- [<span style="color: #44B444">패치</span>]는 천공 카드의 구멍을 덧대는 작업에서 유래되었으며 프로그램 수정 작업을 의미한다.
- 어셈블리어는 기계어에 일대일로 대응된다. 기계어를 사람이 알아보기 쉬운 [<span style="color: #44B444">연상 기호mnemonic</span>]을 사용해서 표현한다.
- C 언어는 1972년 [<span style="color: #44B444">데니스 리치</span>]에 의해 개발되었다.
- C와 C++의 포함관계에 대해서 설명하시오.
  - [<span style="color: #44B444">초기의 C++는 C 언어를 위한 상위 호환 언어였다. 즉, C++ 코드가 변환기를 통해서 C 언어로 변환된 뒤에 사용되는 식이었다. 따라서 최초에는 C 언어가 C++의 부분집합이었다. 그러나 C 언어 독자 표준이 확립됨과 동시에 C++도 자체적인 표준이 제정되면서 둘의 관계는 완전한 포함 관계에서 벗어나게 된다. 그러나 두 언어가 상호 영향을 주면서 사실상 C++가 C 언어를 포함하는 방향으로 변화하고 있다. 아직도 두 언어 사이에는 몇몇 차이점이 존재하지만 사실상 C++가 C 언어를 포함한다고 봐도 무방하다.</span>]
- [<span style="color: #44B444">컴파일러</span>]는 C++ 코드를 기계어로 번역하는 일을 담당한다.
- C++ 소스 파일이 컴파일되면 [<span style="color: #44B444">목적 파일</span>]이 생성된다.
- [<span style="color: #44B444">링커</span>]는 목적 파일과 라이브러리를 연결하여 실행 모듈(프로그램)을 만든다.
- 코드 편집, 컴파일, 링킹 등 프로그래밍에 필요한 모든 작업을 통합적으로 수행할 수 있는 도구를 [<span style="color: #44B444">통합개발환경(IDE)</span>]라고 한다.
- Visual Studio에서 [<span style="color: #44B444">프로젝트</span>]는 하나의 실행 모듈(exe, dll, so 등) 개발을 관리하는 단위이며, [<span style="color: #44B444">솔루션</span>]은 연관성이 있는 프로젝트를 모아서 관리하는 단위이다.
- 프로그램 코드가 기록되는 파일은 크게 두 가지 종류가 있으며 [<span style="color: #44B444">소스</span>] 파일과 [<span style="color: #44B444">헤더</span>] 파일이 있다.
- 헤더 파일을 소스 파일에 포함 및 참조시키는 명령은 [<span style="color: #44B444">#include</span>]이다.
- 표준 입출력에 관련된 내용이 기록되어 있으며 cout, endl 등을 참조하기 위하여 필요한 헤더 파일은 [<span style="color: #44B444">iostream</span>]이다.
- 컴파일러가 코드를 의미 있는 최소 단위로 자르는 작업을 구문 분석이라고 한다. 이때 코드의 의미 있는 최소 단위를 [<span style="color: #44B444">토큰</span>]이라 한다.
- 이미 예약되어 있어서 다른 용도로 사용할 수 없는 토큰을 [<span style="color: #44B444">키워드</span>]라고 한다.
- 올바르지 못한 식별자를 고르시오[<span style="color: #44B444">7up</span>]
  - Coke
  - 7up
  - Pocari
  - \_Fanta
- 문자열은 [<span style="color: #44B444">큰따옴표</span>]로 묶여 있는 문자의 모음을 의미한다.
- 연산자는 [<span style="color: #44B444">피연산자</span>]에 실행할 연산을 나타내는 기호이다.
- 작문에서 문장의 끝을 나타내는 경우 마침표(.)를 사용하지만 C++에서는 [<span style="color: #44B444">세미콜론</span>]을 사용한다.
- 하나의 값으로 도출되는 토큰의 모음을 [<span style="color: #44B444">식</span>]이라 한다.
- 다음 중 식이 아닌 것은? [<span style="color: #44B444">\_for</span>]
  - 3
  - 3 + 4
  - a = 4
  - \_for
- 식 x = 3 끝에 [<span style="color: #44B444">;</span>]을 붙이면 문이 된다.`~
- 표준 C++ main 형식은 다음과 같다. 빈 칸에 올바른 타입을 채우시오.

```
[<span style="color: #44B444">void</span>] main() {

}

[<span style="color: #44B444">void</span>] main([<span style="color: #44B444">int</span>] argc, [<span style="color: #44B444">char</span>] argv){

}
```

- main은 프로그램 코드 전체에 단 하나만 있어야 한다. 그 이유를 작성하시오.

```
>> 프로그램이 시작될 때 최초로 실행되는 함수인데, 여러개가 있다면, 프로그램 시작 시 어떤 main을 호출해야 할 지 알 수 없기 때문이다.
```

- 여러 줄의 주석은 [<span style="color: #44B444"> /* </span>]로 시작해서 [<span style="color: #44B444"> */ </span>]로 끝난다.
- 주석은 컴파일 과정에서 무시된다. 그럼에도 아래 코드가 제대로 컴파일되지 않는 이유는 무엇인가?

```
int main(){
  cout << "Hello World!" << endl;
  ret/* Comment */urn 0;
}

>> 주석은 컴파일링 과정에서 단일 공백 문자로 처리하므로 위의 ret/* 주석 */urn 0;은 컴파일러에게 ret urn 0;으로 인식된다.
```

- C++는 표준 입출력 스트림 객체인 [<span style="color: #44B444">cout</span>], [<span style="color: #44B444">cin</span>]을 사용하여 콘솔에 입출력할 수 있다.
- [<span style="color: #44B444">뽑아내기 (>>)</span>] 연산자는 cin과 함께 쓰이고, [<span style="color: #44B444">끼워넣기 (<<)</span>] 연산자는 cout과 함께 사용된다.

{1} 다음과 같이 출생 연도를 입력받아서 나이를 출력하는 프로그램을 작성하시오.

```
출생 연도를 입력하세요.
1977
2002 한일월드컵 당시 한국 나이는 26세입니다.

>>
#include <iostream>

using namespace std;

int main() {
	int bYear;
	cout << "Input your birth year.";
	cin >> bYear;
	cout << "I was " << 2002 - bYear + 1 << " year old at Korea-Japan World Cup in korean age";

	return 0;
}
```

{2} 다음과 같이 현재 실행되는 프로그램이 x86인지, x64인지를 출력하는 프로그램을 작성하시오(전처리기를 이용하여 미리 정의된 매크로 \_M_X64를 이용하시오).

```
이 프로그램은 x86 프로그램입니다.
이 프로그램은 x64 프로그램입니다.

>>
#include <iostream>

using namespace std;

void PrintSystem() {
#ifdef _M_X64
	cout << "This program is x64 Program." << endl;
#else
	cout << "This program is x86 Program." << endl;
#endif
}

int main() {
	PrintSystem();

	return 0;
}
```

# Chapter 2

- [<span style="color: #44B444">반도체</span>]는 조건에 따라서 도체 혹은 부도체가 된다. 컴퓨터는 전류가 흐르는 경우를 [<span style="color: #44B444">1</span>], 흐르지 않는 경우를 [<span style="color: #44B444">0</span>]으로 약속하여 처리한다.
- 특정한 집합에 포함된 대상을 일정한 대응 규칙에 의해서 비트열로 표현하는 체계를 [<span style="color: #44B444">타입Type</span>]이라고 한다.
- C/C++는 수와 문자를 쉽게 처리하기 위하여 기본 타입을 제공한다. 기본 타입을 다섯 개 이상 나열하시오.
  - <span style="color: #44B444">int</span>
  - <span style="color: #44B444">short</span>
  - <span style="color: #44B444">long</span>
  - <span style="color: #44B444">double</span>
  - <span style="color: #44B444">float</span>
- C++는 정수 타입을 [<span style="color: #44B444">부호</span>]의 존재 여부에 따라서 크게 두 가지로 나눈다.
- unsigned short는 2바이트를 사용한다. unsigned short가 표현할 수 있는 정수의 범위를 나타내어라.
  - <span style="color: #44B444">2^16 = 0~65535</span>
- 어떤 수를 2진법의 비트열로 나타냈을 때, 각 비트를 반전시킨 것을 [<span style="color: #44B444">보수</span>]라고 한다. 2의 보수는 1의 보수에 [<span style="color: #44B444">1</span>]을 더한 것이다.
- -8을 2의 보수법에 의해 1바이트 비트열로 나타내어라.
  - <span style="color: #44B444">1111 1000</span>
- 실수를 비트열로 나타내기 위하여 전기전자기술자협회(IEEE)가 정한 표준은 무엇인가?
- <span style="color: #44B444">IEEE754</span>
- -5.375를 2진법으로 나타내어라.
  - <span style="color: #44B444">1 10000001 01011000000000000000000</span>
- 바로 위 문제의 답을 정규화하여 부호, 지수, 유효 숫자를 말해보시오.
  - <span style="color: #44B444">부호: 1</span>
  - <span style="color: #44B444">지수: 10000001</span>
  - <span style="color: #44B444">유효 숫자: 01011000000000000000000</span>
- int와 float는 크기가 4바이트로 같지만 float의 표현 범위가 훨씬 넓다. 대신 int에 비하여 어떤 점이 단점이 될 수 있는지 말해보시오.
  - <span style="color: #44B444">표현할 수 있는 수의 범위는 훨씬 넓지만 수의 절댓값이 커질수록 int형에 비하여 오차값이 커진다.</span>
- 정수 타입을 부동소수점 타입으로 변환할 경우 주의점은 무엇인가?
  - <span style="color: #44B444">부동소수점 타입과 정수 타입은 절대 호환될 수 없다. 특히 큰 정수를 변환할 때, 부동소수점의 오차로 인하여 잘못된 값을 저장하는 경우가 생기기 때문에 큰 정수를 계산할 땐 반드시 \_\_int64와 같은 정수형 타입을 사용하도록 한다.</span>
- C++는 알파벳, 숫자 및 기호들을 1바이트로 표현하는 char 타입과 유니코드 문자를 나타내는 [<span style="color: #44B444">문자 타입</span>] 타입을 제공한다.
- UTF-8과 UTF-16을 서로 비교하여 각각의 장단점을 말해보시오.
  - <span style="color: #44B444">UTF-8의 경우, 1바이트 문자는 아스키와 호환되며 알파벳을 1바이트로 표현할 수 있기 때문에 알파벳이 많이 사용되는 환경에서 사용한다면 메모리를 절약할 수 있다. 따라서 인터넷 통신에 많이 사용된다. 반면 UTF-16의 경우, 한 글자가 2바이트이므로 길이를 구하거나 검색 및 변환할 때 성능이 좋다.</span>
- Escape Sequence 중 연결이 잘못된 것을 고르시오.[<span style="color: #44B444">/b - Bell</span>]
  - /b - Bell
  - /t - Tab
  - /n - Line Feed
  - /r - Carriage Return
- NULL 종료 문자열을 설명하시오.
  - <span style="color: #44B444">문자 배열의 끝에 문자열의 끝을 표기하기 위하여 NULL을 기록하기위해 사용하는 문자열</span>
- 다음 코드에서 잘못된 부분을 찾아내고 이유를 설명하시오.
  ```
  void main()
  {
    char str1[8] = "C++";
    char str2[] = "C++";
    char str3[8];
    str3 = "C++";
  }
  ```
  > <span style="color: #44B444"> 배열은 오직 정의되는 순간에만 초기화(대입)할 수 있기 때문에 str3에게 값을 할당하는 코드 str3 = "C++"; 구문은 오류가 발생한다. str1[8] = "C++";가 가능한 이유는 str1의 0인덱스에 "C", 1인덱스와 2인덱스에 "+"가 할당되고, 이후에는 NULL문자열이 할당되어 종료되기 때문이다. str2[] = "C++";의 경우는 배열의 길이가 설정되지않은 상태에서 할당되는 값에 따라 자동으로 길이가 설정된다. 이 "C++"이 할당되었으므로 char 배열 4칸이 생성되어 C, +, +, NULL이 할당된다.</span>
- int 요소가 네 개인 배열이 3개 모인 타입을 파생하시오.
  - <span style="color: #44B444">객체를 선언할 땐 Type [NP(Name Place)] 형식으로 선언한다. 배열을 선언할 땐 Type [NP][n] 형식으로 선언한다. 여기서 n은 배열이 갖는 요소의 총 수를 의미한다. 따라서 Type [NP][3]이라면 [NP]에 지정된 이름을 가진 객체는 요소를 3개를 갖는 배열이 된다. 이름자리 바로 뒤에 해당 배열이 갖는 요소의 수를 쓰는 것이 작성 규칙이다. 따라서 2차원 이상의 배열을 생성할 때를 순차적으로 접근하여 살펴본다면 다음과 같다. </span>
    1. <span style="color: #44B444">Type [NP][n] => [NP]는 [n]개의 요소를 갖는 배열이다.</span>
    2. <span style="color: #44B444">Type [n] => [NP]는 생략된다.</span>
    3. <span style="color: #44B444">Type [NP][m][n] => 새로운 배열로 새로운 이름자리와 함께 선언된다. [NP]는 m개의 요소를 갖는 배열이며, 총 m개인 각 요소에 해당하는 배열은 요소를 [n]개를 갖는 배열이다.</span>
    4. <span style="color: #44B444">따라서 n개의 요소를 갖는 배열이 m개가 모인 2차원 배열이라고 할 수 있다.</span>
  - <span style="color: #44B444">따라서 이 문제의 답은 int [NP][3][4]이 된다.</span>
- int 요소가 네 개가 모인 배열을 가리키는 포인터 타입을 파생하시오.
  - <span style="color: #44B444">int (\*[NP])[4]</span>
- int 요소가 4개가 모인 배열을 가리키는 포인터를 반환하는 함수를 파생하시오(함수의 매개변수는 없다.)
  - <span style="color: #44B444">int (\*(\*[NP]))[4]</span>
- int 요소 3개인 배열이 2개 모인 배열 타입을 typedef를 이용하여 사용자 정의 타입으로 INT_ARR_23으로 만드시오.
  - <span style="color: #44B444">typedef int(\*INT_ARR_23)[2][3]</span>
- 다음 함수에서 잘못된 부분을 찾은 후 고치시오.

```
void main()
{
  const int ci;
  ci = 1;
}
```

> <span style="color: #44B444">const는 상수로 확정짓는 한정자다. 따라서 const를 사용하여 객체를 생성할 땐 특정한 값으로 반드시 초기화해야한다. 따라서 "const int ci;"부분을 특정한 값을 부여하여 초기화하며 "ci = 1;"코드에도 적합한 값으로 할당해주면 해결된다. 수정방안은 "const int ci = 1;"로 수정하면 된다.</span>

- const int \*와 int \* const의 차이를 설명하시오. 추가적으로 const int \* const도 설명하시오.
  - <span style="color: #44B444">const int \* 은 가리키는 대상에 const가 한정된다. 따라서 초기화할 때 특정한 값 없이도 객체를 생성할 수 있는 반면 const \* int 는 const \* int 의 포인터에 const가 한정되었기 때문에 초기화할 때 반드시 특정한 값으로 초기화가 이루어져야 한다.</span>
- 다음 구문에서 auto는 어떤 타입으로 추론되는가?

```
void main()
{
  auto a = 1;
  cout << a << endl;
}
```

> <span style="color: #44B444">a에 할당되는 값이 1이고, 1은 정수이므로 정수형 데이터 타입으로 많이 쓰이는 int형으로 추측할 수 있다.</span>

{1} 알파벳 'C'부터 'K'까지 몇 개의 알파벳이 있는지 계산하는 프로그램을 작성하시오.

> ```
> 정답
>
> #include <iostream>
> #include <string>
>
> using namespace std;
>
> void main() {
> 	char alphabet[] = { "ABCDEFGHIJKLMNOPQRSTUVWXYZ" };
> 	int count = 0;
> 	bool isC = false;
> 	for (int i = 0; i < sizeof(alphabet) ; i++) {
> 		cout << alphabet[i] << endl;
>
> 		if (alphabet[i] != 'C') {
> 			isC = false;
> 			count++;
> 		}
> 		else { break; }
>
> 	}
> 	cout << 26-count << endl;
> }
> ```

{2} Name 문자 배열을 정의한 후에 자신의 영문 이름을 배열 요소에 하나씩 입력한 후에 출력하는 프로그램을 작성하시오.

> ```
> 정답
>
> #include <iostream>
> #include <string>
>
> using namespace std;
>
> void main() {
> 	char name[4];
> 	name[3] = NULL;
>
> 	for (int i = 0; i < 3; i++) {
> 		cin >> name[i];
> 	}
> 	cout << name << endl;
> }
> ```

{3} 다음은 분자, 분모를 입력받은 후 나눗셈 결과를 출력하는 프로그램이다. Divide 함수를 완성하시오.

```
void main()
{
  int a, b;
  cout << "Input Molecule." << endl;
  cin >> a;
  cout << "Input denominator" << endl;
  cin >> b;

  auto r = Divide(a, b);
  cout << r << endl;
}
```

> ```
> 정답
>
> #include <iostream>
> #include <string>
>
> using namespace std;
>
> double Divide(int a, int b) {
> 	return (double)a / b;
> }
>
> void main() {
> 	int a, b;
> 	cout << "Input Molecule." << endl;
> 	cin >> a;
> 	cout << "Input denominator"<<endl;
> 	cin >> b;
>
> 	auto r = Divide(a, b);
> 	cout << r << endl;
> }
> ```

{4} 다음은 알파벳 하나를 입력받은 후, 대소문자 여부를 출력하는 프로그램이다. CheckResult 함수를 완성하시오.

```
Input an alphabet.
c
It's a lowercase letter.
```

```
Input an alphabet.
C
It's a capital letter.
```

```
Input an alphabet.
+
It's not an alphabet.
```

```
void main()
{
  char c;
  cout << "Input an alphabet." << endl;
  cin >> c;

  CheckResult(c);
}
```

> ```
> 정답
>
> #include <iostream>
> #include <string>
>
> using namespace std;
>
> void CheckResult(char c) {
> 	if (!isalpha(c)) {
> 		cout << "It's not an alphabet." << endl;
> 		return;
> 	}
>
> 	if (islower(c)) {
> 		cout << "It's a lowercase letter." << endl;
> 	}
> 	else {
> 		cout << "It's a uppercase letter." << endl;
> 	}
> }
>
> void main() {
> 	char c;
> 	cout << "Input an alphabet." << endl;
> 	cin >> c;
>
> 	CheckResult(c);
> }
> ```

# Chapter 3

- 연산자는 [<span style="color: #44B444">피연산자</span>]를 취해서 값을 도출하기 위하여 적용되는 연산을 나타내는 기호이다.
- 사칙 연산자(+, -, \*, /)와 같이 셈을 위한 [<span style="color: #44B444">사칙</span>] 연산자가 있으며 값의 대소와 상등을 비교하기 위한 [<span style="color: #44B444">비교</span>] 연산자가 있다. 조건을 조합하여 참 거짓을 따지는 [<span style="color: #44B444">논리</span>] 연산자도 있다.
- a = b 가 식인 이유를 말하시오. (어떤 값을 나타내는가?)
  - [<span style="color: #44B444"> b를 나타낸다. '='으로 표시되는 대입 연산자는 C++에서 앞의 피연산자에 뒤의 피연산자를 대입한다는 의미다. 따라서 해당 식은 대입하는 뒤의 피연사자인 b를 값으로 가진다. a = b 는 값을 가지기에 하나의 식이다.</span>]
- 다음 프로그램의 출력 결과는 무엇인가?

```
void main()
{
  int a, b;

  a = 1;
  b = ++a;
  cout << b << endl;

  a = 1;
  b = a++;
  cout << b << endl;
}
```

<span style="color: #44B444">2</span>  
<span style="color: #44B444">2</span>

- 다음 표의 빈 칸을 채우시오.

| 비교연산식 | a와 b가 같다.                         | a가 b보다 크다.                       | a가 b보다 작다.                       |
| ---------- | ------------------------------------- | ------------------------------------- | ------------------------------------- |
| a==b       | <span style="color: #44B444">1</span> | <span style="color: #44B444">0</span> | <span style="color: #44B444">0</span> |
| a!=b       | <span style="color: #44B444">0</span> | <span style="color: #44B444">1</span> | <span style="color: #44B444">1</span> |
| a>b        | 0                                     | 1                                     | 0                                     |
| a<b        | 0                                     | 0                                     | 1                                     |
| a>=b       | <span style="color: #44B444">1</span> | <span style="color: #44B444">1</span> | <span style="color: #44B444">0</span> |
| a<=b       | <span style="color: #44B444">1</span> | <span style="color: #44B444">0</span> | <span style="color: #44B444">1</span> |

- 다음의 출력 결과는 무엇인가?

```
void main()
{
  int a = 3;
  cout << !!a << endl;
}
```

<span style="color: #44B444">!는 부정 연산자이다. 0이 아닌 값의 부정은 0이다. 따라서 !a는 0의 값을 가진다. 0의 부정은 1을 나타낸다. 따라서 !(!a)의 값은 !(0)의 값이 되므로 1이 된다.</span>

- 다음 출력 결과는 무엇인가?

```
void main()
{
  cout << ~0 << endl;
  cout << !0 << endl;
}
```

> <span style="color: #44B444">-1</span>  
> <span style="color: #44B444">1</span>

- 다음 표의 빈 칸을 채우시오.

| a   | b   | a^b                                   |
| --- | --- | ------------------------------------- |
| 0   | 0   | <span style="color: #44B444">0</span> |
| 0   | 1   | <span style="color: #44B444">1</span> |
| 1   | 0   | <span style="color: #44B444">1</span> |
| 1   | 1   | <span style="color: #44B444">0</span> |

- 다음은 비트 이동 연산의 특징을 설명한 글이다. 빈 칸에 적절한 단어를 채우시오.

1. **<< N:** 비트열을 N만큼 왼쪽으로 이동시킨다. 가장 왼쪽의 넘치는 N개의 비트들은 버리고, 오른족에 새로 생기는 N개의 비트들은 모두 [<span style="color: #44B444">0</span>]으로 채운다.
2. **>> N:** 비트열을 N만큼 오른쪽으로 이동시킨다. 가장 오른쪽의 넘치는 N개의 비트들을 버리고, 왼쪽에 새로 생기는 N개의 비트들은 [<span style="color: #44B444">부호</span>]가 존재할 경우 [<span style="color: #44B444">1</span>]로 채우고, [<span style="color: #44B444">부호</span>]가 존재하지 않을 경우 [<span style="color: #44B444">0</span>]으로 채운다.

- 다음 프로그램의 c1, c2의 비트열을 나타내시오.

```
void main()
{
  char c1= = 2;
  c1 = c1 >> 1;

  char c2 = -126;
  c2 = c2 >> 1;
}
```

> <span style="color: #44B444">00000001</span>  
> <span style="color: #44B444">11111110</span>

- 다음의 출력 결과는 무엇인가?

```
void main()
{
  char c;
  int i;
  double d;
  int arr[4];

  cout << sizeof(c) << endl;
  cout << sizeof(i) << endl;
  cout << sizeof(d) << endl;
  cout << sizeof(arr) << endl;
}
```

> <span style="color: #44B444">1</span>  
> <span style="color: #44B444">4</span>  
> <span style="color: #44B444">8</span>  
> <span style="color: #44B444">16</span>

- 다음의 출력 결과는 무엇인가?

```
void main()
{
  int a = 0;
  cout << ~ ! +a << endl;
}
```

> <span style="color: #44B444">-1</span>

- 다음 구문은 0을 출력한다. 0.5가 출력되도록 코드를 수정하시오.

```
void main()
{
    cout << 1/2 << endl;
}
```

> ```
> void main(){
>  cout << (double) 1 / 2 >> endl;
> }
> ```
>
> {1} 삼항 연산자를 이용하여 입력받은 정수의 짝수, 홀수 여부를 출력하는 프로그램을 작성하시오.

> ```
> 정답
>
> #include <iostream>
> #include <string>
> using namespace std;
>
>
> void main() {
> 	string val;
> 	cin >> val;
> 	string result;
>
> 	bool r = stoi(val) % 2 - 1 ? 1:0 ;
> 	if (r == 1) {
> 		result = "Not Odd";
> 	}
> 	else {
> 		result = "Odd";
> 	}
> 	cout << result << endl;
> }
> ```

{2} XOR을 이용하여 정수 a와 b의 값을 교환하는 프로그램을 완성하시오.

```
void main()
{
  int a = 3;
  int b = 7;

  // 코드 작성

  cout << a << " " << b << endl;
}
```

> ```
> 정답
>
> #include <iostream>
> using namespace std;
>
>
> void main() {
> 	int a = 3;
> 	int b = 7;
>
> 	a = a ^ b;
> 	b = a ^ b;
> 	a = a ^ b;
>
> 	cout << a << " " << b << endl;
> }
> ```

{3} 삼항 연산자를 이용하여 NOT을 함수로 구현하여 다음 프로그램을 완성하시오.

```
void main()
{
  cout << NOT(0) << endl;
  cout << NOT(1) << endl;
}
```

> ```
> 정답
>
> #include <iostream>
> using namespace std;
>
> int NOT(int i) {
> 	int result = !i;
> 	return result;
> }
>
> void main()
> {
> 	cout << NOT(0) << endl;
> 	cout << NOT(1) << endl;
> }
> ```

{4} 삼항 연산자를 이용하여 10,000보다 작은 정수를 입력받은 후 자리 수를 출력하는 프로그램을 작성하시오. (단, 723이 입력되면 3을 출력, 9872가 입력되면 4를 출력한다.)

> ```
> 정답
>
> #include <iostream>
> #include <string>
> using namespace std;
>
> void main()
> {
> 	while (true) {
>
> 		string input;
> 		cin >> input;
> 		if (stoi(input) < 10000) {
> 			cout << input.length() << endl;
> 			break;
> 		}
> 		else {
> 			cout << "Wrong value. Input again." << endl;
> 		}
> 	}
> }
> ```

# Chapter 4

- 프로그램 실행 흐름에 변화를 주는 구문을 [<span style="color: #44B444">제어문</span>]이라고 한다.
- if 문의 조건식은 [<span style="color: #44B444">0</span>]이면 거짓으로 평가되면서 if 문을 빠져나온다.
- 다음 프로그램에서 a, b가 제대로 교환되도록 잘못된 부분을 수정하시오.

```
#define SWAP(a, b) a ^= b; b ^= a; a ^= b;
void main(){
  int a = 0;
  int b = 1;

  if(0)
    SWAP(a, b);

cout << a << " " << b << endl;
}
```

> ```
> 정답
>
> #define SWAP(a, b) a ^= b; b ^= a; a ^= b;
>
> void main(){
> int a = 0;
> int b = 1;
> if(0){
>   SWAP(a, b);
> }
>
> cout << a << " " << b << endl;
> }
> ```

- switch 문의 case 뒤의 값은 변수를 사용할 수 없다. 그 이유를 설명하시오.
  - [<span style="color: #44B444">case 뒤에 표기되는 값은 switch문의 평가식에서 도출된 결과값과 비교하는 값이기 때문에 상수를 사용해야한다.</span>]
- [<span style="color: #44B444">break</span>]는 각각의 case에 해당하는 코드만 실행한 후에 switch 문을 탈출하기 위하여 제공되는 명령이다.
- 다음 프로그램의 출력 결과는 무엇인가?

```
void main(){
int j = 0;
for (int i = 0; i < 10; i = i + 2)
j = i;

cout << j << endl;
}
```

> ```
> 8
> ```

- 다음은 1부터 10까지 합을 구하는 프로그램이다. 9번 줄의 괄호를 채우시오.

```
void main(){
  int Sum = 0;

  int i = 1;
  for(; i < 11; ){
    Sum += i;
    (           )
  }
  cout << Sum << endl;
}
```

> ```
> 정답
>
> void main(){
>  int Sum = 0;
>
>  int i = 1;
>  for(; i < 11; ){
>    Sum += 1;
>    i += 1;
>  }
>  cout << Sum << endl;
> }
> ```

- 다음 프로그램의 출력 결과는 무엇인가?

```
void main(){
  int i = 0;
  int j = 0;

  while(1){
    j = 0;
    while(j <= i){
      if(j == 3)
        break;


      j++;
    }
    if(i == 5)
      break;

    i++;
  }

  cout<< i * j << endl;
}
```

> ```
> 15
> ```

- continue는 [<span style="color: #44B444">반복문</span>]의 명령문 안에서 사용되는데 continue는 실행 흐름을 [<span style="color: #44B444">반복문</span>]의 조건식이 있는 곳으로 이동시킨다. 괄호에 공통으로 들어가는 제어문은 무엇인가?
- goto는 가능하면 사용하지 말라고 권고되는 명령문이다. 왜 그런지 이유를 말해보시오. -[<span style="color: #44B444">스파게티 코드를 양산할 수 있기 때문이다. goto를 사용하는 빈도가 높아질 수록 코드의 실행 흐름을 파악하기 어려워진다.</span>]

{1} if ~ else를 이용하여 입력받은 정수의 짝/홀수 여부를 출력하는 프로그램을 작성하시오.

```
정답

#include <iostream>
#include <string>

using namespace std;

void main()
{
	string input;
	int i;

	while (1) {
		try {
			cin >> input;
			i = stoi(input);
		}
		catch (...) {
			cout << "정수만 입력하세요." << endl;
			continue;
		}
		if (i % 2 == 0) {
			cout << "The number you input is even." << endl;
			break;
		}
		else {
			cout << "The number you input is odd." << endl;
			break;
		}
	}
}
```

{2} 받아쓰기는 10문제로 이루어지고 각각 10점씩 100점 만점이다. 받아쓰기 점수를 입력받은 후 등급을 출력하는 프로그램을 switch 문만 이용하여 작성하시오!
(A: 100, B: 80 ~ 90, C: 50 ~ 70, D: 10 ~ 40, F: 0)

> ```
> 정답
>
> #include <iostream>
> #include <string>
>
> using namespace std;
>
> void main()
> {
> 	string input;
> 	int score;
> 	string rank;
> 	while (1) {
> 		cout << "Input the student's score." << endl;
> 		cin >> input;
> 		try {
> 			score = stoi(input);
> 			if (score % 10 != 0) {
> 				cout << "The value must be a multiple of 10." << endl;
> 			}
> 		}
> 		catch (...) {
> 			cout << "You can only input the numbers. Not letters. Try agian." << endl;
> 			continue;
> 		}
>
> 		switch (score) {
> 		case 100:
> 			rank = "A";
> 			break;
>
> 		case 90:
> 			rank = "B";
> 		case 80:
> 			rank = "B";
> 			break;
>
> 		case 70:
> 			rank = "C";
> 		case 60:
> 		case 50:
> 			break;
>
> 		case 40:
> 			rank = "D";
> 		case 30:
> 		case 20:
> 		case 10:
> 			break;
>
> 		default:
> 			rank = "F";
> 			break;
> 		}
>
> 		cout << "Student's Grade is " << rank << "." << endl;
>
> 		cout << endl << "If you want to stop this program, Input X." << endl;
> 		cin >> input;
> 		if (input == "X") {
> 			break;
> 		}
> 	}
> }
> ```

{3} do ~ while 문을 이용하여 1부터 10까지 합계를 구하는 프로그램을 작성하시오.

> ```
> #include <iostream>
> #include <string>
>
> using namespace std;
>
> void main()
> {
> 	int sum = 0;
> 	int i = 0;
> 	do {
> 		sum += i;
> 		i++;
> 	} while (i < 11);
> 	cout << sum << endl;
> }
> ```

{4} for 문 안에 while 문을 포함시켜서 구구단을 출력하는 프로그램을 작성하시오.

> ```
> #include <iostream>
> #include <string>
>
> using namespace std;
>
> void main()
> {
> 	for (int i = 1; i < 10; i++) {
> 		int j = 1;
> 		while (j < 10) {
> 			cout << i * j << endl;
> 			j++;
> 		}
> 	}
> }
> ```

{5} for, if, continue를 사용하여 1~100까지 짝수만 출력하는 프로그램을 작성하시오.

> ```
> #include <iostream>
> #include <string>
>
> using namespace std;
>
> void main()
> {
> 	for (int i = 2; i < 101; i++) {
> 		if (i % 2 == 0) {
> 			cout << i << endl;
> 		}
> 		else {
> 			continue;
> 		}
> 	}
> }
> ```

{6} 다음은 수학능력시험 표준 점수의 상위 비율에 따른 등급표이다. 이 표를 기반으로 다음 프로그램을 작성하시오.
| Grade 1 | 0% ~ 4% |
|---------|------------|
| Grade 2 | 4% ~ 11% |
| Grade 3 | 11% ~ 23% |
| Grade 4 | 23% ~ 40% |
| Grade 5 | 40% ~ 60% |
| Grade 6 | 60% ~ 77% |
| Grade 7 | 77% ~ 89% |
| Grade 8 | 89% ~ 96% |
| Grade 9 | 96% ~ 100% |

(1) 수학능력시험 상위 비율을 입력받은 후 등급을 출력하는 프로그램을 if ~ else ~ if문만을 이용하여 작성하시오.

> ```c++
>
> // 정답
> void main()
> {
> 	string input;
> 	float score;
> 	int grade;
> 	while (1) {
> 		cout << "학생의 상위 비율을 입력하세요. 양의 실수만 입력 가능합니다." << endl;
> 		cin >> input;
>
> 		try {
> 			score = stof(input);
> 		}
> 		catch (...) {
> 			cout << "양의 실수만 입력 가능합니다. 다시 입력하세요." << endl;
> 			continue;
> 		}
>
> 		if (score <= 4) 		grade = 1;
> 		else if (score <= 11)	grade = 2;
> 		else if (score <= 23)	grade = 3;
> 		else if (score <= 40)	grade = 4;
> 		else if (score <= 60)	grade = 5;
> 		else if (score <= 77)	grade = 6;
> 		else if (score <= 89)	grade = 7;
> 		else if (score <= 96)	grade = 8;
> 		else					grade = 9;0
>
> 		cout << "This Student achieves Grade " << grade << endl;
> 	}
> }
> ```

(2) 표준 등급을 입력할 경우 100명당 평균 몇 등인지를 출력하는 프로그램을 작성하시오.

```
표준 등급을 입력하세요!
4
평균 31.5등입니다.
```

```c++
// 정답

string input;
unsigned int grade;
float rank;

while (1) {
	try {
		cout << "표준 등급을 입력하세요." << endl;
		cin >> input;
		grade = stoi(input);
		if (grade < 1 || grade > 9) {
			continue;
		}
	}
	catch (...) {
		cout << "자연수만 입력 가능합니다." << endl;
		continue;
	}

	switch (grade) {
	case 1:
		rank = 2;
		break;
	case 2:
		rank = 7.5;
		break;
	case 3:
		rank = 17;
		break;
	case 4:
		rank = 31.5;
		break;
	case 5:
		rank = 50;
		break;
	case 6:
		rank = 68.5;
		break;
	case 7:
		rank = 83;
		break;
	case 8:
		rank = 92.5;
		break;
	default:
		rank = 98;
		break;
	}
	cout << "학생의 등급으로 미루어 평균적인 석차는 " << rank << "등 입니다." << endl;
}
```

# chapter 5

- 포인터는 [<span style="color: #44B444">변수</span>]를 이용하여 메모리 영역에 접근할 수 있도록 제공되는 개념이다.
- 포인터가 가리키는 메모리 영역을 해석하기 위해서는 [<span style="color: #44B444">타입</span>] 정보가 필요하다.
- 변수의 주소를 구하는 연산자는 [<span style="color: #44B444">주소 연산자</span>]이고, 포인터가 가리키는 메모리 영역을 나타내는 연산자는 [<span style="color: #44B444">간접 연산자</span>]이다.
- 다음 프로그램에서 변수 a의 값을 1 증가시키고, 증가시킨 값을 출력하도록 p와 연산자만을 사용하여 괄호를 채우시오.

```c++
void main(){
  int a = 3;
  int* p = &a;

  cout << ( ) << endl;
}
```

> ```c++
> void main(){
>  int a = 3;
>  int* p = &a;
>
>  cout << ++ * p << endl;
> }
> ```

- TYPE\* p; 문에서 p의 타입은 [<span style="color: #44B444">포인터</span>]이고, p의 대상 타입은 [<span style="color: #44B444">TYPE</span>]이다.
- int 요소 3개가 모인 배열을 가리키는 포인터 p를 정의하시오.
  > <span style="color: #44B444">int (\*p)[3];</span>
- int* p1, p2, *p3; 문에서 p1~p3 중 포인터를 모두 고르시오.
  > <span style="color: #44B444">p1, p3 // C++에서의 변수 선언은 쉼표를 활용하여 각자 선언이 가능하지만, 간접 연산자는 각각 개별적으로 할당해주며 선언해야한다.</span>
- 포인터의 크기는 일반적으로 시스템의 크기에 의해서 결정된다. 보통 32비트에서는 [<span style="color: #44B444">4</span>]바이트이고, 64비트에서는 [<span style="color: #44B444">8</span>]바이트이다.
  >
- 다음 프로그램의 출력 결과는 무엇인가?

```c++
void main(){
  char* pC = NULL;
  int* pI = NULL;
  double* pD = NULL;

  cout << (void*)(pC + 2) << endl;
  cout << (void*)(pI + 2) << endl;
  cout << (void*)(pD + 2) << endl;
}
```

> ```
> 0000000000000002
> 0000000000000008
> 0000000000000010
>
> 여기서 각 값은 16진수이다. 따라서 마지막 pD포인터의 +2를 한 값은 10진수로 16을 나타낸다.
> ```

- 포인터 p의 대상 타입이 TYPE일 때, p++는 p가 가리키는 주소보다 [<span style="color: #44B444">sizeof(TYPE) 크기</span> ]만큼 증가된 주소를 가리킨다. 반대로 p--는 p가 가리키는 주소보다 [<span style="color: #44B444">sizeof(TYPE) 크기</span>]만큼 감소된 주소를 가리킨다.
- 포인터 p의 대상 타입이 TYPE일 때, p[N]은 p가 가리키는 주소보다 [<span style="color: #44B444">N * sizeof(TYPE) 크기</span>] 만큼 증가된 주소의 [<span style="color: #44B444">sizeof(TYPE)</span>] 크기의 메모리 영역을 나타낸다. 따라서 p[N]은 \*[<span style="color: #44B444"></span>]과 같다.
- void 포인터가 필요한 이유를 설명하시오.
  - <span style="color: #44B444">오로지 메모리 주소만을 카리키기 위해 존재한다. void 포인터에는 어떤 타입의 포인터도 대입할 수 있다. 또한 void 포인터는 어떤 타입이든 변환될 수 있다. 즉, 범용적인 포인터다.</span>
- 다음 프로그램에서 잘못된 부분을 찾아본 후, i가 1이 되도록 수정하시오.

```c++
void main(){
  int i;
  void* p = &i;
  *p = 1;
}
```

```c++
정답

void main(){
  int i;
  void* p = &i;

  //*p = 1;
  *(int*)p = 1;
}

// void 포인터는 대상 타입이 void이기 때문에 포인터가 가리키는 주소의 메모리 영역 크기가 0이다. 즉, voi d 포인터로 메모리 영역을 접근할 수 없다. 따라서 void 포인터를 사용하여 메모리 영역에 접근할 경우 타입 변환이 필요하다.
```

- 다음 프로그램에서 잘못된 부분을 찾고 1이 출력되도록 ra를 변경하시오.

```c++
void main(){
  int a;
  int& ra;
  ra = a;

  cout << a << endl;
}
```

```c++
정답

void main(){
  int a;
  int* ra = a;
  ra = 1;

  cout << a << endl;
}
```

- 참조 타입 변수에 [<span style="color: #44B444">const</span>]가 지정되면 상수로 초기화가 가능하다.

{1} 다음 프로그램의 출력 결과가 문자열 "C++"가 되도록 Set 함수를 작성하시오.

```c++
void main(){
  int a = 0;
  char* s = (char*)&a;

  Set(s);
  cout << (char*)&a << endl;
}
```

```c++
정답

#include <iostream>
#include <string>

using namespace std;

void Set(char* c) {
	*(c + 0) = 'C';
	*(c + 1) = '+';
	*(c + 2) = '+';
	*(c + 3) = '\0';
}

void main()
{
	int  a = 0;
	char* s = (char*)&a;

	Set(s);
	cout << (char*)&a << endl;
}
```

{2} 다음 프로그램의 출력 결과가 3이 되도록 Set 함수를 작성하시오.

```c++
void main(){
  int a;
  int* p = &a;
  int** pp = &p;

  Set(pp, 3);
  cout << a << endl;
}
```

```c++
정답

#include <iostream>
#include <string>

using namespace std;

void Set(int** p, int i) {
	**p = i;
}

void main()
{
	int a;
	int* p = &a;
	int** pp = &p;

	Set(pp, 3);
	cout << a << endl;
}

```

{3} 다음 프로그램의 출력 결과가 3이 되도록 Increment 함수를 작성하시오.

```c++
void main(){
  int a = 2;
  Increment(a);
  cout << a << endl;
}
```

```c++
정답

void Increment(int& i) {
	int& p = i;
	p++;
}

void main(){
  int a = 2;
  Increment(a);
  cout << a << endl;
}
```

{4} memset 함수는 dest가 가리키는 주소로부터 count 바이트의 메모리 영역에 1바이트씩 값 c를 채우는 역할을 한다.

```c++
void* memset(void *dest, int c, size_t count);
```

같은 기능을 수행하는 MyMemset 함수를 구현하시오.(다음 프로그램을 실행할 경우 -1이 출력되어야 한다.)

```c++
void main(){
  int a;
  MyMemset(&a, -1, 4);
  cout << a << endl;
}
```

```c++
정답

#include <iostream>
#include <string>

using namespace std;

void MyMemset(int* k, int c, size_t count) {
	char* cP = (char*)k;
	for (int i = 0; i < count; i++) {
		*(cP + i) = c;
	}
}

void main()
{
	int a;
	MyMemset(&a, -1, 4);
	cout << a << endl;
}
```
