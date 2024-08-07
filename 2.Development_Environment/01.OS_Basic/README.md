### 01.OS_Basic
* LINUX (Ubuntu)
  - 오픈 소스
 
  ```
  cd home/user1     // 상대경로
  cd /home/user1    // 절대경로

  경로 : / = root (최상위 공간)
  /root (root사용자의 home directory)
  / 와 /root는 다름 (최상위 공간, root사용자의 home directory)

삭제 rm 
rm -rf ./* (현재 위치 파일 모두 삭제)

  cp 시험문제
  문제2. 5중3개
  1.
  ls -l /etc/login.defs /etc/passwd /boot/grub/grub.cfg
  mkdir /backup
  cp /etc/login.defs /etc/passwd /boot/grub/grub.cfg /backup
  2.
  cd /backup
  mkdir test
  cp ./grub.cofg test/grub
  cp ./login.defs test/login
  cp ./passwd test/pass
  3.
  touch /backup/test1 /backup/test/test2
  4.
  mkdir -p /home/test/c/d
  cp -rp /backup/test /home/test/c/d/linux  (r:디렉토리 복사, p:보존 복사)
  5.
  cd /home
  cp -p /backup/grub.cfg /backup/login.defs /backup/passwd /backup/test1 /home/test/c/d/linux

  cat 시험문제
  head&tail 시험문제
  
Virtual Box
