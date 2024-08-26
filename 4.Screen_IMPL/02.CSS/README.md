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
<head>
  <style> main{border-radius 1px solid} </style>      // 주위에 1px 둥근 사각형 생성
</head>

* margin : 바깥쪽 여백
[margin-top, margin-bottom, margin-left, margin-right]
border: 1px solid;               // border 필요
margin: 50px;

* padding : 안쪽 여백
padding: 5% 10%                  // 상하 5%, 좌우 10%

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
.parents{background-color: lightgray}
<main class="parents"></main>

* , : group 선택자
id, .group{border : 5px double red;}

*   : 후손 포함 자손 선택자  // 공백
.par son{}

* > : 후손 제외 자식 선택자
.par>son{}

* ~ : 하위 모든 선택자 동위 선택자
par~son{}

* + : 하위 1개 선택자 동위 선택자

* nth-child(n) : n번째 요소 선택
[first, nth, last]
ul>li:last-child{}                   // list의 마지막 요소 선택

* checkbox : 체크 박스
input[type='checkbox' id="chk"]      // checkbox 입력 생성, 명명chk
<label for="chk">체크 박스</label>   // chk를 위한 문구 표시

* :event : event 생성
[hover, active, click, checked : 커서 위치, 활성화, 클릭, 체크]
<style> son:hover{background-color: tomato;} </style>

* ::after, ::before : 가상 선택자
.parents::after{content:'★';}      // body의 contents 모든 영역 뒤에 ★ 추가 표시
```

### CSS_Layout : 요소 위치 지정
-------------------------------
```
* display : 배치 형태
[flex, grid, block, inline, none : 수평 배치, 2차원, 전체 line, 일부 line, 표시 안함]
* justify-content : 항목 간 공간
[center, start, space-between : 중간, 시작부, 항목 사이 동일 간격]
* align-items : display: flex 정렬 방향 
[stretch, center, flex-end : fit한 기본값, 가운데-height or width 100%, 아래쪽]

<style> div{
  display: flex;
  justify-content: space-between;
  align-items: center;
} </style>
```

**CSS_Position : Box의 위치 지정**
```
* z-index : 요소의 z축 (앞, 뒤) 지정
<div style="z-index: 1">z-인덱스</div>  // 기본값 : 0
 
* static : 순차적 배치되는 기본 속성
* fixed : viewport 기준으로 위치 조정, scroll과 무관하게 위치 고정
* sticky : scroll을 따라가다 넘어가면 위치 fixed

* relative : 순차적 배치, 상위 Box 요소를 기준으로 위치 조정
[margin 영향 X; top, bottom, left, middle로 위치 조정]
* absolute : 상위 요소 (보통 relative) 기준으로 위치 지정
[margin 영향 X; top, bottom, left, middle로 위치 조정]

<style>
  .par{position: relative; top: 50px; left: 100px;}
  .son{position: absolute; bottom: 1200px; right: 1000px;}
</style>
```

**CSS_Animation : 요소 움직임**
```
* transition : 요소 생성 시간
div{
  width: 50px; height: 10px;
  border: 1px solid;
  transition: 1s;}            // 생성 시간 1초

* transform : 생성 요소 설정
[translate, scale, rotate, skew, perspective : 이동, 크기, 회전, 기울기, 3D 회전]
.par:hover{
  transform: translate(200px, 100px);                 // 위치 이동
  transform: scale(2,2);                              // 크기 변경
  transform: rotate(180deg);                          // 회전
  transform: skew(15deg);                             // 기울기
  transform: translate(20px, 20px) skew(30deg);
  trnasform: perspective(30px) rotateY(360deg);       // 3D 회전
  backface-visibility: hidden;                        // 회전체 후면 숨김
}

* animation : 애니메이션 효과 방식 설정
<style> div{
  animation-name: moving1;                 // 효과 이름 moving1
  animation-duration: 2s;                  // 효과 시간 2초
  animation-iteraction-count: infinites;   // 효과 반복 무한
  animation-direction: alternate;          // 역방향 이동
  animation-timing-function: linear;       // 이동 속도 일정
}

@keyframes moving1{                        // 애니메이션 효과 명명
  from{left: 100vw; top: 20vw;}            // 출발 위치
  to{left:500vw; top:50vw;}                // 도착 위치
} </style>
```
