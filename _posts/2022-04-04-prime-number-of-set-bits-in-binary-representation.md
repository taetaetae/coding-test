---
title: prime-number-of-set-bits-in-binary-representation
tags:
  - Math
  - bit-manipulation
  - prime-number
---
[https://leetcode.com/problems/prime-number-of-set-bits-in-binary-representation/](https://leetcode.com/problems/prime-number-of-set-bits-in-binary-representation/)

<!--more-->

- 출력문`System.out.println`으로 디버깅 하며 풀이
- int의 bit count 를 구하려면 Integer.bitCount 을 사용
- 소수 판별 : [참고](https://prod.velog.io/@newtownboy/JAVA1929%EB%B2%88-%EC%86%8C%EC%88%98-%EA%B5%AC%ED%95%98%EA%B8%B0)

  {% highlight java %}
  public boolean prime(int num) {
      if (num == 1) {
          return false;
      }

      for (int i = 2; i * i <= num; i++) {
          if (num % i == 0) {
              return false;
          }
      }
      return true;
  }
  {% endhighlight %}

