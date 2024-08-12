# 01.OS_System (8/7 ~ 8/8)
* OS (Operation System) : 하드웨어와 소프트웨어 사이의 인터페이스 운영 체제
* 커널 : 하드웨어와 소프트웨어의 통신 관리 시스템으로 리눅스의 핵심
  
**환경 설정**
* Visual Box (version 7) 설치
  1. 어댑터에서 VMware 모두 끄기
  2. 파일 -> 도구 -> 네트워크 관리자 -> adapter2 추가 (IP 할당)
  3. 정처산기 LINUX 실행
* Ubuntu 설치
* Putty 설치

### Linux 명령어
```
[디렉토리 = 폴더]

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
cp -p ./ex2 /ex
cp -r /home /ex
cp -f /home/ex1 ex2 /ex      // 마지막 경로로

* rm (remove) : 삭제
[f : 강제 r : 폴더]
rm 1 2
rm /ex/3
rm -f ./*      // 현재 폴더의 모든 파일

* cat : 문서 (내용) 전체 출력
[n : 행 번호 추가]
cat /home/1
cat -n ex

* head & tail : 위 & 아래에서 부분 출력
[num : 출력할 행 수 / 생략 -> 10줄]
head ex1
head 8 /home/1
tail ./3
tail 3 /ex/ex1

* more : 창 크기만큼 출력
[num : 한 페이지의 행 수 / space바 누르면 다음 페이지]
more /home/ex1
more -15 ex1
```
### ReDirection
**리다이렉션 : 표준 입력 & 출력을 파일로 대체**
```
* cat (> or >>) : 사용자가 키보드 입력
[탈출 : ctrl+c]

* > : 파일 생성, 기존 파일 덮어쓰기
cat > ex - hello
ls -l cat > ex1

* >> : 파일 생성, 기존 파일에 추가
cat >> ex2 - Example
cat c
tail -3 c >> ex3
```
권한
----
* 소유권 : 파일, 폴더를 소유할 사용자 권한
* 허가권 (permission) : 파일에 접근할 권한
* r : Read = 4
* w : Write = 2
* x : eXcute = 1
*  **drwx-rw---x -> d/rwx/rw-/--x**
   1. d : 파일의 타입 (d = directory)
   2. rwx : 소유자
   3.  rw- : 소유 그룹
   4.  --x : 게스트 사용자 (other)
   5. ls -l로 권한 확인 가능
```
* useradd : 사용자 추가
useradd user1 : user1 추가
passwd user1 : user1 비밀번호 설정

* chown : 소유권 변경 = 사용자에게 권한 부여
chown user1:user1 /ex    // 소유자, 소유그룹변경
chown .root /ex          // 소유그룹변경
chown -R user1.user1 /ex // 하위파일, 폴더 포함 변경

* chmod-numeric : 숫자로 허가권 변경
[rwx의 숫자를 더 해서 표현]
chmod 755 ex    // 4+2+1, 4+1, 4+1 = rwx, rx-, r-x
chmod 421 ex    // 4, 2, 1 = r--, -w-, --x
chmod 376 ex    // 2+1, 4+2+1, 4+2 = -wx, rwx, rw-

* chmod-symbolic : 문자로 허가권 변경
[u : 소유권자, g : 소유그룹, g : other, a : 모두, +- : 허가, 불허]
chmod u-rw ex
chmod g+w ex
chmod a-x, u+r ex

* ps -e : 핑 확인
ps -elf

* kill : 연결된 IP 강제 종료
kill eqd12r

* nice : 연결 우선 순위 (PRI) 변경
[기본 80 +- = PRI : 낮을 수록 높음]
nice -n -10 ping 127.0.0.1
```
