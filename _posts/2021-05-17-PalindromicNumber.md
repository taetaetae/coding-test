---
title: 대칭수(회문수) 찾기
tags:
  - etc
  - string
  - number
---
[누가 IT시장 취업에 성공하는가](http://www.kyobobook.co.kr/product/detailViewKor.laf?barcode=9788997924837) > 114 page

<!--more-->

### # 문제 해석

121, 131, 123454321 등은 대칭수이다.  122, 123, 124 등은 대칭수가 아니다.

n부터 m사이의 대칭수를 찾는 코드를 작성하시오.

입력타입 : int n, int m

출력타입 : String

* 입력

  10, 30
  
* 출력

  11, 22

### # 해결 코드
```java
public String solution(int n, int m) {
  List<String> resultList = new ArrayList<>();

  while (n <= m) {
    String checkString = String.valueOf(n);
    char[] checkCharArray = checkString.toCharArray();
    boolean isPalindromicNumber = true;
    int endIndex = checkCharArray.length - 1;
    for (int startIndex = 0; startIndex < checkCharArray.length / 2; startIndex++) {
      if (checkCharArray[startIndex] != checkCharArray[endIndex]) {
        isPalindromicNumber = false;
        break;
      }
      endIndex--;
    }
    if (isPalindromicNumber) {
      resultList.add(checkString);
    }
    n++;
  }

  return String.join(",", resultList);
}
```

### # 후기

꼭 int 를 String 으로 바꾼다음에 그걸 또 다시 char 배열로 바꿔서 검사를 했어야 했을까...

자릿수를 알려면 어쩔수 없는 선택인것 같기도 하고.

