# 220707 Git branch

# 오늘 배운 것

## Branch
- 분기점을 생성하여 독립적으로 코드를 변경할수 있도록 도와주는 모델  

- 어떤 일을 하는지 설명할 수 있도록 이름 짓기

```
git branch // branch 확인

git branch -r // remote branch 확인

git branch -a // 모든 branch 확인

git branch [브랜치 이름] //생성

git switch [브랜치 이름명 // branch 이동

git branch -D [브랜치 이름] // 브랜치 지우기

git push -u origin [브랜치 이름] // 첫 push에는 -u를 사용 저장소 싱크를 맞춤
-u : upstream set

git fetch origin main 
// remote에 최신 데이터를 fetch_head(임시 브랜치)에 임시 저장 됐는지 확인 가능
//git merge FETCH_HEAD로 저장소 동기화를 해줌

git pull origin main 
//remote 최신 데이터를 local에 저장
//pull = fetch + merge 명령을 둘 다 실행
```
//원래 두 가지 일을 하다 버전 업 후 분리
- git checkout
    - git switch 
    - git restore

Pull : 따로 생성한 branch에서 작업한 것을 main branch로 보내는 것

Merge : main에서 branch 내용을 가져오는 것

----

<협업 시 발생할 수 있는 문제>
 Merge Conflict :
 내용을 수정하고 조합해서 그냥 저장하면 해결된다. 


----

`git commit --amend` : 최신 commit 내용 수정


remote(저장소)에서 일어난 일을 rocal로 당기기 위해서는 pull을 사용한다. pull을 사용하지 않으면 rocal과 remote간의 저장소 동기화가 되지 않아 push 에러를 만든다. 

<git flow 모델>

(hotfix) - main - (release) - develop - (feature)

- 각 단계가 명확하게 구분되지만 복잡하다. 

[git flow](https://danielkummer.github.io/git-flow-cheatsheet/index.ko_KR.html
)


```
git flow init; //flow로 개발 시작

//기능 개발 단계 
git flow feature start [이름] //commit까지만 진행함

git flow feature fininsh [이름] //finish 후 push 진행 
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
    - `$ git reset HEAD`
 
 - `git revert --no-commit HEAD 1~3`
    - 커밋 전으로 돌아감
    - --no-commit : 돌아간 커밋의 수만큼 메시지를 작성하지 않고 마지막에 작성할 수 있도록 함 

  - git restore [파일 이름] : 특정 파일 HEAD commit으로 복구
  - git restore --staged [파일 이름] : staging에 올라간 파일 내리기(add 전)

풀 리퀘스트 요청 시 :
develop인지 확인 후 요청

## 오늘의 생각
직접 만들어보는 게 더 이해하기 좋다. 
