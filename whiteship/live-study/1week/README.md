## 1주차 과제: JVM은 무엇이며 자바 코드는 어떻게 실행하는 것인가.

https://github.com/whiteship/live-study/issues/1

### 목표

자바 소스 파일(.java)을 JVM으로 실행하는 과정 이해하기.

### 학습할 것

- JVM이란 무엇인가
- 컴파일 하는 방법
- 실행하는 방법
- 바이트코드란 무엇인가
- JIT 컴파일러란 무엇이며 어떻게 동작하는지
- JVM 구성 요소
- JDK와 JRE의 차이

### 학습 내용

#### JVM이란 무엇인가?

Java Virtual Machine(JVM)은 자바를 실행하기 위한 가상 머신이다.
생성된 자바 바이트 코드는 OS와 상관없이 OS에 의존적인 JVM에서 실행 가능하다.

예를 들어 윈도우에서 생성된 .class 파일은 추가적인 조작 없이도 리눅스나 유닉스에서
실행이 가능하다.

C 개발자에게는 상상도 못할 획기적인 일임에는 분명하다.

#### 컴파일 하는 방법

컴파일이란? 인간 또는 기계에 의해 작성된 .java 파일을 .class 파일로 만든다는 것을 의미하며, 이것은 JVM이 이해할 수 있다는 의미이다.

JDK(Java Development Kit, 자바 개발자 도구) 를 설치하면 javac 가 포함 되어 있다

javac를 사용하여 .class를 생성할 수 있는데, 이 때 정적인 검사도 포함되어
문법 오류가 있으면 수정해야 한다.

#### 실행하는 방법

JDK나 JRE(Java Runtime Environment, 자바 실행 환경)를 설치하면 java 가 포함되어 있다.

java로 .class를 실행할 수 있으며, 이 때 외부 라이브러리를 사용했다면, 실행 시에 라이브러리를 포함해야
오류가 나지 않는데.

#### 바이트코드란 무엇인가

JVM이 이해할 수 있는 코드
.java -> .class -> assembler code -> binary code -> 동작

#### JIT 컴파일러란 무엇이며 어떻게 동작하는지

#### JVM 구성 요소

1. Class Loader

클래스나 클래스의 인스턴스를 생성하면 메모리에 로드

2. GC (Garbage Collector)

메모리를 정리 도구
GC 알고리즘을 선택하여 실행 할 수 있다.

C 개발자는 너무 부러워 할 얘기다.

3. Execution Engine

메모리에 로드 된 바이트코드를 실행
인터프리터 방식 or JIT 방식으로 실행

4. Runtime Data Area

JVM의 메모리 영역

1. 클래스 영역
2. 힙 영역
3. 런타임 스택 영역
4. 네이티브 메소드 스택 영역

실행시에는 메모리 OVERFLOW가 발생하지 않도록, 옵션으로 조정해야 한다.
없으면, 메모리를 추가해야 함은 물론디ㅏ.

#### JDK와 JRE의 차이

- JDK(Java Development Kit, 자바 개발자 도구) : 프로그래밍 도구를 포함한 자바 실행 환경
- JRE(Java Runtime Environment, 자바 실행 환경) : 자바 실행 환경

개발하고자 하면 JDK가 반드시 있어야 하며, 실행만 할 경우 JRE만 있으면 된다.

### REF
