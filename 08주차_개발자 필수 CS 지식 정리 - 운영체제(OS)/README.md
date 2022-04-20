# < 8주차 - 개발자 필수 CS 지식 정리 - 운영체제(OS) >

| - 220420 작성완료 | 작성자 : `도진욱` / 학습 기간 : *2022.04.14. ~ 2022.04.20.* |
| ----------------- | ----------------------------------------------------------: |


---

<br>

 지난 5주 동안, 팀원들과 함께 개발 직군 면접에 대한 지식을 학습하였는데, 그 동안 배운 내용에 대해 더 확실하게 알아가는 시간을 가졌었다. 그러고 앞으로는 각자 파트를 맡아 학습하고 그 내용에 대해 발표하는 시간을 가져보려고 한다. 나는 그 중에서도 컴퓨터 공학에서 배울 수 있는 CS 지식을 학습하고 그에 대한 지식을 정리해보려고 한다. 

이번 한 주는 **운영체제**에 관련하여 공부해 보았는데, 그 이유는 본 파일 최하단의 '컴퓨터 공학 기초가 중요한 이유' 링크에서 확인할 수 있었다. 즉, 기업에서는 운영체제에 대한 이해가 깊은 개발자를 찾고 있기 때문에 이번 한 주 동안 학습해 보았다. 아래는 내가 이번 한 주 동안 조사하고 공부한 내용을 선별하여 정리해 보았다. (참고한 출처는 각 질문에 대한 답변 혹은 파일의 하단에 모두 링크를 걸어두었습니다.)

---

<br>

## 운영 체제(OS)란 무엇인가?

> **운영 체제(OS, Operating System)**
>
> : 컴퓨터 시스템의 자원들을 효율적으로 관리하며, 사용자가 컴퓨터를 편리하고, 효과적으로 사용할 수 있도록 환경을 제공하는 여러 프로그램의 모임. 컴퓨터 사용자와 컴퓨터 하드웨어 간의 인터페이스로써 다른 응용프로그램이 유용한 작업을 할 수 있도록 환경을 제공해 준다.
>
> 즉, 운영 체제는 **컴퓨터가 소프트웨어와 통신하고 작동하도록 하는 소프트웨어 프로그램** 이다.
>
> - 종류로는 Windows, Linux, UNIX, MS-DOS등이 있다.
>
> - 운영체제의 기능(외우지 말고 이해만!) :
>   1. 프로세서, 기억장치, 입출력장치 등의 자원을 관리한다.
>   2. 자원을 효율적으로 관리하기 위해 자원의 스케줄링 기능을 제공한다.
>   3. 사용자와 시스템 간의 편리한 인터페이스를 제공한다.
>   4. 시스템의 각종 하드웨어와 네트워크를 관리, 제어한다.
>   5. 데이터를 관리하고 데이터 및 자원의 공유 기능을 제공한다.
>   6. 시스템의 오류를 검사하고 복구한다.
>   7. 자원 보호 기능을 제공한다.
>   8. 입출력에 대한 보조 기능을 제공한다.

*(출처 : https://coding-factory.tistory.com/300)*

<br>

## 프로세스란 무엇인가?

> **프로세스** : 컴퓨터에서 연속적으로 실행되고 있는 컴퓨터 프로그램. 
>
> - 프로그램은 일반적으로 하드 디스크 등에 저장되어 있는 실행코드를 뜻하고, 프로세스는 프로그램을 구동하여 프로그램 자체와 프로그램의 상태가 메모리 상에서 실행되는 작업 단위를 지칭한다. 만약 하나의 프로그램을 여러 번 구동한다면, 여러 개의 프로세스가 메모리 상에서 실행되게 된다.
>
> - 프로세스의 상태는 다음의 이미지로 설명이 가능하다.
>
>   ![https://upload.wikimedia.org/wikipedia/commons/thumb/8/83/Process_states.svg/1280px-Process_states.svg.png](https://upload.wikimedia.org/wikipedia/commons/thumb/8/83/Process_states.svg/1280px-Process_states.svg.png)
>
>   - Create : 프로세스를 생성한다.
>   - Waiting : 프로세스가 시그널 수신, 입출력 완료 등 어떤 사건을 기다리는 상태이다.
>   - Running : 프로세스가 CPU를 차지하고 명령어들이 실행되게 된다.
>   - Blocked : 보류 상태를 뜻하며, 프로세스가 요청한 사건이 즉시 만족되지 않아 기다리는 상태이다.
>   - Terminated : 프로세스의 실행 종료 상태를 뜻한다.
>   - Swap space란 active 상황에서 inactive 상황으로 전환시킬 때에 존재하게 되는 공간으로, '예비 공간'이라고 설명할 수 있다. 메모리에 다른 프로세스를 대체하여 실행시켜야 할 때 swap되고, 이 때 해당 프로세스를 종료시키진 않고 하드디스크, SSD같은 저장소에 잠깐 저장을 시키게 된다. 이렇게 프로세스 단위로 전환시키는 것을 'Swap out'이라고 한다.
>
> - 특징(외우지 말고 이해만!) :
>
>   1. 프로세스는 각각 독립된 메모리 영역을 할당받는다.
>   2. 기본적으로 프로세스 당 최소 1개의 스레드(메인 스레드)를 가지고 있다.
>   3. 각 프로세스는 별도의 주소 공간에서 실행되며, 한 프로세스는 다른 프로세스의 변수나 자료구조에 접근할 수 없다.
>   4. 한 프로세스가 다른 프로세스의 자원에 접근하려면 프로세스 간의 통신(IPC, inter-process communication)을 사용해야 한다.

*(출처 :*

*https://hyonee.tistory.com/95*

*https://ko.wikipedia.org/wiki/%ED%94%84%EB%A1%9C%EC%84%B8%EC%8A%A4*

*https://developyo.tistory.com/198*

*https://jhnyang.tistory.com/103)*

<br>

## 스레드란 무엇인가?

> **Thread(스레드)** : CPU 사용의 기본 단위. 프로세스 내에서 실행되는 여러 흐름의 단위를 말한다. 또한, 프로세스의 특정한 수행 경로를 뜻하기도 하며, 프로세스가 할당받은 자원을 이용하는 실행 단위이다.
>
> ![https://gmlwjd9405.github.io/images/os-process-and-thread/multi-thread.png](https://gmlwjd9405.github.io/images/os-process-and-thread/multi-thread.png)
>
> : 스레드는 프로세스 내에서 Stack만 할당받고 Code, Data, Heap 영역은 공유하여 사용한다.
>
> - 한 프로그램은 하나의 스레드를 가지는 것이 일반적이지만, 프로그램 환경에 따라 둘 이상의 스레드를 동시에 실행할 수 있는데, 그것을 *MultiThread(멀티 스레드)*라고 한다.
>
>   ![https://upload.wikimedia.org/wikipedia/commons/thumb/a/a5/Multithreaded_process.svg/1920px-Multithreaded_process.svg.png](https://upload.wikimedia.org/wikipedia/commons/thumb/a/a5/Multithreaded_process.svg/1920px-Multithreaded_process.svg.png)
>
>   위는 멀티스레드(2개)를 실행하고 있는 하나의 프로세스를 설명한 그림이다. 즉, 여러 개의 스레드를 효과적으로 실행할 수 있게끔 하는 것이다. 또한, 멀티 스레딩은 위처럼 프로그램 안에서 병렬 처리를 가능하게 하면서 하나의 코어에 대한 이용성을 증가시키는 것에 중점을 두고 있다.
>
> - 당연하게도 면접 상황에서는 프로세스와의 차이점을 빈번하게 물어보곤 한다. 이에 대한 답변은 다음과 같다.
>
>   > 스레드는 '흐름의 단위'이므로 CPU에서는 작업을 할 때 스레드를 최소 단위로 삼고 작업을 하게 된다. 반면에, 운영체제는 이렇게 작은 단위보다는 프로세스를 최소 작업 단위라고 보고 작업을 한다는 것이다.
>   >
>   >  그러므로, 만약 한 프로세스를 실행하다가 오류가 발생하여 프로세스가 강제로 종료된다면, 다른 프로세스에게 영향을 주지 않는다. 다만 스레드는 프로세스 내에 존재하는 개념이며, 하나의 스레드에서 오류가 발생한다면 같은 프로세스 내의 다른 스레드 모두가 강제로 종료된다.

*(출처 :*

*https://ko.wikipedia.org/wiki/%EC%8A%A4%EB%A0%88%EB%93%9C_(%EC%BB%B4%ED%93%A8%ED%8C%85)*

*https://velog.io/@raejoonee/%ED%94%84%EB%A1%9C%EC%84%B8%EC%8A%A4%EC%99%80-%EC%8A%A4%EB%A0%88%EB%93%9C%EC%9D%98-%EC%B0%A8%EC%9D%B4*

*https://gmlwjd9405.github.io/2018/09/14/process-vs-thread.html)*

<br>

## 데드락(DeadLock, 교착상태)이란 무엇인가?

> 데드락은 두 개 이상의 프로세스나 스레드가 서로 자원을 기다리면서 무한히 기다리게 되는 상태를 말한다. 두 개 이상의 작업이 서로 다른 작업이 끝나기만 기다리고 있기 때문에, 다음 단계로 진행하지 못한다.
>
> 쉽게 말하자면, '시스템 자원에 대한 요구가 뒤엉킨 상태'를 뜻한다.
>
> > ( 더 쉽게 말해, 외나무 다리의 양 끝에서 서로가 비켜주기만을 기다리고만 있는 것이다. )
>
> ![https://postfiles.pstatic.net/MjAxODA5MjZfNCAg/MDAxNTM3OTY4ODE3NjMx.9_awN4b8lLXsYLMQf8ZedACVkoZdxJpAC-mw7DUk05Yg.2fuM-_ltDPAq94Xs8hmzcAmZrHPgNQ3nJF7-0yk3kM8g.PNG.qbxlvnf11/deadlock.png?type=w773](https://postfiles.pstatic.net/MjAxODA5MjZfNCAg/MDAxNTM3OTY4ODE3NjMx.9_awN4b8lLXsYLMQf8ZedACVkoZdxJpAC-mw7DUk05Yg.2fuM-_ltDPAq94Xs8hmzcAmZrHPgNQ3nJF7-0yk3kM8g.PNG.qbxlvnf11/deadlock.png?type=w773)
>
> 이 데드락은 다중 프로그래밍 환경에서 흔히 발생할 수 있는 문제이다.
>
> 
>
> > 데드락 발생 조건 4가지. (이해만!)
> >
> > 1. 상호배제 : 한 번에 하나의 프로세스만 자원을 사용 가능하다.
> > 2. 점유대기 : 프로세스가 할당된 자원을 가진 상태에서, 다른 자원을 기다린다.
> > 3. 비선점 : 프로세스가 어떤 자원의 사용을 끝낼 때까지 그 자원을 가질 수 없다.
> > 4. 순환대기 : 각 프로세스는 순환적으로 다음 프로세스가 요구하는 자원을 가지고 있다.
> >
> > *( 이 조건들이 모두 만족하는 상황에서 교착 상태가 발생할 수 있다고 한다.*
> >
> > *또한, 위 조건들은 서로 완전히 독립적인 조건이 아니므로 좀 애매한 감이 있는 것 같다. 외우진 말자!! )*
>
> 
>
> > 데드락 해결방법은 예방, 회피, 탐지, 복구 이렇게 4가지가 있다.
> >
> > 순서대로,
> >
> > 데드락 발생을 예방하고, 피할 수 있도록 하고, 발생 여부를 탐지할 수 있도록 하고, 탐지되었다면 프로세스를 중지시키는 것을 의미한다.
> >
> > *(이 또한 정말 당연하고, 이를 외우는 건 의미가 없다. 이해만 하자! )*

*(출처 :*

*https://ko.wikipedia.org/wiki/%EA%B5%90%EC%B0%A9_%EC%83%81%ED%83%9C*

*https://blog.naver.com/PostView.naver?blogId=qbxlvnf11&logNo=221366002162&parentCategoryNo=&categoryNo=62&viewDate=&isShowPopularPosts=false&from=postView*

*https://chanhuiseok.github.io/posts/cs-2/)*

<br>

## 프로세스 스케줄링(Process Scheduling)이란 무엇인가?

- 다중 프로그래밍 운영 체제의 필수적인 부분으로, CPU에서 실행 중인 프로세스를 제거하고 특정 전략을 기반으로 다른 프로세스를 선택하는 프로세스 관리자의 활동이다.

- 정말 간단하게, 이는 CPU가 쉬지않고 효율적으로 일하게 할 수 있도록 하는 것이다.

> **프로세스 스케줄링 Queues**
>
> : OS는 Process Scheduling Queues의 모든 'PCB'*(Process Control Block, 프로세스 제어 블록 : 운영체제가 프로세스에 대한 중요한 정보를 저장해 놓는 곳)*를 유지 관리하는데, OS는 각 프로세스 상태에 대해 별도의 큐를 유지하고, 동일한 실행 상태에 있는 모든 PCB는 동일한 큐에 배치된다.
>
> 프로세스의 상태 변경에 따라, PCB는 새로운 Queue로 이동하게 된다.
>
> ![https://www.tutorialspoint.com/operating_system/images/queuing_diagram.jpg](https://www.tutorialspoint.com/operating_system/images/queuing_diagram.jpg)
>
> : 위의 그림처럼 OS의 프로세스 스케줄링 Queue들이 이루어져 있고 PCB의 이동경로를 확인할 수 있다.
>
> - Job Queue : 시스템의 모든 프로세스를 유지한다.
> - Ready Queue : 주 메모리에 있는 모든 프로세스 집합을 실행 준비 상태로 유지한다. 새 프로세스는 항상 이 큐에 넣는다.
> - Device Queue : 장치 큐로, I/O 장치를 사용할 수 없어서 차단된 프로세스가 이 대기열을 구성한다.(I/O Waiting Queue)
>
> Scheduling의 단계는 다음과 같다.
>
> > - 1단계 스케줄링 : 어느 작업부터 시스템의 자원들을 실제로 사용할 수 있도록 할지 결정한다.
> >
> > - 2단계 스케줄링 : 어느 프로세스부터 CPU를 차지할 수 있게 할지 결정한다.
> > - 3단계 스케줄링 : CPU가 사용 가능한 경우 어느 프로세스에게 배당할지 결정한다.

*(출처 :*

*https://www.tutorialspoint.com/operating_system/os_process_scheduling.htm*

*https://coding-factory.tistory.com/308*

*https://ko.wikipedia.org/wiki/%EC%8A%A4%EC%BC%80%EC%A4%84%EB%A7%81_(%EC%BB%B4%ED%93%A8%ED%8C%85))*

---

<br>

마지막으로, 주제와 관련하여 참고하면 좋은 곳 링크입니다.

1. 글 - 컴퓨터 공학 기초가 중요한 이유 (https://media.fastcampus.co.kr/knowledge/dev/computer-sci/)
2. 글 - 운영체제(OS) 면접 예상 질문과 답변 (https://hyonee.tistory.com/95)
3. 글 - 비전공자가 개발자로 취업하기까지의 후기 (https://media.fastcampus.co.kr/knowledge/dev/school_wps_ksu/)
4. 글 - 신입 개발자 면접용 컴퓨터 공학 기본지식 (https://www.clien.net/service/board/lecture/16150836)