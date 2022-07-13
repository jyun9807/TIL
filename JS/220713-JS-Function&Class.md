# 220713 JS Function 

# 오늘 배운 것

## ECMAscript(=javascript)
- ECMA라는 기관에서 만든 표준화된 스크립트 프로그래밍 언어
- 여러 웹 브라우저 상에서 정상적으로 동작하게 하기 위해서 자바스크립트를 표준화하기 위해서 만들어졌다.

## Function
### - 기명 함수(함수 선언)
```
function 함수이름(매개변수){
  return ...//값을 반환, 함수종료
}

함수이름(인수) //함수 실행
```
### - 익명 함수 (함수 할당)
 
 함수 이름을 선언하지 않고 변수에 담아서 사용 

- arguments 객체 : 모든 함수 내에서 이용 가능한 배열 객체(인수 참조)

### - 화살표 함수
```
const test = (x) => {
  return
}

//다른 코드없이 단순 실행문만 있을 때 축약 가능
//인수값이 하나인 경우 () 생략 가능
const test = x => 실행문 

>객체 데이터를 반환할 시 ({객체데이터})
```
### - 즉시 실행 함수(IIFE)
```
코드 ;  //즉시 실행 함수 사용시 ;를 사용하여 코드를 구분

(function (){
  코드 입력...
})();

(function (){
  코드 입력...
}()); 
```
### 호이스팅
- 함수 선언부가 유효범위 최상단으로 끌어올려지는 현상
- 함수선언문에서만 호이스팅이 가능 

### 타이머 함수
- setTimeout(함수, 시간) : 일정 시간 후 함수 실행
- setInterval(함수, 시간) : 시간 간격마다 함수 실행
- clearTimeout() : 실행된 setTimeout함수 종료
- clearInterval() : 실행된 setInterval 함수 종료

```
const timer = setTimeout(function () {
  코드...
}, 시간)

const time = setInterval(() =>{
 코드...
}, 시간)

clearTimeout(timer)
clearInterval(time)
```
###  collback
- 함수의 인수로 사용되는 함수 
- 실행위치를 보장한다.

