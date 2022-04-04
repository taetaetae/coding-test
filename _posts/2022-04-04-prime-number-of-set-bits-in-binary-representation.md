---
title: prime-number-of-set-bits-in-binary-representation
tags:
  - Math
  - bit-manipulation
  - prime-number
---
https://leetcode.com/problems/prime-number-of-set-bits-in-binary-representation/

<!--more-->

### # review
- 출력문`System.out.println`으로 디버깅 하며 풀이
- int의 bit count 를 구하려면 Integer.bitCount 을 사용
- 소수 판별
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
