---
title: reverse-string
tags:
  - reverse
  - array
---

미리보기에서는 뭘 보여주고<!--more-->
그다음에는 뭘 보여줄지 고민해보자
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