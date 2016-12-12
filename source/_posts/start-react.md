---
title: React实战(一)
date: 2016-12-12 15:32:47
tags: [asset,React]
---

第一步：构建一个react开发环境

<!--more-->

## 关于npm版本

最新的react需要npm 3.0+的版本。

通过 ```npm -v``` 来查看npm的版本，如果版本小于3.0，可以通过```npm install -g npm```来进行升级。


## 安装react

通过安装create-react-app脚手架在进行安装

```
npm install -g create-react-app  
create-react-app hello-world
cd hello-world
npm start
```
一个简单的React页面已经完成了。

![](http://of6m03mmi.bkt.clouddn.com/post_2016_12_12_react_start.png)

如果npm速度慢可以使用国内淘宝的npm镜像源
```
npm config set registry "https://registry.npm.taobao.org/"
```
