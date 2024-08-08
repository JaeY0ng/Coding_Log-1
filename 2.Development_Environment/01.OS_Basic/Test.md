  cp 시험문제
  ```
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
  more
```
시험 표준 출력redirection

Virtual Box
