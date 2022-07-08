# 220708 GIT ORGANIZATION

# 오늘 배운 것

## 협업 과정 (팀원편)

## git flow

- main/master : 사용자가 사용하는 브랜치
- develop : 개발자가 사용하는 브랜치
- release : 출시 준비 브랜치
- hotfix : 출시 전 버그 수정(긴급)

### 1. fork를 이용하여 작업
- `git clone [개인 로컬 저장소 생성 주소]
- 작업을 위해 issues 생성

### 2. git flow init
- git flow 저장소 생성
- 자동으로 develop 브랜치로 이동
- git flow 설정이 자동으로 이뤄짐

### 3. git feature start [브랜치 이름]
- feature [브랜치 이름] 를 생성한 후 자동으로 이동
- 개발 시작

### 4. git 작업
- feature 브랜치 내에서 작업 후 add, commit

### 5. git feature finish [브랜치 이름]
 - develop 브랜치에 feature 브랜치를 자동으로 병합
 - 자동으로 feature 브랜치는 삭제

### 6. git push origin develop  
 - 첫 push에는 -u를 붙여 진행

### 7. github 내 내용 전달 
- compare & pull request 클릭 후 본인의 develop 브랜치에서 팀장의 develop 브랜치인지 확인 후 진행

### 8. 팀장 confirm 후
- 수정할 부분이 있다면 수정 후 각각 commit
- `git push origin develop` 다시 진행

### 9. 팀장이 승인 후 Merge pull request 완료
 - 수정된 develop을 pull 진행

### 10. remote
 - 앞서 pull를 진행하기 위해서는 remote 진행 필요
 
 ```
 git remote

 git remote add upstream [팀 레포 주소]
 
 git remote -v //확인

 git pull upstream develop // 내용 가져오기
```

### 11. 마침
 - github와 local 저장소를 확인해보고 동기화 완료되었다면 다음 작업 다시 반복!

 ----
 - origin과 upstream 
    - upstream : 포크한 원본 저장소 
    - origin : 원본 저장소를 복제한 본인의 저장소 


#### 협업 과정에서 오류
- 팀장이 push를 못하는 경우가 발생
    - 동기화 문제인 거 같아 pull을 진행함
    - 장비 과부하로 다음에 하기로 함. (07.11 예정)

- 팀장의 clone 여부가 논의 되었는데 팀장의 오류가 clone을 하지 않은 것으로 추측됨.

주의할 점 
- 팀장은 git pull origin develop
- 팀원은 git pull upstream develop