---
title: React实战(二)
date: 2016-12-16 22:36:56
tags: [asset,React,Webpack]
---

通过 react.js、七牛云存储 实现一个具有管理功能的静态页面  
第一步：构建一个react开发环境  
第二步：使用webpack打包项目

<!--more-->

---

## 什么是Webpack，用来干什么？

![](http://of6m03mmi.bkt.clouddn.com/post_16_12_16_react_start.png)
* 传统页面需要引入各种组件、资源，并且需要按照它们之间的依赖关系来进行顺序加载。人工维护容易出错。
* 加载资源需要减少请求链接数量来提高加载速度。

Webpack就是为了解决上面的资源打包问题。他的Loader功能能把各种资源当成一种模块(css, js, png ……)，然后打包成一个bundle。

## 如何使用Webpack

1. 创建一个 webpack.config.js 的配置文件
2. 提供一个入口文件
3. 提供一个输出文件的名称和位置
4. 给各种资源选择相对应的Loader加载器
5. 敲入 `webpack` ，文件就已经打包完成了

## 对上一期的React脚手架代码进行配置Webpack
在开始之前清空 node_modules 里面的文件，使用  `npm init` 创建一个package.json文件，并在里面添加下面内容，最后使用 `npm install` 安装模块。
```Json
"devDependencies": {
  "babel-cli": "^6.18.0",
  "babel-core": "^6.20.0",
  "babel-loader": "^6.2.10",
  "babel-preset-latest": "^6.16.0",
  "babel-preset-react": "^6.16.0",
  "css-loader": "^0.26.1",
  "file-loader": "^0.9.0",
  "react": "^15.4.1",
  "react-dom": "^15.4.1",
  "style-loader": "^0.13.1",
  "url-loader": "^0.5.7",
  "webpack": "^1.14.0"
}
```

Webpack配置文件的内容：
```JavaScript
module.exports = {
  entry: './src/index.jsx',
  output: {
    path: './dist/',
    filename: 'bundle.js'
  },
  module: {
    loaders: [
      {test: /\.css$/, loader: 'style!css'},
      {
        test: /\.(js|jsx)$/,
        exclude: /node_modules/,
        loader: "babel-loader",
        query: {
          "presets": ["latest","react"]
        }
      },
      {
        test: /\.(mp4|ogg|svg|mp3)$/,
        loader: 'url'
      }
    ]
  }
}
```
entry 是文件的入口位置，webpack会根据入口文件内的require、import进行一层层的自动加载依赖。  
output 是打包文件的存放位置。  
loaders 是一些资源的加载方式。  
`{test: /\.css$/, loader: 'style!css'}` 指对于.css的文件使用css-loader、style-loader加载器进行加载，loader的顺序是从右到左。css-loader的作用是用来解析css文件，style-loader的作用是插入到打包文件bundle中。  
对于js、jsx文件由于用到了ES6+的特性所以需要使用babel来进行转换成js。里面query的参数其实就是原先babel里面.babelrc的配置文件中的内容。

最后在public文件夹中的index.html文件末尾中引入打包好的文件
```Html
<script type="text/javascript" src="../dist/bundle.js"></script>
```
