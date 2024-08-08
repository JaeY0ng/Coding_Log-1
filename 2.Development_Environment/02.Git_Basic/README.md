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
git reset : 커밋 취소
-soft : 커밋 취소, staging(add) 상태 유지 (head만 옮겨짐 = 작업 위치만 변경 = add 후 단계) -> commit만 하면 됨 
=head만 옮겨짐. 시점 이후 commit만 취소
-mixed : 커밋 취소, staging 취소, local 변경 상태로 유지 (add 전 단계로) -> add, commit 필요 (Staging area까지 초기화)
=staging area 삭제. add, commit 필요
-hard : commit 취소 staging 취소 , local 변경 초기화, 해당 시점으로 완전 롤백 -> 파일도 삭제됨 -> file, add, commit 필요
=파일 삭제. file 제작, add, commit 필요하다

(soft : 커서 이동 -> commit : enter로 작성 완료 필요)

git reflog : reset 한거 복원

