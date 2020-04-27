---
title: termux
tags:
---

## nodejs
當在 termux上，執行 `npm install` 時會 failed, 大絕招就是
``` bash    
rm -rf $PREFIX
```
