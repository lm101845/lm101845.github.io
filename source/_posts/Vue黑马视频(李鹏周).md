---
title: Vue黑马视频(李鹏周)
date: 2020-11-11 23:44:22
tags: Vue
categories: Vue
---

(注1：学到Vuex的时候发现自己组件部分学的很不好，想着先暂停一下王红元的视频再回去复习一下前面的Vue组件这些知识？想了一下准备快速再过一下Vue的基础知识吧，就选择李鹏周的4天Vue视频看一下吧，这个没办法，其实Vue的知识点已经快学完了，也是时候回过头来查漏补缺了。这次想换换口味，看看别的老师的视频。)

(注2：视频链接为[18年4天vue.js教程，李鹏周老师版](https://www.bilibili.com/video/BV1R54y1i7u4?from=search&seid=15202497373420980607))

(注3：这个视频其实知识点不全，但是现在也没关系了，先快速过一遍吧。)

(注4：这个视频还有一个好处是，老师经常打开官网，给我们讲官方文档，这也是熟悉官方文档的好机会。)

#  Vue课程讲义

## 网站交互及开发方式

### 经典的多页面

> 例如：京东商城，唯品会

* 前后端糅合在一起，开发和维护效率低下
* 用户体验一般，点击刷新跳转，等待时间过长
* 每个页面都需要重新加载渲染，速度慢
* 有利于SEO搜索引擎搜索(蜘蛛会爬链接)

### 现代式的单页面应用程序(SPA)

> 例如：网易云音乐、coding
>
> 单页面应用程序最重要的目的是为了让你的前后端开发能够分离，用户体验反而是其次的

* 开发方式好，前后端分离，开发效率高，可维护性好(自此前后端二者只通过接口来交互，此外再无交集)

  * 服务端不关心页面，只关心数据
  * 客户端不关心数据库及数据操作，只关心通过接口拿数据和服务端交互，处理页面

* **用户体验**好，就像一个原生的客户端软件一样使用

* 只需要加载渲染**局部视图**即可，不需要整页刷新

  > 技术只是工具，谁给钱就用什么就得了。没有排名之分，也不要去排斥一个技术，任何技术都有它的价值。
  >
  > 现在前端整个技术圈都很浮躁，连用个技术都要占阵营。后端藐视所有人，前端藐视UI，UI藐视......

* 单页面技术其实已经很成熟了，但是都无法兼顾低版本浏览器。(你要做SPA,肯定会用到框架，一旦用了，几乎就照顾不了低版本浏览器。)

* 但是现在除了一些电商网站，其实已经很少有系统去兼容低版本浏览器了

  * 技术不值钱，开发人员也不值钱，你给我兼容了低版本浏览器，那些使用低版本浏览器的用户可以顺利的买到东西，这才是价值。

* 大部分都是IE 9以上(IE 6,7,8已经很少去考虑了，Vue就不兼容IE9一下的浏览器。)

* 单页面由于数据都是异步加载过来的，所以不会被搜索引擎搜索到，不利于SEO

* 手机Web网页

* 服务端管理系统

#### SPA详解

单页面应用程序(Single Page Application)，简称SPA。

例如网易云音乐电脑端官网就是单页面应用程序，点击`发现音乐`、`我的音乐`等选项页面不刷新，整个页面都是被异步加载过来的，几乎所有的数据交互都是在一个页面中完成的。

(我先点击播放音乐，音乐播放后再点击排行榜，如果页面刷新，就无法保持播放音乐的这个状态了。)

说白了，SPA是对AJAX的极致应用。以前AJAX可能只是请求一个数据，渲染一个表格。

一般网页，点击刷新，它会整理渲染，会点一下跳一下，点一下刷新一下。而SPA如果你网络足够好的情况下，就可以做到无缝体验，就像原生APP一样。

交互方式的不同决定了你如何开发。

![](Vue黑马视频(李鹏周)/01.png)

### 多页面：以服务端为主导，前后端混合

* PHP案例，`.php`文件

### 单页面：前后端分离，各司其职

* 服务端只处理数据
* 前端只处理页面
* 两者通过接口来进行交互

![](Vue黑马视频(李鹏周)/02.png)

### 模拟前后端分离开发模式

* 项目立项
* 需求分析
* 服务端的工作
  * 需求分析
  * 设计数据库
  * 接口设计(有时候也需要前端参与其中——前端是接口的使用方)
  * 接口(处理数据)开发
* 前端的工作
  * 需求分析
  * 写页面
  * 页面写好写功能
  * 通过接口和服务端进行交互

#### 前后端分离：多页(不多)

##### 具体步骤

* 首先建立2个文件夹：`be-project(后端)`和`fe-project(前端)`

* 这个时候前端可以写页面了，后端开始设计接口

* 在`be-project`文件夹下打开Node，输入`npm init-y`来设计一个接口，会在`be-project`文件夹下自动生成一个`package.json`文件。

  ![](Vue黑马视频(李鹏周)/03.png)

* 再在`be-project`文件夹下输入`npm install express`下载Node中的express框架。

![](Vue黑马视频(李鹏周)/04.png)

* 此时`be-project`文件夹下面的文件有这些：

  ![](Vue黑马视频(李鹏周)/05.png)

* 再在`be-project`文件夹下新建一个`app.js`文件，内容如下：

  ~~~javascript
  const express = require('express')
  
  // 服务于POST
  const bodyParser = require('body-parser')
  
  const app = express()
  
  app.use(bodyParser.urlencoded({ extended: false }))
  // parse application/json
  app.use(bodyParser.json())
  
  
  const todos = [
      {
          id: 1,
          title:'吃饭'
      },
       {
          id: 2,
          title:'睡觉'
      },
        {
          id: 3,
          title:'打豆豆'
      },
  ]
  
  // 对todos进行增删改查
  
  // 很好的方法：
  //  GET/todos               获取所有的todos(查)
  //  POST/todos              添加一个todo(增)
  //  PATCH/todos/:todoId     更新指定的todo(改)
  //  DELETE/todos/:todoId    删除指定的todo(删)
  
  // 其实也可以只用一个关键字来增删改查
  // 不好的方法：没有表意性
  // POST/todos/:todoId/          更新指定的todo(改)
  // POST/todos/:todoId/delete    删除指定的todo(删)
  // 但是这样做没有表意性，不省事
  
  // 写接口其实挺好写的，只关心数据，不关心页面
  app
      .get('/todos',(req,res)=>{
          res.json(todos)
      })
      .post('/todos', (req, res) => {
          const todo = {
               title: req.body.title,
               id:todos[todos.length - 1].id + 1
          }
          todos.push(todo)
          res.json(todo)
      })
      .patch('/todos/:todoId',(req,res)=>{
          // 后面的这2个老师不写了，就是给我们个印象
      })
      .delete('/todos/:todoId',(req,res)=>{
  
      })
  
  app.listen(3000, () => { 
      console.log('api server running 3000.');
  })
  ~~~

* 在`de-project`文件夹下输入`nodemon app.js`

  ![](Vue黑马视频(李鹏周)/06.png)

* 然后在浏览器中输入：`127.0.0.1:3000/todos`就可以看到数据了。

  ![](Vue黑马视频(李鹏周)/07.png)

* 在`de-project`文件夹下输入`npm install body-parser`来添加数据。

* 使用`Postman`软件进行接口测试

  ![](Vue黑马视频(李鹏周)/08.png)

  > 这软件以前用过几次，但是一直不知道怎么用，就只是照着视频操作。计算机网络，Http知识也要好好学一下啊。

* 在`fe-project`文件夹下输入`npm init -y`，生成`package.json`文件

* 在`fe-project`文件夹下输入`npm install jquery`，安装jquery。

* 在`fe-project`文件夹下输入`npm install http-server -g`，安装http服务器

* 在`fe-project`文件夹下输入`hs -c-l-o`，启动服务器

* 在`fe-project`文件夹下输入`npm install art-template`，安装模版引擎

* `fe-project`和`be-project`文件夹下的文件最终如下：

  ![](Vue黑马视频(李鹏周)/09.png)

* `index.html`文件内容如下：

  ~~~html
  <!DOCTYPE html>
  <html lang="en">
  
  <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>Document</title>
  </head>
  
  <body>
      <div class="header">
          公共的头部
      </div>
      <div class="aside">
          侧边栏
      </div>
      <a href="todo/add.html">添加todo</a>
      <ul id="container">
          <!-- <li>吃饭</li>
          <li>睡觉</li>
          <li>打豆豆</li> -->
      </ul>
      <script id="tpl" type="text/template">
          {{each todos}}
              <!-- <li>{{$value}}</li> -->
              <li>{{$value.title}}</li>
          {{/each}}
          <!-- 这个模版引擎渲染也是在前端做的 -->
      </script>
  
      <script src="node_modules/jquery/dist/jquery.js"></script>
      <script src="node_modules/art-template/lib/template-web.js"></script>
      <script>
          $.get('http://127.0.0.1:3000/todos', function (data) {
              // console.log(data);
              var htmlStr = template('tpl', {
                  todos: data
              })
              $('#container').html(htmlStr)
              console.log(htmlStr);
          })
          // ajax要想发起请求，必须运行在http服务器里面(不能脱离服务器去运行)
      </script>
  </body>
  
  </html>
  ~~~

* `add.html`文件内容如下：

  ~~~html
  <!DOCTYPE html>
  <html lang="en">
  
  <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>Document</title>
  </head>
  
  <body>
      <form id="add_form">
          <div>
              <label for="title">标题</label>
              <input type="text" name="title" id="title">
          </div>
          <div>
              <input type="submit" value="保存">
          </div>
      </form>
      <script src="../node_modules/jquery/dist/jquery.js"></script>
      <script>
          $('#add_form').on('submit', handleAddSubmit)
  
          function handleAddSubmit(e) {
              e.preventDefault();
              $.post('http://127.0.0.1:3000/todos', $(this).serialize(), function (data) {
                  // console.log(data);
                  window.location.href = '../index.html'
                  // window.location.href = '/'
                  // 直接写/也行
              })
          }
  
      </script>
  </body>
  
  </html>
  ~~~

#### 前后端分离：单页

##### 具体步骤

## 前端开发三大框架

单页面应用开发技术复杂，有一定的技术支撑，所以就有了我们现在需要学习的三大框架。

* Angular
  * 09年诞生
  * Google
  * 它的目的就是为了让我们开发单页应用程序更加方便
  * 但是它最主要的就是为前端带来了MVVM开发模式
  * MVVM一句话：数据驱动视图，不操作DOM
  * Angular后来步子迈得太大，太超前把自己玩死了，Angular2.0版本相当于出来了一个新框架，相对来说比较复杂。
* React
  * 13年诞生
  * Facebook
  * 最主要的东西：组件化(组件有自己的HTML,CSS,JS)
* Vue
  * 14年诞生，作者：尤雨溪
  * 早期由个人开发
  * Vue借鉴了Angular和React之所长，自己做了一个前端框架，后起之秀。

## 上午总结

![](Vue黑马视频(李鹏周)/10.png)

![](Vue黑马视频(李鹏周)/11.png)

![](Vue黑马视频(李鹏周)/12.png)

## Vue介绍

* 作者：尤雨溪
* Vue.js（读音 /vjuː/，类似于**view**）是一套构建用户界面的**渐进式框架**(就是JavaScript框架)
  * 什么叫渐进式：你可以把它当成**库**来简单的用一下，也可以当成**框架**，并使用它的配套解决方案，也就是说，它什么都能做。
* 发展历史

​	

### MVVM

