# HTML (8/19 ~ 20)
 
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

* <head>, </head> : viewport가 아님
* <header>, </header> : Logo 등이 들어가는 위쪽 머리말 부분
* <body>, </body> : 문서의 본문, viewport (사용자가 보는 영역)
* <footer>, </footer> : 사용자 정보 같은 꼬리말 부분
```

**Emmet**
```
* <___ class=""></___> : Class 선택자
<div class="fst_div"></div>      // fst_div 이름 부여

* <___ id="slider"></___> : ID 선택자
<div id="password"></div>        // 유형 선택

* ! -> Tab : HTML5 표준 문서 생성
* Ctrl + / : 주석 생성
* Shift + Alt + ↓ : 현재 행 복제
* > : 하위 자식 요소 생성
* ^ : 상위 부모 요소 생성
* + : 동급 형제 요소 생성
* *n : n번 만큼 반복 요소 생성
* $ : 순서대로 넘버링
* {} : 안에 텍스트 생성

wrapper>div>section1+section2^main{메인$}*2
<wrapper>
  <div>
    <section1>{섹션1}</section1>
    <section2>{섹선2}</section2>
  </div>
  <main>메인1</main>
  <main>메인2</main>
</wrapper>
```

### Block Tag : Box 처럼 구조를 만드는 태그 (Line 단독 사용)
-------------------------------------------
```
* <p>, </p> : 단락 태그로 위, 아래 공백 생성
<p>My cat is very grumpy</p>

* <div>, </div> : 정해진 역할 없는 블럭형 태그 (span)
<div>My dog is very tough</div>

* Entity - &nbsp  : 공백 표현
&nbsp; &nbsp; &nbsp    // 공백 3개

* <ul>, </ul> / <ol>, </ol> : 순서 있는 목록 생성 / 순서 없는 목록 생성
<ul>
  <li>List1</li>       // li는 list의 개별 요소
  <li>List2</li>
</ul>            
<ol type="1"> <li>list1></li><li>list2</li> </ol>  // 순서 표현 방식 1, A, a, I, i

* form : html 입력받을 수 있는 폼 생성

* <h1>, </h1> ~ <h6>, </h6> : 보통 제목으로 사용되는 글자의 크기를 지정 
<h1>Hellow World</h1> : 최대 크기
<h6>Hellow World</h6> : 최소 크기

* <section>. </section> : 독립 요소
<section> <h1></h1><h6></h6> </section>   // 보통 h 요소를 포함

* <title>, </title> : 생성 페이지의 제목
<title>Naver</tilte>   // Head 안에 존재
```

**Table : 행, 열로 구성된 데이터의 집합**
```
* <tr>, </tr> : 행 구분
* <th>, </th> : 가장 위 행 (열 제목)
* <td>, </td> : 행의 내용
* <caption>, </caption> : 테이블 제목
* <thead>, </thead> : 테이블 머릿말
* <tbody>, </tbody> : 테이블 본문
* <tfoot>, <t/foot> : 테이블 꼬리말
* <rowspan> : 행 병합
<___ rowspan="2">1</___>     // 1위치 기준으로 하단 2칸만큼 셀 생성

* <colspan> : 열 병합
<___ colspan="3">2</___>     // 2위치 기준으로 우측 3칸만큼 셀 생성

<table>
    <caption>테이블 연습</cation>
    <tbody>
      <tr>
        <td rowspan="3">1,1</td>      // (1,1)과 (2,1), (3,1) 병합  
        <td>1,2</td>  
        <td>1,3</td></tr>
      <tr>
        <td>2,2</td>
        <td>2,3</td> </tr>  
      <tr>3,1</td>
        <tr colspan="2">3,2</tr>     // (3,2)와 (3,3) 병합
    </tbody>
</table>
```

### Inline Tag : Block Tag에 내용을 작성하는 태그 (Line 일부 사용)
--------------------------------------------------
```
* <a href="">, </a> : 하이퍼 링크 연결
<a href="www.naver.com>네이버로 이동!</a>

* <span>, </span> : 정해진 역할 없는 라인형 태그 (div) 
<span>my cat is cute</span>

* <button>, </button> : 클릭할 수 있는 버튼 생성
<button>네이버로 이동</button>

* <img src="" alt=> : 이미지 연결
<img src="https://showcat.webp" alt="작은 고양이">                  //연결 주소, 이미지 이름
<img src=C:\Users\Administrator\Desktop\Cat.png alt="큰 고양이">    // 파일 경로, 이미지 이름

* <video></video><source src="" type=""></video> : 동영상 연결
<video controls autoplay muted loop>                                // 자동 재생, 음소거, 반복    
  <source src="C:\Users\Administrator\Desktop\Dog.mp4" type="video/mp4">
</video>

* <iframe src=""> : 현재 문서에 다른 문서 포함
<iframe src="www.google.com>

* <form action="" method="" class""> : 정보를 입력 받고 서버로 전달
<form action="test.jsp" method="GET" class"container w-25">
          <input type="text"      name="userid"            placeholder="아이디 입력">
</form>  // text형식을 입력받는다   정보를 userid라고 저장   출력메시지
```

