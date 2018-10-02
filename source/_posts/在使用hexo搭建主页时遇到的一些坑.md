---
title: 在使用hexo搭建主页时遇到的一些坑
date: 2018-10-02 13:52:40
categories: "hexo" #分类
tags:   #标签
    - hexo
    - github
---
主页使用hexo搭建时，遇到一些问题，在此记录一下，希望能帮到有需要的朋友。

## 安装hexo-deployer-git异常
安装hexo-deployer-git异常，提示This package is no longer maintained，该插件不再维护。
解决方案，使用淘宝cnpm即可:
``` 
$ cnpm install hexo-deployer-git --save
```

## DeprecationWarning: fs.SyncWriteStream is deprecated.
按照网上所有能找到的答案，如重装各种插件，最后表示仍然还是会弹出这个提示，但不影响发布。


## 格式不正确
使用hexo d -g发布时，一直无法提交，后面经hexo群里一个朋友提醒，原来是下面代码：后面没有空格导致。

``` 
deploy:
   type:git
   repo:git@github.com:zhangdaren/zhangdaren.github.io.git
   branch:master
```
后面把空格去掉就ok了。

