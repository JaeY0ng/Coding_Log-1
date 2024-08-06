# 2. MiddleWare Basic (8/1 ~ 8/2)
```
* HardWare : PC의 부품    
* SoftWare
 1. System Software : WindowOS, Linux, macOS
 2. Application
```
* **MiddleWare : 하나의 시스템에서 앱을 동시에 실행, 연계시켜도 안정적으로 실행 가능 (Hardware + Software)**

**미들웨어 주요 기능**
* IT 자원 관리 : IT 자원의 성능과 가용성 관리
* 서비스 플랫폼 : 통합 환경에서 다양한 서비스 사용
* 네트워크 보안 : 연결된 호스트의 정보 보호
* 분산 시스템 : 물리적으로 분산된 환경을 하나의 시스템처럼 사용
|IT 자원 관리|서비스 플랫폼|네트워크 보안|분산 시스템|
|-|-|-|-|
|시스템 관리|IoT|네트워크 접근 제어|웹 앱 서버|
|SW 실행 관리|클라우드|보안 통신|연계 솔루션|
|네트워크 관리|UI/UX|침입 방지|실시간 처리|
|IT 서비스 관리|CND|사고 대응|TP 모니터|
|||보안 관리|분산 병렬 처리|


   
### JDK (Java Development Kit) 미들웨어 환경 설정
---------------------------------------------

1. JDK 설치 (11 version)
   1. 파일 C 드라이브로 이동
   2. 해당 폴더 환경 변수 설정 (sysdm.cpl)
3. Tomcat 설치 (9 version - Service Installer)
   1. JDK 위치 연동
   2. Login : admin / 1234
   3. 마지막 체크 박스 : Run Apache Tomcat, Show readme 해제
5. Eclipse 설치 (Java and Web Developers package)
   1. Preferences -> Workspace, CSS files, HTML files, JSP files Encoding == UTF-8 (유니코드) 확인
   2. File -> New -> Other -> Server -> Tomcat -> 하단 Server에서 Run
   3. Tomcat Server 실행 -> 실행 중인 파일 더블 클릭 -> Overview -> Port Number 할당
   4. File -> New -> Dynamic Web Project (Ex00) -> Target Runtime : Apache Tomcat
   5. Ex00 -> src -> webapp -> index.html 파일 생성 -> body 변경 -> Run As (Server)
   6. Ex00 -> Properties -> Java Built Path -> Tomcat 여부 확인
                         -> Facets -> Java 11로 변경, Runteimes Tomcat 선택      
                         -> Server Tomcat 선택               
   7. Ex00 -> src -> webapp -> WEB-INF -> lib -> (Tomcat 설치 경로 -> Tomcat 9.0 -> lib의 jsp, servlet 파일 복사) -> 붙여넣기
   8. Ex00 -> src -> webapp -> index.jsp 파일 생성 -> body 변경 -> Runs As (Server)


### DBMS 환경 설정

1. MySQL 설치 (community-window version)
   1. MySQL Installer -> MySQL Server 다운로드
   2. MySQL Installer -> MySQL Workbench 다운로드
