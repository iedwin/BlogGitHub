---
title: Sublime 3取消自动更新
date: 2017-01-10 09:32:01
categories: [OS, Mac]
tags: [Sublime]
---

### 点击首选项–设置(用户)，将配置文件修改为如下：
```
{ 
    “color_scheme”: “Packages/Color Scheme - Default/Monokai.tmTheme”, 
    “ignoredpackages”: 
[ 
    “Vintage” 
], 
   "update_check": false, 
} 
```