# 3. DataBase (8/2 ~
```
* Database : 데이터의 저장소
* Schema : DB의 구조를 전반적으로 기술한 것 - 외부, 내부, 개념
* DBMS (DataBase Management System) : DB를 관리, 운영하는 소프트웨어 / 대부분 관계형 DBMS 형태  
* SQL (Structured Query Language) : 관계형 DB에서 사용되는 언어
* 지식 피라미드 : Data -> Information -> Knownledge -> Wisdom
```
#### CRUD
* DDL (Data Definition Language) : 정의어로 데이터의 구조, 골격 - Create, Alter, Drop, Truncate
* DML (Date Manipulation Language) : 조작어로 데이터의 값 - Select, Insert, Update, Delete
* DCL (Date Control Language) : 권한 부여 - Grant, Revoke
* TCL - Commit, Rollback

DDL
----
```
* cmd 로그인
mysql -u root -p [port ____];    // mysql -user root -password port 8125 [port 번호 변경 시]

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

DML
---
```
* select : 값 확인
select * from tbl_ex1

* insert : 값 삽입
insert into dbex.tbl_ex1 values('홍길동', '대구 반월당', '23');
insert into dbex.tb1_ex1 values(ex1_name, ex1_age) values ('남길동', '23');

* update : 값 수정
update tbl_ex1 set ex1_age='30';                                    // 모든 ex1_int 값 30로 일괄 변경
update tbl_ex1 set ex1_addr='경북 구미시' where ex1_name='홍길동';  // ex1_name=홍길동인 row의 ex1_addr만 경북 구미로 변경

* delete : 값 삭제
delete from tlb_ex1 where ex1_addr='경북 구미시';                   // ex1_addr=경북 구미시가 포함된 row 값 모두 삭제      
```
