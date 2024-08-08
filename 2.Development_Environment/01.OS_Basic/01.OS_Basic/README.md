### 01.OS_System
* OS (Operation System) : 하드웨어와 소프트웨어 사이의 인터페이스 운영 체제
* 커널 : 하드웨어와 소프트웨어의 통신 관리 시스템으로 리눅스의 핵심
* 환경 설정
   1. Visual Box 설치
   2. Ubuntu 설치
   3. Putty 설치

### Linux 명령어
```
[디렉토리 => 폴더]
* sudo : 관리자 계정 로그인
user1      // 일반 계정 로그인
sudo su    // 관리자 계정 로그인

* cd : 폴더 이동
[. : 현재 폴더, .. : 이전 폴더, / : 다음 폴더]
cd /              // root로 이동
cd ~              // home으로 이동
cd /home/ex2      // 절대 경로 : 어디서든 home -> ex2 폴더
cd ../ex1         // 상대 경로 : 현 폴더 -> 상위 폴더 -> ex1 폴더

* pwd : 현재 작업 경로 확인
pwd

* ls (list) : 파일, 폴더 목록 출력
[a : 모두, l : 자세히, R : 하위, d : 폴더]
ls -l               // 현재 폴더의 목록
ls -R /ex1          // ex1 폴더 하위 파일까지
ls -al ../home/ex2    // 현재 폴더 -> home -> ex2 모두 자세히

* mkdir (make directory) : 폴더 생성
[p : 현재 없는 상위 폴더도 생성]
mkdir /home/ex2/C  // home -> ex2에 폴더C 생성
mkdir A B C        // 현재 폴더에 폴더A, B, C 생성
mkdir /ex1/A/B     // ex1에 폴더A 생성 안에 폴더B 생성


* touch : 파일 생성, 생성 시점 변경
[d : 시간 변경, -t : 시각 변경]
touch 1 2                  // 현재 폴더에 파일1, 2 생성
touch /home/ex2/C/1        // home -> ex2 -> C에 파일1 생성
touch -d 12:12 ex1/A/2    // 현재 폴더 -> ex1 -> A -> 파일2의 시간 12:12로 변경
touch -t 202408070523 1    // 현재 폴더의 파일1의 시각 2024년08월07일05시23분00초로 변경

* cp (copy) : 복사
[r : 강제, 폴더, p : 보존]
cp /home/ex2
```







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
-soft : 커밋 취소, staging(add) 상태 유지 (head만 옮겨짐 = 작업 위치만 변경 = add 후 단계) -> 커밋만 하면 됨
-mixed : 커밋 취소, staging 취소, local 변경 상태로 유지 (add 전 단계로) -> add, commit 필요
-hard : commit 취소 staging 취소 , local 변경 초기화, 해당 시점으로 완전 롤백 -> 파일도 삭제됨


