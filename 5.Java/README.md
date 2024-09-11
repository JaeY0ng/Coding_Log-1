# 05. Java (9/7 ~ )

**Github <-> Eclipse**
1. Eclipse에서 Java Project 생성
2. Java Project -> Team -> Share
3. Window -> Show View -> Other -> Git Repositories, Git Staging
4. Github -> New Repository -> add Readme 해제 -> Repository HTTPS 복사
5. Git Repositories -> Java Project -> Remote -> Create Remote -> Github Repository Link와 연결
        
**Java Basic : C언어 (절차 지향) + C++언어 (객체 지향)를 기반으로 하는 객체지향 프로그래밍 언어, 소프트웨어 플랫폼**
* Programming : Pro (미리) + Gram (쓰다) -> 앞으로 할 일을 미리 적어두는 작업
* Class 영역 : 객체 지향 문법 적용 단위
* Method (함수) : 작업 수행에 필요한 코드들을 묶어서 실행하는 단위
* Main Method : 최초 실행 함수
* Library Method : 미리 만들어져 제공되는 함수
* 사용자 정의 메서드 : 개발자에 의해 만들어진 함수
```
package C00;	// 패키지 명
public class C00HelloWorld {	// 클래스영역 - 객체지향 문법 적용 단위
	public static void main(String[] args) {	// 메서드 영역 - 절차지향 문법 적용 단위 (Main 메서드)
    }
}
```
            
**표준 입출력**
* 그래픽 문자 ("") : 일반적 문자
* 비그래픽 문자 ("\\") : 문자의 역할을 하는 비일반적 문자
  * \n : 줄 바꿈
  * \t : tab (8칸) 만큼 공백 생성
  * \b : 백스페이스
  * \\' : 특수 기호 표현
    
* 서식 문자 : 서식에 사용되는 비일반적 문자
  * %d : 10진수 (%o : 8진수, %x : 16진수)
  * %f : 실수
  * %c : 단일 문자
  * %s : 문자열
```
* print : 표준 출력 장치
System.out.print("Hello World");		// 그래픽 문자

* println : 표준 출력 장치 + 줄바꿈
System.out.println("Hello \t World");		// 비그래픽 문자

* printf : 표준 출력 장치 + 서식 문자 사용
System.out.printf("Today is %d day \n", 28);	// 서식 문자, 비그래픽 문자
```
**진수**
* 2진수 : 두 수 (0, 1)만 이용하는 체계
* 10진수 -> 2진수 (8bit = 00000000)
  1. 10진수를 2로 나눌 수 없을 때까지 나누기		(56 -> 28,0 14,0 7,0 3,1 1,1)
  2. 마지막 몫을 배치					(1)
  3. 마지막 몫에 가까운 순서부터 나머지들을 배치		(1/11000)
  4. 남는 자리수 만큼 앞에 0 배치				(00/1/11000  =>  00111000)
* 2의 보수 : 
```
10진수		2진수			2의 보수
0 		00000000		10000000 = -128				
1		00000001		11111111
3		00000011		11111101
7		00000111		11111001
15		00001111		11110001
31		00011111		11100001
63		00111111		11000001
127		01111111		10000001
```

**자료형**
* 선언 :
* 초기화 :
* 정의 :
* 자료형 :
