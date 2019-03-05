---
title: 344. Reverse String
tags:
  - reverse
  - array
categories : Easy
---
<!--more-->
https://leetcode.com/problems/reverse-string/

### # 문제 해석
어쩌고 저쪼고

### # 결과
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