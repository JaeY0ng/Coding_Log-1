### 01.OS_Basic
* OS (Operation System) : 하드웨어와 소프트웨어 간의 상호작용을 관리하는 운영 체제
* 커널 : 리눅스의 기반이 되는 UNIX OS

**환경 설정**
1. Visual Box 설치
2. Ubuntu 설치
3. Putty 설치
   
### LINUX 실습

```
* sudo su : 관리자 로그인
user1       // 일반계정 로그인
sudo su     // 일반계정 로그인 후 관리자 계정 로그인

* cd : 현재 위치 이동
cd ../home/user1     // 상대경로     . : 현재 디렉토리 
cd /home/user1       // 절대경로    .. : 전 디렉토리
cd /                 // 절대경로 Root
cd ~                 // 홈 디렉토리

* pwd : 현재 위치 확인
pwd         // 현재 작업 경로 확인

* ls : 목록 확인 (a : 모두, l : 자세히, R : 하위, d : 디렉토리)
ls -ls 자세히 보기
ls -al 모두 자세히 보기
ls -Ra 하위까지 모두 보기
ls -Rd 하위까지 디렉토리 보기

* mkdir : 폴더 생성 (p : 상위 디렉토리 자동 생성)
mkdir -p ex/ex1    // ex 자동 생성 -> 안에 ex1 디렉토리 생성
mkdir ex/ex1/ex2   // ex안의 ex1안에 ex2 디렉토리 생성

* touch : 파일 생성, 파일 변형 (d : 시간, t : 세부 시각)
touch 1 2 3             // 현재 위치에 1, 2, 3 파일들 생성
touch /ex/1             // ex안에 파일1 생성
touch -d 12:12 1        // 파일1 생성 시간 12:12로 변경
touch -t 202408071200 1 // 파일1 생성 시간 2024년 08월 07일 12시 00분 00초

* cp : 복사 (r : 디렉토리, p : 보존 상태로)
cp a /ex/A         // 파일a ex 안에 A 이름으로 복사
cp a /ex           // 파일a ex 안에 a (자동)으로 복사
cp /home/b ex/B    //home에 파일b ex안에 B로 복사
삭제 rm 
rm -rf ./* (현재 위치 파일 모두 삭제)

* mv : 이동
mv a /ex            // 현재 폴더의 a 파일 ex 폴더로 이동
mv /home/b /ex/B    // home 폴더의 b 파일 ex 폴더에 B로 이동

* rm : 삭제 (f : 강제)
rm A      // 파일 A 삭제
rm ./*    // 현재 폴더의 전체 삭제
rm -f ex  // ex 폴더 삭제

* cat : 문서 전체 출력 (n : 행 번호 추가)
cat a          // a 파일 전체 출력
cat -n /ex/B   // ex 폴더의 B파일 행과 출력

* head : 위에서 출력 (num : 숫자만큼 행 출력 / 기본 10줄)
head a
head -5 /home/B

* tail : 아래에서 출력 (num : 숫자만큼 행 출력 / 기본 10줄)
tail b
tail -9 ./A

* more : 창 사이즈 만큼 출력 (num : 숫자만큼 끊어서 보기)
more ex/ex1
more -13 /home/B
```

## ReDirection 
**리다이렉션 : 표준 입력, 출력을 파일로 제작**
```
* cat : 입력 모드 시작 (나가기 ctrl+c)

* > : 입력내용 백지 파일에 입력
cat > /home/ex/ex1    // 입력 내용 새로 ex1에 저장
ls -l > ./C           // 목록을 C에 저장

* >> : 입력내용 기존 파일에 입력
cat >> B              // 입력 내용 이어서 B에 저장

*파이프라인 (|) : 왼쪽의 명령어를 오른쪽으로 넘김
ls -la | cat -n | more   // 목록을, 행을 붙여서, 창 크기만큼 보기
```
