---
title: 카드섞기
tags:
  - etc
  - array
  - random
---
[누가 IT시장 취업에 성공하는가](http://www.kyobobook.co.kr/product/detailViewKor.laf?barcode=9788997924837) > 112 page

<!--more-->

### # problem summary
```
정수 n을 매개변수로 입력 받아 무작위로 나열하는 프로그램을 작성하자.
입력타입 : int n
출력타입 : int []
* 입력
  4
* 출력
  1,4,3,2 (매번 다름)
```

### # pseudo-code
```
체크배열 과 결과배열을 n사이즈 만큼 만들고
n보다 작은 랜덤수를 구하고 이를 인덱스로 지정한다음
체크배열의 인덱스에 해당해는 값이 -1이 아니면 
결과배열의 앞부터 랜덤수 + 1을 넣어가며
결과배열을 다 채웠으면 종료
```

### # solution
```java
public int[] solution(int num) {
  int[] checkArray = new int[num];
  int[] result = new int[num];
  int fillIndex = 0;

  while (fillIndex < num) {
    int randomIndex = (int) (Math.random() * num);
    if (checkArray[randomIndex] != -1) {
      result[fillIndex++] = randomIndex + 1;
      checkArray[randomIndex] = -1;
    }
  }
  return result;
}
```

### # review

공간을 너무 허비한건 아닌가 싶기도 하고 (배열이 아닌 비트연산으로 체크? 그렇다면 10번째 까지밖에 체크 못함 (int max...)

최악으로 랜덤수를 구하는데 중복이 안되는게 계속 안나온다면?;;;

