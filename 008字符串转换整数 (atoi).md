---
title: 
data: 2020-12-02
question: https://leetcode-cn.com/problems/string-to-integer-atoi/
tags:
- python
categories:
- medium
---

```Python
class Solution:
    def myAtoi(self, s: str) -> int:
        re_list=re.findall('^[\-\+]?\d+',s.strip())
        if len(re_list)==0:
            return 0
        ans=int(re_list[0])
        if ans>2**31-1:
            return 2**31-1
        elif ans<-2**31:
            return -2**31
        else:
            return ans
```