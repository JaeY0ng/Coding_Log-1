# 1. SW_Basic
``` 
* Network : 정보 교환을 위해 통신 장치를 연결한 통신망
1. LAN (Local Area Network) : 근거리 고속 통신망
2. WAN (Wide Area Network) : 원거리 (광대역) 안정적 통신망

* Internet : 전 세계적 통신망의 집합
* Protocol : 네트워크 통신을 위한 규칙 (문법 + 의미 + 순서)
* Network Model : 호환을 위한 통신망 제작 모델 / 문제 해결

* 부호 : 의미를 가지는 약속된 기호
* 신호 (Signal) : 부호가 특정 매개체를 이용해 전달되는 상태
 -전기 에너지, 통신망 필요
```

<br>

7 OSI 계층 (7/30)
----------
|7 OSI 모델|TCP/IP|역할|
|-|-|-|
|애플리케이션 + 프레젠테이션 + 세션 계층|애플리케이션 계층|APP 작업|
|전송 계층 |전송 계층|송신, 수진지의 데이터 신뢰성 확보|
|네트워크 계층|인터넷 계층|경로 탐색|
|데이터 링크 계층|Network Interface 계층|장치 간 데이터 전송 방식|
|물리 계층|Network Interface 계층|장치 연결, 신호 전달|

<br>

**1. OSI 물리 계층 : 신호 전달을 위한 물리적 연결**
 * 케이블 : 장치, 네트워크를 연결하는 물리적 매체로 데이터를 전송하는 전선 <br>
   -LAN Cable : UTP, FTP, STP
 * 리피터 : 신호 증폭, 재생
 * 허브 : 네트워크 장치를 연결하여 데이터 중계, 전송 -> 스위치로 대체

<br>

**2. OSI 데이터 링크 계층 : 장치간 운송방식 지정 -> 신뢰성**
 * L2 Switch <- 초기 이더넷 CSMA/CD의 충돌
 * 장치 식별 + 오류 제어 + 흐름 제어
 * LAN : Ethernet
 * WAN : HDLC, Frame-relay, PPP, ATM

<br>

**3. OSI 네트워크 계층 : 경로 탐색**
 * Router
 * IP : 기본 주소 (IPv4, Ipv6)
 * ICMP (Internet Control Message Protocol) : 통신 가능 여부 판단 (ex Ping)
 * ARP (Address Resolution Protocol) : MAC 주소와 IP 주소 연결
 * Routing Protocol : 최적 경로 탐색

 <br>
 
IPv4 (7/30 ~ 7/31)
----
* IPv4 통신방식 : Unicast, Broadcast, Multicast <br>
* 서브넷 마스크 : IP 지정 <br>
* 클래스풀 : IP를 규격화된 클래스로 구분하는 방식 = 10.12.31.0 / 24 -> 255.255.255.0 <br>
* 클래스리스 : 클래스 구분 없이 IP범위를 가변적으로 구현 = 10.21.31.0 / 8 -> 255.0.0.0  <br>
 1. A클래스 : 8비트 = 255.0.0.0 
 2. B클래스 : 16비트 = 255.255.0.0 
 3. C클래스 : 24비트 = 255.255.255.0
```
IP 주소 표현
IP : 10.5.4.9
서브넷 마스크 : 255.0.0.0
네트워크 IP : 10.0.0.0
사용 호스트 IP : 10.5.4.9
호스트 범위 : 10.0.0.1 ~ 10.255.255.254

서브넷 마스크 : 255.255.0.0
네트워크 IP : 10.5.0.0
사용 호스트 IP : 10.5.4.9
호스트 범위 : 10.5.0.1 ~ 10.5.255.255

서브넷 마스크 : 255.255.255.0
네트워크 IP : 10.5.4.0
사용 호스트 IP : 10.5.4.9
호스트 범위 : 10.5.4.1 ~ 10.5.4.254
```
 <br>
 
### Cisco 실습
1. 지정 IP 입력
2. PC, Router에 맞는 IP, 서브넷 마스크 입력
3. ICMP로 실행 확인

![353716662-dc55db80-cfc0-4086-b747-3477cf621ac8](https://github.com/user-attachments/assets/af429c20-9678-4879-be9c-b34a82547fe9)

 <br>
 
**Routing Protocol : 경로 탐색 (Router 간의 통신)**
* 정적 : 관리자가 직접 경로 설정 <br>
  -Static : 설정한 진행 방향 (목표 노드 / 서브넷 마스크 / 진행 방향 라우터 IP) <br>
  -Defualt : 모든 진행 방향 = 진행 방향이 하나인 말단 라우터 (0.0.0.0 / 0.0.0.0 진행 방향 라우터 IP) <br>
  
  ![353714928-16ab3bfb-05b7-419b-8eba-025ca8720f0c](https://github.com/user-attachments/assets/e102a9fa-9663-48da-b2d5-5b5fbc770cc9)
 
* 동적 (Distance Vector) : 전체 경로 학습 -> 자동 최적 경로 계산 <br>
   -AS (Autonomous System) : 자치 시스템 = 관리자가 관리하는 라우터의 집합
  1. IGP (Interior Gateway Protocol) -> RIP (Hop이 가장 적은 경로, Max = 15), EIGRP OSPF
  2. EGP (Exterior Gateway Protocol) -> BGP

 <br>
 
**Sever**
* DNS (Domain Name Service) : 문자 주소 + 숫자 주소 = www.(naver.com) + 223.130.200.236
* Web Service : 하이퍼텍스트 형식의 문서파일 제공 (Hyper Text Markup Language, Hyper Text Transfer Protocol) 

![353731743-607360c9-7f04-48f6-b979-14106ca91868](https://github.com/user-attachments/assets/1ae25c00-c4b7-4165-b7c0-9872d6ed05cc)

  
