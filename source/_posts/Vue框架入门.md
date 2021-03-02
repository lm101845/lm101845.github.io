---
title: Vue框架入门
date: 2020-01-01 11:46:42
tags: Vue
categories: 前端框架
top: 2021
---

(注1：将Vue视频知识点部分看完，但是越到后面越吃力，于是决定视频后面的项目部分暂缓，将官网的Vue文档再重新看一遍，相当于复习一遍，看完之后再继续看视频后面的实战项目部分。)

(注2：现在是2020年2月19日，只是看了2周基础知识视频，然后就再也没有再学习Vue了，现在还是先把以前学的基础知识再复习一遍吧，然后再看官方文档，然后再继续把剩下的项目视频看完。)

(注3：官方文档学习另起一篇博客，这样感觉显得简洁一些，此博文就全部都是看的王红元老师(codewhy)视频知识的汇总了)

(注4：现在是2020年4月3日了，箭在弦上不得不发了，抓紧时间了啊——然后后面2个多月的时间一点前端知识都没学，学网络运维和Linux去了，学了一部分的基础知识)

(注5：Vue我朦朦胧胧觉得可以先分成2部分，第一部分是各种API，第二部分是组件。我现在先把各种API再巩固一下吧，现在是2020年10月20日，学到后面发现完全不是这样的，还是当初学的比较浅啊。)

(注6：现在是2020年7月27日，4个月过去了，一点没看Vue,现在一直在补以前的基础知识，查漏补缺，还有很多基础概念没搞明白，所以一定要先忍住，不能一口气吃个胖子，先把基础打牢，概念都掌握清楚之后再去学框架。今天在网上找了一张图，贴在下面。所以，别急吧，我已经因为着急吃了很多亏了，一定要把握好现在的学习节奏啊，慢慢来吧)

(注7：现在是2020年9月4日，时隔半年之后，我又一次重新开始学习Vue了，考虑了很久，还是决定不换视频 了，还是看原来的那个60几个小时的视频，希望最多1个半月的时间一定要把它给看完啊！！)

(注8：现在和之前元旦刚开始学不一样了，8个月过去了，我就算是再废柴也有所长进吧，所以这次学习我还是比较有信心的，嗯，就怀着这样的信心开始新的征程吧！！加油！！！)

(注9:决定在学习Vue的同时再新建一篇Vue面试题的博文，刚开始一天写一道就足够了)

(注10：[视频链接](https://www.bilibili.com/video/BV15741177Eh?from=search&seid=16250798732798430553) ，老师叫王红元)

(注11：学的Vue.js的版本是2.x,而Vue最新的版本是3.x,不过没有关系，因为3.x刚出来也还没多久，学完了2.x再学3.x就只要看一下新增和删减了哪些功能就好了)

(注12：好像之前看到过一个文章讲述Angular和Vue的关系，好像尤雨溪之前也是在谷歌(Angular是谷歌发明的)工作过，然后在Angular的基础上发明了更简单的Vue，因为谷歌的步子迈得太大，新版的Angular 2不用JavaScript，用的是TypeScript语言，和Angular1相比简直就像是2个不同的框架，也很难，所以就慢慢被人们难以接受。但是现在来看，Augular 2集成了Vue + Vuex+ axios??这些，显得更加的有远见了，这篇文章我现在找不到了，等以后有机会我想学React 和Angular 2,这样就可以更加直观的比较这3种框架之间的异同了。)

(注13：[尤雨溪创立vue的心路历程](https://www.bilibili.com/video/BV1iE411H71U/?spm_id_from=333.788.videocard.6))

(注14：现在是2020年10月31日，从2020年9月4日开始算起，我学Vue不知不觉都学了有快2个月了，现在才学到VueRouter这里，学到了第7天了。之前的目标一个半月学完那就有点搞笑了。希望最多再学一个月，把Vue给学完吧。)

(注15：现在是2020年11月21日1点10分，从2020年9月4日开始算起，将近2个半月的学习，Vue的基础知识终于学完了！！！完结撒花！！接下来就只剩下一个大的实战项目没有看了，我现在是充满了信心了。从2020年元旦刚开始邂逅Vue到现在，不知不觉11个月过去了，我从之前的一脸懵逼到现在终于有所成了，接下来就要开始多做一些实战项目来好好的巩固一下Vue的各个知识点了，不禁感叹时间过得是真的太快了啊，2020年转眼间就只剩下1个多月了。)

(注16：后面的Vue实战视频我打算重新起一篇博文来写，这一篇博文有点长了，全篇将近25万字了，再接着往下写就不太好阅读了。)

(注17：现在是2020年12月11日，我的知识点学完后都没有完整的再重新看一遍这篇博文，我决定再重新温故一下，尤其是后面的，只是过了一遍，学习的并不深刻。)

# 什么时候可以学框架

![](Vue框架入门/41.png)

# Vue.js知识点总览

![](Vue框架入门/42.png)

# 邂逅Vue.js

![](Vue框架入门/43.png)

## 遇见Vue.js

### 为什么学习Vue.js

![](Vue框架入门/44.png)

> 使用Vue会告别jQuery，Vue里面没有jQuery的代码(而Angular里面还有jQuery的代码)，以后很多的大公司都在慢慢的告别jQuery，把它给淘汰掉。(但是jQuery算是前端的基本功，不能不学。)
>
> 比如Github网站就宣布他们在慢慢移除jQuery代码，不再使用jQuery了。

[GitHub 被微软收购后的 52 天，改版并放弃了 jQuery ！](https://mp.weixin.qq.com/s?__biz=MjM5MjAwODM4MA==&mid=2650701571&idx=1&sn=61b9cf057317fe00b7bcab4a5a00f034&chksm=bea60ed089d187c67557636b61b73f877ddcce5cf4c946cdf7f27278e8dc3c4b60221c67145c&scene=21#wechat_redirect)

### 简单认识Vue.js

![](Vue框架入门/00.png)

> 渐进式：你的整个项目都是用jQuery写的，你可以选择把某个页面用Vue重构一下，等你以后有空了，再把另外页面再用Vue重构，可以慢慢的，一点一点的，把整个项目最后都用Vue进行重构，把jQuery代码给全部替换为Vue代码，这个就叫做渐进式。使用Vue不会牵一发而动全身。

## Vue.js安装

![](Vue框架入门/45.png)

> 后面学Webpack的时候就是用NPM来安装Vue的。

## 体验Vue.js

### Hello Vue.js

![](Vue框架入门/01.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <!-- 在创建Vue实例的时候，我们给它创建了一个对象 -->
    <!-- 这个对象它首先有一个参数，用于挂载这些元素 -->
    <!-- <div id="app">{{message}}</div> -->
    <!-- 一个保姆只能照顾一个孩子，按照id认孩子 -->
    <div id="app">
        <h2>{{message}}</h2>
        <h1>{{name}}</h1>
    </div>
    <!-- 要想在div里显示message里的数据，就用双大括号 -->
    <div>{{message}}</div>
    <!-- 第2个div没有交给Vue实例管理，是个没人管的孤儿 -->
    <script src="js/vue.js"></script>
    <!-- <script>
        function Vue() {
            //Vue源码里面肯定是类似这样写的,肯定会创建个Vue实例
            //Vue实例里面可以有参数，而且参数是对象类型的
        }
    </script> -->

    <script>
        // 我们既然创建了一个实例，就可以用一个变量来接收它。
        //let(定义变量)/const(定义常量)
        //Vue中基本上不会再用到var了，用ES6中的let和const
        // let name = 'why';
        // name = 'kobe';
        // 这个app我们以后不会再改了，所以用const常量
        //这是另一种编程范式：声明式编程(编程范式变化了，思想也要变化)
        //好处是能做到数据和界面完全分离：界面在上面写(孩子)，数据在下面写(保姆)
        const app = new Vue({
            //你在new Vue实例的时候，就把div交给它管理了。(Vue实例就是个保姆，div是个宝宝)
            //一旦交给它(Vue实例)管理，它就会解析里面的语法
            el: '#app',		//#不能少
            //el属性用于挂载要管理的元素
            //把div这个元素传给了Vue实例，让Vue实例来管理一下上面的div
            //管理上面的div有什么用呢？
            data: {
                //data属性用于定义一些数据
                message: '你好，世界！',
                // message数据一旦改掉后，界面会自动跟着改：这个就叫响应式
                name: 'codewhy'
            }
        })

        //原生JS的做法(变成范式：命令式编程——第一步怎么做，第二步怎么做)
        //1.创建div元素，设置id属性
        //2.定义一个变量叫message
        //3.将message变量放在前面的div元素中显示
        //4.修改message数据：今天天气不错
        //5.将修改后的数据再次替换到div元素中
    </script>
</body>

</html>
~~~

#### 补充知识1:let与const(ES6)

1.ES6新增了let命令，用于声明变量。其用法类似于var，但是所声明的变量只在**let命令所在的代码块内**有效。

2.const声明一个只读的常量。一旦声明，常量的值就不能改变。

#### 补充知识2：块级作用域(ES6)

ES5只有全局作用域和函数作用域，没有块级作用域，这导致很多场景不合理。

[ES6之块级作用域](https://www.cnblogs.com/giggle/p/5572006.html)

### Vue列表显示

> 前面的Hello Vue.js展示的是很简单的数据，现在开始数据升级，展示一些复杂的数据：数据列表。

![](Vue框架入门/02.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <!-- 1.0版 -->
        {{movies}}
        <!-- 这样展示是直接展示的 -->

        <!-- 2.0版 -->
        <ul>
            <li>{{movies[0]}}</li>
            <li>{{movies[1]}}</li>
            <li>{{movies[2]}}</li>
            <li>{{movies[3]}}</li>
        </ul>
        <!-- 这样做可以列表展示，但是这样写很捞 -->

        <!-- 3.0版 -->
        <ul>
            <li v-for="item in movies">{{item}}</li>
            <!-- v-for表示遍历 -->
            <!-- 它会自动创建4个li -->
        </ul>
    </div>

    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                message: '你好啊',
                movies: ['海上钢琴师', '星际穿越', '忠犬八公', '白夜行']
            }
        })
    </script>
</body>

</html>
~~~

#### 补充知识：v-for的用法

![](Vue框架入门/04.png)

### Vue案例-计数器

![](Vue框架入门/03.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <h2>当前计数: {{counter}}</h2>
        <!-- 写法1.0 -->
        <!-- h2里面的"当前计数"是死的，不用放到大括号里面去 -->
        <!-- <button v-on:click="counter++">+</button> -->
        <!-- 改的时候直接使用变量的名字counter改的 -->
        <!-- 监听事件用v-on -->
        <!-- :click表示监听的是click事件 -->
        <!-- <button v-on:click="counter--">-</button> -->

        <!-- 写法2.0 -->
        <!-- <button v-on:click='add'>+</button> -->
        <!-- 表示点击按钮会执行add和sub函数 -->
        <!-- <button v-on:click='sub'>-</button> -->

        <!-- 写法3.0：语法糖版 -->
        <!-- 语法糖：本质就是简写 -->
        <button @click='add'>+</button>
        <button @click="sub">-</button>
    </div>
    <script src="js/vue.js"></script>
    <script>
        // 响应式里面有做一层代理(proxy)的
        // 2.0 data升级版
      	// 代理会把obj里的数据加到Vue里面去的。
        // 不管改的是app里面的counter还是obj里面的counter,结果都是一样的
        const obj = {
            counter: 0
        }
        const app = new Vue({
            el: '#app',
          	//el也可以传HTMLElement
            // 如el: document.querySelector("#app"),这样也是可以的
          
            // 1.0 data初始版
            // data: {
            //     counter: 0
            // },

            // 2.0 data升级版
            data: obj,
            methods: {
                // s表示负数，说明可以定义很多个方法
                add: function () {
                    console.log("add被执行了");
                  // 在方法里不能直接写变量的名字counter了，否则它会在全局里找counter，但是找不到
                    // console.log(this.data);
                    // this表示当前对象
                    this.counter++;
                    //疑问：为什么是this.counter而不是this.data呢？？？？？
                    //这个this不是应该指向的是app吗？还是指向谁？？
                    //应该是counter是个变量(属性名)吧
                },
                sub: function () {
                    console.log("sub被执行了");
                    this.counter--;
                }
            },
        })

        //原生JS做法：
        //1.拿buttton元素
        //2.添加监听事件
    </script>
</body>

</html>
~~~

> 如何使用原生JS进行实现，并比较二者的优劣？——记得以后动手用原生写一下啊。

#### 原生JS写法(自己手写)

~~~javascript
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        h2 {
            display: inline;
        }

        button {
            margin-top: 20px;
        }
    </style>
</head>

<body>
    <div>
        <h2>当前计数：</h2>
        <h2 class="data">0</h2>
    </div>
    <button class="add">+</button>
    <button class="sub">-</button>

    <script>
        var add = document.querySelector(".add");
        var sub = document.querySelector(".sub");
        var data = document.querySelector(".data");
        console.log(data.innerHTML);
        add.onclick = function () {
            data.innerHTML++;
        }
        sub.onclick = function () {
            data.innerHTML--;
        }
    </script>
</body>

</html>
~~~

#### 补充知识：v-on的用法

![](Vue框架入门/05.png)

#### 补充知识：methods属性

![](Vue框架入门/06.png)

## Vue中的MVVM

![](Vue框架入门/08.png)

### 计数器的MVVM

![](Vue框架入门/09.png)

![](Vue框架入门/46.png)

### 创建Vue实例传入的options

![](Vue框架入门/10.png)

> **el**：既可以传**字符串**(如`el:"#app"`)也可以传**HTMLElement**(如:`el:document.querySelector("#app")`)
>
> **data**:既可以传入**对象**(如：`data:{counter:0}`)也可以传入**函数**
>
> **methods**:传入**方法**(用键：值写的函数)，methods可以定义多个方法，所以用的是复数s。

#### 补充知识：方法和函数

![](Vue框架入门/47.png)

> 在实际开发中也很少去区分方法和函数。

### Vue的生命周期

 生命周期：事物从诞生到消亡的整个过程。

Vue生命周期：

![](Vue框架入门/07.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>05-Vue生命周期</title>
</head>
<body>

<div id="app">
  {{message}}
</div>

<script src="js/vue.js"></script>
<script>
  let app = new Vue({
    el: '#app',
    data: {
      message: '你好啊,李银河'
    },
    beforeCreate() {
	   console.log('beforeCreate');
    },
    created() {
	   console.log('created');
    },
    beforeMount() {
	   console.log('beforeMount');
    },
    mounted() {
	   console.log('mounted');
    },
    beforeUpdate() {
	   console.log('beforeUpdate');
    },
	updated() {
	   console.log('updated');
	  },
    beforeDestroy() {
	   console.log('beforeDestroy');
    },
    destroyed() {
	   console.log('destroyed');
    }
  })
</script>

</body>
</html>
~~~

![](Vue框架入门/48.png)

#### 补充知识：生命周期钩子

![](Vue框架入门/15.png)

> 现在是2020年12月13日，截止到上面复习完。

# Vue基础语法

![](Vue框架入门/30.png)

## 插值语法

> 除了胡子语法，后面的用的都挺少的。

### Mustache(胡子)语法

[mustache](https://github.com/mustache/mustache.github.com)

[mustache语法](<http://www.hxstrive.com/article/581.htm>)

[Mustache 使用说明](https://www.cnblogs.com/singoocms/p/9454884.html)

![](Vue框架入门/11.png)

![](Vue框架入门/14.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <h2>{{message}}</h2>
        <h2>{{message}},世界</h2>

        <!-- Mustache语法中，不仅仅可以直接写变量，也可以写简单的表达式 -->
        <h2>{{firstName + lastName}}</h2>
        <h2>{{firstName + ' ' + lastName}}</h2>
        <h2>{{firstName}} {{lastName}}</h2>
        <h2>{{counter * 2}}</h2>
    </div>
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                message: '你好啊',
                firstName: 'Hello',
                lastName: 'Kitty',
                counter: 100
            }
        })
    </script>
</body>
</html>
~~~

### v-once指令的使用

> once表示一次！只改一次！之后不再响应！！响应式失效！！
>
> v-once后面啥也没有，没有表达式！就是一条简简单单的指令！
>
> 这条指令只在特殊情况下才会用到，大部分情况下不会用到这条指令。

![](Vue框架入门/12.png)

![](Vue框架入门/13.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <title>Title</title>
</head>

<body>

  <div id="app">
    <h2>{{message}}</h2>
    <!-- 这个会随着message变化而变化 -->

    <h2 v-once>{{message}}</h2>
    <!-- message以后变化时这个不会再变化了 -->
  </div>

  <script src="js/vue.js"></script>
  <script>
    const app = new Vue({
      el: '#app',
      data: {
        message: '你好啊'
      }
    })
  </script>

</body>
</html>
~~~

### v-html指令的使用

> 易被攻击，只有确保安全性时才可使用。

![](Vue框架入门/16.png)

![](Vue框架入门/17.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <h2>{{url}}</h2>
        <!-- 服务器会将这个整个作为字符串返回，不会进行解析 -->

        <h2 v-html='url'></h2>
        <!-- 这个表示我将以html的形式展示这个url -->
    </div>
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                message: '你好啊',
                url: '<a href="http://www.baidu.com">百度一下</a>'
            }
        })
    </script>
</body>

</html>
~~~

### v-text指令的使用

> `v-html`用于展示**可解析的字符串**
>
> `v-text`用于展示**一般的字符串**
>
> 一般不用`v-text`,因为不够灵活

![](Vue框架入门/18.png)

![](Vue框架入门/19.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <h2>{{message}},世界</h2>
        <!-- 上面这个可以进行拼接 -->

        <h2 v-text='message'>，世界</h2>
        <!-- 下面这个不会拼接，会覆盖掉元素里面的内容(,世界)，不够灵活-->
        <!-- 和Mustache语法相比，v-text就黯然失色了 -->
    </div>
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                message: '你好啊'
            }
        })
    </script>
</body>

</html>
~~~

### v-pre指令的使用

> 不希望被解析，希望原汁原味的代码展示出来就用这个。
>
> `v-pre`和`v-once`一样，就是一个指令，后面什么都不用加的，就写个`v-pre`就可以了。

![](Vue框架入门/21.png)

![](Vue框架入门/23.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <h2>{{message}}</h2>
        <!-- 上面这个会正常解析 -->

        <h2 v-pre>{{message}}</h2>
        <!-- 下面这个不会被解析，原汁原味的展示出来{{message}} -->
    </div>
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                message: '你好啊'
            }
        })
    </script>
</body>

</html>
~~~

### `v-cloak`指令的使用

> cloak是斗篷，可以隐身，王者荣耀装备：魔女斗篷。
>
> 不要拼成了"clock(时钟)"啊！！！！
>
> 如果JS代码卡了或者出了别的问题，界面上会先快速显示原始代码：`{{message}}`,等过了一段时间后才会显示编译后的结果"你好啊"，我们不希望看到这个一闪而过的`{{message}}`，就可以用`v-cloak`指令，将一闪而过的`{{message}}`隐藏起来。
>
> 原来它用一个斗篷把`{{message}}`给遮住了，等你解析的时候会把斗篷给你移除掉。没有斗篷的话，`{{message}}`就被正常解析，显示出来了。
>
> 这个用的也很少，我们真正到时候用的是**虚拟DOM**。

![](Vue框架入门/22.png)

![](Vue框架入门/24.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        [v-cloak] {
            /* 代码还没执行的时候，{{message}}是不会被显示的，因为设置为none了 */
            display: none;
        }
    </style>
</head>

<body>
    <div id="app" v-cloak>
        <h2>{{message}}</h2>
    </div>
    <script src="js/vue.js"></script>
    <script>
        // 在Vue解析之前，div中有一个属性v-cloak
        // 在Vue解析之后，div中就没有这个v-cloak属性了
        setTimeout(function () {
            //延迟执行来模拟JS卡顿的现象
            //刚开始显示{{message}}1秒钟，之后再显示"你好啊"
            const app = new Vue({
                el: '#app',
                data: {
                    message: '你好啊'
                }
            })
        }, 1000)
    </script>
</body>
</html>
~~~

## 绑定属性

### v-bind介绍

![](Vue框架入门/25.png)

### v-bind基础

![](Vue框架入门/26.png)

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
       <!-- <h2>{{message}}</h2> -->
       <!-- 之前的插值操作学的是将Vue实例里的值(如data里面的值)插入到模版的内容中(如插入得到div中) -->
       <!-- 之前学的都是动态绑定内容 -->

       <!--现在学的是动态绑定属性，如src里面的内容我们不想写死，就先把src里面的数据放到Vue实例中再引入-->

       <!-- <img src="{{imgURL}}" alt=""> -->
       <!-- 错误的做法：这里不可以使用胡子语法 -->
       <!-- 但是我们不能这样写。胡子语法只能写在标签内容中，不能写在标签属性里-->

       <!-- <img src="imgURL" alt=""> -->
       <!-- 这样写也不行，它无法解析 -->

       <!-- 正确的做法：使用v-bind指令 -->
       <!-- 你想给哪个属性绑定值，你就在它前面加上v-bind: -->
       <!-- 加了v-bind:后，"imgURL"就不是一个简单的字符串了，摇身一变成为了一个变量了 -->
       <img v-bind:src="imgURL" alt="">
       <!-- imgURL是从Vue实例里中转过来的数据，而不是写死的数据 -->
       <!-- imgURL虽然外面被“”包围着，但是它不是字符串！！！它是变量！！！ -->

       <a href="https://www.baidu.com">百度一下</a>
       <!-- 在真实开发中，很少这样把某个东西给写死，都是从服务器请求过来数据，根据请求来的数据决定的 -->

       <a v-bind:href="aHref">百度一下</a>
       <!-- 都是这样写 -->
    </div>
    
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                message: '你好啊',
                imgURL: 'https://vuejs.bootcss.com/images/logo.png',
                // 从服务器请求过来的数据，一般都在Vue实例里做一个中转
                aHref: 'https://www.baidu.com'
            }
        })
    </script>
</body>

</html>
~~~

### v-bind语法糖

> 完整形式：`v-bind:`
>
> 语法糖形式：`:`(即可以不用写v-bind了，直接写一个冒号就可以了)

![](Vue框架入门/27.png)

![](Vue框架入门/28.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <!-- 语法糖写法：直接写个冒号(:)就可以了,前面的v-bind可以省略不写 -->
        <img :src="imgURL" alt="">
        <a :href="aHref">百度一下</a>
    </div>

    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                message: '你好啊',
                imgURL: 'https://vuejs.bootcss.com/images/logo.png',
                aHref: 'https://www.baidu.com'
            }
        })
    </script>
</body>

</html>
~~~

> `v-bind`记得要写在属性名的前面。
>
> 真实开发中都是语法糖写法，这样更加的简洁。

### 绑定class

#### v-bind动态绑定class属性(对象语法)

> 记住class是属性的一种啊！！！而且它还是**计算属性**，后面可以加方法(函数)——见后面实例

![](Vue框架入门/29.png)



> 我们一般很少用直接给它绑定字符串的方式，例如：`<h2 v-bind:class="active">{{message}}</h2>`
>
> (这种方式属于脱裤子放屁，还不如使用原生的`<h2 class="active">{{message}}</h2>`)
>
> 所以这里说了有**两种**方式，而不是三种方式。

![](Vue框架入门/39.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        .active {
            color: red;
        }
    </style>
</head>

<body>
    <div id="app">
       <h2 class="active">{{message}}</h2>
       <!-- 以前绑定class都是这样的，写死了 -->

       <!-- 动态绑定class之1.0写法：字符串写法 -->
       <!-- 现在可以这样写，来动态绑定class，但是纯属脱裤子放屁，多捞啊 -->
       <h2 v-bind:class="active">{{message}}</h2>

       <!-- 这里"active"是字符串的形式，更进一步，它也可以是对象！！ -->
       <!-- 跟的是一个大括号，表示是一个对象，而不是胡子语法 -->

       <!-- <h2 v-bind:class="{key1：value1,key2:value2}">{{message}}</h2> -->
       <!-- 绑定对象的固定写法是下面这样的:布尔值为true,类名会添加到标签上，否则不会-->
       <!-- <h2 v-bind:class="{类名1：boolean,类名2:boolean}">{{message}}</h2> -->

       <!-- 动态绑定class之2.0写法：对象写法 -->
       <h2 v-bind:class="{active:true,line:false}">{{message}}</h2>

       <!-- 更进一步3.0：true和false我们也不写死，我们写到Vue实例下面 -->
       <h2 v-bind:class="{active:isActive,line:isLine}">{{message}}</h2>

       <!-- 再进一步4.0：还可以在v-bind外写传统的class，保守派和激进派二者可以相安无事，共同生存。-->
       <!-- 到时候Vue会将这2种class(v-bind里面的和外面单独的)进行合并 -->
       <!-- 一般固定的class，必须要有的，我们单独写在v-bind外面，
			一些视情况而定的class则写到v-bind里面 -->
       <h2 class="title" v-bind:class="{active:isActive,line:isLine}">{{message}}</h2>

       <!-- 再进一步5.0,大括号{active:isActive,line:isLine}里面内容太多，可以抽离出来 -->
       <!-- 因为class是一个可计算的属性，所以可以将其放在一个methods或者computed中 -->
       <!-- 这里的getClasses方法(函数)，记得要加上小括号！！ -->
       <h2 class="title" v-bind:class="getClasses()">{{message}}</h2>

       <button v-on:click="btnClick">按钮</button>
       <!-- 这个btnClick也是方法(函数)，之所以后面没有加小括号，是因为被省略掉了！！ -->
    </div>
    <script src="js/vue.js"></script>

    <script>
       const app = new Vue({
          el: '#app',
          data: {
              message: '你好啊',
              active: 'active',
              isActive: true,
              isLine: true
          },
          methods: {
              btnClick: function () {
                  // 点一下变红，再点一下就变黑了，如此循环往复
                  this.isActive = !this.isActive;
              },
              getClasses: function () {
                  return { active: this.isActive, line: this.isLine }
                  // 记得要写上this啊！！！
              }
          },
      })
    </script>
</body>

</html>
~~~

> 解释：我们在开发里面有时候需要给某个元素加上class，有时候不需要加class，比如一个电影列表，我想要点击哪个，哪个就给我展示红色，不点击则不展示红色。
>
> 以前的做法是：点击谁给它加上class属性，并且同时把以前那个给移除class属性。
>
> 现在的做法是：通过对象的方式，给class设置布尔值，以此操纵这个class是否在这个元素里。
>
> 之所以叫对象语法是因为有大括号表示对象。

#### v-bind动态绑定class属性(数组语法)

> 数组语法用的比较少，视频中一笔带过。

![](Vue框架入门/49.png)

#### 作业(v-bind和v-for的结合)

> **需求：**
>
> 1.在页面上显示四个列表，初始时字体为黑色。
>
> 2.鼠标点击某一个列表时，该列表的颜色变为红色，其余列表仍为黑色。

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
      .active {
          color: red;
      }
    </style>
</head>

<body>
    <!-- 作业需求：点击列表中的哪一项，那么该项的文字就会变成红色。一定要试着自己独立写！！-->
    <!-- 唉，我写不出来 -->
    <div id="app">
       <ul>
          <!-- <li v-for="(item,index) in movies" class='active'>{{index}}-{{item}}	               </li> -->
          <!-- 不能直接加class，直接加所有的人都变成了红色 -->

           <!-- <li v-for="(item,index) in movies" :class='{active:currentIndex === 					index}'>{{index}}-{{item}}</li> -->
            
          <!-- v-for属性用于遍历，v-bind属性用于动态绑定class -->
          <!-- 但是这个class有还是没有我们怎么决定呢？就用currentIndex === index来决定 -->
          <!-- 我们要动态的给它加class，采用对象语法-->
          <!-- 但是又不能给它写死了-->

          <!-- 我们每个li都有属于自己的index -->
          <!-- <li :class="{active:0 === currentIndex}"></li>
          <li :class="{active:1 === currentIndex}"></li>
          <li :class="{active:2 === currentIndex}"></li>
          <li :class="{active:3 === currentIndex}"></li> -->

          <!-- 最后一步：再来监听li的点击就可以了 -->
          <li v-for="(item,index) in movies" 
              :class='{active:currentIndex === index}'
              @click='liClick(index)'>
              {{index}}-{{item}}</li>
       </ul>
    </div>
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                movies: ['海尔兄弟', '猫和老鼠', '舒克贝塔', '太阳之子'],
                currentIndex: -1
                // currentIndex用于记录到底谁会显示红色的
                // 你想不到这个没事，以后写多了慢慢就会写了
            },
            methods: {
                liClick(index) {
                    // 要有一个index参数！！！
                    // 每个li都有index参数，所以直接传就好了
                    this.currentIndex = index;
                }
            }
        })
    </script>
</body>

</html>
~~~

### 绑定样式

> 后面学到组件化开发的时候，动态样式用的比较多。
>
> 我突然感到前面的类class和这里的样式style，我已经不知道它们二者有什么区别了！！彻底懵了。
>
> 说白了还是基础不扎实，概念混乱了。

[javascript中style,与class有什么区别？](https://zhidao.baidu.com/question/41856023.html)

#### v-bind动态绑定style属性(对象语法)

![](Vue框架入门/50.png)

![](Vue框架入门/51.png)

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <!-- <h2 v-bind:class="{key1：value1,key2:value2}">{{message}}</h2> -->
        <!-- v-bind绑定class时，里面的value1,value2是布尔值 -->

        <!-- <h2 :style="{key(CSS属性名):value(属性值)}">{{message}}</h2> -->
        <!-- v-bind绑定style时，里面的value是字符串 -->

        <!-- 属性名可以用驼峰语法写，也可以短横线分隔，但是驼峰语法用的更多 -->
        <!-- <h2 :style="{font-size:}">{{message}}</h2> -->

        <!-- <h2 :style="{fontSize:50px}">{{message}}</h2> -->
        <!-- 如果不加单引号，Vue会把50px当成是一个变量去解析,会报错 -->

        <h2 :style="{fontSize:'50px'}">{{message}}</h2>
        <!-- 把50px外面写上2个单引号就可以了 -->
        <!-- 这样写类似于行内式，还是写死的 -->

        <h2 :style="{fontSize:finalSize}">{{message}}</h2>
        <!-- 这里的finalSize不用加单引号，将finalSize当成变量进行解析的 -->

        <h2 :style="{fontSize:finalSize2 + 'px',color:finalColor}">{{message}}</h2>
        <!-- 这里finalSize2后面跟的是数字，不是字符串，那么必须在后面加上+'px'进行连接 -->

        <h2 :style=getStyles()>{{message}}</h2>
        <!-- 如果感觉style里面的东西(对象)很长，也可以把它给抽出来 -->
    </div>
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
           el: '#app',
           data: {
              message: '你好啊',
              finalSize: '100px',
              finalSize2: 30,
              finalColor: 'red'
           },
           methods: {
              getStyles: function () {
                 return {fontSize: this.finalSize2 + 'px', backgroundColor: 							 this.finalColor}
              }
          },
     })
 	</script>
</body>

</html>
~~~

#### v-bind动态绑定style属性(数组语法)

> 这个用的很少！！

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <h2 :style='[baseStyle,baseStyle1,baseStyle2]'>{{message}}</h2>
        <!-- 数组中放的是一个一个元素，而不是键值对 -->
        <!-- 里面的baseStyle不要加单引号，要把它当成变量 -->
    </div>
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                message: '你好啊',
                baseStyle: { backgroundColor: 'pink' },
                baseStyle1: { fontSize: '100px' },
                baseStyle2: { color: 'green' }

            }
        })
    </script>
</body>

</html>
~~~

> 现在是2020年12月14日，截止到这里复习完。

## 计算属性

[什么时候用methods，什么时候用computed](https://segmentfault.com/q/1010000008963374)

### 什么是计算属性

![](Vue框架入门/52.png)

### 计算属性的基本使用

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <h2>{{firstName + ' '+ lastName}}</h2>
        <h2>{{firstName}} {{lastName}}</h2>
        <!-- 这样写很长，书写不方便，不简洁，也不易阅读 -->

        <h2>{{getFullName()}}</h2>
        <!-- 这个要好一点了，但是里面跟的是方法，不是名字，看起来有点别扭 -->

        <!-- 为了看上去不那么别扭，我们引入了计算属性 -->
        <!-- 计算属性：当我们需要对我们的数据进行某种变化之后再来进行显示，
						 可以在计算属性里给它重新定义一个属性 -->
        <!-- 并且给它返回你变化之后的数据 -->
        <h2>{{fullName}}</h2>
        <!-- 计算属性我们是把它当作属性来用的，所以后面不加小括号！！！！看着更加舒服 -->
    </div>
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                firstName: 'kobe',
                lastName: 'Bryant'
            },
            methods: {
                // 方法里面定义的是函数
                // 方法里面的函数名一般是动词：getFullName
                getFullName() {
                    // getFullName: function () {
                    //上面的是函数的简写形式，省去了:function 
                    return this.firstName + ' ' + this.lastName;
                }
            },
            computed: {
                // computed:计算属性。(我们在起名字的时候一般按照名词的方式给这个函数起名字)
                // 计算属性和方法(methods)一样，定义的也是函数
                // 计算属性里的函数名一般是名词：fullName
              	// 看上去是个函数，实际上是个属性，后面讲是如何从函数转换为属性的
                fullName: function () {
                    return this.firstName + ' ' + this.lastName;
                }
            }
        })
    </script>
</body>

</html>
~~~

### 计算属性的复杂操作

[JavaScript reduce() 方法](https://blog.csdn.net/weixin_42220533/article/details/89920493)

[JS高阶函数——reduce()用法总结](https://zhuanlan.zhihu.com/p/65235741)

[JS进阶篇--JS数组reduce()方法详解及高级技巧](https://segmentfault.com/a/1190000010731933)

![](Vue框架入门/53.png)

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <h2>总价格：{{books[0].price + books[1].price +books[2].price +books[3].price }}</h2>
        <!-- 这样写能得到结果，但是这个代码太恶心 -->

        <h2>总价格：{{totalPrice}}</h2>
        <!-- 这样写就好多了 -->

        <!-- 像这种数据你是不可能直接用胡子语法直接把数据给写上去的，必须要进行一定的操作和转换 -->
        <!-- 这个时候你就不得不用计算属性了(计算属性比方法要好！) -->
    </div>
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                books: [
                    { id: 001, name: 'Unix编程艺术', price: 128 },
                    { id: 002, name: '代码大全', price: 25 },
                    { id: 003, name: '深入理解计算机原理', price: 158 },
                    { id: 004, name: '现代操作系统', price: 38 },
                ]
            },
            // methods: {
            // 我们这里就不用methods了，改用computed:计算属性了
            // }

            //计算属性和methods的区别：多次调用时计算属性只会调用一次，
            //而methods你调用几次它就会执行几次
            //methods是没有缓存的，它的性能会更低一点
            computed: {
                totalPrice: function () {
                    // 这个用高阶函数比较好，以后讲
                    //高阶函数如：filter/map/reduce
                    // return this.books.reduce()

                    // 计算属性的名字记得起个名词形式的:totalPrice
                    let result = 0;

                    // for循环写法1：
                    // for (let i = 0; i < this.books.length; i++) {
                    //     result += this.books[i].price;
                    // }

                    // ES6中的for也可以这样简写
                    //for循环写法2：
                  	// 推荐在循环对象属性(key)的时候，用for...in
                    // for (let i in this.books) {
                    //     result += this.books[i].price;
                    // }

                    //for循环写法3：
                  	// 推荐在遍历数组(value)的时候，用for...of
                    for (let book of this.books) {
                        // console.log(book.price);
                        result += book.price;
                    }
                    return result;
                }
            }
        })
    </script>
</body>

</html>
~~~

### 计算属性的getter和setter

[理解JS中getter和setter的应用](https://www.jiangweishan.com/article/js20200702a1.html)

![](Vue框架入门/54.png)

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <h2>{{fullName}}</h2>
        <!-- fullName不是一个函数，它是一个属性，所以可以直接用胡子语法 -->
        <!-- 如果用写法1.0，fullName成了一个函数，但也可以直接用胡子语法啊 -->
    </div>
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                firstName: 'Kobe',
                lastName: 'Bryant'
            },
            computed: {
                //computed后面的大括号里面的内容(fullName)本质上就是一个对象 

                // 写法1.0
                // fullName: function () {
                //     return this.firstName + ' ' + this.lastName;
                // }

                //写法2.0
                fullName: {
                    // 我们在{}这个对象里面定义了一个属性叫fullName,而fullName它的类型也是对象
                    // fullName在外面是一个属性(属性有setter和getter方法)，在内部是一个方法
                    // 完整的计算属性它其实是这样写的

                    set: function (newValue) {
                        // 计算属性一般情况下实现get方法就可以了，set方法一般不用实现
                        // 我们不希望别人随便给我们计算属性设置值，所以我们经常会把set方法给删除掉
                        //当我们在控制台输入app.fullName = 'abc'时就会
                      	//调用set方法(修改属性)，会打印'---'
                        console.log('-----------');
                        // 像下面这样写的话如果修改属性值，浏览器上显示的内容也会响应的修改了！！
                        console.log('-----------', newValue);
                        const names = newValue.split(' ');
                        this.firstName = names[0];
                        this.lastName = names[1];
                    },

                    // 计算属性一般是没有set方法的，没有了set方法其实它就是一个只读属性
                    get: function () {
                        // return 'abc';
                        // 之后使用fullName属性时，会显示abc。
                        // 因为当我们使用fullName属性时，本质上会来调用我们get方法，
                        // 拿到的结果进行显示
                        return this.firstName + ' ' + this.lastName;
                    }
                },
                //写法3.0（2.0的简便写法）
                //一般我们不写set方法，只写get方法，在此基础上的简写如下：
                // fullName: function () {
                //     return this.firstName + '-' + this.lastName;

                // }
            }
        })
    </script>
</body>

</html>
~~~

### 计算属性的缓存

![](Vue框架入门/57.png)

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <!-- 方法1.直接拼接:其语法过于繁琐，不采用 -->
        <h2>{{firstName}} {{lastName}}</h2>

        <!-- 方法2.通过定义methods -->
        <h2>{{getFullName()}}</h2>
        <h2>{{getFullName()}}</h2>
        <h2>{{getFullName()}}</h2>
        <h2>{{getFullName()}}</h2>

        <!-- 方法3.通过computed -->
        <h2>{{fullName}}</h2>
        <h2>{{fullName}}</h2>
        <h2>{{fullName}}</h2>
        <h2>{{fullName}}</h2>

        <!-- 第2种和第3种方法看上去差不多，但还是有区别的 -->
        <!-- 区别是：计算属性有缓存，可以提升性能，而methods没有 -->
    </div>
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                firstName: 'Kobe',
                lastName: 'Bryant'
            },
            methods: {
                getFullName: function () {
                    console.log('该方法被调用了');
                    // 这句话被打印了4次
                    return this.firstName + ' and ' + this.lastName
                }
            },
            computed: {
                fullName: function () {
                    console.log('该方法被调用了');
                    //这句话只打印了1次——性能更高
                    return this.firstName + ' & ' + this.lastName
                }
            }
        })
    </script>
</body>

</html>
~~~

> 现在是2020年12月15日，截止到这里复习完。

## ES6补充

### let和var

> var是没有块级作用域的，而let是有块级作用域的。
>
> JavaScript在设计的时候，if没有作用域，for没有作用域，只有函数(function)是有作用域的。
>
> 你必须要理解作用域，才能理解下面的代码。

![](Vue框架入门/58.png)

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <button>按钮1</button>
    <button>按钮2</button>
    <button>按钮3</button>
    <button>按钮4</button>
    <button>按钮5</button>
    <script>
        //ES5中的var是没有块级作用域的(if/for没有)
        //ES6中的let是有块级作用域的(if/for有)

        //在ES5之前，因为if和for都没有块级作用域的概念，所以在很多时候，我们都必须借助于函数		               //(function)的作用域
        //来解决我们引用外面变量的问题。

        //而在ES6中加入了let,let它是有if和for的块级作用域的，这个问题也就随之解决了

        //1.变量的作用域：变量在什么范围内是可用的
        // {
        //     // 这个大括号是代码块
        //     var name = 'why';
        //     console.log(name);
        // }

        // console.log(name);
        // 在外面也可以访问到大括号里面的变量name：大括号形同虚设，变量name非常自由，
        // 随时可以翻墙去外面玩
        // 但是外面的小孩(变量)无法翻墙进去和墙里面的孩子玩。

        //2.没有块级作用域引起的问题：if的块级
        var func;
        //这个func先不给它赋值,在if语句里面再给它赋值
        if (true) {
            var name = 'why';
            // 在这里定义的name,在其他地方都能把这个name给改掉，这样就会出现一些问题
            func = function () {
                console.log(name);
            }

            // func();
            //你想用函数的话直接这样来使用就可以了
        }
        name = 'kobe';
        // 如果别人把name改掉了，这个函数打印的就是kobe了，而不是why了(但我们只想打印why)
        func();
        // 在if语句外面也是可以访问这个函数的
        // console.log(name);

        //3.没有块级作用域引起的问题：for的块级
        //下面全用ES5的语法写
      	//方式1：错误的方式
        var btns = document.getElementsByTagName('button');
        for (var i = 0; i < btns.length; i++) {
            // 这个i在函数外面
            btns[i].addEventListener('click', function () {
                // 这个函数只在被点击时才触发，不点击不触发
                // 但是循环，它不管你点不点击，它直接就循环完了，最终结果i为5
                console.log('第' + i + '个按钮被点击了');
                // 这个i在函数里面，引用的函数外面的i(for里面的i)
                //在我点击第一个按钮之前，已经进行了好几次循环，函数外面的这个i被改掉了
                // 这样写的话，不管你点击第几个按钮，都会显示第5个按钮被点击了
            })
        }
				
      	//方式2：ES5中使用立即执行函数
        //为了解决3这个问题没有ES6的时候我们可以用立即执行函数解决(但是代码有点恶心)
        //为什么立即执行函数可以解决这个问题：因为函数是一个作用域
        for (var j = 0; j < btns.length; j++) {
            // (function (j) {
            // 我这里甚至可以不叫j,我随便叫什么都可以，不影响 
            (function (num) {
                btns[j].addEventListener('click', function () {
                    // 这里一共有5个函数
                    // 这个j是不会被别人改掉的
                    console.log('第' + num + '个按钮被点击了');
                })
            })(j)
        }

        // 举个例子说明上面j不会变的原因
        //例子1
        var age = 18;
        function abc(age) {
            // 函数内部有属于我自己的age
            // 这个age在函数范围之内是有自己的作用域的
            // 里面的age和外面的age是没有任何影响的
            console.log(age);
        }
        age = 20;
        abc(25);
        // 不管你外面的age怎么改，我的abc里面的age还是25(函数age里有作用域)

        //例子2
        var name1 = 'Li';
        function abc(bbb) {  //bbb = 'Li'
            console.log(bbb);
        }
        abc(name1);
        // 你再改name1的值，对前面没有任何影响，最终打印出来还是'Li'
        //如果把abc(name1);放在name1 = 'Wang'下面，那打印出来的就是'Wang'了
        name1 = 'Wang';
	
        //方式3：ES6中使用let
        const btns1 = document.getElementsByTagName('button');
        for (let k = 0; k < btns1.length; k++) {
            // 现在这个大括号有自己的作用域了，意味着for小括号里面的k只属于这个大括号
            // 我们在第一次执行for循环的时候会执行大括号里面这段代码，这段代码有属于自己的k
            btns1[k].addEventListener('click', function () {
                console.log('第' + k + '个按钮被点击了');
            });
        }

        // {
        //     i = 0;
        //     btns1[k].addEventListener('click', function () {
        //         console.log('第' + k + '个按钮被点击了');
        //     });
        // }

        // {
        //     i = 1;
        //     btns1[k].addEventListener('click', function () {
        //         console.log('第' + k + '个按钮被点击了');
        //     });
        // }

        // {
        //     i = 2;
        //     btns1[k].addEventListener('click', function () {
        //         console.log('第' + k + '个按钮被点击了');
        //     });
        // }

        // {
        //     i = 3;
        //     btns1[k].addEventListener('click', function () {
        //         console.log('第' + k + '个按钮被点击了');
        //     });
        // }

        // {
        //     i = 4;
        //     btns1[k].addEventListener('click', function () {
        //         console.log('第' + k + '个按钮被点击了');
        //     });
        // }

        // 以前因为if,for都没有作用域，所以相当于共用了一个k
        // 而现在有了作用域以后，作用域范围内有属于我们每个人自己的k
    </script>
</body>

</html>
~~~

### const

![](Vue框架入门/59.png)

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <script>
        // 注意1：一旦给const修饰的标识符被赋值之后，不能修改
        const name = 'why';
        // name = 'abc';
        // 修改后会报错

        // 注意2：在使用const定义标识符，必须进行赋值
        // var name;
        // var可以只是定义，先不赋值(初始化)，但是const不可以

        // const name;
        // 只定义，不初始化会报错

        // 注意3：常量的含义是指向的对象不能修改，但是可以修改对象内部的属性
        const obj = {
            name: 'why',
            age: 18,
            height: 1.88
        }
        console.log(obj);
        // obj = {};
        //这样写会报错，你不可以改变obj的指向

        obj.name = 'Kobe';
        // 虽然我不看篮球，但还是悼念科比
        obj.age = 42;
        obj.height = 1.87;
        // 但这样写不会报错，你可以修改obj内部的属性
        console.log(obj);
    </script>
</body>

</html>
~~~

![](Vue框架入门/60.png)

### 对象字面量的增强写法

![](Vue框架入门/61.png)

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <script>
        // const obj = new Object();
        // 我们一般不这么写

        // var obj = {
        //     name: 'why',
        //     age: 18,
        //     run: function () {
        //         console.log('我在奔跑');
        //     },
        //     eat: function () {
        //         console.log('我在吃东西');
        //     }
        // };
        // 这个叫对象字面量写法

        //1.属性的增强写法
        const name = 'why';
        const age = 18;
        const height = 1.88;

        //ES5的写法
        // const obj = {
        //     name: name,
        //     age: age,
        //     height: height
        // }

        //ES6属性的增强写法
        const obj = {
            name,
            age,
            height
        }
        console.log(obj);

        //2.函数的增强写法
        // ES5的写法
        // const obj = {
        //     run: function () {
        //         console.log('我在奔跑');
        //     },
        //     eat: function () {
        //         console.log('我在吃东西');
        //     }
        // };

        //ES6函数的增强写法
        const obj = {
            run() {
                console.log('我在奔跑');
            },
            eat() {
                console.log('我在吃东西');
            }
        }
    </script>
</body>

</html>
~~~

## 事件监听

### v-on介绍

> on表示在什么之上，意思是当我们在做某些事情的时候，在它的基础之上进行一些对应的操作。(如用户点击，在点击的基础之上触发某些函数。)

![](Vue框架入门/62.png)

### v-on基础

![](Vue框架入门/63.png)

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <h2>{{counter}}</h2>
        <!-- 方法1:直接在里面写方法(只适合方法比较简单的情况)-->
        <!-- <button v-on:click="counter++">+</button>
        <button v-on:click="counter--">-</button> -->

        <!-- 方法2：调用定义的方法-->
      	<!-- 因为increment()和decrement()这2个方法的小括号里没有参数，所以调用这2个方法时，-->				<!--小括号可以不用写，直接写click="increment"这样就行，但是写了肯定也没问题,写-->			       	 <!--click="increment()是最保险的"-->
        
      	<!--要记住只有在进行事件监听调用方法且小括号内没有参数时小括号才可以省略(2个条件！！！)，-->				<!--而其他的，比如胡子语法里面的方法，小括号是不可以省略的-->
        <!-- <button v-on:click="increment">+</button>
        <button v-on:click="decrement">-</button> -->

        <!-- 方法2的语法糖写法：把"v-on:"替换为@ -->
        <!-- click是因为我们这里监听的是click事件，还有keyup等各种事件 -->
        <button @click="increment">+</button>
        <button @click="decrement">-</button>
    </div>
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                counter: 0
            },
            methods: {
                // 这个是对象字面量函数的增强写法
                // 大括号就是对象，对象里面定义了increment函数
                // 以前是这么写的：
                // increment:function(){

                // }
                increment() {
                    this.counter++;
                },
                decrement() {
                    this.counter--;
                }
            }
        })
    </script>
</body>
</html>
~~~

### v-on参数

![](Vue框架入门/64.png)

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <!-- 事件调用的方法没有参数,此时加不加小括号都行-->
        <button @click="btnClick">按钮1不加小括号</button>
        <button @click="btnClick()">按钮1加小括号</button>

        <!-- 在事件定义时，写方法时省略了小括号(小括号都没有，更别说参数了)，但是方法本身是需要一个参数的，
             这个时候Vue会默认将浏览器生成的event事件对象作为参数传入到方法中-->
        <button @click="btn2Click(123)">按钮2正常情况</button>

        <!-- btn2Click这个函数定义时是要传参数的，但是引用时没有写参数 -->
        <!-- 后面写了小括号，但是里面没有写参数，会显示undefined -->
        <button @click="btn2Click()">按钮2有小括号但里面没参数</button>

        <!-- 函数后面连小括号都没写会显示MouseEvent -->
        <button @click="btn2Click">按钮2连小括号都没有</button>

        <!--方法定义时，我们需要event对象，同时又需要其他参数-->

        <!-- 2个参数都不写会显示MouseEvent对象和undefined-->
        <!-- Vue会把MouseEvent对象赋值给第一个参数——abc,undefined赋值给第二个参数event-->
        <button @click="btn3Click">按钮3中2个参数都不写</button>

        <!-- 只写第1个参数，第二个参数写的还是形参 -->
        <!-- 此时小括号里的第二个参数event会被当成变量解析 -->
        <button @click="btn3Click(123,event)">按钮3第2个参数是形参event</button>

        <!-- 在调用方法时，如何手动的获取到浏览器参数的event对象呢？ 答：通过$event即可 -->
        <!-- 如果第1个参数写的是'abc',那它会将其当成字符串；如果是abc,它会将其当成变量，就会
             在下面找有没有这个变量，如果没有这个变量它就会报错-->
        <button @click="btn3Click(123,$event)">按钮3第2个参数是$event</button>

        <button>按钮4</button>
    </div>
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                // event: 'codewhy'
                //如果没有找到变量event的值，就会报错说找不到这个属性。
            },
            methods: {
                btnClick() {
                    console.log("点击第一个按钮了");
                },
                btn2Click(event) {
                    console.log('------------------', event);
                },
                btn3Click(abc, event) {
                    console.log('++++++++++++++++++', abc, event);
                }
            }
        })

        // 如果函数需要参数，但是没有传入，那么函数的形参为undefined
        // function fun(name) {
        //     console.log(name);
        // }
        // fun();
        // fun()因为小括号里没有传入参数,所以会显示undefined
    </script>
</body>
</html>
~~~

### v-on修饰符

![](Vue框架入门/65.png)

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <!-- 1.".stop"修饰符的使用 -->
        <div @click="divClick">
            div里面的内容
            <!-- btn在div里面，而且都绑定了点击事件，会产生冒泡 -->
            <!-- 在Vue中阻止冒泡使用修饰符就可以了 -->
            <button @click="btnClick">按钮1</button>
            <button @click.stop="btnClick">按钮2</button>
        </div>

        <br>

        <!-- 2.".prevent"修饰符的使用 -->
        <form action="baidu">
            <!-- 有些情况下我可能希望自己手动提交，而不用它自动帮我提交-->
            <!-- 这样写有打印("提交表单了"这句话会一闪而过)，同时有提交 -->
            <input type="submit" value="提交1" @click="submitClick">

            <!-- 这样写只有打印，不会再提交了 -->
            <input type="submit" value="提交2" @click.prevent="submitClick">
        </form>

        <br>

        <!-- 3.监听某个键盘的键帽的点击 -->
        <!-- ".keyCode"修饰符的使用 -->
        <!-- keyup表示键盘弹起时触发的事件 -->
        <!-- 如果我们只想监听用户敲下回车的按键，加上修饰符".enter"就可以了 -->
        <input type="text" @keyup="keyUp">

        <!-- 这个只会监听敲回车的事件 -->
        <input type="text" @keyup.enter="keyUp">

        <!-- 4.监听组件 -->
        <!-- 这个要等到我们学组件的时候再说了 -->
        <!-- ".native"修饰符的使用 -->
        <!-- <cpn @click="cpnClick"></cpn> -->
        <!-- 如果不写修饰符".native"则组件无法监听到这个cpnClick这个方法 -->
        <!-- <cpn @click.native="cpnClick"></cpn> -->

        <!-- 5.只触发一次回调 -->
        <!-- ".once"修饰符的使用 -->
        <!-- 有了这个修饰符则按钮就只有在第一次点击的时候才会触发btn2Click这个方法，-->
   		<!-- 之后怎么点也不会再触发了-->
        <button @click="btn2Click">按钮3</button>
        <button @click.once="btn2Click">按钮4</button>
    </div>
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                message: '你好啊'
            },
            methods: {
                btnClick() {
                    console.log("btn被打印了");
                },
                divClick() {
                    console.log("div被打印了");
                },
                submitClick() {
                    console.log('提交表单了');
                },
                keyUp() {
                    console.log("按键被弹起了");
                },
                cpnClick() {
                    console.log("组件被监听了");
                },
                btn2Click() {
                    console.log("按钮2被打印了");
                }
            }
        })
    </script>
</body>

</html>
~~~

> 现在是2020年12月16日，截止到这里复习完。

## 条件和循环

### v-if、v-else-if、v-else有条件渲染元素

![](Vue框架入门/66.png)

#### v-if的使用

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <!-- 有时候我们希望只有在满足一定条件时才渲染这个message,这个时候就用到了v-if -->
        <h2 v-if='true'>{{message}}</h2>

        <!-- 当为false时，不会被渲染，所以不会显示 -->
        <h2 v-if='false'>{{message}}</h2>

        <h2 v-if='isShow'>{{message}}</h2>
        <!--变量isShow外边记得加引号 -->
    </div>
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                message: '你好啊',
                isShow: true
            }
        })
    </script>
</body>

</html>
~~~

#### v-if和v-else的使用

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <h2 v-if='isShow'>
            <!--变量isShow外边记得加引号 -->
            <div>abc</div>
            <div>abc</div>
            <div>abc</div>
            {{message}}
        </h2>
      
        <h1 v-else>isShow为false时显示我</h1>
        <!-- 要记得加上v-else啊！！-->
    </div>
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                message: '你好啊',
                isShow: true
            }
        })
    </script>
</body>

</html>
~~~

#### v-if和v-else-if和v-else的使用

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <!-- 方法1 -->
        <!-- 下面这样的写法用的不是特别多，因为如果真有这样复杂的逻辑判断， -->
        <!-- 不建议使用标签的形式来进行判断-->
        <!-- 一方面阅读性不强，另一方面写起来也会感到很别扭 -->
        <h2 v-if='score>=90'>优秀</h2>
        <h2 v-else-if='score>=80'>良好</h2>
        <!-- 因为是else-if，是在上面条件不满足的情况下才会判断下面的条件，
            所以第二个条件可以不用写'&&score < 90' -->
        <h2 v-else-if='score>=60'>及格</h2>
        <h2 v-else>不及格</h2>

        <!-- 方法2 -->
        <!-- 可以使用计算属性来做，更加简单 -->
        <h1>{{result}}</h1>
    </div>
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                score: 99
            },
            computed: {
                result() {
                    let showMessage = '';
                    if (this.score >= 90) {
                        showMessage = '优秀';
                    } else if (this.score >= 80) {
                        showMessage = '良好';
                    } else if (this.score >= 60) {
                        showMessage = '及格';
                    } else {
                        showMessage = '不及格';
                    }
                    return showMessage;
                }
            }
        })
    </script>
</body>

</html>
~~~



### 条件渲染案例

![](Vue框架入门/67.png)

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <!-- 通过v-if和v-else来控制到底显示上面这段代码还是显示下面这段代码 -->

        <span v-if="isUser">
            <!-- label 标签为 input 元素定义标注（标签） -->
            <!-- 作用:用于绑定一个表单元素, 当点击label标签的时候, 被绑定的表单元素就会获得输入焦点-->
            <label for="username">用户账号</label>
            <input type="text" id="username" placeholder="用户账号">
        </span>

        <span v-else>
            <label for="email">用户邮箱</label>
            <input type="text" id="email" placeholder="用户邮箱">
        </span>
        <button @click="isUser = !isUser">切换类型</button>
    </div>
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                isUser: true
            }
        })
    </script>
</body>

</html>
~~~

#### 条件渲染案例的小问题

> 用户先输入账号，输到一半发现账号忘记了，于是想切换输入邮箱，等切换到邮箱的时候，发现之前输入的内容还存在，没有消失掉。
>
> 原因是使用了虚拟DOM,为了节约性能，所以复用了原来的input元素，如果我们不希望它复用，而是新建一个input元素，那么可以在对应的input中添加key。

![](Vue框架入门/68.png)

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <!-- 通过v-if和v-else来控制到底显示上面这段代码还是显示下面这段代码 -->

        <span v-if="isUser">
          <!-- label 标签为 input 元素定义标注（标签） -->
          <!-- 作用:用于绑定一个表单元素, 当点击label标签的时候, 被绑定的表单元素就会获得输入焦点-->
          <label for="username">用户账号</label>
          <!-- 上面的input的key值是abc,下面input的key值是123,Vue就知道你不想让input元素被复用了-->
          <!-- 于是它就会重新创建出一个新的input元素 -->
          <input type="text" id="username" placeholder="用户账号" :key="abc">
        </span>

        <span v-else>
          <label for="email">用户邮箱</label>
          <input type="text" id="email" placeholder="用户邮箱" :key="123">
        </span>
        <button @click="isUser = !isUser">切换类型</button>
    </div>
    
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                isUser: true
            }
        })
    </script>
</body>

</html>
~~~

### v-show渲染元素

![](Vue框架入门/69.png)

### v-if(死亡)和v-show(隐身)对比

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <!-- 
            v-if:死亡(当条件为false时，包含v-if指令的元素，根本就不会存在DOM中)
            如果将条件再次改为true,它会再重新创建一个新的元素，原来的那个死了，再也回不来了。
            你不需要我的时候，我就直接自杀了(铮铮铁骨)

            v-show:隐身(当条件为false时，v-show只是给我们的元素添加一个行内样式:display:none)
            你不需要我的时候，我就隐身，但仍然留在你身边(终极舔狗)，等你需要的时候，我再现身服务						你:display:block
         -->
        <h2 v-if="isShow" id="aaa">v-if的{{message}}</h2>
        <h2 v-show="isShow" id="bbb">v-show的{{message}}</h2>
    </div>
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                message: '你好啊',
                isShow: true
            }
        })
    </script>
</body>

</html>
~~~

### v-for指令

#### v-for遍历数组

> v-for其实不仅仅能遍历数组，还能遍历对象。

![](Vue框架入门/70.png)

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <!-- 1.在遍历的过程中，没有使用索引值(下标值) -->
        <ul>
            <li v-for="item in names">{{item}}</li>
        </ul>

        <!-- 2.在遍历的过程中，获取我们的索引值：下标值 -->
        <ul>
            <!-- 加小括号这种方式和元组很像 -->
            <li v-for="(item,index) in names">{{index+1}}.{{item}}</li>
        </ul>
    </div>
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                names: ['why', 'Kobe', 'James', 'Tom']
            }
        })
    </script>
</body>

</html>
~~~

#### v-for遍历对象

![](Vue框架入门/71.png)

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <!-- 方法1：这算是比较笨的方法，但是也是可以的 -->
        <ul>
            <li>{{info.name}}</li>
            <li>{{info.age}}</li>
            <li>{{info.height}}</li>
        </ul>

        <!-- 方法2-1：使用v-for遍历,获取value-->
        <!-- 在遍历对象的过程中，如果只是获取一个值，那么获取到的是value -->
        <ul>
            <!-- 遍历对象的话，不确定你每次给我的item到底是什么东西 -->
            <!-- 在数组中可以确定item是数组中的一个一个元素 -->
            <!-- 但是对象里面既包含key也包含value,所以不确定item到底是key还是value还是其他什么东西 -->
            <!-- 经过代码检测，item拿到的是value!!! -->
            <li v-for="item in info">{{item}}</li>
        </ul>

        <!-- 方法2-2：使用v-for遍历，获取key和value  格式：(value,key) -->
        <!-- 注意：前面是value,后面是key -->
        <ul>
            <li v-for="(value,key) in info">{{value}}- {{key}}</li>
        </ul>

        <!-- 方法2-3：使用v-for遍历，获取key,value和index   格式:(value,key,index)-->
        <ul>
            <li v-for="(value,key,index) in info">{{value}}- {{key}}-{{index}}</li>
        </ul>
    </div>
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                info: {
                    name: 'why',
                    age: 18,
                    height: 1.88
                }
            }
        })
    </script>
</body>

</html>
~~~

#### 组件的key属性

> 现在是2020年12月16日，我是一点都不懂diff算法的。

[Vue的diff算法解析](https://www.infoq.cn/article/uDLCPKH4iQb0cR5wGY7f)

[你了解 vue 的diff算法吗](https://juejin.im/post/6844903592483094535)

![](Vue框架入门/72.png)

![](Vue框架入门/73.png)

### 哪些数组方法是响应式的

![](Vue框架入门/74.png)

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <ul>
            <!-- <li v-for="item in letters" :key="item">{{item}}</li> -->
            <!-- 加上key的话可以让它内部的性能更高，不加也没事 -->

            <li v-for="item in letters">{{item}}</li>
            <!-- 算了，还是不先绑定key了，不然后面添加"aaa"时会报错 -->
        </ul>
        <button @click="btnClick">按钮</button>
    </div>
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                letters: ['A', 'B', 'C', 'D', 'E']
                // 并不是所有改变数据的方法都能做到响应式的
            },
            methods: {
                btnClick() {
                    // 1.push方法-后面添加元素(是响应式的)
                    // 如果绑定了key值的话控制台会报个错：
                    //vue.js:616 [Vue warn]: Duplicate(重复) keys detected: 'aaa'. 
                    //This may cause an update error.
                    //原因是key绑定了item，新增了很多同样的aaa,key值会重复
                    // this.letters.push('aaa');
                    // this.letters.push('aaa','bbb','ccc');
                    // push可以一次加多个


                    //2.pop()方法-删除数组中最后一个元素(是响应式的)
                    // this.letters.pop();

                    //3.shift()方法-删除数组中第一个元素(是响应式的)
                    // this.letters.shift();

                    //4.unshift()方法-在数组最前面添加元素(是响应式的)
                    // this.letters.unshift('ccc');
                    // this.letters.unshift('aaa','bbb','ccc');
                    // unshift也可以一次加多个

                    //5.splice()方法-数组中比较全能的方法(是响应式的)
                    //splice作用：插入元素/删除元素/替换元素
                    //第一个参数是start,3个作用第一个参数都一样
                    //删除元素：第二个参数传入你要删除几个元素(如果没传则删除后面所有元素)
                    //替换元素：第二个参数，表示我们要替换几个元素，后面跟着的是用于替换前面的元素
                    //插入元素：第二个参数，传入0，并且后面跟上要插入的元素
                    // 这个函数的关键就是第二个元素了！！！
                    // this.letters.splice(1, 2);  //把BC给删了
                    // this.letters.splice(1);  

                    // const start = 1;
                    // this.letters.splice(start, this.letters.length - start);

                    //this.letters.splice(1, 3, 'l', 'm', 'n');
                    //这个是替换

                    // this.letters.splice(1, 0, 'l', 'm', 'n');

                    //6.sort()方法-用于排序(是响应式的)
                    // this.letters.sort();

                    //7.reverse()方法-用于反转(是响应式的)
                    // this.letters.reverse();

                    //8.通过索引值修改数组中的元素(不是响应式，数组变了，但是界面不会改变)
                    //this.letters[0] = 'bbb';

                    //使用splice()进行替换从而达到想达到的效果
                    // this.letters.splice(0, 1, 'bbb');

                    //Vue中的set方法(Vue内部实现的函数)
                    //set(要修改的对象，索引值，修改后的值)
                    Vue.set(this.letters, 0, 'bbb');
                }
            }
        })

        //介绍可变参数
        // function sum(num1, num2) {
        //     return num1 + num2;
        // }

        // function sum(num1, num2, num3) {
        //     return num1 + num2 + num3;
        // }
        // 如果我的需求是想对10个数字相加，你也不能写十个num吧，办法是可以使用可变参数
        function sum(...num) {
            //当你的函数类似''...num'这样一个参数的时候(可变参数)
            //它会把你传入的多个值放入数组里面，然后再利用数组
            console.log(num);
        }
        sum(20, 30, 40, 50, 60);
    </script>
</body>

</html>
~~~

## 阶段案例：图书购物车

> 这个现在让我独立写我是写不出来的。

[过滤器](https://cn.vuejs.org/v2/guide/filters.html#ad)

![](Vue框架入门/75.png)

**HTML代码**

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <link rel="stylesheet" href="style.css">
</head>

<body>
    <div id="app">
        <!-- 把table和下面的总金额都包含在一个大div里面 -->
        <div v-if="books.length">
            <table>
                <thead>
                    <tr>
                        <th></th>
                        <th>书籍名称</th>
                        <th>出版日期</th>
                        <th>价格</th>
                        <th>购买数量</th>
                        <th>操作</th>
                    </tr>
                </thead>

                <tbody>
                    <!-- 通过遍历将数组中的数据展示出来 -->
                    <!-- 以前遍历都是li中使用v-for，现在遍历要在ul中使用v-for了 -->
                    <!-- 一本书是一行 -->
                    <tr v-for="(item,index) in books">
                        <!-- 1.0：item是一个对象，对象也是可以遍历的 -->
                        <!-- <td v-for="value in item">{{value}}</td> -->
                        <!-- 这个写法我现在不会 -->
                        <!-- 但是我们不建议遍历item这个对象，因为有些东西我们要定制，
                             比如数量前后都有按钮，价格保留2位小数，且前面有人民币符号 -->

                        <!-- 2.0：接下来我们自己写遍历item -->
                        <td>{{item.id}}</td>
                        <td>{{item.name}}</td>
                        <td>{{item.date}}</td>
                        <!-- <td>{{item.price}}</td> -->
                        <!-- 修饰价格：保留2位小数并且前面加上人民币符号(拼接即可)-->
                        <!-- <td>{{'￥' + item.price.toFixed(2)}}</td> -->
                        <!-- 但是这样写不好，待会计算出总价格的时候，结果也是保留2位小数的，
							 前面也有人民币符号 -->
                        <!-- 总价格那里也要进行拼接，很麻烦 -->
                        <!-- 这个拼接应该是可重复利用的才好-->
                        <!-- 方案1：可以使用methods -->
                        <!-- <td>{{getFinalPrice(item.price)}}</td> -->

                        <!-- 方案2：使用过滤器 -->
                        <!-- <td>{{item.price|过滤器}}</td> -->
                        <td>{{item.price|showPrice}}</td>
                        <td>
                            <button @click="decrement(index)" 
                                    v-bind:disabled="item.count <= 1">
                               		-
                            </button>
                            <!-- 动态绑定disabled属性，当数字减少为1时，
								 就变成disabled，不能点击 -->
                            {{item.count}}
                            <button @click="increment(index)">+</button>
                        </td>
                        <td>
                            <button @click="removeHandle(index)">移除</button>
                        </td>
                    </tr>
                </tbody>
                <!-- tbody在真实开发中肯定不是写死的，而是用户将书籍加入购物车中，动态的生成的 -->
                <!-- 在Vue里面我们用一个变量来保存数据 -->
            </table>
            <h2>总价格：{{totalPrice | showPrice}}</h2>
        </div>
        <h2 v-else>购物车为空</h2>
    </div>
    <script src="js/vue.js"></script>
    <script src="main.js"></script>
    <script>
        // 如何在JS里面给数字保留2位小数？？
        // 123.toFixed(2)即可;
    </script>
</body>

</html>
~~~

**CSS代码**

~~~css
table {
  border: 1px solid #e9e9e9;
  border-collapse: collapse;
  border-spacing: 0;
}

th,
td {
  padding: 8px 16px;
  border: 1px solid #e9e9e9;
  text-align: left;
}

th {
  background-color: #f7f7f7;
  color: #5c6b77;
  font-weight: 600;
}

~~~

**js代码**

~~~javascript
const app = new Vue({
  el: "#app",
  data: {
    books: [
      {
        id: 1,
        name: "《算法导论》",
        date: "2006-9",
        price: 85.0,
        count: 1,
      },
      {
        id: 2,
        name: "《UNIX编程艺术》",
        date: "2006-2",
        price: 59.0,
        count: 1,
      },
      {
        id: 3,
        name: "《编程珠玑》",
        date: "2008-10",
        price: 39.0,
        count: 1,
      },
      {
        id: 4,
        name: "《代码大全》",
        date: "2006-3",
        price: 128.0,
        count: 1,
      },
      //在data里面弄一个数组，一旦你把某本书弄到购物车里面，就在数组里面追加一个对象
    ],
  },
  methods: {
    //方案1：使用methods
    // getFinalPrice(price) {
    //   return "￥" + price.toFixed(2);
    // },
    decrement(index) {
      //console.log("减法", index);
      //因为每本书都有count,不确定是哪本书的count减法，所以要加一个参数index
      this.books[index].count--;
      //但是减法不能是负数，最少是1，之后按钮就要变成"disabled",不可以点击了
    },
    increment(index) {
      //console.log("加法", index);
      this.books[index].count++;
    },
    removeHandle(index) {
      //数组中的splice()方法有移除功能
      //把自己删除第二个参数传个1就可以了
      this.books.splice(index, 1);
    },
  },
  filters: {
    // 方案2：使用过滤器
    // 因为有多个，所以用复数s
    showPrice(price) {
      return "￥" + price.toFixed(2);
    },
  },
  computed: {
    //计算总金额用计算属性比较好
    totalPrice() {
      // 方法1：普通的for循环
      // let totalPrice = 0;
      // for (let i = 0; i < this.books.length; i++) {
      //   totalPrice += this.books[i].price * this.books[i].count;
      // }
      // return totalPrice;
      //注意这个return不要忘记写

      //方法2：for...in循环
      //for (let i in  this.books)
      // let totalPrice = 0;
      // for (let i in this.books) {
      //   // console.log(i);
      //   totalPrice += this.books[i].price * this.books[i].count;
      // }
      // return totalPrice;

      //方法3:for...of循环
      //for(let i od this.books)
      //let totalPrice = 0;
      //for (let item of this.books) {
        //totalPrice += item.price * item.count;
      //}
      //return totalPrice;

      //方法4：使用高阶函数
      //reduce
      return this.books.reduce(function(preValue,value){
        return preValue + book.price * book.count;
      },0)
    },
  },
});
~~~

### 补充知识：高阶函数的使用

[JavaScript 高阶函数浅析](http://muyiy.cn/blog/6/6.1.html#%E5%BC%95%E8%A8%80)

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <script>
        //编程范式划分1：命令式编程/声明式编程
        //编程范式划分2：面向对象编程(第一公民：对象)/函数式编程(第一公民：函数)
        //三个高阶函数：filter/map/reduce
        //高阶函数的意思是：函数本身需要的参数，它可能也是一个函数
        const nums = [10, 20, 111, 222, 444, 40, 50];

        // 需求1：要求把所有小于100的数字都取出来
        let newNums = [];
        for (let n of nums) {
            //for...in保存的是键名(key)
            //for...of保存的是键值(value)
            if (n < 100) {
                newNums.push(n);
            }
        }
        console.log(newNums);

        // 需求2：将所有小于100的数字进行转化，全部乘以2
        let new2Nums = [];
        for (let n of newNums) {
            new2Nums.push(n * 2)
        }
        console.log(new2Nums);

        // 需求3：将new2Nums里面的数字相加，得到最终的结果
        let total = 0;
        for (let n of new2Nums) {
            total += n;
        }
        console.log(total);

        //如果用高阶函数来做这3个需求，一切都会变得简单很多了

        // filter第一个参数就是一个函数
        // 而这个函数的第一个参数则表示数组当前项的值，第一次是10，第二次是20，所以一共会回调7次 
        // filter中的回调函数有一个要求：必须返回一个布尔值(true或false)
        // true:当返回true时，函数内部会自动将这次回调的value加入到新的数组中去
        // false:当返回false时，函数内部会过滤掉这次的value(不再使用这个value了，过滤掉了)

        // 高阶函数filter实现需求1
        let new3Nums = nums.filter(function (value) {
            // 第一个参数(函数)必须返回一个布尔值
            // return true;
            return value < 100;
            // 过滤掉大于100的项，只留下小于100的项，变成新的数组
        })
        console.log(new3Nums);

        // 高阶函数map实现需求2
        let new4Nums = newNums.map(function (value) {
            // 这个函数每次返回的值会作为我们新的值
            // return 100;
            return value * 2;
            // 20,40,80,100
        })
        console.log(new4Nums);

        // 高阶函数reduce实现需求3
        //用法：对数组中所有内容进行汇总(比如数组中所有内容进行相加)
        let total1 = new4Nums.reduce(function (preValue, value) {
            //reduce有2个参数，第一个参数是函数，里面还有2个参数；第2个参数是初始化值，我们一般填0
            // preValue表示前一个值，value表示当前的值
            // 数组中有4个值，所以这个函数会遍历4次
            // 第1次：preValue为0(因为它的初始化为0)——在我们的案例里面value是20
            // 第2次：preValue为0+20(它返回100)——在我们的案例里面value是40
            // 第3次：preValue为0+20+40(它返回100)——在我们的案例里面value是80
            // 第4次：preValue为0+20+40+80(它返回100)——在我们的案例里面value是100
            // return 0+20+40+80+100=240;
            return preValue + value;
        }, 0)
        console.log(total1);

        // 终结版：通过高阶函数直接把240给弄出来
        // 进行链式编程
        // 原先要写三坨代码才能得到240，现在只要1坨代码就可以了！！！牛皮！！
        let total2 = nums.filter(function (value1) {
            return value1 < 100;
        }).map(function (value1) {
            return value1 * 2;
        }).reduce(function (preValue1, value1) {
            return preValue1 + value1;
        }, 0)
        console.log(total2);

        // 使用箭头函数的终结版:看上去更加的简洁优美
        let total3 = nums.filter(value2 => value2 < 100)
            			  .map(value2 => value2 * 2)
            			  .reduce((preValue2, value2) => (preValue2 + value2));
        console.log(total3);
    </script>
</body>
</html>
~~~

## 表单绑定

### 基本使用

> 单独把一个指令做一小节，可见这个指令还是很重要的。

![](Vue框架入门/76.png)

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <input type="text" v-model="message">
        <!-- 直接在input标签里面写上v-model指令 -->
        <!-- v-model可以实现数据的双向绑定 -->

        <!-- 以前的响应式，你把元素里面的内容改了，app里面的message是不会变的 -->
        <!-- 即以前的胡子语法只能实现单向绑定 -->
        {{message}}
    </div>
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                message: '你好啊'
            }
        })
    </script>
</body>
</html>
~~~

### v-model基本原理

[input事件](https://developer.mozilla.org/zh-CN/docs/Web/Events/input)

> 当一个 `<input>`, `<select>`, 或 `<textarea> `元素的 value 被修改时，会触发 input 事件。

![](Vue框架入门/77.png)

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <!-- <input type="text" v-model="message"> -->
        <!-- v-model实际上相当于是两个指令的结合，它就是一个语法糖 -->
        <!-- 我不用v-model,我也能实现双向绑定 -->

        <!-- 第一步：把下面的message想办法绑定到上面来 -->
        <!-- <input type="text" :value="message"> -->

        <!-- 第二步： -->
        <!-- v-on上面有个input事件(内部事件)，就像button有个click一样 -->
        <input type="text" :value="message" v-on:input="valueChange">

        <!-- <input type="text" :value="message" v-on:input="valueChange1(event)"> -->
        <!-- valueChange1()函数有一个参数event,但是这里不用写，参数会自动带上来 -->
        <input type="text" :value="message" v-on:input="valueChange1">

        <input type="text" :value="message" @input="message = $event.target.value">
        <!-- 不想写表达式了，直接这样写也行 -->
        <!-- $event在v-on那一节里讲过，记忆不深刻 -->
        <h2>{{message}}</h2>
    </div>
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                message: '你好啊'
            },
            methods: {
                valueChange() {
                    // console.log('---------------');
                    // 我一旦在表单里面输入内容或内容发生变化都会触发这个函数
                    // 当一个 <input>, <select>, 或 <textarea> 元素的 value 被修改时，
                    // 会触发 input 事件。

                    // message = "aaa";
                    this.message = "aaa";
                    // 一旦表框里面的内容发生变化，下面的message就变成了aaa
                    // 我对this的理解还是不那么透彻啊，前面不写this就不行
                },
                valueChange1(event) {
                    // 要获取到app下面的message,要通过event来获取
                    // 一旦在界面上产生一个事件之后，浏览器会生成一个event对象
                    // event对象里面就会包含我们想要的信息了
                    // this.message = "bbb";
                    console.log(event);
                    this.message = event.target.value;
                    // event里面有一个target,target里面有一个value
                    // 我找了一下确实可以找到
                }
            },
        })
    </script>
</body>
</html>
~~~

### 其他类型

#### v-model：radio

[< label>标签](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/label)

![](Vue框架入门/78.png)

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <label for="male">
            <input type="radio" id="male" name="sex" value="男" v-model="sex">男
            <!-- 绑定了相同的v-model="sex",此时name可以不用写也能实现互斥了！！ -->
            <!-- 在没有v-model的情况下，必须添加name属性，2个选项才能互斥，-->
			<!-- 有了v-model就可以不用添加name属性了 -->
        </label>

        <label for="female">
            <input type="radio" id="female" name="sex" value="女" v-model="sex">女
        </label>
        
        <h2>您选择的性别是：{{sex}}</h2>
        <!-- 用户在选择时，要么选择男，要么选择女，现在可以两个都选上，有问题 -->
        <!-- 我们要让这2个input互斥:给它们每个人都加上相同的name:sex即可-->
        <!-- 一旦两个radio绑定的都是sex,name可以不用写！！！ -->
        <!-- 往服务器提交表单的时候，key都是name,2个key的名字相同只能提交一个-->
    </div>
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                message: '你好啊',
                // sex: ''
                // 我在表单里选择男，你就把男绑定到下面的sex里面，选择女同理。
                sex: '男'
                // 如果想要有个默认值，sex可以填上内容，如"男",因为数据双向绑定，
                //所以上面的单选按钮选项会选择为男
            }
        })
    </script>
</body>
</html>
~~~

#### v-model：checkbox

[checkbox的value和checked属性详解](https://blog.csdn.net/kouryoushine/article/details/87984749)

![](Vue框架入门/79.png)

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <!-- 不是很理解checkbox里面的value属性有什么用 -->

        <!-- 1.checkbox为单选框的用法 -->
        <label for="agree">
            <input type="checkbox" id="agree" v-model="isAgree">同意协议
        </label>
        <h2>您选择的是：{{isAgree}}</h2>
        <button :disabled="!isAgree">下一步</button>

        <br><br><br>
        <!-- 2.checkbox为多选框的用法 -->
        <!-- <label for=""> -->
        <!-- 多选框就不要用label了，因为一般一个label绑定一个input,-->
		<!-- 不能一个label绑定多个input -->
        
        
        <!-- checkbox在里面写value不会显示文字，value用于之后我获取的文字 -->
        <!-- 所以还要在input标签外面写上这些球的名字 -->
        <input type="checkbox" value="足球" v-model="hobbies">足球
        <input type="checkbox" value="网球" v-model="hobbies">网球
        <input type="checkbox" value="棒球" v-model="hobbies">棒球
        <h2>您的爱好是：{{hobbies}}</h2>
        <!-- </label> -->
    </div>
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                message: '你好啊',
                // isAgree: '否'
                isAgree: false,  //单选框
                hobbies: []      //多选框
                //你首先要弄一个变量，这个变量是数组类型，记录这个人所有的爱好
                //当你有多个选项的时候，你就不再是一个值了
                //checkbox里如果没有value属性，当你点击选项框时，数组中您的爱好会显示null
            }
        })
    </script>
</body>
</html>
~~~

#### v-model：select

![](Vue框架入门/80.png)

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <!-- 现在很少有网站用select了，但是我们还是演示一下 -->
        <!-- 1.选择一个 -->
        <select name="abc" v-model="fruit">
            <!-- name是往服务器提交的时候的一个key -->
            <!-- 注意：v-model是往select标签里写的，不是往option标签里写的 -->
            <option value="苹果">苹果</option>
            <option value="香蕉">香蕉</option>
            <option value="橘子">橘子</option>
            <option value="芒果">芒果</option>
        </select>
        <h2>您选择的水果是：{{fruit}}</h2>


        <!-- 2.选择多个 -->
        <select name="abc" v-model="fruits" multiple>
            <!-- id不能2个都为空，所以索性把select标签里的id给删掉了 -->
            <option value="苹果">苹果</option>
            <option value="香蕉">香蕉</option>
            <option value="橘子">橘子</option>
            <option value="芒果">芒果</option>
        </select>
        <h2>您选择的水果是：{{fruits}}</h2>
    </div>
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                message: '你好啊',
                fruit: "香蕉",
                fruits: []
            }
        })
    </script>
</body>
</html>
~~~

### 补充知识：值绑定

> 值绑定的意思是数据不要写死，而是动态的去获取。

![](Vue框架入门/81.png)

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <!-- 上面的这些都被写死了，实际中不能写死-->
        <!-- <input type="checkbox" value="篮球" v-model="hobbies">篮球
        <input type="checkbox" value="足球" v-model="hobbies">足球
        <input type="checkbox" value="网球" v-model="hobbies">网球
        <input type="checkbox" value="棒球" v-model="hobbies">棒球 -->

        <label v-for="item in originHobbies" :for="item">
            <input type="checkbox" :value="item" :id="item" v-model="hobbies">{{item}}
        </label>
        <h2>您的爱好是：{{hobbies}}</h2>
    </div>
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                message: '你好啊',
                // isAgree: '否'
                isAgree: false,  //单选框
                hobbies: [],      //多选框
                originHobbies: ['篮球', '足球', '网球', '棒球']
                // 你先来一个原始的，这样上面就不用写死了
            }
        })
    </script>
</body>
</html>
~~~

### 补充知识：修饰符

> 前面我们将事件监听的时候也讲过修饰符

![](Vue框架入门/82.png)

> 现在是2020年12月16日，截止到上面看完。上面的知识虽然很基础，但是我发现我并不熟悉，很多知识点也没有透彻的理解，自己单独写肯定也写不出来。基础还是要继续打扎实一点啊！！！

# 组件化开发

> 组件部分我又单独写了一篇博文《Vue组件复习》，又重头把它再学了一下，里面写的内容和下面的几乎完全一样，不过我觉得这是一种十分必要的重复。现在已经不一味的追求进度了，打好基础最重要了。
>
> 组件化是一种非常重要的思想，就是初中时学的课文《走一步，再走一步》中从整到零，从繁到简的思想。后面还会学习模块化思想，到时候可以对比一下，二者是不一样的。
>
> 现在是2020年12月26日，文章我已经来来回回看了几遍了，但是没有敲代码，今天放假，我又把之前学的组件有关代码重头敲了一遍。

## 认识组件化

[vue 实例与组件的关系](https://blog.csdn.net/weixin_41796631/article/details/89048282)

> 组件其实就是实例。
>
> 一个Vue项目是由一个根实例和多个组件组成，组件其实就是实例。只不过是为了区分使用方式，所以才用了两个叫法，即组件和实例
>
> 区分什么使用方式呢？
>
> 一般说的实例就是根实例，一个Vue项目只能有一个（new Vue）
>
> 一个Vue项目能有多个组件，并且每个组件都可重复使用。

### 什么是组件化

![](Vue框架入门/31.png)

### Vue组件化思想

![](Vue框架入门/32.png)

> 一个大的页面是一个组件，所以最上面是一个正方形。

## 组件化基础

### 注册组件

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <!-- 方法2：利用组件化思想引用某段代码 -->
    <!-- 在div的外面写 -->
    <!-- cpn这个标签名是我们自己起的名字 -->
    <cpn>
        <h2>我是标题-组件</h2>
        <p>我是内容，哈哈哈-组件</p>
        <p>我是内容，呵呵呵-组件</p>
    </cpn>

    <div id="app">
        <!-- 但是这样写只能有一个生效，其他2个都没生效 -->
        <cpn></cpn>
        <cpn></cpn>
        <cpn></cpn>
    </div>

    <div id="app">
        <!-- 组件只能够在Vue的实例范围之内使用，这里可以用，因为它受Vue管理 -->
        <!-- 方法1：通过复制粘贴方式重复引用某段代码 -->
        <h2>我是标题</h2>
        <p>我是内容，哈哈哈</p>
        <p>我是内容，呵呵呵</p>
        <!-- 这里面的代码想多次使用，以前你可能会复制粘贴这段代码 -->
        <h2>我是标题</h2>
        <p>我是内容，哈哈哈</p>
        <p>我是内容，呵呵呵</p>
        <!-- 使用复制粘贴的方式进行多次引用 -->
        <h2>我是标题</h2>
        <p>我是内容，哈哈哈</p>
        <p>我是内容，呵呵呵</p>
        <!-- 但是这种方式不好，存在大量的重复代码 -->
    </div>

    <div>
        <!-- 这里就没有办法用Vue组件了，不受Vue管理 -->
    </div>
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                message: '你好啊'
            }
        })
    </script>
</body>
</html>
~~~

#### 注册的基本步骤

![](Vue框架入门/33.png)

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <!-- 步骤3：使用组件 -->
        <!-- 这个组件写好后，另一个页面，甚至另一个项目中都能使用它 -->
        <my-cpn></my-cpn>
        <my-cpn></my-cpn>
        <my-cpn></my-cpn>
        <!-- 这个是组件的标签名，下面定义的 -->
    </div>
    <script src="js/vue.js"></script>
    <script>
        // ES6的新的语法:``
        //以前用双引号，单引号定义字符串，现在可以用``来定义字符串了
        //``的功能更加强大，它可以换行定义(以前用单双引号换行要加一个+号)
        //`abc`

        // 步骤1：创建组件构造器对象
        const cpnC = Vue.extend({
            // extend要传入参数，和new Vue一样，传入的参数也是一个对象
            template: `
                <div>
                    <h2>我是标题</h2>
                    <p>我是内容，哈哈哈</p>
                    <p>我是内容，呵呵呵</p>
                </div>`
        })

        // 步骤2：注册组件(通过这种方式注册的组件就是全局组件)
        // 要传入2个参数
        // Vue.component('组件的标签名', 组件构造器)
        Vue.component('my-cpn', cpnC)
      	//Vue.component语句是在script标签里面的
        const app = new Vue({
            el: '#app',
            data: {
                message: '你好啊'
            }
        })
    </script>
</body>
</html>
~~~

![](Vue框架入门/34.png)

![](Vue框架入门/35.png)

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <my-cpn></my-cpn>
        <!--位置1：组件在id为app的div里(在Vue的实例里)-->
        <div>
            <div>
                <my-cpn></my-cpn>
                <!-- 位置2：组件在id为app的div的更深几层(也在Vue的实例里) -->
            </div>
        </div>
    </div>
    <my-cpn></my-cpn>
    <!-- 位置3：组件不在id为app的div里(不在Vue的实例里，这个不行，无法渲染出来) -->
    <!-- 只会显示这个标签，但浏览器不认识这个标签，所以没有太大意义 -->
    <script src="js/vue.js"></script>
    <script>

        const cpnC = Vue.extend({
            template: `
                <div>
                    <h2>我是标题</h2>
                    <p>我是内容，哈哈哈</p>
                    <p>我是内容，呵呵呵</p>
                </div>`
        })
        Vue.component('my-cpn', cpnC)
        const app = new Vue({
            el: '#app',
            data: {
                message: '你好啊'
            }
        })
    </script>
</body>
</html>
~~~

#### 全局和局部组件

![](Vue框架入门/83.png)

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <cpn></cpn>
        <cpn></cpn>
        <cpn></cpn>
    </div>

    <div id="app2">
        <cpn></cpn>
    </div>
    <script src="js/vue.js"></script>
    <script>
        // 1.创建组件构造器
        // cpnC是cpnContructor的缩写
        const cpnC = Vue.extend({
            template: `
                <div>
                    <h2>我是标题</h2>
                    <p>我是内容，哈哈哈</p>
                </div>  
            `
        })
        // 2.注册组件(全局组件!!!意味着可以在多个Vue实例下面使用)
        // 全局组件这样写
        // Vue.component('cpn', cpnC)
        // 我们之前在Vue开发的时候，只是创建了一个Vue实例对象(开发中可以有很多个)
        // 但是真实开发一般只有一个

        // 疑问：怎么注册的组件才是局部组件呢
        // 答：你去某个Vue的实例下面注册，它就只能在这个Vue的实例下面用了
        const app = new Vue({
            el: '#app',
            data: {
                message: '你好啊'
            },
            components: {
                // 直接在Vue实例里面注册组件，就只能在这个Vue实例里用了
                // components是复数，意味着可以注册多个组件
                // 局部组件这样写
                cpn: cpnC
                // 这个是使用组件时的标签名
                // 和上面的全局组件的写法Vue.component('cpn', cpnC)效果一样，
              	// 只不过这是局部组件的写法
                // components是个对象，key(cpn)就是标签名，value(cpnC)就是组件构造器
                // 在开发中用的最多的还是局部组件
            }
        })

        const app2 = new Vue({
            el: '#app2'
        })
    </script>
</body>
</html>
~~~

#### 父组件和子组件

[Vue中到底是什么是父组件，什么是子组件？](https://segmentfault.com/q/1010000008766204)

> 在我们组件化开发过程中，有些组件是互为父子关系的。

![](Vue框架入门/84.png)

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <cpn2></cpn2>
        <cpn1></cpn1>
        <!-- 单独写cpn1无法渲染，还会报错 -->
        <!-- 在Vue实例这个作用域里面，要想使用某一个组件，要么它是一个全局组件，
             要么在Vue实例中组件的components里已经注册过了(只注册过cpnC2,没有注册过cpnC1)
             所以直接在上面写cpn1会报错，写cpn2的话会渲染出里面的cpn1,
             儿子自己不能展示，只能通过爸爸像别人介绍来展示自己的儿子
             要想儿子自己独立展示，只能在Vue实例中再单独自己注册一次cpn1:cpnC1-->
    </div>
    <script src="js/vue.js"></script>
    <script>
        // 因为是父子组件，所以我至少要创建2个组件才行
        // 1.创建第一个组件构造器cpnC1(子组件)
        const cpnC1 = Vue.extend({
            template: `
                <div>
                    <h2>我是儿子标题</h2>   
                    <p>我是儿子，哈哈哈</p> 
                </div>
            `
        })

        // 2.创建第二个组件构造器cpnC2(父组件)
        const cpnC2 = Vue.extend({
            template: `
                <div>
                    <h2>我是爸爸标题</h2>   
                    <p>我是爸爸，呵呵呵</p> 
                    <cpn1></cpn1>
                </div>
            `,
            // 我们之前只给它添加了一个属性：template,其实它还可以添加别的属性
            components: {
                // 这个components不是放到Vue实例里的，而是放到组件构造器对象里的
                cpn1: cpnC1
              	//这里子组件cpn1在父组件cpn2里面注册了
                // 如果cpn1只在这里注册，不再Vue实例里再注册一次，则永无出头之日，
                // 只能通过爸爸向其他人展示，自己不能主动展示
            }
        })
        // root组件
        const app = new Vue({
            //  Vue实例其实你也可以把它看成是一个组件，它是最顶层的组件(root)
            //  Vue实例是爷爷，cpnC2是爸爸，cpnC1是儿子
            el: '#app',
            data: {
                message: '你好啊'
            },
            components: {
                cpn2: cpnC2,
                // 组件构造器cpnC1不是在Vue实例里注册的，而是在组件构造器cpnC2里注册的
                // 要想自己主动单独展示，而不是被动的通过爸爸展示，需要在这里再注册一次
                cpn1: cpnC1
                // 不写这个会报错
              	//这里子组件cpn1又在Vue实例里面注册了
            }
        })
        // 总结：组件构造器cpnC1放在组件构造器cpnC2里面注册的，
        // 而组件构造器cpnC2是放在Vue实例里注册的
        // 这样就可以保证2个组件构造器都注册过了
    </script>
</body>
</html>
~~~

#### 注册组件语法糖

> 现在已经很少有`Vue.extend()`这样的写法了，现在基本上都用**语法糖**来实现注册组件了。

![](Vue框架入门/85.png)

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <cpn1></cpn1>
        <!-- 这个是全局组件 -->
        <cpn2></cpn2>
        <!-- 这个是局部组件 -->
    </div>
    <script src="js/vue.js"></script>
    <script>
        // 全局组件注册的原始写法
        // 1.创建组件构造器
        // const cpnC = Vue.extend({
        //     template: `
        //         <div>
        //             <h2>我是标题</h2>    
        //             <p>我是内容，哈哈哈</p>
        //         </div>
        //     `
        // })
        // // 2.注册组件(全局组件，可以在实例下面使用)
        // Vue.component('cpn1', cpnC)

        // 全局组件注册的语法糖写法:创建组件构造器和注册组件一步到位，放在一起写。
        Vue.component('cpn1', {
            template: `
                <div>
                    <h2>我是标题</h2>    
                    <p>我是内容，哈哈哈</p>
                </div>
            `
        })
        // 但是本质上内部还是会调extend方法的
        const app = new Vue({
            el: '#app',
            data: {
                message: '你好啊'
            },
            components: {
              	//但是要使用对象写法，函数写法会报错
                // 局部组件注册的语法糖写法
                cpn2: {
                    template: `
                <div>
                    <h2>我是标题-局部</h2>    
                    <p>我是内容，呵呵呵-局部</p>
                </div>`
                }
            }
        })
    </script>
</body>
</html>
~~~

#### 模版的分离写法

> 如果你在JS代码里面写很多HTML代码的话(template属性里面的内容)，就会感到很乱。

![](Vue框架入门/86.png)

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <cpn></cpn>
        <cpn></cpn>
        <cpn></cpn>
    </div>
    <!-- 写法1：通过script标签-->
    <!-- 注意：这个type类型不要写错了，是text/x-template类型-->
    <script type="text/x-template" id="cpn">
    <div>
        <h2>我是标题-方法1</h2>
        <p>我是内容，哈哈哈</p>
    </div>
    </script>

    <!-- 写法2：使用template标签 -->
    <template id="cpn1">
        <div>
            <h2>我是标题-方法2</h2>
            <p>我是内容，呵呵呵</p>
        </div>
    </template>
  
    <script src="js/vue.js"></script>

    <script>
        //1.注册一个全局组件
        // 写在script标签里面，我都快搞晕了
        Vue.component('cpn', {
            // template: '#cpn',
          	// 使用方法1:script标签
            template: '#cpn1',
          	// 使用方法2:template标签
            // 这个模版内容写在最上面，使用id让二者产生联系，采用了分离的写法
        })
        const app = new Vue({
            el: '#app',
            data: {
                message: '你好啊'
            }
        })
    </script>
</body>
</html>
~~~

> 现在是2020年12月22日，截止到上面复习完，能看懂。

#### 组件的其他属性

> 我们前面学的组件里的内容都是写死的，能不能把组件里的数据抽离到一个变量里面，之后通过胡子语法直接显示这个变量？如果这样可以的话，我就可以改变这个变量，界面就会自动刷新了。
>
> 那么这个变量放到哪里呢？可以放到data属性里吗？——不可以。
>
> **组件内部是不能访问Vue实例里面的数据的**。

![](Vue框架入门/87.png)

![](Vue框架入门/88.png)

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <cpn></cpn>
        <cpn></cpn>
        <cpn></cpn>
    </div>

    <template id="cpn">
        <div>
            <!-- <h2>{{message}}</h2> -->
            <!-- 这样写不行，组件内部是无法访问到Vue实例里的数据的 -->
            
            <h2>{{title}}</h2>
            <!-- 这个title是组件里面data函数定义的变量 -->
            <p>我是内容，呵呵呵</p>
        </div>
    </template>
  
    <script src="js/vue.js"></script>

    <script>

        Vue.component('cpn', {
            template: '#cpn',
            // data: {
            //     title: 'abc'
            //     // 如果硬要写对象类型的话会报错
            // }
            // 这个data属性用于存放组件内部属于我自己的一些变量，这样就不会写死了
            // Vue实例里的data是一个对象类型，但是组件里的data不能是对象类型，只能是函数！！！
            data() {
                return {
                    title: 'abc'
                    // data本身是一个函数，返回的是一个对象，这个则没有问题
                }
            }
        })
        const app = new Vue({
            el: '#app',
            data: {
                message: '你好啊',
              	title: '我是标题'
              	//如果组件中的data里面没有定义title,即使Vue实例里面定义了title也没用
              	//它是找不到Vue实例里的title的！！！
            }
        })
    </script>
</body>
</html>
~~~

> 其实组件的原型就是指向Vue的，所以**Vue实例里面的很多东西组件里面也有**。

![](Vue框架入门/89.png)

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <!-- 组件实例：就是实例对象的意思 -->
    <div id="app">
        <cpn></cpn>
        <cpn></cpn>
        <cpn></cpn>
        <!-- 根据下面注册的组件，创建出来了3个组件实例 -->
        <!-- 这3个组件实例有无共享同一个data对象啊？？？ 答案是否！！！-->
        <!-- 因为组件中的data是一个函数，创建组件实例时会调用data函数，-->								<!-- 我们会在每次调用的时候return个新的对象-->
    </div>

    <template id="cpn">
        <div>
            <h2>当前计数：{{counter}}</h2>
            <button @click="increment">+</button>
            <button @click="decrement">-</button>
            <!-- 这2个方法不能写到Vue实例里面！！ -->
            <!-- 组件里面还可以有自己的methods，写到组件里的methods里面 -->
        </div>
    </template>

    <script src="js/vue.js"></script>
    <script>
        // 1.注册组件(先来个全局的)
        Vue.component('cpn', {
            template: '#cpn',
            data() {
                return {
                    counter: 0
                }
            },
            methods: {
                // 组件也有自己的methods
                // 组件就是一个封闭的空间，我自己里面有自己的数据，有自己的方法
                increment() {
                    this.counter++
                },
                decrement() {
                    this.counter--
                }
            }
        })
        const app = new Vue({
            el: '#app',
            data: {
                message: '你好啊'
            }
        })
    </script>

    <script>
        // 例子1：obj1,obj2,obj3不是同一个对象
        function abc() {
            return {
                name: 'why',
                age: 18
            }
        }

        let obj1 = abc();
        let obj2 = abc();
        let obj3 = abc();
        // 调用了3次abc函数，函数有返回值，分别给个名字obj1,obj2,obj3
        // 问题：obj1,obj2,obj3是不是同一个对象？？？肯定不是！！！
        // 因为函数每次执行的时候都会在栈空间创建很多新的变量

        // 验证obj1，obj2，obj3不是同一个对象——比较内存地址
        obj1.name = 'Kobe';
        console.log(obj2.name);     //why
        console.log(obj3.name);     //why
        // 改变obj1的name,obj2和obj3中的name都没有变化，所以它们3个不是同一个东西


        //例子2:obj4,obj5,obj6是同一个对象
        const objj = {
            name: 'why',
            age: 18
        }

        function bcd() {
            return objj;
        }

        let obj4 = bcd();
        let obj5 = bcd();
        let obj6 = bcd();
        // 此时obj4,obj5,obj6是同一个对象！！！
      
        obj4.name = 'Kobe';
        console.log(obj5.name);     //Kobe
        console.log(obj6.name);     //kobe

        // 所以如果data不是函数而是对象的话，所有的组件实例都会引用同一个data对象
        // 这个时候你改其中一个组件，其他组件也都会改变，所有的组件之间都相互关联，没有独立性。
        // 组件之间一定要独立！！改了这个组件不能其他组件也会随着变化，这样就会乱套了！！！
    </script>
</body>
</html>
~~~

### 数据传递

> 组件通信这块我是真的薄弱啊！！要多看几遍，查漏补缺。
>
> 现在是2020年12月23日，再来复习一遍，好好看，仔细消化。
>
> 我决定再把这个知识点的视频再看一遍，这是一个不错的决定。

[Vue组件选项props](https://www.cnblogs.com/xiaohuochai/p/7388866.html)

[【Vue原理】Props - 白话版](https://cloud.tencent.com/developer/article/1479097)

![](Vue框架入门/90.png)

> props是properties(属性)的**缩写**。

#### 父级向子级传递

![](Vue框架入门/91.png)

![](Vue框架入门/92.png)

> 凌晨看的视频，头脑晕乎乎的，然后概念又不容易懂，所以看的效果不好，之后还要再反复看一下课堂代码。
>
> 现在是2020年10月5日，我没有再继续看下去视频了，我先暂停，把之前的组件又重头到尾再复习了一遍，代码重新敲了一遍，现在感觉好多了，只有知识点掌握扎实了，才能看接下来的视频，不然脑子里一团浆糊，看了也是白看。
>
> 现在是2020年11月12日，组件通信这块已经忘光了，基础掌握的极其不牢固，导致后面学Vuex的时候卡壳了，所以回过头来再重新学一遍。
>
> 现在是2020年12月13日，我又重新来复习一遍组件部分的知识了啊，到时候还会把后面的Vuex，Axios等都看看别的视频再复习一遍的。
>
> 现在是2020年12月23日，我现在头脑明显清楚很多了，对于组件通信总算是入门了吧。

**写法1：**

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <cpn cmovies="movies" cmessage="message"></cpn>
        <!-- 如果不写v-bind:它就会把字符串赋值给变量 -->
        <cpn v-bind:cmessage="message" v-bind:cmovies="movies" ></cpn>
    </div>

    <template id="cpn1">
        <!-- 这个是子组件的模版 -->
        <div>
            <!-- {{movies}} -->
            <!-- 我们是不能直接使用Vue实例里的数据的 -->
            <!-- 但是可以用组件中定义的自己的变量：cmessage和cmovies-->
            <h2>{{cmessage}}</h2>
            <p>{{cmovies}}</p>
            <ul>
                <li v-for="item in cmovies">{{item}}</li>
            </ul>
        </div>
    </template>

    <script src="js/vue.js"></script>
    <script>
        // 父传子：props
        // 这种写法是省略了Vue.component吧？？？——是的
        const cpnC = {
            template: '#cpn1',
            // 方式1：传入数组——不好，怪怪的
            // props: ['cmovies', 'cmessage'],
            // 不要把它当成字符串，把它当成变量
            // 但是把变量的名字放到字符串里面看起来就有点别扭
            // props有好几种类型，可以写成数组或者对象
            // c表示children:子组件

            //方式2：传入对象
            props: {
                // 1.类型限制
                // cmovies: Array,
                // cmessage: String,

                // 2.提供一些默认值
                cmessage: {
                    type: String,
                    default: 'aaa',
                    // default是指当别人没有给你传值的情况下，默认值是什么
                    required: true
                    // 表明cmessage必须要传值
                },
                cmovies: {
                    // 类型是对象或数组时，默认值必须是一个函数
                    type: Array,
                    // default: []     //Vue2.5.17以下没问题
                    default() {
                        return []
                        // 这样写就不会报错了
                    }
                }
            }
        }

        const app = new Vue({
            el: '#app',
            data: {
                message: '你好啊',
                movies: ['海王', '海贼王', '海尔兄弟']
                // 这个数据是定义在父组件(root组件)中的(Vue实例里)
            },
            components: {
                // 写法1：普通写法
                // cpn: cpn

                // 写法2：增强写法——直接写个cpn
                // cpn

                // 我还不太熟，先写下面这个吧
                cpn: cpnC
            }
        })

        // 对象自变量增强写法之属性的增强写法
        // const name = 'why'
        // const obj = {
        //     // name: name,
        //     // 写法1：普通写法
        //     name
        //     // 写法2：增强写法——直接写个name
        // }
    </script>
</body>

</html>
~~~

> 这段代码看的晕晕乎乎的，看不太通透。
>
> 哈哈，现在不晕了。
>
> 现在是2020年12月23日，我终于能完全看得懂这段代码了。

**写法2：**

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <cpn :cmessage='message' :cmovies="movies"></cpn>
    </div>

    <template id="cpn">
        <div>
            <!-- 这个div不能少！！我少写了div就报错了，找了好久错误在哪！！ -->
            <p>{{cmessage}}</p>
            <p>{{cmovies}}</p>
        </div>
    </template>
  
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                message: '你好啊',
                // 这个message是在data里面的,data是在Vue实例里面的(组件中无法访问)
                movies: ['海王', '海贼王', '海尔兄弟']
                // movies也是在Vue实例里面的(组件中无法访问)
            },
            components: {
                cpn: {
                    template: '#cpn',
                    props: {
                        // props不仅可以传入数组，也可以传入对象
                        cmessage: {
                            // c表示child，子组件在父组件(Vue实例)里借窝生蛋(注册组件)
                            type: String,
                            default: 'aaa',
                            // default是指当别人没有给你传值的情况下，默认值是什么
                            // required: true
                            // 表明cmessage必须要传值
                        },
                        cmovies: {
                            type: Array,
                            // 类型是对象或数组时，默认值必须是一个函数
                            default() {
                                return []
                                // 这样写就不会报错了
                            }
                        }
                    }
                }
            }
        })
    </script>
</body>
</html>
~~~

##### 补充知识：props中的驼峰标识

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <!-- <cpn :cInfo="info"></cpn> -->
        <!-- 这里是不支持驼峰写法的，所以写cInfo是不认识的 -->
        <cpn :c-info="info"></cpn>
        <!-- 如果一定要写驼峰方法：可以在中间加个横杠 -->
        <!-- <cpn :cinfo="info"></cpn> -->
    </div>
    
    <template id="cpn">
        <h2>{{cInfo}}</h2>
    </template>
    
    <script src="js/vue.js"></script>
    <script>
        const cpn = {
            template: '#cpn',
            props: {
                // props一般都用对象
                cInfo: {
                    type: Object,
                    default() {
                        // default如果是对象的话必须要是一个函数
                        return {}
                    }
                }
            }
        }
        const app = new Vue({
            el: '#app',
            data: {
                info: {
                    // 现在的个人信息是被定义在父组件里面了(root组件)
                    //想要把父组件的个人信息传到子组件里面并且做一个展示
                    name: 'why',
                    age: 18,
                    height: 1.88
                }
            },
            components: {
                cpn
                // ES6属性增强写法
            }
        })
    </script>
</body>
</html>
~~~

> 现在是2020年12月23日下午5点，我流鼻血了，也快下班了，就看到这里吧。

#### 子级向父级传递

[Vue通过$emit实现父子组件的通讯原理](https://juejin.cn/post/6844904115806404615)

[观察者模式 vs 发布订阅模式](https://zhuanlan.zhihu.com/p/51357583)

[Vue中$emit应用](https://segmentfault.com/a/1190000019363722)

> 下面的代码及其不熟悉啊！！！因为`$emit()`的不熟，导致后面做项目也是懵逼的。

![](Vue框架入门/93.png)

![](Vue框架入门/297.png)

![](Vue框架入门/94.png)

**写法1：**

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <!-- 这个是父组件的模版！！！ -->
    <div id="app">
        <cpn v-on:item-click="cpnClick"></cpn>
      	<!-- 父组件任务：监听事件-->
      	<!--v-on以前都是监听click等默认的事件，其实它也可以监听子组件发射出去的事件-->
        <!-- 子组件发射出去的事件也是一种事件，也可以监听 -->
        <!-- 不要写驼峰，用横杠代替 -->
        <!-- 在脚手架里才能写驼峰 -->
        <!-- cpnClick是父组件(Vue实例)里面定义的方法-->
    </div>

    <!-- 这个是子组件的模版！！！ -->
    <template id="cpn">
        <div>
            <button v-for="item in categories" 
                    @click="btnClick(item)">{{item.name}}
                	<!--子组件的模版里调用它自己的btnClick方法，很合理-->
                	<!--一点击这个按钮，它就触发btnClick这个方法-->
                	<!--categoryies是子组件里面的数据，很合理-->
            </button>
        </div>
    </template>
    
    <script src="js/vue.js"></script>
    <script>
        // 1.子组件
        const cpn = {
            // 常见子组件发生了一些事情，希望父组件知道
            template: '#cpn',
            data() {
                return {
                    categories: [
                        { id: "01", name: "热门推荐" },
                        { id: "02", name: "手机数码" },
                        { id: "03", name: "家用电器" },
                        { id: "04", name: "服装鞋帽" },
                        //这个数据是保存在子组件里面的
                    ]
                }
            },
            methods: {
                btnClick(item) {
                //btnClick(item)这个方法是子组件里面的
         				//在这个组件内部你得需要我点击了谁
                //发生点击的时候最好把item一起传过来，因为这样我才能通过item拿到id
                //所以这里这个函数加了一个参数item
                    console.log(item);
                    // 我们在自己的组件里面知道点击了谁
                    // 但是是我们的组件里面根据点击了谁发送请求的吗？——不是
                    // 我们要把点击了哪个按钮告诉父组件，让父组件向服务器发送请求
                  	// 那么我们应该怎么传呢？——通过自定义事件的方式进行传递(子传父)
                    this.$emit('item-click', item)
                  	// 子组件任务：发射事件
                    // 第一个参数是要发射的事件的名称(item-click)
                  	// 第二个参数是要发射过去的一个参数(可以不写)
                    // 子组件负责发射事件：自定义事件
                  	// 自定义事件的名字(item-click)你是可以随便起的
                }
            },
        }
        // 2.父组件
        const app = new Vue({
            el: '#app',
            data: {
                message: '你好啊'
            },
            components: {
                cpn
              	//ES6属性增强写法，等价于cpn:cpn,即组件标签名和组件构造器名字都是cpn
            },
            methods: {
                cpnClick(item) {
                //cpnClick(item)是父组件的方法
                    //console.log("cpnClick");
                    console.log("cpnClick"，item);
                  	//再加一个参数item就可以知道点击的是哪个按钮了
                }
            },
        })
    </script>
</body>
</html>
~~~

> 其实我并没有看懂这段代码啊，所以学习知识一定要脚踏实地，基础打牢。
>
> 因为子组件进行传值其父组件应该有一个触发条件，
>
> 而去知道何时触发可以进行监听在这里你可以使用点击事件也可以是其他的事件。
>
> 子组件向父组件传递值如果需要父组件去进行显示那么这个显示条件或者说值得获取一定要有触发的，
>
> 而原理呢就是事件监听，也可以说是发布订阅模式。
>
> 父组件通过`v-on`监听子组件的事件，子组件通过`$emit`来触发自己的事件。
>
> 这个不能光看，回家后要去VSCode里敲一遍，好好想一下，想清楚了就不用再看视频了。
>
> 现在是2020年12月26日，我终于大概是懂了啊！！！！

![](Vue框架入门/298.png)

![](Vue框架入门/299.png)

![](Vue框架入门/300.png)

#### 父子组件通信案例(普通方式)

> 组件这里本来就看的晕晕乎乎的，看到这个案例，感觉彻底找不到北了，不行，我不能想做任务一样赶进度，现在需要自己慢下来，遇到不懂的概念不能跳过不管了，我打算再看一下其他的视频，做一个补充。组件这个知识点一定要好好的把它学懂，不能像2月份过年的时候那样，就像完成任务一样，视频就硬看，看完了10天的视频，到现在是一点印象也没有。这次一定要好好的，给自己时间消化这些知识点啊。
>
> 现在是2020年12月24日，我还是没有消化好，慢一点，再慢一点。
>
> 现在是2020年12月27日，我重新把这段代码敲了一遍，因为原来代码感觉逻辑有点复杂，所以我由简到繁写了几个版本，这样看起来更加的循序渐进一些。

**1.0版**

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <!-- 这里是Vue的模版 -->
    <div id="app">
        <!-- 有了组件里定义的两个属性number1,2 -->
        <!-- {{num1}} -->
        <!-- {{num2}} -->
        <!-- num1,num2也是在Vue里面的数据，所以可以在这里直接用 -->
        <cpn :number1="num1" :number2="num2"></cpn>
        <!-- 但是在Vue模版里使用组件的时候，组件里不能直接使用num1,2 -->
        <!-- 需要间接使用number1,2属性进行动态绑定 -->
    </div>

    <!-- 这里是组件的模版 -->
    <template id="cpn">
        <div>
            <!-- 组件模版里必须有个根，所以这里写个div -->
            <!-- 在Vue实例里面写好后，我们再在这里做一个展示，看有没有传过来 -->
            <h2>{{number1}}</h2>
            <h2>{{number2}}</h2>
            <!-- 注意：number1,number2是组件里面定义的属性!! -->
        </div>
    </template>
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                num1: 1,
                num2: 0
                // 这个是组件里面的数据
                // 现在需要将num1,num2传到组件里面
            },
            // 在Vue实例里面注册了一个组件
            components: {
                // 如果抽离的话可以cpn:cpnC
                // 其中cpn是标签名，cpnC是组件构造器名
                // 然后在外面写组件构造器cpnC里面的内容
                cpn: {
                    template: '#cpn',
                    // 如果想要往组件里面传值(父组件Vue实例里面的num1,num2)
                    // 并且在div里面进行展示
                    // 必须在组件内部定义props
                    props: {
                        number1: Number,
                        number2: Number
                        // 注意：number1,number2是组件里面定义的属性
                        // 名字是随便起的
                    }
                }
            }
        });
    </script>
</body>

</html>
~~~

**2.0版**

~~~javascript
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <cpn :number1="num1" :number2="num2"></cpn>
    </div>

    <template id="cpn">
        <div>
            <h2>{{number1}}</h2>
            <!-- 需求：在子组件里面想要做一件事：弄一个input -->
            <!-- input可以通过v-model做一个双向绑定 -->
            <!-- 想要通过input对number1做一个双向绑定 -->
            <!-- 希望input里面的数字发生变化的话，number1跟着变 -->
            <!-- 并且Vue实例里面的num1,2也一起跟着发生改变 -->
            <input type="text" v-model="number1">
            <!-- 刚开始这样写的，直接绑定number1 -->
            <h2>{{number2}}</h2>
            <input type="text" v-model="number2">
            <!-- 以前v-model绑定的都是Vue实例里面data数据 -->
            <!-- 现在这个v-model绑定的是组件里面通过props自定义的两个属性number1,2了 -->
            <!-- 虽然v-model直接绑定number1,2看上去没有问题，但其实控制台报错了 -->
        </div>
    </template>
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                num1: 1,
                num2: 0
            },
            components: {
                cpn: {
                    template: '#cpn',
                    props: {
                        number1: Number,
                        number2: Number
                    }
                }
            }
        });
    </script>
</body>

</html>
~~~

![](Vue框架入门/301.png)

**3.0版**

~~~javascript
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <cpn :number1="num1" :number2="num2"></cpn>
    </div>

    <template id="cpn">
        <div>
            <h2>props里面的：{{number1}}</h2>
            <h2>data里面的：{{dnumber1}}</h2>
            <input type="text" v-model="dnumber1">

            <h2>props里面的：{{number2}}</h2>
            <h2>data里面的：{{dnumber2}}</h2>
            <input type="text" v-model="dnumber2">
            <!-- v-model不绑定number1,2而是绑定dnumber1,2，这样更合理 -->
            <!-- 因为v-model绑定的是data里面的dnumber1,2，所以number1,2不会变化 -->
        </div>
    </template>
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                num1: 1,
                num2: 0
            },
            components: {
                cpn: {
                    template: '#cpn',
                    props: {
                        number1: Number,
                        number2: Number
                    },
                    data() {
                        // 这个是组件里面的data
                        return {
                            dnumber1: this.number1,
                            dnumber2: this.number2,
                            // 根据props里面的number1,2来初始化一下组件里面的dnumber1,2
                            // 等你初始化完成之后，上面的v-model就不绑定number1,2了
                            // 而是转而绑定dnumber1,2了
                            // 这样绑定才是一个合理的做法
                        }
                    }
                }
            }
        });
    </script>
</body>

</html>
~~~

![](Vue框架入门/302.png)

**4.0版**

~~~javascript
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <cpn :number1="num1" 
        	 :number2="num2" 
 			 @num1change="num1change" 
			 @num2change="num2change"></cpn>
        <!-- 等号左边的@num1change是黑中介的名字 -->
        <!-- 等号右边的"num1change"是父组件(Vue实例里的方法) -->
    </div>

    <template id="cpn">
        <div>
            <h2>props里面的：{{number1}}</h2>
            <h2>data里面的：{{dnumber1}}</h2>
            <!-- 但是这样写的话有点写死了，可以下面这样写 -->
            <!-- 相当于把v-model代码进行了分拆，最终效果还是一样的 -->
            <!-- <input type="text" v-model="dnumber1"> -->
            <input type="text" :value="dnumber1" @input="num1Input">
            <!-- 我们可以弄一个value，动态绑定dumber1 -->
            <!-- v-model的本质就是2个指令的结合体：v-bind:和@input事件 -->
            <!-- v-model只不过是一个语法糖而已 -->
            <!-- 不熟悉的可以看我上面讲v-model的博文 -->
            <!-- <input type="text" :value="dnumber1" 			                                            @input="dnumber1=$event.target.value"> -->
            <h2>props里面的：{{number2}}</h2>
            <h2>data里面的：{{dnumber2}}</h2>
            <!-- <input type="text" v-model="dnumber2"> -->
            <input type="text" :value="dnumber2" @input="num2Input">
            <!-- 我们希望dnumber1,2数字发生改变后，将改变后的数字再传给父组件 -->
            <!-- 将父组件的num1,num2也改变掉 -->
        </div>
    </template>
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                num1: 1,
                num2: 0
            },
            methods: {
                num1change(value) {
                    // 根据下面的this.$emit(传过来一个参数dnumber1,2)
                    // 所以这里有一个value参数来访问它
                    // 这里报错，估计是因为value的类型不对
                    // 这里value估计是字符串类型
                    console.log(typeof value);
                    // String类型，要把它转为数字类型
                    // 因为props里面的number1,2设置为Number类型的
                    // this.num1 = value
                    this.num1 = parseFloat(value)
                },
                num2change(value) {
                    this.num2 = parseFloat(value)
                }
            },
            components: {
                cpn: {
                    template: '#cpn',
                    props: {
                        number1: Number,
                        number2: Number
                    },
                    data() {
                        return {
                            dnumber1: this.number1,
                            dnumber2: this.number2,
                        }
                    },
                    methods: {
                        num1Input(event) {
                            this.dnumber1 = event.target.value;
                            // 在这个值发生改变的同时，发出一个事件,起个名字叫num1change
                            // 并且把dnumber1给它传出去
                            this.$emit('num1change', this.dnumber1)
                        },
                        num2Input(event) {
                            this.dnumber2 = event.target.value;
                            this.$emit('num2change', this.dnumber2)
                        },
                    },
                }
            }
        });
    </script>
</body>

</html>
~~~

![](Vue框架入门/303.png)

![](Vue框架入门/304.png)

**5.0版**

~~~javascript
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <cpn :number1="num1" 
        	 :number2="num2"
			 @num1change="num1change" 
			 @num2change="num2change"></cpn>
    </div>

    <template id="cpn">
        <div>
            <h2>props里面的：{{number1}}</h2>
            <h2>data里面的：{{dnumber1}}</h2>
            <input type="text" :value="dnumber1" @input="num1Input">

            <h2>props里面的：{{number2}}</h2>
            <h2>data里面的：{{dnumber2}}</h2>
            <input type="text" :value="dnumber2" @input="num2Input">
        </div>
    </template>
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                num1: 1,
                num2: 0
            },
            methods: {
                num1change(value) {
                    this.num1 = parseFloat(value)
                },
                num2change(value) {
                    this.num2 = parseFloat(value)
                }
            },
            components: {
                cpn: {
                    template: '#cpn',
                    props: {
                        number1: Number,
                        number2: Number
                    },
                    data() {
                        return {
                            dnumber1: this.number1,
                            dnumber2: this.number2,
                        }
                    },
                    methods: {
                        num1Input(event) {
                            // 1.将input中的value赋值到dnumber1中
                            this.dnumber1 = event.target.value;
                            // 2.为了让父组件可以修改子组件值，发出一个事件
                            this.$emit('num1change', this.dnumber1)
                            // 3.还同时修改number2的值
                            this.dnumber2 = this.dnumber1 * 100
                            // 这样写的话，虽然子组件里的number1改变了，但是props没有改
                            // 所以还需要接下来这样做
                            this.$emit('num2change', this.dnumber2)
                        },
                        num2Input(event) {
                            this.dnumber2 = event.target.value;
                            this.$emit('num2change', this.dnumber2)
                            this.dnumber1 = this.dnumber2 / 100
                            this.$emit('num1change', this.dnumber1)
                        },
                    },
                }
            }
        });
    </script>
</body>

</html>
~~~

![](Vue框架入门/305.png)

> 这个案例我已经看不懂了，先暂停接下来的视频，要花时间把组件的基础知识再温习一遍，再看看其他的视频做一个补充了啊。
>
> 这种需求在真实开发中比较少见，不会这样来传递的。
>
> 现在是2020年12月27日，我终于可以比较透彻的看得懂了，所以说学习是一个循环往复的过程，一个知识点当时没看懂没关系，过一段时间后再重新来学习一遍，温故而知新，慢慢的就会被自己掌握了。
>
> 对付难理解的知识点最有效的方法就是：不断的重复！！！
>
> 现在是2020年12月27日，截止到上面复习完。

#### 父子组件通信案例(watch方式)

> watch可以用于监听我们某个属性的改变。

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>

<body>

    <div id="app">
        <cpn :number1="num1" 
             :number2="num2" 
             @num1change="num1change" 
             @num2change="num2change" />
    </div>

    <template id="cpn">
        <div>
            <h2>props:{{number1}}</h2>
            <h2>data:{{dnumber1}}</h2>
            <input type="text" v-model="dnumber1">
          
            <h2>props:{{number2}}</h2>
            <h2>data:{{dnumber2}}</h2>
            <input type="text" v-model="dnumber2">
        </div>
    </template>

    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                num1: 1,
                num2: 0
            },
            methods: {
                num1change(value) {
                    this.num1 = parseFloat(value)
                },
                num2change(value) {
                    this.num2 = parseFloat(value)
                }
            },
            components: {
                cpn: {
                    template: '#cpn',
                    props: {
                        number1: Number,
                        number2: Number,
                    },
                    data() {
                        return {
                            dnumber1: this.number1,
                            dnumber2: this.number2
                        }
                    },
                    watch: {
                        dnumber1(newValue) {
                            this.dnumber2 = newValue * 100;
                            this.$emit('num1change', newValue);
                        },
                        dnumber2(newValue) {
                            this.number1 = newValue / 100;
                            this.$emit('num2change', newValue);
                        },
                      name(newValue,oldValue){
                        
                      }
                    }
                }
            }
        })
    </script>

</body>
</html>
~~~

##### 父子组件通信案例文字及画图分析

1.首先，我们有个Vue实例，Vue实例里面有一个data,data里面有2个数字，一个是num1,数值是1,一个是num2,数值是0。

2.然后我们有一个子组件，现在我们希望把Vue实例data中的num1,num2传递给子组件。要传递给子组件，必须在子组件里定义一个东西：props。只有定义了props才能传过来。

3.props里面有2个属性，number1和number2,它们的类型都是Number。

4.这样num1就可以通过number1属性传到子组件，同样num2就可以通过number2属性传到子组件里来。

5.在子组件里面，我们又搞了2个input在里面，我们希望把这2个input和这2个number属性进行双向绑定。

6.但是浏览器不推荐这样的绑定，会报错。

7.它推荐搞一个data,根据上面的number的值给dnumber初始化。

8.现在只要让input和dnumber进行绑定就可以了。

9.input是一个输入框，用户可以在里面输入很多东西。因为是双向绑定，所以input里面的内容变化，dnumber里面的内容也会随之改变。

10.但是dnumber里面的内容发生了改变，上面的number是不会变化的。因为下面的dnumber是根据上面的number进行初始化的，而上面的number不是根据下面的dnumber进行初始化的，它是根据父组件传过来的数据进行初始化的。

11.而我希望把下面的dnumber的值改变的时候，希望把num的值也改了。

12.dnumber的值随便改，num是不知道的，所以我们要监听下面的dnumber的值的改变。

13.一旦用户在input里面输入东西的时候，它就会调用一个`@input`方法，给`@input`方法绑定一个事件`numchange。`

14.此时我们要在组件里通过定义methods方法来处理这个函数。

![](Vue框架入门/95.png)

> 我靠，这图画的我吐了。现在水平不够，这么多线条，思绪理不清啊。
>
> 现在是2020年12月13日，这图依旧还是不懂，看的依旧想吐。 
>
> 现在是2020年12月27日，我又看了一遍视频，敲了一遍代码，终于懂了，呵呵。

#### 父子组件的访问

> 某些情况下，我们可能希望在父组件里面能拿到子组件的对象，拿到子组件对象后，直接操作子组件里的一些东西(比如子组件里面有某个方法，我想直接调用一下这个方法)。这个要求就不是父子组件二者之间相互传东西了。
>
> 子组件本身就是一个对象。

##### 父=>子组件的访问方式： $children

![](Vue框架入门/96.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <cpn></cpn>
        <!-- 注意这里如果使用单标签它就无法显示下面的按钮了，不知道为什么 -->
        <button @click="btnClick">按钮</button>
        <!-- 当你点击Vue实例(父组件)的这个按钮时，要求访问子组件里面的一些东西 -->
        <!-- 注意：这个按钮是Vue实例里面的！！点击它却可以访问到子组件里面的方法！！ -->
    </div>

    <template id="cpn">
        <div>我是子组件</div>
    </template>

    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                message: '你好啊'
            },
            methods: {
                btnClick() {
                    console.log(this.$children);
                    // 会显示[VueComponent],是一个数组类型
                    // 这个VueComponent里面也有一个$children的属性，只不过是一个空的数组
                    // 因为cpn子组件里面已经没有子组件了
                    // 这个VueComponent里面也有一个showMessage函数的
                    this.$children[0].showMessage()
                    //通过this.$children[0]拿到这个子组件，然后调用它里面的showMessage方法
                }
            },
            components: {
                cpn: {
                    template: '#cpn',
                    methods: {
                        showMessage() {
                            console.log('我是子组件里面的showMessage');
                        }
                    },
                }
            }
        }); 
    </script>
</body>

</html>
~~~

##### 父=>子组件的访问方式： $refs

![](Vue框架入门/97.png)

> refs是reference(引用)的缩写，表明父组件引用子组件。

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <cpn ref="bbb"></cpn>
        <!-- <my-cpn></my-cpn> -->
        <!-- 中间不管你怎么加其他的组件，refs不会因为位置错乱而产生错误 -->
        <cpn></cpn>
        <cpn ref="aaa"></cpn>
        <!-- 通过ref属性和下面的$refs进行对应上，aaa就相当于key了 -->
        <button @click="btnClick">按钮</button>
        <!-- 弄一个按钮，点击按钮的时候，就把子组件对象打印一下 -->
    </div>

    <template id="cpn">
        <div>我是子组件</div>
    </template>

    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                message: '你好啊'
            },
            methods: {
                btnClick() {
                    // 方法1：通过$children(数组类型)获取子组件信息(用的少，10%)
                    // 只有当我们希望拿到所有的子组件时才会用它
                    // 我们希望在Vue实例里访问刚才的子组件
                    console.log(this.$children);
                    console.log(this.$children[0]);
                    
                    // $children是一个数组，数组里只有一项，VueComponent
                    console.log(this.$children[0].name);
                    this.$children[0].showMessage();

                    for (let c of this.$children) {
                        console.log(c.name);
                        c.showMessage();
                    }
                    // 但是在真实开发中我们一般不会用$children
                    // 因为我们组件之间的位置可能会变化，变化了结果就不一样了

                    // console.log(this.$children[2].name);
                    // 用下标值来拿东西不好，不稳定

                    // 方法2：通过$refs(对象类型)获取子组件信息(用的多，90%！)
                    console.log(this.$refs);
                  	// 默认是一个空的对象
                  	// 你必须要在组件上面加属性，比如叫aaa
                  	// aaa是一个名字，会作为这个对象的一个key
                    console.log(this.$refs.aaa);
                    console.log(this.$refs.aaa.name);
                    // 必须要在组件标签上面给它加上属性
                }
            },
            components: {
                cpn: {
                    template: '#cpn',
                    data() {
                        return {
                            name: '我是子组件的name'
                        }
                    },
                    methods: {
                        showMessage() {
                            // 子组件里面有个简单的函数叫showMessage
                            console.log('这是一个子组件');
                        }
                    },
                }
            }
        })
    </script>
</body>
</html>
~~~

##### 子=>父组件的访问方式\$parent和$root

> 用的更少，实际开发中也不建议这样使用

![](Vue框架入门/98.png)

**案例：**

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <cpn></cpn>
    </div>

    <template id="cpn">
        <div>
            <h2>我是子组件</h2>
            <button @click="btnClick">按钮</button>
            <!-- 这个按钮是在子组件里面的 -->
            <!-- 在子组件里点击之后看如何访问父组件 -->
        </div>
    </template>

    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                message: '你好啊'
            },
            components: {
                cpn: {
                    template: '#cpn',
                    methods: {
                        btnClick() {
                            // 访问父组件(亲爸爸，不是爷爷)$parent
                            console.log(this.$parent);
                            // 打印出来的就是一个Vue实例
                        }
                    }
                }
            }
        })
    </script>
</body>
</html>
~~~

**案例升级版：**

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <cpn></cpn>
    </div>

    <template id="cpn">
        <div>
            <h2>我是cpn组件</h2>
            <ccpn></ccpn>
        </div>
    </template>

    <template id="ccpn">
        <div>
            <h2>我是子子组件</h2>
            <button @click="btnClick">按钮</button>
            <!-- 这个按钮是在子子组件里面的 -->
            <!-- 在子组件里点击之后看如何访问父组件 -->
        </div>
    </template>
    
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                message: '你好啊'
            },
            components: {
                cpn: {
                    template: '#cpn',
                    data() {
                        return {
                            name: "我是cpn组件的name"
                        }
                    },
                    components: {
                        // 真实开发中不会这样组件套组件的
                        // 因为这样写的话，子组件就不够独立了(没有复用性了)
                        ccpn: {
                            template: '#ccpn',
                            methods: {
                                btnClick() {
                                    // 1.访问父组件(亲爸爸，不是爷爷)$parent
                                    console.log(this.$parent);
                                    // 打印出来的就是一个VueComponent
                                    console.log(this.$parent.name);

                                    // 2.访问根组件$root
                                    console.log(this.$root);
                                    //打印出来的就是一个Vue实例
                                    console.log(this.$root.message);
                                    // 这个也很少用，因为真实开发中Vue实例里面一般什么东西也没有
                                    // 非常简单，里面就一些非常重要的东西
                                }
                            }
                        }
                    }
                }
            }
        })
    </script>
</body>
</html>
~~~

#### 非父子组件通信

![](Vue框架入门/99.png)

## 组件化高级

### 插槽slot

#### 编译作用域

> 必须要先把编译作用域这个概念理解完才能理解后面要学的作用域插槽。

![](Vue框架入门/105.png)

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <cpn v-show="isShow"></cpn>
        <!-- 它会使用实例里面的isShow,而不是组件里面的isShow -->
        <!-- 意味着模版里的东西会显示出来(实例里的isShow是true) -->
        <!-- 它不关心你用的是哪个组件，它把cpn当成是普通的div看待了 -->
        <!-- 虽然里面出现了cpn标签，但是整体上里面的内容是在Vue模版里写的 -->
        <!-- 它看你在哪个模版里，我们当前的模版属于Vue实例的模版，所以就在Vue实例里找 -->
        <!-- 所以里面出现的变量都会在Vue实例里找，不会在组件里找的 -->
    </div>

    <template id="cpn">
        <div>
            <h2>我是子组件</h2>
            <p>我是内容，哈哈哈</p>
            <button v-show="isShow">按钮</button>
            <!-- 这个按钮无法显示，因为组件里面的isShow是false -->
            <!-- 模版里的东西会在自己的作用域(组件)里查找变量的 -->
            <!-- 我的这个template是属于我的组件的，所以在template里出现的任何变量都会在组件里找的-->
        </div>
    </template>
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                message: '你好啊',
                isShow: true
            },
            components: {
                cpn: {
                    template: '#cpn',
                    data() {
                        return {
                            isShow: false
                        }
                    }
                }
            }
        })
    </script>
</body>
</html>
~~~

#### 为什么使用slot

> 插槽是为了让组件有更强的扩展性，以前我们写的组件是没有扩展性的。

![](Vue框架入门/100.png)

![](Vue框架入门/101.png)

> 你想让这3个页面共用一个导航栏组件，又不想让这3个导航栏长的一样，那么这个组件你就可以分成3个部分，这3个部分都写成插槽就可以了。

![](Vue框架入门/102.png)

#### slot的基本使用

![](Vue框架入门/103.png)

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <!-- 
        1.插槽的基本使用：在组件里定义一个slot标签 <slot></slot>
        2.插槽的默认值：<slot>button</slot>
        3.如果有多个值，同时放到组件中进行替换时，会一起作为替换元素(替换掉默认的button)
    -->
    <div id="app">
        <cpn></cpn>
        <!-- 这样写的话，就会把这个按钮替换到插槽slot这个位置上面去了 -->
        <cpn><span>哈哈哈</span></cpn>
        <cpn></cpn>
        <cpn></cpn>
        <!-- 如果有某一类东西显示的次数非常多(大部分都显示按钮)，只有一些是特殊的， -->
        <!-- 如果我们这样写反而显得有些啰嗦了 -->
        <!-- 解决方法：在插槽里面给它一个默认值(比如默认是button) -->
        <cpn>
            <i>呵呵呵</i>
            <div>我是div元素</div>
            <p>我是p元素</p>
            <!-- 这3个会全部显示出来 -->
        </cpn>
        <cpn></cpn>
        <!-- 这里封装的组件是没有扩展性的-->
        <!-- 比如第一个组件下面我想显示一个button,第二个组件下面我想显示span标签
             第三个组件下面我想显示一个i标签等等等 -->
        <!-- 在模板下面给组件定义一个插槽就可以了 -->
    </div>

    <template id="cpn">
        <div>
            <h2>我是组件</h2>
            <p>我是组件，哈哈哈</p>
            <!-- <button>按钮</button> -->
            <!-- 如果我直接把按钮加到这个组件模版里面，那所有组件下面都有一个按钮 -->
            <slot></slot>
            <!-- 插槽就相当于给组件预留了一个空间，就像电脑上预留的USB插孔一样 -->
            <!-- 你想让我这里显示什么，你可以自主决定 -->
            <!-- 在真实开发过程中封装的组件，你都要给它预备插槽 -->
            <slot><button>按钮</button></slot>
            <!-- 这个插槽有默认值，如果你没有指定的话，就默认值button了 -->
        </div>
    </template>
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                message: '你好啊'
            },
            components: {
                cpn: {
                    template: '#cpn'
                }
            }
        })
    </script>
</body>
</html>
~~~

#### slot的具名插槽

![](Vue框架入门/104.png)

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <cpn><span>标题1</span></cpn>
        <!-- 组件模版有3个插槽，你只写了一个组件，它会把默认的插槽都替换为标题 -->
        <!-- 但是现在我只想你给我改一个，另外的不要给我改 -->
        <!-- 这个时候你可以给插槽起个名字就可以了 -->

        <!-- 要想替换有名字的插槽，必须在使用的时候给它写上名字 -->
        <cpn><span slot="center">标题2</span></cpn>
        <cpn><button slot="right">返回</button></cpn>
    </div>

    <template id="cpn">
        <div>
            <slot name="left"><span>左边</span></slot>
            <slot name="center"><span>中间</span></slot>
            <slot name="right"><span>右边</span></slot>
            <slot>哈哈哈</slot>
            <!-- 别的插槽有名字，你这个插槽没有名字，它只会替换没有名字的插槽 -->
        </div>
    </template>
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                message: '你好啊'
            },
            components: {
                cpn: {
                    template: '#cpn'
                }
            }
        })
    </script>
</body>
</html>
~~~

#### slot作用域插槽

[vue作用域插槽，你真的懂了吗？](https://juejin.im/post/6844903812130422792)

[深入理解vue中的slot与slot-scope](https://blog.csdn.net/weixin_33882443/article/details/88894364?utm_medium=distribute.pc_relevant_t0.none-task-blog-BlogCommendFromBaidu-1.control&depth_1-utm_source=distribute.pc_relevant_t0.none-task-blog-BlogCommendFromBaidu-1.control)

![](Vue框架入门/106.png)

![](Vue框架入门/107.png)

> 父组件替换插槽中间的标签，但是内容仍由子组件提供。

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <cpn></cpn>
        <cpn>
            <span>Java-</span>
            <span>JavaScript-</span>
            <span>C-</span>
            <span>C++-</span>
            <span>Go-</span>
            <span>Python</span>
        </cpn>
        <!-- 第二次展示的时候我希望能用横杠进行分割来展示 -->
        <!-- 但是我们总不能手写吧！！ -->
        <!-- 父组件替换插槽中间的标签，但是内容仍由子组件提供。 -->

        <!-- <cpn v-for="item in pLanguages"></cpn> -->
        <!-- 这样写也是不行的，因为在Vue实例里找不到pLanguages这个变量！！ -->
        <!-- 可以看前面学的编译作用域就知道了 -->
        <!-- 我们父组件想要展示子组件的数据，但是父组件里拿不到子组件的数据(编译作用域) -->
        <cpn>
            <!-- 我们的目的是获取子组件中的变量:pLanguages -->
            <!-- Vue2.5.x以下必须要用template模版 -->
            <template slot-scope="slot">
                <!-- <span v-for="item in slot.data">{{item}} -</span> -->
                <!-- 但是这样写最后还会有一个横杠，强迫症表示不行 -->
                <span>{{slot.data.join(' - ')}}</span>
            </template>

            <template slot-scope="slot">
                <!-- <span v-for="item in slot.data">{{item}} * </span> -->
                <!-- 但是这样写最后还会有一个乘号，强迫症表示不行 -->
                <span>{{slot.data.join(' * ')}}</span>
            </template>
        </cpn>
    </div>
    <template id="cpn">
        <div>
            <slot :data="pLanguages">
                <!-- slot这样写 -->
                <ul>
                    <li v-for="item in pLanguages">{{item}}</li>
                    <!-- 有些人希望这样展示，有些人不希望，所以我们要弄一个插槽 -->
                    <!-- 当别人没有写的时候，就默认ul li这样展示 -->
                </ul>
            </slot>
        </div>
    </template>
    <script src="js/vue.js"></script>
    <script>
        const app = new Vue({
            el: '#app',
            data: {
                message: '你好啊'
            },
            components: {
                cpn: {
                    template: '#cpn',
                    data() {
                        return {
                            pLanguages: ['Java', 'JavaScript', 'C', 'C++', 'Go', 'Pytho']
                        }
                    }
                }
            }
        })
    </script>
</body>
</html>
~~~

> 现在是2020年12月28日，截止到上面复习完。
>
> 以上的内容终于又复习一遍了，终于基本上都理解了。作用域插槽没有看视频了，还不算透彻理解，到时候再说了。

# 模块化开发

> 模块化开发有2个核心，一个叫做导出，一个叫做导入。先导出，再导入。

[前端模块化详解(完整版)](https://juejin.im/post/6844903744518389768)

[前端开发的模块化和组件化的定义，以及两者的关系？](https://www.zhihu.com/question/37649318) 

[前端模块化和组件化理解](https://segmentfault.com/a/1190000015437724)

[JavaScript modules 模块](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Guide/Modules)

> 如果你不接触服务器端的`Node.js`,一般是接触不到模块化的，因为早期前端是没有模块化这个概念的。而现在前端已经发展到了三大框架这个阶段了，而三大框架在开发的时候基本上都用到了模块化的思想。现在公司里开发也是用模块化思想来开发的。

![](Vue框架入门/110.png)

## 为什么使用模块化

### JavaScript原始功能

> 以前JavaScript设计出来就是用来做一些简单的数据验证的，没想到现在发展的这么复杂。

![](Vue框架入门/108.png)

### 匿名函数的解决方案

![](Vue框架入门/109.png)

### 使用模块作为出口

![](Vue框架入门/111.png)

### 演示案例

**index.html**

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <!-- 
        1.项目组长
        2.小明
        3.小红
     -->
    <script src="main.js"></script>
    <script src="aaa.js"></script>
    <script src="bbb.js"></script>
    <script src="xiaoming.js"></script>
    <script src="xiaohong.js"></script>
    <!-- 项目组长先弄一些公共的东西:main.js -->
    <!-- 小明写了aaa.js和xiaoming.js -->
    <!-- 小红写了bbb.js和xiaohong.js -->
    <!-- JS文件的引用顺序也会导致代码跑起来有没有问题 -->
</body>

</html>
~~~

**aaa.js**

~~~javascript
// 小明创建aaa.js

// 方法1：直接写
// var name = "小明";
// var age = 22;

// function sum(num1, num2) {
//   return num1 + num2;
// }

// var flag = true;

// if (flag) {
//   console.log(sum(10, 20));
// }

// 方法2：在匿名函数里写，解决全局变量名冲突的问题
var moduleA = (function () {
  // 在这里做了一个接收
  // 因为这个函数是立即执行，你一执行这个函数就返回obj
  // 那么这个obj就等于moduleA了
  // 则在全局里面就有moduleA这个东西，里面就保存着小明想要导出的一些东西了
  // moduleA是在全局的！！！！！！！！

  // 早期大家都是这样实现模块化的，但是随着前端越来越复杂，已经不这样实现了
  // 我们以后会采用别人已经实现好的模块化规范来写代码

  // 使用模块化思想：导出的对象
  var obj = {};
  // 先给它弄一个空的对象
  // 使用的是ES5的语法，ES5里面没有模块化，而ES6则自带模块化，不这么写了

  var name = "小明";
  var age = 22;

  function sum(num1, num2) {
    return num1 + num2;
  }

  var flag = true;

  if (flag) {
    console.log(sum(10, 20));
  }

  obj.flag = flag;
  // 上面弄一个空的对象，下面给这个空的对象加一个flag属性，把之前定义的flag变量赋值给它
  obj.sum = sum;
  // 把sum函数也给它
  // console.log(obj);
  return obj;
  // 我们把这个obj给return出去(但是没有人接收它)
})();
~~~

**bbb.js**

~~~javascript
// 小红创建bbb.js

// 方法1：直接写
// var name = "小红";
// var flag = false;
// // 全局变量同名问题可以用匿名函数(闭包)的方式进行解决，但是这也会导致一些问题。
// console.log(name);

// 方法2：在匿名函数里写，解决全局变量名冲突的问题
var moduleB = (function () {
  // 如果小红也有东西想导出，也可以这样做：先定义一个空对象，再返回它
  var obj = {};
  var name = "小红";
  var flag = false;
  // 全局变量同名问题可以用匿名函数(闭包)的方式进行解决，但是这也会导致一些问题。
  console.log(name);
  obj.flg = flag;
  return obj;
})();
~~~

**xiaoming.js**

~~~javascript
// 小明创建的另一个js文件
// 小明知道自己之前定义过flag变量，并且知道这个变量为true

// if (flag) {
//   console.log("小明是天才，哈哈哈");
//   // 因为aaa.js使用了匿名函数，所以无法在这里直接使用flag变量了，代码无法复用
// }

// 如果aaa使用了匿名函数，那么虽然解决了aaa.js和bbb.js变量重名的问题，但也带来了新的问题：
// 我想用aaa.js里面的变量flag是用不了的

// 比如这里想用aaa.js里面的sum函数，用不了，只能自己在这里再定义一个

// 在xiaoming.js里面也弄一个闭包吧
(function () {
  // 要求1：想使用aaa.js里的flag变量
  // 写法1：不行
  // if (flag) {
  // 这样写不行
  //     console.log("小明是天才，哈哈哈");
  //   }

  // 写法2：行
  if (moduleA.flag) {
    console.log("小明是天才，哈哈哈");
    //   这样写可以！！！
  }

  // 要求2：想使用aaa.js里的sum函数
})();
~~~

**xiaohong.js**

~~~javascript
(function () {
  if (!moduleB.flag) {
    console.log("小红也是天才，嘻嘻嘻");
  }
})();

~~~

**main.js**

(无)

## CommonJS(了解)

[CommonJS 详细介绍](https://neveryu.github.io/2017/03/07/commonjs/)

> 模块化里面**一个js文件**就可以把它看成是一个模块，没有命名冲突的问题。

![](Vue框架入门/112.png)

### 演示案例

**aaa.js**

~~~javascript
// 小明创建aaa.js
// 在module里面可以这样写
var name = "小明";
var age = 22;

function sum(num1, num2) {
  return num1 + num2;
}

var flag = true;

if (flag) {
  console.log(sum(10, 20));
}

module.exports = {
  // 导出在Common.js里面用exports关键字
  // 这样写不行，因为这个代码里没有人帮你解析这个结构
  // 现在这个结构没有意义，肯定要有底层支撑
  // 不然module这个关键字系统都不认识
  // 我们后面会讲Webpack,Webpack要想正常的运行，是依赖于Node环境的，而Node环境底层里有module
  // 1.先导出
  // 导出的是一个对象！！
  flag: flag,
  // // 导出一个属性叫flag,它对应的值是flag
  sum: sum,

  //对象属性的增强写法如下：更简洁
  // flag,
  // sum,
};
~~~

**xiaoming.js**

~~~javascript
// 小明创建的另一个js文件

// 导入在Common.js里面用require关键字;
// 写法1：对象的解构写法
var { flag, sum } = require("./aaa.js");

// 写法2：分开写更加好懂
// 上面的写法等价于：
// var module = require("./aaa.js");
// var flag = module.flag;
// var sum = module.sum;

// 然后就可以直接使用了

// sum(20, 30);
~~~

> 注意：这里只是演示如何导入导出，无法运行的，因为这里没有module的底层实现。
>
> 这个不是我们的重点，我们的重点是ES6的模块化。
>
> ES6的模块化中新增了2个关键字：`export(导出)`和`import(导入)`

## ES6的export指令

一旦把它当成一个模块，你就把它想像成一个个独立的房间，彼此之间无法共享信息。

别人想要访问我里面的某个信息，我首先要把这个信息进行导出，然后别人再把这个信息进行导入，这样它才能访问到我里面的某个信息。

### export基本使用

模块作用域：相当于在自己独立的空间里面，你可以随便命名，不会和别人的命名冲突。

虽然不会和别人命名冲突，但是带来另外一个问题是，**别人也不能访问**(闭关锁国)。

要向让别人访问，你需要通过**导出的方式(开个小孔)**让别人导入才能访问到。

![](Vue框架入门/113.png)

### 导出函数或类

> 除了导出变量以外，开发中还可以导出函数或者导出类。

![](Vue框架入门/114.png)

### export default

![](Vue框架入门/115.png)

## ES6的import指令

> 注意：必须先有export，后有import。
>
> 2个国家直接都是闭关锁国，中间有一堵厚厚的墙，谁都访问不到对方。
>
> 如果一个国家愿意被访问，它就可以先export，里面装有愿意被访问的东西。
>
> 此时另一个国家才能import，拿到export里面的东西，注意那个愿意被访问的国家其他没有export出来的东西，你是照样不可以访问到的。它有选择哪些东西可以被你访问，哪些你不可以访问的权利。
>
> 这就叫做和平共处，这就是没有强迫，其乐融融。

### import使用

![](Vue框架入门/116.png)

### 演示案例

**index.html**

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <script src="aaa.js" type="module"></script>
    <script src="bbb.js" type="module"></script>
    <script src="xiaoming.js" type="module"></script>
    <!-- 加上type="module"就不会有命名冲突的问题了 -->
    <!-- 表示我使用这2个文件的时候，是按照模块化的思想来使用的 -->
</body>
</html>
~~~

**aaa.js**

~~~javascript
// 小明开发aaa.js
let name = "小明";
let age = 18;
let flag = true;

function sum(num1, num2) {
  return num1 + num2;
}

if (flag) {
  console.log(sum(20, 30));
}

// 别的地方(xiaoming.js想要用我的flag和sum，就需要把这2个进行导出给别人用)

// 初始写法写法：但是这种写法写了会报错，不知道为什么不支持了
// export {
//     flag: flag,
//     sum:sum
// }

// 1.导出方式1：简写(对象的增强写法)
export { flag, sum };

// 2.导出方式2：直接导出 (先把变量定义好，然后直接导出)
export let num1 = 1000;
export let height = 1.88;

// 3.导出函数/类
export function mul(num1, num2) {
  return num1 * num2;
}

export class Person {
  run() {
    console.log("在奔跑");
  }
}

// 4.export default
// const address = "北京市";

// 我们现在有很多种导出方式了
// 方法1
// export { address };

// 方法2
// export const address = "北京市";

// 但是方法1,2导出时必须要给它起个名字，但是我们有时候不想给它起名字

// 方法3
// 这样导出address也不需要写大括号了
// export default address;

export default function (argument) {
  console.log(argument);
}
~~~

**bbb.js**

~~~javascript
// 小红开发bbb.js
import { sum } from "./aaa.js";

let name = "小红";
let flag = false;
// 这个时候还是会有命名冲突的问题
// 那怎么让它们没有命名冲突的问题呢？——script标签上加上type="module"即可
// 这样就意味着我们是按照模块化的思想来使用这2个文件的
// 则这2个文件就是2个单独的模块，单独的模块有自己单独的作用域，就不会有命名冲突的问题了

console.log(sum(100, 200));
~~~

**xiaoming.js**

~~~javascript
// 1.导入的是对象中{}定义的变量
import { flag, sum } from "./aaa.js";
// 像这些别人导出叫什么名字，我导入必须也叫相同的名字，不够灵活
// 可以用export default让导入者自己起名字

// 先在aaa.js中实施导出
// 再在xiaoming.js里实施导入
// aaa.js的后缀.js可以省略不写(但是这里省略会报错，以后开发可以省略)

if (flag) {
  console.log("小明是天才，哈哈哈");
  console.log(sum(3, 5));
}

// 2.直接导入export定义的变量
import { num1, height } from "./aaa.js";
console.log(num1);
console.log(height);

// 3.导入export的function,类
import { mul, Person } from "./aaa.js";
console.log(mul(5, 7));

const p = new Person();
p.run();

// 4.导入export default中的内容
import addr from "./aaa.js";
console.log(addr);
addr("你好啊");
// 使用export default这种方式导出，导入的话我可以自己命名
// 但是在开发中 export default这种方式只能有一个
// 不能弄多个export default,默认的只能有一个，不然分不清是哪个

// 5.统一全部导入
// 只要script标签中有type="module"的话就全部进行导入
// import { flag, num, num1, height, Person, mul, sum } from "../aaa.js";
// 这样写太长了，而且找导入的变量也不好找
// 而且导入的变量和我命名的变量有可能会冲突
import * as quanbu from "./aaa.js";
//as quanbu 表示所有导入的变量打个包，统一叫quanbu
console.log(quanbu.flag);
console.log(quanbu.height);
// 通过点的方式来拿里面的变量
~~~

> 现在是2020年12月28日，截止到上面复习完。

# Webpack详解

Webpack就是一个前端**模块化**打包工具，之后你可以向面试官解释一下模块化的概念，再向面试官解释一下打包的概念。

> 注：国内npm太慢，最好通过`npm install cnpm -g --registry=https://registry.npm.taobao.org`
>
> 来下载一个国内的淘宝镜像，以后使用cnpm来执行命令。

[npm 和 cnpm 的区别，你真的搞懂了嘛](https://www.cnblogs.com/chase-star/p/10455703.html)

[webpack-安装踩坑](https://segmentfault.com/a/1190000014159004)

[如何评价 Webpack 4.0？](https://www.zhihu.com/question/267767207)

## 内容概述

![](Vue框架入门/117.png)

## 认识Webpack

### 什么是Webpack？

> 你用ES6写的代码，要转成ES5；你用Sass,Less写的代码，要转成CSS；你用TypeScript写的代码，要转成JavaScript。 我们不能直接给它放到服务器，总要经过一些工具，进行一下打包和转化，生成浏览器可以识别并且执行的代码。

![](Vue框架入门/118.png)

### 前端模块化

![](Vue框架入门/119.png)

### 和grunt/gulp的对比

![](Vue框架入门/120.png)

## webpack安装

> Webpack这个东西本身要想让它正常的工作，本身它也依赖一个环境：Node环境。
>
> Node环境为了可以正常的执行很多代码，其中必须包含各种依赖的包。而这些包如果手动管理，太麻烦了，所以安装Node时也会同时给你安装一个Node包管理工具：npm。

![](Vue框架入门/121.png)

> Node版本不能太低，以后还要用脚手架，对Node版本要求大于V8.9。

![](Vue框架入门/122.png)

## Webpack起步

### 准备工作

[js模块化编程三：main.js的介绍](https://blog.csdn.net/fengchao2016/article/details/54381333)

> 开发的项目这个大的文件夹里面一般会包含另外2个文件夹，一个是**src(源码)文件夹**，另一个是**dist文件夹**(dist全拼是distribution,发布的意思，等我开发完源码后将它打包，打包之后的东西就放到dist文件夹里面，之后把dist文件夹发送给服务器就可以了)。
>
> 我们开发的话都是在src文件夹里面开发的。
>
> src里面基本是都会有一个**main.js**(或index.js),作为应用程序的准备工作。(就像C语言有个main函数，作为C语言的入口一样)
>
> (main.js作为入口，不要往js文件夹里面放！！！)
>
> 有main.js还不行，还要有一个index.html,在里面通过src来引入main.js。(index.html最终也要放到dist文件夹里面，我们会通过工具来完成这个过程)
>
> 在src里面所有的JS代码,都可以按照模块化的方式(AMD,CMD,CommonJS,ES6的module都行)去写，不会发生命名冲突的问题。

![](Vue框架入门/123.png)

> 尽量早点在终端输入:`npm init`生成`package.json`文件，反正迟早要用到。

### js文件的打包

![](Vue框架入门/126.png)

### 使用打包后的文件

![](Vue框架入门/127.png)

### 演示案例

![](Vue框架入门/125.png)

**index.html**

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <!-- <script src="./src/mathUtils.js"></script> -->
    <!-- <script src="./src/main.js"></script> -->
    <!-- 我们按照模块化的思想去开发，不用这样来写的 -->

    <!-- 代码写好后我们要测试，但是不能直接打开index.html来测试 -->
    <!-- 因为里面什么也没有，因为我们是没有通过scr的方式来引用main.js和mathUtils.js文件的 -->
    <!-- 这2个js文件使用了模块化思想，没有采用src的方式来引用 -->
    <!-- 况且这2个js文件包含了CommonJS代码，而浏览器根本不认识CommonJS代码的 -->
    <!-- 解决方法：可以利用我们之前安装的Webpack进行打包 -->
    <!-- 你只要打包出一个浏览器能够认识的文件，然后让index.html引用那个打包的文件(浏览器认识)就可以了 -->

    <!-- 在这里我们引用打包好的bundle.js(浏览器认识)，可以进行代码测试了-->
    <script src="./dist/bundle.js"></script>
    <!-- 我们的开发模式：在src里面开发，想用什么模块化开发，就用什么模块化开发，
         开发完后用webpack打包一下，打包完后我们再引用打包后的文件，
         就可以进行测试，发送给服务器等一系列操作了 -->
</body>
</html>
~~~

**main.js**

~~~javascript
// 使用模块化思想
// 方法1：使用CommonJS导入mathUtils.js
const { add, mul } = require("./mathUtils.js");

console.log(add(20, 30));
console.log(mul(20, 30));

// 方法2：使用ES6导入info.js
import { name, age, height } from "./info.js";
// 这里可以不加js后缀，webpack文件会帮你找的
console.log(name);
console.log(age);
console.log(height);
~~~

**mathUtils.js**

~~~javascript
function add(num1, num2) {
  return num1 + num2;
}

function mul(num1, num2) {
  return num1 * num2;
}

// 使用模块化思想
// 方法1：使用CommonJS导出
module.exports = {
  add,
  mul,
};
~~~

**info.js**

~~~javascript
// 这个文件里面定义了很多的信息
// 使用模块化思想
// 方法2：使用ES6模块化导出
export const name = "why";
export const age = 18;
export const height = 1.88;
~~~

**自动生成的bundle.js**

~~~javascript
/******/ (function(modules) { // webpackBootstrap
/******/ 	// The module cache
/******/ 	var installedModules = {};
/******/
/******/ 	// The require function
/******/ 	function __webpack_require__(moduleId) {
/******/
/******/ 		// Check if module is in cache
/******/ 		if(installedModules[moduleId]) {
/******/ 			return installedModules[moduleId].exports;
/******/ 		}
/******/ 		// Create a new module (and put it into the cache)
/******/ 		var module = installedModules[moduleId] = {
/******/ 			i: moduleId,
/******/ 			l: false,
/******/ 			exports: {}
/******/ 		};
/******/
/******/ 		// Execute the module function
/******/ 		modules[moduleId].call(module.exports, module, module.exports, __webpack_require__);
/******/
/******/ 		// Flag the module as loaded
/******/ 		module.l = true;
/******/
/******/ 		// Return the exports of the module
/******/ 		return module.exports;
/******/ 	}
/******/
/******/
/******/ 	// expose the modules object (__webpack_modules__)
/******/ 	__webpack_require__.m = modules;
/******/
/******/ 	// expose the module cache
/******/ 	__webpack_require__.c = installedModules;
/******/
/******/ 	// define getter function for harmony exports
/******/ 	__webpack_require__.d = function(exports, name, getter) {
/******/ 		if(!__webpack_require__.o(exports, name)) {
/******/ 			Object.defineProperty(exports, name, {
/******/ 				configurable: false,
/******/ 				enumerable: true,
/******/ 				get: getter
/******/ 			});
/******/ 		}
/******/ 	};
/******/
/******/ 	// getDefaultExport function for compatibility with non-harmony modules
/******/ 	__webpack_require__.n = function(module) {
/******/ 		var getter = module && module.__esModule ?
/******/ 			function getDefault() { return module['default']; } :
/******/ 			function getModuleExports() { return module; };
/******/ 		__webpack_require__.d(getter, 'a', getter);
/******/ 		return getter;
/******/ 	};
/******/
/******/ 	// Object.prototype.hasOwnProperty.call
/******/ 	__webpack_require__.o = function(object, property) { return Object.prototype.hasOwnProperty.call(object, property); };
/******/
/******/ 	// __webpack_public_path__
/******/ 	__webpack_require__.p = "";
/******/
/******/ 	// Load entry module and return exports
/******/ 	return __webpack_require__(__webpack_require__.s = 0);
/******/ })
/************************************************************************/
/******/ ([
/* 0 */
/***/ (function(module, __webpack_exports__, __webpack_require__) {

"use strict";
Object.defineProperty(__webpack_exports__, "__esModule", { value: true });
/* harmony import */ var __WEBPACK_IMPORTED_MODULE_0__info_js__ = __webpack_require__(2);
// 使用模块化思想
// 方法1：使用CommonJS导入mathUtils.js
const { add, mul } = __webpack_require__(1);

console.log(add(20, 30));
console.log(mul(20, 30));

// 方法2：使用ES6导入info.js

// 这里可以不加js后缀，webpack文件会帮你找的
console.log(__WEBPACK_IMPORTED_MODULE_0__info_js__["c" /* name */]);
console.log(__WEBPACK_IMPORTED_MODULE_0__info_js__["a" /* age */]);
console.log(__WEBPACK_IMPORTED_MODULE_0__info_js__["b" /* height */]);


/***/ }),
/* 1 */
/***/ (function(module, exports) {

function add(num1, num2) {
  return num1 + num2;
}

function mul(num1, num2) {
  return num1 * num2;
}

// 使用模块化思想
// 方法1：使用CommonJS导出
module.exports = {
  add,
  mul,
};


/***/ }),
/* 2 */
/***/ (function(module, __webpack_exports__, __webpack_require__) {

"use strict";
// 这个文件里面定义了很多的信息
// 使用模块化思想
// 方法2：使用ES6模块化导出
const name = "why";
/* harmony export (immutable) */ __webpack_exports__["c"] = name;

const age = 18;
/* harmony export (immutable) */ __webpack_exports__["a"] = age;

const height = 1.88;
/* harmony export (immutable) */ __webpack_exports__["b"] = height;



/***/ })
/******/ ]);
~~~



![](Vue框架入门/124.png)

> webpack会自动处理模块之间的依赖，所以mathUtils.js文件不用我们管。
>
> 当我们项目变得很大的时候，各个模块之间会成为一个网络，你依赖我，我依赖你。你不用管，只要找`main.js,`网页的入口文件，其他的依赖文件webpack会自动帮我们弄好。
>
> 当你打包完后，又对原先的js文件进行了增删改操作，那么就要重新打包一下就可以了。

## Webpack配置

> 每次写`webpack ./src/main.js ./dist/bundle.js`太麻烦,能不能只写个webpack，它就自动知道要把src的`main.js`文件打包，并且放到dist文件夹下并且以bundle.js命名呢？

### 入口和出口

![](Vue框架入门/128.png)

> webpack.config.js这个文件名是固定的，不能随便改名字！！(目前是固定的，后面会讲怎么改名字。)

> package.json里面的script标识脚本，你在终端输入`npm run test`,它就会执行test后面的代码，所以我们在后面添加`"build":"webpack"`这样输入`npm run build`就等价于输入`webpack`命令了，二者之间就产生了映射了

**webpack.config.js**

~~~javascript
// 通过CommonJS给它导出一个对象
// 你在终端输入webpack这个命令的时候，它会自动找到webpack.config.js这个文件
// 然后看一下你这里有没有导出入口和出口
// 它就会读取这个入口和出口，就知道你从哪里作为入口，哪里作为出口了

// path:要动态的获取路径(要用到node的语法了)
// const path = require("./path");
// 我们没有这样写，说明不是从当前文件找的这个path,而是从node的包里找的path
// 要想用path,就必须要有path这个包
// 如果装包：终端输入 npm init(进行初始化)
// 然后它会让你起个包的名字，告诉你版本号，描述，入口(随便写，也用不上)是什么等
// 最终会生成一个package.json这个文件
// 如果package.json还依赖一些别的东西的话，我们还会敲npm install
// 这样如果package.json依赖一些东西，它会根据package.json里面所有的依赖帮助我们在当前文件夹里安装一些东西
// 因为我们这里package.json没有什么依赖，所以敲npm install就没有什么效果
// 但是一旦依赖于Node相关的东西，我们肯定要建立package.json这个文件夹的
const path = require("path");
// require是导入，并且赋值给path变量了
module.exports = {
  entry: "./src/main.js",
  // entry:入口
  //   output: "./dist/bundle.js",
  // 出口一般不要这样写，要写成对象类型
  // output:出口
  output: {
    // 出口这里要写2个东西：路径加上文件名字，不能像入口这样简单写
    // path: "./dist",
    // path不能这样写，这样写就是相对路径，人家要求你是绝对路径
    // path:要动态的获取路径(要用到node的语法了)
    path: path.resolve(__dirname, "dist"),
    // __dirname是Node里面的一个全局变量，可以获取当前文件所在路径(dirname前面要加2个下横线)
    // 第二个参数填dist,会将当前路径后面拼接一个dist(这样的话我们整个路径就拥有了)
    // 而且还是一个绝对路径，就不会报错了
    // path这个东西就是一个模块，模块里面有一个函数叫做resolve
    // 它可以把2个路径拼接到一起
    filename: "bundle.js",
  },
};

// 这样写想达成的效果是：终端输入webpack,就自动知道要把src的main.js文件打包，
// 并且放到dist文件夹下并且以bundle.js命名呢
// 而不用这样写了：webpack ./src/main.js ./dist/bundle.js
// 更加的简单

// 我们这里做了半天就做了一件事：将入口和出口的东西放到一个配置文件里了
// 而不用我们每次在终端里敲命令，又写入口(./src/main.js)，又写出口(./dist.bundle.js)，很麻烦

// 但是其实我们实际中也不敲'webpack'这个命令，而是敲`npm run build`这个命令来构建，打包
// 虽然好像直接敲`webpack`命令好像更加简单，但是如果webapck.config.js名字变了，比如成了production.config.js
// 那你的命令就要重新敲为了webpack production.config.js

// 所以我们可以把webpack这个命令映射到npm run build中，就可以执行webpack相关的命令了
// 怎么映射呢？在package.json里进行配置
~~~

### 局部安装webpack

![](Vue框架入门/129.png)

> 怪不得我在Github上下载的很多项目运行不了呢，我全局安装的Webpack版本是V3.6.0,估计下载的项目依赖的Webpack版本不一样导致无法运行。
>
> 全局Webpack一般用的比较少，一般本地的Webpack用的比较多。
>
> 安装本地Webpack命令：`npm install webpack@3.6.0 --save-dev` (给全局Webpack安装的版本是V3.6.0)，此时的`package.json`文件会多出一行，显示`"devDependencies:{"webpack":"^3.6.0"}"`,表示开发时依赖。

> 依赖分为**开发时依赖**(在开发的时候才依赖Webpack,真正项目运行的时候是不需要Webpack了，因为Webpack的作用就是打包出去一个包，然后把这个包放到服务器。打包完后Webpack就没有利用价值了，就被抛弃了)和**运行时依赖**(运行的时候才依赖Webpack)两种

> 只要在终端里敲命令，用的Webpack都是全局的。但是如果定义了脚本，那么执行命令的时候就会优先执行本地的Webpack命令了。
>
> `node_modules/.bin/webpack`这样写也可以启用本地的Webpack版本。

### package.json中定义启动

![](Vue框架入门/130.png)

**package.json**

> 我的`npm install webpack@3.6.0 --save-dev`命令一直没有成功,不知道咋回事。
>
> 我试了一个网上的办法，安装淘宝的cnpm,即：`npm install -g cnpm --registry=https://registry.npm.taobao.org`,以后安装什么东西的时候，用cnpm替换npm看行不行了。
>
> 试了一下`cnpm install webpack@3.6.0 --save-dev`,命令正常使用了，那先就这样吧。

~~~json
{
  "name": "meetwebpack",
  "version": "1.0.0",
  "description": "这个主要是学习配置webpack.config.js,就可以直接使用webpack命令打包了，不用输入webpack ./src/main.js ./dist/bundel.js这么长的命令了",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "build": "webpack"
  },
  "author": "lm",
  "license": "ISC",
  "devDependencies":{
    "webpack":"^3.6.0"
  }
}
~~~

以后只要开发中有`.js`文件都可以像上面这样使用模块化的方法进行开发了，到时候打个包就可以用了。

但是开发中不仅仅有`.js`文件，还有`.css`文件等其他文件，这个时候就要用别的办法了。

## css-loader的使用

### 什么是loader？

![](Vue框架入门/131.png)

> 不同的文件处理会用到不同的loader。
>
> 你不知道用哪个loader可以到[Webpack](https://webpack.js.org/)官网上去看看。

![](Vue框架入门/133.png)

### CSS文件处理 - 准备工作

[css-loader](https://webpack.docschina.org/loaders/css-loader/)

![](Vue框架入门/132.png)

### CSS文件处理 – 打包报错信息

![](Vue框架入门/134.png)

### CSS文件处理 – css-loader

![](Vue框架入门/135.png)

### CSS文件处理 – style-loader

![](Vue框架入门/136.png)

> 这个最终还是遇到了一些问题，导致最后的结果，页面最终无法显示为红色。
>
> 估计还是版本的问题，版本太高了不行，太低了也不行，真的是很难伺候啊。
>
> 浪费了很多时间还是不行，先算了吧。
>
> 果然是版本的问题！！我输入`cnpm install webpack@^4.0.0 `后突然发现可以了！！

## less文件处理

> 第一步：安装；第二步：配置

### less文件处理-准备工作

![](Vue框架入门/137.png)

### less文件处理 – less-loader

[npm 安装参数中的 --save-dev 是什么意思](https://segmentfault.com/q/1010000000403629)

![](Vue框架入门/138.png)

![](Vue框架入门/139.png)

## 图片文件处理 

### 资源准备阶段

![](Vue框架入门/140.png)

### url-loader

![](Vue框架入门/141.png)

![](Vue框架入门/142.png)

> 我这个图片死活也出现不了背景图，也按视频敲的代码了啊。

![](Vue框架入门/143.png)

### file-loader

![](Vue框架入门/144.png)

### 修改文件名称

![](Vue框架入门/145.png)

> 图片文件处理不知道怎么了一直失败，图片路径一直出问题。但是我也不能一直卡在这里浪费时间，就只能先把这个放到一边，开始学习接下来的内容了。
>
> Webpack这部分我发现学习是真的很花时间啊，现在都2020年10月13日了，进度堪忧啊。
>
> 最终，我想到了一个解决方案，我打开了最最原始的视频文件，解压出来了最最原始的老师写的代码，把里面的node_modules文件给重新复制到我的项目里面，把原先的node_modules文件给删了，结果：喜大普奔，前面的图片最终成功显示了！！！！

## ES6语法处理

![](Vue框架入门/146.png)

> 报错：`Uncaught Error: Module build failed: Error: Plugin/Preset files are not allowed to export objects, only functions. In D:\vedio\4-Vue.js\Vue现在代码-2020.09\13-webpack\01-webpack的使用\03-webpack的loader\node_modules\babel-preset-es2015\lib\index.js`
>
> 报错是真的烦，意味着没有办法跟着视频看得到结果，直接忽略进行下一步又感觉前面有东西卡着，总是感觉到美中不足。
>
> 最终，我想到了一个解决方案，我打开了最最原始的视频文件，解压出来了最最原始的老师写的代码，把里面的node_modules文件给重新复制到我的项目里面，把原先的node_modules文件给删了，结果：喜大普奔，不仅ES6这里没有问题了，前面的图片也最终成功显示了！！！！
>
> 我现在感觉我非常有必要去研究一下node_modules这个文件夹了，里面的东西特别多，而我突然发现我对于node_modules这个文件夹到底是干什么的都不知道。需要搜一搜有关它的信息了。

## Webpack配置Vue

### 引入vue.js

![](Vue框架入门/147.png)

> 我们以后会以`.vue`的形式来使用Vue

### 打包项目 – 错误信息

![](Vue框架入门/148.png)

> runtime-only:代码中，不可以有任何的template
>
> runtime-compiler:代码中，可以有template,因为有compiler可以用于编译template

* 首先，通过`cnpm install vue --save`(注意，不要写dev)来安装Vue(先安装)
* 然后，在`main.js`里`import Vue form 'vue'`导入Vue(再引入)
* 导入后系统会在node_modules包里面找到你安装的东西(Vue)
* 在`main.js`中写入Vue实例
* 在`index.html`中挂载Vue实例
* 运行时发现报错，在`webpack.config.js`里写一个Vue的别名(alias)

#### 项目整体代码

![](Vue框架入门/149.png)

**normal.css**

~~~css
body {
  background-color: pink;
  /* 这里面要加引号才行！！ */
  /* 我发现不加引号其实也行 */
  /* background: url("../img/test02.jpg"); */
  background: url(../img/test.jpg);
}
~~~

**special.less**

~~~less
@fontSize: 100px;
@fontColor: blue;

body {
  font-size: @fontSize;
  color: @fontColor;
}
~~~

**info.js**

~~~javascript
// 这个文件里面定义了很多的信息
// 使用模块化思想
// 方法2：使用ES6模块化导出
export const name = "why";
export const age = 18;
export const height = 1.88;
~~~

**mathUtils.js**

~~~javascript
function add(num1, num2) {
  return num1 + num2;
}

function mul(num1, num2) {
  return num1 * num2;
}

// 使用模块化思想
// 方法1：使用CommonJS导出
module.exports = {
  add,
  mul,
};
~~~

**main.js**

~~~javascript
// 使用模块化思想
// 方法1：使用CommonJS导入mathUtils.js
const { add, mul } = require("../src/js/mathUtils");

console.log(add(20, 30));
console.log(mul(20, 30));

// 方法2：使用ES6导入info.js
import { name, age, height } from "../src/js/info.js";
// 这里可以不加js后缀，webpack文件会帮你找的
console.log(name);
console.log(age);
console.log(height);

//3.依赖css文件
require('./css/normal.css')

//4.依赖less文件
require('./css/special.less')
document.writeln('<h2>你好，世界</h2>')

// 5.使用Vue进行开发
// 我们在用Vue之前要先引入这个Vue
// 我们已经在node_modules里通过cnpm install vue --save安装过了
// 但是安装只是安装，我们还要进行引用(依赖它)
import Vue from 'vue'

// const app = new Vue({
// 真实开发中不需要赋值给一个变量，直接用就可以了
new Vue({
    el: '#app',
    data: {
        message:'Hello Webpack'
    }
})
~~~

**index.html**

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <div id="app">
        <h2>{{message}}</h2>
    </div>

    <script src="./dist/bundle.js"></script>
</body>

</html>
~~~

**package.json**

> 自从使用`cnpm init`初始化项目之后，每次下载包都加上`--save`它就会自动把下载包的配置信息都放到上面了，不用我们手动添加了。

[package.json和package-lock.json区别小结](https://juejin.im/post/6844903907290775565)

~~~json
{
  "name": "meetwebpack",
  "version": "1.0.0",
  "description": "这个主要是学习配置webpack.config.js,就可以直接使用webpack命令打包了，
  不用输入webpack ./src/main.js ./dist/bundel.js这么长的命令了",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "build": "webpack"
  },
  "author": "lm",
  "license": "ISC",
  "devDependencies": {
    "babel-core": "^6.26.3",
    "babel-loader": "^7.1.5",
    "babel-preset-env": "^1.7.0",
    "babel-preset-es2015": "^6.24.1",
    "css-loader": "^2.0.2",
    "file-loader": "^6.1.1",
    "less": "^3.12.2",
    "less-loader": "^7.0.2",
    "sass-loader": "^7.3.1",
    "style-loader": "^2.0.0",
    "url-loader": "^4.1.1",
    "webpack": "^3.6.0",
    "webpack-cli": "^4.0.0"
  },
  "dependencies": {
    "vue": "^2.6.12"
  }
}
~~~

**webpack.config.js**

~~~javascript

const path = require("path");
// require是导入，并且赋值给path变量了
module.exports = {
  entry: "./src/main.js",

  output: {
    // 出口这里要写2个东西：路径加上文件名字，不能像入口这样简单写
    // path: "./dist",
    // path不能这样写，这样写就是相对路径，人家要求你是绝对路径
    // path:要动态的获取路径(要用到node的语法了)
    path: path.resolve(__dirname, "dist"),
    // __dirname是Node里面的一个全局变量，可以获取当前文件所在路径(dirname前面要加2个下横线)
    // 第二个参数填dist,会将当前路径后面拼接一个dist(这样的话我们整个路径就拥有了)
    // 而且还是一个绝对路径，就不会报错了
    // path这个东西就是一个模块，模块里面有一个函数叫做resolve
    // 它可以把2个路径拼接到一起
    filename: "bundle.js",
    publicPath:"dist/"
    // 以后只要涉及到url前面都会加入dist/了
  },
  module: {
    rules: [
      {
        test: /\.css$/i,
        // css-loader只负责将css文件进行加载
        // style-loader负责将样式添加到DOM中
        // 使用多个loader时, 是从右向左
        use: ['style-loader', 'css-loader'],
      },
      {
        test: /\.less$/,
        use: [{
          loader: "style-loader" // creates style nodes from JS strings
        }, {
          loader: "css-loader" // translates CSS into CommonJS
        }, {
          loader: "less-loader" // compiles Less to CSS
        }]
      },
      {
        test: /\.(png|jpg|gif|jpeg)$/i,
        use: [
          {
            loader: 'url-loader',
            options: {
              // 当加载的图片小于limit时，会将图片编译成base64字符串形式
              // 当加载的图片大于limit时，需要使用file-loader模块进行加载
              limit: 1300,
              name:'img/[name].[hash:8].[ext]'
            },
          },
        ],
      },
       {
         test: /\.js$/,
      //exclude:排除
      exclude: /(node_modules|bower_components)/,
      use: {
        loader: 'babel-loader',
        options: {
          // preset:预设
          // presets: ['@babel/preset-env']
          // 不要写这个，写ES2015就可以了
          presets:['es2015']
        }
      }
    }
    ],
  },
  resolve: {
    alias: {
      // alias:别名的意思
      // 举例:
      // git commit -m'注释'
      // git config alias ...
      // $符号表示结尾的意思
      'vue$':'vue/dist/vue.esm.js'
    }
  }
};
~~~

### el和template区别（一）

![](Vue框架入门/150.png)

> 在我们的SPA(single page web application)单页富应用程序中，一般来说只有一个`index.html`文件，如果有多个页面到时候会用路由(vue-router)进行跳转。
>
> 当只有一个`index.html`的时候，一般这里面的内容是不改的，是固定的。

[一种SPA（单页面应用）架构](https://segmentfault.com/a/1190000000607661)

#### 项目部分代码升级1.0

> 因为老师是每次讲几个知识点，项目代码也会相应的修改和完善，我觉得有必要记录这种完善的过程。

**index.html**

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <!-- <div id="app">
        <h2>{{message}}</h2>
        <button>按钮</button>
    </div> -->
    <!-- 一般来说单页面富应用(SPA)里面只有一个index.html -->
    <!-- 而且这里面的东西基本上不会随便更改 -->
    <!-- 所以上面基本不会出现{{message}}这样的东西 -->

    <div id="app">
        <!-- 只会这样，干干净净的里面只有一个div -->
    </div>
    <!-- 那么如果我想要显示Vue里面的内容怎么办呢？ -->
    <!-- 解决方法：就在Vue里面添加template -->

    <script src="./dist/bundle.js"></script>
    <!-- 到了后面这行代码都不用写，都是可以删除掉的！！ -->
</body>

</html>
~~~

**main.js**

~~~javascript
//前面的东西都学过了，和Vue关系不大，我都删除了

// 5.使用Vue进行开发
// 我们在用Vue之前要先引入这个Vue
// 我们已经在node_modules里通过cnpm install vue --save安装过了
// 但是安装只是安装，我们还要进行引用(依赖它)
import Vue from 'vue'

// const app = new Vue({
    // 真实开发中不需要赋值给一个变量，直接用就可以了
new Vue({
    el: '#app',
    // 一旦你定义了一个template,template里面的东西，
    // vue内部源码会将这一坨东西复制到index.html中id为app的div里面去

    // 但是有一个问题：在Vue实例里面写很多template肯定不好，以后Vue实例里的代码肯定会越来越多
    template: `
        <div>
            <h2>{{message}}</h2>
            <h2>{{name}}</h2>
            <button @click="btnClick">按钮</button>
        </div>
    `,
    data: {
        message: 'Hello Webpack',
        name:'codewhy'
    },
    methods: {
        btnClick() {
            console.log('按钮点击了');
        }
    },
})
~~~

### el和template区别（二）

![](Vue框架入门/151.png)

#### 项目部分代码升级2.0

**main.js**

~~~javascript
// 前面的东西都学过了，和Vue关系不大，我都删除了

// 5.使用Vue进行开发
// 我们在用Vue之前要先引入这个Vue
// 我们已经在node_modules里通过cnpm install vue --save安装过了
// 但是安装只是安装，我们还要进行引用(依赖它)
import Vue from 'vue'

const App = {
    // 这个就是一个对象
    // 在实例里写template太臃肿了，在这里定义一个组件
    template: `
        <div>
            <h2>{{message}}</h2>
            <h2>{{name}}</h2>
            <button @click="btnClick">按钮</button>
        </div>
    `,
    data() { 
        // 把data相关的东西也放到这里，不放到实例里面
        return {
            message: 'Hello Webpack',
            name:'codewhy'
        }
    },
       methods: {
        btnClick() {
            console.log('按钮点击了');
        }
    }
} 

new Vue({
    el: '#app',
    // 一旦你定义了一个template,template里面的东西，
    // vue内部源码会将这一坨东西复制到index.html中id为app的div里面去

    // 但是有一个问题：在Vue实例里面写很多template肯定不好，以后Vue实例里的代码肯定会越来越多
    template: '<App/>',
    // 到时候<App/>会被替换为<div id="app"><App></App></div>
    components: {
        App
        // 这个是ES6对象的简写，完整版是App:App,表示组件标签：组件构造器
    }
    // 把template也放到App对象里
    // template: `
    //     <div>
    //         <h2>{{message}}</h2>
    //         <h2>{{name}}</h2>
    //         <button @click="btnClick">按钮</button>
    //     </div>
    // `,
    // 把data,methods这些东西都放到template里
    // data: {
    //     message: 'Hello Webpack',
    //     name:'codewhy'
    // },
    // methods: {
    //     btnClick() {
    //         console.log('按钮点击了');
    //     }
    // },
})
~~~

### Vue组件化开发引入

![](Vue框架入门/152.png)

#### 项目部分代码升级3.0

> 我们在src文件夹下新建一个vue文件夹，vue文件夹下建立一个`app.js`文件

**main.js**

~~~javascript
// 前面的东西都学过了，和Vue关系不大，我都删除了

// 5.使用Vue进行开发
// 我们在用Vue之前要先引入这个Vue
// 我们已经在node_modules里通过cnpm install vue --save安装过了
// 但是安装只是安装，我们还要进行引用(依赖它)
import Vue from 'vue'

import App from './vue/app.js'
// 这样写，立马main.js里面的代码变得很简洁了

new Vue({
    el: '#app',
    template: '<App/>',
    components: {
        App
    }
})
~~~

**app.js**

~~~javascript
// 以后改App组件这个代码，以后就可以全部在这里改了
// 但是这里也是有一点不好的地方，就是模版和js代码没有进行分离
export default {
    template: `
        <div>
            <h2>{{message}}</h2>
            <h2>{{name}}</h2>
            <button @click="btnClick">按钮</button>
        </div>
    `,
    data() { 
        // 把data相关的东西也放到这里，不放到实例里面
        return {
            message: 'Hello Webpack',
            name:'codewhy'
        }
    },
       methods: {
        btnClick() {
            console.log('按钮点击了');
        }
    }
} 
~~~

### .vue文件封装处理

[初识 Vue.js 中的 *.Vue文件](https://blog.csdn.net/qq_36838191/article/details/80413977)

![](Vue框架入门/153.png)

> 遇到问题先去`package.json`里改一下'vue-loader'的版本，改为`"^13.0.0.0"`，然后在终端执行`npm install`重新做一下安装。

#### 项目部分代码升级4.0

> 在vue文件夹下新建一个App.vue的文件

**main.js**

~~~javascript
// 前面的东西都学过了，和Vue关系不大，我都删除了

// 5.使用Vue进行开发
// 我们在用Vue之前要先引入这个Vue
// 我们已经在node_modules里通过cnpm install vue --save安装过了
// 但是安装只是安装，我们还要进行引用(依赖它)
import Vue from 'vue'

// import App from './vue/app.js'
// 在app.js的基础上升级，新建了App.vue。原先的app.js可以不用了
// 转而引入APP.vue这个文件
import App from './vue/App.vue'

new Vue({
    el: '#app',
    template: '<App/>',
    components: {
        App
    }
})
~~~

**App.vue**

~~~vue
<template>
<!-- 新建了.vue文件，它是不知道怎么加载的，所以要进行配置对应的loader -->
<!-- 模版写最上面 -->
<!-- 把app.js里面template标签里面的内容放到这里 -->
   <div>
        <h2 class="title">{{message}}</h2>
        <h2>{{name}}</h2>
        <button @click="btnClick">按钮</button>
    </div>
</template>

<script>
// JS代码写中间
// 把app.js里面data()函数里面的内容放到这里面\
export default {
    name:"App",
     data() { 
        // 把data相关的东西也放到这里，不放到实例里面
        return {
            message: 'Hello Webpack',
            name:'codewhy'
        }
    },
       methods: {
        btnClick() {
            console.log('按钮点击了');
        }
    }
}
</script>


<style scoped>
    /* 样式写下面 */
    /* 模版，JS代码，样式三者之间形成了完全的分离 */
    /* 这整个App.vue就是一个组件 */
    /* 这里面还可以写样式 */
    .title{
        color:green
    }
</style>
~~~

#### 项目部分代码升级5.0

> 在在vue文件夹下再新建一个Cpn.vue的文件(也是一个组件，让App.vue引用Cpn.vue)

**App.vue**

~~~vue
<template>
<!-- 新建了.vue文件，它是不知道怎么加载的，所以要进行配置对应的loader -->
<!-- 模版写最上面 -->
<!-- 把app.js里面template标签里面的内容放到这里 -->
   <div>
        <h2 class="title">{{message}}</h2>
        <h2>{{name}}</h2>
        <button @click="btnClick">按钮</button>
        <Cpn></Cpn>
        <!-- 其实这里大写小写都没问题 -->
    </div>
</template>

<script>
// JS代码写中间
// 把app.js里面data()函数里面的内容放到这里面
import Cpn from './Cpn.vue'
// 把Cpn.vue导入到App.vue中去

export default {
    name:"App",
    // 导入Cpn之后，还要在这里对它进行注册
    components:{
        Cpn
        // 这个是在组件里面注册组件
    },
     data() { 
        // 把data相关的东西也放到这里，不放到实例里面
        return {
            message: 'Hello Webpack',
            name:'codewhy'
        }
    },
       methods: {
        btnClick() {
            console.log('按钮点击了');
        }
    }
}
</script>


<style scoped>
    /* 样式写下面 */
    /* 模版，JS代码，样式三者之间形成了完全的分离 */
    /* 这整个App.vue就是一个组件 */
    /* 这里面还可以写样式 */
    .title{
        color:green
    }
</style>
~~~

**Cpn.vue**

~~~vue
<template>
    <div>
        <h2>我是cpn组件的标题</h2>
        <p>我是cpn组件的内容，哈哈哈</p>
        <h2>{{name}}</h2>
    </div>
</template>

<script>
export default {
    name:"Cpn",
    data(){
        return {
            name:'cpn组件的名字'
        }
    }
}
</script>

<style scoped>
    
</style>
~~~

## plugin的使用

### 认识plugin

![](Vue框架入门/154.png)

### 添加版权的Plugin

![](Vue框架入门/155.png)

### 打包html的plugin

![](Vue框架入门/156.png)

### JS压缩的Plugin

![](Vue框架入门/157.png)

> 在开发阶段不建议使用这个插件，因为JS被压缩(丑化)后，我们就十分不方便调试修改代码了。
>
> 我们只在最后发布的时候才把丑化加进来。

## 搭建本地服务器

> 我们每次修改文件时都要`npm run build`重新编译，很麻烦，所以来搭建一个本地服务器。
>
> 第一步：使用`npm install--save-dev webpack-dev-server@2.9.1`安装devserver本地服务器
>
> 第二步：在`webpack.config.js`里配置`contentBase`和`inline`
>
> 第三步：在`package.json`里配置` "dev": "webpack-dev-server --open"`(位置在script标签下面)

![](Vue框架入门/158.png)

> 安装完后在终端敲`webpack-dev-server`,但是会报错，因为我们只要在终端敲的命令，都会在全局找，但是我们没有在全局装过这个东西。
>
> 解决方法1：我们在终端敲`.\node_modules\.bin\webpack-dev-server`,使用相对路径运行这个指令，是可以运行的。
>
> 解决方法2：在`package.json`里配置脚本scripts(后面加上--open就不用自己点击网页地址打开浏览器了，输入命令后自动打开浏览器了)，然后再输入命令`npm run dev`就可以运行`webpack-dev-server`这个命令，就可以搭建起本地服务器了。
>
> 等你使用过`npm run dev`进行测试在本地服务器上运行感觉可以的时候，再使用`npm run build`命令进行真正的打包，就可以了。

## Webpack配置文件抽离

[关于vue的npm run dev和npm run build的区别介绍](https://www.jb51.net/article/154579.htm)

[pro、pre、test、dev环境](https://blog.csdn.net/linzhiqiang0316/article/details/82749649)

[开发环境、测试环境、生产环境 -- 区别](https://blog.csdn.net/yanglangdan/article/details/102552388)

> **开发环境（development）**：开发环境是程序猿们专门用于开发的服务器，配置可以比较随意， 为了开发调试方便，一般打开全部错误报告。(程序员接到需求后，开始写代码，开发，运行程序，看看程序有没有达到预期的功能；)
>
> **测试环境（testing）**：一般是克隆一份生产环境的配置，一个程序在测试环境工作不正常，那么肯定不能把它发布到生产机上。(程序员开发完成后，交给测试部门全面的测试，看看所实现的功能有没有bug，测试人员会模拟各种操作情况；)
>
> **生产环境（production）**：是指正式提供对外服务的，一般会关掉错误报告，打开错误日志。(就是线上环境，发布到对外环境上，正式提供给客户使用的环境。)
>
> 三个环境也可以说是系统开发的三个阶段：开发->测试->上线，其中生产环境也就是通常说的真实环境。

webpack.config.js文件配置中，有些是在打包的时候才需要进行配置，开发阶段不用（比如JS丑化，代码压缩），有些是在开发的时候才需要进行配置，打包的时候不用（比如devserver本地服务器配置）

我们建立一个build文件夹，所有配置相关的文件都放到这里面。

首先在里面建立一个`base.config.js`文件，这里面放一些公共的东西(开发时和生产时都依赖的配置文件才放到这里面)， 然后把`webpack.config.js`里面的所有内容都复制到`base.config.js`里面。

再在build文件夹下建立一个`prod.config.js`(prod是production的缩写)文件，表明生产时依赖，然后把`webpack.config.js`里面的所有内容都复制到`prod.config.js`里面。

再在build文件夹下建立一个`dev-config-js`文件，表明开发时依赖，然后把`webpack.config.js`里面的所有内容都复制到`dev.config.js`里面。

先全部拷贝过来后，再开始根据需要删除。

* 我们开发的时候的配置文件就是`base.config.js` + `prod.config.js`,

* 我们生产(编译)的时候的配置文件就是`base.config.js` + `dev-config.js`。

但是我们并没有进行真正的文件分离，我们要在终端里输入命令装一些东西，命令是：`npm install webpack-merge --save-dev`(这个也是开发时依赖，所以加上-dev)

最后删除`webpack.config.js文件`，一分为三：`base.config.js`,`dev-config-js`,`prod.config.js`。

### 配置前

**wepack.config.js**

~~~javascript
const path = require("path");
const webpack = require('webpack');
const HtmlwebpackPlugin = require('html-webpack-plugin')
const UglifyjsWebpackPlugin = require('uglifyjs-webpack-plugin')
// require是导入，并且赋值给path变量了
module.exports = {
  entry: "./src/main.js",
  output: {
    // 出口这里要写2个东西：路径加上文件名字，不能像入口这样简单写
    // path: "./dist",
    // path不能这样写，这样写就是相对路径，人家要求你是绝对路径
    // path:要动态的获取路径(要用到node的语法了)
    path: path.resolve(__dirname, "dist"),
    // __dirname是Node里面的一个全局变量，可以获取当前文件所在路径(dirname前面要加2个下横线)
    // 第二个参数填dist,会将当前路径后面拼接一个dist(这样的话我们整个路径就拥有了)
    // 而且还是一个绝对路径，就不会报错了
    // path这个东西就是一个模块，模块里面有一个函数叫做resolve
    // 它可以把2个路径拼接到一起
    filename: "bundle.js",
    // publicPath:"dist/"
    // 添加了index插件后，配置这个反而多余了
    // 以后只要涉及到url前面都会加入dist/了
  },
  module: {
    rules: [
      {
        test: /\.css$/i,
        // css-loader只负责将css文件进行加载
        // style-loader负责将样式添加到DOM中
        // 使用多个loader时, 是从右向左
        use: ['style-loader', 'css-loader'],
      },
      {
        test: /\.less$/,
        use: [{
          loader: "style-loader" // creates style nodes from JS strings
        }, {
          loader: "css-loader" // translates CSS into CommonJS
        }, {
          loader: "less-loader" // compiles Less to CSS
        }]
      },
      {
        test: /\.(png|jpg|gif|jpeg)$/i,
        use: [
          {
            loader: 'url-loader',
            options: {
              // 当加载的图片小于limit时，会将图片编译成base64字符串形式
              // 当加载的图片大于limit时，需要使用file-loader模块进行加载
              limit: 1300,
              name:'img/[name].[hash:8].[ext]'
            },
          },
        ],
      },
       {
         test: /\.js$/,
      //exclude:排除
      exclude: /(node_modules|bower_components)/,
      use: {
        loader: 'babel-loader',
        options: {
          // preset:预设
          // presets: ['@babel/preset-env']
          // 不要写这个，写ES2015就可以了
          presets:['es2015']
        }
      }
      },
      {
        test: /\.vue$/,
        use: ['vue-loader']
      },
    ],
  },
  resolve: {
    alias: {
      // alias:别名的意思
      // 举例:
      // git commit -m'注释'
      // git config alias ...
      // $符号表示结尾的意思
      'vue$':'vue/dist/vue.esm.js'
    },
    extensions: [".js", ".css", ".vue"]
    // 意思是以后这些后缀可以不写
  },
  // 添加版权插件
  plugins: [
    new webpack.BannerPlugin('最终版权归筛滤淘所有'),
    // JS压缩插件和版权插件只能选一个，因为压缩插件会将所有注释都去掉，包括版权声明
    new HtmlwebpackPlugin({
      template: 'index.html'
      // 意思是根据index.html生成模版
    }),
    new UglifyjswebpackPlugin()
    // 我们在开发阶段不需要JS压缩，只在发布阶段才需要这个

  ],
  devServer: {
    contentBase: './dist',
    inline: true
    // inline表示是否需要实时监听
    // 暂时只需要配置这2个东西就可以了
    // 我们在开发的时候才需要这个，真正编译打包后就不需要这个了
  }
};
~~~

### 配置后

**base.config.js**

~~~javascript
const path = require('path')
const webpack = require('webpack')
const HtmlWebpackPlugin = require('html-webpack-plugin')
const UglifyjsWebpackPlugin = require('uglifyjs-webpack-plugin')

module.exports = {
  entry: './src/main.js',
  output: {
    path: path.resolve(__dirname, '../dist'),
    filename: 'bundle.js',
    // publicPath: 'dist/'
  },
  module: {
    rules: [
      {
        test: /\.css$/,
        // css-loader只负责将css文件进行加载
        // style-loader负责将样式添加到DOM中
        // 使用多个loader时, 是从右向左
        use: [ 'style-loader', 'css-loader' ]
      },
      {
        test: /\.less$/,
        use: [{
          loader: "style-loader", // creates style nodes from JS strings
        }, {
          loader: "css-loader" // translates CSS into CommonJS
        }, {
          loader: "less-loader", // compiles Less to CSS
        }]
      },
      {
        test: /\.(png|jpg|gif|jpeg)$/,
        use: [
          {
            loader: 'url-loader',
            options: {
              // 当加载的图片, 小于limit时, 会将图片编译成base64字符串形式.
              // 当加载的图片, 大于limit时, 需要使用file-loader模块进行加载.
              limit: 13000,
              name: 'img/[name].[hash:8].[ext]'
            },
          }
        ]
      },
      {
        test: /\.js$/,
        // exclude: 排除
        // include: 包含
        exclude: /(node_modules|bower_components)/,
        use: {
          loader: 'babel-loader',
          options: {
            presets: ['es2015']
          }
        }
      },
      {
        test: /\.vue$/,
        use: ['vue-loader']
      }
    ]
  },
  resolve: {
    // alias: 别名
    extensions: ['.js', '.css', '.vue'],
    alias: {
      'vue$': 'vue/dist/vue.esm.js'
    }
  },
  plugins: [
    new webpack.BannerPlugin('最终版权归aaa所有'),
    new HtmlWebpackPlugin({
      template: 'index.html'
    })
  ]
}
~~~

**dev.config.js**

~~~javascript
const webpackMerge = require('webpack-merge')
const baseConfig = require('./base.config')

module.exports = webpackMerge(baseConfig, {
  devServer: {
    contentBase: './dist',
    inline: true
  }
})
~~~

**prod.config.js**

~~~javascript
const UglifyjsWebpackPlugin = require('uglifyjs-webpack-plugin')
const webpackMerge = require('webpack-merge')
const baseConfig = require('./base.config')

module.exports = webpackMerge(baseConfig, {
  plugins: [
    new UglifyjsWebpackPlugin()
  ]
})
~~~

这个时候运行`npm run build`会报错：`A configuration file could be named 'webpack.config.js' in the current directory.`这个时候在`package.json`里修改`build`,由原来的`"webpack"`改为` "webpack --config ./build/prod.config.js"`,修改`dev`,由原来的`"webpack-dev-server --open"`改为`"webpack-dev-server --open --config ./build/dev.config.js"`即可。

# Vue CLI脚手架

> 视频里老师先让我们学的脚手架2，再学脚手架3，脚手架4当时还没出来，所以没学。

[Vue CLI中文文档](https://cli.vuejs.org/zh/)

[vue-cli和webpack是什么关系?](https://segmentfault.com/q/1010000018799188)

## 什么是Vue CLI

![](Vue框架入门/159.png)

### Vue CLI使用前提 - Node

![](Vue框架入门/160.png)

### Vue CLI使用前提 - Webpack

![](Vue框架入门/161.png)

### Vue CLI的使用

> 脚手架我们一般直接安装到全局就可以了。

![](Vue框架入门/162.png)

## Vue CLI2

### Vue CLI2详解

> ESLint可以让代码更加规范，但是有些地方感觉不好用，比如，代码后面它不让加分号，不然报错；函数名和小括号之间要有空格，不然也报错。另外它这个规范不一定就是公司自己的规范，所以后面老师讲课的时候不使用ESLint了。
>
> 如果你之前安装了ES Lint，后来又不想用它了，怎么关呢？`config文件夹-->index.js-->useEslint: false`，然后把项目关掉，重新进行编译即可。

![](Vue框架入门/163.png)

### 目录结构详解

![](Vue框架入门/164.png)

### Runtime-Compiler和Runtime-only的区别

> `devDependencies`表示**开发时依赖**(只在开发的时候用)，`dependencies`表示**运行时依赖**(比如我们运行时需要用Vue)。
>
> `main.js`里面有一个`new Vue({})`,里面有`el:'#app'`,还有`template:'<App/>'`,到时候会将`index.html`里面`<div id="app"></div>`里面的内容自动替换为template里面的内容。

![](Vue框架入门/165.png)

### render和template

![](Vue框架入门/167.png)

`Runtime-compiler`和`Runtime-only`的区别只在一个文件里面，那就是`main.js`。

![](Vue框架入门/166.png)

* `Runtime-compiler`在用我们App的时候，它是怎么用的呢？
  * 第一步：它要把这个App在components里面做一个注册
  * 第二步：注册完之后就可以在template里面使用这个东西

* `Runtime-only`没有注册，搞了一个render属性，里面是一个箭头函数`h=>h(App)`，这个箭头函数的原始表达式是：`render:function(h){return h(App)}`，这里面的h其实是一个东西(createElement函数)的缩写。

[关于Vue中的 render: h => h(App) 具体是什么含义？](https://segmentfault.com/q/1010000007130348)

### Vue程序运行过程

![](Vue框架入门/168.png)

>  当我们把我们的template(模版)传给Vue的时候，Vue里面会做一个保存，保存到Vue实例下面的options里(`vm.options`)，保存完后会把这个template进行一个parse(解析)，把template解析为一个AST(抽象语法树)，然后把抽象语法树再进行compiler(编译)成另外一个东西：render函数，通过render函数把对应的template转成virtual DOM(虚拟DOM)节点，最终转换为虚拟DOM树,再把这个虚拟DOM树渲染成真实的DOM,也就是UI上面的一些东西。

`Runtime-compiler`：`template ——> AST——>render函数——>虚拟DOM——>真实DOM(UI)`

> `Runtime-compiler`需要更多Vue的原始代码(用来处理`<template>`)

`Runtime-only(性能更高)`：`render函数——>虚拟DOM——>真实DOM(UI)`(不经过前面的`template——>AST`了)

> 不需要处理`<template>`,所以代码量更少，比`Runtime-compiler`要少6KB的代码量。

疑问：老师不对啊，那个`App.vue`里面不是也有`<template>`吗？

回答：最终这个`<template>`是不存在的,App对象最后会被渲染成一个普通对象，里面是没有`<template>`的！！是由`vue-template-compiler(开发时依赖，最终运行出来的所有项目中的所有的组件都不包含任何的<template>了)`将`<template>`解析为render函数了。

### render函数的使用

![](Vue框架入门/169.png)

**`Runtime-compiler`里的main.js**

~~~javascript
// The Vue build version to load with the `import` command
// (runtime-only or standalone) has been set in webpack.base.conf with an alias.
import Vue from 'vue'
import App from './App'

Vue.config.productionTip = false

console.log(App);
// App对象最后会被渲染成一个普通对象，里面是没有template的！！

/* eslint-disable no-new */
// const cpn = {
//   template: `<div>{{message}}</div>`,
//   data() { 
//     // 组件里面可以有data,可以return一些东西
//     return {
//       message:'我是组件message'
//     }
//   }
// }

// 上面这段是老师讲课时添加的

new Vue({
  el: '#app',
  // components: { App },
  // template: '<App/>',
  // 01里面其实也是可以使用render函数的
  render: function (createElement) { 
    // 1.0版普通用法(从零开始自己创建标签)
    // 1.createElement('标签',{标签的属性},['标签里面的内容'])
    // return createElement('h2', {class:'box'},['Hello World'])
    // 到时候<div id="app"></div>会变成<h2></h2>了

    // 2.0版普通用法(从零开始自己创建标签)
    // return createElement('h2',
    //   { class: 'box' },
    //   ['Hello World', createElement('button', ['按钮'])])
    
    // 3.0版升级用法：传入一个组件对象
    // cpn是前面定义的组件，这里就没有template进行编译了
    // return createElement(cpn)
    // 既然可以传入cpn组件，那App这个组件也是可以传进去的
    return createElement(App)

  }
})

// 下面的例子是用来演示eslint的，注释掉
// function sum(num1, num2) { 
//   // 如果用了eslint,函数名和小括号之间必须有空格，否则报错
//   // 如果用了eslint，你定义完函数必须要用它，不用它也会报错
//   return num1 + num2
// }

// console.log(sum(1, 2));

// 这个函数后面必须要再敲回车，来个新行，否则还报错 Trailing spaces not allowed
// eslint标准里面一行结尾后不加分号 
~~~

### npm run build过程

![](Vue框架入门/170.png)

### npm run dev过程

![](Vue框架入门/171.png)

### 修改配置：webpack.base.conf.js起别名

> 先不讲，到时候用到的时候再讲。

![](Vue框架入门/172.png)

## Vue CLI3

### 认识Vue CLI3

> 脚手架版本不是依赖Vue的版本的，而是依赖Webpack版本的，这一点要弄清楚。
>
> 脚手架3的设计原则是"0配置"，它把原本在根目录下的配置文件给你隐藏起来了，但是如果你还想手动配置的话也是可以的，到时候会说。
>
> Vue CLI2里面有一个单独的`config`文件夹，所有的配置信息都放在里面，Vue CLI3里面就没有了，给你藏起来了。
>
> 隐藏的位置：`node_modules-@vue-'cli-service'-webpack.config.js`，就藏在这里面了。
>
> 如果你确实需要对默认的配置进行修改，你就在当前的项目下创建一个文件，名字是固定的，不要随便修改，叫`vue.config.js`
>
> 你可以把新增的public文件夹当成移除了的static文件夹，到时候它里面的东西也是原封不动的封装到dist文件夹里面去的。

![](Vue框架入门/173.png)

### Vue CLI3配置信息

> Vue CLI3初始化项目命令是：`vue create 项目名称`
>
> Vue CLI2初始化项目命令是：`vue init webpack 项目名称`
>
> 不要弄混了！！

> 输入命令初始化项目后按空格键是选中和取消。

![](Vue框架入门/174.png)

> PWA意思是渐进式Web应用，一个PWA应用首先是一个网页，可以通过Web技术编写出一个网页应用随后添加上App Manifest和Service Worker来实现PWA的安装和离线等功能。
>
> 它可以缓存很多东西。

[讲讲PWA](https://segmentfault.com/a/1190000012353473)

![](Vue框架入门/175.png)

![](Vue框架入门/176.png)

> preset：配置   
>
> manually：手动的
>
> 脚手架3默认会创建`.git`的文件夹，用于版本控制。这个文件夹是隐藏的，取消隐藏才能看到。
>
> 当我们通过`npm`安装包的时候，它的安装位置就是在`node_modules`里面。

### 目录结构详解

![](Vue框架入门/177.png)

> 脚手架3里面的`package.json`使用了工具(cli-service)，导致里面的配置信息少了很多，它不想让你看到这么多的配置，它的设计原则就是"0配置"。
>
> `package-lock.json`是一个中间文件，表示你真实安装的文件版本，`package.json`里面的文件版本前面有一个波浪号，表示在这个版本之上，但是并没有明确说是哪个版本。

**.gitignore**

~~~javascript
# .gitignore表示不需要上传到服务器上的东西，忽略掉
.DS_Store
node_modules
# node_modules不需要上传到服务器上去！！
/dist
# dist表示打包的东西，打包只要一个人打包(组长或项目精力)就可以了

# /src
# 如果加上/src,则以后src文件夹里面的所有东西都不会提交到服务器了

# local env files
# 这个时忽略本地环境文件
.env.local
.env.*.local

# Log files
# 这个时忽略日志文件
npm-debug.log*
yarn-debug.log*
yarn-error.log*
pnpm-debug.log*

# Editor directories and files
# 这个是集成开发环境有关的忽略文件
# 用WebStorm开发就忽略.idea文件
# 用VSCode开发就忽略.vscode文件
.idea
.vscode
*.suo
*.ntvs*
*.njsproj
*.sln
*.sw?
~~~

**package.json**

~~~json
{
  "name": "01-testvuecli3",
  "version": "0.1.0",
  "private": true,
  "scripts": {
    "serve": "vue-cli-service serve",
    "build": "vue-cli-service build"
  },
  "dependencies": {
    "core-js": "^3.6.5",
    "vue": "^2.6.11"
  },
  "devDependencies": {
    "@vue/cli-plugin-babel": "~4.5.0",
    "@vue/cli-service": "~4.5.0",
    "vue-template-compiler": "^2.6.11"
  }
}
~~~

> Vue CLI3启动项目的命令：`npm run serve`，打包项目的命令`npm run build`

**main.js**

> src文件夹里面放的都是源代码，我们以后的代码都会放到src文件夹里面。源代码的入口就是`main.js`。

~~~javascript
import Vue from 'vue'
import App from './App.vue'

Vue.config.productionTip = false
// 你在发布产品，打包项目，npm run build的时候，它会给你提示信息，告诉你现在构建了什么东西
// 但是我们在执行npm run serve的时候，是不需要这些提示信息的，所以它改成了false
// 这个东西只在产品构建的时候才显示提示信息，在开发阶段不需要显示

new Vue({
  render: h => h(App),
}).$mount('#app')
~~~

### 隐藏的配置去哪了

> Vue CLI3中的`package.json`里面的配置文件很少，绝大多数都被隐藏了，那么这些隐藏的配置去哪里了呢？如果去查看呢？
>
> 有三种方案可以查看：
>
> 第一种：启动服务器(本地vue ui)，在CMD(不管在哪里敲都行)输入`vue ui`指令，它就会帮你启动一个本地服务，这个本地服务可以帮你管理很多的项目。

**vue.config.js**

~~~javascript
module.exports = {
    // 导出你想要修改的配置
    // 到时候它会自动将你写的这个配置和它之前隐藏在node_modules里面的配置进行合并
    // 合并之后你这里写的配置就会有效果了
}
~~~

![](Vue框架入门/178.png)

![](Vue框架入门/179.png)

![](Vue框架入门/180.png)

![](Vue框架入门/181.png)

![](Vue框架入门/182.png)

[前端运行依赖（dependencies）和开发依赖（devDependencies）区分](https://www.cnblogs.com/sue7/p/11759146.html)

> 顾名思义devDenpendencies是开发依赖，也就是开发中所使用的的依赖，**线上生产环境上并不需要他们**。

![](Vue框架入门/183.png)

> Source Map文件可以用于调试代码。

[JavaScript Source Map 详解](http://www.ruanyifeng.com/blog/2013/01/javascript_source_map.html)

![](Vue框架入门/184.png)

### 自定义配置：起别名

![](Vue框架入门/185.png)

# 箭头函数

## 箭头函数的基本使用

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <script>
        // 箭头函数：也是一种定义函数的方式
        // 定义函数的方式1：function
        const aaa = function () {

        }

        // 定义函数的方式2：对象字面量中定义函数
        const obj = {
            bbb: function () {

            },
            ccc() {
                // 这种是ES6的简单写法
            }
        }

        // 定义函数的方式3：ES6中的箭头函数
        // const ddd = (参数列表) =>{

        // }

        const ddd = () => {

        }
    </script>
</body>

</html>
~~~

## 箭头函数的参数和返回值

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <script>
        // 1.参数问题

        // 1.1 放入2个参数
        const sum = (num1, num2) => {
            return num1 + num2;
        }

        // 1.2 放入1个参数(小括号是可以省略的)
        // 1.2写法1
        // const power = (num) => {
        //     return num * num;
        // }

        // 1.2写法2
        const power = num => {
            return num * num;
        }

        // 2.函数中的代码块
        // 2.1 函数代码块中有多行代码时
        const test = () => {
            // 打印hello world
            console.log('hello world');

            // 打印hello vue.js
            console.log('hello vue.js');
        }

        //2.2 函数代码块中只有一行代码
        // 此时不需要写return 和大括号了
        const mul = (num3, num4) => num3 + num4
        console.log(mul(20, 30));

        // const demo = () => {
        //     console.log('hello demo');
        // }

        const demo = () => console.log('hello demo');
        console.log(demo());
        // 最终显示hello demo，然后是undefined(没有返回值，显示undefined)
    </script>
</body>

</html>
~~~

## 箭头函数中this的使用

> 这个可以看我的另一篇博文：《ES6标准入门(第3版)》，里面解释的挺好的。
>
> 但是我这里还是不熟。

~~~javascript
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <script>
        // 什么时候使用箭头函数最多？
        // 当我们把一个函数作为参数传到另一个函数里面的时候，用箭头函数最多
        // setTimeout(function () {
        //     console.log(this);
        //     // setTimeout里的this指向window
        // }, 1000)

        // setTimeout(() => {
        //     // 我们以后这样写，更加简洁
        //     console.log(this);
        //     // 这个也是window
        // }, 1000)

        // const obj = {
        //     aaa() {
        //         // 对象里面直接定义函数这样写(ES6写法)
        //         setTimeout(function () {
        //             console.log(this);
        //             // window
        //         }, 2000)
        //         setTimeout(() => {
        //             console.log(this);
        //             // 打印的是obj对象
        //             // aaa:f
        //         }, 2000)
        //     }
        // }

        // obj.aaa();
        // 问题：箭头函数中的this是如何查找的？
        // 答案：向外层作用域中一层层查找this,直到有this的定义


        const obj = {
            aaa() {
                // 对象里面直接定义函数这样写(ES6写法)
                setTimeout(function () {
                    setTimeout(function () {
                        console.log(this);
                        // window
                    })

                    setTimeout(() => {
                        console.log(this);
                        // window
                    })
                })

                setTimeout(() => {
                    setTimeout(function () {
                        console.log(this);
                        // window
                    })

                    setTimeout(() => {
                        console.log(this);
                        // aaa:f
                    })
                })
            }
        }

        obj.aaa();
    </script>
</body>

</html>
~~~

# Vue Router详解

[前端路由和后端路由有什么优劣？](https://www.zhihu.com/question/305791434)

[什么是前端路由？](https://zhuanlan.zhihu.com/p/38444032)

[什么是外网IP和内网IP?](https://www.zhihu.com/question/27714563)

## 内容概述

![](Vue框架入门/186.png)

## 认识路由

### 什么是路由？

![](Vue框架入门/187.png)

### 后端路由阶段

> 现在淘宝用的应该还是后端渲染，后端渲染对于SEO优化比较好一些。

[什么是前端渲染和后端渲染，前端路由和后端路由](https://zhuanlan.zhihu.com/p/166175382)

[后端渲染html、前端模板渲染html，jquery的html，各有什么区别？](https://www.zhihu.com/question/28725977/answer/42077482)

[web数据是前端渲染还是后端渲染好？](https://www.zhihu.com/question/65214701/answer/228898069)

![](Vue框架入门/188.png)

> 早期在浏览器中输入域名，服务器会直接生成HTML+CSS+一些Java代码，然后Java代码会从数据库读取数据，然后直接传给浏览器，你看到的页面是服务器直接渲染而来的，这个就叫后端渲染(通过特殊的技术，如JSP等)。
>
> 我又在淘宝上点击男装，则又向服务器请求了另一个网页，服务器又会拿到第二个url，服务器会对这个url进行解析，服务器再通过JSP技术(HTML+CSS+Java)将网页渲染好，再将网页传给浏览器端，传过来后前端直接展示最终网页就可以了。
>
> 再点击女装，服务器又再进行上述步骤一次。
>
> 在服务器这边，已经形成了一种映射关系了，服务器在处理这种映射关系。

![](Vue框架入门/189.png)

### 前后端分离阶段

> 单页面富应用阶段(SPA)在前后端分离的基础上，又添加了一层前端路由的概念。

![](Vue框架入门/190.png)

> 你写的所有代码，都是放到**静态资源服务器**里面的。
>
> 你在浏览器输入url,静态资源服务器会给你返回相应的`HTML+CSS+JS`，其中`HTML`和`CSS`浏览器可以直接渲染，而`JS`要由浏览器先执行。
>
> 当浏览器执行JS代码的时候，发现你有API请求，这个时候它才会去API服务器进行相应的请求。
>
> 网页端和手机端淘宝请求的都是同一个服务器，前后端分离的话，服务器就不用管你到底是通过电脑请求的，还是通过手机来请求的了，只要提供对应的AIP接口就可以了。

![](Vue框架入门/191.png)

![](Vue框架入门/192.png)

## 前端路由的规则

> 前后端分离阶段：静态服务器里根据URL的不同放了好几套的`HTML+CSS+JS`
>
> 单页面富应用阶段：只有一个HTML，叫`index.html`，另外的话，有一些CSS和JS,甚至它可能只有一个CSS和一个JS。按照我们的理解，我们只给它开发了一个网页，但是其实不是一个网页。
>
> 举个例子：我们自己开发了一个网站，浏览器输入`codewhy.com`，此时从静态服务器上传入了一套`HTML+CSS+JS`，这一套是全部的资源，全部请求下来了，但是不是所有的内容都被渲染的。
>
> 此时你开发的网站只有3个东西：一个HTML,一个CSS,一个JS。
>
> 如果你的网站上有3个按钮："首页，关于和我的"
>
> 我希望点击第一个按钮时，从请求的全套资源里面抽离出来在首页中需要显示的东西，点击第二，三个按钮同理。
>
> 此时也相当于我虽然是一个网站，但是这个网站也分成了3个页面(首页，关于，我的)，这个必须要有前端路由这个技术来进行支撑。
>
> 前端路由就是用来映射我们浏览器上这种url和我们大的整套资源里面到底要渲染哪个组件的。
>
> 目前的映射关系就是前端路由在管理！！！！！！！！！！！！后端不管了。
>
> 那是怎么管理的？？——用我们的Vue Router，它就会自动帮我们管理了。等我们讲Vue Router的时候，到时候就会配置一套映射关系的，到时会就会一个url对应一个组件的。
>
> 其实，抽取的资源就是Vue里面的一个个的组件。我们可能一个`.vue`文件就是一个页面。

![](Vue框架入门/193.png)

### URL的hash

[路由的hash和history模式](https://juejin.im/post/6844903641531285518)

> 一般情况下，更改url页面会自动进行刷新的。但是我们有2种情况，更改url页面不自动进行刷新，这里是第一种。
>
> 当发现hash(哈希)发生改变的时候，此时浏览器不会向服务器请求一套资源的。它会在我们前端这里有一个路由的映射，会从路由的映射关系里面去找一下这个时候我要渲染哪一个组件。然后它就会把这个组件取出来，并且把这个组件放到我们整个网页上面进行渲染。
>
> 它内部会监听的，它是怎么监听的？这个你先不用去了解了，Vue-Router里面它会自动去监听的。你实在想了解的话可以去读一下Vue-Router的源码。
>
> 我们现在只需要通过Vue-Router来配置路由的关系，它就可以通过我们的这种方案来这里改变url并且让整个网站不发生刷新。

![](Vue框架入门/194.png)

![](Vue框架入门/195.png)

![](Vue框架入门/196.png)

### HTML5的history模式：pushState

[HTML5 History 模式](https://router.vuejs.org/zh/guide/essentials/history-mode.html)

> `pushState`函数有3个参数(对象参数，title参数，url参数)，其中对象参数可以不传，给它一个空的对象；title参数也可以不传，给他一个空的字符串；最主要的是传url参数。

![](Vue框架入门/197.png)

![](Vue框架入门/198.png)

![](Vue框架入门/199.png)

> 栈顶(最后写的那个`history.push({},'','url路径')`)永远显示的是最新的url(即最后压入的url)

![](Vue框架入门/200.png)

> pushState相当于入栈，back相当于出栈。
>
> pushState也可以改变我们的url,同时让我们的页面不发生刷新。

### HTML5的history模式：replaceState

> `replaceState`它是不能点击返回按钮的，就是url进行替换，我杀死你，你消失，我替换掉你。

![](Vue框架入门/201.png)

### HTML5的history模式：go

> 注意：go这个东西只能在`pushState`里面使用，因为它要通过go直接跳到某个栈的位置，要前进返回的，而`replaceState`是没有返回的，所以用不了go。
>
> `history.back()` 只能一步一步的返回url,而go更加的灵活，步子可以迈得更大，并且可以前进也可以后退。
>
> `history.go(-1)`的效果等价于`history.back()`。
>
> `history.go(1)`的效果等价于`history.forward()`。

![](Vue框架入门/202.png)

## Vue Router基础

[从头开始学习vue-router](https://www.jianshu.com/p/4c5c99abb864)

[exports、module.exports和export、export default到底是咋回事](https://segmentfault.com/a/1190000010426778)

### 认识vue-router

![](Vue框架入门/203.png)

### 安装和使用vue-router

> `--save`是因为运行到**客户端**的时候还是要依赖路由的，所以**开发环境**和**运行环境**都要装。
>
> 我们之前`vue create 项目名称`新建项目的时候就安装了Vue Router了，所以这里就不用安装了。

![](Vue框架入门/204.png)

> 到时候一个路径和一个路由组件要产生对应关系，你都没有这个组件，怎么和不同的url产生对应关系呢。

### 创建router实例

![](Vue框架入门/205.png)

### 挂载到Vue实例中

[vue.js文件app.vue是如何调用的](https://segmentfault.com/q/1010000009706842)

![](Vue框架入门/206.png)

#### 基础配置Vue Router代码1.0

**index.js**(位置在src文件夹下的router文件夹里面)

~~~javascript
// 老师新建的index.js，从头给我们写如何创建路由
// index.js是在router文件夹下的(router在src文件夹下)

// 第一步：导入
// 配置路由相关的信息
// 既然你要使用路由，那第一步你就要先导入这个路由
// 这个'vue-router'是安装的框架对象，它里面导出了'vue-router',所以我们可以导入
import VueRouter from 'vue-router'

// 第二步：使用
// 2.1 通过Vue.use(插件),安装插件
// VueRouter就是一个插件
// 只要是插件，必须通过Vue.use来安装这个插件

// 但是我们现在这里(index.js)没有Vue,所以也要导入一下Vue
import Vue from 'vue'
Vue.use(VueRouter)

//2.2 创建VueRouter(路由)对象
// 这个和const app = new Vue({})没啥区别
const routes = [
    // 我们要在这里配置很多映射关系(一个url对应一个组件)后，路由才能起到它的作用
]
const router = new VueRouter({
    // new VueRouter的时候也需要给它传一些东西
    // routers对象里面就是来配置路由和组件之间的映射关系的
    // routes:{
    //     // 但是这样写嵌套关系有点多，所以我们可以在外部写routes
    // }
    routes:routes
    // routes在外面写个数组，里面这样写就可以了
})


//2.3 将router对象传入到Vue实例中
// 这个router对象什么时候才能产生效果呢？你必须把这个对象挂载到Vue实例上(main.js)才行
// 你挂载后怎么才能拿到它呢？————你要导出啊！！！
// 你在index.js里导出，要在main.js里导入！！！
export default router

// 但是我们现在这个路由没有起到具体的效果，因为映射关系我们这里一个也没有
~~~

**main.js**

~~~javascript
import Vue from 'vue'
import App from './App'
// import router from './router/index.js'
// 你在index.js里导出router，要在main.js里导入！！！
// 如果你导入的是一个目录，它会自动找这个文件夹里面的index文件的！！！
import router from './router'
// 所以你也可以这样写
// 后面的index.js可以写，也可以不写
Vue.config.productionTip = false

/* eslint-disable no-new */
new Vue({
  el: '#app',
  router,
  // 这个是简写
// 详细写法为router:router,
// 这个router对象什么时候才能产生效果呢？你必须把这个对象挂载到Vue实例上(main.js)才行
  render: h => h(App)
})
~~~

### 步骤一：创建路由组件

> 以后Vue里面只要写组件，都是以`.vue`文件写的。

[name 在 export default {} 中的作用。](https://segmentfault.com/q/1010000013317296)

![](Vue框架入门/207.png)

### 步骤二：配置组件和路径的映射关系

![](Vue框架入门/208.png)

### 步骤三：使用路由

![](Vue框架入门/209.png)

### 最终效果

![](Vue框架入门/210.png)

#### 基础配置Vue Router代码2.0

**index.js**(位置在src文件夹下的router文件夹里面)

~~~javascript
// 老师新建的index.js，从头给我们写如何创建路由
// index.js是在router文件夹下的(router在src文件夹下)

// 第一步：导入
// 配置路由相关的信息
// 既然你要使用路由，那第一步你就要先导入这个路由
// 这个'vue-router'是安装的框架对象，它里面导出了'vue-router',所以我们可以导入
import VueRouter from 'vue-router'

// 第二步：使用
// 2.1 通过Vue.use(插件),安装插件
// VueRouter就是一个插件
// 只要是插件，必须通过Vue.use来安装这个插件

// 但是我们现在这里(index.js)没有Vue,所以也要导入一下Vue
import Vue from 'vue'

// About.vue和Home.vue这2个组件里面分别导出，我们这里要导入，才能用它们
import Home from '../components/Home'
import About from '../components/About'
// 后面的.vue后缀名可以不写

Vue.use(VueRouter)

//2.2 创建VueRouter(路由)对象
// 这个和const app = new Vue({})没啥区别
const routes = [
    // 我们要在这里配置很多映射关系(一个url对应一个组件)后，路由才能起到它的作用
    {
        // 一个映射关系就是一个对象(配置2个东西：path和component)
        path: '/home',
        // 意思是我浏览器路径里面只要出现/home的话，到时候就显示下面的这个组件
        // 注意：映射关系不是写url:'./home',而是写path!!!!!!
        // 原因：/home它不是一个完整的url。完整的url包括：协议头//主机名//query等其他东西
        component:Home
    },
    {
        // 一个映射关系就是一个对象(配置2个东西：path和component)
        // 因为不可能在页面上同时显示两个路径(home和about只能二选一)
        path: '/about',
        component:About
    }
]
const router = new VueRouter({
    // new VueRouter的时候也需要给它传一些东西
    // routers对象里面就是来配置路由和组件之间的映射关系的
    // routes:{
    //     // 但是这样写嵌套关系有点多，所以我们可以在外部写routes
    // }
    routes:routes
    // routes在外面写个数组，里面这样写就可以了
})


//2.3 将router对象传入到Vue实例中
// 这个router对象什么时候才能产生效果呢？你必须把这个对象挂载到Vue实例上(main.js)才行
// 你挂载后怎么才能拿到它呢？————你要导出啊！！！
// 你在index.js里导出，要在main.js里导入！！！
export default router

// 但是我们现在这个路由没有起到具体的效果，因为映射关系我们这里一个也没有
~~~

**main.js**和配置1.0一样，没有发生变化。

在src文件夹下的components文件夹中新建`Home.vue`文件和`About.vue`文件

**App.vue**

~~~vue
<template>
  <div id="app">
    <!-- app里面的东西必然会被main.js里面render出来 -->

    <!-- <img src="./assets/logo.png"> -->
    <!-- 把之前的helloworld.vue里面的东西都去掉 -->

  

    <!-- 要求：创建2个标签，点击这2个标签，页面会调到特定的url中去 -->
    <!-- 因为想要打开项目就看到这2个标签，所以写到总组件这里 -->

    <!-- <router-view></router-view> -->
    <!-- router-view如果放到上面，那么渲染处理的内容就在"超链接"首页，关于的上面了 -->

    <router-link to="/home" >首页</router-link>
    <router-link to="/about" >关于</router-link>
    <!-- router-link是vue-router里面已经注册过的2个组件 -->
    <!-- 这2个组件是全局组件，所以这2个组件可以在任意的位置用 -->
    <!-- router-link最终会被渲染成a标签的，所以看起来像a标签 -->

    <!-- <button>首页</button> -->
    <!-- <button>关于</button> -->
    <h2>我是App组件</h2>
    <!-- 上面和下面的h2和router-view是同级关系 -->
    <!-- 上下的h2不会随着url切换而消失掉的 -->
    <router-view></router-view>
    <!-- router-view组件用于决定我们之后渲染出来的Home组件或About组件是放在什么位置的-->
    <h2>Hello World</h2>

  </div>
</template>

<script>
export default {
  // 我发现我对export default是真的不熟
  // 我对App.vue也是真的不熟！！！
  // 我们在这里导出了Aoo.vue,在main.js里面导入了App.vue
  // 而且在main.js里面还写了render: h => h(App)，把App.vue里面的东西进行了渲染！！
  // App.vue是总组件！！！！！！！！
  name: 'App'
}
</script>

<style>
/* #app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
/* 把这个也删掉 */
</style>
~~~

**Home.vue**

~~~vue
<template>
    <div>
        <h2>我是首页</h2>
        <p>我是首页内容，哈哈哈</p>
    </div>
</template>

<script>
export default {
    name:'Home'
}
</script>

<style scoped>
      /* 在vue组件中，在style标签上添加scoped属性，以表示它的样式
       作用于当下的模块，很好的实现了样式私有化的目的， */
</style>
~~~

**About.vue**

~~~vue
<template>
     <div>
        <h2>我是关于</h2>
        <p>我是关于内容，呵呵呵</p>
    </div>
</template>

<script>
export default {
    name:'About'
}
</script>

<style scoped>
    /* 在vue组件中，在style标签上添加scoped属性，以表示它的样式
       作用于当下的模块，很好的实现了样式私有化的目的， */
</style>
~~~

## 细节处理

### 路由的默认路径

![](Vue框架入门/211.png)

### HTML5的History模式

> 如果用哈希值表示路径的话，url里面会有井号(#)，看上去非常的别扭。(默认情况下是哈希模式的)
>
> 而HTML5的history模式里面没有井号，看起来很舒服。

![](Vue框架入门/213.png)

![](Vue框架入门/212.png)

### router-link补充

> `router-link`一般情况下会渲染称为a标签，但是有些情况下我们不想渲染成a标签，我们想让它以按钮的形式表现出来。

![](Vue框架入门/214.png)

### 修改linkActiveClass

![](Vue框架入门/216.png)

### 路由代码跳转

![](Vue框架入门/217.png)

#### 基础配置Vue Router代码3.0

**index.js(表示router文件夹的入口)**

~~~javascript
// 老师新建的index.js，从头给我们写如何创建路由
// index.js是在router文件夹下的(router在src文件夹下)

// 第一步：导入
// 配置路由相关的信息
// 既然你要使用路由，那第一步你就要先导入这个路由
// 这个'vue-router'是安装的框架对象，它里面导出了'vue-router',所以我们可以导入
import VueRouter from 'vue-router'

// 第二步：使用
// 2.1 通过Vue.use(插件),安装插件
// VueRouter就是一个插件
// 只要是插件，必须通过Vue.use来安装这个插件

// 但是我们现在这里(index.js)没有Vue,所以也要导入一下Vue
import Vue from 'vue'

// About.vue和Home.vue这2个组件里面分别导出，我们这里要导入，才能用它们
import Home from '../components/Home'
import About from '../components/About'
// 后面的.vue后缀名可以不写

Vue.use(VueRouter)

//2.2 创建VueRouter(路由)对象
// 这个和const app = new Vue({})没啥区别
const routes = [
    // 我们要在这里配置很多映射关系(一个url对应一个组件)后，路由才能起到它的作用
    {
        // 这个配置是为了让用户一打开页面就默认显示首页内容
        path: '/',
        // 先把path里面什么都不写，表示缺省值(里面加上/也是可以的)
        // 然后再把path进行重定向(重新定义一个方向)
        // redirect:重定向
        redirect: '/home'
        // 现在修改路径都是通过哈希值，但是哈希值不好看，里面有井号(#)
        // 路径后面有一个井号总是感觉有一点别扭
    },
    {
        // 一个映射关系就是一个对象(配置2个东西：path和component)
        path: '/home',
        // 意思是我浏览器路径里面只要出现/home的话，到时候就显示下面的这个组件
        // 注意：映射关系不是写url:'./home',而是写path!!!!!!
        // 原因：/home它不是一个完整的url。完整的url包括：协议头//主机名//query等其他东西
        component:Home

    },
    {
        // 一个映射关系就是一个对象(配置2个东西：path和component)
        // 因为不可能在页面上同时显示两个路径(home和about只能二选一)
        path: '/about',
        component:About
    }
]
const router = new VueRouter({
    // new VueRouter的时候也需要给它传一些东西
    // routers对象里面就是来配置路由和组件之间的映射关系的
    // routes:{
    //     // 但是这样写嵌套关系有点多，所以我们可以在外部写routes
    // }
    routes:routes,
    // routes在外面写个数组，里面这样写就可以了

    // 如果用哈希值表示路径的话，url里面会有井号(#)，看上去非常的别扭。
    // (默认情况下是哈希模式的)
    // 而HTML5的history模式里面没有井号，看起来很舒服。
    // 写这一行代码就可以去掉难看的井号了
    mode: 'history',
    linkActiveClass: 'active'
    // outer-link-active这个默认的类名字很长，可以把它的名字改掉，改短一点
    // 但是如果标签很多的话，这样一个一个改太麻烦了，有一个简便方法：在路由里面改(index.js里面改) 
})


//2.3 将router对象传入到Vue实例中
// 这个router对象什么时候才能产生效果呢？你必须把这个对象挂载到Vue实例上(main.js)才行
// 你挂载后怎么才能拿到它呢？————你要导出啊！！！
// 你在index.js里导出，要在main.js里导入！！！
export default router

// 但是我们现在这个路由没有起到具体的效果，因为映射关系我们这里一个也没有
~~~

**App.vue**

~~~vue
<template>
  <div id="app">
    <!-- app里面的东西必然会被main.js里面render出来 -->

    <!-- <img src="./assets/logo.png"> -->
    <!-- 把之前的helloworld.vue里面的东西都去掉 -->

  

    <!-- 要求：创建2个标签，点击这2个标签，页面会调到特定的url中去 -->
    <!-- 因为想要打开项目就看到这2个标签，所以写到总组件这里 -->

    <!-- <router-view></router-view> -->
    <!-- router-view如果放到上面，那么渲染处理的内容就在"超链接"首页，关于的上面了 -->

    <router-link to="/home" >首页</router-link>
    <router-link to="/about" >关于</router-link>

    <!-- router-link是vue-router里面已经注册过的2个组件 -->
    <!-- 这2个组件是全局组件，所以这2个组件可以在任意的位置用 -->

     <router-link to="/home" tag='button'>首页</router-link>
    <router-link to="/about" tag='button'>关于</router-link>
    <!-- router-link最终会被渲染成a标签的，所以看起来像a标签 -->
    <!-- 如果加上tag属性，可以渲染成其他的形式， tag='button'就可以变成button了-->

    <router-link to="/home" replace>首页</router-link>
    <router-link to="/about" replace>关于</router-link>
    <!-- vue-router源码默认用的是pushState,可以点击浏览器上的返回箭头-->
    <!-- 加上replace属性，用户就没法点击返回箭头了 -->

    <router-link to="/home" tag='button' replace active-class="active">首页</router-link>
    <router-link to="/about" tag='button' replace active-class="active">关于</router-link>
    <!--router-link-active这个默认的类名字很长，可以把它的名字改掉，改短一点-->
    <!-- 但是如果标签很多的话，这样一个一个改太麻烦了，有一个简便方法：在路由里面改(index.js里面改) -->

    <button @click="homeClick">首页</button>
    <button @click="aboutClick">关于</button>
    <!-- 不在router-link标签里面，怎么实现点击按钮更改路径？-->
    <!-- 此时我们就需要通过代码的方式来修改路由路径了 -->
    <!-- 注意：不要使用pushState这种方式，不知道行不行，而且它绕过了vue-router，不好！！-->
    <!-- 路由代码跳转 -->
    <!-- 有时候, 页面的跳转可能需要执行对应的JavaScript代码, 
         这个时候, 就可以使用第二种跳转方式了
    -->

    <h2>我是App组件</h2>
    <!-- 上面和下面的h2和router-view是同级关系 -->
    <!-- 上下的h2不会随着url切换而消失掉的 -->
    <router-view></router-view>
    <!-- router-view组件用于决定我们之后渲染出来的Home组件或About组件是放在什么位置的-->
    <h2>Hello World</h2>

  </div>
</template>

<script>
export default {
  // 我发现我对export default是真的不熟
  // 我对App.vue也是真的不熟！！！
  // 我们在这里导出了Aoo.vue,在main.js里面导入了App.vue
  // 而且在main.js里面还写了render: h => h(App)，把App.vue里面的东西进行了渲染！！
  // App.vue是总组件！！！！！！！！
  name: 'App',
  // homeClick和aboutClick方法在这里实现
  methods: {
    homeClick(){
      // this拿到的是当前组件，所有的组件都有一个属性叫router属性
      this.$router.push('/home')
      // push相当于内部在调用pushState方法，也可以用replace方法
      // this.$router.replace('/home')

      // $router这个属性来自于vue-router这个源码里面
      // console.log('homeClick');
    },
    aboutClick(){
      // console.log('aboutClick');
      this.$router.push('/about')
      // this.$router.replace('/about')


    }
  },
}
</script>

<style>
/* #app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
/* 把这个也删掉 */

/* 我点击谁，哪个字体就变成红色 */
/* vue-router有个active-class类，可以自动检测谁活跃(哪个被点哪个就活跃) */
  .router-link-active{
    /* 但是这个默认的类名字很长，可以把它的名字改掉，改短一点 */
    color:#f00;
}

.active{
  background-color: pink;
}
</style>
~~~

### 动态路由

> 你要学会用我们的一些文件夹对我们项目里面多个文件进行划分，不要把所有的东西全部写到一坨。
>
> `$router`和`$router`是两个不一样的东西。` $router`这个属性来自于vue-router这个源码里面，就是`const router = new VueRouter()`里面的router对象，而我们的`$route`不等于`$router`,`$route`指的是当前哪个路由处于活跃状态，你拿到的就是哪个路由。

![](Vue框架入门/218.png)

#### 基础配置Vue Router代码4.0

**User.vue**

~~~javascript
<template>
  <div>
    <h2>我是用户界面</h2>
    <p>我是用户的相关信息，嘿嘿嘿</p>
    <h2>{{userId}}</h2>
    <!-- 注意：$router和$route是两个不一样的属性！！！！！！ -->
    <!-- 因为我们在App.vue里面写的就是userId,所以这里也是写userId -->

    <h2>{{$route.params.abc}}</h2>
    <!-- 这里也一样，不用加this -->
    <!-- 也可以这样直接写 -->

    <h2>{{message}}</h2>
    <!-- 但是这里要用message，直接用message,不用加this的 -->
  </div>
</template>

<script>
  export default{
    name:'User',
    data(){
      message:'zzzzz'
    },
    computed: {
      userId(){
        // return this.$route;
        //$router就是const router = new VueRouter()里面的router对象
        //而我们的$route不等于$router,$route指的是当前哪个路由处于活跃状态，你拿到的就是哪个路由
        return this.$route.params.abc
        // index.js里面写的就是 path: '/user/:abc',,所以这里也写abc
      },
      finalMessage(){
        return this.message
        // 这里要拿messae要用this.message
      }
    },
  }
</script>

<style scoped>
  
</style>
~~~

**App.vue**

~~~javascript
<template>
  <div id="app">
    <!-- app里面的东西必然会被main.js里面render出来 -->

    <!-- <img src="./assets/logo.png"> -->
    <!-- 把之前的helloworld.vue里面的东西都去掉 -->

  

    <!-- 要求：创建2个标签，点击这2个标签，页面会调到特定的url中去 -->
    <!-- 因为想要打开项目就看到这2个标签，所以写到总组件这里 -->

    <!-- <router-view></router-view> -->
    <!-- router-view如果放到上面，那么渲染处理的内容就在"超链接"首页，关于的上面了 -->

    <!-- <router-link to="/home" >首页</router-link>
    <router-link to="/about" >关于</router-link> -->

    <!-- router-link是vue-router里面已经注册过的2个组件 -->
    <!-- 这2个组件是全局组件，所以这2个组件可以在任意的位置用 -->

     <!-- <router-link to="/home" tag='button'>首页</router-link>
    <router-link to="/about" tag='button'>关于</router-link> -->
    <!-- router-link最终会被渲染成a标签的，所以看起来像a标签 -->
    <!-- 如果加上tag属性，可以渲染成其他的形式， tag='button'就可以变成button了-->

    <!-- <router-link to="/home" replace>首页</router-link>
    <router-link to="/about" replace>关于</router-link> -->
    <!-- vue-router源码默认用的是pushState,可以点击浏览器上的返回箭头-->
    <!-- 加上replace属性，用户就没法点击返回箭头了 -->

    <!-- <router-link to="/home" tag='button' replace active-class="active">首页</router-link>
    <router-link to="/about" tag='button' replace active-class="active">关于</router-link> -->
    <!--router-link-active这个默认的类名字很长，可以把它的名字改掉，改短一点-->
    <!-- 但是如果标签很多的话，这样一个一个改太麻烦了，有一个简便方法：在路由里面改(index.js里面改) -->

    <!-- <button @click="homeClick">首页</button>
    <button @click="aboutClick">关于</button> -->
    <!-- 不在router-link标签里面，怎么实现点击按钮更改路径？-->
    <!-- 此时我们就需要通过代码的方式来修改路由路径了 -->
    <!-- 注意：不要使用pushState这种方式，不知道行不行，而且它绕过了vue-router，不好！！-->
    <!-- 路由代码跳转 -->
    <!-- 有时候, 页面的跳转可能需要执行对应的JavaScript代码, 
         这个时候, 就可以使用第二种跳转方式了
    -->

    <h2>我是App组件</h2>
    <!-- 上面和下面的h2和router-view是同级关系 -->
    <!-- 上下的h2不会随着url切换而消失掉的 -->
    <!-- <router-view></router-view> -->
    <!-- router-view组件用于决定我们之后渲染出来的Home组件或About组件是放在什么位置的-->
    <!-- <h2>Hello World</h2> -->

    <!-- 这里老师开始讲动态路由了 -->
    <!-- 上面的全部给注释掉 -->
    <router-link to='/home'>首页</router-link>
    <router-link to='/about'>关于</router-link>
    <!-- <router-link to='/user/zhangsan'>用户</router-link> -->
    <!-- 但是真实开发的时候用户名是动态获取的，肯定不是固定的张三 -->

    <router-link v-bind:to="'/user/' + userId">用户</router-link>
    <!-- 属性里面如何动态绑定下面data里面的数据呢？ -->

    <!-- <img v-bind:src="imgURL" alt=""> -->
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  // 我发现我对export default是真的不熟
  // 我对App.vue也是真的不熟！！！
  // 我们在这里导出了Aoo.vue,在main.js里面导入了App.vue
  // 而且在main.js里面还写了render: h => h(App)，把App.vue里面的东西进行了渲染！！
  // App.vue是总组件！！！！！！！！
  name: 'App',
  data(){
    return {
      userId:'lisi',
      imgURL:'http://www.baidu.com/logo.png'
    }
  },
  // homeClick和aboutClick方法在这里实现
  methods: {
    homeClick(){
      // this拿到的是当前组件，所有的组件都有一个属性叫router属性
      this.$router.push('/home')
      // push相当于内部在调用pushState方法，也可以用replace方法
      // this.$router.replace('/home')

      // $router这个属性来自于vue-router这个源码里面
      // console.log('homeClick');
    },
    aboutClick(){
      // console.log('aboutClick');
      this.$router.push('/about')
      // this.$router.replace('/about')


    }
  },
}
</script>

<style>
/* #app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
/* 把这个也删掉 */

/* 我点击谁，哪个字体就变成红色 */
/* vue-router有个active-class类，可以自动检测谁活跃(哪个被点哪个就活跃) */
  .router-link-active{
    /* 但是这个默认的类名字很长，可以把它的名字改掉，改短一点 */
    color:#f00;
}

.active{
  background-color: pink;
}
</style>
~~~

## 路由懒加载

> 我们之前使用Webpack进行打包，打包文件都在`bundle.js`里面，到时候`bundle.js`文件会非常大。
>
> 请求JS花太长时间的话，页面上会出现短暂的空白的。
>
> 所以我们要对JS文件进行分包，Webpack打包后里面就是分包的。
>
> 开发中我们常见的做法是：一个路由到时候打包一个JS文件。

### 认识路由的懒加载

> 所谓路由懒加载，就是**用到时再加载**。

![](Vue框架入门/219.png)

![](Vue框架入门/220.png)

### 路由懒加载的效果

![](Vue框架入门/221.png)

### 懒加载的方式

![](Vue框架入门/222.png)

#### 基础配置Vue Router代码5.0

**index.js**

~~~javascript
// 老师新建的index.js，从头给我们写如何创建路由
// index.js是在router文件夹下的(router在src文件夹下)

// 第一步：导入
// 配置路由相关的信息
// 既然你要使用路由，那第一步你就要先导入这个路由
// 这个'vue-router'是安装的框架对象，它里面导出了'vue-router',所以我们可以导入
import VueRouter from 'vue-router'

// 第二步：使用
// 2.1 通过Vue.use(插件),安装插件
// VueRouter就是一个插件
// 只要是插件，必须通过Vue.use来安装这个插件

// 但是我们现在这里(index.js)没有Vue,所以也要导入一下Vue
import Vue from 'vue'

// 方法1：一般的导入方式
// About.vue和Home.vue这2个组件里面分别导出，我们这里要导入，才能用它们
// import Home from '../components/Home'
// import About from '../components/About'
// // 后面的.vue后缀名可以不写
// import User from '../components/User'

// 方法2：路由懒加载方式导入
const Home = () => import('../components/Home')
const About = () => import('../components/About')
const User = () => import('../components/User')


Vue.use(VueRouter)

//2.2 创建VueRouter(路由)对象
// 这个和const app = new Vue({})没啥区别
const routes = [
    // 我们要在这里配置很多映射关系(一个url对应一个组件)后，路由才能起到它的作用
    {
        // 这个配置是为了让用户一打开页面就默认显示首页内容
        path: '/',
        // 先把path里面什么都不写，表示缺省值(里面加上/也是可以的)
        // 然后再把path进行重定向(重新定义一个方向)
        // redirect:重定向
        redirect: '/home'
        // 现在修改路径都是通过哈希值，但是哈希值不好看，里面有井号(#)
        // 路径后面有一个井号总是感觉有一点别扭
        // 这个重定向路径比较特殊，把它放上面，以后可以一眼就找到它。
        // 不是说这个东西一定要放到最上面的，只是习惯而已。
    },
    {
        // 一个映射关系就是一个对象(配置2个东西：path和component)
        path: '/home',
        // 意思是我浏览器路径里面只要出现/home的话，到时候就显示下面的这个组件
        // 注意：映射关系不是写url:'./home',而是写path!!!!!!
        // 原因：/home它不是一个完整的url。完整的url包括：协议头//主机名//query等其他东西
        component:Home

    },
    {
        // 一个映射关系就是一个对象(配置2个东西：path和component)
        // 因为不可能在页面上同时显示两个路径(home和about只能二选一)
        path: '/about',
        component:About
    },
    {
        // path: '/user',
        // 这样不行，要想弄成动态路由(用户张三登陆就是/user/zhangsan，李四登陆就是/user/lisi)要向下面这样
        path: '/user/:abc',
        // 只写这个，点击用户的时候，里面的东西渲染不出来了(相当于没有找到这个组件)
        component:User
    }
]
const router = new VueRouter({
    // new VueRouter的时候也需要给它传一些东西
    // routers对象里面就是来配置路由和组件之间的映射关系的
    // routes:{
    //     // 但是这样写嵌套关系有点多，所以我们可以在外部写routes
    // }
    routes:routes,
    // routes在外面写个数组，里面这样写就可以了

    // 如果用哈希值表示路径的话，url里面会有井号(#)，看上去非常的别扭。
    // (默认情况下是哈希模式的)
    // 而HTML5的history模式里面没有井号，看起来很舒服。
    // 写这一行代码就可以去掉难看的井号了
    mode: 'history',
    linkActiveClass: 'active'
    // outer-link-active这个默认的类名字很长，可以把它的名字改掉，改短一点
    // 但是如果标签很多的话，这样一个一个改太麻烦了，有一个简便方法：在路由里面改(index.js里面改) 
})


//2.3 将router对象传入到Vue实例中
// 这个router对象什么时候才能产生效果呢？你必须把这个对象挂载到Vue实例上(main.js)才行
// 你挂载后怎么才能拿到它呢？————你要导出啊！！！
// 你在index.js里导出，要在main.js里导入！！！
export default router

// 但是我们现在这个路由没有起到具体的效果，因为映射关系我们这里一个也没有
~~~

## 路由嵌套

### 认识嵌套路由

![](Vue框架入门/223.png)

### 嵌套路由实现

![](Vue框架入门/224.png)

### 嵌套默认路径

![](Vue框架入门/225.png)

#### 基础配置Vue Router代码6.0(完整版)

> 这个我试了一下不知道为什么没有成功，出了一些问题。
>
> 弄了半个小时，弄好了，也不知道是哪里出了问题，路由这块还要再学一下。

![](Vue框架入门/226.png)

**index.js**

~~~javascript
// 老师新建的index.js，从头给我们写如何创建路由
// index.js是在router文件夹下的(router在src文件夹下)

// 第一步：导入
// 配置路由相关的信息
// 既然你要使用路由，那第一步你就要先导入这个路由
// 这个'vue-router'是安装的框架对象，它里面导出了'vue-router',所以我们可以导入
import VueRouter from 'vue-router'

// 第二步：使用
// 2.1 通过Vue.use(插件),安装插件
// VueRouter就是一个插件
// 只要是插件，必须通过Vue.use来安装这个插件

// 但是我们现在这里(index.js)没有Vue,所以也要导入一下Vue
import Vue from 'vue'

// 方法1：一般的导入方式
// About.vue和Home.vue这2个组件里面分别导出，我们这里要导入，才能用它们
// import Home from '../components/Home'
// import About from '../components/About'
// // 后面的.vue后缀名可以不写
// import User from '../components/User'

// 方法2：路由懒加载方式导入
const Home = () => import('../components/Home')
// 这2个是嵌套路由的懒加载
const HomeNews = () => import('../components/HomeNews')
const HomeMessage = () => import('../components/HomeMessage')

const About = () => import('../components/About')
const User = () => import('../components/User')

// 1.通过Vue.use(插件), 安装插件
Vue.use(VueRouter)

// 2.创建VueRouter对象
// 这个和const app = new Vue({})没啥区别
const routes = [
    // 我们要在这里配置很多映射关系(一个url对应一个组件)后，路由才能起到它的作用
    {
        // 这个配置是为了让用户一打开页面就默认显示首页内容
        path: '',
        // 先把path里面什么都不写，表示缺省值(里面加上/也是可以的)
        // 然后再把path进行重定向(重新定义一个方向)
        // redirect:重定向
        redirect: '/home'
        // 现在修改路径都是通过哈希值，但是哈希值不好看，里面有井号(#)
        // 路径后面有一个井号总是感觉有一点别扭
        // 这个重定向路径比较特殊，把它放上面，以后可以一眼就找到它。
        // 不是说这个东西一定要放到最上面的，只是习惯而已。
    },
    {
        // 一个映射关系就是一个对象(配置2个东西：path和component)
        path: '/home',
        // 意思是我浏览器路径里面只要出现/home的话，到时候就显示下面的这个组件
        // 注意：映射关系不是写url:'./home',而是写path!!!!!!
        // 原因：/home它不是一个完整的url。完整的url包括：协议头//主机名//query等其他东西
        component: Home,
        // 下面是嵌套路由，home下面有news和message两个
        children: [
            {
                path: '',
                redirect:'news'
            },
            {
                path: 'news',
                // 这个是子路由，所以不需要加/
                component: HomeNews
            },
            {
               path: 'message',
               component: HomeMessage
            }
        ]

    },
    {
        // 一个映射关系就是一个对象(配置2个东西：path和component)
        // 因为不可能在页面上同时显示两个路径(home和about只能二选一)
        path: '/about',
        component:About
    },
    {
        // path: '/user',
        // 这样不行，要想弄成动态路由(用户张三登陆就是/user/zhangsan，李四登陆就是/user/lisi)要向下面这样
        path: '/user/:abc',
        // 只写这个，点击用户的时候，里面的东西渲染不出来了(相当于没有找到这个组件)
        component:User
    }
]
const router = new VueRouter({
    // new VueRouter的时候也需要给它传一些东西
    // routers对象里面就是来配置路由和组件之间的映射关系的
    // routes:{
    //     // 但是这样写嵌套关系有点多，所以我们可以在外部写routes
    // }
    routes:routes,
    // routes在外面写个数组，里面这样写就可以了

    // 如果用哈希值表示路径的话，url里面会有井号(#)，看上去非常的别扭。
    // (默认情况下是哈希模式的)
    // 而HTML5的history模式里面没有井号，看起来很舒服。
    // 写这一行代码就可以去掉难看的井号了
    mode: 'history',
    linkActiveClass: 'active'
    // outer-link-active这个默认的类名字很长，可以把它的名字改掉，改短一点
    // 但是如果标签很多的话，这样一个一个改太麻烦了，有一个简便方法：在路由里面改(index.js里面改) 
})


//2.3 将router对象传入到Vue实例中
// 这个router对象什么时候才能产生效果呢？你必须把这个对象挂载到Vue实例上(main.js)才行
// 你挂载后怎么才能拿到它呢？————你要导出啊！！！
// 你在index.js里导出，要在main.js里导入！！！
export default router

// 但是我们现在这个路由没有起到具体的效果，因为映射关系我们这里一个也没有
~~~

**App.vue**

~~~vue
<template>
  <div id="app">
    <!-- app里面的东西必然会被main.js里面render出来 -->

    <!-- <img src="./assets/logo.png"> -->
    <!-- 把之前的helloworld.vue里面的东西都去掉 -->

  

    <!-- 要求：创建2个标签，点击这2个标签，页面会调到特定的url中去 -->
    <!-- 因为想要打开项目就看到这2个标签，所以写到总组件这里 -->

    <!-- <router-view></router-view> -->
    <!-- router-view如果放到上面，那么渲染处理的内容就在"超链接"首页，关于的上面了 -->

    <!-- <router-link to="/home" >首页</router-link>
    <router-link to="/about" >关于</router-link> -->

    <!-- router-link是vue-router里面已经注册过的2个组件 -->
    <!-- 这2个组件是全局组件，所以这2个组件可以在任意的位置用 -->

     <!-- <router-link to="/home" tag='button'>首页</router-link>
    <router-link to="/about" tag='button'>关于</router-link> -->
    <!-- router-link最终会被渲染成a标签的，所以看起来像a标签 -->
    <!-- 如果加上tag属性，可以渲染成其他的形式， tag='button'就可以变成button了-->

    <!-- <router-link to="/home" replace>首页</router-link>
    <router-link to="/about" replace>关于</router-link> -->
    <!-- vue-router源码默认用的是pushState,可以点击浏览器上的返回箭头-->
    <!-- 加上replace属性，用户就没法点击返回箭头了 -->

    <!-- <router-link to="/home" tag='button' replace active-class="active">首页</router-link>
    <router-link to="/about" tag='button' replace active-class="active">关于</router-link> -->
    <!--router-link-active这个默认的类名字很长，可以把它的名字改掉，改短一点-->
    <!-- 但是如果标签很多的话，这样一个一个改太麻烦了，有一个简便方法：在路由里面改(index.js里面改) -->

    <!-- <button @click="homeClick">首页</button>
    <button @click="aboutClick">关于</button> -->
    <!-- 不在router-link标签里面，怎么实现点击按钮更改路径？-->
    <!-- 此时我们就需要通过代码的方式来修改路由路径了 -->
    <!-- 注意：不要使用pushState这种方式，不知道行不行，而且它绕过了vue-router，不好！！-->
    <!-- 路由代码跳转 -->
    <!-- 有时候, 页面的跳转可能需要执行对应的JavaScript代码, 
         这个时候, 就可以使用第二种跳转方式了
    -->

    <h2>我是App组件</h2>
    <!-- 上面和下面的h2和router-view是同级关系 -->
    <!-- 上下的h2不会随着url切换而消失掉的 -->
    <!-- <router-view></router-view> -->
    <!-- router-view组件用于决定我们之后渲染出来的Home组件或About组件是放在什么位置的-->
    <!-- <h2>Hello World</h2> -->

    <!-- 这里老师开始讲动态路由了 -->
    <!-- 上面的全部给注释掉 -->
    <router-link to='/home'>首页</router-link>
    <router-link to='/about'>关于</router-link>
    <!-- <router-link to='/user/zhangsan'>用户</router-link> -->
    <!-- 但是真实开发的时候用户名是动态获取的，肯定不是固定的张三 -->

    <router-link v-bind:to="'/user/' + userId">用户</router-link>
    <!-- 属性里面如何动态绑定下面data里面的数据呢？ -->

    <!-- <img v-bind:src="imgURL" alt=""> -->
    <router-view></router-view>
    <!-- 这个是决定最外层的vue-router展示什么，但是路由还可以嵌套路由，里面的路由也要展示，不通过它 -->
  </div>
</template>

<script>
  // import HomeNews from "./components/HomeNews";
  // import Home from "./components/Home";
export default {
  // 我发现我对export default是真的不熟
  // 我对App.vue也是真的不熟！！！
  // 我们在这里导出了Aoo.vue,在main.js里面导入了App.vue
  // 而且在main.js里面还写了render: h => h(App)，把App.vue里面的东西进行了渲染！！
  // App.vue是总组件！！！！！！！！
  name: 'App',
  data(){
    return {
      userId:'lisi',
      imgURL:'http://www.baidu.com/logo.png'
    }
  },
  // homeClick和aboutClick方法在这里实现
  methods: {
    homeClick(){
      // this拿到的是当前组件，所有的组件都有一个属性叫router属性
      this.$router.push('/home')
      // push相当于内部在调用pushState方法，也可以用replace方法
      // this.$router.replace('/home')

      // $router这个属性来自于vue-router这个源码里面
      // console.log('homeClick');
    },
    aboutClick(){
      // console.log('aboutClick');
      this.$router.push('/about')
      // this.$router.replace('/about')
    }
  },
}
</script>

<style>
/* #app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
/* 把这个也删掉 */

/* 我点击谁，哪个字体就变成红色 */
/* vue-router有个active-class类，可以自动检测谁活跃(哪个被点哪个就活跃) */
  .router-link-active{
    /* 但是这个默认的类名字很长，可以把它的名字改掉，改短一点 */
    color:#f00;
}

.active{
  background-color: pink;
}
</style>
~~~

**main.js**

~~~javascript
import Vue from 'vue'
import App from './App'
// import router from './router/index.js'
// 你在index.js里导出router，要在main.js里导入！！！
// 如果你导入的是一个目录，它会自动找这个文件夹里面的index文件的！！！
import router from './router'
// 所以你也可以这样写
// 后面的index.js可以写，也可以不写
Vue.config.productionTip = false

/* eslint-disable no-new */
new Vue({
  el: '#app',
  router,
  // 这个是简写
// 详细写法为router:router,
// 这个router对象什么时候才能产生效果呢？你必须把这个对象挂载到Vue实例上(main.js)才行
  render: h => h(App)
})
~~~

**Home.vue**

~~~javascript
<template>
    <div>
        <h2>我是首页</h2>
        <p>我是首页内容，哈哈哈</p>
        <router-link to="/home/news">新闻</router-link>
        <router-link to="/home/message">消息</router-link>
        <!-- 这2个自路由还是设置在什么情况下显示，所以还要单独弄个router-link -->
        <!-- 注意：这里的router-link应该写上一个完整的路径 -->
        <router-view></router-view>
        <!-- Home底下有2个自路由，它们的显示是单独通过这个显示的 -->
    </div>
</template>

<script>
export default {
    name:'Home'
}
</script>

<style scoped>
      /* 在vue组件中，在style标签上添加scoped属性，以表示它的样式
       作用于当下的模块，很好的实现了样式私有化的目的， */
</style>
~~~

**About.vue**

~~~vue
<template>
     <div>
        <h2>我是关于</h2>
        <p>我是关于内容，呵呵呵</p>
    </div>
</template>

<script>
export default {
    name:'About'
}
</script>

<style scoped>
    /* 在vue组件中，在style标签上添加scoped属性，以表示它的样式
       作用于当下的模块，很好的实现了样式私有化的目的， */
</style>
~~~

~~~javascript
<template>
  <div>
    <h2>我是用户界面</h2>
    <p>我是用户的相关信息，嘿嘿嘿</p>
    <h2>{{userId}}</h2>
    <!-- 注意：$router和$route是两个不一样的属性！！！！！！ -->
    <!-- 因为我们在App.vue里面写的就是userId,所以这里也是写userId -->

    <h2>{{$route.params.abc}}</h2>
    <!-- 这里也一样，不用加this -->
    <!-- 也可以这样直接写 -->

    <!-- <h2>{{message}}</h2> -->
    <!-- 但是这里要用message，直接用message,不用加this的 -->
  </div>
</template>

<script>
  export default{
    name:'User',
    // data(){
    //   message:'zzzzz'
    // },
    computed: {
      userId(){
        // return this.$route;
        //$router就是const router = new VueRouter()里面的router对象
        //而我们的$route不等于$router,$route指的是当前哪个路由处于活跃状态，你拿到的就是哪个路由
        return this.$route.params.abc
        // index.js里面写的就是 path: '/user/:abc',,所以这里也写abc
      },
      // finalMessage(){
      //   return this.message
      //   // 这里要拿messae要用this.message
      // }
    }
  }
</script>

<style scoped>
  
</style>
~~~

**HomeMessage.vue**

~~~vue
<template>
  <div>
    <ul>
      <li>消息1</li>
      <li>消息2</li>
      <li>消息3</li>
      <li>消息4</li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: "HomeMessage"
  }
</script>

<style scoped>

</style>
~~~

**HomeNews**

~~~vue
<template>
  <div>
    <ul>
      <li>新闻1</li>
      <li>新闻2</li>
      <li>新闻3</li>
      <li>新闻4</li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: "HomeNews"
  }
</script>

<style scoped>

</style>
~~~

## 传递参数

### 准备工作

![](Vue框架入门/227.png)

### 传递参数的方式

> 传简单的东西用`params`，传复杂的东西用`query`，因为它是一个对象，可以传的东西有很多。

![](Vue框架入门/228.png)

### 传递参数方式一：`<router-link>`

![](Vue框架入门/229.png)

### 传递参数方式二：JavaScript代码

![](Vue框架入门/230.png)

### 获取参数

![](Vue框架入门/231.png)

### \$route和$router是有区别的

> 老师在这节课里讲了一些vue router的源码，听得云里雾里，说到底还是代码写的太少，一点都不熟啊。

![](Vue框架入门/232.png)

## 导航守卫

### 为什么使用导航守卫

![](Vue框架入门/233.png)

### 导航守卫使用

![](Vue框架入门/234.png)

### 导航守卫补充

![](Vue框架入门/235.png)

#### 基础配置Vue Router代码7.0

**index.js**

~~~javascript
// 老师新建的index.js，从头给我们写如何创建路由
// index.js是在router文件夹下的(router在src文件夹下)

// 第一步：导入
// 配置路由相关的信息
// 既然你要使用路由，那第一步你就要先导入这个路由
// 这个'vue-router'是安装的框架对象，它里面导出了'vue-router',所以我们可以导入
import VueRouter from 'vue-router'

// 第二步：使用
// 2.1 通过Vue.use(插件),安装插件
// VueRouter就是一个插件
// 只要是插件，必须通过Vue.use来安装这个插件

// 但是我们现在这里(index.js)没有Vue,所以也要导入一下Vue
import Vue from 'vue'

// 方法1：一般的导入方式
// About.vue和Home.vue这2个组件里面分别导出，我们这里要导入，才能用它们
// import Home from '../components/Home'
// import About from '../components/About'
// // 后面的.vue后缀名可以不写
// import User from '../components/User'

// 方法2：路由懒加载方式导入
const Home = () => import('../components/Home')
// 这2个是嵌套路由的懒加载
const HomeNews = () => import('../components/HomeNews')
const HomeMessage = () => import('../components/HomeMessage')

const About = () => import('../components/About')
const User = () => import('../components/User')
const Profile = () => import('../components/Profile')

// 1.通过Vue.use(插件), 安装插件
Vue.use(VueRouter)

// 2.创建VueRouter对象
// 这个和const app = new Vue({})没啥区别
const routes = [
    // 我们要在这里配置很多映射关系(一个url对应一个组件)后，路由才能起到它的作用
    {
        // 这个配置是为了让用户一打开页面就默认显示首页内容
        path: '',
        // 先把path里面什么都不写，表示缺省值(里面加上/也是可以的)
        // 然后再把path进行重定向(重新定义一个方向)
        // redirect:重定向
        redirect: '/home',
        // 现在修改路径都是通过哈希值，但是哈希值不好看，里面有井号(#)
        // 路径后面有一个井号总是感觉有一点别扭
        // 这个重定向路径比较特殊，把它放上面，以后可以一眼就找到它。
        // 不是说这个东西一定要放到最上面的，只是习惯而已。
      
    },
    {
        // 一个映射关系就是一个对象(配置2个东西：path和component)
        path: '/home',
        // 意思是我浏览器路径里面只要出现/home的话，到时候就显示下面的这个组件
        // 注意：映射关系不是写url:'./home',而是写path!!!!!!
        // 原因：/home它不是一个完整的url。完整的url包括：协议头//主机名//query等其他东西
        component: Home,
        // 下面是嵌套路由，home下面有news和message两个
         meta: {
            title: '首页'
            // 加上一个元数据
        },
        children: [
            {
                path: '',
                redirect:'news'
            },
            {
                path: 'news',
                // 这个是子路由，所以不需要加/
                component: HomeNews
            },
            {
               path: 'message',
               component: HomeMessage
            }
        ]

    },
    {
        // 一个映射关系就是一个对象(配置2个东西：path和component)
        // 因为不可能在页面上同时显示两个路径(home和about只能二选一)
        path: '/about',
        component: About,
          meta: {
            title: '关于'
            // 加上一个元数据
        },
          beforeEnter: (to, from, next) => {
              console.log('about beforeEnter');
              next()
          }
    },
    {
        // path: '/user',
        // 这样不行，要想弄成动态路由(用户张三登陆就是/user/zhangsan，李四登陆就是/user/lisi)要向下面这样
        path: '/user/:id',
        // 只写这个，点击用户的时候，里面的东西渲染不出来了(相当于没有找到这个组件)
        component: User,
          meta: {
            title: '用户'
            // 加上一个元数据
        }
    },
    {
        path: '/profile',
        component: Profile,
         meta: {
            title: '档案'
            // 加上一个元数据
        }
    }
]
const router = new VueRouter({
    // new VueRouter的时候也需要给它传一些东西
    // routers对象里面就是来配置路由和组件之间的映射关系的
    // routes:{
    //     // 但是这样写嵌套关系有点多，所以我们可以在外部写routes
    // }
    routes:routes,
    // routes在外面写个数组，里面这样写就可以了

    // 如果用哈希值表示路径的话，url里面会有井号(#)，看上去非常的别扭。
    // (默认情况下是哈希模式的)
    // 而HTML5的history模式里面没有井号，看起来很舒服。
    // 写这一行代码就可以去掉难看的井号了
    mode: 'history',
    linkActiveClass: 'active'
    // outer-link-active这个默认的类名字很长，可以把它的名字改掉，改短一点
    // 但是如果标签很多的话，这样一个一个改太麻烦了，有一个简便方法：在路由里面改(index.js里面改) 
})

//2.3 将router对象传入到Vue实例中
// 这个router对象什么时候才能产生效果呢？你必须把这个对象挂载到Vue实例上(main.js)才行
// 你挂载后怎么才能拿到它呢？————你要导出啊！！！
// 你在index.js里导出，要在main.js里导入！！！

// 这里老师开始讲全局导航守卫的知识了
// 前置守卫(guard)——也叫前置钩子(hook)——回调这个东西很多时候也叫钩子
router.beforeEach((to, from, next) => { 
    // 从from跳转到to
    document.title = to.matched[0].meta.title;
    // console.log(to);
    document.title = to.meta.title;
    // console.log('+++++++++++++');
    next()
})

// 后置钩子(hook)
// router.afterEach((to, from) => { 
//     console.log('------------');
// })
// 3.将router对象传入到Vue实例
export default router

// 但是我们现在这个路由没有起到具体的效果，因为映射关系我们这里一个也没有
~~~

> meta：元数据(描述数据的数据)

## keep-alive

### keep-alive遇见vue-router

> 我先点击首页里的消息，然后再点击关于，最后再点击首页，发现下面显示的是新闻，而不是我之前点击的消息，即组件内部的状态没有被保留下来。
>
> 当我再点击首页切换回来的时候，它会重新创建一个新的组件。
>
> 而如果你希望它把状态保留下来，不希望它重新创建新的组件，这个时候，你就可以使用一个东西：`keep-alive`

![](Vue框架入门/236.png)

#### 基础配置Vue Router代码8.0

**Home.vue**

~~~vue
<template>
    <div>
        <h2>我是首页</h2>
        <p>我是首页内容，哈哈哈</p>
        <router-link to="/home/news">新闻</router-link>
        <router-link to="/home/message">消息</router-link>
        <!-- 这2个自路由还是设置在什么情况下显示，所以还要单独弄个router-link -->
        <!-- 注意：这里的router-link应该写上一个完整的路径 -->
        <router-view></router-view>
        <!-- Home底下有2个自路由，它们的显示是单独通过这个显示的 -->
        <h2>{{message}}</h2>
    </div>
</template>

<script>
export default {
    name:'Home',
    data(){
        return {
            message:'你好啊',
            path:'/home/news'
        }
    },
    // 老师在这里又复习了一些生命周期函数
    created() {
        console.log('home created');
        document.title = '首页';
        this.$router.push('/home/news')
    },
    destroyed() {
        console.log('home destroyed');
    },
    // 这2个函数，只有该组件被保持了状态，使用了keep-alive时才有效
    activated() {
        // 这个表示活跃的
        console.log('actived');
        this.$router.push(this.path);
    },
    deactivated() {
        // 这个表示不活跃的
        console.log('deactived');
        // console.log(this.$route.path);
        // this.path = this.$route.path;
    },
    // mounted() {
    //       //mouted:挂载的意思 
    //     console.log('mounted')
    // },
    // updated() {
    //     console.log('updated')
    // },
    beforeRouteLeave (to, from, next) {
        // 最后使用导航守卫来解决吧
        console.log(this.$route.path);
        this.path = this.$route.path;
        next()
    }
}
</script>

<style scoped>
      /* 在vue组件中，在style标签上添加scoped属性，以表示它的样式
       作用于当下的模块，很好的实现了样式私有化的目的， */
</style>
~~~

## 案例：TabBar练习

[我对CSS vertical-align的一些理解与认识（一）](https://www.zhangxinxu.com/wordpress/2010/05/%E6%88%91%E5%AF%B9css-vertical-align%E7%9A%84%E4%B8%80%E4%BA%9B%E7%90%86%E8%A7%A3%E4%B8%8E%E8%AE%A4%E8%AF%86%EF%BC%88%E4%B8%80%EF%BC%89/)

### TabBar实现思路

![](Vue框架入门/237.png)

![](Vue框架入门/239.png)

### 代码实现

![](Vue框架入门/240.png)

#### **TabBar代码1.0之基本结构搭建**

![](Vue框架入门/238.png)

**main.js**

~~~javascript
import Vue from 'vue'
import App from './App'
import router from './router'

Vue.config.productionTip = false

/* eslint-disable no-new */
new Vue({
  el: '#app',
  router,
  render: h => h(App)
})

// require('./assets/css/base.css')
// 但是main.js里面以后尽量不要写这种代码
// 这种代码只是对样式的一种引用，写到这里的话，看起来就有点乱了。
// 所以最好把这个放到App.vue里面的style里面引用比较好

// 因为main.js一开始渲染的话就是渲染的App.vue
~~~

**App.vue**

~~~vue
<template>
  <div id="app">
      <!--如果你没有封装的思想的话可能会这样做-->
      <div id="tab-bar">
        <div class="tab-bar-item">首页</div>
        <div class="tab-bar-item">分类</div>
        <div class="tab-bar-item">购物车</div>
        <div class="tab-bar-item">我的</div>
        <!-- 左上角，并且没有挨在边上。 -->
        <!-- 因为它默认有一个margin:8px -->
      </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  components:{

  }
}
</script>

<style>
/* 让字体挨着边 */
/* 在App.vue里面写，不在main.js里面写 */
/* 这样写也是可以的，但是如果我要初始化的样式非常多，到时候把所有初始化的样式都写到这里会很拥挤 */
/* 所以，最终，我们还是在assets-css里面新建一个base.css，把初始化样式都写在里面吧 */
/* 所以我们在App.vue里面动态的引用base.css样式文件，而不是在main.js里面引用 */
/* 但是不能通过" require('./assets/css/base.css'"这样引用，会报错 */
/* 要通过@import来引用base.css样式 */
 
  /* 写法1： */
  @import url('assets/css/base.css');

  /* 写法2： */
  /* @import "./assets/css/base.css" */

  /* 如果你在JS里面引入.css文件直接使用import文件就可以了 */
  /* 但是因为在style里面做这件事情，它有一个固定的格式，要用@import */

  /* 写法3：这样写不好，初始化样式要单独放在一个文件里面比较好*/
   /* body{
     padding: 0;
     margin: 0;
  
  } */

  /* 接下来使用flex布局让它们四个到下面来，并且水平居中布局 */
  #tab-bar{
    display:flex;
    background-color:#f6f6f6;

    /* 让它们4个跑到下面去 */
    position: fixed;
    left: 0;
    right: 0;
    bottom: 0;

    /* 弄个阴影，有个过渡效果 */
    box-shadow: 0 -1px 1px rgba(100, 100, 100, .2);
  }

  .tab-bar-item{
    flex: 1;
    /* 这个表示均等分 */
    text-align: center;
    /* 一般tab-bar的高度是49px——移动端，可以网上搜的 */
    height: 49px;
  }
</style>
~~~

**base.css**

~~~css
body {
  padding: 0;
  margin: 0;
  /* body默认有一个margin为8px，没有挨着边 */
  /* 但是这个东西不会生效的，因为webpack在打包的时候是从入口开始的 */
  /* 我们要用这个东西，要在main.js里引入它 */
}
~~~

#### **TabBar代码2.0之TabBar和TabBarItem组件封装**

> `main.js`和1.0一样，就不写了

![](Vue框架入门/241.png)

**App.vue**

~~~javascript
<template>
  <div id="app">
      <!--如果你没有封装的思想的话可能会这样做-->
      <!-- <div id="tab-bar">
        <div class="tab-bar-item">首页</div>
        <div class="tab-bar-item">分类</div>
        <div class="tab-bar-item">购物车</div>
        <div class="tab-bar-item">我的</div> -->
        <!-- 左上角，并且没有挨在边上。 -->
        <!-- 因为它默认有一个margin:8px -->
        <!-- 但是这样写不好，没有复用性，别的项目要用这个还要把它拷贝进去 -->
        <!-- 而且不仅你这里要拷贝，下面的样式也要拷贝，不好 -->
        <!-- 所以我们最好把这个东西封装成一个独立的组件 -->
        <!--我们在components这里新建一个文件夹tabbar(components文件夹里面以后要封装很多组件的)-->
        <!-- 如果所有的组件全部放在components文件夹里面管理起来太乱了 -->
        <!-- 所以我针对某个功能，单独建立一个个文件夹，这样管理起来就比较好 -->
      <!-- </div> -->
      <tab-bar>
      <!-- 在App.vue里面刚开始用的是TabBar -->

        <!-- <div class="tab-bar-item">
            <img src="../../assets/img/tabbar/home.svg" alt=""> -->
            <!-- 但是这样写路径太恶心了 -->
            <!-- 我们可以给路径起别名，后面讲 -->
              <!-- 首页
          </div>
        <div class="tab-bar-item">
            <img src="../../assets/img/tabbar/home.svg" alt="">
            分类
        </div>
        <div class="tab-bar-item">
            <img src="../../assets/img/tabbar/home.svg" alt="">
            <div>购物车</div>
        </div>
        <div class="tab-bar-item">
            <img src="../../assets/img/tabbar/home.svg" alt="">
            我的
        </div> -->
        <!-- 这里面的代码到时候还会继续抽取的，放心 -->
          <tab-bar-item>
              <img slot="item-icon" src="./assets/img/tabbar/home.svg" alt="">
              <div slot="item-text">首页 </div>
          </tab-bar-item>

          <tab-bar-item>
              <img slot="item-icon" src="./assets/img/tabbar/category.svg" alt="">
              <div slot="item-text">分类</div>
          </tab-bar-item>

          <tab-bar-item>
              <img slot="item-icon" src="./assets/img/tabbar/shopcart.svg" alt="">
              <div slot="item-text">购物车</div>
          </tab-bar-item>

          <tab-bar-item>
              <img slot="item-icon" src="./assets/img/tabbar/profile.svg" alt="">
              <div slot="item-text">我的</div>
          </tab-bar-item>
          <!-- 这个代码又有点多了，到时候可以再抽到另一个文件里面 -->
      </tab-bar>
    <!-- 这个组件标签名tab-bar是哪里来的呢？？？？ -->
    <!-- 我试了一下：Tab-Bar也是可以的,tab-Bar也是可以的 -->
  </div>
</template>

<script>
import TabBar from'./components/tabbar/TabBar'
import TabBarItem from './components/tabbar/TabBarItem'
// 第一步先把TabBar组件导入
export default {
  name: 'App',
  components:{
    // 第二步要在components组件里注册
    // 只有注册过了才能在模版里面使用
    TabBar,
    TabBarItem
  }
}
</script>

<style>
/* 让字体挨着边 */
/* 在App.vue里面写，不在main.js里面写 */
/* 这样写也是可以的，但是如果我要初始化的样式非常多，到时候把所有初始化的样式都写到这里会很拥挤 */
/* 所以，最终，我们还是在assets-css里面新建一个base.css，把初始化样式都写在里面吧 */
/* 所以我们在App.vue里面动态的引用base.css样式文件，而不是在main.js里面引用 */
/* 但是不能通过" require('./assets/css/base.css'"这样引用，会报错 */
/* 要通过@import来引用base.css样式 */
 
  /* 写法1： */
  @import url('assets/css/base.css');

  /* 写法2： */
  /* @import "./assets/css/base.css" */

  /* 如果你在JS里面引入.css文件直接使用import文件就可以了 */
  /* 但是因为在style里面做这件事情，它有一个固定的格式，要用@import */

  /* 写法3：这样写不好，初始化样式要单独放在一个文件里面比较好*/
   /* body{
     padding: 0;
     margin: 0;
  
  } */

  /* 接下来使用flex布局让它们四个到下面来，并且水平居中布局 */
  /* #tab-bar{
    display:flex;
    background-color:#f6f6f6; */

    /* 让它们4个跑到下面去 */
    /* position: fixed;
    left: 0;
    right: 0;
    bottom: 0; */

    /* 弄个阴影，有个过渡效果 */
    /* box-shadow: 0 -1px 1px rgba(100, 100, 100, .2);
  } */

  /* .tab-bar-item{
    flex: 1; */
    /* 这个表示均等分 */
    /* text-align: center; */
    /* 一般tab-bar的高度是49px——移动端，可以网上搜的 */
    /* height: 49px;
  } */

   /* .tab-bar-item img{ */
      /* 图片有了，但是太大了，要给它改一下大小 */
      /* width: 24px;
      height: 24px;
  } */

  /* 这里style代码给它挪个地方到TabBar.vue里面去 */
  /* 之后再挪到TabBarItem组件里面去 */
</style>
~~~

**TabBar.vue**

~~~vue
<template>
    <div id="tab-bar">
        <!-- <div class="tab-bar-item">
            <img src="../../assets/img/tabbar/home.svg" alt=""> -->
            <!-- 但是这样写路径太恶心了 -->
            <!-- 我们可以给路径起别名，后面讲 -->
            <!-- 首页
        </div>
        <div class="tab-bar-item">
            <img src="../../assets/img/tabbar/home.svg" alt="">
            分类
        </div>
        <div class="tab-bar-item">
            <img src="../../assets/img/tabbar/home.svg" alt="">
            <div>购物车</div>
        </div>
        <div class="tab-bar-item">
            <img src="../../assets/img/tabbar/home.svg" alt="">
            我的
        </div> -->
        <!-- 这里面只有文字，文字下面的4张图片还没有 -->
        <!-- 我们把图片放到img文件夹里面单独的tabbar文件夹下面 -->
        <!-- 不要为了省事把所有的图片都放到img一个文件夹里面 -->
        <slot></slot>
        <!-- 上面的全部不要，只弄一个插槽即可 -->
    </div>

    <!-- 但是我这个TabBar组件里面的东西太杂了，这个是一个大组件，里面的明细我不应该关系的 -->
    <!-- TabBar组件应该只负责TabBar自己的东西：div id="tab-bar"和#tab-bar{}这2个-->
    <!-- 至于item相关的东西不应该交给我管理 -->
    <!-- 全部交给TabBar管理的话，最后封装的组件就会乱七八糟的 -->
    <!-- 所以TabBar封装完之后只给它弄一个插槽(slot)就可以了 -->
</template>

<script>
export default {
    name:'TabBar'
}
</script>

<style scoped>
#tab-bar{
    display:flex;
    background-color:#f6f6f6;

    /* 让它们4个跑到下面去 */
    position: fixed;
    left: 0;
    right: 0;
    bottom: 0;

    /* 弄个阴影，有个过渡效果 */
    box-shadow: 0 -1px 1px rgba(100, 100, 100, .2);
  }

/* .tab-bar-item{
    flex: 1; */
    /* 这个表示均等分 */
    /* text-align: center; */
    /* 一般tab-bar的高度是49px——移动端，可以网上搜的 */
    /* height: 49px;
  } */

  /* .tab-bar-item img{ */
      /* 图片有了，但是太大了，要给它改一下大小 */
      /* width: 24px;
      height: 24px;
  } */
</style>
~~~

**TabBarItem.vue**

~~~vue
<template>
<!-- 所有的item都展示同一个图片，同一个文字 -->
<!-- 所以不要写死，用插槽 -->
    <div class="tab-bar-item">
        <slot name="item-icon"></slot>
        <slot name="item-text"></slot>
        <!-- <img src="../../assets/img/tabbar/home.svg" alt=""> -->
        <!-- 图片最下面会多3个像素，导致图片和文字之间有空隙 -->
        <!-- <div>首页 </div> -->
        <!-- 但是这2个东西(图片和文字)你是不能写死的 -->
        <!-- 不可以的话搞插槽就可以了 -->
    </div>
</template>

<script>
export default {
    name:'TabBarItem'
}
</script>

<style scoped>
    /* 再把App.vue里面关于tab-bar-item的样式放到这里来 */
     .tab-bar-item{
    flex: 1;
    /* 这个表示均等分 */
    text-align: center;
    /* 一般tab-bar的高度是49px——移动端，可以网上搜的 */
    height: 49px;
    font-size: 14px;
  }

   .tab-bar-item img{
      /* 图片有了，但是太大了，要给它改一下大小 */
      width: 24px;
      height: 24px;
      margin-top: 3px;
      vertical-align: middle;
    /* 图片最下面会多3个像素，导致图片和文字之间有空隙 */
    margin-bottom: 2px;
  }
</style>
~~~

#### TabBar代码3.0之传入active图片

**TabBarItem.vue**

~~~vue
<template>
<!-- 所有的item都展示同一个图片，同一个文字 -->
<!-- 所以不要写死，用插槽 -->
    <div class="tab-bar-item">
        <!-- <slot v-if="!isActive" name="item-icon"></slot>
        <slot v-else name="item-icon-active"></slot> -->

        <div v-if="!isActive"><slot name="item-icon"></slot></div>
        <div v-else><slot name="item-icon-active"></slot></div>
        <!-- 插槽这种东西很有可能某些属性就被替换掉，所以上面这么写不保险，按下面的来写 -->
        <!-- v-if和v-else都写到div里面，不写到插槽里面比较好 -->
        
        <!-- 这2个插槽最终只会展示一个 -->
        <!-- <slot :class="{active:isActive}" name="item-text"></slot> -->
        <div :class="{active:isActive}">
          <slot name="item-text"></slot>
        </div>
        <!-- 这样写就可以了 -->
        <!-- 插槽这里最终会被<div slot="item-text">首页 </div>替换掉 -->
        <!-- 所以在插槽里写:class没有用 -->
        <!-- <img src="../../assets/img/tabbar/home.svg" alt=""> -->
        <!-- 图片最下面会多3个像素，导致图片和文字之间有空隙 -->
        <!-- <div>首页 </div> -->
        <!-- 但是这2个东西(图片和文字)你是不能写死的 -->
        <!-- 不可以的话搞插槽就可以了 -->
    </div>
</template>

<script>
export default {
    name:'TabBarItem',
    data(){
     return {
        isActive:true
     }
    }
}
</script>

<style scoped>
    /* 再把App.vue里面关于tab-bar-item的样式放到这里来 */
     .tab-bar-item{
    flex: 1;
    /* 这个表示均等分 */
    text-align: center;
    /* 一般tab-bar的高度是49px——移动端，可以网上搜的 */
    height: 49px;
    font-size: 14px;
  }

   .tab-bar-item img{
      /* 图片有了，但是太大了，要给它改一下大小 */
      width: 24px;
      height: 24px;
      margin-top: 3px;
      vertical-align: middle;
    /* 图片最下面会多3个像素，导致图片和文字之间有空隙 */
    margin-bottom: 2px;
  }

  .active{
    color: red;
  }
</style>
~~~

**App.vue**

~~~vue
<template>
  <div id="app">
      <!--如果你没有封装的思想的话可能会这样做-->
      <!-- <div id="tab-bar">
        <div class="tab-bar-item">首页</div>
        <div class="tab-bar-item">分类</div>
        <div class="tab-bar-item">购物车</div>
        <div class="tab-bar-item">我的</div> -->
        <!-- 左上角，并且没有挨在边上。 -->
        <!-- 因为它默认有一个margin:8px -->
        <!-- 但是这样写不好，没有复用性，别的项目要用这个还要把它拷贝进去 -->
        <!-- 而且不仅你这里要拷贝，下面的样式也要拷贝，不好 -->
        <!-- 所以我们最好把这个东西封装成一个独立的组件 -->
        <!--我们在components这里新建一个文件夹tabbar(components文件夹里面以后要封装很多组件的)-->
        <!-- 如果所有的组件全部放在components文件夹里面管理起来太乱了 -->
        <!-- 所以我针对某个功能，单独建立一个个文件夹，这样管理起来就比较好 -->
      <!-- </div> -->
      <tab-bar>
      <!-- 在App.vue里面刚开始用的是TabBar -->

        <!-- <div class="tab-bar-item">
            <img src="../../assets/img/tabbar/home.svg" alt=""> -->
            <!-- 但是这样写路径太恶心了 -->
            <!-- 我们可以给路径起别名，后面讲 -->
              <!-- 首页
          </div>
        <div class="tab-bar-item">
            <img src="../../assets/img/tabbar/home.svg" alt="">
            分类
        </div>
        <div class="tab-bar-item">
            <img src="../../assets/img/tabbar/home.svg" alt="">
            <div>购物车</div>
        </div>
        <div class="tab-bar-item">
            <img src="../../assets/img/tabbar/home.svg" alt="">
            我的
        </div> -->
        <!-- 这里面的代码到时候还会继续抽取的，放心 -->
          <tab-bar-item>
              <img slot="item-icon" src="./assets/img/tabbar/home.svg" alt="">
              <img slot="item-icon-active" src="./assets/img/tabbar/home_active.svg" alt="">
              <div slot="item-text">首页 </div>
          </tab-bar-item>

          <tab-bar-item>
              <img slot="item-icon" src="./assets/img/tabbar/category.svg" alt="">
              <img slot="item-icon-active" src="./assets/img/tabbar/category_active.svg" alt="">
              <div slot="item-text">分类</div>
          </tab-bar-item>

          <tab-bar-item>
              <img slot="item-icon" src="./assets/img/tabbar/shopcart.svg" alt="">
              <img slot="item-icon-active" src="./assets/img/tabbar/shopcart_active.svg" alt="">
              <div slot="item-text">购物车</div>
          </tab-bar-item>

          <tab-bar-item>
              <img slot="item-icon" src="./assets/img/tabbar/profile.svg" alt="">
              <img slot="item-icon-active" src="./assets/img/tabbar/profile_active.svg" alt="">
              <div slot="item-text">我的</div>
          </tab-bar-item>
          <!-- 这个代码又有点多了，到时候可以再抽到另一个文件里面 -->
      </tab-bar>
    <!-- 这个组件标签名tab-bar是哪里来的呢？？？？ -->
    <!-- 我试了一下：Tab-Bar也是可以的,tab-Bar也是可以的 -->
  </div>
</template>

<script>
import TabBar from'./components/tabbar/TabBar'
import TabBarItem from './components/tabbar/TabBarItem'
// 第一步先把TabBar组件导入
export default {
  name: 'App',
  components:{
    // 第二步要在components组件里注册
    // 只有注册过了才能在模版里面使用
    TabBar,
    TabBarItem
  }
}
</script>

<style>
/* 让字体挨着边 */
/* 在App.vue里面写，不在main.js里面写 */
/* 这样写也是可以的，但是如果我要初始化的样式非常多，到时候把所有初始化的样式都写到这里会很拥挤 */
/* 所以，最终，我们还是在assets-css里面新建一个base.css，把初始化样式都写在里面吧 */
/* 所以我们在App.vue里面动态的引用base.css样式文件，而不是在main.js里面引用 */
/* 但是不能通过" require('./assets/css/base.css'"这样引用，会报错 */
/* 要通过@import来引用base.css样式 */
 
  /* 写法1： */
  @import url('assets/css/base.css');

  /* 写法2： */
  /* @import "./assets/css/base.css" */

  /* 如果你在JS里面引入.css文件直接使用import文件就可以了 */
  /* 但是因为在style里面做这件事情，它有一个固定的格式，要用@import */

  /* 写法3：这样写不好，初始化样式要单独放在一个文件里面比较好*/
   /* body{
     padding: 0;
     margin: 0;
  
  } */

  /* 接下来使用flex布局让它们四个到下面来，并且水平居中布局 */
  /* #tab-bar{
    display:flex;
    background-color:#f6f6f6; */

    /* 让它们4个跑到下面去 */
    /* position: fixed;
    left: 0;
    right: 0;
    bottom: 0; */

    /* 弄个阴影，有个过渡效果 */
    /* box-shadow: 0 -1px 1px rgba(100, 100, 100, .2);
  } */

  /* .tab-bar-item{
    flex: 1; */
    /* 这个表示均等分 */
    /* text-align: center; */
    /* 一般tab-bar的高度是49px——移动端，可以网上搜的 */
    /* height: 49px;
  } */

   /* .tab-bar-item img{ */
      /* 图片有了，但是太大了，要给它改一下大小 */
      /* width: 24px;
      height: 24px;
  } */

  /* 这里style代码给它挪个地方到TabBar.vue里面去 */
  /* 之后再挪到TabBarItem组件里面去 */
</style>
~~~

#### TabBar代码3.0之和路由结合

[indexof()方法](https://www.jianshu.com/p/c6dfe9229e2c)

> components文件夹只放公共的组件，而views文件夹放单独的组件。

![](Vue框架入门/242.png)

**App.vue**

~~~vue
<template>
  <div id="app">
    <router-view></router-view>
    <!--  -->
      <!--如果你没有封装的思想的话可能会这样做-->
      <!-- <div id="tab-bar">
        <div class="tab-bar-item">首页</div>
        <div class="tab-bar-item">分类</div>
        <div class="tab-bar-item">购物车</div>
        <div class="tab-bar-item">我的</div> -->
        <!-- 左上角，并且没有挨在边上。 -->
        <!-- 因为它默认有一个margin:8px -->
        <!-- 但是这样写不好，没有复用性，别的项目要用这个还要把它拷贝进去 -->
        <!-- 而且不仅你这里要拷贝，下面的样式也要拷贝，不好 -->
        <!-- 所以我们最好把这个东西封装成一个独立的组件 -->
        <!--我们在components这里新建一个文件夹tabbar(components文件夹里面以后要封装很多组件的)-->
        <!-- 如果所有的组件全部放在components文件夹里面管理起来太乱了 -->
        <!-- 所以我针对某个功能，单独建立一个个文件夹，这样管理起来就比较好 -->
      <!-- </div> -->
      <tab-bar>
      <!-- 在App.vue里面刚开始用的是TabBar -->

        <!-- <div class="tab-bar-item">
            <img src="../../assets/img/tabbar/home.svg" alt=""> -->
            <!-- 但是这样写路径太恶心了 -->
            <!-- 我们可以给路径起别名，后面讲 -->
              <!-- 首页
          </div>
        <div class="tab-bar-item">
            <img src="../../assets/img/tabbar/home.svg" alt="">
            分类
        </div>
        <div class="tab-bar-item">
            <img src="../../assets/img/tabbar/home.svg" alt="">
            <div>购物车</div>
        </div>
        <div class="tab-bar-item">
            <img src="../../assets/img/tabbar/home.svg" alt="">
            我的
        </div> -->
        <!-- 这里面的代码到时候还会继续抽取的，放心 -->
          <tab-bar-item path='/home'>
              <img slot="item-icon" src="./assets/img/tabbar/home.svg" alt="">
              <img slot="item-icon-active" src="./assets/img/tabbar/home_active.svg" alt="">
              <div slot="item-text">首页 </div>
          </tab-bar-item>

          <tab-bar-item path='/category'>
              <img slot="item-icon" src="./assets/img/tabbar/category.svg" alt="">
              <img slot="item-icon-active" src="./assets/img/tabbar/category_active.svg" alt="">
              <div slot="item-text">分类</div>
          </tab-bar-item>

          <tab-bar-item path='/cart'>
              <img slot="item-icon" src="./assets/img/tabbar/shopcart.svg" alt="">
              <img slot="item-icon-active" src="./assets/img/tabbar/shopcart_active.svg" alt="">
              <div slot="item-text">购物车</div>
          </tab-bar-item>

          <tab-bar-item path='/profile'>
              <img slot="item-icon" src="./assets/img/tabbar/profile.svg" alt="">
              <img slot="item-icon-active" src="./assets/img/tabbar/profile_active.svg" alt="">
              <div slot="item-text">我的</div>
          </tab-bar-item>
          <!-- 这个代码又有点多了，到时候可以再抽到另一个文件里面 -->
      </tab-bar>
    <!-- 这个组件标签名tab-bar是哪里来的呢？？？？ -->
    <!-- 我试了一下：Tab-Bar也是可以的,tab-Bar也是可以的 -->
  </div>
</template>

<script>
import TabBar from'./components/tabbar/TabBar'
import TabBarItem from './components/tabbar/TabBarItem'
// 第一步先把TabBar组件导入
export default {
  name: 'App',
  components:{
    // 第二步要在components组件里注册
    // 只有注册过了才能在模版里面使用
    TabBar,
    TabBarItem
  }
}
</script>

<style>
/* 让字体挨着边 */
/* 在App.vue里面写，不在main.js里面写 */
/* 这样写也是可以的，但是如果我要初始化的样式非常多，到时候把所有初始化的样式都写到这里会很拥挤 */
/* 所以，最终，我们还是在assets-css里面新建一个base.css，把初始化样式都写在里面吧 */
/* 所以我们在App.vue里面动态的引用base.css样式文件，而不是在main.js里面引用 */
/* 但是不能通过" require('./assets/css/base.css'"这样引用，会报错 */
/* 要通过@import来引用base.css样式 */
 
  /* 写法1： */
  @import url('assets/css/base.css');

  /* 写法2： */
  /* @import "./assets/css/base.css" */

  /* 如果你在JS里面引入.css文件直接使用import文件就可以了 */
  /* 但是因为在style里面做这件事情，它有一个固定的格式，要用@import */

  /* 写法3：这样写不好，初始化样式要单独放在一个文件里面比较好*/
   /* body{
     padding: 0;
     margin: 0;
  
  } */

  /* 接下来使用flex布局让它们四个到下面来，并且水平居中布局 */
  /* #tab-bar{
    display:flex;
    background-color:#f6f6f6; */

    /* 让它们4个跑到下面去 */
    /* position: fixed;
    left: 0;
    right: 0;
    bottom: 0; */

    /* 弄个阴影，有个过渡效果 */
    /* box-shadow: 0 -1px 1px rgba(100, 100, 100, .2);
  } */

  /* .tab-bar-item{
    flex: 1; */
    /* 这个表示均等分 */
    /* text-align: center; */
    /* 一般tab-bar的高度是49px——移动端，可以网上搜的 */
    /* height: 49px;
  } */

   /* .tab-bar-item img{ */
      /* 图片有了，但是太大了，要给它改一下大小 */
      /* width: 24px;
      height: 24px;
  } */

  /* 这里style代码给它挪个地方到TabBar.vue里面去 */
  /* 之后再挪到TabBarItem组件里面去 */
</style>
~~~

**index.js**

~~~javascript
import Vue from 'vue'
import VueRouter from 'vue-router'

const Home = () => import('../views/home/Home')
const Category = () => import('../views/category/Category')
const Cart = () => import('../views/cart/Cart')
const Profile = () => import('../views/profile/Profile')

// 1.安装插件
Vue.use(VueRouter)

// 2.创建路由对象
const routes = [
  {
    path: '',
    redirect: '/home'
  },
  {
    path: '/home',
    component: Home
  },
  {
    path: '/category',
    component: Category
  },
  {
    path: '/cart',
    component: Cart
  },
  {
    path: '/profile',
    component: Profile
  }
]
const router = new VueRouter({
  routes,
  mode: 'history'
})

// 3.导出router
export default router
~~~

**TabBarItem.vue**

~~~vue
<template>
<!-- 所有的item都展示同一个图片，同一个文字 -->
<!-- 所以不要写死，用插槽 -->
    <div class="tab-bar-item" @click="itemClick">
        <!-- <slot v-if="!isActive" name="item-icon"></slot>
        <slot v-else name="item-icon-active"></slot> -->

        <div v-if="!isActive"><slot name="item-icon"></slot></div>
        <div v-else><slot name="item-icon-active"></slot></div>
        <!-- 插槽这种东西很有可能某些属性就被替换掉，所以上面这么写不保险，按下面的来写 -->
        <!-- v-if和v-else都写到div里面，不写到插槽里面比较好 -->
        
        <!-- 这2个插槽最终只会展示一个 -->
        <!-- <slot :class="{active:isActive}" name="item-text"></slot> -->
        <div :class="{active:isActive}">
          <slot name="item-text"></slot>
        </div>
        <!-- 这样写就可以了 -->
        <!-- 插槽这里最终会被<div slot="item-text">首页 </div>替换掉 -->
        <!-- 所以在插槽里写:class没有用 -->
        <!-- <img src="../../assets/img/tabbar/home.svg" alt=""> -->
        <!-- 图片最下面会多3个像素，导致图片和文字之间有空隙 -->
        <!-- <div>首页 </div> -->
        <!-- 但是这2个东西(图片和文字)你是不能写死的 -->
        <!-- 不可以的话搞插槽就可以了 -->
    </div>
</template>

<script>
export default {
    name:'TabBarItem',
    props:{
      path:String
    },
    data(){
     return {
        // isActive:true,
        // 这个也不能写死
        // path:'/home'
        // 不能这样写死
     }
    },
    computed:{
      isActive(){
        // home -> item1(/home) = true
        // home -> item2(/category) = false
        // home -> item1(/cart) = false
        // home -> item1(/profile)  = false
        return this.$route.path.indexOf(this.path) !== -1
      }
    },
    methods: {
     itemClick(){
      //  console.log('itemClick');
      this.$router.replace(this.path)
     }
    }
}
</script>

<style scoped>
    /* 再把App.vue里面关于tab-bar-item的样式放到这里来 */
     .tab-bar-item{
    flex: 1;
    /* 这个表示均等分 */
    text-align: center;
    /* 一般tab-bar的高度是49px——移动端，可以网上搜的 */
    height: 49px;
    font-size: 14px;
  }

   .tab-bar-item img{
      /* 图片有了，但是太大了，要给它改一下大小 */
      width: 24px;
      height: 24px;
      margin-top: 3px;
      vertical-align: middle;
    /* 图片最下面会多3个像素，导致图片和文字之间有空隙 */
    margin-bottom: 2px;
  }

  .active{
    color: red;
  }
</style>
~~~

**Cart.vue**

> `Category.vue`，`Home.vue`、`Profile.vue`类似。

~~~vue
<template>
  <h2>购物车</h2>
</template>

<script>
  export default {
    name: "Cart"
  }
</script>

<style scoped>

</style>
~~~

#### TabBar代码4.0最终版

> alias(别名):@表示src路径

![](Vue框架入门/243.png)

**App.vue**

~~~javascript
<template>
  <div id="app">
    <router-view></router-view> 
    <main-tab-bar/>
  </div>
</template>

<script>
import MainTabBar from './components/mainTabbar/MainTabBar'
// 第一步先把TabBar组件导入
export default {
  name: 'App',
  components:{
    // 第二步要在components组件里注册
    // 只有注册过了才能在模版里面使用
    MainTabBar
  }
}
</script>

<style>
/* 让字体挨着边 */
/* 在App.vue里面写，不在main.js里面写 */
/* 这样写也是可以的，但是如果我要初始化的样式非常多，到时候把所有初始化的样式都写到这里会很拥挤 */
/* 所以，最终，我们还是在assets-css里面新建一个base.css，把初始化样式都写在里面吧 */
/* 所以我们在App.vue里面动态的引用base.css样式文件，而不是在main.js里面引用 */
/* 但是不能通过" require('./assets/css/base.css'"这样引用，会报错 */
/* 要通过@import来引用base.css样式 */
 
  /* 写法1： */
  @import url('assets/css/base.css');

  /* 写法2： */
  /* @import "./assets/css/base.css" */

  /* 如果你在JS里面引入.css文件直接使用import文件就可以了 */
  /* 但是因为在style里面做这件事情，它有一个固定的格式，要用@import */

  /* 写法3：这样写不好，初始化样式要单独放在一个文件里面比较好*/
   /* body{
     padding: 0;
     margin: 0;
  
  } */

  /* 接下来使用flex布局让它们四个到下面来，并且水平居中布局 */
  /* #tab-bar{
    display:flex;
    background-color:#f6f6f6; */

    /* 让它们4个跑到下面去 */
    /* position: fixed;
    left: 0;
    right: 0;
    bottom: 0; */

    /* 弄个阴影，有个过渡效果 */
    /* box-shadow: 0 -1px 1px rgba(100, 100, 100, .2);
  } */

  /* .tab-bar-item{
    flex: 1; */
    /* 这个表示均等分 */
    /* text-align: center; */
    /* 一般tab-bar的高度是49px——移动端，可以网上搜的 */
    /* height: 49px;
  } */

   /* .tab-bar-item img{ */
      /* 图片有了，但是太大了，要给它改一下大小 */
      /* width: 24px;
      height: 24px;
  } */

  /* 这里style代码给它挪个地方到TabBar.vue里面去 */
  /* 之后再挪到TabBarItem组件里面去 */
</style>
~~~

**main.js**

~~~javascript
import Vue from 'vue'
import App from './App'
import router from './router'

Vue.config.productionTip = false

/* eslint-disable no-new */
new Vue({
  el: '#app',
  router,
  render: h => h(App)
})

// require('./assets/css/base.css')
// 但是main.js里面以后尽量不要写这种代码
// 这种代码只是对样式的一种引用，写到这里的话，看起来就有点乱了。
// 所以最好把这个放到App.vue里面的style里面引用比较好

// 因为main.js一开始渲染的话就是渲染的App.vue
~~~

**index.js**

~~~javascript
import Vue from 'vue'
import VueRouter from 'vue-router'

const Home = () => import('../views/home/Home')
const Category = () => import('../views/category/Category')
const Cart = () => import('../views/cart/Cart')
const Profile = () => import('../views/profile/Profile')

// 1.安装插件
Vue.use(VueRouter)

// 2.创建路由对象
const routes = [
  {
    path: '',
    redirect: '/home'
  },
  {
    path: '/home',
    component: Home
  },
  {
    path: '/category',
    component: Category
  },
  {
    path: '/cart',
    component: Cart
  },
  {
    path: '/profile',
    component: Profile
  }
]
const router = new VueRouter({
  routes,
  mode: 'history'
})

// 3.导出router
export default router
~~~

**MainTabBar.vue**

~~~vue
<template>
   
      <!--如果你没有封装的思想的话可能会这样做-->
      <!-- <div id="tab-bar">
        <div class="tab-bar-item">首页</div>
        <div class="tab-bar-item">分类</div>
        <div class="tab-bar-item">购物车</div>
        <div class="tab-bar-item">我的</div> -->
        <!-- 左上角，并且没有挨在边上。 -->
        <!-- 因为它默认有一个margin:8px -->
        <!-- 但是这样写不好，没有复用性，别的项目要用这个还要把它拷贝进去 -->
        <!-- 而且不仅你这里要拷贝，下面的样式也要拷贝，不好 -->
        <!-- 所以我们最好把这个东西封装成一个独立的组件 -->
        <!--我们在components这里新建一个文件夹tabbar(components文件夹里面以后要封装很多组件的)-->
        <!-- 如果所有的组件全部放在components文件夹里面管理起来太乱了 -->
        <!-- 所以我针对某个功能，单独建立一个个文件夹，这样管理起来就比较好 -->
      <!-- </div> -->
      <tab-bar>
      <!-- 在App.vue里面刚开始用的是TabBar -->

        <!-- <div class="tab-bar-item">
            <img src="../../assets/img/tabbar/home.svg" alt=""> -->
            <!-- 但是这样写路径太恶心了 -->
            <!-- 我们可以给路径起别名，后面讲 -->
              <!-- 首页
          </div>
        <div class="tab-bar-item">
            <img src="../../assets/img/tabbar/home.svg" alt="">
            分类
        </div>
        <div class="tab-bar-item">
            <img src="../../assets/img/tabbar/home.svg" alt="">
            <div>购物车</div>
        </div>
        <div class="tab-bar-item">
            <img src="../../assets/img/tabbar/home.svg" alt="">
            我的
        </div> -->
        <!-- 这里面的代码到时候还会继续抽取的，放心 -->
          <tab-bar-item path='/home' activeColor="deeppink">
              <img slot="item-icon" src="@/assets/img/tabbar/home.svg" alt="">
              <img slot="item-icon-active" src="@/assets/img/tabbar/home_active.svg" alt="">
              <div slot="item-text">首页 </div>
          </tab-bar-item>

          <tab-bar-item path='/category' activeColor="deeppink">
              <img slot="item-icon" src="@/assets/img/tabbar/category.svg" alt="">
              <img slot="item-icon-active" src="@/assets/img/tabbar/category_active.svg" alt="">
              <div slot="item-text">分类</div>
          </tab-bar-item>

          <tab-bar-item path='/cart' activeColor="deeppink">
              <img slot="item-icon" src="@/assets/img/tabbar/shopcart.svg" alt="">
              <img slot="item-icon-active" src="@/assets/img/tabbar/shopcart_active.svg" alt="">
              <div slot="item-text">购物车</div>
          </tab-bar-item>

          <tab-bar-item path='/profile' activeColor="deeppink">
              <img slot="item-icon" src="@/assets/img/tabbar/profile.svg" alt="">
              <img slot="item-icon-active" src="@/assets/img/tabbar/profile_active.svg" alt="">
              <div slot="item-text">我的</div>
          </tab-bar-item>
          <!-- 这个代码又有点多了，到时候可以再抽到另一个文件里面 -->
      </tab-bar>
    <!-- 这个组件标签名tab-bar是哪里来的呢？？？？ -->
    <!-- 我试了一下：Tab-Bar也是可以的,tab-Bar也是可以的 -->
</template>

<script>
  import TabBar from '@/components/tabbar/TabBar'
  import TabBarItem from '@/components/tabbar/TabBarItem'

export default {
    name:'MainTabBar',
    components:{
        TabBar,
        TabBarItem
    }
}
</script>

<style scoped>
    
</style>
~~~

**TabBar.vue**

~~~vue
<template>
    <div id="tab-bar">
        <!-- <div class="tab-bar-item">
            <img src="../../assets/img/tabbar/home.svg" alt=""> -->
            <!-- 但是这样写路径太恶心了 -->
            <!-- 我们可以给路径起别名，后面讲 -->
            <!-- 首页
        </div>
        <div class="tab-bar-item">
            <img src="../../assets/img/tabbar/home.svg" alt="">
            分类
        </div>
        <div class="tab-bar-item">
            <img src="../../assets/img/tabbar/home.svg" alt="">
            <div>购物车</div>
        </div>
        <div class="tab-bar-item">
            <img src="../../assets/img/tabbar/home.svg" alt="">
            我的
        </div> -->
        <!-- 这里面只有文字，文字下面的4张图片还没有 -->
        <!-- 我们把图片放到img文件夹里面单独的tabbar文件夹下面 -->
        <!-- 不要为了省事把所有的图片都放到img一个文件夹里面 -->
        <slot></slot>
        <!-- 上面的全部不要，只弄一个插槽即可 -->
    </div>

    <!-- 但是我这个TabBar组件里面的东西太杂了，这个是一个大组件，里面的明细我不应该关系的 -->
    <!-- TabBar组件应该只负责TabBar自己的东西：div id="tab-bar"和#tab-bar{}这2个-->
    <!-- 至于item相关的东西不应该交给我管理 -->
    <!-- 全部交给TabBar管理的话，最后封装的组件就会乱七八糟的 -->
    <!-- 所以TabBar封装完之后只给它弄一个插槽(slot)就可以了 -->
</template>

<script>
export default {
    name:'TabBar'
}
</script>

<style scoped>
#tab-bar{
    display:flex;
    background-color:#f6f6f6;

    /* 让它们4个跑到下面去 */
    position: fixed;
    left: 0;
    right: 0;
    bottom: 0;

    /* 弄个阴影，有个过渡效果 */
    box-shadow: 0 -1px 1px rgba(100, 100, 100, .2);
  }

/* .tab-bar-item{
    flex: 1; */
    /* 这个表示均等分 */
    /* text-align: center; */
    /* 一般tab-bar的高度是49px——移动端，可以网上搜的 */
    /* height: 49px;
  } */

  /* .tab-bar-item img{ */
      /* 图片有了，但是太大了，要给它改一下大小 */
      /* width: 24px;
      height: 24px;
  } */
</style>
~~~

**TabBarItem.vue**

~~~vue
<template>
<!-- 所有的item都展示同一个图片，同一个文字 -->
<!-- 所以不要写死，用插槽 -->
    <div class="tab-bar-item" @click="itemClick">
        <!-- <slot v-if="!isActive" name="item-icon"></slot>
        <slot v-else name="item-icon-active"></slot> -->

        <div v-if="!isActive"><slot name="item-icon"></slot></div>
        <div v-else><slot name="item-icon-active"></slot></div>
        <!-- 插槽这种东西很有可能某些属性就被替换掉，所以上面这么写不保险，按下面的来写 -->
        <!-- v-if和v-else都写到div里面，不写到插槽里面比较好 -->
        
        <!-- 这2个插槽最终只会展示一个 -->
        <!-- <slot :class="{active:isActive}" name="item-text"></slot> -->
        <!-- <div :class="{active:isActive}"> -->
        <!--现在动态绑定class已经没用了  -->
        <div :style="activeStyle">
          <!-- v-bind动态绑定style并且把这个style抽到一个计算属性里面 -->
          <slot name="item-text"></slot>
        </div>
        <!-- 这样写就可以了 -->
        <!-- 插槽这里最终会被<div slot="item-text">首页 </div>替换掉 -->
        <!-- 所以在插槽里写:class没有用 -->
        <!-- <img src="../../assets/img/tabbar/home.svg" alt=""> -->
        <!-- 图片最下面会多3个像素，导致图片和文字之间有空隙 -->
        <!-- <div>首页 </div> -->
        <!-- 但是这2个东西(图片和文字)你是不能写死的 -->
        <!-- 不可以的话搞插槽就可以了 -->
    </div>
</template>

<script>
export default {
    name:'TabBarItem',
    props:{
      path:String,
      activeColor:{
        type:String,
        default:'red'
      }
    },
    data(){
     return {
        // isActive:true,
        // 这个也不能写死
        // path:'/home'
        // 不能这样写死
     }
    },
    computed:{
      isActive(){
        // home -> item1(/home) = true
        // home -> item2(/category) = false
        // home -> item1(/cart) = false
        // home -> item1(/profile)  = false
        return this.$route.path.indexOf(this.path) !== -1
      },
      activeStyle(){
        return this.isActive?{color:this.activeColor}:{}
      }
    },
    methods: {
     itemClick(){
      //  console.log('itemClick');
      this.$router.replace(this.path)
     }
    }
}
</script>

<style scoped>
    /* 再把App.vue里面关于tab-bar-item的样式放到这里来 */
     .tab-bar-item{
    flex: 1;
    /* 这个表示均等分 */
    text-align: center;
    /* 一般tab-bar的高度是49px——移动端，可以网上搜的 */
    height: 49px;
    font-size: 14px;
  }

   .tab-bar-item img{
      /* 图片有了，但是太大了，要给它改一下大小 */
      width: 24px;
      height: 24px;
      margin-top: 3px;
      vertical-align: middle;
    /* 图片最下面会多3个像素，导致图片和文字之间有空隙 */
    margin-bottom: 2px;
  }

  /* .active{
    color: red; */
    /* 这个颜色也不能写死 */
  /* } */
</style>
~~~

# ES6补充知识：Promise

## 认识Promise

### 什么是Promise

![](Vue框架入门/244.png)

### 网络请求的回调地狱

![](Vue框架入门/245.png)

## Promise的基本使用

> 需求：延迟1秒钟打印3遍"hello world"，打印完后再延迟1秒钟打印3遍"hello vue.js",打印完后再延迟1秒钟打印3遍"你好，世界"

**Promise写法1.0之回调地狱**

~~~javascript
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <script>
        // 1.使用setTimeout
        // setTimeout(() => {
        //     console.log('hello world');
        // }, 1000);

        // Promise首先是一个类，我们要通过这个类给它new一个对象
        // new Promise(参数(本身是一个函数))
        // 而这个参数(函数)本身也包含2个参数，一个是resolve,一个是reject
        // resolve,reject本身又是函数
        new Promise((resolve, reject) => {
            // 需求，延迟一秒钟打印3遍"hello world"，打印完后再延迟一秒钟打印3遍"hello vue.js",
            // 打印完后再延迟一秒钟打印3遍"你好，世界"
            setTimeout(() => {
                console.log('hello world');
                console.log('hello world');
                console.log('hello world');
                // 在Promise里面要执行的代码不会放到这里面，而是放到外面
                setTimeout(() => {
                    console.log('hello Vue.js');
                    console.log('hello Vue.js');
                    console.log('hello Vue.js');
                    setTimeout(() => {
                        console.log('你好，世界！');
                        console.log('你好，世界！');
                        console.log('你好，世界！');
                    }, 1000);
                }, 1000);
            }, 1000)
        })
    </script>
</body>

</html>
~~~

**Promise写法2.0之抽离未完全**

~~~javascript
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <script>
        new Promise((resolve, reject) => {
            // resolve,reject这2个参数都是函数
            setTimeout(() => {
                resolve()
            }, 1000);
        }).then(() => {
            // then也是一个函数
            console.log('hello world');
            console.log('hello world');
            console.log('hello world');
            setTimeout(() => {
                console.log('hello Vue.js');
                console.log('hello Vue.js');
                console.log('hello Vue.js');
                setTimeout(() => {
                    console.log('你好，世界！');
                    console.log('你好，世界！');
                    console.log('你好，世界！');
                }, 1000);
            }, 1000);
        })
    </script>
</body>

</html>
~~~

**Promise写法2.0之抽离完全**

> 虽然看上去更加复杂了，但是我们已经将对应的结构给它划分清楚了。
>
> 虽然代码变得比较复杂了，但是逻辑变得非常清晰了，我们的处理代码都是放在then后面的。
>
> 这个就是链式编程。

~~~javascript
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <script>
        new Promise((resolve, reject) => {
            // resolve,reject这2个参数都是函数
            // 我们可以把一次setTimeout看成一次网络请求
		
            // 第一次网络请求的代码
            setTimeout(() => {
                resolve()
            }, 1000);
        }).then(() => {
            // then也是一个函数
            // 第一次处理的代码
            console.log('hello world');
            console.log('hello world');
            console.log('hello world');
            return new Promise((resolve, reject) => {
                // 第二次网络请求的代码
                setTimeout(() => {
                    resolve()
                }, 1000);
            })
        }).then(() => {
            // 第二次处理的代码
            console.log('hello Vue.js');
            console.log('hello Vue.js');
            console.log('hello Vue.js');
            return new Promise((resolve, reject) => {
                // 第三次网络请求的代码
                setTimeout(() => {
                    resolve()
                }, 1000);
            })
        }).then(() => {
            // 第三次处理的代码
            console.log('你好，世界！');
            console.log('你好，世界！');
            console.log('你好，世界！');
        })
    </script>
</body>

</html>
~~~

**Promise写法总结**

~~~javascript
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <script>
        // 什么情况下会用到Promise？一般情况下是有异步操作时，使用Promise对这个异步操作进行封装
        // new -> 构造函数(1.保存了一些状态信息 2.执行传入的函数)
        // 在执行我们传入的回调函数时会传入2个参数：resolve,reject,而它们两个本身又是函数
        new Promise((resolve, reject) => {
            setTimeout(() => {
                // 你在这里进行网络请求的时候，会传过来一些data，你肯定要处理这些data
                // 但是Promise不会在这里处理data(否则看起来会很乱)
                // 它会在then后面进行处理

                // resolve(data)
                // 成功的时候调用resolve处理成功的结果
                // 一旦调用resolve这个函数就会调用后面的then函数进行处理
                // resolve('hello world')

                // 失败的时候调用reject
                reject('error message')
            }, 1000);
        }).then((data) => {
            // 这里会把数据"hello world"传入到data里面
            // 1.100行的处理代码
            console.log(data);
        }).catch((err) => {
            // 这里会把数据"error message"传入到error里面
            console.log(err);
        })
        // 处理代码在这里写
    </script>
</body>

</html>
~~~

### 定时器的异步事件

![](Vue框架入门/246.png)

### 定时器异步事件解析

![](Vue框架入门/247.png)

### Promise三种状态

![](Vue框架入门/248.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <script>
        new Promise((resolve, reject) => {
            setTimeout(() => {
                // resolve('Hello Vue.js')
                reject('error message')
                // 这2句话注释其中一个
            }, 1000)
            // }).then(函数1，函数2)
            // 你也可以不写catch,直接在then里面写，函数1表示满足，函数2表示不满足
        }).then(data => {
            console.log(data);
        }, err => {
            console.log(err);
        })
    </script>
</body>

</html>
~~~

## Promise链式调用

### 链式调用

![](Vue框架入门/249.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Promise链式调用/title>
</head>

<body>
    <script>
        // 需求：
        // 网络请求：aaa->自己处理(10行代码)
        // 处理：aaa111(在aaa后面拼接上111) ->自己处理(10行代码)
        // 处理aaa111222(再拼接上222)->自己处理(10行代码)
        new Promise((resolve, reject) => {
            // reject是可选参数，可传可不传
            setTimeout(() => {
                resolve('aaa')
                // 这个网络请求花费的时间是1秒，等你请求完之后再执行这里面的操作
            }, 1000);
        }).then(res => {
            // 1.自己处理10行代码
            console.log(res, '第一层的10行处理代码');
            // 再给aaa拼接上111传给下一层进行处理

            // 2.
            // res = res + '111';
            // 我不想这样做，这样做把下一层的代码和这一层的代码给混到一起了
            // 如果这2层代码都非常复杂的话，混到一起非常不方便管理
            return new Promise((resolve) => {
                // 当你只有一个resolve的时候，另一个参数reject是可以不写的
                resolve(res + '111')
            })
        }).then(res => {
            console.log(res, '第二层的10行处理代码');
            return new Promise((resolve) => {
                resolve(res + '222')
            })
        }).then(res => {
            console.log(res, '第三层的10行处理代码');
        })
        // 这里第二层和第三层都没有进行异步操作，只有第一层进行了异步操作
    </script>
</body>

</html>
~~~

### 链式调用简写

![](Vue框架入门/250.png)

**简写1.0版本**

~~~javascript
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <script>
        // new Promise(resolve=>resolve(结果))简写
        new Promise((resolve, reject) => {
            // reject是可选参数，可传可不传
            setTimeout(() => {
                resolve('aaa')
            }, 1000);
        }).then(res => {
            console.log(res, '第一层的10行处理代码');
            return Promise.resolve(res + '111')
            // 这样写更加的简洁，不用再return Promise对象了
        }).then(res => {
            console.log(res, '第二层的10行处理代码');
            return Promise.resolve(res + '222')
        }).then(res => {
            console.log(res, '第三层的10行处理代码');
        })
    </script>
</body>

</html>
~~~

**简写2.0版本**

~~~javascript
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <script>
        // 省略掉Promise.resolve
        new Promise((resolve, reject) => {
            // reject是可选参数，可传可不传
            setTimeout(() => {
                resolve('aaa')
            }, 1000);
        }).then(res => {
            console.log(res, '第一层的10行处理代码');
            return res + '111'
            // 更加简洁，Promise.resolve都不需要了
        }).then(res => {
            console.log(res, '第二层的10行处理代码');
            return res + '222'
        }).then(res => {
            console.log(res, '第三层的10行处理代码');
        })
    </script>
</body>

</html>
~~~

我们前面写的代码都是没有写reject参数，默认3层代码都是成功的。但是实际上也许某一层代码会失败，所以还要进行划分。

**第一层就拒绝的代码**

~~~javascript
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <script>
        // 省略掉Promise.resolve
        new Promise((resolve, reject) => {
            // reject是可选参数，可传可不传
            setTimeout(() => {
                // resolve('aaa')
                reject('error message')
                // 第一步就给你拒绝掉了，返回给你一个error
                // 那么下面的第二层，第三层代码都不会执行的
            }, 1000);
        }).then(res => {
            console.log(res, '第一层的10行处理代码');
            return res + '111'
        }).then(res => {
            console.log(res, '第二层的10行处理代码');
            return res + '222'
        }).then(res => {
            console.log(res, '第三层的10行处理代码');
        }).catch(err => {
            console.log(err);
            // 第一层就有错，直接执行catch，第二层，第三层都不会执行的
        })
    </script>
</body>

</html>
~~~

**第二层拒绝的代码**

~~~javascript
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <script>
        new Promise((resolve, reject) => {
            // reject是可选参数，可传可不传
            setTimeout(() => {
                resolve('aaa')
            }, 1000);
        }).then(res => {
            console.log(res, '第一层的10行处理代码');
            return new Promise((resolve, reject) => {
                // return res + '111'
                reject('error message')
            })
            // 第二步就给你拒绝掉了，返回给你一个error
            // 那么下面的第三层代码不会执行的
        }).then(res => {
            console.log(res, '第二层的10行处理代码');
            return res + '222'
        }).then(res => {
            console.log(res, '第三层的10行处理代码');
        }).catch(err => {
            console.log(err);
            // 第二层就有错，直接执行catch，第一层会执行，第三层不会执行
        })
    </script>
</body>

</html>
~~~

**第二层拒绝的代码简写(使用Promise.reject)**

~~~javascript
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <script>
        new Promise((resolve, reject) => {
            // reject是可选参数，可传可不传
            setTimeout(() => {
                resolve('aaa')
            }, 1000);
        }).then(res => {
            console.log(res, '第一层的10行处理代码');
            return Promise.reject('error message')
            // 打印error message每次还要new Promise也很麻烦，但是也有简写的
            // 这样就是简写
        }).then(res => {
            console.log(res, '第二层的10行处理代码');
            return res + '222'
        }).then(res => {
            console.log(res, '第三层的10行处理代码');
        }).catch(err => {
            console.log(err);
        })
    </script>
</body>

</html>
~~~

**第二层拒绝的代码简写2.0(使用throw)**

~~~javascript
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <script>
        new Promise((resolve, reject) => {
            // reject是可选参数，可传可不传
            setTimeout(() => {
                resolve('aaa')
            }, 1000);
        }).then(res => {
            console.log(res, '第一层的10行处理代码');
            throw 'error message'
            // 打印error message每次还要new Promise也很麻烦，但是也有简写的
            // 这样就是简写
        }).then(res => {
            console.log(res, '第二层的10行处理代码');
            return res + '222'
        }).then(res => {
            console.log(res, '第三层的10行处理代码');
        }).catch(err => {
            console.log(err);
        })
    </script>
</body>

</html>
~~~

### Promise的all方法

[Promise对象Promise.all()方法的使用](https://itbilu.com/javascript/js/41KMSZ9a.html)

**原始写法：**

~~~javascript
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <script>
        // 需求本身依赖2个请求：请求1，请求2
        // 必须2个请求都请求完成了才能继续往下做需求

        // 请求1
        let isResult1 = false;
        let isResult2 = false;
        $ajax({
            url: '',
            success: function () {
                console.log('结果1');
                handleResult();
                // 我没办法确定请求1和请求2谁先返回
                // 没办法，只能先定义一个函数，2个里面都处理
            }
        })

        // 请求2
        $ajax({
            url: '',
            success: function () {
                console.log('结果2');
                handleResult();
            }
        })

        // 如何判断2个请求都拿到了？？
        function handleResult() {
            if (isResult1 && isResult2) {
                // 2个结果都为true再执行下面的操作
            }
        }
    </script>
</body>

</html>
~~~

**Promise.all写法**

~~~javascript
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <script>
        Promise.all([
            //     new Promise((resolve, reject) => {
            //         $ajax({
            //             url: 'url1',
            //             success: function (data) {
            //                 resolve(data)
            //             }
            //         })
            //     })
            // ]),
            //     new Promise((resolve, reject) => {
            //         $ajax({
            //             url: 'url2',
            //             success: function (data) {
            //                 resolve(data)
            //             }
            //         })

            new Promise((resolve, reject) => {
                setTimeout(() => {
                    resolve({ name: 'why', age: '18' })
                }, 2000);
            }),
            new Promise((resolve, reject) => {
                setTimeout(() => {
                    resolve({ name: 'Kobe', age: '19' })
                }, 1000);
                // 这2个setTimeout都要达到(1个要1秒，1个要2秒)才能执行接下来的操作
            })
        ]).then(results => {
            console.log(results);
        })
    </script>
</body>

</html>
~~~

# Vuex详解

> 学Vuex的时候突然感到有点崩溃，感觉前面组件通信什么的没有学好，进度又慢，心里又乱，于是又重头看了2天别的Vue视频，学了些SPA有关的知识。最近有点排斥Vue的学习了，Node也有几天没有学了，今天慢慢的缓过来了，又接着开始接下来的课程了。
>
> 加油啊，我看Vuex学完，再学个axios基本上Vue基础知识就全部学完了啊！！！
>
> 接下来就是一个6天的完整案例了！！！
>
> 坚持下去吧，都走到这一步了。
>
> 现在学着学着，感觉Vuex的难度还没有VueRouter难，很好理解啊，我之前纯属自己吓自己，搞得自己有点崩溃，其实完全没必要，Vuex现在是可以很轻松的拿下的。
>
> 前面感觉还行，后面也没我想得这么简单了，有些语法也不太好理解。

## 认识Vuex

### Vuex是做什么的?

> Vuex就是一个大管家，专门用来管理一些公共的东西(多个组件之间共享状态)

![](Vue框架入门/251.png)

![](Vue框架入门/252.png)

### 管理什么状态呢?

![](Vue框架入门/253.png)

### 单界面的状态管理

> 变量一般是用来保存我们的状态的，而我们的变量一般保存到data里面。

![](Vue框架入门/254.png)

### 单界面状态管理的实现

![](Vue框架入门/255.png)

### 多界面状态管理

![](Vue框架入门/256.png)

### Vuex状态管理图例

![](Vue框架入门/257.png)

## Vuex基本使用

> 其实这个也不算难，硬是被自己拖了好几天没有接下去学。

### 简单的案例

![](Vue框架入门/258.png)

### 挂载到Vue实例中

![](Vue框架入门/259.png)

### 使用Vuex的count

![](Vue框架入门/260.png)

### 代码示例1.0

目录结构如下：

![](Vue框架入门/262.png)

**HelloVuex.vue**

~~~vue
<template>
  <div>
    <!-- <h2>{{counter++}}</h2> -->
    <h2>{{$store.state.counter}}</h2>
  </div>
</template>

<script>
  export default{
    name:'HelloVuex',
    // HelloVuex组件其实是App组件的子组件
    // props:{
    //   counter:Number 
    // }
  }
</script>

<style scoped>
  
</style>
~~~

**index.js(这个是store文件夹里面的)**

~~~javascript
import Vue from 'vue'
import Vuex from 'vuex'

// 我们一般不把文件名起名叫vuex，而是叫store(仓库)
// 1.安装插件(vuex是一个插件，需要先进行安装)
Vue.use(Vuex)

// 2.创建对象
const store = new Vuex.Store({
    state: {
        // state用于保存状态
        counter:1000
    },
    mutations: {
        // 在这里面定义方法
        increment(state) { 
            state.counter++
        },
        decrement(state) { 
            state.counter--
        }
    },
    actions: {

    }, getters: {

    }, modules: {

    }
})
// Vuex里面有一个属性叫做store

// 3.导出store对象
export default store
~~~

**App.vue**

~~~vue
<template>
  <div id="app">
    <h2>---------------------Appp内容------------------</h2>
   <!-- <h2>{{message}}</h2> -->
   <!-- <h2>{{counter}}</h2> -->
   <h2>{{$store.state.counter}}</h2>
   <!-- 而状态是在view里面显示的，也就是这里显示 -->
   <!-- <button @click='counter++'>+</button> -->
   <!-- <button @click='counter--'>-</button> -->

   <!-- <button @click="$store.state.counter++">+</button> -->
   <!-- <button @click="$store.state.counter--">-</button> -->
   <!-- 这样写可以，但是这样写不好 -->

   <button @click="addition">+</button>
   <button @click="subtraction">-</button>

   <h2>------------------Hello Vuex内容----------------------</h2>
   <hello-vuex/>
   <!-- 页面当中也可以发生一些action(行为)，比如点击事件 -->

   <!-- <hello-vuex :counter="counter"></hello-vuex> -->
   <!-- 标签里面不需要写东西(比如写插槽)的话用单标签比较清爽 -->
   <!-- 这里是把变量值传过去 -->
  </div>
</template>

<script>
import HelloVuex from './components/HelloVuex'
export default {
  components:{
    HelloVuex
  },
  data(){
    return {
      message:'我是App组件'
    }
  },
  methods: {
    addition(){
      this.$store.commit('increment')
    },
   subtraction(){
      this.$store.commit('decrement')
    }
  },
}
</script>

<style scoped>

</style>
~~~

**main.js**

~~~javascript
import Vue from 'vue'
import App from './App'
// import Vuex from 'vuex'
import store from './store'
Vue.config.productionTip = false

// Vue.use(Vuex)
// 但是这样写的话代码就混在一起了


/* eslint-disable no-new */
new Vue({
  el: '#app',
  store,
  render: h => h(App)
})
~~~

## Vuex核心概念

### 核心概念汇总

![](Vue框架入门/261.png)

### State

![](Vue框架入门/263.png)

### Getters

#### Getters基本使用

![](Vue框架入门/264.png)

#### Getters作为参数和传递参数

![](Vue框架入门/265.png)

### 代码示例2.0

**HelloVuex.vue**

~~~javascript
<template>
  <div>
    <!-- <h2>{{counter++}}</h2> -->
    <h2>{{$store.state.counter}}</h2>
    <h2>{{$store.state.counter * $store.state.counter}}</h2>
    <h2>{{$store.getters.more20stu}}</h2>

  </div>
</template>

<script>
  export default{
    name:'HelloVuex',
    // HelloVuex组件其实是App组件的子组件
    // props:{
    //   counter:Number 
    // }

    // 如果这里也想要获得年龄大于等于20岁的学生，
    // 还要把App.vue里面的 more20stu方法拷贝一份到这里
  }
</script>

<style scoped>
  
</style>
~~~

**index.js(这个是store文件夹里面的)**

~~~javascript
import Vue from 'vue'
import Vuex from 'vuex'

// 我们一般不把文件名起名叫vuex，而是叫store(仓库)
// 1.安装插件(vuex是一个插件，需要先进行安装)
Vue.use(Vuex)

// 2.创建对象
const store = new Vuex.Store({
    // 推荐只建立一个store，为了方便管理(单一状态树)
    state: {
        // state用于保存状态
        counter: 1000,
        students: [
            {id:110,name:'why',age:18},
            {id:111,name:'Kobe',age:24},
            {id:112,name:'James',age:30},
            { id: 113, name: 'curry', age: 10 },
            // 我想要获取年龄大于20岁的学生
        ]
    },
    mutations: {
        // 在这里面定义方法
        increment(state) { 
            state.counter++
        },
        decrement(state) { 
            state.counter--
        }
    },
    actions: {

    },
    getters: {
        powerCounter(state) { 
            // getters方法和之前学的计算属性差不多
            return state.counter * state.counter
        },
        more20stu(state) { 
            return state.students.filter(s => s.age > 20)
        },
        // 我还想获取年龄大于20岁学生的个数
         more20stuLength(state) { 
            return state.students.filter(s => s.age > 20).length
        },
        //  方法2如下
        more20stuLength2(state,getters) { 
            return getters.more20stu.length
        },

        // 之前的age是写死的，现在我希望别人自己决定age是多少
        moreAgeStu(state) { 
            // return function (age) { 
            //     return state.students.filter(s=> s.age > age)
            // }

            // 简写如下：
            return age => { 
                return state.students.filter(s=> s.age > age)
            }
        }
    },
    modules: {

    }
})
// Vuex里面有一个属性叫做store

// 3.导出store对象
export default store
~~~

**App.vue**

~~~javascript
<template>
  <div id="app">
    <h2>---------------------Appp内容------------------</h2>
   <!-- <h2>{{message}}</h2> -->
   <!-- <h2>{{counter}}</h2> -->
   <h2>{{$store.state.counter}}</h2>
   <!-- 而状态是在view里面显示的，也就是这里显示 -->
   <!-- <button @click='counter++'>+</button> -->
   <!-- <button @click='counter--'>-</button> -->

   <!-- <button @click="$store.state.counter++">+</button> -->
   <!-- <button @click="$store.state.counter--">-</button> -->
   <!-- 这样写可以，但是这样写不好 -->

   <button @click="addition">+</button>
   <button @click="subtraction">-</button>

    <h2>---------------Appp内容：getters相关信息--------------</h2>
    <!-- <h2>{{$store.state.counter * $store.state.counter}}</h2> -->
    <h2>{{$store.getters.powerCounter}}</h2>
    <!-- 但是这样写太长了，不好 -->

    <!-- <h2>{{more20stu}}</h2> -->
    <h2>{{$store.getters.more20stu}}</h2>

    <h2>{{$store.getters.more20stu.length}}</h2>
    <!-- 我还想获取年龄大于20岁学生的个数 -->
    <!--你可以通过length拿到，但是我现在希望你通过getters来拿  -->
    <h2>{{$store.getters.more20stuLength}}</h2>
    <h2>{{$store.getters.more20stuLength2}}</h2>

    <h2>{{$store.getters.moreAgeStu(8)}}</h2>
    <!-- 这个年龄不是写死的，我可以写18，也可以写25等等，可以写任何数 -->


   <h2>------------------Hello Vuex内容----------------------</h2>
   <hello-vuex/>
   <!-- 页面当中也可以发生一些action(行为)，比如点击事件 -->

   <!-- <hello-vuex :counter="counter"></hello-vuex> -->
   <!-- 标签里面不需要写东西(比如写插槽)的话用单标签比较清爽 -->
   <!-- 这里是把变量值传过去 -->
  </div>
</template>

<script>
import HelloVuex from './components/HelloVuex'
export default {
  components:{
    HelloVuex
  },
  data(){
    return {
      message:'我是App组件'
    }
  },
  computed:{
    // more20stu(){
    //   // return this.$store.state.students
    //   // return this.$store.state.students.filter(s=>{
    //   //   return s.age >= 20
    //   // })

    //   return this.$store.state.students.filter(s=> s.age >= 20)
    //     // 这样更加简单
    // }
  },
  methods: {
    addition(){
      this.$store.commit('increment')
    },
   subtraction(){
      this.$store.commit('decrement')
    }
  },
}
</script>

<style scoped>

</style>
~~~

### Mutation

#### Mutation状态更新

![](Vue框架入门/266.png)

#### Mutation传递参数

![](Vue框架入门/267.png)

#### Mutation提交风格

![](Vue框架入门/268.png)

#### Mutation响应规则

![](Vue框架入门/269.png)

![](Vue框架入门/273.jpg)

#### Mutation常量类型 – 概念

![](Vue框架入门/270.png)

#### Mutation常量类型 – 代码

![](Vue框架入门/271.png)

#### Mutation同步函数

>  以后在Mutation里面写的所有的代码，都不能是异步的。

![](Vue框架入门/272.png)

### Action

#### Action的基本定义

![](Vue框架入门/273.png)

#### Action的分发

![](Vue框架入门/274.png)

#### Action返回的Promise

![](Vue框架入门/275.png)

### 代码示例3.0

**App.vue**

~~~vue
<template>
  <div id="app">
    <h2>---------------------Appp内容------------------</h2>
   <!-- <h2>{{message}}</h2> -->
   <!-- <h2>{{counter}}</h2> -->
   <h2>{{$store.state.counter}}</h2>
   <!-- 而状态是在view里面显示的，也就是这里显示 -->
   <!-- <button @click='counter++'>+</button> -->
   <!-- <button @click='counter--'>-</button> -->

   <!-- <button @click="$store.state.counter++">+</button> -->
   <!-- <button @click="$store.state.counter--">-</button> -->
   <!-- 这样写可以，但是这样写不好 -->

   <button @click="addition">+</button>
   <button @click="subtraction">-</button>

    <!-- <button @click="addFive">每次加5</button> -->
    <!-- <button @click="addTen">每次加10</button> -->
    <!-- 这样写不好，定义了2个方法 -->

    <button @click="addCount(5)">每次加5</button>
    <button @click="addCount(10)">每次加10</button>
    <!--这样写比较好，只定义了1个方法 -->

    <button @click="addStudent">添加学生</button>

    <h2>---------------Appp内容：getters相关信息--------------</h2>
    <!-- <h2>{{$store.state.counter * $store.state.counter}}</h2> -->
    <h2>{{$store.getters.powerCounter}}</h2>
    <!-- 但是这样写太长了，不好 -->

    <!-- <h2>{{more20stu}}</h2> -->
    <h2>{{$store.getters.more20stu}}</h2>

    <h2>{{$store.getters.more20stu.length}}</h2>
    <!-- 我还想获取年龄大于20岁学生的个数 -->
    <!--你可以通过length拿到，但是我现在希望你通过getters来拿  -->
    <h2>{{$store.getters.more20stuLength}}</h2>
    <h2>{{$store.getters.more20stuLength2}}</h2>

    <h2>{{$store.getters.moreAgeStu(8)}}</h2>
    <!-- 这个年龄不是写死的，我可以写18，也可以写25等等，可以写任何数 -->

    <h2>--------Appp内容：info对象的内容是否是响应式的--------</h2>
    <h2>{{$store.state.info}}</h2>
    <button @click="updateInfo">修改信息</button>

   <h2>------------------Hello Vuex内容----------------------</h2>
   <hello-vuex/>
   <!-- 页面当中也可以发生一些action(行为)，比如点击事件 -->

   <!-- <hello-vuex :counter="counter"></hello-vuex> -->
   <!-- 标签里面不需要写东西(比如写插槽)的话用单标签比较清爽 -->
   <!-- 这里是把变量值传过去 -->
  </div>
</template>

<script>
import HelloVuex from './components/HelloVuex'
import {
  INCREMENT
} from './store/mutations-types'
export default {
  components:{
    HelloVuex
  },
  data(){
    return {
      message:'我是App组件'
    }
  },
  computed:{
    // more20stu(){
    //   // return this.$store.state.students
    //   // return this.$store.state.students.filter(s=>{
    //   //   return s.age >= 20
    //   // })

    //   return this.$store.state.students.filter(s=> s.age >= 20)
    //     // 这样更加简单
    // }
  },
  methods: {
    addition(){
      this.$store.commit('increment')
    },
   subtraction(){
      this.$store.commit('decrement')
    },
    addCount(count){
      // payload:负载
      // 1.普通的提交风格
      this.$store.commit('incrementCount',count)
      // 新增一个count参数，把count传给index.js

      // 2.特殊的提交风格
      // this.$store.commit({
      //   type:'incrementCount',
      //   // count:count
      //   count,
      //   // 这个是简写
      // })
    },

    // 2种不同的提交风格最后提交到index.js里面的参数是不一样的
    addStudent(){
      const stu = {id:114,name:'alien',age:35}
      this.$store.commit('addStudent',stu)
    },
    updateInfo(){
      // this.$store.commit('updateInfo')
      // 要想办法让它经过actions

      // 1.0版
      // this.$store.dispatch('aUpdateInfo','我是payload')

      // 2.0版
      // this.$store.dispatch('aUpdateInfo',()=>{
      //   console.log('里面已经完成了');
      // })

      // 3.0版
      //  this.$store.dispatch('aUpdateInfo',{
      //    message:'我是携带的信息',
      //    success:()=>{
      //      console.log('里面已经完成了');
      //    }
      //   //  这样写不够优雅，我携带的信息和我回调的信息写到一坨去了
      //  })

      // 4.0版
      this.$store
      .dispatch('aUpdateInfo','我是携带的信息')
      .then(res=>{
        // 里面完成了提交
        console.log(res);
      })
    }
  }
}
</script>

<style scoped>

</style>
~~~

### Module

#### 认识Module

![](Vue框架入门/276.png)

#### Module局部状态

![](Vue框架入门/277.png)

#### Actions的写法

![](Vue框架入门/278.png)

### 代码示例4.0(最终版)

![](Vue框架入门/280.png)

**HelloVuex.vue**

~~~vue
<template>
  <div>
    <!-- <h2>{{counter++}}</h2> -->
    <h2>{{$store.state.counter}}</h2>
    <h2>{{$store.state.counter * $store.state.counter}}</h2>
    <h2>{{$store.getters.more20stu}}</h2>

  </div>
</template>

<script>
  export default{
    name:'HelloVuex',
    // HelloVuex组件其实是App组件的子组件
    // props:{
    //   counter:Number 
    // }

    // 如果这里也想要获得年龄大于等于20岁的学生，
    // 还要把App.vue里面的 more20stu方法拷贝一份到这里
  }
</script>

<style scoped>
  
</style>
~~~

**index.js**

~~~javascript
import Vue from 'vue'

import Vuex from 'vuex'

import { 
    INCREMENT
} from './mutations-types'
// 我们一般不把文件名起名叫vuex，而是叫store(仓库)
// 1.安装插件(vuex是一个插件，需要先进行安装)
Vue.use(Vuex)

// 2.创建对象
const moduleA = {
    state: {
        name:'zhangsan'
    },
    mutations: {
        updateName(state,payload) { 
            state.name = payload
        }
    },
  
    getters: {
        fullname1(state) { 
            return state.name + '11111'
        },
        fullname2(state, getters) { 
            // 这个getters对应的是上面的getters
            return getters.fullname1 + '22222'
        },
        fullname3(state, getters, rootState) { 
            return getters.fullname2 + rootState.counter
        }
    },
    actions: {
        aUpdateName(context) { 
            // 这个context上下文就不再是store对象了，这个就变得比较复杂了
            setTimeout(() => {
                context.commit('updateName','wangwu')
            }, 1000);
        }
    },
}
const store = new Vuex.Store({
    // 推荐只建立一个store，为了方便管理(单一状态树)
    state: {
        // state用于保存状态
        counter: 1000,
        students: [
            {id:110,name:'why',age:18},
            {id:111,name:'Kobe',age:24},
            {id:112,name:'James',age:30},
            {id:113,name: 'curry', age: 10 },
            // 我想要获取年龄大于20岁的学生
        ],
        info: {
            name: 'Kobe',
            age: 40,
            height:1.98
        }
    },
    mutations: {
        // 在这里面定义方法
        [INCREMENT](state) { 
            state.counter++
        },
        decrement(state) { 
            state.counter--
        },
        // incrementCount(state, count) { 
        //     console.log(count);
        //     // state.counter += count
        // },
        // incrementCount(state, payload) {
        incrementCount(state, count) {
            //  把count改成payload更加合适
            // console.log(count);
            state.counter += count
        },
        addStudent(state,stu) { 
            state.students.push(stu)
        },
        updateInfo(state) { 
            state.info.name = 'codewhy'
            // state.info['address'] = '洛杉矶'
            // 这里没有响应式
            // 要想让这里有响应式，可以用Vue.set方法
            // Vue.set(state.info, 'address', '洛杉矶')

            // 该方式做不到响应式
            // 删除对象的原始属性
            // delete state.info.age
            // Vue.delete(state.info,'age')

            // 错误代码：不能在这里进行异步操作
            // setTimeout(() => {
            //     state.info.name = 'codewhy'
            //     // 在mutation里面进行异步操作的话vue-devtools识别不出来
            //     // 所以不要在mutation里面进行异步操作
            // }, 1000);
        }
    },
    actions: {
        // context:上下文
        //  mutations和getters里面都有一个参数叫state,但是这里action里的参数叫context
        // 这里的context也可以当作是store
        // aUpdateInfo(context,payload) { 
        //     setTimeout(() => {
        //         // context.state.info.name = 'codewhy'
        //         // 但是也不能这样修改，修改state唯一途径就是通过mutation
        //         context.commit('updateInfo')
        //         // 使用commit会调用对应的方法
        //         // console.log(payload);
        //         console.log(payload.message);
        //         payload.success()
        //     }, 1000);
        // },
          aUpdateInfo(context,payload) { 
            return new Promise((resolve, reject) => { 
                setTimeout(() => {
                    context.commit('updateInfo')
                    console.log(payload);
                    resolve('11111111')
                }, 1000);
            })
        },

    },
    getters: {
        powerCounter(state) { 
            // getters方法和之前学的计算属性差不多
            return state.counter * state.counter
        },
        more20stu(state) { 
            return state.students.filter(s => s.age > 20)
        },
        // 我还想获取年龄大于20岁学生的个数
         more20stuLength(state) { 
            return state.students.filter(s => s.age > 20).length
        },
        //  方法2如下
        more20stuLength2(state,getters) { 
            return getters.more20stu.length
        },

        // 之前的age是写死的，现在我希望别人自己决定age是多少
        moreAgeStu(state) { 
            // return function (age) { 
            //     return state.students.filter(s=> s.age > age)
            // }

            // 简写如下：
            return age => { 
                return state.students.filter(s=> s.age > age)
            }
        }
    },

    modules: { 
        a: moduleA
}

})
// Vuex里面有一个属性叫做store


// 3.导出store对象
export default store
~~~

**mutations-types.js**

~~~javascript
export const INCREMENT = 'increment'
~~~

**App.vue**

~~~vue
<template>
  <div id="app">
    <h2>---------------------Appp内容------------------</h2>
   <!-- <h2>{{message}}</h2> -->
   <!-- <h2>{{counter}}</h2> -->
   <h2>{{$store.state.counter}}</h2>
   <!-- 而状态是在view里面显示的，也就是这里显示 -->
   <!-- <button @click='counter++'>+</button> -->
   <!-- <button @click='counter--'>-</button> -->

   <!-- <button @click="$store.state.counter++">+</button> -->
   <!-- <button @click="$store.state.counter--">-</button> -->
   <!-- 这样写可以，但是这样写不好 -->

   <button @click="addition">+</button>
   <button @click="subtraction">-</button>

    <!-- <button @click="addFive">每次加5</button> -->
    <!-- <button @click="addTen">每次加10</button> -->
    <!-- 这样写不好，定义了2个方法 -->

    <button @click="addCount(5)">每次加5</button>
    <button @click="addCount(10)">每次加10</button>
    <!--这样写比较好，只定义了1个方法 -->

    <button @click="addStudent">添加学生</button>

    <h2>---------------Appp内容：getters相关信息--------------</h2>
    <!-- <h2>{{$store.state.counter * $store.state.counter}}</h2> -->
    <h2>{{$store.getters.powerCounter}}</h2>
    <!-- 但是这样写太长了，不好 -->

    <!-- <h2>{{more20stu}}</h2> -->
    <h2>{{$store.getters.more20stu}}</h2>

    <h2>{{$store.getters.more20stu.length}}</h2>
    <!-- 我还想获取年龄大于20岁学生的个数 -->
    <!--你可以通过length拿到，但是我现在希望你通过getters来拿  -->
    <h2>{{$store.getters.more20stuLength}}</h2>
    <h2>{{$store.getters.more20stuLength2}}</h2>

    <h2>{{$store.getters.moreAgeStu(8)}}</h2>
    <!-- 这个年龄不是写死的，我可以写18，也可以写25等等，可以写任何数 -->

    <h2>--------Appp内容：info对象的内容是否是响应式的--------</h2>
    <h2>{{$store.state.info}}</h2>
    <button @click="updateInfo">修改信息</button>

   <h2>------------------Hello Vuex内容----------------------</h2>
   <hello-vuex/>
   <!-- 页面当中也可以发生一些action(行为)，比如点击事件 -->

   <!-- <hello-vuex :counter="counter"></hello-vuex> -->
   <!-- 标签里面不需要写东西(比如写插槽)的话用单标签比较清爽 -->
   <!-- 这里是把变量值传过去 -->

   <h2>--------------Appp内容:modules中的内容---------------</h2>
   <h2>{{$store.state.a.name}}</h2>
   <button @click="updateName">修改名字</button>
   <h2>{{$store.getters.fullname1}}</h2>
   <h2>{{$store.getters.fullname2}}</h2>
   <h2>{{$store.getters.fullname3}}</h2>
    <button @click="asyncUpdateName">异步修改名字</button>
  </div>
</template>

<script>
import HelloVuex from './components/HelloVuex'
import {
  INCREMENT
} from './store/mutations-types'
export default {
  components:{
    HelloVuex
  },
  data(){
    return {
      message:'我是App组件'
    }
  },
  computed:{
    // more20stu(){
    //   // return this.$store.state.students
    //   // return this.$store.state.students.filter(s=>{
    //   //   return s.age >= 20
    //   // })

    //   return this.$store.state.students.filter(s=> s.age >= 20)
    //     // 这样更加简单
    // }
  },
  methods: {
    addition(){
      this.$store.commit('increment')
    },
   subtraction(){
      this.$store.commit('decrement')
    },
    addCount(count){
      // payload:负载
      // 1.普通的提交风格
      this.$store.commit('incrementCount',count)
      // 新增一个count参数，把count传给index.js

      // 2.特殊的提交风格
      // this.$store.commit({
      //   type:'incrementCount',
      //   // count:count
      //   count,
      //   // 这个是简写
      // })
    },
    // 2种不同的提交风格最后提交到index.js里面的参数是不一样的
    addStudent(){
      const stu = {id:114,name:'alien',age:35}
      this.$store.commit('addStudent',stu)
    },
    updateInfo(){
      // this.$store.commit('updateInfo')
      // 要想办法让它经过actions

      // 1.0版
      // this.$store.dispatch('aUpdateInfo','我是payload')

      // 2.0版
      // this.$store.dispatch('aUpdateInfo',()=>{
      //   console.log('里面已经完成了');
      // })

      // 3.0版
      //  this.$store.dispatch('aUpdateInfo',{
      //    message:'我是携带的信息',
      //    success:()=>{
      //      console.log('里面已经完成了');
      //    }
      //   //  这样写不够优雅，我携带的信息和我回调的信息写到一坨去了
      //  })

      // 4.0版
      this.$store
      .dispatch('aUpdateInfo','我是携带的信息')
      .then(res=>{
        // 里面完成了提交
        console.log(res);
      })
    },
    updateName(){
       this.$store.commit('updateName','lisi')
    },
    asyncUpdateName(){
      this.$store.dispatch('aUpdateName')
    }
  }
}
</script>

<style scoped>

</style>
~~~

**main.js**

~~~javascript
import Vue from 'vue'
import App from './App'
// import Vuex from 'vuex'
import store from './store'
Vue.config.productionTip = false

// Vue.prototype.$store = store

// Vue.use(Vuex)
// 但是这样写的话代码就混在一起了


/* eslint-disable no-new */
new Vue({
  el: '#app',
  store,
  render: h => h(App)
})
~~~

### 项目结构组织

> 这个老师又把`index.js`里面的代码进行了抽取，我就不再写代码示例了。

#### 项目结构

![](Vue框架入门/279.png)

# 网络模块封装

## 主要内容

> 这里老师没有讲JSONP了，说讲过很多遍了，但是我还很不熟，需要再补充这个知识。

![](Vue框架入门/281.png)

## 模块的选择

### 选择什么网络模块

![](Vue框架入门/282.png)

## JSONP封装

> JSONP以后要花点时间再复习一下，之前学过一点，但是印象一点也不深刻，几乎是没印象了。

### JSONP

![](Vue框架入门/283.png)

### JSONP封装

![](Vue框架入门/284.png)

## 认识axios

### 为什么选择axios

![](Vue框架入门/285.png)

### axiox请求方式

![](Vue框架入门/286.png)

## 发送基本请求

### 发送get请求演示

![](Vue框架入门/287.png)

### 发送并发请求

![](Vue框架入门/288.png)

#### 示例代码

**main.js**

~~~javascript
import Vue from 'vue'
import App from './App'

import axios from 'axios'
Vue.config.productionTip = false


new Vue({
  el: '#app',
  render: h => h(App)
})


// 1.基本使用
// axios(config)
// config一般是对象类型
// axios({
//   // url: 'httpbin.org'
//   // 这里要填写一个真实的服务器地址让我们访问
//   // httpbin.org这个网站可以做很多网络请求的模拟

//   url: 'http://123.207.32.32:8000/home/multidata',
//   // 这个是老师的服务器接口
//   // axios是支持Promise的
//   // 默认情况下只传一个url的话它默认就是get请求
//   method: 'get'
//   // 老师的这个接口暂时不支持Post请求
//   // 老师这个接口考虑过跨域的问题，后面可以这样跟东西：
//   // http://123.207.32.32:8000/home/multidata&callback=json123(json123是随便写的)
//   // 老师把服务器里面的跨域给关掉了
// }).then(res => { 
//   console.log(res);
// })

// axios.get()

// axios({
//   url: 'http://123.207.32.32:8000/home/data',
//   // 专门针对get请求的参数拼接
//   params: {
//     type: 'pop',
//     page:1
//   }
// }).then(res => { 
//   console.log(res);
// })

// 2.axios发送并发请求(同时发送2个请求，希望2个请求都能拿到结果后再去完成对应的事情)
axios.all([axios({
  url:'http://123.207.32.32:8000/home/multidata'
}), axios({
  url: 'http://123.207.32.32:8000/home/data',
  params: {
    type: 'sell',
    page:1
  }
// })]).then(results => { 
//   console.log(results);
//   console.log(results[0]);
//   console.log(results[1]);

  // 也可以使用spread来写
})]).then(axios.spread((res1, res2) => { 
    console.log(res1);
    console.log(res2);
}))
~~~

### 全局配置

![](Vue框架入门/289.png)

### 常见的配置选项

![](Vue框架入门/290.png)

> GET请求对应的是URL查询对象：`params:{id:12}`,而POST请求对应的是request body(请求体):`data:{key:'aa'}`

## axios实例

### axios的实例

![](Vue框架入门/291.png)

### axios封装

![](Vue框架入门/292.png)

#### 示例代码

![](Vue框架入门/296.png)

**HelloWorld.vue**

~~~vue
<template>
    <h2>{{categories}}</h2>
</template>

<script>
import axios from 'axios'

export default {
    name:'HelloWorld',
    data(){
        return{
           categories:''
        }
    },
    created(){
        axios({
            url:'http://123.207.32.32:8000/home/multidata'
            // 写个一样的接口吧，其他的接口没有了
        }).then(res=>{
            console.log(res);
            this.categories = res;
        })
    }
}
</script>

<style scoped>
    
</style>
~~~

**request.js**

~~~javascript
<template>
    <h2>{{categories}}</h2>
</template>

<script>
import axios from 'axios'

export default {
    name:'HelloWorld',
    data(){
        return{
           categories:''
        }
    },
    created(){
        axios({
            url:'http://123.207.32.32:8000/home/multidata'
            // 写个一样的接口吧，其他的接口没有了
        }).then(res=>{
            console.log(res);
            this.categories = res;
        })
    }
}
</script>

<style scoped>
    
</style>
~~~

**App.vue**

~~~vue
<template>
  <div id="app">
      <div>{{result}}</div>
      <h2>-------------------------</h2>
      <hello-world></hello-world>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'

import axios from 'axios'
// 但是这种开发方式不好，对第三方框架依赖性太强了
// 如果我有100个组件都要发生网络请求，都要依赖axios框架，都要导入这个框架
// 如果突然有一天这个框架不再维护了，那就GG了，你得一个文件一个文件删除掉
// 所以，你千万不要在每个组件(.vue文件)里都对第三方框架有个依赖
// 解决方法是：单独搞一个文件，对它进行封装
// 之后所有的组件进行网络请求的时候都是面向我写的这个文件就可以了
export default {
  name: "App",
  components: {
    HelloWorld
  },
  data(){
    return {
      result:''
    }
  },
  // 监听这个组件什么时候创建完
  created() {
    console.log('-----------');
    axios({
      url:'http://123.207.32.32:8000/home/multidata'
    }).then(res=>{
      // console.log(res);
      this.result = res;
    })
  },
};
</script>

<style></style>
~~~

**main.js**

~~~javascript
import Vue from 'vue'
import App from './App'

import axios from 'axios'
Vue.config.productionTip = false


new Vue({
  el: '#app',
  render: h => h(App)
})


// 1.基本使用
// axios(config)
// config一般是对象类型
// axios({
//   // url: 'httpbin.org'
//   // 这里要填写一个真实的服务器地址让我们访问
//   // httpbin.org这个网站可以做很多网络请求的模拟

//   url: 'http://123.207.32.32:8000/home/multidata',
//   // 这个是老师的服务器接口
//   // axios是支持Promise的
//   // 默认情况下只传一个url的话它默认就是get请求
//   method: 'get'
//   // 老师的这个接口暂时不支持Post请求
//   // 老师这个接口考虑过跨域的问题，后面可以这样跟东西：
//   // http://123.207.32.32:8000/home/multidata&callback=json123(json123是随便写的)
//   // 老师把服务器里面的跨域给关掉了
// }).then(res => { 
//   console.log(res);
// })

// axios.get()

// axios({
//   url: 'http://123.207.32.32:8000/home/data',
//   // 专门针对get请求的参数拼接
//   params: {
//     type: 'pop',
//     page:1
//   }
// }).then(res => { 
//   console.log(res);
// })

// 2.axios发送并发请求(同时发送2个请求，希望2个请求都能拿到结果后再去完成对应的事情)

// axios.defaults.baseURL = 'http://123.207.32.32:8000'
// axios.defaults.timeout = 5000
// // 一些公共的东西才用上面的这2个请求

// // 3.使用全局的axios和对应的配置在进行网络请求
// axios.all([axios({
//   // baseURL: 'http://123.207.32.32:8000',
//   // timeout:5,
//   url:'/home/multidata'
//   // url:'http://123.207.32.32:8000/home/multidata'
// }), axios({
//   // baseURL:'http://123.207.32.32:8000',
//   // url: 'http://123.207.32.32:8000/home/data',
//   // timeout:5,
//   url: '/home/data',
//   params: {
//     type: 'sell',
//     page:1
//   }
// // })]).then(results => { 
// //   console.log(results);
// //   console.log(results[0]);
// //   console.log(results[1]);

//   // 也可以使用spread来写
// })]).then(axios.spread((res1, res2) => { 
//     console.log(res1);
//     console.log(res2);
// }))

// 有时候为了减轻服务器压力，会买很多服务器，把首页请求相关的东西放到A服务器，分类请求相关的东西放到B服务器..
// 但是如果这样干客户端需要知道A,B服务器的IP地址
// 它会弄一个反向代理服务器，不管有多少客户，它面向的都是反向代理服务器，一般是nginx服务器
// nginx服务器可以根据哪个服务器目前请求量不是很多，来决定去A服务器请求还是B服务器请求

// axios.defaults.baseURL = 'http://222.111.33.33:8000'
// // 随便编的一个服务器地址
// axios.defaults.timeout = 10000

// axios({
//   // url:'http://123.207.32.32:8000/category',
//   url:'/category'
// })

// // 4.创建对应的axios实例
// const instance1 = axios.create({
//   baseURL: 'http://123.207.32.32:8000',
//   timeout:5000
// })

// instance1({
//   url:'/home/multidata'
// }).then(res => { 
//   console.log(res);
// })

// instance1({
//   url: '/home/data',
//   params: {
//     type: 'pop',
//     page:1
//   }
// }).then(res => { 
//   console.log(res);
// })

// 我上面的这2个请求使用的都是instance1这个实例

// const instance2 = axios.create({
//   baseURL: 'http://222.111.33.33:8000',
//   // 这个是编的
//   timeout: 10000,
//   headers: {
//     // 如果你需要headers也可以写
//   }
// })

// 之前我们的代码都是在main.js里面写，现在我们要对网络请求的代码进行封装了

import { request } from './network/request'
// 5.封装一个request模块 方法1
// request({
//   url:'/home/multidata'
// }, res => { 
//     console.log(res);
// }, err => { 
//     console.log(err);
// })

// 5.封装一个request模块 方法2
// request({
//   baseConfig: {

//   },
//   success: function (res) { 

//   },
//   failure: function (err) { 

//   }
// })

// 5.封装一个request模块 方法3——最终版
request({
  url:'/home/multidata'
}).then(res => { 
  console.log(res);
}).catch(err => { 
  console.log(err);
})
~~~



## 拦截器

### 如何使用拦截器

![](Vue框架入门/293.png)

### 拦截器中都做什么呢？

![](Vue框架入门/294.png)

![](Vue框架入门/295.png)

#### 示例代码

**main.js**

~~~javascript
import Vue from 'vue'
import App from './App'

import axios from 'axios'
Vue.config.productionTip = false


new Vue({
  el: '#app',
  render: h => h(App)
})


// 1.基本使用
// axios(config)
// config一般是对象类型
// axios({
//   // url: 'httpbin.org'
//   // 这里要填写一个真实的服务器地址让我们访问
//   // httpbin.org这个网站可以做很多网络请求的模拟

//   url: 'http://123.207.32.32:8000/home/multidata',
//   // 这个是老师的服务器接口
//   // axios是支持Promise的
//   // 默认情况下只传一个url的话它默认就是get请求
//   method: 'get'
//   // 老师的这个接口暂时不支持Post请求
//   // 老师这个接口考虑过跨域的问题，后面可以这样跟东西：
//   // http://123.207.32.32:8000/home/multidata&callback=json123(json123是随便写的)
//   // 老师把服务器里面的跨域给关掉了
// }).then(res => { 
//   console.log(res);
// })

// axios.get()

// axios({
//   url: 'http://123.207.32.32:8000/home/data',
//   // 专门针对get请求的参数拼接
//   params: {
//     type: 'pop',
//     page:1
//   }
// }).then(res => { 
//   console.log(res);
// })

// 2.axios发送并发请求(同时发送2个请求，希望2个请求都能拿到结果后再去完成对应的事情)

// axios.defaults.baseURL = 'http://123.207.32.32:8000'
// axios.defaults.timeout = 5000
// // 一些公共的东西才用上面的这2个请求

// // 3.使用全局的axios和对应的配置在进行网络请求
// axios.all([axios({
//   // baseURL: 'http://123.207.32.32:8000',
//   // timeout:5,
//   url:'/home/multidata'
//   // url:'http://123.207.32.32:8000/home/multidata'
// }), axios({
//   // baseURL:'http://123.207.32.32:8000',
//   // url: 'http://123.207.32.32:8000/home/data',
//   // timeout:5,
//   url: '/home/data',
//   params: {
//     type: 'sell',
//     page:1
//   }
// // })]).then(results => { 
// //   console.log(results);
// //   console.log(results[0]);
// //   console.log(results[1]);

//   // 也可以使用spread来写
// })]).then(axios.spread((res1, res2) => { 
//     console.log(res1);
//     console.log(res2);
// }))

// 有时候为了减轻服务器压力，会买很多服务器，把首页请求相关的东西放到A服务器，分类请求相关的东西放到B服务器..
// 但是如果这样干客户端需要知道A,B服务器的IP地址
// 它会弄一个反向代理服务器，不管有多少客户，它面向的都是反向代理服务器，一般是nginx服务器
// nginx服务器可以根据哪个服务器目前请求量不是很多，来决定去A服务器请求还是B服务器请求

// axios.defaults.baseURL = 'http://222.111.33.33:8000'
// // 随便编的一个服务器地址
// axios.defaults.timeout = 10000

// axios({
//   // url:'http://123.207.32.32:8000/category',
//   url:'/category'
// })

// // 4.创建对应的axios实例
// const instance1 = axios.create({
//   baseURL: 'http://123.207.32.32:8000',
//   timeout:5000
// })

// instance1({
//   url:'/home/multidata'
// }).then(res => { 
//   console.log(res);
// })

// instance1({
//   url: '/home/data',
//   params: {
//     type: 'pop',
//     page:1
//   }
// }).then(res => { 
//   console.log(res);
// })

// 我上面的这2个请求使用的都是instance1这个实例

// const instance2 = axios.create({
//   baseURL: 'http://222.111.33.33:8000',
//   // 这个是编的
//   timeout: 10000,
//   headers: {
//     // 如果你需要headers也可以写
//   }
// })

// 之前我们的代码都是在main.js里面写，现在我们要对网络请求的代码进行封装了

import { request } from './network/request'
// 5.封装一个request模块 方法1
// request({
//   url:'/home/multidata'
// }, res => { 
//     console.log(res);
// }, err => { 
//     console.log(err);
// })

// 5.封装一个request模块 方法2
// request({
//   baseConfig: {

//   },
//   success: function (res) { 

//   },
//   failure: function (err) { 

//   }
// })

// 5.封装一个request模块 方法3——最终版
request({
  url:'/home/multidata'
}).then(res => { 
  console.log(res);
}).catch(err => { 
  console.log(err);
})
~~~















