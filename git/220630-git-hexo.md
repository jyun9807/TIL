# 220630 GIT&GIT BLOG WITH HEXO
# 오늘 배운 내용
- gitignore
- License 
- hexo를 이용해 github blog 운영해보기

----
####README.md
- 프로젝트와 repository를 나타내는 메인 문서
- 이 프로젝트를 얼마나 잘 이해하고 수행했는지 결과물은 어떤지 보여주는 문서

**기본적인 5가지 정보**
1. Projet Name
- 프로젝트를 설명하는 한 줄 요약을 꼭 적기
- 프로젝트의 데모나 샘플 링크를 남기는 것도 좋다!
2. Documents
- installation
- supported versions
3. More information 
- 참조 언어나 라이브러리 공식 페이지 혹은 책 등 참조한 문서를 기재
4. Contributing 
- 오픈소스 프로젝트일 경우 참조할 내용이나 문서를 명시
5. License
- 책임을 위한 것
- 프로젝트는 하나의 링센스만을 가짐
- 명시되지 않은 경우 확인 필 
	- MIT Licens : 모든 행동에 제약이 없이 자유롭게 사용할 수 있음
	- Apache license 2.0 : 특허권 내용이 포함되어 있음 자유롭게 써도 되지만 꼭 명시해야함! (기타 구체적 내용은 확인 필요)
	- GNU(general public license v3.0) : GPL 라이센스를 갖는 순간 무조건 이 규칙을 따라야함! 

####gitignore
- os idle 언어 라이브러리 등 저장소에 올리지 않을 것들을 list 하기 위한 것
- 임시 파일나 보안 상 중요한 것들을 선별한다.
- [gitignore 작성](https://www.toptal.com/developers/gitignore)
```
*.java // java 파일을 필터
server.* //server라는 이름의 파일을 필터
secret/** //secret 폴더를 필터
```

####hexo
- hexo는 Node.js 기반 정적인 블로그 생성기이다 
- node와 npm이 설치되어 있어야지 작동 가능하다

#####hexo 블로그 만들어보기
1. 초기 페이지를 작성해보자.
```
<!doctype html>
<html>
  <head>
   <meta charset="utf-8">
   <title>My first github page</title>
  </head>
  <body>
   <div id="main-wrapper">
    <h1>Home</h1>
    <p>This is home.</p>
    <a href="https://github.com/kingwangzzang1234/kingwangzzang1234.github.io">Visit this repository</a>
   </div>
  </body>
</html>
```

2. hexo를 설치하자
```
$ npm install -g hexo-cli
```
```
$ hexo init <folder>
$ cd <folder>
$ npm install
```
- _config.yml 파일을 확인할 수 있다.
- 위 파일의 deploy 수정 (주의 형식이 틀리면 deploy가 되지 않음)
```
deploy:
type: git
repo : <repo url>
branch : [branch]
```
  // 새 포스트 파일 만들기
$ hexo new post "post"
  // vim 으로 작업하기
$ vi source/_posts/post.md
  // local에서 확인하기 위한 파일 재생성
$ hexo clean && hexo generate
  // localhost:4000 에서 확인하기 위한 로컬서버 시작(종료할땐 ctrl+c)
$ hexo server
  // 문제없음을 확인한 후 repository에 업로드
$ hexo clean && hexo deploy
```

- 테마 변경
[thema](https://hexo.io/themes/)

- hexo 추가 정보를 위한 공식 page
[hexo](https://hexo.io/ko/)

- 이렇게 업로드 되는 github bloh 주소
	- {username}.github.io

**오늘의 시련(?)**
- node.js 설치 중 2502, 2503 설치 에러 발생
	- 관리자 권한 문제라는데 cmd를 권리자 권한으로 실행 후 설치 (해결)
- zoom 강의 도중 시스템 리소스 부족이나 인터넷 문제로 튕김
	- 인터넷을 바꾸거나 어떻게 잘 버티자(?)
	- 장비를 바꾸는 게 도움이 될 수 도
----
# 오늘 추가적으로 할 일
- 1주일 공부 정리 블로그 작성
- 내일 할 일 정하기 


# 오늘의 생각
항상 생각하지 못한 작은 에러들 때문에 진행이 안 돼
어쩌면 환경 설정이 제일 문제일지도..
