---
title: add-to-array-form-of-integer
tags:
  - Math
  - Array
  - reverse
  - Easy
---
[https://leetcode.com/problems/add-to-array-form-of-integer/](https://leetcode.com/problems/add-to-array-form-of-integer/)

<!--more-->

01:19:07.62

- 입/출력으로 숫자가 주어질때 10자리(21억) 이 넘어갈 경우 숫자연산이 안됨을 빠르게 캐치하자.
- Wrapper Class Array 거꾸로 할때는 Collections.reverse
- primitive Type Array 거꾸로 할때는 ArrayUtils.reverse
- 거꾸로 연산은 deque 로도 활용 가능. [참조](https://soft.plusblog.co.kr/24)
- 자리수의 한칸 숫자 구할땐 `10^n`으로 나눈뒤 `%10` 연산
