---
title: SVN ignore Patterns
date: 2017-01-10 09:38:55
categories: [OS, Mac]
tags: [SVN]
---

### SVN经常需要ignore一些文件或文件夹，可以用工具加入ignore文件名匹配:
```
 *iml*
*.idea*
*target*
*.class*
```

### 或在项目的根目录下运行(不要漏掉最后的 .)：
```
svn propset svn:ignore "*iml*" .
svn propset svn:ignore "*.idea*" .
svn propset svn:ignore "*target*" .
svn propset svn:ignore "*.class*" .
```
