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

# Chapter 6

- 일반적으로 배열 요소의 수는 상수만 가능하다 그러나 [<span style="color: #44B444">가변 크기 배열</span>]을 지원하는 GCC의 경우 변수도 배열 요소의 수가 될 수 있다.
- 배열의 요소는 일렬로 모아져 있어서 차례가 있다. 따라서 각 요소에는 순번이 있으며, 순번을 [<span style="color: #44B444">인덱스</span>]라고 한다. [<span style="color: #44B444">인덱스</span>]는 0부터 시작한다.
- TYPE arr[N]; 문에서 첫 번째 요소와 마지막 요소를 arr과 첨자를 이용하여 나타내시오.
  - <span style="color: #44B444">첫번째 요소: \*arr 또는 arr[0] // 마지막 요소: arr[N-1]</span>
- 다음 프로그램에서 잘못된 부분을 설명하시오.

```c++
void main(){
  int a[2] = {0,1};
  int b[2] = a;
}
```

> <span style="color: #44B444">배열명 b를 선언하고 초기화를 배열 a로 하려할 때, 배열명 a가 배열의 값인 {0, 1}을 나타내지 않기 때문에 컴파일 오류가 난다.</span>

- TYPE arr[N]; 문에서 배열 이름 arr은 포인터로 사용될 수 있다. 포인터로 사용되는 arr의 타입은 [<span style="color: #44B444">TYPE*</span>]이며 요소의 수 N은 영향을 주지 않는다.
- TYPE arr[N]; 문에서 &arr은 배열 자체를 가리키는 포인터이다. &arr의 타입은 [<span style="color: #44B444">배열 타입</span>]이다.
- 다음 배열 arr1 ~ arr4 중에서 다른 값을 가지고 있는 배열은 무엇이고 이유는 무엇인가?

```c++
void main(){
  int arr1 = {};
  int arr2 = {0};
  int arr3 = {0, };
  int arr4;
}
```

> <span style="color: #44B444">arr4는 다른 값을 가지는 배열이다. arr1 ~ arr3까지는 모두 초기화는 되었지만, 요소의 값이 정해지지 않아 미정인 요소에는 0 또는 NULL이 할당된다. 하지만 초기화조차 되지않은 arr4의 요소는 어떤 값이 들어갔는지 알 수 없다. 이를 미정의 값 또는 쓰레기 값이 들어있다고 한다.</span>

- char str[] = "C++"; 문에서 str 배열의 요소의 수와 마지막 요소의 값은 무엇인가?
  > <span style="color: #44B444">3개의 요소를 가지는 char 배열이다. 마지막 요소의 값은 +이다.</span>
- int 요소가 세 개인 배열이 두 개 모인 배열 arr은 왜 int arr[3][2]가 아닌지 설명하시오.

  > <span style="color: #44B444">타입 파생 규칙에 따라 </span>  
  > <span style="color: #44B444">1. 배열의 가장 작은 요소는 int이다. 따라서 int [NP]이다. </span>  
  > <span style="color: #44B444">2. int 요소가 3개인 배열이므로 우선 int [NP][3]으로 선언된다.</span>  
  > <span style="color: #44B444">3. 이어서 int [NP][3]를 2개 갖는 2차원 배열이므로, [NP]바로 뒤에 [2]를 선언한다. int [NP[2][3]]</span>  
  > <span style="color: #44B444">4. [NP]자리에 배열의 이름을 쓰고 세미콜론으로 마무리한다. int arr[2][3];</span>

- int arr[2][3]의 여섯 개 요소를 순서대로 11, 12, 13, 21, 22, 23으로 초기화하는 코드를 작성하시오.

```c++
정답

#include <iostream>

void main()
{
	int arr[2][3] = { {11, 12, 13,}, {21, 22, 23} };
}
```

- 2차원 배열은 종종 행렬로 여겨진다. 그러나 2차원 배열을 행렬과 비교하기에는 무리한 점이 있다. 어떤 점에서 다른지 설명하시오.
  > <span style="color: #44B444">행렬은 테이블 형태를 띄는 2차원이지만, 배열은 항상 1차원이다. 메모리로 접근하게 되면 TYPE arr[2][3]의 경우엔 arr[0,0], arr[0,1], arr[0,2], arr[1,0], arr[1,1], arr[1,2] 순서대로 메모리에 1차원 선형인 형태로 저장되어 접근할 수 있기 때문에 행렬과 비교하기엔 무리가 있다.</span>
- 다음 프로그램의 s1과 s2를 포인터 관점에서의 차이점을 설명하시오.

```c++
void main(){
  char s1[] = "C++";
  char* s2 = "C++";
}
```

> <span style="color: #44B444">s1에는 더 이상 다른 값이 대입될 수 없지만 s2는 상수가 아닌 일반 포인터이므로 다른 주소를 할당해버릴 수도 있다. s1은 상수이고, s2는 변수이다.</span>

- 다음 프로그램의 문제점을 찾아서 수정하시오.

```c++
void main(){
  int arr[2][3] = {{11, 12, 13,}, {21, 22, 23}};
  int** pp = (int**)arr;
  cout << pp[1][2] << endl;
}
```

```c++
정답

void main()
{
	int arr[2][3] = { {11, 12, 13,}, {21, 22, 23} };
	int** pp = (int**)arr;
	cout << pp[1][2] << endl;
}

또는

void main()
{
	int arr[2][3] = { {11, 12, 13,}, {21, 22, 23} };
	int* arrM[2] = { arr[0], arr[1] };
	int** pp = arrM;
	cout << pp[1][2] << endl;
}

// arr이 포인터로 사용될 경우 대상 타입은 int [3]이므로 int (*)[3]이 된다. int**인 포인터 pp에 타입이 전혀 다른 arr을 대입하면 안된다. 하지만 강제 타입 변환(int**)을 이용하여 pp에 arr을 대입하였으니 pp[1][2]가 어딜 가리키는지 살펴보자.

// pp는 포인터의 포인터로서 타입은 int**이다. 따라서 대상 타입은 int*이다. pp[1]은 타입이 int*면서 *(pp + 1)과 같다. *(pp + 1)은  pp의 대상 타입인 int*의 크기, 즉 sizeof(int*) = 8(64bit)만큼 pp의 주소에서 증가시킨 후 sizeof(int*) 크기의 영역을 나타낸다. 따라서 arr[0][2]와 arr[1][0]이 나타내는 영역을 합한 영역이 된다. 각각 13과 21이 있으므로 8바이트로 합쳐 계산하면 0x15,0000,000D가 된다. pp[1]의 타입은 int*이므로 pp[1][2]는 *(pp[1] + 2)와 같다. *(pp[1] + 2)는 pp[1]의 대상 타입인 int의 크기, 즉 2 * sizeof(int) = 8만큼 pp[1]의 주소에서 증가시키고 sizeof(int) = 4 크기의 영역을 나타낸다. 실제 가리키는 영역의 주소는 0x15,0000,000D + 8 = 0x15,0000,0015가 된다. pp[1][2]가 나타내는 영역이다. 아마 해당 주소는 가상 메모리에서 commit 되지 않았기 때문에 읽기 금지 상태여서 런타임 오류가 발생할 것이다.
```

- 다음 프로그램의 출력 결과를 설명하시오.

```c++
void func(int arg[1]){
  arg[0] = 2;
}

void main(){
  int arr[1] = {1};
  func(arr);
  cout << arr[0] << endl;
}
```

> <span style="color: #44B444">arr[0]은 함수를 거쳐 2를 나타낸다. C++은 배열을 인자로 넘길 때 값으로 넘기지 않는다. 정확히 얘기하자면 값으로서 넘길 수가 없다. 배열명은 상수 포인터이므로 정확하게는 배열의 주소가 인자로 넘어갈 뿐이다. (번외로 func의 매개 변수인 int arg[1]은 컴파일러에 의해 int\* arg로 치환된다.)</span>

- 함수 void func(int arg[3])의 매개 변수 타입은 컴파일러에 의해서 자동으로 변환되어 void func<span style="color: #44B444">(int\* arg)</span>이 된다.

  > <span style="color: #44B444">배열이 매개 변수로 사용되는 경우, 컴파일러에 의해 매개 변수는 포인터 타입으로 치환된다.</span>

- 함수 void func(int arg[3][4])의 매개 변수 타입은 컴파일러에 의해서 자동으로 변환되어 void func<span style="color: #44B444">(int (\*arg)[3])</span>이 된다.

  > <span style="color: #44B444">앞서 포인터의 포인터가 2차원 배열과 제대로 호환될 수 없다는 것을 안다면 이해하기 쉽다. int\** arg는 될 수 없고, 배열과 호환될 수 있는 배열 요소 타입인 포인터는 가능하다. 즉, 매개 변수 int arr[2][3]의 요소 타입은 int [3]이므로 대상 타입이 int [3]인 포인터로 변환되어야 한다. 따라서 int arg[2][3]은 정확히 int (*arg)[3]으로 치환된다.</span>

- 다음 프로그램의 출력 결과는 무엇인가?

```c++
void main(){
  double arr[2][3];
  cout << sizeof(arr) << endl;
  cout << sizeof(arr[0]) << endl;
  cout << sizeof(arr[0][0]) << endl;
}
```

> <span style="color: #44B444">48</span>  
> <span style="color: #44B444">24</span>  
> <span style="color: #44B444">8</span>

{1} 배열 int arr[] = { 1, 6, 9, 7, 3, 2, 0, 4, 8, 5}를 가지고 다음 프로그램을 작성하시오.

- (1) arr의 모든 원소의 합을 구하는 프로그램
- (2) arr의 최솟값과 최댓값을 구하는 프로그램
- (3) arr의 원소들을 역순으로 재구성하는 프로그램
- (4) arr의 원소들을 오름차순으로 정렬하여 재구성하는 프로그램

```c++
정답

#include <iostream>

using namespace std;

void main()
{
	int arr[] = { 1,6,9,7,3,2,0,4,8,5 };
	int sum = 0;

  // (1)
	for (int i = 0; i < (sizeof(arr) / sizeof(int)); i++) {
		sum += arr[i];
	}
	cout << sum << endl;


  // (2)
	int min = 0;
	int max = 0;
	for (int i = 0; i < (sizeof(arr) / sizeof(int)); i++) {
		if (max < arr[i]) {
			max = arr[i];
		}
		if (min > arr[i]) {
			min = arr[i];
		}
	}
	cout << min << ", " << max << endl;

  // (3)
	for (int i = 0; i < (sizeof(arr) / sizeof(int)); i++) {
		for (int j = i; j < (sizeof(arr) / sizeof(int)); j++) {
			if (arr[j] <= arr[i]) {
				continue;
			}
			else{
				int cur = arr[i];
				arr[i] = arr[j];
				arr[j] = cur;
			}
		}
	}

  // (4)
	for (int i = 0; i < (sizeof(arr) / sizeof(int)); i++) {
		for (int j = i; j < (sizeof(arr) / sizeof(int)); j++) {
			if (arr[j] >= arr[i]) {
				continue;
			}
			else {
				int cur = arr[i];
				arr[i] = arr[j];
				arr[j] = cur;
			}
		}
	}

}
```

{2} 다음은 네 학생의 국어, 영어, 수학 성적이다. 각 학생별 총점을 구하고, 각 과목별 평균을 출력하시오.
| 번호 | 국어 | 영어 | 수학 |
|------|------|------|------|
| 1 | 100 | 100 | 50 |
| 2 | 90 | 70 | 80 |
| 3 | 70 | 80 | 90 |
| 4 | 80 | 100 | 90 |

```c++
정답

#include <iostream>

using namespace std;

void main()
{
	int grade[4][4] = {
		{1,100,100,50},
		{2,90,70,80},
		{3,70,80,90},
		{4,80,100,90}
	};

	int sum[4];
	float avg[3];

	for (int i = 0; i < 4; i++) {
		int s = 0;
		float a = 0;
		for (int j = 0; j < 4; j++) {
			a += grade[j][i];
			if (j > 0) {
				s += grade[i][j];
			}
		}
		sum[i] = s;
		if (i > 0) {
			avg[i - 1] = a / 4;
		}
	}

	for (int i = 0; i < 4; i++) {
		for (int j = 1; j < 4; j++) {

		}
	}

	for (int i = 0; i < 4; i++) {
		cout << sum[i] << " ";
		if (i > 2)
			continue;
		cout << avg[i] << endl;
	}
}
```

# Chapter 7

- 구조체 정의와 일반 변수 정의의 차이를 설명하시오.

  > <span style="color: #44B444">구조체를 정의하는 것은 새로운 파생 타입을 정의하는 것이다. 일반 변수를 정의하는 것과 같이 객체가 만들어지는 것이 아닌, 설계도를 정의하는 것이기 때문에 메모리를 차지하지 않는다.</span>

- 구조체 타입을 정의할 때는 <span style="color: #44B444">태그명</span>을 사용할 수도 있으며, <span style="color: #44B444">typedef</span>를 이용하여 새로운 타입 이름으로 사용자 정의할 수도 있다.

- 멤버로 char m을 가지는 구조체를 typedef를 이용하여 SType으로 사용자 정의하시오.

```c++
정답

typedef struct SType {
	char m;
}Stype;
```

- 구조체 객체는 대입 연산의 <span style="color: #44B444">피연산자</span>가 될 수 있다. 단 좌변과 우변의 구조체 타입이 일치해야 한다.

- <span style="color: #44B444">직접 멤버 </span> 연산자는 구조체 멤버를 접근하기 위하여 제공된다. <span style="color: #44B444">직접 멤버 </span> 연산자의 피연산자는 두 개이며, 좌변이 구조체 객체 이름이고 우변은 멤버 이름이다.

- <span style="color: #44B444">간접 멤버</span> 연산자는 구조체 멤버를 접근하기 위하여 제공된다. <span style="color: #44B444">간접 멤버</span> 연산자의 피연산자는 두 개이며, 좌변이 구조체 포인터이고 우변은 멤버 이름이다.

- 다음 프로그램에서 잘못된 부분을 찾고 그 이유를 설명하시오.

```c++
typedef struct STag
{
  char m;
} SType;

void main(){
  Stype a, b;

  a.m = 1;
  b = a;

  if(a == b){
    cout << "Equal" << endl;
  }
}
```

> <span style="color: #44B444">구조체에는 비교 연산자를 사용할 수 없다. 따라서 if 조건문의 조건식은 에러를 유발한다.</span>

- 구조체의 크기는 모든 멤버들의 타입 크기의 총합보다 클 수 있다. 구조체 내부에 <span style="color: #44B444">패딩(Padding)</span>이 존재하기 때문이다. 따라서 실제 구조체가 차지하는 메모리 크기를 구하기 위해서는 <span style="color: #44B444">sizeof</span> 연산자를 사용해야 한다.

- 다음 구조체에 대하여 구조체 멤버 맞춤(/Zp8, /Zp2, /Zp1)에 따른 메모리 구조도를 그려보시오.

```c++
typedef struct
{
  char c;
  int i;
}SType
```

> <span style="color: #44B444">char 형식은 1바이트, int 형식은 4바이트의 크기를 갖는다. 그리고 구조체 멤버 맞춤을 할 때, 멤버 오프셋은 구조체 멤버 맞춤 형식과 멤버 타입의 크기 중 작은 값의 배수가 되어야 한다. 또, 메모리 영역이 할당되는 순서는 먼저 선언된 멤버부터 할당된다.</span>
>
> <span style="color: #44B444">따라서 /Zp8 형식의 메모리 구조도는 오프셋 0의 위치에 char c가 1바이트 할당된다. 이후 두번째 멤버인 int i의 크기와 8 중 작은 것의 배수가 오프셋이 되므로 비교를 하면 int 형식은 4바이트, /Zp8 형식의 크기는 8바이트이므로 int 형식의 크기가 더 작다. 따라서 오프셋은 4바이트로 결정되고, 오프셋 0에 c가 할당됐으니, 다음 멤버는 4에 할당 된다. 하지만 char c는 1바이트의 크기를 가지니, 4-1 = 3, 남은 3 바이트의 크기는 패딩(padding)이 된다. 이렇게 8바이트 크기의 SType 구조체 객체가 메모리에 할당된다.</span>
>
> <span style="color: #44B444">/Zp4는 두번째 멤버의 크기와 4의 크기가 같으므로 첫번째 멤버는 오프셋 0, 두번째 멤버는 오프셋 4가 된다. 따라서 남은 3바이트 크기의 1~3에 해당하는 오프셋은 패딩이 된다.</span>
>
> <span style="color: #44B444">/Zp2는 두번째 멤버의 크기가 2보다 크다. 따라서 멤버의 오프셋은 2바이트가 된다. 첫번째 멤버는 오프셋 0, 두번째 멤버는 오프셋 2를 갖게 된다. char c는 1바이트 이므로 0~1 영역에는 c가 할당되고, 1~2 영역은 패딩이 된다. 2~6까지 총 4바이트 크기의 영역은 int i에 할당된다. 따라서 SType 구조체 객체는 6바이트 크기가 된다.</span>
>
> <span style="color: #44B444">/Zp1는 패딩이 없는 형식이다. 최소단위인 1의 크기로 오프셋을 형성해야 한다. 첫번째 멤버는 언제나 오프셋 0을 가진다. 첫번째 멤버인 char c의 크기는 1바이트 이므로 바로 오프셋 1을 가진다. 0~1은 char c, 1~5는 int i가 할당된다. 패딩은 없으며, SType 구조체는 5바이트의 크기를 갖는다.</span>

- 다음 프로그램의 출력 결과와 이유를 설명하시오.

```c++
typedef struct
{
  int m;
}SType;

void Func(SType arg)
{
  arg.m = 2;
}

void main(){
  SType a;
  a.m = 1;

  Func(a);

  cout << a.m << endl;
}
```

> <span style="color: #44B444">배열에서도 그랬듯이 함수에 인수로 값을 전달하면 함수의 매개변수의 객체가 임시로 메모리에 생성되어 해당 값을 복사한다. 위 코드에선 함수 실행동안 SType 타입의 arg라는 객체가 생성되어 a의 값을 복사해온다는 뜻이다. 그리고 함수 내에서 연산은 arg를 이용하여 이뤄지기 때문에 a에는 영향을 줄 수 없다.</span>
>
> <span style="color: #44B444">하지만 함수에 인자로 전달한 객체의 값을 함수 내에서 직접 변경할 수 있는데, 이는 매개변수를 포인터타입으로 삼으면 된다. SType\* pArg로 생성하여 a의 포인터를 전달한다면 실제 a의 주소에 접근이 가능해지므로 함수 내부에서 일어나는 연산들은 a에 영향을 줄 수 있게 된다. 코드는 다음과 같다.</span>

```
정답

typedef struct {
    int m;
}SType;

void Func(SType* pArg) {
    pArg->m = 2;
    cout << pArg->m << endl;
}

void main() {
    SType a;
    a.m = 1;

    Func(&a);

    cout << a.m << endl;
}
```

### ※ <span style="color: #FF7777">구조체를 값에 의한 함수의 인자로 사용할 경우 객체 간 복사가 이루어지므로 효율이 떨어지기 마련이다. 따라서 대부분은 구조체 객체를 값에 의해 전달하기 보다는 구조체의 포인터를 전달하는 방식을 많이 사용한다.</span>

- <span style="color: #44B444">공용체</span>는 구조체의 일종이며 멤버들이 메모리 영역을 공유한다. <span style="color: #44B444">공용체</span>를 정의할 때는 struct 대신 <span style="color: #44B444">union</span>을 사용한다.

- 다음 프로그램의 출력 결과는 무엇인가?

```c++
typedef union
{
  __int64 a;
  int b;
}UType;

void main(){
  UType u;
  u.a = 1;

  cout << u.b << endl;
  cout << sizeof(u) << endl;
}
```

```c++
1
8

// 공용체 멤버는 같은 메모리 영역을 점유한다. 그리고 __int64타입은 8바이트, int타입은 4타입이므로 멤버 중 가장 큰 타입의 크기가 곧 공용체의 크기다. UType은 __int64의 크기인 8바이트의 크기를 가지며, a에 값을 할당한다면 공용체의 메모리 영역과 a의 메모리 영역은 같을 것이므로 공용체의 값은 a의 값을 나타나게 된다.
```

{1} 다음 로봇 명세를 보고 프로그램을 작성하시오.
| 이름 | 신장(m) | 무게(T) | 마력 |
|------------|---------|---------|------|
| 태권브이 | 18 | 80 | 3000 |
| 마징가 | 17 | 70 | 2500 |
| 메칸더브이 | 20 | 90 | 3500 |
| 그랜다이져 | 33 | 100 | 5000 |

(1). 로봇을 나타내는 구조체(Robot)를 설계하시오.

```c++
typedef struct Robot {
    string name = {};
    int height;
    int weight;
    int power;
};
```

(2). 로봇의 명세를 출력하는 함수 Print를 작성하시오(매개 변수 타입은 Robot\*).

```c++
void Print(Robot* pRobot) {
    cout << pRobot->name << endl
        << "Height: " << pRobot->height << "m" << endl
        << "Weight: " << pRobot->weight << "T" << endl
        << "Power: " << pRobot->power << endl;
}
```

(3). 로봇들의 평균 신장, 평균 무게, 평균 마력을 출력하는 함수 Avg를 작성하시오. (매개 변수 타입은 Robot [4])

```c++
void Avg(Robot robots[4], int size) {
	int hSum = 0;
	int wSum = 0;
	int pSum = 0;

	for (int i = 0; i < size; i++) {
		hSum += robots[i].height;
		wSum += robots[i].weight;
		pSum += robots[i].power;
	}


	cout << endl
		<< "=== Average Result ===" << endl
		<< "Height: " << hSum / size << endl
		<< "Weight: " << wSum / size << endl
		<< "Power: " << pSum / size << endl;
}
```

(4). (1), (2), (3)을 이용하여 모든 로봇의 명세를 출력하는 프로그램을 작성하시오.

```c++
#include <iostream>
#include <string>

using namespace std;

// 사용된 함수들은 이미 서술함.
void main() {

	Robot a, b, c, d;

	a.name = "태권브이";
	a.height = 18;
	a.weight = 80;
	a.power = 3000;

	b.name = "마징가";
	b.height = 17;
	b.weight = 70;
	b.power = 2500;

	c.name = "메칸더브이";
	c.height = 20;
	c.weight = 90;
	c.power = 3500;

	d.name = "그랜다이져";
	d.height = 33;
	d.weight = 100;
	d.power = 5000;

	Robot robots[4] = { a,b,c,d };

	int size = sizeof(robots) / sizeof(Robot);

	Print(&a);
	Print(&b);
	Print(&c);
	Print(&d);

	Avg(robots, size);
}
```

# Chapter 8

- 함수 호출이 완료되면 반환을 한다. 이때 특정한 반환 값이 없는 경우가 있다. 이런 경우 사용하는 반환 타입은 <span style="color: #44B444">void</span>이다.

- 함수 선언이 필요한 이유는 무엇인가?

  > <span style="color: #44B444">컴파일러는 코드를 위에서 아래로 순차적으로 컴파일하기 때문에 함수를 선언해두지 않고 main함수 이후에 함수를 선언하며 정의한다면 컴파일러에서 함수라고 확신하지 못해 main함수 이전에 미리 선언해두는 것이 중요하다.</span>

- C 표준 라이브러리 함수인 printf를 사용하기 위하여 포함시켜야 할 헤더 파일을 하나 이상 말해보시오.

  > <span style="color: #44B444">stdio.h</span>

- 함수의 인자는 <span style="color: #44B444">매개 변수</span>와 <span style="color: #44B444">실인자</span>로 구분된다. <span style="color: #44B444">매개 변수</span> 는 함수 본체에서 사용되는 인자를 의미하며, <span style="color: #44B444">실인자</span>는 함수를 호출할 때 넘어가는 인자를 의미한다.

- 다음 프로그램의 함수 Increment의 매개 변수와 실인자를 말해보시오.

```c++
int Increment(int arg){
  arg++;
  return arg;
}

void main(){
  cout << Increment(3) << endl;
}
```

> <span style="color: #44B444">매개 변수: arg, 실인자: 3</span>

- C++ 함수의 인자 전달 방식은 일반적으로 세 가지로 나누어진다. <span style="color: #44B444">값</span> 전달, <span style="color: #44B444">주소</span> 전달, <span style="color: #44B444">참조</span> 전달 방식이 있다.

- 다음 프로그램의 출력 결과는 무엇인가?

```c++
void FuncValue(int  arg){
  arg = 1;
}

void FuncPointer(int* arg){
  *arg = 2;
}

void FuncReference(int& arg){
  arg = 3;
}

void main(){
  int i = 0;
  FuncValue(i);
  cout << i << endl;

  int j = 0;
  FuncPointer(&j);
  cout << j  << endl;

  int k = 0;
  FuncReference(k);
  cout << k << endl;
}
```

> <span style="color: #44B444">0</span>  
> <span style="color: #44B444">2</span>  
> <span style="color: #44B444">3</span>

- 함수 인자의 참조 전달은 내부적으로 포인터를 이용하여 구현되므로 본질적으로 주소 전달의 일종이라고 생각할 수 있다. 그렇다면 왜 C++에서는 참조 전달을 많이 사용하는 것인지 이유를 기술하시오.

  > <span style="color: #44B444">포인터를 이용한 주소 전달보다 사용성에서 편리하기 때문이다. 인자 전달이나 접근 과정에서 주소 연산자나 간접 연산자를 사용할 필요가 없기 때문이다.</span>

- 다음 프로그램의 함수 GetNextValue를 출력 결과가 2가 나오도록 수정하시오.

```c++
int GetNextValue(int& arg){
  return arg + 1;
}

void main(){
  cout << GetNextValue(1) << endl;
}
```

```c++
정답

int GetNextValue(const int& arg) {
	return arg + 1;
}

void main() {
	cout << GetNextValue(i) << endl;
}
```

- 다음은 함수 Increment의 선언이다. 이 함수를 제대로 호출하지 못한 경우는 무엇인가?

```c++
int Increment(int arg = 0, int delta = 1);
```

    1. Increment(3);
    2. Increment(3, 2);
    3. Increment();
    4. Increment( , 2);

> <span style="color: #44B444">4번은 호출하지 못한다. 기본인자가 설정된 함수의 경우, 인수를 생략하려면 생략한 인수 이후에 나열되는 모든 인수도 기본값으로 사용해야 한다. 하지만 4번은 첫번째 인자를 기본값으로 사용하려하지만 두번째 인자는 값을 주려하므로 호출할 수 없는 형태이다.</span>

- 가변 인자 함수의 인자는 최소 하나 이상의 고정 인자와 <span style="color: #44B444">줄임표</span>로 이루어진다.

- 가변 인자 함수의 인자 중에서 고정 인자의 마지막 인자를 기준 인자라고 한다. 기준 인자는 어떤 역할을 하는지 기술하시오.

  > <span style="color: #44B444">함수 본체에서 가변 인자를 추출하기 위한 기준 위치가 된다.</span>

- 인자 타입열이 다르고 이름이 같은 함수를 여러 개 정의하는 것을 <span style="color: #44B444">중복 정의(Overloading)</span>라 한다.

- 인자 타입열과 함수 이름은 같지만 반환 타입이 다른 경우는 함수 중복 정의를 할 수 없다. 그 이유를 실제 사례를 들어서 설명하시오.

```c++
int Func(int arg){
  return arg;
}

double Func(int arg){
  return (double)arg;
}

void main(){
  Func(1);  // Error
}

// 위 코드를 실행햇을 때, 컴파일러는 어느 Func함수를 호출해야할지 모른다. 따라서 함수 이름과 인자 타입열이 같지만 반환 타입이 다른 경우는 함수 중복 정의를 사용할 수 없다.
```

- 다음 두 함수는 중복 정의가 되지 않는다. 그 이유를 설명하시오.

```c++
void Func(int arg);
void Func(const int arg);
```

> <span style="color: #44B444">만약 Func의 실인자로 a라는 1의 값을 가진 int형 변수를 전달한다고 가정하자. 그렇다면 a라는 변수가 직접 전달되는 것이 아닌, 실인자로 전달되는 것이기 때문에 a의 값인 1이 전달된다. 1은 상수이다. 따라서 Func(int arg)가 아닌 Func(const int arg)가 호출된다. 따라서 Func(int arg)는 전혀 쓰이지않게 되므로 존재 가치가 사라진다.</span>

> > <span style="color: #44B444">하지만 int\*와 const int\*를 매개 변수로 선언한다면, int\* 에는 int타입을 가리키는 포인터, const int\*에는 const가 한정된 변수를 가리키는 포인터로, 컴파일러가 함수 호출 시 실인자로 넘어가는 포인터가 가리키는 대상에 const가 한정되어 있는지를 통해서 구분할 수 있으므로 함수 중복 정의 관점에서 TYPE\*과 const TYPE\*은 다른 것으로 취급한다.</span>

- 다음 두 함수는 중복 정의가 되지 않는다. 그 이유를 설명하시오.

```c++
void Func(int* arg);
void Func(int arg[]);
```

> <span style="color: #44B444">함수의 매개 변수의 타입이 배열일 때, 해당 매개 변수는 배열의 맨 앞을 가리키는 포인터가 된다. 따라서 int\* arg과 int arg[]는 매개 변수로 쓰일 때 같은 타입이므로 같은 인자열과 같은 함수 이름이므로 함수 중복 정의가 불가하다.</span>

{1} ++a, a++과 같은 동작을 하는 함수 IncrementPrev, IncrementPost를 작성하시오.

```c++
정답

void IncrementPrev(int& arg) {
	++arg;
}

void IncrementPost(int& arg) {
	arg++;
}

void main() {
	int  a = 0;

	IncrementPrev(a);
	cout << a << endl;

	IncrementPost(a);
	cout << a << endl;
}
```

{2} 다음 프로그램의 함수 Absolute는 인자의 값을 절댓값으로 변환하는 함수이다. 출력 결과가 3, 5가 나오도록 Absolute를 작성하시오.

```c++
void main(){
  int a = 3;
  int b = -5;

  Absolute(a);
  Absolute(b);

  cout << a << endl;
  cout << b << endl;
}
```

```c++
정답

void Absolute(int& arg) {
	if (arg < 0) {
		arg *= -1;
	}
	else {
		arg;
	}
}
```

{3} 다음 프로그램의 출력 결과가 6, 3, 1, 0이 되도록 함수 Sum을 작성하시오.

```c++
void main() {
	cout << Sum(1, 2, 3) << endl;
	cout << Sum(1, 2) << endl;
	cout << Sum(1) << endl;
	cout << Sum() << endl;
}
```

```c++
정답

int Sum(int arg1 = 0, int arg2 = 0, int arg3 = 0) {
	int sum = 0;
	sum = arg1 + arg2 + arg3;
	return sum;
}
```

{4} 가변 인자의 합계를 구하는 Sum 함수를 작성하시오. (단, 첫 매개 변수는 고정 인자로서 가변 인자의 개수를 나타낸다.)

```c++
void main() {
	cout << Sum(5, 1, 2, 3, 4, 5) << endl;
	cout << Sum(3, 1, 2, 3) << endl;
	cout << Sum(1, 1) << endl;
}
```

```c++
정답

int Sum(int count, ...) {
	va_list arg_ptr;
	va_start(arg_ptr, count);

	int sum = 0;
	for (int i = 0; i < count; i++) {
		sum += va_arg(arg_ptr, int);
	}

	va_end(arg_ptr);

	return sum;
}
```

{5} 다음 프로그램과 같이 인자로 전달된 배열 요소를 출력하는 함수 Print를 작성하시오.

```c++
void main() {
	const int size = 7;
	int arr[10] = { 1,2,3,4,5,6,7 };
	Print(arr, size);
}
```

```c++
정답

void Print(int* arr, int size) {
	for (int i = 0; i < size; i++) {
		cout << arr[i] << endl;
	}
}
```

{6} 다음 프로그램과 같이 인자로 전달된 배열 요소의 순서를 뒤집는 함수 Reverse를 작성하시오.

```c++
void main() {
	const  int size = 7;
	int  arr[10] = { 1,2,3,4,5,6,7 };
	Reverse(arr, size);
	Print(arr, size);
}
```

```c++
정답

void Reverse(int* arr, const int size) {
	for (int i = 0; i < size / 2; i++) {
		int temp = arr[i];
		arr[i] = arr[size - 1 - i];
		arr[size - 1 - i] = temp;
	}
}
```

{7} 다음 프로그램과 같이 인자로 전달된 배열을 오름차순으로 정렬하는 함수 Sort를 작성하시오.

```c++
void main() {
	const int  size = 7;
	int arr[10] = { 7,1,3,5,6,2,4 };
	Sort(arr, size);
	Print(arr, size);
}
```

```c++
정답

void Sort(int* arr, const int size) {
	for (int i = 0; i < size; i++) {
		for (int j = i; j < size; j++) {
			if (arr[i] > arr[j]) {
				int temp = arr[i];
				arr[i] = arr[j];
				arr[j] = temp;
			}
		}
	}
}
```

# Chapter 9 Class

- 구조적 프로그래밍의 특징을 설명하시오.

  > <span style="color: #44B444">코드를 서브루틴과 블록으로 나누고 분기, 반복문을 사용함으로써 goto와 jump의 사용을 최소화하는 데 초점을 둔다. 그로 인해서 개발 생산성을 크게 향상시키는 데 기여한다.</span>

- 절차적 프로그래밍은 프로그램의 상태를 나타내는 데이터를 함수 호출에 의해서 변경하면서 처리하는 과정을 거친다. 이때 나타날 수 있는 절차적 프로그래밍의 문제점을 데이터와 함수 관점에서 설명하시오.
- > <span style="color: #44B444">함수의 인자로 부적절한 데이터가 전달되어 잘못된 처리가 수행되는 경우가 생길 수 있는데, 프로그램의 크기가 커질수록 복잡도가 증가하며 이러한 버그 발생 빈도가 높아진다. 또한 모든 프로그램이 조금씩 다른 처리를 하기 때문에 범용성있게 만든 함수라 하더라도 수정이 필요한 경우가 많아 코드의 재사용이 어렵다.</span>

- 객체 지향 프로그래밍에서 객체의 의미는 무엇인가?

  > <span style="color: #44B444">데이터와 명령의 결합</span>

- 객체 지향 프로그래밍의 장점을 두 가지 이상 제시하시오.

  > <span style="color: #44B444">1. 분업이 쉬워진다.</span>  
  > <span style="color: #44B444">2. 코드의 재사용 가능성이 높아진다.</span>  
  > <span style="color: #44B444">3. 각 클래스를 전문적인 개발자에게 맡길 경우 신뢰성이 높아지고 기능 확장도 쉬워진다.</span>  
  > <span style="color: #44B444">4. 각 클래스의 내부 동작을 몰라도 사용 방법을 안다면 부품처럼 조립하여 새로운 프로그램을 쉽게 만들 수 있다.</span>

- 클래스와 인스턴스 차이를 설명하시오.

  > <span style="color: #44B444">클래스는 여러 종류의 데이터와 해당 데이터를 처리할 수 있는 함수를 하나로 묶는 설계도라고 할 수 있다. 인스턴스는 클래스에 따라 메모리에 실제 생성된 객체를 말한다. 각각의 객체 멤버는 서로 다른 메모리를 점유하지만 멤버 함수는 동일하기 때문에 함수를 공유하게 된다.</span>

- C 언어 구조체 태그명과 C++ 클래스명의 차이를 비교 설명하시오.

- 클래스 멤버에 대한 접근 지정자는 <span style="color: #44B444">private</span>, <span style="color: #44B444">public</span>, <span style="color: #44B444">protected</span>가 있으며 생략할 경우 <span style="color: #44B444">private</span>이 된다.

- C++ 구조체의 멤버 접근 지정자는 기본이 public이다. 이유를 설명하시오.

  > <span style="color: #44B444">클래스의 경우 객체 지향 프로그래밍의 특징을 최대한 나타내기 위해서 기본값이 private이지만, 구조체의 경우 호환성을 지키기 위해 기본값이 public으로 설정되어있다.</span>

- 다음 프로그램의 잘못된 부분을 수정하시오.

```c++
class CTest{
  public:
  CTest() : m_C1(1){

  }
  const int m_C1;
  const int m_C2;
  const int m_C3;
};
```

```c++
정답

class CTest{
  public:
  CTest() : m_C1(1){

  }
  const int m_C1;
  const int m_C2 = 1;
  const int m_C3 = 1;
};

// 생성자에서 m_C1만 1로 초기화하고 있기 때문에 초기화되지 않는 m_C2와 m_C3를 초기화해주어야 한다.
```

- 클래스 멤버 함수에서 <span style="color: #44B444">this</span>키워드는 클래스 인스턴스의 포인터를 나타낸다.

- 다음 프로그램은 런타임 예외가 발생한다. 잘못된 부분과 이유를 설명하시오.

```c++
class CTest{
  public:
  int m_Value;

  void Show(){
    cout << m_Value << endl;
  }
};

void main(){
  CTest& pT  = NULL;
  pT->Show();
}
```

> <span style="color: #44B444">CTest의 객체 주소를 나타내는 pT가 NULL로 할당되며 사라졌다. 즉, 클래스 인스턴스의 포인터가 NULL이 된 것이다. 따라서 pT->m_Value에 접근하려 했지만 pT가 NULL이라 접근 가능한 메모리 영역이 아니므로 런타임 예외가 발생한다.</span>
>
> <span style="color: #44B444">여기서 알 수 있는 점은 숨은 인자로 넘겨진 객체의 주소(this)가 유효하지 않을 경우 잘못된 멤버에 접근하게 되며 그로 인해서 런타임 오류가 발생할 수 있다는 점이다. 이것을 반대로 해석하자면 멤버 함수에서 멤버에 접근하지 않는다면 숨은 인자로 넘겨진 객체의 주소(this)가 유효하지 않아도 문제가 없다는 것이다.</span>

- 비정적 멤버 함수와 정적 멤버 함수의 차이를 설명하시오.

  > <span style="color: #44B444">비정적 멤버 함수는 오직 클래스 객체를 기준으로 호출될 수 있다. 클래스 객체의 주소가 멤버 함수의 숨겨진 인자로 전달되고 그것을 통해서 함수 안에서 객체의 멤버에 접근할 수 있다.</span>
  >
  > <span style="color: #44B444">하지만 정적 멤버 함수는 클래스 객체를 기준으로 호출되지 않는다. 객체의 주소가 숨겨진 인자로 전달될 필요가 없으며 그로 인해서 함수 내부에서 this를 사용할 수도 없다. 따라서 정적 멤버 함수에서는 객체의 멤버에 전혀 접근할 수 없다. 한마디로 C++의 전역 함수와 같다고 할 수 있다. 정적 멤버 함수는 클래스 자체에 소속된다. 클래스 객체가 아닌 클래스 자체의 정보를 처리한다는 개념으로 클래스 소속 전역 함수를 정적 멤버 함수라고 부르는 것이다.</span>

- 다음 클래스 정의에서 잘못된 부분을 찾고 그 이유를 설명하시오.

```c++
class CTest{
  public:
  int m_Value;

  void Func(){
    cout << m_Value << endl;
  }

  static void SFunc(){
    cout << m_Value << endl;
  }
};
```

```c++
정답

class CTest{
  public:
  int m_Value;

  void Func(){
    cout << m_Value << endl;
  }

  static void SFunc(){
    // 정적 멤버 함수는 클래스 객체와는 상관없이 호출되므로 숨겨진 인자로 전달되는 인자도 없다. 그렇기에 함수 안에서 this를 포함하여 클래스 멤버를 사용할 수 없다.
    //m_Value를 사용하지 않던가 정적 멤버를 사용하도록 바꿔야 한다.

    // cout << m_Value << endl;
  }
};
```

- 다음 프로그램에서 잘못된 부분을 찾고 그 이유를 설명하시오.

```c++
class CTest{
  public:
  static void SFunc(){

  }
};

void main(){
  CTest t;
  t.SFunc();

  CTest* pT = &t;
  pT->SFunc();

  CTest::SFunc();

  SFunc();
}
```

> <span style="color: #44B444">클래스의 정적 멤버 함수를 사용하는 것이므로 클래스는 명시해주어야 한다. SFunc(); 코드만 쓰여진 행의 경우 클래스 명시가 되어있지 않으므로 컴파일이 불가하다.</span>
>
> <span style="color: #44B444">오래된 컴파일러의 경우엔 t.Func(); 코드와 pT->SFunc(); 또한 컴파일되지 않는데, 요즘 컴파일러에선 가능하다. 객체를 사용한다고 착각할 수 있는데, 기존 함수 호출 일관성을 위해 허용한 표기일 뿐이지, 객체로 보이는 t는 어떠한 영향도 주지 않는다.</span>

- 다음 클래스의 const 멤버 함수는 컴파일 오류가 발생한다. 컴파일 오류가 발생하지 않도록 수정하시오.

```c++
class CTest{
  public:
  CTest&  CFunc1() const{
    return *this;
  }

  CTest* CFunc2()  const{
    return this;
  }
};
```

```c++
정답

class CTest{
  public:
  const CTest&  CFunc1() const{
    return *this;
  }

  const CTest* CFunc2() const{
    return this;
  }
};

// 멤버 함수 앞에 const를 붙여 반환 타입이 변하지 않도록 한정한다. 이렇게 해야 컴파일러가 멤버 함수를 호출하며 반환 타입이 변하지 않는다는 것을 알고 안전하게 호출할 수 있기 때문이다.
// 컴파일러는 const 멤버 함수를 호출할 때 멤버의 변경이 가능한 상황이 있다면 const 멤버 함수를 호출하지 않으며 오류를 발생한다.
```

- 다음 프로그램의 출력 결과는 무엇인가?

```c++
class CTest{
  public:
  void Func(){
    cout << "General Function" << endl;
  }

  void Func() const{
    cout << "Const Function" << endl;
  }
};

void main(){
  const CTest ct;
  ct.Func();
}
```

> <span style="color: #44B444">Const Function</span>
>
> <span style="color: #44B444">Const 객체는 비 const 함수를 호출할 수 없다. 따라서 오로지 const 함수만 호출한다. 하지만 일반 객체의 경우, General Function을 호출한다. 하지만 비 const 함수가 정의되지 않았다면 const 함수를 호출한다.</span>

- 다음 프로그램에서 부모 클래스 CParent의 멤버인 m_Value의 값을 출력하도록 괄호 안을 채우시오.

```c++
class CParent{
  public:
  int  m_Value = 1;
};

class CTest : public CParent{
  public:
  int m_Value = 2;
};

void  main(){
  CTest t;
  cout << (       ) << endl;
}
```

```c++
정답

class CParent{
  public:
  int  m_Value = 1;
};

class CTest : public CParent{
  public:
  int m_Value = 2;
};

void  main(){
  CTest t;
  cout << t.CParent::m_Value << endl;
}

// 범위(::) 연산자를 사용하여 이름이 중복된 부모 클래스의 멤버 데이터를 지정할 수 있다.
```

{1} 다음 로봇 명세를 보고 프로그램을 작성하시오.
| 이름 | 신장(m) | 무게(T) | 마력 |
|------------ |--------- |--------- |------ |
| 태권브이 | 18 | 80 | 3000 |
| 마징가 | 17 | 70 | 2500 |
| 메칸더브이 | 20 | 90 | 3500 |
| 그랜다이져 | 22 | 100 | 5000 |

(1) 로봇을 나타내는 클래스 CRobot을 설계하시오. 명세를 입력할 수 있는 멤버 함수 Set과 명세를 출력하는 멤버 함수 Print가 있다.

```c++
class CRobot {
	string name;
	int height;
	int weight;
	int power;

public:
	void Set(string n, int h, int w, int p) {
		name = n;
		height = h;
		weight = w;
		power = p;
	}

	void Print() {
		cout << endl << "Name: " << name << endl
			<< "Height: " << height << endl
			<< "Weight: " << weight << endl
			<< "Power: " << power << endl;
	}
};
```

(2) 클래스 CRobot을 이용하여 모든 로봇의 명세를 출력하는 프로그램을 작성하시오.

```c++
int main() {

	CRobot robots[4] = {};

	CRobot t;
	t.Set("태권브이", 18, 80, 3000);

	CRobot m;
	m.Set("마징가", 17, 70, 2500);

	CRobot mk;
	mk.Set("메칸더브이", 20, 90, 3500);

	CRobot g;
	g.Set("그랜다이져", 22, 100, 5000);

	robots[0] = t, robots[1] = m, robots[2] = mk, robots[3] = g;

	for (int i = 0; i < 4; i++) {
		robots[i].Print();
	}
	return 0;
}
```

(3) 타입 정적 멤버 s_Value를 가지는 class CTest를 정의하고, s_Value에 1을 대입한 뒤에 출력하는 프로그램을 작성하시오.

```c++
class CRobot {
	static int s_Value;
	static void PrintS() {
		cout << s_Value << endl;
	}
};

int CRobot::s_Value = 1;

int main() {
  CRobot::PrintS();

	return 0;
}
```

(4) 다음 프로그램은 자정부터 지나간 초를 입력받은 후 시, 분, 초를 출력한다. 프로그램이 완성될 수 있도록 클래스 CTime을 작성하시오.

```c++
void main(){
  cout << "자정부터  지나간 초를 입력하세요"  << endl;

  int Elapsed;
  cin >> Elapsed;

  CTime t;
  t.SetElapesed(Elapsed);
  t.PrintTime();
}
```

```c++
class CTime {
	int elapsedTime;

public:
	void SetElapesed(int e) {
		elapsedTime = e;
	}

	void PrintTime() {
		cout << elapsedTime / 3600 << "시 "
			<< (elapsedTime % 3600) / 60 << "분 "
			<< (elapsedTime % 60) << "초 입니다." << endl;
	}
};
```

# Chapter 10 Constructor and Destructor

- 생성자와 멤버 함수의 차이점을 두 가지 이상 기술하시오.

- 생성자는 중복 정의를 할 수 있으나 소멸자는 오직 단 하나만 존재할 수 있는데, 그 이유를 기술하시오.
- 암시적 생성자가 컴파일러에 의해서 논리적으로 추가되는 경우를 기술하시오.

- 상속 관계 클래스에서 소멸자의 호출 순서는 <span style="color: #44B444"></span> 클래스 소멸자, <span style="color: #44B444"></span> 클래스 소멸자이다.

- 클래스 CTest 복사 생성자를 선언해보시오.

- 암시적 복사 생성자가 컴파일러에 의해서 논리적으로 추가되는 경우를 기술하시오.

- 암시적 복사 생성자는 블록 시작 전(선처리 영역)에 부모 클래스와 멤버 데이터 클래스의 <span style="color: #44B444"></span>를 호출한다.

- 다음 프로그램의 출력 결과는 무엇인가?

```c++
class CParent{
  public:
  CParent(){
    cout << "CParent Constructor" << endl;
  }

  CParent(const CParnet& obj){
    cout << "CParent Copy Constructor" << endl;
  }
};

class CTestA : public CParent{
  public:
  CTestA(){

  }

  CTestA(const CTestA& obj){

  }
};

class CTest B : public CParent{
  public:
  CTestB(){

  }
};

void main(){
  CTestA a0;
  CTestA a1 = a0;

  CTestB b0;
  CTestB b1 = b0;
}
```

- 다음 프로그램의 출력 결과는 무엇인가?

```c++
class CChild{
  public:
  CChild(){
    cout << "CChild Constructor" << endl;
  }

  CChild(const CChild& obj){
    cout << "CChild Copy Constructor" << endl;
  }
};

class CTestA{
  public:
  CTestA(){

  }

  CTestA(const CTestA& obj){

  }

  CChild m_C;
};

class CTestB{
  public:
  CTestB(){

  }

  CChild m_C;
};

void main(){
  CTestA a0;
  CTestA a1 = a0;

  CTestB b0;
  CTestB b1 = b0;
}
```

- <span style="color: #44B444"></span>는 컴파일러가 타입 변환 생성자를 사용하여 암시적 타입 변환을 수행할 수 없도록 지시하는 역할을 한다.

- 다음 코드의 출력 결과로 "CParent B"가 나오도록 CTest의 생성자를 수정하시오.

```c++
class CParent{
  public:
  CParent(){
    cout << "CParent A" << endl;
  }

  CParent(int arg){
    cout << "CParent B" << endl;
  }
};

class CTest : public CParent{
  public:
  CTest(){
  }
};

void main(){
  CTest t;
}
```

- 다음 코드의 출력 결과로 "CChild B"가 나오도록 CTest의 생성자를 수정하시오.

```c++
class CChild{
  public:
  CChild(){
    cout << "CChild A" << endl;
  }

  CChild(int arg){
    cout << "CChild B" << endl;
  }
};

class CTest{
  public:
  CTest(){
  }

  CChild m_Child;
};

void main(){
  CTest t;
}
```

- 다음 프로그램에서 초기화 리스트를 사용하여 m_Const는 1로, m_Ref는 m_Value로 초기화되도록 생성자를 수정하시오.

```c++
class CTest{
  public:
  CTest(){

  }

  int m_Value;
  const int m_Const;
  int& m_Ref;
};

void main(){
  CTest t;
}
```

{1} 다음 프로그램처럼 정수를 문자열로 바꾼 후 멤버 m_Str에 저장하는 클래스 CIntToStr를 타입 변환 생성자를 이용하여 작성하시오. (단, C 표준 라이브러리 함수인 \_itoa를 사용한다.)

```c++
void main(){
  char* str = CIntToStr(1).m_Str;
  cout << str << endl;
}
```

{2} 클래스 CPerson은 멤버 데이터로 이름(m_Name)과 ID(m_ID)를 갖는다. CPerson 객체가 다른 CPerson 객체로부터 복사되어 생성될 경우 이름에는 Copy를 붙이고, ID는 -1으로 만드는 클래스를 작성하시오.

```c++
void main(){
  CPerson p1("Bill", 1);
  CPerson p2 = p1;

  cout << p1.m_Name << " " << p1.m_ID << endl;
  cout << p2.m_Name << " " << p2.m_ID << endl;
}

// 결과값
// Bill 1
// Bill Copy -1
```

{3} 다음 프로그램에서 복사 생성된 CPerson 객체의 이름에는 뒤에 Copy를 붙이고, 부모 이름은 '유전자공학'으로 변경하고 싶다. 출력 결과가 다음처럼 나오도록 클래스 CParent와 CPerson의 부족한 부분을 완성하시오.

```c++
class CParent{
  public:
  CParent(){

  }

  char m_Name[16] = {0};
};

class CPerson : public CParent{
  public:
  CPerson(char* ParentName, char* Name){
    strcat(CParent::m_Name, ParentName);
    strcat(m_Name, Name);
  }

  char m_Name[16] = {0};
};

void main(){
  CPerson p1("광개토대왕", "장수왕");
  CPerson p2 = p1;

  cout << p1.CParent::m_Name << " - " << p1.m_Name << endl;
  cout << p2.CParent::m_Name << " - " << p2.m_Name << endl;
}

// 결과값
// 광개토대왕 - 장수왕
// 유전자공학 - 장수왕 Copy
```

{4} 다음 프로그램처럼 문자열을 인자로 받는 생성자를 가진 클래스 CLength를 정의하시오. (CLength의 멤버 함수 GetLength는 인자의 길이를 반환한다.)

```c++
void main(){
  CLength l = "abc";
  cout << l.GetLength() << endl;
}

// 결과값
// 3
```
