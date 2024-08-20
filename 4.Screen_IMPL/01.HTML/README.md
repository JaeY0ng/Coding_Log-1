# HTML (8/19 ~

* VS code 설치 (최신 version)
  1. Auto Rename Tag
  2. Liver Server
  3. Prettier Code for Formatter
  4. 설치 경로 -> cmd -> code // 현재 위치에서 vscode 실행               


**HTML (Hyper Text Markup Language) : 웹 페이지에서 다른 페이지로 이동 가능**
* 요소 (Element) : 콘텐츠를 감싸는 태그
* 속성 (Attribute)
* 값 (Value)

```
* !DOCTPYE : HTML 버전 정보
<!DOCTYPE HTML5>

* <html>, </html> : html 문서의 시작, 끝
<html lang="ko"></html>       // lang 속성으로 기본 언어가 한국어임을 표시

*<meta name="viewport" contetnt="width=device-width, initial-scale=1.0>
<meta name="viewport"         // 반응형 웹을 위한 뷰포트 설정
content="width=device-width   // 뷰포트의 너비를 디바이스 너비만큼 설정
initial-scale=1.0>            // 페이지 첫 로드 시에 확대, 축소 지정

* <head>, </head>
* <body>, </body> : 문서의 본문, viewport (사용자가 보는 영역)
* <foot>, </foot> a
```

###Block Tag : Box 처럼 구조를 만드는 태그
-------------------------------------------
```
* <p>, </p> : 여는 태그, 닫는 태그로 위 아래 여백 생성
<p>My cat is very grumpy</p>

* <div>, </div> : 정해진 역할 없이 Line 단독 사용
<div>My dog is very tough</div>

* Entity - &nbsp  : 공백 표현
&nbsp; &nbsp; &nbsp    // 공백 3개

* <li>, </li>  : 목록의 개별 요소

* <ul>, </ul> / <ol>, </ol> : list 목록 생성
<ul> <li>List1</li><li>List2</li> </ul>            // ul은 순서가 없는 목록 
<ol type="1"> <li>list1></li><li>list2</li> </ol>  // ol은 순서가 있는 목록

* <h1>, </h1> ~ <h6>, </h6> : 글자 크기 지정 
<h1>Hellow World</h1> : 최대 크기
<h6>Hellow World</h6> : 최소 크기

* <title>, </title> : 페이지의 제목
<title>Naver></tilte>        // Head 안에 존재

* <table>, <table>
* <caption>, <caption>

```
**Inline Tag : Block Tag에 내용을 작성하는 태그**
```
* <a>, </a>
* <span>, </span>
* <button>, </button>
* <img>, </img>
<video controls autoplay muted loop>
<form action="test.jsp" method="">
```
style
section
emmet
entitiy
width height
maggin
form
input + type
radio : 택1 버튼

bootstrap
