# 220711 JS 

# 오늘 배운 것

## javascript 
-  html, css를 역동적으로 사용하기 위해 탄생한 프로그래밍 언어
- ECMAscript 표준을 따라 개발되어 브라우저에 내장되어 있음
- 브라우저에서 js 개발/디버깅을 도와주기 위해 내장된 개발자 콘솔을 이용하기도 함.
- 코드라인을 ;으로 구분하나 사용은 선택이지만
- ;은 가독성과 예상치 못한 버그를 막기 위해 사용하기도 함

### 변수(vaiable) 
 - 하나의 값을 저장할 수 있는 저장공간, 변수명을 붙여서 접근한다.

 - var, let, const로 변수를 선언
 - var : 다시 선언이 가능하며 여러 차례 값을 대입할 수 있다.
 - let : 같은 이름으로 다시 선언을 할 수 없고, 대입으로 통해서 값을 변경할 수 있다. 
 - const : 한 번 값이 정해지면 변경할 수 없기에 같은 이름으로 다시 선언할 수 없어 대입이 필수이다.

 ### 자료형
 - 변수의 자료형은 고정되어 있지 않다.
 - 원시 타입/참조 타입

 - 원시 타입 : 값의 불변성, 값 자체가 변하는 것이 아니라 새로운 값을 변수에 할당하는 것.

    - String : 문자열
          - "",''(섞어서 사용 가능) 
          - template literals : `${문자열 내 js 코드 사용 가능}`
    - Number : 정수, 소수 표현
          - 특수 숫자값 : Infinity, NaN
          - 각 연산자는 숫자에만 사용할 수 있는 게 아니다!
    - Boolean : 참과 거짓
          - 비교 연산, 논리 연산 등에 활용
          - true (1) false(0)
    - Undefined
          - 변수를 선언만 하면 기본적으로 undefined 상태
    - Null
          - 값이 의도적으로 비어있음을 명시적으로 표현 
### 형변환

- Number(), +
- String(), '', `${}`
- Boolean(), !!

### 연산자 
- 연산 : 주어진 식을 계산하여 결과를 얻어내는 과정
- 연산자(operator) : 연산을 수행시키는 기호 
    - 항의 갯수나 자료형에 따라 동작이 달라질 수 있음
- 피연산자 = 향 =인수 : 연산자가 연산을 수행하는 대상
- 단항, 이항, 삼항 : 연산자가 필요로 하는 항의 개수

- 이항 연산자 : 두개의 항을 대상으로 = 대입 연산자를 사용하는 경우 왼쪽 피연산자에 오른족 피연산자의 값을 대입
모든 연산자는 반환 값을 가짐  

- + 단항 연산자 : 피연산자를 숫자 자료형으로 바꾸어 변환

- 거듭제곱 나머지 : ** %

- -, / : 피연산자를 형변환하는 역할을 포함하고 있다 피연산자를 숫자로 형변환 시킨 뒤 값을 계산

- 복합 대입 연산자(+=,-= 등)  : -+*/ %** 를 = 와 함꼐 사용하는 경우 복합 대입연산자를 사용하여 간결하게 표현 가능

- 증감 연산자 : ++ , -- 단항 연산자

### 연산자 우선순위

- 모든 연산자는 우선순위를 가짐
    -문자열은 알파벳 순 "a" < "b"

논리 연산자 (|| && !)
- && : false 표현식을 만나면 논리 연산을 종료하고 해당 표현식의 값을 반환

- || : 첫번째 true표현식을 만나면 논리연산 종료 해당 표현식의 값을 반환

typeof 
- 모든 연산자가 기호로 되어있진 않다
- typeof 라는 단항연산자는 우측 피연산자의 자료형을 반환
(null은 object가 아니지만 typeof  null은 object를 반환()

> !!(undefined) == !!(null) 요렇게 비교

### 조건부 연산자
유일하게 세개의 항을 필요로 하는 연산자

- 첫번째 항의 반환값이 True이면 2항
false이면 3항

- (조건) ? "참일 경우 실행" : "거짓일 경우 실행"


> 예약어(reserved word) : 프로그래밍 언어에서 기본적으로 역할을 가지고 있는 키워드