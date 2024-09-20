# 04. JavaScript (8/30 ~ 9/7)
**JavaScript (JS) : 웹에서 복잡한 기능을 구현할 수 있는 스크립팅 프로그래밍 언어**
* 변수  
  * var : 전역 가변수
  * let : 지역 가변수
  * const : 지역 불변수
* 자료형
  * Number : 숫자
  * String : 문자열
  * Boolean : 참, 거짓
  * Null : 빈값
* 참고 자료형 (인스턴스)
  * Object : 여러 속성을 저장 가능 (Key - Value)
  * Array : 배열
  * Function : 함수
  * Date : 날짜

```
let Ob = new Object();
Ob.age = 23;
let Obj = {
  name: 'Object';
  gemder: 'none';
  Info: function () {
   console.log("Obj Information" + name + gender);
 }
}
var Problem = function (cnt) {
  console.log("I Have " + cnt + "problems)");
}

* console.log : console에 확인용 정보 생성
console.log(Ob);

* getElementById() : id명으로 요소 접근
document.getElementById(Ob);       // id명만 불러오기에 #Ob라고 적지 않아도 됨

* querySelector() : class, id명으로 요소 접근
[Selector, SelectorAll]
document.querySelector(#Ob);       // 클래스명
document.querySelectorAll(.Obj);   // id

* element.appendChilde() : 자식 추가

* getAttribute() : CSS 수정

* addEventLisnter() : 이벤트 추가
Ob.addEventListner((event, 'click') -> {
  Ob.getAttribute('style', 'background-color: black');
})
``` 
