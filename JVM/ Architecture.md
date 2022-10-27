## JVM Architecture

JVM 기반 언어의 compiler는 .class 라는 자바 바이트코드(`Byte Code`)로 변환시켜주는데 Byte Code 는 기계어(`Native Code`)가 아니므로 OS 에서 바로 실행이 되지 않는다.그래서 바이트코드를 실행하기 위한 환경이 필요한데 그것이 바로 JVM(`Java Virtual Machine`)이다.

### JVM 컴파일 과정

<img width="577" alt="image" src="https://user-images.githubusercontent.com/51963264/198292023-bc3cc409-6126-4c7b-a073-c97914af8370.png">

 먼저 작성된 소스파일을 컴파일러가 해석하여 바이트 코드 파일을 생성한다. 바이트 코트 파일은 JVM에서 해석되고 해당 운영체제에 맞게 기계어로 번역된다.

 결국 운영체제가 읽을 수 있는 기계어 생성이 최종 목적이기 때문에 JVM은 운영체제에 맞게 설치되어야 한다.

### JVM 구성요소

<img width="538" alt="image" src="https://user-images.githubusercontent.com/51963264/196954440-e4653e9d-9ffe-4cce-80e2-c5b2279410be.png">

일반적으로 JVM의 구성은 다음과 같이 크게 세가지로 나눌 수 있다

- `ClassLoader Subsystem`:   
런타임 중에 JVM의 메소드 영역에 동적으로 Java 클래스를 로드하는 역할을 담당

- `Runtime Data Area`:
JVM이 프로그램을 수행하기 위해 운영체제로부터 할당 받는 메모리 영역

- `Execution Engine`:   
RuntimeDataArea에 할당된 byteCode를 실행하는 역할을 담당
