## Garbage Collector

가비지 컬렉션이 실행되면 GC 작업을 맡은 스레드를 제외한 나머지 스레드는 모두 멈추게되고 GC 작업이 종료되면 재개된다.

GC는 이름에서 알 수 있듯 JVM의 `힙 Heap 영역`에 있는 객체들을 추적하고 쓰이지 않는 객체들을 삭제 시킴으로써 메모리 공간을 효율적으로 사용할 수 있게 해준다.

### 동작 원리

> Mark & Sweep

일반적으로 GC의 작업은 두 단계 구성되는데 다음과 같다.

- `Mark`:   

- `Sweep`:


### 메모리 누수 memory leak

>사용되지 않는 객체들이 GC에 의해 회수되지 않고 계속 누적이 되는 현상을 말한다.

Old 영역에 계속 누적된 객체로 인해 Major GC가 빈번하게 발생하게 되면서, 프로그램 응답속도가 늦어지면서 성능 저하를 불러온다. 이는 결국 OutOfMemory Error로 프로그램이 종료되게 된다.
