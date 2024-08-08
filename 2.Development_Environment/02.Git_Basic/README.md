Git : 분산형 버전 관리 시스템의 일종 (file1.v1, file1.v2, file1.v3, ...)



git hub
git download
원한는 workingdirectory 생성
파일 경로에서 cmd -> git init -> 해당 폴더에 .git이라는 숨김폴더 제작
git status 폴더 내에 공유? 되지 않은 파일 확인
git add ex.txt : 추가
git add * 
git status 재확인하면 추가돼 있음
git commit -m "V1.0 b.txt added" : 내 git hub에 메시제 추가   //"V_._"은 롤백(reset)에 사용
git log : 작업 로그
git log --oneline
git reset : 커밋 취소
-soft : 커밋 취소, staging(add) 상태 유지 (head만 옮겨짐 = 작업 위치만 변경 = add 후 단계) -> commit만 하면 됨 
=head만 옮겨짐. 시점 이후 commit만 취소
-mixed : 커밋 취소, staging 취소, local 변경 상태로 유지 (add 전 단계로) -> add, commit 필요 (Staging area까지 초기화)
=staging area 삭제. add, commit 필요
-hard : commit 취소 staging 취소 , local 변경 초기화, 해당 시점으로 완전 롤백 -> 파일도 삭제됨 -> file, add, commit 필요
=파일 삭제. file 제작, add, commit 필요하다

(soft : 커서 이동 -> commit : enter로 작성 완료 필요)

git reflog : reset 한거 복원

branch
-기본 master branch
git branch : 확인
git branch dev : dev branch  추가
git switch dev : 작업 branch dev로 바구기
타브랜치에서 한 작업은 인식 불가 -> 파일 안보임, log의 head 위치로 확인 가능

git merge dev : 작업 병합
master에서 dev로 넘어감 -> dev에서의 작업을 master는 모름
-> master로 넘어가서 git merge dev 하면 병합됨
conflict
dev에서 병합 시도 -> conflict -> 수정 -> add -> git merge --continue
feature에서도 병합해주기 git merge dev


git hub 연동
작업 폴더에 txt 파일 생성
git hub -> new repositories (readme 없이, public)
main에 있는 그대로 cmd에 입력 (https version)
입력 후 cmd에 뜬 upstream 문구 입력
-> git hub 로그인 창 생성됨
-> 새로고침
-> cmd 작업 후 git push origin (올리기)
-> git hub 작업 후 git pull origin


or


new repositories (readme랑 같이)
-> https 링크 복사
-> 작업 폴더 가서 cmd
-> git clone https://github.com/100chun/git_test2.git
-> cmd 작업 후 git push origin
-> git hub 작업 후 git pull origin
