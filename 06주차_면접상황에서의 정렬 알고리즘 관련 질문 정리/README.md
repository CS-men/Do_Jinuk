# < 6주차 - 면접상황에서의 정렬 알고리즘 관련 질문 정리 >

| - 220406 작성완료 | 작성자 : `도진욱` / 학습 기간 : *2022.03.31. ~ 2022.04.06.* |
| ----------------- | ----------------------------------------------------------: |


---

<br>

 스터디원들과 의논해 본 결과, 우리가 각 회사 입사 면접에 대해 조사하기 전에, 우리가 가장 많이 받게 될 질문은 비전공자로서 알아야 할, 배웠던, 알고리즘 관련한 질문들이지 않을까 하였다. 또한, 배웠음에도 제대로 답을 하지 못한다는 것은 반성해야 할 점이며, 그것을 고쳐나가려고 우리가 함께 모여 공부를 하고 있지 않나 생각하였다. 그러므로 이번 한 주는 면접상황에서 받게 될 여러가지 알고리즘 관련한 질문들을 조사해 보았고, 그 중 정말 유용할 정렬 알고리즘에 관한 질문들에 대해서 정리해 보았다. 이 끝은 모든 알고리즘에 대해 이해하는 것이어야 하겠지만은, 그러기 위해 지금 내가 할 수 있는 건 기초적인 정렬 알고리즘에 대한 답변 제시인 것 같다. 아래는 내가 이번 한 주 동안 조사해 본 정보에 대한 서술이다. (참고한 출처는 각 질문에 대한 답변 혹은 파일의 하단에 모두 링크를 걸어두었습니다.)

---

<br>

- **정렬이 필요한 이유가 무엇인가요?**

  - 이 질문에 대해서는 따로 프로그래밍을 배우지 않은 사람이어도 할 수 있는 질문인데, 만약 개발 직군 면접 상황에서 이러한 질문을 마주쳤을 때 대처하기란 쉽지 않을 수 있다. 왜냐하면, '정렬'이라고 한다면 배웠던 여러 정렬 알고리즘을 떠올릴 것이고 그것이 왜 필요한지는 정작 생각을 해보지 않고 배우는 과정이었으니 자연스럽게 혹은 억지로 학습하였을 것이기 때문이다. 아니, 적어도 나는 그랬다. 또한 더 솔직하게 말하자면, '정렬 알고리즘'이라고 한다면 '왜 필요한가?' 대신, '왜 필요하지 않은가?' 라는 질문에 더 대답을 할 수 있을 것 같다. 하지만, 이 질문은 '정렬 알고리즘'의 필요성에 대해서 물어본 것이 아니고, 그저 '정렬'이 왜 필요한가? 라는 질문이다. 그리고 그 대답으로 필요한 이유를 머릿 속에서 얼른 끄집어 낼 수 있어야 할 것이다.

  - 그 대답은 다음과 같이 할 수 있을 것이다.

    > 정렬이 필요한 이유는, 정렬이 되어 있다면 자료 탐색에 있어서 편리함을 가질 수 있기 때문이다. 정렬이 되어 있다면, 찾고자 하는 값을 log N의 시간 복잡도 만으로 찾을 수가 있기 때문입니다. 또한 그 정렬 과정마저도 빠르게 해결하고자 여러가지의 정렬 알고리즘을 제시하였고 이를 배웠습니다. 즉 '정렬'은 어떠한 문제를 해결하려 할 때에, 해결 속도를 최소화 하는 목적에 있어서 가장 적합한 과정이라고 생각합니다.

---

<br>

- **시간 복잡도란 무엇인가요?**

  - 정렬 알고리즘을 배웠을 때 가장 난해했던 것이 '시간 복잡도' 라는 개념이었던 것 같다. 내가 받아들이기로는, 어느정도의 시간이 걸리느냐 라는 것을 수학적으로 표현한 것. 이라고 생각하였다. 조사를 하다 보니 '공간 복잡도'라는 개념도 존재하는데, 일단 이번 한 주는 시간 복잡도에 대해 완벽하게 이해를 하고자 하였다.

  > 시간 복잡도(Time Complexity)
  >
  > : **알고리즘의 수행 시간을 평가하여 표기하는 것**. 
  >
  > - 수행 시간은 실행 환경에 따라 다르게 측정되기 때문에, 기본 연산의 실행 횟수로 수행 시간을 평가한다.
  >
  > - 주로 점근적 표기법 중 '빅 오 표기법'을 이용하여 나타낸다. 그 이유는, 최악의 경우에도 해당 알고리즘이 어떤 성능을 낼 수 있는지 가늠해 볼 수 있기 때문이다. 즉, 빅 오 표기법을 사용한다면, 최악의 시나리오로 아무리 오래 걸려도 이 시간보다 덜 걸린다는 것 뜻하게 된다.
  >
  > 시간 복잡도의 표기에 대해서는 (https://yoongrammer.tistory.com/79)에서 공부할 수 있으며, 아래는 빅 오 표기법으로 표현한 알고리즘의 시간복잡도 차트이다.
  >
  > ![https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fs0pox%2Fbtq6Mbphdwr%2Fs5K0D58hi5hiSrBuxmHHwk%2Fimg.png](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fs0pox%2Fbtq6Mbphdwr%2Fs5K0D58hi5hiSrBuxmHHwk%2Fimg.png)
  >
  > 즉, 시간 복잡도를 낮출 수 있는 것 자체가 프로그램의 성능과 연관이 크다는 것을 알 수 있다.



*(출처 : https://yoongrammer.tistory.com/79, https://www.bigocheatsheet.com/)*

---

<br>

- **Sorting Algorithm이 종류가 많은데, 그 이유가 무엇일 것 같나요?**

  - 이 질문에 대해서는 평소에 내가 생각하고 있던 바가 있었다. 그것은, 과거부터해서 시간이 지나면 지날수록 여러가지의 알고리즘을 제시하게 되었고 그 중에서 효율성을 인정받은 알고리즘들은 많은 주목을 받아서 지금의 내가 배우게 되었다고 생각하였다. 나의 교수님이 하셨던 말씀 중에, 불편함이 있어야 더 편한 것을 찾을 수 있다는 말씀과 연관지어 설명할 수 있다고 생각한다.

  - 아래는, 한 기술 블로그에서 작성해 놓은 답안이다. (물론 나의 답보다 더 면접상황에 적합한 답변일 것 같다.)

    > 정렬 알고리즘의 종류가 많은 이유.
    >
    > 1. 과거부터 계속해서 더 나은 정렬 알고리즘을 찾기 위해 연구하다보니, 기존의 정렬 알고리즘을 대체할 방안이 계속 나왔다.
    > 2. 정렬 알고리즘 하나가 어느 상황에서나 효율적인 것이 아니고, 주어진 상황에 따라 *trade-off*가 있기 때문이다.

    - (trade-off : 상충 관계. 다른 측면에서 이득을 얻으면서 손해가 수반되는 것.)

---

<br>

- **Quick sort에 대해서 설명해 주세요.**

  - 이번 한 주 동안 정렬 알고리즘에 대해 정말 많이 찾아보았고, 특히나 면접 상황에서의 정렬 알고리즘에 대한 질문을 찾아보게 되었는데, 그 중에서도 가장 많이 받은 질문이 이 질문이었다고 한다. 시간이 좀 지난 예전 면접 상황에서는 손코딩을 시킨 경우도 있다고 하였고, 얼마 전 까지만 해도 구현하는 과정에 대해 설명해 달라고 한 적도 있었다고 한다. 그렇기에 Quick Sort에 대해 정말 많은 공부를 할 수 있었고, 아래는 내가 가장 도움을 많이 받은 한 사이트 주소의 첨부와 내가 배운 내용에 대한 요약을 하려 한다.

  > 퀵 정렬(Quick sort) -
  >
  > : **불안정 정렬**~~(안정, 불안정에 대해서는 저번 주에 학습하였다.)~~이며, 다른 원소와의 비교를 통해 정렬을 수행하는 **비교 정렬**이다. 또한 **분할 정복 알고리즘**의 하나로, 이름 그대로 **매우 빠른 수행속도**를 가진다. Merge sort와는 달리 퀵 정렬은 리스트를 비균등하게 분할한다.
  >
  > (나는 개인적으로 퀵 정렬을 *pivot이 있는 알고리즘* 이라고 생각하기로 하였다.)
  >
  > 정렬 과정은 다음과 같다.
  >
  > 1. 리스트 안의 한 요소를 선택한다. 이는 pivot이라 부른다.
  > 2. pivot을 기준으로 pivot보다 작은 요소들은 모두 피벗의 왼쪽으로 옮기고, pivot보다 큰 요소들은 모두 피벗의 오른쪽으로 옮긴다. (실제 코드 작성 중에 pivot과 동일한 크기를 가진 요소들을 담는 리스트도 생성할 수 있었다.)
  > 3. pivot을 제외한 왼쪽 리스트와 오른쪽 리스트를 다시 정렬한다. (재귀를 통해 위 과정을 똑같이 수행하게 한다.)
  > 4. 위 과정을 리스트의 크기가 0이나 1이 될 때 까지 반복하게 하고 모두 병합한다.
  >
  > 아래는 퀵정렬에 대한 그림이다.
  >
  > ![https://gmlwjd9405.github.io/images/algorithm-quick-sort/quick-sort.png](https://gmlwjd9405.github.io/images/algorithm-quick-sort/quick-sort.png)
  >
  > 
  >
  > 물론 퀵정렬의 단점도 있는데, 단점은 다음과 같다.
  >
  > 단점 : 정렬된 리스트에 대해서는 퀵 정렬의 불균형 분할에 의해 오히려 수행시간이 더 많이 걸린다.



(출처 : https://gmlwjd9405.github.io/2018/05/10/algorithm-quick-sort.html)

---

<br>

- **버블 정렬(Bubble Sort)에 대해 설명해 주세요.**

  - 이 질문은 사실, 넣을까 말까 정말 고민을 많이하였다. 왜냐하면, 내가 기억하기로는 정렬 알고리즘에 대해 가장 먼저 배웠던 것이 버블 정렬이어서 너무 관심있게 보았었는데, 배우면서도 이렇게 수행속도가 느린 알고리즘을 '내가 알 필요가 있을까?' 라고 생각했었기 때문이다. 그러면서도 내가 이 질문을 넣은 이유는 무시할 수 없을 만큼 면접 상황에서 Bubble Sort와 관련하여 정말 많은 질문을 받았다고 들었기 때문이다. 그렇기에 이번 한 주, 정확하게 버블 정렬에 대해 알고 끝장내기로 하였다.

  - 아래는 내가 공부한 내용에 대한 요약이다.

    > 버블 정렬은 서로 인접한 두 원소를 비교하며 정렬하는 알고리즘이다.
    >
    > 맨 처음의 인덱스부터 가장 마지막 인덱스까지 비교하며 정렬할 수 있다.
    >
    > 그런 만큼, 시간 복잡도는 O(n^2)으로 다른 정렬 알고리즘보다 상대적으로 높다.
    >
    > 아래는 정렬 알고리즘의 그림이다.
    >
    > ![https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FdF7CXf%2FbtrunN5i9wZ%2FwDQ3px86zQFffgoq8X6jk0%2Fimg.png](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FdF7CXf%2FbtrunN5i9wZ%2FwDQ3px86zQFffgoq8X6jk0%2Fimg.png)
    >
    > 
    >
    > 위 그림처럼 요소가 5개인 상황에서도 요소끼리의 비교를 너무 많이 하게 되는데, 숫자가 늘어났을 때는 더 심각한 속도를 예상할 수 있다.
    >
    > 각 정렬 알고리즘의 속도를 애니메이션으로 비교한 사이트 'Sorting Algorithms Animations'(https://www.toptal.com/developers/sorting-algorithms)에서 쉽게 비교할 수 있다.

---

<br>

기타 참고 사이트 :

신입 면접시 자주 나왔던 질문(https://okky.kr/article/673648)

면접 질문 및 답변 정리(https://velog.io/@xoqja055/)

Sorting Algorithms Animations(https://www.toptal.com/developers/sorting-algorithms)

