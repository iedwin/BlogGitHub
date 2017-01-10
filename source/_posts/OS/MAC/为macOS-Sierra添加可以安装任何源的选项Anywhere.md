---
title: 为macOS Sierra添加可以安装任何源的选项Anywhere
date: 2017-01-10 09:46:33
categories: [OS, Mac]
---

#### macOS Sierra默认只能安装App store下载的app，去掉了EI Capitain中可以安装任何源app的选项Anywhere。其实这个选项只是被隐藏了，可以用以下命令让它显示出来：
```
sudo spctl --master-disable
```