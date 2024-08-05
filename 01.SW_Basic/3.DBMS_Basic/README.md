# 3. DataBase (8/2 ~ 8/5)
```
* Database : 데이터의 저장소
* Schema : DB의 구조를 전반적으로 기술한 것 - 외부, 내부, 개념
* DBMS (DataBase Management System) : DB를 관리, 운영하는 소프트웨어 / 대부분 관계형 DBMS 형태  
* SQL (Structured Query Language) : 관계형 DB에서 사용되는 언어
* 지식 피라미드 : Data -> Information -> Knownledge -> Wisdom
```
### CRUD
* DDL (Data Definition Language) : 정의어로 데이터의 구조, 골격 - Create, Alter, Drop, Truncate
* DML (Date Manipulation Language) : 조작어로 데이터의 값 - Select, Insert, Update, Delete
* DCL (Date Control Language) : 권한 부여 - Grant, Revoke
* TCL - Commit, Rollback
  
### DDL
```
* cmd 로그인
mysql -u root -p [-port ____];    // mysql -user 계정 -password -port 8125 [port 번호 변경 시]

* use : DB 위치 지정
use mysql;
use dbex; 

* show : 조회
show databases;
show tables;

* desc : 세부 구조 조회
desc tbl_ex1;

* create : 생성
create database dbex;
create table tbl_ex;
create table tbl_ex1(
-> ex1_name varchar(10) primary key,     // varchar() : string,       primary key : 기본키 (not null)
-> ex1_addr varchar(1024) null,
-> ex1_age int not null);

* drop : 삭제
drop database dbex1;
drop table tbl_ex;

* alter : 변경 (add-삽입, change-수정, drop-삭제)
alter table tbl_ex1 add column ex1_year int null [after ex1_addr];      // [after ex1_name] 삽입할 column 위치
alter table tbl_ex1 change column ex1_addr ex1_address varchar(1024) null;
alter table tlb_ex1 drop ex1_year;
```

### DML
```
* select : 값 확인
select * from tbl_ex1    // * : 모든 열

* insert : 값 삽입
insert into dbex.tbl_ex1 values('홍길동', '대구 반월당', '23');
insert into dbex.tb1_ex1 values(ex1_name, ex1_age) values ('남길동', '23');

* update : 값 수정
update tbl_ex1 set ex1_age='30';                                    // 모든 ex1_int 값 30로 일괄 변경
update tbl_ex1 set ex1_addr='경북 구미시' where ex1_name='홍길동';  // ex1_name=홍길동인 row의 ex1_addr만 경북 구미로 변경

* delete : 값 삭제
delete from tlb_ex1 where ex1_addr='경북 구미시';                   // ex1_addr=경북 구미시가 포함된 row 값 모두 삭제      
```

### DCL
```
* grant : 계정 추가
create user user1@localhost [identified by port]    // 로컬 계정
create user user2@'%'                               // 외부 접근 계정

* drop, delete : 계정 삭제
drop user user1@localhost
ddelete from user where user='user2'

* grant : 권한 부여
grant * on dbex.* to user1@localhost               // dbex의 모든 테이블에 대한 모든 권한 부여
grant select, insert on dbex.* to user2@'%'        // dbex의 모든 테이블에 대한 select, insert 권한 부여

* show : 권한 확인
show grants for user1@localhost
show grants for user2@'%'

* revoke : 권한 제거
revoke all on dbex.* from user1@localhost

* flush : 권한 새로고침
flush privileges
```
<br>

**계정 생성**     
![DCL](https://github.com/user-attachments/assets/93c9d39f-d134-41de-a759-1f54c1d42d78)

<br>

**외부 접근**     
![DCL2](https://github.com/user-attachments/assets/64f21771-d2a2-42b1-879a-326cd3455f0b)

<br>

GUI 운용 실습
-------------
**DB 설계 순서 : 요구 분석 -> 개념적 설계 -> 논리적 설계 -> 물리적 설계 -> 구현**
  1. 사용자, 목적, 사용 범위, 제약 조건을 정리
  2. 추성적 개념으로 표현하며 E-R 다이어그램 (Chen model, Craw's Foot) 작성
     * 1:1 관계
     * 1:N 관계
     * N:M 관계
  3. 테이블 설계, 정규화로 논리적 자료로 변환
  4. 물리적 데이터로 변환
  5. 실제 파일 제작
