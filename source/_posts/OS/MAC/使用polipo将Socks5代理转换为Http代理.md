---
title: 使用polipo将Socks5代理转换为Http代理
date: 2017-01-10 09:42:22
categories: [OS, Mac]
tags: [polipo]
---

#### 1. brew install polipo
#### 2. Modify '/usr/local/opt/polipo/homebrew.mxcl.polipo.plist' 
```
  <?xml version="1.0" encoding="UTF-8"?><!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd"><plist version="1.0"><dict><key>Label</key><string>homebrew.mxcl.polipo</string><key>RunAtLoad</key><true/><key>KeepAlive</key><true/><key>ProgramArguments</key><array><string>/usr/local/opt/polipo/bin/polipo</string><string>socksParentProxy=localhost:1080</string></array></dict></plist>
```
#### 3. brew services stop polipo
#### 4. polipo socksParentProxy=localhost:1080
#### >> Now can use http proxy localhost:8123

#### ----------------------------------------------------------

#### 安装polipo，ubuntu下直接安装即可。
```
sudo apt-get install polipo
```
#### 停止polipo服务 
```
sudo service polipo stop
```
#### 编辑polipo配置文件/etc/polipo/config，添加如下内容：

```
socksParentProxy = localhost:1080
proxyPort = 8787
```
#### 启动polipo服务 
```
sudo service polipo start
```