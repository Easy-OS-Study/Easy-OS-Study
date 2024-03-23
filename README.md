# BookStudy

![운영체제](https://github.com/Easy-OS-Study/BookStudy/assets/50690859/26d27f91-657b-4fc0-8f9e-dcf08cb5bde2)

<br>

## 진행 방법
- 쉽게배우는운영체제 독서 스터디
- 매주 각자 1 챕터씩 독서 진행
- 매주 시작 시 무작위로 1명이 해당 챕터 읽은 소감 발표
- 매주 각자 3문제씩 면접문제 준비 후 2문제씩 총 8문제 질문 진행
- 블로그나 깃허브 등 독서 내용 정리의 경우 자율적으로 진행

<br>
<br>

<details>
<summary>1Chapter</summary>
<div markdown="1">
<br>

### 정리

|이름|링크|
|:---:|:----------:|
|임규리|[정리 링크](https://newbie-in-softengineering.tistory.com/entry/OS-Ch1-%EC%9A%B4%EC%98%81%EC%B2%B4%EC%A0%9C%EC%9D%98-%EA%B0%9C%EC%9A%94)|
|김민우|[정리 링크](https://velog.io/@kmw89891/운영체제의-개요)|
|황인준|[정리 링크](https://github.com/InJun2/TIL/blob/main/BookStudy/SE/쉽게배우는운영체제/Chapter1.md)|
|황하림||

<br>

### 질문

1. 실시간 시스템이란?

   
2. 데이터베이스 서버나 게임 서버같은 경우 어떤 시스템을 사용하는 것이 좋을지?
- 클라이언트 서버 시스템 : 클라이언트/서버 아키텍처는 각각의 역할을 분리하여 시스템을 관리할 수 있음. 데이터베이스 서버는 데이터 관리와 관련된 작업에, 게임 서버는 게임 로직 처리와 관련된 작업에 중점을 둠으로써 코드를 더 명확하게 구조화 가능, 효율적인 네트워크 사용 가능
- 분산 시스템 : 분산 시스템은 여러 대의 서버로 작업을 분산시킴으로써 전체 시스템의 성능을 향상시키고. 각 서버는 일부 작업을 담당하므로 전체적으로 빠른 응답 속도를 제공할 수 있음. 여러 서버에 작업을 분산시키면 하나의 서버가 고장 나더라도 시스템은 계속해서 작동할 수 있어 대규모 응용 프로그램에 유용
   
3. 레이아웃서비스와 마이크로서비스는 각자 어느 경우에 사용하는지?

   
4. 가상머신 장점과 사례
가상 머신의 장점은 특정 운영체제에 제한을 받지 않고 다양한 운영 체제를 동시에 사용 할 수있습니다.
- JVM
  JAVA가 어떤 os 환경에서 실행가능하게 해주는 역할을 하는 Java vritual Machine이 대표적인 예라고 할 수 있습니다.
   
6. 시스템 호출과 드라이버
   
   
7. 운영체제에서 직접적으로 자원을 사용하게 하지 않았는지. 그 이점은 무엇인지?
직접 적으로 메모리에 어디에 저장되고 찾아오는지 등 크리티컬한 작업을 사용자가 자유롭게 조작 할 수 있다면 많은 번거로움과 효율적이 못합니다.
이를 막기 위해 운영체제에서 사용자가 시스템 호출을 받게 되면 커널을 통해 실질 적인 자원 관리를 통해 간편하고 보안성을 높이는 이점을 갖습니다.

9. 실시간 시스템
- 특정 시스템에서 일정 시간 안에 작업이 처리되도록 보장하는 시스템
- 경성 실시간 시스템 (hard real-time system) : 지정한 응답 시간을 정확히 지키는 시스템
   - ex) 미사일
- 연성 실시간 시스템 (soft real-time system) : 지정한 응답 시간을 최대한 지키지만, 융통성이 어느 정도 허용된 시스템
   - ex) 동영상 재생


</div>
</details>

<details>
<summary>2Chapter</summary>
<div markdown="1">
<br>

### 정리

|이름|링크|
|:---:|:----------:|
|임규리|[정리 링크](https://newbie-in-softengineering.tistory.com/entry/OS-Ch2-%EC%BB%B4%ED%93%A8%ED%84%B0%EC%9D%98-%EA%B5%AC%EC%A1%B0%EC%99%80-%EC%84%B1%EB%8A%A5-%ED%96%A5%EC%83%81)|
|김민우|[정리 링크](https://velog.io/@kmw89891/컴퓨터-구조와-성능-향상)|
|황인준|[정리 링크](https://github.com/InJun2/TIL/blob/main/BookStudy/SE/쉽게배우는운영체제/Chapter2.md)|
|황하림||

<br>

### 질문

1. 캐시 데이터를 메모리에 반영하는 즉시 쓰기와 지연 쓰기의 경우 각각 어느때 사용해야 할지?
- 즉시 쓰기 : 성능 보다 데이터의 일관성을 더 중요시 하는 경우. 항상 최신의 데이터를 보장하는 시스템에 적용
- 지연 쓰기 : 데이터 동기화보다 성능을 우선시하는 경우. 파일 시스템에서 로그 기록과 같이 지속적인 쓰기 작업이 빈번한 경우

2. 멀티 프로세스 대신 멀티 스레드를 사용하는 이유<br>
- 쉽게 설명하면, 프로그램을 여러 개 키는 것보다 하나의 프로그램 안에서 여러 작업을 해결하는 것이 더 낫기 때문이다.
- 자원의 효율성 증대
  - 멀티 프로세스로 실행되는 작업을 멀티 스레드로 실행할 경우, 프로세스를 생성하여 자원을 할당하는 시스템 콜이 줄어들어 자원을 효율적으로 관리할 수 있다.
  - 스레드는 프로세스 내의 메모리를 공유하기 때문에 독립적인 프로세스와 달리 스레드 간 데이터를 주고받는 것이 간단해지고 시스템 자원 소모가 줄어들게 된다.
- 처리 비용 감소 및 응답 시간 단축
  - 프로세스 간의 통신(IPC)보다 스레드 간의 통신의 비용이 적으므로 작업들 간의 통신의 부담이 줄어든다.
  - 프로세스 간의 전환 속도보다 스레드 간의 전환 속도가 빠르다.
- 단점 : 동기화 문제(불필요한 부분까지 동기화하면 대기 시간으로 인해 성능저하 발생), 하나의 스레드 장애로 전체 스레드가 종료될 위험, 디버깅의 어려움, 단일 프로세스 시스템의 경우 효과가 크지 않음

3. 주소 버스가 단방향인 이유
- 주소를 표현하는 신호가 CPU로부터 다른 장치로 향하고 반대로의 전송은 필요 없기 때문
- 데이터 버스는 데이터를 주고 받아야 하기 때문에 양방향
- 제어 버스는 읽기/쓰기 동작을 모두 수행하기 때문에 양방향

4. C/C++의 포인터는 무엇인가?
- 메모리의 각 바이트마다 부여되는 고유의 주소값을 뜻한다.
- 변수들은 메모리 공안을 연속적으로 차지하는데 (e.g. `int` 변수 : 4 byte -> 4칸 차지) 할당된 공간의 맨 앞 주소값을 포인터라 한다.
   
5. 성능 향상을 위한 방법인 비동기와 병렬은 각각 무엇인지
- 비동기 처리 : 특정 작업을 비동기적으로 수행하면 그 작업을 호출한 스레드가 작업의 결과에 신경쓰지 않고 자기가 하던 일을 수행. 여러 작업이 동시에 진행되도록 허용하며 작업이 완료될 때까지 대기하지 않는 것으로 논블로킹을 참조하면 이해하기 쉬울 것 같음. 주로 이벤트가 발생할 때마다 작업을 수행하는 이벤트 기반 프로그래밍. 비동기 코드는 단일 쓰레드에서도 여러 작업을 동시에 처리할 수 있음
- 병렬 처리 : 큰 작업을 작은 작업으로 나누어 여러 프로세서 혹은 코어에서 동시에 실행하도록 함. 큰 문제를 작은 문제로 분할하고 한번에 실행되기 때문에 성능적 이점을 가지게 됨. 실행 단위는 쓰레드로 한번에 여러 쓰레드를 실행

6. OS 또한 소프트웨어이므로 사용자 프로세스가 실행중이라면 중단된다. 그렇다면 사용자 프로세스가 실행중일 때 비정상적인 메모리 접근을 막을 수 있는 이유는?
- CPU의 경계/한계 레지스터(하드웨어)를 통해 실행중인 프로그램에 할당된 메모리 영역을 기억한다.
- 프로세스 진행 중 이 영역 외에 접근이 발생하면 인터럽트를 통해 응용 프로그램을 강제 종료시킨다.
  
7. Python과 비교했을 때 Java의 장점?
- Java는 컴파일 방식을 통해 코드 실행 속도가 인터프리터 방식만 사용하는 Python에 비해 빠르다.
- 멀티스레드 환경에 적합하다.

8. LRU Cache가 무엇인가요?
- 페이지 교체 알고리즘으로 가장 오랫동안 참조되지 않은 페이지를 교체 대상으로 삼는 기법
- chache에 있는 데이터를 호출하게 되면 호출한 데이터는 chache 가장 뒤로 이동한다. 

<br>

### 이후 다시 이야기해볼 주제
- 하나의 코어에서 멀티스레딩 병렬처리 하는 방법
- 비동기 처리, 병렬 처리

</div>
</details>

<details>
<summary>3Chapter</summary>
<div markdown="1">
<br>

### 정리

|이름|링크|
|:---:|:----------:|
|임규리|[정리 링크](https://newbie-in-softengineering.tistory.com/entry/OS-Ch3-%ED%94%84%EB%A1%9C%EC%84%B8%EC%8A%A4%EC%99%80-%EC%8A%A4%EB%A0%88%EB%93%9C)|
|김민우|[정리 링크](https://velog.io/@kmw89891/%ED%94%84%EB%A1%9C%EC%84%B8%EC%8A%A4%EC%99%80-%EC%8A%A4%EB%A0%88%EB%93%9C)|
|황인준|[정리 링크](https://github.com/InJun2/TIL/blob/main/BookStudy/SE/쉽게배우는운영체제/Chapter3.md)|
|황하림||

<br>

### 질문

1. 프로세스 계층 구조를 두었을 때 장점?
- 프로세스 간 서로 독립적이라면 OS가 자원 회수를 직접해야 해서 작업이 복잡해진다.
- 자식 프로세스가 끝난 경우 자원 회수를 부모 프로세스가 할 수 있어 자원 관리에 용이하다.

2. 일반적으로 함수마다 스택 공간을 할당받으므로 하나의 로직에 대해 함수가 많아진다면 비효율적이다. 그러나, Java에선 메서드 추출을 해도 성능상 이슈가 없다. 그 이유는?
- JVM의 JIT 컴파일러가 컴파일 시 인라인(inline) 기능을 사용한다.
> 참고
> 
> [인라인 함수](https://tcpschool.com/cpp/cpp_cppFunction_inlineFunction)
>
> C++의 경우 `inline`이라는 키워드를 직접 메서드에 명시해야 이 기능을 사용할 수 있지만, Java의 경우 JIT 컴파일러가 이를 대신 해주므로 별도의 `inline` 키워드가 없다.

3. 커널 스레드와 사용자 스레드의 차이
- 사용 차이로는 주로 스레드의 관리 방식과 성능, 그리고 운영 체제와의 상호작용에 관련
 - 커널 스레드는 운영체제 영역에서  스레드 연산을 수행하여 운영체제의 의존적이고 사용자 스레드는 사용자 영역에서 사용하여 운영체제의 의존적이지 않음
- 커널 스레드는 운영 체제 커널에 의해 직접 관리되는 스레드로 운영 체제가 스레드의 생성, 스케줄링, 스레드 간의 동기화, 스레드 간 통신 등을 담당하며 커널 스레드는 운영 체제에 의해 직접적인 자원 할당 및 관리가 이루어지므로 정교한 스레드 스케줄링 및 동기화를 가능하게 하며, 다중 코어 시스템에서의 병렬 실행을 지원하지만 스케줄링과 동기화를 위해 커널을 빈번하게 호출하고 컨텍스트스위칭이 빈번하게 발생하여 성능 저하가 발생하며 스레드의 생성 및 관리에 비용이 더 많이 소요됨
- 사용자 스레드는 스레드 라이브러리나 런타임 환경에 의해 관리되는 스레드로 운영 체제는 사용자 스레드의 존재를 알지 못하여 모드 전환이 없어 커널에 의존적이지 않은 형태로 라이브러리를 활용하여 성능 이득이 발생 (운영체제의 의존적이지 않음). 라이브러리가 직접 스케줄링을 하고 작업에 필요한 정보를 처리하여 컨텍스트 스위칭이 필요없음. 사용자 스레드의 생성, 스케줄링, 동기화 등은 런타임 환경에서 처리되는데 해당 과정에서 커널을 호출하지 않아 인터럽트가 발생할 때 커널 레벨 스레드보다 오버헤드가 적음. 그러나 사용자 스레드는 운영 체제의 멀티코어 활용과 같은 고급 기능에 대한 직접적인 지원을 받지 못할 수 있음 ( 시스템 전반에 걸친 스케줄링 우선순위를 지원하지 않고 프로세스에 속한 스레드 중 I/O 작업등에 의해 하나라도 블록이 걸린다면 전체 스레드가 블록됨)

4. 대기 상태에서 인터럽트 프로세스를 다중 대기큐에 관리하는 이유는?
   - 대기 상태는 프로세스를 실행하는 과정에서 외부의 입출력을 받아야 할 때 해당 작업을 대기상태로 보낸다.
   - 대기 상태로 넘간 프로세스는 장치마다 나뉘어져 있는 대기 큐에 들어가게 된다.
   - 장치마다 작업 대기 프로세스가 존재하므로 여러작업 장치의 요청을 백터의 형태로 처리하여 처리 능력이 좋다.
   - 또한 빠른 작업처리로 원활한 작업을 지원한다는 장점을 갖는다.
5. 멀티 스레드 장단점
   - 장점 : 응답성 향상, 자원 공유, 효율성 향상, 다중 CPU 지원
   - 단점 : 동기화 문제, 하나의 스레드 3장애로 전체 스레드가 종료될 위험, 단일 프로세스 시스템의 경우 효과가 크지 않음
6. PCB는 무엇이며 왜 사용하는지
   PCB
   - 프로세스 제어 블록
   - 프로세스를 실행하는데 필요한 중요한 정보를 보관하는 자료 구조
   - 모든 프로세스는 고유의 프로세스 제어 블록을 가지며, 프로세스 제어 블록은 프로세스 생성 시 만들어져서 프로세스가 실행을 완료하면 폐기된다.
  PCB를 사용하는 이유
   - 말 그대로 프로세스를 제어하기 위해 사용
   - **문맥 교환하려고!**
   - 프로세스마다 CPU 퀀텀이 시분할로 할당되는데, 이 시간을 넘기거나 프로세스의 우선순위와 스케줄링 알고리즘 등에 의해 프로세스 상태 전이가 일어난다. 이때, CPU는 모든 프로세스의 레지스터 값들과 해당 프로세스의 위치, 이 프로세스가 어떤 프로세스인지는 구별하지 않는다. 따라서 이를 구별하기 위해 운영체제는 PCB라는 자료구조를 이용해 프로세스를 체계적으로 관리한다.
8. 자바와 프로세스 제어 블록이 연관이 있는지?
- PCB는 운영체제 수준의 데이터 구조로 커널 내부에 존재하기 때문에 자바에서 직접 PCB에 관여할 수 없음.  JVM(Java Virtual Machine)은 운영 체제의 프로세스 내에서 동작하고 PCB에 직접적으로 접근하거나 조작할 수 없음. 대신, JVM(Java Virtual Machine)이 운영 체제와 상호작용하여 자바 프로세스를 관리
- JVM은 운영 체제로부터 프로세스 및 스레드 관련 정보를 얻어와 자바 런타임 환경 내에서 이를 관리. 이러한 과정에서 PCB와 같은 운영 체제 수준의 자료구조는 JVM 내부에서 추상화되어 자바 프로그램에 직접 노출되지 않지만 JVM은 운영 체제와의 인터페이스를 통해 필요한 리소스를 요청하고 프로세스 및 스레드를 생성하므로 자바 언어 자체가 PCB에 직접적인 영향을 미치는 것은 아니지만, 자바 프로그램이 운영 체제에서 실행되는 동안에는 운영 체제의 프로세스 관리 기능을 활용하게 됨. 따라서 자바 프로그램이 운영 체제의 PCB와 상호 작용하며 프로세스를 생성하고 제어할 수 있음. 그러나 이는 자바 언어의 특성이 아니라 운영 체제와의 상호 작용에서 발생하여 연관이 있다고 봐야할 것 같음

8. 

</div>
</details>

<details>
<summary>4Chapter</summary>
<div markdown="1">
<br>

### 정리

|이름|링크|
|:---:|:----------:|
|임규리|[정리 링크](https://newbie-in-softengineering.tistory.com/entry/OS-Ch4-CPU-%EC%8A%A4%EC%BC%80%EC%A4%84%EB%A7%81)|
|김민우|[정리 링크](https://velog.io/@kmw89891/CPU-%EC%8A%A4%EC%BC%80%EC%A4%84%EB%A7%81)|
|황인준|[정리 링크](https://github.com/InJun2/TIL/blob/main/BookStudy/SE/쉽게배우는운영체제/Chapter4.md)|
|황하림||

<br>

### 질문

1. 오늘날 OS에서 타임 슬라이스를 고정하지 않은 이유는?
  - 오늘날 CPU 스케줄링 방식으로 MLFQ 이 사용된다. 이 방식은 프로세스를 우선순위로 마다 별도의 큐에 저장하는데 우선순위가 낮을 수록 타임 슬라이스의 크기를 늘려 공평성을 지킨다.
  - 즉, 프로세스의 우선순위마다 타임 슬라이스를 다르게 하므로 타임 슬라이스를 고정하지 않는다.
2. 다중 큐를 도입하는 이유
  - 대기 상태 : 같은 입출력을 요구하는 프로세스끼리 모아둬 입출력 완료 인터럽트 시 해당 프로세스를 효율적으로 찾기 위함
  - 준비 상태 : 프로세스 우선순위마다 큐를 만들어 다음 실행할 프로세스를 효율적으로 조회하기 위함

3. 사이클 훔치기란?
   - CPU와 직접 메모리 접근이 동시에 메모리에 접근하려 할 때, CPU가 메모리 사용 권한을 양보하는 것
   - CPU의 작업 속도보다 입출력장치의 작업 속도가 느리기 때문
   - CPU 입장에서는 직접 메모리 접근이 사이클(순서)를 훔쳐간 것
4. CPU 스케줄링은 언제 발생합니까?
   - 준비상태로 올라갈 때
   - 실행상태에서 대기상태로 전활될 때 (ex. 입출력 요청)
   - 실행상태에서 준비상태로 전환될 때 (ex. 인터럽트 발생) : 종료되는 상황 제외?
   - 대기상태에서 준비상태로 전환될 때 (ex. 입출력이 종료될 때)
   - 종료될 때 (Terminated)
5. 로드 밸런싱에서 라운드 로빈 알고리즘은 무엇인가?
   - 클라이언트로부터 받은 요청을 대상 서버에 __순차적으로 할당하는 방식__
   - 서버들의 성능이 동일하고 처리 시간이 짧은 어플리케이션에서 사용한다.
   - (라운드 로빈 : 순환 순서)
6. 사용자 프로세스로 부터 시스템 자원을 보호하기 위한 하드웨어/소프트웨어적 기법은?
   - 하드웨어 : CPU 경계/한계 레지스터
   - 소프트웨어 : 인터럽트
7. 스케줄링 알고리즘에서 구분하는 방법을 주로 평균 대기 시간으로 보는 이유
   - 우선 책에서 CPU 알고리즘의 효율성을 평가할 때 사용률과 처리량은 계산하기 어렵기 때문에 대기시간, 응답시간, 반환 시간을 계산하는데 사용자 관점에서 시스템의 성능을 평가할 때 대기 시간은 사용자가 경험하는 작업 완료 시간에 직접적으로 영향을 끼치기 때문
   - 대기 시간이 적어야 여러 프로세스들이 실행될 기회가 늘어나고 작업이 빨리 처리되므로 시스템 전체 자원 활용도가 향상되어서
   - 다른 지표의 경우 추가적인 변수를 고려해야할 수 있으며 결과를 해석하는 것이 복잡할 수 있어서
   - 그렇기 때문에 평균 대기 시간이 적은 스케줄링 알고리즘은 프로세스들이 가장 적게 대기하여 CPU를 효율적으로 활용하는 알고리즘
8. 저수준 스케줄링과 중간수준 스케줄링에서 실제로 작업이 이루어지는 이유
   - 고수준 스케줄링은 프로세스를 할당할지 말지에 대하여 관여하므로 작업을 승인할지 거부할지의 여부이며 그 외 스케줄링들은 모두 시스템의 자원을 관리하고 프로세스 또는 스레드를 실행하는데 관여하여 자원 할당, 우선순위 결정, 작업 전환, 자원 관리 등의 역할을 수행하기 때문에
   - 그렇게 현대 시스템에서 고수준 스케줄러를 추가로 사용하는 것은 시스템의 복잡성을 증가 시킬 수 있어 현대에는 저수준과 중간 수준 스케줄러만으로도 충분히 시스템을 관리할 수 있음. 저수준과 중간 수준 스케줄러는 더 직접적이고 빠른 접근을 제공하므로 자원을 효율적으로 활용

</div>
</details>

<details>
<summary>5Chapter</summary>
<div markdown="1">
<br>

### 정리

|이름|링크|
|:---:|:----------:|
|임규리|[정리 링크](https://newbie-in-softengineering.tistory.com/entry/OS-Ch5-%ED%94%84%EB%A1%9C%EC%84%B8%EC%8A%A4-%EB%8F%99%EA%B8%B0%ED%99%94)|
|김민우|[정리 링크](https://velog.io/@kmw89891/%ED%94%84%EB%A1%9C%EC%84%B8%EC%8A%A4-%EB%8F%99%EA%B8%B0%ED%99%94)|
|황인준|[정리 링크](https://github.com/InJun2/TIL/blob/main/BookStudy/SE/쉽게배우는운영체제/Chapter5.md)|
|황하림||

<br>

### 질문

1. 뮤텍스와 세마포어의 차이<br>
**Mutex (상호 배제)**
- 공유 자원을 사용하기 전에 설정하고 사용한 후에 해제하는 잠금
- 잠금이 설정되면 다른 스레드는 잠긴 코드 영역에 접근할 수 없음
- 하나의 상태(잠금 또는 잠금 해제)만 가짐<br>
**Semaphore**
- 일반화된 뮤텍스
- 간단한 정수 값과 두 가지 함수 wait(), signal()로 공유 자원에 대한 접근을 처리함<br>
**차이점**
- 가장 큰 차이점은 동기화 대상의 개수
- Mutex는 동기화 대상이 오직 1개일 때 사용 / Semaphore는 대상이 1개 이상일 때 사용
- Mutex는 자원을 소유할 수 있고 책임을 가짐 / Semaphore는 자원 소유 불가
- Mutex는 상태가 0, 1 뿐이므로 Lock을 가질 수 있고, 소유하고 있는 스레드만이 이 Mutex를 해제할 수 있음 / Semaphore는 Semaphore를 소유하지 않는 스레드가 Semaphore를 해제할 수 있음
- Semaphore는 시스템 범위에 걸쳐 있고, 파일 시스템 상의 파일로 존재 / Mutex는 프로세스의 범위를 가지며 프로세스가 종료될 때 자동으로 clean up 됨
2. 파일을 이용한 통신 : 파일 open()은 언제 실행되어야 하며 이유는 무엇인가?<br>
fork()문 실행 전<br>
파일 기술자(fd)가 자식 프로세스에도 상속되기 위해<br>
fd가 자식 프로세스에도 복사되므로 같은 fd를 사용<br>
자식 프로세스에서 처리를 하고 종료된 후, 부모 프로세스에서 접근하려면 fd를 lseek()을 통해 맨 앞으로 옮겨주어야 함<br>

3. 프로세스 통신 방법에서 멀티 스레드 환경일 때 하나의 프로세스에서 여러 스레드가 공유 자원에 접근해야 한다면 어떻게 동작해야 할까?
   - 스레드도 동일하게 동작. 프로세스간 통신을 통해 임계구역에 적당한 수의 프로세스만 접근이 가능
   - 프로세스의 작업 단위는 스레드(Thread)이며, 프로세스 내의 스레드는 같은 주소 공간을 공유하고 이로 인해 프로세스 내의 각 스레드는 동일한 자원에 접근할 수 있으며, 이를 통해 동일한 방법으로 공유 자원에 접근할 수 있음
   - 프로세스 간 통신(IPC)을 기준으로 공유 자원을 획득한 후에는 해당 자원을 사용하는 것을 스레드 단위로 관리하는 것이 일반적. 스레드도 마찬가지로 프로세스의 공유 자원을 나눠 가줘야 하므로 스레드 간에도 뮤텍스나 세마포어와 같은 동기화 메커니즘을 사용하여 각 스레드가 공유 자원에 접근
   
4. 소켓이란 무엇인가?
   - 소켓이란 네트워크 상의 두 지점 간의 양방향 통신을 할 수 있는 연결점. 네트워크 통신에서 데이터는 패킷이라는 작은 조각으로 분할되어 전송되는데 소켓이 이러한 데이터 통신을 관리하고 제어하기 위한 인터페이스 임
   - 데이터를 보내는 쪽에서도 소켓을 생성하고 데이터를 전송하며 데이터를 받는 쪽에서도 소켓을 생성하여 데이터를 수신
   - 소켓은 TCP/IP 프로토콜을 사용하는 경우 TCP 소켓이나 UDP 소켓으로 사용됨
   
5. 임계 구역에서 문제가 발생하는 대표적인 원인 2가지와 해결책은?
   - 타임 아웃
     - 하드웨어의 도움
   - 클라이언트의 잘못된 사용
     - 추상화를 통해 직접적인 접근을 막는다 

6. 모니터는 공유 자원을 숨기고 접근을 위한 퍼블릭 인터페이스(e.g. `increase()`)만 제공하는 기법이다. Java에서 이와 같은 기법을 사용하는 예시는?
   - 참조(Reference)
     - 사용자로부터 메모리 주소 직접 노출을 막는다. 덕분에 메모리 자원을 보호할 수 있다.
   - `Collection<E>` 하위 인터페이스 및 구현 클래스
     - 각 컬렉션에 알맞는 퍼블릭 인터페이스(e.g. `Stack<E>`의 `push()`)만 제공하여 사용자가 내부 규칙을 와해하는 것으로 부터 보호할 수 있다.

7. 서버가 여러 클라이언트의 요청을 처리하는 방법?
   - 서버는 포트마다 여러 개의 소켓을 만들어 두고 (무한 루프를 돌며) 주기적으로 클라이언트의 요청을 확인 및 처리한다.

</div>
</details>

<details>
<summary>6Chapter</summary>
<div markdown="1">
<br>

### 정리

|이름|링크|
|:---:|:----------:|
|임규리|[정리 링크](https://newbie-in-softengineering.tistory.com/entry/OS-Ch6-%EA%B5%90%EC%B0%A9%EC%83%81%ED%83%9C)|
|김민우||
|황인준||
|황하림||

<br>

### 질문

1. 교착 상태 해결 방법 중 프로세스가 시작 초기에 자신이 사용하려는 모든 자원을 한꺼번에 점유하거나, 그렇지 못할 경우 자원을 모두 반납하는 방법이 있는데, 이의 단점은?
- 프로세스가 자신이 사용하는 모든 자원을 알기가 어려움
- 자원의 활용성이 떨어짐
- 많은 자원을 사용하는 프로세스가 적은 자원을 사용하는 프로세스보다 불리함
- 결국 **일괄 작업 방식**으로 동작함

2. 아사 현상과 교착 상태의 차이점
- 아사는 운영체제의 정책 중 "공평성"을 지키지 않는 스케줄링으로 인해서 특정 프로세스가 자원을 할당받지 못하는 상황을 의미
- 교착 상태의 경우 프로세스가 작업을 진행하다가 4개의 조건을 만족하는 상황에서 두 개 이상의 프로세스가 작업을 진행하지 못하는 "무한 대기"상황에 빠지는 것을 의미
- 아사의 경우 정책을 보완하면 충분하게 해결할 수 있지만, 교착 상태의 경우는 정책이나 알고리즘으로 해결하기가 어려움

데드락과 기아는 자원 할당을 무한히 대기한다는 점에서는 같아보이나 차이점이 있습니다.
데드락은 여러 프로세스나 스레드가 절대 발생하지 않는 이벤트나 자원 할당을 위해 무한정 대기를 합니다.
데드락은 프로세스의 상태 중 blocked 상태에서 발생합니다.
기아는 프로세스가 CPU 자원의 할당을 무한히 대기합니다.
기아는 CPU 스케쥴링과 관련이 있습니다.
기아는 프로세스의 상태 중 ready 상태에서 발생합니다.

3. 교착 상태와 병목 현상의 차이점 
- 병목 현상 : 여러 구성 요소가 동시에 실행될 때 가장 느린쪽에 속도를 맞춰 전체 시스템 속도가 느려지는 현상
- 교착 상태 : 둘 이상의 주체가 서로 상대방이 사용중인 자원을 쓰기 위해 대기하는 현상
이 둘은 발생 원인이 다르다.
 
4. 은행원 알고리즘에서 자원이 낭비되는 이유는?
- 항상 최악의 경우를 고려하여 가용할 수 있는 자원을 계산하므로 자원을 효율적으로 사용하지 못한다.   

5. 교착 상태 해결을 위한 기법인 검출은 윈도우/유닉스 환경과 DB 환경에서 서로 다른 매커니즘으로 구현된다. 각각 적용되는 매커니즘이 무엇이며 이로 인한 이점은?
- 윈도우/유닉스 환경에선 교착 상태 원인 분석 및 해결 비용이 재부팅, 프로세스 종료보다 상대적으로 비용이 비싸다. 따라서, 타임 아웃 기법을 사용한다.
- DB는 데이터 일관성이 매우 중요하므로 롤백, 체크포인트 기법을 사용한다.   
6. 

7. 

8. 

</div>
</details>

<details>
<summary>7Chapter</summary>
<div markdown="1">
<br>

### 정리

|이름|링크|
|:---:|:----------:|
|임규리||
|김민우||
|황인준||
|황하림||

<br>

### 질문

1. 컴파일러와 인터프리터의 차이
    
    컴파일러
    
    - 소스코드를 컴퓨터가 실행할 수 있는 기계어로 번역한 후 한꺼번에 실행
    - 컴파일러를 사용하는 프로그래밍 언어는 사용할 변수를 먼저 선언한 후 코드 작성
    - 변수 선언은 오류를 찾고 코드를 최적화하기 위해 반드시 필요한 작업
    - 실행 전에 소스코드를 점검하여 오류를 수정하고 필요 없는 부분을 정리하여 최적화된 실행 파일을 만듦
    - **초기 스캔 시간이 오래 걸리지만, 한 번 실행 파일이 만들어지고 나면 빠름**
    - **기계어 번역 과정에서 더 많은 메모리 사용**
    - 크고 복잡한 프로그램에는 컴파일러를 사용
    
    인터프리터
    
    - 소스코드를 한 행씩 번역하여 실행
    - **실행 시간이 느림**
    - **메모리 효율이 좋음**
    - **프로그램을 실행시키고 나서 오류를 발견하면 실행 중지, 실행 후에 오류 발견**
    - 같은 일을 반복하는 경우나 필요 없는 변수 확인 불가
    - 간단한 프로그램에는 인터프리터 사용

2. 버디 시스템 (개념과 장단점)
    - 프로세스의 크기에 맞게 메모리를 1/2로 자르고 프로세스를 메모리에 배치
    - 나뉜 메모리의 각 구역에는 프로세스가 1개만 들어감
    - 프로세스가 종료되면 주변의 빈 조각과 합쳐서 하나의 큰 덩어리를 만듦
    - 장점 : 가변 분할 방식보다 효과적인 공간 관리 → 비슷한 크기의 덩어리가 서로 모여 있어 통합이 쉽기 때문
    - 단점 : 고정 분할 방식이 메모리 관리 측면에서 더 단순
    
    동적 할당과 임베디드 시스템에서도 버디 시스템이 더 좋은 선택인지는 상황에 따라 다릅니다. 버디 시스템은 특정 상황에서 유용할 수 있지만, 모든 상황에 적합하지는 않습니다. 일반적으로 다음과 같은 경우에는 버디 시스템이 동적 할당 및 임베디드 시스템에서 더 적합할 수 있습니다.
    
    1. 메모리 할당과 해제의 빈도가 적은 경우: 동적 할당이 자주 발생하지 않거나, 메모리 할당이 고정된 크기의 블록으로 이루어지는 경우에는 버디 시스템이 더 효율적일 수 있습니다. 이러한 상황에서는 버디 시스템이 메모리 관리를 단순화하고 외부 단편화를 방지할 수 있습니다.
    2. 제한된 자원이 있는 경우: 임베디드 시스템에서는 시스템 자원이 제한되어 있을 수 있습니다. 이런 경우에는 메모리 관리를 간단하게 유지하면서도 메모리 사용을 최적화할 수 있는 버디 시스템이 적합할 수 있습니다.
    
    그러나 모든 상황에 있어서 버디 시스템이 항상 최적의 선택은 아닙니다. 동적 할당이 빈번하게 발생하거나 메모리 할당이 다양한 크기의 객체에 대해 이루어지는 경우에는 다른 메모리 관리 기법이 더 적합할 수 있습니다. 종합적으로, 상황과 요구 사항을 고려하여 적절한 메모리 관리 기법을 선택해야 합니다.

3. 메모리 분할 방식과 메모리 오버레이는 각각 메모리를 어떻게 사용하는지 차이
   - 메모리 분할 방식은 사용할 메모리를 가변 혹은 고정 크기로 분할하는 것으로 프로세스를 해당 메모리에 할당
   - 메모리 오버레이는 물리적인 메모리보다 프로그램이 필요로 하는 메모리 공간이 더 클 때 사용되는 메모리 관리 기법으로 메모리를 분할하는 것이 아닌 프로세스를 분할하여 물리적인 메모리에 일부씩 적재하는 방법(책에서는 사용하는 특정 기능만 메모리에 적재)으로 다 들어가지 못하면 스왑영역에 보관됨
   	- 메모리가 초과되고 바로 스왑영역으로 가는것이 아니라 메모리의 캐싱 메모리를 없애고 해당 부분에 넣고 남는 부분을 스왑영역에 보관한다
   
4. 네트워크 세그먼테이션과 가상 메모리 관리에서 세그먼테이션의 차이, 각각 뭘 분리하고 왜 분리하는지?
   - 가상 메모리에서 세그먼테이션은 프로세스의 주소공간을 논리적인 단위(코드 세그먼트, 데이터 세그먼트, 스택 세그먼트 등)로 분할하고 각 세그먼트는 크기가 다를 수 있으며 동적으로 할당됨
   - OSI 7계층의 전송 계층에서 전송되는 데이터를 세그먼테이션하여 분할된 것이 세그먼트
  
5. 현재 메모리 용량보다 큰 프로세스를 실행할 수 있는 이유는?
   - 캐시 메모리 영역을 해제하여 여유 공간을 만든다.
   - 이로 부족한 경우 스왑 기능을 통해 디스크 일부를 메모리처럼 사용 가능하도록 한다.
6. 현대 OS 대부분 메모리 배치 정책으로 페이징 기법을 채택하는 이유는?
   - 프로세스마다 메모리를 같은 크기로 나누므로 조각 모음과 같은 오버헤드가 없어 메모리 관리가 상대적으로 편하다.
7. 실행중인 프로세스가 없어도 메모리 용량이 부족한 이유는? (재부팅 직후 컴퓨터 성능이 상대적으로 안좋은 이유)
  - 모든 프로세스는 최초 실행 시 디스크에서 가져와 메모리에 올린다. 프로세스 종료 후에도 OS에 의해 메모리에 캐싱되어 이후 실행시 디스크를 거치지 않고 바로 실행된다.
8. OS가 추상화 기법을 사용하는 사례와 이점
  - OS는 커널단에서 물리 메모리 주소를 추상화한다.
  - 이를 통해, 현 메모리 상태에 따라 사용자 프로세스로부터 리소스를 보호할 수 있다.

#### 차주 다시 이야기 필요한 문제 : 자바에서 gradle과 maven를 통해 사용되는 라이브러리들은 동적라이브러리인가 정적 라이브러리인가?

</div>
</details>

<details>
<summary>8Chapter</summary>
<div markdown="1">
<br>

### 정리

|이름|링크|
|:---:|:----------:|
|임규리||
|김민우||
|황인준|[정리 링크](https://github.com/InJun2/TIL/blob/main/BookStudy/SE/쉽게배우는운영체제/Chapter8.md)|
|황하림||

<br>

### 질문

1. 페이지 테이블이 프로세스와 운영체제 영역에 각각 있는데 각각의 용도는 무엇인지
- 프로세스의 페이지 테이블 : 가상 주소와 물리 주소 간의 매핑 정보를 저장하는 자료구조로 각 프로세스는 고유한 주소 공간을 가지고 있음. 운영 체제는 해당 프로세스의 페이지 테이블을 사용하여 가상 주소를 물리 주소로 변환
- 운영체제 영역의 페이지 테이블 :  프로세스의 페이지 테이블을 관리하기 위한 구조로 페이지 테이블 관리자는 각 프로세스의 페이지 테이블에 대한 접근을 제어 및 메모리 관리를 수행하는 역할

1-2. 페이지 테이블이 운영체제 영역에 있는 이유
- 페이지 테이블 관리는 시스템에 여러 프로세스가 존재하고 프로세스마다 페이지 테이블이 하나씩 존재하기 때문인데 메모리 관리자는 특정 프로세스가 실행할 때마다 페이지 테이블을 참조하여 가상 주소를 물리 주소로 변환하는 작업을 반복하는데 페이지 테이블은 메모리 관리자가 자주 사용하는 자료 구조 이므로 빨리 접근하기 위해 페이지 테이블은 물리 메모리 영역 중 운영체제 영역에 일부분 모아놓음

2. 페이지 테이블 매핑 방식에서 역매핑만 페이지 테이블 기준 레지스터(PTBR)이 필요 없는 이유와 다른 매핑 방식에서 해당 레지스터가 하는 역할
- 역매핑은 물리 주소에서 가장 주소로 매핑을 수행하기 때문에 페이지 테이블을 탐색하기 위한 레지스터가 필요없음. 역매핑의 역매핑 테이블은 1개이기 때문.
- 다른 매핑 방식에서는 페이지 테이블의 시작 주소를 가르켜 탐색을 위한 테이블의 위치를 바로 접근할 수 있음. ( 집합-연관 매핑 방식에서는 디렉터리 테이블의 시작 주소를 가르킴 )

2-2. 프로세스마다 테이블 기준 레지스터를 가지고 있는 이유
- 테이블 기준 레지스터는 프로세스 제어 블록 안에 존재하여 프로세스 내부에 존재하고, 프로세스가 메모리에 접근하려 할때 메모리 관리자가 페이지 테이블을 확인하기 용도

3. 논리 주소와 가상 주소의 차이
논리 주소(상대 주소)는 물리 메모리의 주소 공간에 비례하고, 가상 주소는 물리 메모리 공간이 아닌 가상의 주소 공간을 가짐

4. 세그먼테이션-페이징 혼용 기법
사용자 입장에서는 세그먼테이션 기법을 사용하고 메모리 관리자 입장에서는 페이징 기법을 사용하는 가상 메모리 관리 기법

메모리 보호 및 중복 정보를 세그먼테이션 테이블에서 관리함으로써 메모리 관리를 효율적으로 할 수 있음 

→ 메모리 접근 권한 검사 시행 시기 : 가상 주소에서 물리 주소로 주소 변환이 일어날 때마다

5. 
   
6. 

7. 

8. 

</div>
</details>

<details>
<summary>9Chapter</summary>
<div markdown="1">
<br>

### 정리

|이름|링크|
|:---:|:----------:|
|임규리||
|김민우||
|황인준|[정리 링크](https://github.com/InJun2/TIL/blob/main/BookStudy/SE/쉽게배우는운영체제/Chapter9.md)|
|황하림||

<br>

### 질문

1. p.425 PTE의 맨 앞에 있는 페이지 번호는 8장에서 설명한 주소 변환 방식 중 직접 매핑에서는 필요없다. → 이유    
**직접 매핑** 
- 페이지 테이블 **전체**가 물리 메모리의 운영체제 영역에 존재하는 방식
- 물리 메모리를 페이지 단위로 나누고 가상 주소 공간의 페이지와 물리 메모리의 페이지를 일대일 대응 시킴
- 가상 주소의 페이지 번호 = 물리 메모리의 페이지 번호
- 변환이 필요 없음  

p.425 그러나 연관 매핑에서는 페이지 번호와 프레임 번호가 둘 다 필요하다. → 이유  
**연관 매핑**
- 전체 페이지 테이블을 스왑 영역에 두고 페이지 테이블의 **일부**를 물리 메모리에 가져오는 방식 → 변환 색인 버퍼 사용 (페이지 번호, 프레임 번호)


2. 세그먼테이션 오류와 페이지 부재의 차이  
세그먼테이션 오류  
- 해결방법 : 프로세스 강제 종료
- 원인 : 사용자 프로세스의 메모리 접근 관련 오류
- 영향 : 주로 개별 프로세스에 영향을 미침, 오류를 일으킨 프로세스만 종료되거나 영향을 받음
- 비용 : 비교적 적게 듬. 프로세스 종료 후 재시작은 간단한 편

페이지 부재  
- 원인 : 요구 페이지의 물리 메모리 부재
- 해결방법 : 스왑
- 영향 : 시스템 전체에 영향을 미칠 수 있음, 메모리 부족으로 인해 여러 프로세스가 느려지거나 작동을 멈출 수 있음
- 비용 : 더 큼. 디스크에서 페이지를 가져오는 작업은 디스크 I/O에 의존하며 상대적으로 느린 작업임

3. goto문 사용 지양 이유
- 캐시 적중률을 낮춤
    - 지역성에 근거하여 현재 실행하는 행과 가까운 행을 캐시 메모리로 가져오고 있는데 goto문을 사용해버리면 이미 가져온 데이터가 쓸모없어짐
- 코드 가독성 저하 : 스파게티 코드가 될 우려
- 오류 발생 가능성 증가 : 의도치 않은 동작 유발
- 유지 보수의 어려움 : 이해하기 어려움
- 구조적인 문제 : 구조적 프로그래밍의 원칙을 어김 (명확성, 예측가능성, 이해성, 유지보수성 등)
- 대체 가능성 : if문 or 반복문 등으로 대체 가능

getter/setter 지양과 비슷한 맥락에서 지양해라! 일 뿐이지 아예 사용하지 마라! 는 아닌 듯함. 오히려 goto문을 사용할 때 더 깔끔하다는 블로그 참조
[https://cypsw.tistory.com/entry/C-GOTO-를-쓰지-말라는-개소리](https://cypsw.tistory.com/entry/C-GOTO-%EB%A5%BC-%EC%93%B0%EC%A7%80-%EB%A7%90%EB%9D%BC%EB%8A%94-%EA%B0%9C%EC%86%8C%EB%A6%AC)

4. FIFO 페이지 교체 알고리즘과 2차 기회 페이지 교체 알고리즘의 공통점과 차이점
- 둘 다 큐를 사용하여 FIFO 순서를 보장하는 것이 공통점
- FIFO는 페이지가 성공을 해도 성공한 페이지의 위치를 그대로 두기 때문에 최근에 실행된 페이지가 스왑아웃 될 수 있으나 2차 기회 페이지 교체 알고리즘의 경우는 페이지가 성공했을 경우 해당 페이지를 큐에 다시 삽입하여 나중에 스왑아웃되게 뒤로 이동 시킴
   
5. 물리메모리와 스레싱과의 관계와 스레싱 해결 방안
- 스레싱은 페이지 부재가 많이 발생하여 I/O 바운드로 인하여 멈춘 것 처럼 보이는 현상인데 물리 메모리가 크다면 스왑영역으로 넘어가는 페이지가 적어져 이러한 페이지 부재가 많이 일어나지 않게 됨
- 물리 메모리 확보 : 위의 방법
- 페이지 교체 알고리즘 개선 : 페이지 부재율을 감소시켜 성능을 개선하고 스레싱 해결
- 동적 자원 할당 : 시스템이 현재 상태를 모니터링하여 동적으로 자원을 재할당
- 캐시 메모리 사용 : 캐시 메모리를 통해 메모리 액세스의 지역성을 활용하여 스레싱을 완화
   
6. 

7. 

8. 

</div>
</details>

<details>
<summary>10Chapter</summary>
<div markdown="1">
<br>

### 정리

|이름|링크|
|:---:|:----------:|
|임규리||
|김민우||
|황인준||
|황하림||

<br>

### 질문

1. 

2. 

3. 
   
4. 
   
5. 
   
6. 

7. 

8. 

</div>
</details>

<details>
<summary>11Chapter</summary>
<div markdown="1">
<br>

### 정리

|이름|링크|
|:---:|:----------:|
|임규리||
|김민우||
|황인준||
|황하림||

<br>

### 질문

1. 

2. 

3. 
   
4. 
   
5. 
   
6. 

7. 

8. 

</div>
</details>

<details>
<summary>12Chapter</summary>
<div markdown="1">
<br>

### 정리

|이름|링크|
|:---:|:----------:|
|임규리||
|김민우||
|황인준||
|황하림||

<br>

### 질문

1. 

2. 

3. 
   
4. 
   
5. 
   
6. 

7. 

8. 

</div>
</details>
