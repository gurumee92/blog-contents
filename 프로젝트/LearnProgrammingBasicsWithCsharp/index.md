---
title: C#으로 배우는 기초 프로그래밍
---

C#으로 배우는 기초 프로그래밍 강좌입니다.

## 목차
### **1부 프로그래밍 기초 및 개발 환경 설정**

1. **프로그래밍이란?**
    - 컴퓨터가 코드를 이해하는 방식
    - 프로그래밍 언어란 무엇인가?
    - C#이란 무엇인가?
2. **개발 환경 구축**
    - .NET SDK 및 Visual Studio Code 설치
    - 콘솔 프로그램 만들기 (`dotnet new console`)
    - C# 기본 코드 실행 (`Hello, World!` 출력)


### **2부 프로그래밍 기본 문법 익히기**

3. **변수와 데이터 타입**
    - **변수 선언 및 초기화** (`int`, `double`, `char`, `string`, `bool`)
	- **기본 데이터 타입의 크기와 범위**
	- **var 키워드와 명시적 타입 선언의 차이**
	- **상수(`const`)와 읽기 전용 변수(`readonly`)**
4. 문자열과 문자열 조작
	- 문자열 연결
	- 문자열 메서드
	- 문자열 분리 및 결합
	- `StringBuilder`를 활용한 성능 최적화
5. **조건문**
	* 논리 연산자
	* 조건문 
	- 패턴 매칭
6. **반복문과 배열**
	* 산술 연산자와 비교 연산자
    - `for`, `while`, `do-while` 반복문
	- 배열 (`int[]`, `string[]`)
	- 다차원 배열 (`int[,]`)
7. **함수 만들기**
    - 매개변수와 반환값
	- 메서드 오버로딩 (같은 이름, 다른 매개변수)
	- `params` 키워드를 이용한 가변 인수
	- `ref`와 `out` 키워드의 차이
	- `static` 메서드와 인스턴스 메서드의 차이
8. 실전 프로젝트! CLI 기반 미니 트렐로 만들기
	* **목표:** 2부에서 배운 기본 문법을 활용하여 **CLI 기반 Trello 프로젝트를 처음으로 만들어본다.**
	* 기능 목록
		* 보드 관리 기능 (추가, 삭제, 목록 출력)
		* 리스트 관리 기능 (보드 내 리스트 추가, 삭제, 조회)
		* 작업(Task) 관리 기능 (할 일 추가, 이동, 삭제)
		* 사용자 입력을 받아 CLI에서 실행 가능하도록 구현

### **3부부 객체 지향 프로그래밍 기초 익히기**

9. **클래스와 객체**
    - 클래스 선언 및 객체 생성 (`class Board { ... }`)
	- 필드(Field)와 속성(Property)
	- 생성자(Constructor)의 역할과 오버로딩
	- `static` 키워드의 의미와 활용
10. **상속(Inheritance)과 다형성(Polymorphism)**
	- 상속을 활용한 코드 재사용 (`class TaskCard : BaseCard`)
	- `abstract`, `virtual`, `override`, `sealed` 키워드 사용
	- 부모 클래스와 자식 클래스 관계
	- 업캐스팅(Upcasting)과 다운캐스팅(Downcasting)
11. 인터페이스
	* 인터페이스란? (`interface IBoard { ... }`)
	- 인터페이스 구현 (`class Board : IBoard { ... }`)
	- 추상 클래스(`abstract class`)와 차이점
	- 상속과 포함 어느 것이 더 좋은가?
12. **Enum 클래스**
	- Enum의 개념 (`enum TaskStatus { Todo, InProgress, Done }`)
	- switch문과 함께 활용
	- Enum을 문자열로 변환 (`Enum.Parse()`, `Enum.ToString()`)
13. 실전 프로젝트! CLI 기반 미니 트렐로 만들기 2차 OOP 적용
	* **목표:** 2부에서 만든 CLI 프로젝트를 **OOP 개념을 적용하여 리팩토링한다**
	* 개선 사항
		* `Board`, `List`, `TaskCard` 클래스를 만들어 객체 지향적으로 구조화
		* 인터페이스와 추상 클래스를 활용하여 유연한 설계 적용
		* `TaskStatus` 열거형(Enum)을 사용하여 작업 상태 관리


### **4부 C# 고급 기능 익히기** 
14. 파셜 클래스(Partial Class)와 확장 메서드(Extension Method)
	- `partial class`를 이용한 클래스 분리
	- **확장 메서드**를 사용한 기능 추가
15. 컬렉션과 데이터 관리
	- 대표 컬렉션
		- 리스트
		- 딕셔너리
		- 큐
		- 스택
	- **LINQ 기본 문법** (`Where()`, `Select()`, `OrderBy()`, `GroupBy()`)
	- LINQ를 활용한 **데이터 필터링 및 정렬**
	- **Lambda 표현식** 
16. **예외 처리와 디버깅**
	- `try-catch-finally` 문법과 예외 흐름
	- 예외 클래스 (`Exception`, `ArgumentException`, `NullReferenceException` 등)
	- **사용자 정의 예외 클래스** 만들기
	- **디버깅 기초**
	    - `Console.WriteLine()`을 활용한 디버깅
	    - **VS Code 디버깅 기능** 활용 (`breakpoint`, `watch` 등)
	    - 예외 발생 시 **콜 스택(Call Stack) 분석하는 방법**
17. **단위 테스트 (Unit Testing) 기초 및 실습**
	- **단위 테스트란 무엇인가?** (Why & When)
	- `xUnit` 또는 `NUnit`을 활용한 기본적인 단위 테스트
	- **테스트 메서드 작성 (`Assert.Equal()`, `Assert.Throws()`)**
	- **Mock 객체를 활용한 테스트**
18. **파일 입출력 (JSON, CSV 등 데이터 저장 및 불러오기)**
	- **파일 읽고 쓰기 (`File.ReadAllText()`, `File.WriteAllText()`)**
	- CSV 파일 저장 및 불러오기 (`StreamReader`, `StreamWriter`)
	- **JSON 데이터 관리 (`System.Text.Json`)**
	    - JSON 직렬화(Serialize)와 역직렬화(Deserialize)
	    - CLI 프로젝트의 데이터 저장을 JSON으로 구현하기
	- **파일 예외 처리 (`FileNotFoundException`, `UnauthorizedAccessException`)**
19. 실전 프로젝트! CLI 기반 미니 트렐로 만들기 3차 C# 고급 기능 적용
	* **목표:** 고급 기능을 적용하여 **완성도 높은 Trello 프로젝트를 만든다.**
	* 개선 사항
		* 단위 테스트를 작성하여 프로젝트의 신뢰성을 높임
		* LINQ를 활용한 데이터 검색 및 정렬 추가
		* JSON 파일을 활용하여 작업 내용을 저장하고 불러오는 기능 추가
		* 예외 처리 적용하여 프로그램 안정성 향상
### **5부 강좌를 마치며**
20. 이제 시작이다.
	* Trello를 개선해볼까?
		* 웹 애플리케이션 
		* 모바일 애플리케이션
	* 다른 걸 만들어볼까?
		* AI & 데이터 분석
		* 게임 개발