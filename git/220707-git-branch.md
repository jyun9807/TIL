# 220707 Git branch

# 오늘 배운 것

<Branch>
- 분기점을 생성하여 독립적으로 코드를 변경할수 있도록 도와주는 모델
- 어떤 일을 하는지 설명할 수 있도록 이름 짓기

```
git branch // 기본 명령어 (생성)

git branch -r 

git remote //git remote 주소 등록

git remote -v

git branch -D [브랜치 이름] : 브랜치 지우기

```
첫 branch push 시에는 -u를 사용 //동기화 저장소 싱크를 맞춤


//원래 두 가지 일을 하다 버전 업 후 분리
git checkout => git switch //git 
             => git restore

Pull : 따로 생성한 branch에서 작업한 것을 main branch로 보내는 것

Merge : main에서 branch 내용을 가져오는 것

----

<협업 시 발생할 수 있는 문제>
 Merge Conflict :
 내용을 수정하고 조합해서 그냥 저장하면 해결된다. 


----

git commit --amend : commit 내용 수정



remote(저장소)에서 일어난 일을 rocal로 당기기 위해서는 pull을 사용한다. pull을 사용하지 않으면 rocal과 remote간의 저장소 동기화가 되지 않아 push 에러를 만든다. 

pull = fetch + merge 명령을 둘 다 실행

git fetch origin main  // fetch_head 임시 헤드 생성
fetch_head에 변경된 사항을 담아 둠.
//다시 merge를 통해서 저장소 동기화를 해줌

<git flow 모델>
(hotfix) - main - (release) - develop - (feature)

- 각 단계가 명확하게 구분되지만 복잡하다. 

[git flow](https://danielkummer.github.io/git-flow-cheatsheet/index.ko_KR.html
)

- 
```
git flow init; 

//기능 개발 단계 
git flow feature start [이름] //commit까지만 진행함

git flow feature fininsh [이름]
```

릴리즈 단계
```
git flow release start v0.1
git flow release finish v0.1

git push -u origin develop//

git switch main

git push origin main

git tag

git push --tags
```
<특정한 순간으로 돌아가기>

 - add한 상태, stage안에 있는 것을 내리고 싶을 때
 `$git reset HEAD`
 
 - git revert --no-commit

풀 리퀘스트 요청 시 :
develop인지 확인 후 요청

## 오늘의 생각
직접 만들어보는 게 더 이해하기 좋다. 
