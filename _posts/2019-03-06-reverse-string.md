---
title: 344. Reverse String
tags:
  - reverse
  - array
categories : Easy
---
[https://leetcode.com/problems/reverse-string/](https://leetcode.com/problems/reverse-string/)
<!--more-->

### # 문제 해석
어쩌고 저쪼고

### # 해결 코드
```java
class Solution {
    public void reverseString(char[] s) {
        int swapIndex = s.length-1;
        for(int i=0 ; i<(s.length)/2 ; i++){
            char temp = s[i];
            s[i] = s[swapIndex];
            s[swapIndex--] = temp;
        }
    }
}
```

### # 후기
이러쿵 저러쿵