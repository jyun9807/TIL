# 220704 CSS 배치

##오늘 배운 것

###Margin & Padding

 - margin : 테두리 외부 여백
 - padding : 테두리 내부의 여백

### 요소 배치
 - float, flex, grid

#### positon
 - absolute : 부모 요소를 기준
 - relative : 요소 자신을 기준
 - static : 기준 없음
 - fixed : 뷰포트 기준 
 
#### Float 
 - float : right, left /좌우 배치만 가능, 자기 자신에 대한 배치만 가능
 - 특정한 요소 왼쪽 홍은 오른쪽에 정렬하고자 할 때 쓰는 속성
 - 자연스러운 배치를 하고자 만들었다
 - 다음 요소가 줄바꿈이 도지 않는다(흐르는 속성)
 - 흐르는 속성은 clear : both, right left 로 제거한다. 

#### flex
 - display flex (정렬하고자 하는 요소들을 감싸는 부모 요소에 적용)
 - 특정한 요소들을 정렬하기 위해 쓰는 속성
 - 여러 요소들을 한 번에 배차할 수 있다.
 - flex는 내부 요소들은 모두 가로가 기본 정렬

##### justify-content
 - 메인 축이 기본적으로 가로이니 가로를 기준으로 정렬할 때 사용
 - center, flex-start, flex-end, space-between, space-around, space-evenly

##### align-items
 - 교차 축이 기본적으로 세로이니 세로를 기준으로 정렬할 때 사용
 - center, flex-start, flex-end, stretch, baseline
 - 부모 요소의 height가 내부 요소의 height 커야만 의미가 있다. 

##### flex-direction
 - flex-direction은 기본적으로 row로 설정, column으로 변경 가능

```css 중앙 정렬
display: flex;
align-items: center;
justify-content: center;
```

##### 자기 정렬(align-self)
 - 자기 자신을 교차 축으로 정렬하고자 할 때 쓰는 속성

##### 줄바꿈
 - flex-wrap, flex-flow, align-content

##### 순서 결정
 - order는 요소의 순서를 설정하기 위한 속성
 - 내부 요소에 설정
 - 기본 값은 0, 0에 가까운 값이 가장 앞에 위치하게 됨

#### grid
 - 복잡한 정렬을 위해 쓰는 속성
 - 격자 형태로 요소를 배치할 수 있도록 도와준다.
 - 정렬하고자 하는 요소들의 부모 요소에 적용해야 한다.

##### 정의
 - grid-template-colums: repeat(반복횟수, 지정 크기)
 - grid-template-row: 1fr 1fr 1fr //비율로 설정 가능
 - minmax(최소크기, 최대 크기)
 - auto-fill (개수 미정, 가로 행애 채울 수 있는 만큼 요소 채우기)
 - gap 간격을 정의하는 속성
----
#### 표현 단위
 - px : 픽셀
 - % : 부모 요소 크기를 기준으로 /상대적 백분율
 - em : 요소의 글꼴 크기 기준
 - rem : html루트 요소의 글꼴 크기 기준
 - vw : 뷰포트 가로 너비의 백분율
 - vh : 뷰포트 세로 너비의 

####색상 표현

 - 색상 이름 : 브라우저에서 제공하는 색상 이름
 - hex 색상코드 : 16진수 색상(hexadecimal colors) #000,#fffff
 - RGB 빛의 삼원색 rgb(255, 255, 255)
 - RGBA 빛의 삼원색 + 투명도 rgb(0, 0, 0, 0.5) 0~1

----

####box-sizing
요소의 크기 계산 기준을 지정
 - border-box : 요소의 내용 padding border 크기로 계산    
 - content-box : 내용으로 크기 계산

####overflow
요소의 크기 이상으로 내용이 넘쳤을 때 보여짐을 제어하는 단축 속성
 - visible: 넘친 내용을 그대로 보여줌
 - hidden: 넘친 내용을 잘라냄
 - auto: 넘친 내용이 있는 경우에만 잘라내고 스크롤바 생성

####display 요소의 화면 출력(보여짐) 특징
 - block 상자 요소
 - inline  글자 요소
 - inline-block 글자 + 상자 요소

####opacity 
요소의 투명도 1 불투명 0 투명

####글꼴 
 - line-height :  숫자 요소의 글꼴 ㅋ기의 배수로 지정
 - serif : 바탕체 계열
 - sans-serif  :고딕쳋 계열
 - monospace : 고정너비 글꼴 계열 가록폭이 동등
 - cursive : 필기체 계열 
 - fantasy : 장식 글꼴 계열

####요소 쌓임 순서(stack order)
어떤 요소가 사용자와 더 가깝게 있는지 (위에 쌓이는지 ) 결정

1. 요소에 position 속성 값이 있는 경우 위에 쌓임 static 제외
2. 1q번 조건이 같은 경우, z-index 속성의 숫자 값이 높을 수록 위에 쌓임
3. 1,2 번 조건까지 같은 경우 html 의 다음 구조일 수록 위에 쌓임
