# 02.CSS (8/20 ~
**CSS (Cascading Style Sheet) : HTML 페이지를 꾸미기위해 사용되는 스타일 언어**
* px (pixel) :  고정크기
* % : 상위 태그 기준으로 %가 결정되는 가변 크기
* vw, vh : viewport 기준으로 %가 결정되는 가변 크기
* em : 부모 크기 기준으로 배수형태인 상대적 크기
* rem : root를 기준으로 배수형태인 상대적 크기

**CSS_Basic**
```
* width, height : 너비, 높이
<div style="min-width: 50px; max-height:70px">           // 최소 너비 50px, 최대 높이 70px

* color : 색상
<section style="color : violet; background-color : red>  // 글자 색 violet, 배경색 red

* spacing : 글자 간격
<body style="letter-spacing: 20px">                      // 글자 간격 20px, word-spacing은 단어 간격

* font-size : 글자 크기
<footer style="font-size:10px">                          // 글자 크기 10px

* font-family : 글꼴
<head><style> @font-family: "궁서체"                     // 궁서체 등록
  src:url("___")                
<wrapper style="font-family:'궁서체'>Hello World         // 궁서체로 Hello World 출력

* <link rel="styleshee" href"./css/common.css"> : 외부 CSS 파일 적용
```

**CSS_Box**
```
* border : 주위 선
<head <style> main{border-radius 1px solid} </style></head>     // 주위에 1px 둥근 사각형 생성

* margin : 바깥쪽 여백
border: 1px solid;               // border 필요
margin: 50px;

* padding : 안쪽 여백
padding: 5% 10%                  // 상하 5%, 좌우 10%

* position : 요소 배치
[none, fixed, static : 표시 안함, 고정, 기본]   
position relative;               // 부모 위치 등록
position absolute;               // 자식 위치 상대적 등록

* display: flex   : 자식 요소 수평 배치
[block, inline-block]
display: flex;
justify-content: center;        // 가로축: 중앙
align-items: center;            // 세로축: 중앙

* overflow : 내용이 넘칠 경우 표시 방법

* box-sizing : 총 너비, 총 높이
box-sizing: content-box;
```

**CSS_Selector**
```
* * : 전체 선택자
*{margin: 0; padding: 0}

* ____>__ : 요소 선택자
div>ul{display: flex;}
<div><ul></ul></div>

* id : ID 선택자
name{color: red;}
<div id="name"></div>

* class : class 선택자
.mains{background-color: lightgray}
<main class="mains></main>
```
