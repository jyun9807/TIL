#220629 GIT&GIT HUB START

##오늘 배운 내용
- 기본 배경
- shell, vim command
- git for window
- repo 제작부터 push까

- shell 
	-운영체제의 커널과 사용자를 이어주는 소프트웨어 

-shell command
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

-vim command 
 - ESC : normal 상태/ 명령 모드
 - `:set nu` : 라인 출력
 - :wq : 저장하고 종료
 - :q! : 종료(!는 오버라이드)
 - i : insert 모드로 변경
 - o, O : 커서를 밑, 위로 빈 행을 추가하여 입력
 
-git != github 
 	-git : vcs 버전관리시스템
		-빠른 속도, 단순한 구조 
		-분산형 저장소 지원
	-github : git을 이용한 웹서비스 

-git command 
	- git clon {repo url}
	- git status
	- git add {filename}
	- git commit 
	- git push origin main

-git commit 
	- 최소단위로 자주 동작하도록 할 것
	- 제목과 내용은 한 줄 [[O공백으로 분리할 것
	- 제목은 50자 이내, 내용은 문장형으로 자세하게추가 설명
	- 팀의 작성 방식을 따를 것
	- commit의 의도와 구성을 충분히 하도록 작성
-Conventional Commits
	- commit제목은 하나의 구나 절로 commit을 설명
	- importance of capitalize
	- prefix 꼭 달기 
		- feat : 기능 개발
		- fix : 오류 개선 혹은 버그 패치
		- docs : 문서화 작업
		- test : test 관련
		- conf : 환경설정 관련
		- build : 빌드 관련
		- ci : Continuous Integration 관련
-git objects
	-blob : 변경사항 (라인 단위)
	-Tree : blob의 메타데이터 

-git flow

#오늘 할 일
practice(1), practice(2), practice(3), error message 확인
#내일 할 일
