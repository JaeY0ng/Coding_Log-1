# Git (8/8 ~ 8/13)  
**Git : 분산형 버전 관리 시스템의 일종 (file1.v1, file1.v2, file1.v3, ...)**
* Working Directory : PC 내에 Git 정보가 저장되는 작업 폴더 
* Staging Area : 임시 저장 공간 (commment를 추가해 Local로 전달 ->Head 이동)
* Local Repository : 최종 저장 공간 comment를 통해 파일을 구분하여 저장
* Remote Repository : 원격 저장 공간
* branch : 독립 작업을 위한 Repository 내에 파생된 저장 공간 (서로 병합 가능)
* Head : 작업 중인 부분
* 작업 폴더 -> Staging Area -> Local Repository <=> Remote Repository  

```
* cmd : working directory의 경로 창에서 cmd로 실행
cmd

* init : git 기초 파일 생성
git init    //workingdirectory 내 숨김폴더 생성

* branck : branch 확인, 추가
git branch
git branch ex    // ex branch 추가

* status : WorkingDirectory 내에 존재하지만, StagingArea에 없는 폴더 확인
git status

* add : WorkingDirectory의 파일 StagingArea에 추가
git add ex1

* commit : comment를 추가하여 LocalRepository로 이동
git commit -m v0.0 ex1    // -m : messagy

* log : LocalRepository의 파일+comment 확인
git log                 // 파일 상세 정보 확인
git log --oneline       // 파일명 + comment + 파일 번호 확인

* reset : LocalRepository의 파일 번호로 WorkingDirectory Rollback
git reset --soft b45aeq   // Local Repository에서 삭제 -> commit 필요
git reset --mixed b45aeq  // Staging Area에서 삭제 -> add, commit 필요
git reset --mixed b45aeq  // 파일 자체 삭제 -> 파일 제작, add, commit 필요

* reflog : reset된 파일 복원
git reset b45aeq         
```

**Merge**
```
* merge : branch간 병합
git merge ex            // 병합 받을 branch명

* merge --continue : 이어서 merge 진행
 1. conflict = 충돌 : 같은 문서명 내에 내용 겹침
 2. 충돌 파일 (ex1) 실행
 3. ex1 내용 수정
 4. git add ex1
 5. git merge --continue
 6. 다른 branch에서도 git merge master

* merge --abort : 강제 merge
```

Git hub
----------
* Git hub - Local Repository
  1. git hub -> New Repositories (Read me X, Public)
  2. WorkingDirectory 생성
  3. Directory 내 파일 하나 생성
  4. Directory 경로에서 cmd 실행
  5. git init
  6. git add *
  7. git commit -m [message]
  8. git branch -M main
  9. git remote -v                       // 연동된 원격저장소 확인
  10. git remote add origin HTTPS.URL    // 연결 추가 orign[이름] 경로
  11. git push -u origin                 // git hub에 내용 추가
  
* Eclipse -> Git
  1. Eclise
  2. File -> New -> Dyanamic Web Project (Test)
  3. Test -> Team -> Share Project -> 상단 Use or create 체크 -> 하단 Create Repository 체크 -> Project 체크 -> Finish
  4. Window -> Respective -> Open Respective -> Other -> Git
  5. Git hub -> 계정 Settings -> Developer Settings -> Personal access tokens (classic) -> repo 체크 -> Token (password) 발급
  6. Git Repositories -> 좌측 Test 옆 화살표-> Remotes -> Create Remote -> Change                          
     -> Git hub HTTPS URL, Git hub ID, token (Password) 입력 -> Save and Push         
  7. Push : Test -> Team -> Commit -> Add -> Commit Message -> Commit and Push

* Git -> Eclipse
  1. Git hub에서 Repository 생성 -> URI 복사
  2. 빈 Workspace 폴더 생성
  3. New -> Other -> Server -> Tomcat v9.0 -> Port 번호 부여 (8081)
  4. New -> Import -> Projects from Git -> Clone URI -> Local Destination : Workspace 경로
     
```
* push : 원격저장소에 저장
git add *
git commit -m [v0.1]
git push origin

* pull : 원격저장소의 정보 불러오기
git fetch origin
git pull origin       
```

Project
------------
* git hub1 : Project -> Todo에 작업 추가 -> Issue -> Convert to issue -> 좌측 Create a branch
* cmd : 폴더 경로에서 cmd 실행 -> git clone HTTPS -> 생성된 파일 내부 경로에서 cmd 실행                                            
              -> git switch [branch]로 git hub에서 생성한 것과 동일한 branch 생성 후 작업 (fetch origin -> checkout [branch])              
              -> 작업 -> add, commit -> git push origin
* eclipse : Team -> Swith to -> Others -> Remote -> Tracking -> 작업 -> Commit & Push
* git hub2 : Compare & Pull request -> merge -> close request -> 가급적 branch 삭제
