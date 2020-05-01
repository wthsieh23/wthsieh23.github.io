---
title: termux
date: 2020-05-01 08:06:46
categories:
- android
- termux
tags:
- termux
---


## nodejs
當在 termux上，執行 `npm install` 時會 failed, 大絕招就是
``` bash    
rm -rf $PREFIX
```
