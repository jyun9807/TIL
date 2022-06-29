# 220629 GIT&GIT HUB START

# 오늘 배운 내용
- 기본 배경
- shell, vim command
- git for window
- repo 제작부터 push까지
- shell :운영체제의 커널과 사용자를 이어주는 소프트웨어 
***
**shell command**
 - pwd : 현재 위치/절대 경로
 - ls : 현재 디렉토리에 위치한 모든  파일 및 디렉토리  확인
 	- ls -a : 숨긴 파일까지 모두 확인
	- ls -l : line으로 세부 정보까지 확인
	- ls -al : -a, -l가 같은 기능
 - cd : 디렉토리 이동
 - mkdir : 디렉토리 생성
 - touch : 파일 생성
 - mv : 파일 이동
 - cp : 파일 복사
 - mv : 파일 이름 바꾸기, 파일 이동
 	- mv 파일이름 ./바꿀이름
 - rm : 파일 삭제 (rm -rf 지울폴더 : 폴더 삭제)
 - cat : 문서 내용 확인
 - vim : vim 열기
 -* : 전체를 의미

 **vim command**
 - ESC : normal 상태/ 명령 모드
 - `:set nu` : 라인 출력
 - :wq : 저장하고 종료
 - :q! : 종료(!는 오버라이드)
 - i : insert 모드로 변경
 - o, O : 커서를 밑, 위로 빈 행을 추가하여 입력
 
 - vim을 닫지 않고 종료한다면 이상한 문서(?) 뭔가가 생기는데 그때는 rm 건드린문서.swp 
 
 **git != github**
	- git : vcs 버전관리시스템
		-빠른 속도, 단순한 구조 
		-분산형 저장소 지원	
	- github : git을 이용한 웹서비스 

 **git command**
	- git clon {repo url} 
	- git status : 상태 확인
	- git add {filename} : 임시 저장
	- git commit : 임시 저장한 현 상태를 저장(스냅샷)
	- git push origin main : 깃허브 등 저장소에 저장

 **git commit**
	- 최소단위로 자주 동작하도록 할 것
	- 제목과 내용은 한 줄 공백으로 분리할 것
	- 제목은 50자 이내, 내용은 문장형으로 자세하게추가 설명
	- 팀의 작성 방식을 따를 것
	- commit의 의도와 구성을 충분히 하도록 작성
	
- Conventional Commits
	- commit 제목은 하나의 구나 절로 commit을 설명
	- importance of capitalize
	- prefix 꼭 달기 
		- feat : 기능 개발
		- fix : 오류 개선 혹은 버그 패치
		- docs : 문서화 작업
		- test : test 관련
		- conf : 환경설정 관련
		- build : 빌드 관련
		- ci : Continuous Integration 관련
		- 
 **git objects**
	- blob : 변경사항 (라인 단위)
	- Tree : blob의 메타데이터 

 **git flow**

# 오늘 추가적으로 할 일

 **practice(1)**
 	```
	~/Documents/dev
	 -cli-practice/
	   -bin/
	    -introduce.md
	    -README.txt
	```
	
	- $ mkdir cli-practice
	- $ mkdir cli-practice/bin
	- $ touch cli-practice/bin/README.txt
	- $ cp ./cli-practice/bin2/README.txt ./cli-practice/bin2/introduce.md
  
  - 루트 디렉토리에서 작업하는 것이 좋다길래 해보았으나 번거로워서 모르겠다 이것을 말한 것이 아닌가? practice 완료
 
 ---
 
 **practice(2)**
 
 
 <!-- 주석을 표기하는 것으로 자기소개라는 것을 알려주기 -->

## 간단한 자기소개

- 닉네임: jyun9807
        - 지금 하는 거 : 프론트엔드 개발
                - 현재 중요하게 생각하는 거 : js 공부

* 성별 : 표기하기 싫음
+ 그냥 마크업 여러 개 써보는 중

*자기소개 별 강조*

**자기소개 별별 강조 중**

~물결 강조~

_언더바 강조_

>인용하는 거니까 음  > '너 자신을 알라'

js로 code 강조 `console.log(hello)` 실험

```
let e = 'hello';
console.log(e);
```
아무튼 열심히 하자
***
정리도 잘 하고 블로그 운영도!
----

- 일단 해보았다...완료
	
 **practice(3)**
 
 	- repo 해보면서 commit 해보았으니 나중 프로젝트 때 정확하게 작성해보는 걸로 하자 
 
 **error message 확인**
 
 	```
 	 ! [rejected]        main -> main (fetch first)
	error: failed to push some refs to 'https://github.com/jyun9807/first-repo.git'
	hint: Updates were rejected because the remote contains work that you do
	hint: not have locally. This is usually caused by another repository pushing
	hint: to the same ref. You may want to first integrate the remote changes
	hint: (e.g., 'git pull ...') before pushing again.
	hint: See the 'Note about fast-forwards' in 'git push --help' for details.
	```
 -상황 : README.md 파일을 command로 실험(?)해보는 중에 아마 commit을 뭔가를 잘못 입력한 듯 함(코드에 의하면)
 
 -원인 : 원격 저장소와 local 저장소가 동기화 되어 있지 않는 상태
 	 기존 데이터 손실 우려 때문에 push를 막았다는 것.
 
 - 해결방안 
  	1. 해당 폴더 프로젝트를 삭제하고 다시 생성
  	2. $git push origin +main( + 이 방법을 실행함)
  		- 강제로 소스 전체가 push 되어서 기존 데이터 손실 위험이 있음
  		- 협업 시 다른 분의 소스 코드를 덮어쓸 위험이 있음
  	3. pull 등 여러 다른 방법이 있었으나 확인 불가, pull을 아직 잘 모름
  		- 추후 공부 및 만약 같은 오류가 생긴다면  
  		
  **오늘 아쉬운 점/이상한 점**
  
	- github 내에 token을 생성했으나 제시된 페이지를 찾을 수 없었고 따로 검색해야했다. 결국 사용할 일이 없었음 (찾아보자..)
	- 빠르게 강의 내용을 정리하고 작성해보도록 노력이 더 필요함
	 
# 오늘의 생각
 계속 노력하는 것이 익숙해지는 지름길
