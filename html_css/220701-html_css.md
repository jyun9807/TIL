# 220701 HTML&CSS 

# 오늘 배운 것

## 프론트엔드 개발
HTML,CSS,JS를 사용해서 데이터를  사용자 인터페이스로 변환한 후 사용자와 상호작용할 수 있도록 하는 것.

- 웹 페이지를 본다는 것은 HTML 파일을 보는 것. 해당 페이지가 가진 html,css,js, v파일이 순간적으로 다운로드 되는 것
- 웹 사이트에 접속(request : 요청) 

## html
- Hyper Text Markup Language
- 요소를 어떻게 보여줄지생각하여 웹의 구조를 구성
- `<태그>내용</태그>` 

### 기본 태그
각 태그의 이름은 어떤 용도로 작성된 것읨을 명시
- `<!DOCTYPE html>` : 해당 문서가 html 문서임을 알려줌
- `<head>` : 문서의 틀 정의, 파일 연결
- `<body>` : 문서 작성함
	- div 태그 : 요소를 구분(사용 빈도 높음) 
	- p 태그 : 문단을 표현(글 쓸 때 기본)
	- h 태그 : 제목을 표현 (1~6)
	- strong, b 태그 : 글자를 강조하기 위해 사용(strong : 매우 중요할 때 사용)
	- em, i 태그 : 글자 기울이기 (em : 강조하고 싶을 때)
	- hr 태그 : 가로줄 표시, 주세가 분리될 때 확실하게 강조하기 위해서 사용
	- br 태그 : 줄바꿈을 위한 태그
####심화 태그
- a 태그 : 하이퍼링크, href에 주소를 명시해야함
- img태그 : src에 이미지 파일명이나 주소를 명시 
- input태그 : 사용자로부터 글자 등을 입력받기 위해 사용하는 태그
  - type을 통해 어떤 요소를 입력받을지 명시
  - type 종류 : button, checkbox, date, file, radio 등
- form : input 태그를 모아서 하나의 입력 양식을 만들기 위한 태그
- ol 태그 : ordered list, 순서대로 정렬된 목록을 표시
- ul 태그 : 순서없는 목록을 표시
  - li 태그 : 목록 태그 내부에 사용하는 태그

### 시맨틱 태그(Sementic Tag)
태그 자체만으로 안의 내용을 유추할 수 있도록 작성되는 태그

1. 검색엔진최적화
2. 시각장애인 분들이 편리
3. 개발자 간 명확한 의사 전달

- HTML 문서를 작성할 때 추천하는 전체적인 구조
`header 태그` : 사이트 제목 표시
`nav 태그` : 사이트 메뉴 표시
`main 태그` : 사이트 본문 표시
`section 태그` :사이트 특정 부분 제목 표시
`article 태그` : 세부 주요 글표시
`aside 태그` : 보조적인 글 표시
`footer 태그` : 관련 출처 등의 정보 표시

![구조](/uploads/1848994ad25765da30fa8ef3/uploads/1848994ad25765da30fa8ef3684c67bc/캡처.PNG684c67bc/캡처.PNG)


## css
- Cascading Style Sheets
- 요소를 어떻게 표시될지 자세하게 정의하기 위한 스타일 시트 언어
- 선택자{속성:값;}

#### 선택자 
css를 어디에 적용할 지 명시해주는 것
- class(.): 스타일을  여러개의 요소에 적용하고 싶을 때//정할 때 -을 이용
- id(#): 스타일을 한 가지 요소에만 적용하고 싶을 때// 정할 때 카멜 방식을 이용

#### 문법
1. 글자
- color: 글자의 색상 지정
- font-size: 글자의 크기 지정
- font-weight: 글자의 굵기를 지정
- font-family: 글자의 폰트를 지정
- line-height: 줄간격을 지정
- line-spaing: 자간을 지정
- text-align : 텍스트 정렬 방식을 지정
2. 표시(display, visibility)
- display : 요소의 표시 방식 설정
  - inline, block, none, inline-block(내부 block, 외부 inline)
- visibility : 요소의 표시 여부
   - visible, hidden
3. 크기
- width(가로), height(세로)
- 사용단위
  - 절대단위: px(픽셀) //현업에서는 사용하지 않는 것이 원칙
  - 상대단위: %, vw/vh
4. 위치
- position: 요소의 위치를 어떻게 배치할지 지정
  - static, fixed, absolute, relative(화면 전체 맥락 요소들과의 관계 고려x)
- border : 테두리 지정
  - style, width, color. radius
- margin, padding

![box-model](img width="240" alt="box_model" src="https://user-images.githubusercontent.com/91234001/176929357-eb6577b1-5522-45bd-b450-dfde864b249f.png")

  - margin: 요소의 border 기준으로 외부에 여백을 지정
  - padding: 요소의 border 기준으로 내부에 여백을 지정
