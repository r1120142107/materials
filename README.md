# learning-materials
前端开发学习资料，也包括移动平台，例如 react native， phonegap。

## 电子书
* [it-ebooks](http://www.it-ebooks.info/)

## 社区
独学而无友，则孤陋而寡闻。
* [stackoverflow](http://stackoverflow.com/) 绝对是最权威的技术社区，有很多精品问题。大神很多。
* [前端网](http://www.w3cfuns.com/portal.php) 专业的前端社区，可以看到很多优秀的前端作品
* [cnode](https://cnodejs.org/) [网站代码](https://github.com/cnodejs/nodeclub/)
* [nodejs 中文社区](http://www.nodejs.net/)
* [segmentfault](http://segmentfault.com/)中文版的stackoverflow

## 在线学习
* [w3school](http://www.w3school.com.cn/index.html)

## 热门博客
排名不分先后
* [阮一峰的网络日志] (http://www.ruanyifeng.com/blog/)
* [玉伯 lifesinger] (https://github.com/lifesinger/lifesinger.github.io/issues)
* [粉丝日志] (http://blog.fens.me/)
* [掌心] (http://www.zhanxin.info/)
* [云路] (http://www.iyunlu.com/view/)
* [张云龙] (https://github.com/fouber/blog)
* [邱俊涛 I code it] (http://icodeit.org/)
* [lucida] (http://zh.lucida.me/blog)
* [司徒正美] (http://www.cnblogs.com/rubylouvre/)
* [淘宝 ued] (http://ued.taobao.org/blog/)
* [张鑫旭](http://www.zhangxinxu.com/)

## 基础知识

### javascript

#### 书单
* [ES6 入门](http://es6.ruanyifeng.com/)
* [eloquent javascript](http://eloquentjavascript.net/)
## 编码规范
* [google js style](http://google-styleguide.googlecode.com/svn/trunk/javascriptguide.xml)

### html

### css

### http
* [status code 定义](http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html)

### nodejs
* [node 7天教程](http://www.lvtao.net/content/book/node.js.htm)
* [node 从零开始系列文章] (http://blog.fens.me/series-nodejs/)
* [best practices](http://www.innofied.com/node-js-best-practices/)
* [创建模块共享的常量](http://stackoverflow.com/questions/8595509/how-do-you-share-constants-in-nodejs-modules)
  
  个人比较推荐这种方式
  ```
  module.exports = Object.freeze({
    MY_CONSTANT: 'some value',
    ANOTHER_CONSTANT: 'another value'
  });
  ```
  在其他模块使用：
  ```
  var constants = require('./constants');

  console.log(constants.MY_CONSTANT); // 'some value'

  constants.MY_CONSTANT = 'some other value';

  console.log(constants.MY_CONSTANT); // 'some value'
  ```

## 框架

### 前端组件相关
* [react]()
* [react-native]()
* [redux](http://redux.js.org/docs/introduction/)
* [Rxjs](https://github.com/Reactive-Extensions/RxJS)

### web框架
* Express api [英文](http://expressjs.com/4x/api.html) [中文](http://www.expressjs.com.cn/4x/api.html)
* [Koa](https://github.com/koajs/koa)

### html模板
* [jade api] (http://jade-lang.com/reference/)
* ejs

### UI
* [jquery UI](http://jqueryui.com/)

### 数据库
* [sequelzie 官方文档](http://sequelize.readthedocs.org/en/latest/) sequelize是成熟的orm框架。

### 单元测试
* [Testing With Mocha, Sinon.js & Mocking Request](http://bulkan-evcimen.com/testing_with_mocha_sinon)
* [node 单元测试入门](http://blog.csdn.net/wp270280522/article/details/48734409) 鄙人写的小文章
* [sinon 官方文档](http://sinonjs.org/docs/) 用于在测试中模拟数据库，http和任何你想要模拟的函数
* [chai 官方文档](http://chaijs.com/) 简单好用的断言库

## 拓展

### 设计
* [Material Design](https://material.io/guidelines/#)
* [Dribbble](https://dribbble.com/)
* [Huaban](http://huaban.com/)

### 浏览器
* [Chromium](https://www.chromium.org/Home)

### 显示文档，图片
* [如何在浏览器中显示word文档] (http://stackoverflow.com/questions/9418850/how-to-display-a-word-document-using-fancybox)

### 优化

* ***前端优化是一个循序渐进的过程***。
* ***只要适合当前技术和业务的优化方案，就是好的方案***。

### 架构
* [理解RESTful架构] (http://www.ruanyifeng.com/blog/2011/09/restful)

### 网络
* [不同网段的访问问题](http://networkengineering.stackexchange.com/questions/10530/ping-between-different-subnet-across-a-link)

### 算法


### 操作系统
* [鸟哥linux基础篇](http://vbird.dic.ksu.edu.tw/linux_basic/linux_basic.php)
* [鸟哥linux服务器篇](http://vbird.dic.ksu.edu.tw/linux_server/)


