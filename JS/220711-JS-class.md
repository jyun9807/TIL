# 220711 JS CLASS

# 오늘 배운 것

## Class
- 메모리를 효율적으로 관리하기 위해 생성
### 생성자 함수(prototye)
- 객체 데이터를 생성(인스턴스)
- new 연산자를 붙여서 실행
- 파스칼 케이스로 작명

### this 
- 일반 함수 : 호출 위치에 따라서 this를 정의
- 화살표 함수 : 자신이 선언된 함수 범위에서 this를 정의

### Es6 Classes
```
> 객체 데이터 내부에서 일반 함수를 사용할 때 :function 생략가능

class Test{
  constructor(인수, 인수){
    this.인수 = ''
    코드...
  }
  함수(){
    코드...
  }
}

```

### 상속(확장)
- extends
```
class 클래스{ this.-- = }
class 자식클래스 extends 클래스{
  constructor(){
    super() //부모 클래스를 실행하는 코드 
    this.- = - //기존 내용에서 더 추가된 코드 
  }
}
```

# 오늘의 생각
- 개념 정리가 더 필요
- 많이 보고 많이 사용해보자