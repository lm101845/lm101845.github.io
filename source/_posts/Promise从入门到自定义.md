---
title: Promise从入门到自定义
date: 2020-10-25 15:55:10
tags: Promise
categories: 前端理论
---

(注1：网上看到有个视频，单独讲Promise的，时长7个小时，感觉很不错，Promise也值得单独好好的学习一下，需要深刻的了解一下到底什么是异步编程。)

(注2：视频链接：[尚硅谷Promise教程(promise前端进阶必学)](https://www.bilibili.com/video/BV1MJ41197Eu/?spm_id_from=333.788.videocard.8)，看弹幕老师好像叫张晓飞)

(注3：听了2节课，发现老师讲的课程质量是真的好，一下子有种茅塞顿开的感觉，很不错的一套课程。)

# 第1章：准备工作

> 现在去中大型企业面试前端工程师，问的最多的问题之一就是手写自定义Promise。
>
> 第1章准备工作表面上和学习promise关系不大，但是后面是会用到的。

## 区分实例对象与函数对象

* 实例对象：new函数产生的对象，称为实例对象，简称为对象
* 函数对象：将函数作为对象使用时，简称为函数对象

~~~javascript
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>01_准备_函数对象与实例对象</title>
</head>

<body>

  <script>
    /* 
    1. 函数对象与实例对象
      函数对象: 将函数作为对象使用时, 简称为函数对象
      实例对象: new 函数产生的对象, 简称为对象(实例对象)
    */

    function Fn() {
      // 第一步我先定义了一个函数
      // 现在我还不能说它是一个构造函数
    }

    const fn = new Fn()
    // 再写个这个才能说Fn是构造函数,而fn是实例对象
    // 大写只是起一个暗示作用
    // 主要看你在调用执行这个函数的时候，函数左边有没有加new

    console.log(Fn.prototype);
    // 你怎么知道你在使用一个函数？？——你的括号()左边肯定是一个函数
    // 比如a()[0]()表示：首先a是一个函数，它的返回值是一个数组，数组的第一个参数还是函数
    // 我们要先看懂语法，其次再看懂功能。

    // 括号的左边必然是函数，而点的左边必然是对象
    // 则此时Fn不是函数了，它现在的角色是一个对象(但它本身是一个函数)
    // 那Fn就称为函数对象
    // 我们知道函数本身就是一个对象，但是我们加括号的时候不能体现出它对象的特点，加点的时候才能体现它对象的特点。


    // function Person(params) {

    // }

    // const p = new Person()
    // p是Person的实例对象

    Fn.bind({})     //Fn是函数对象
    // 我们调用Fn函数对象的bind方法
    // 此时这里的Fn不是函数的角色，而是对象的角色了
    // 注意：只有函数对象才有bind方法！！！用于改变函数的this指向。
    // 实例对象(如fn)是没有bind方法的！！！！
    // 为什么所有的函数对象都有bind方法呢？说明它在Function的原型上。
    // 我们所有的函数都是Function的实例，实例就会找原型对象的方法

    Fn.call({})     //Fn是函数对象
    // 从语法上我们执行的是Fn这个函数对象的call方法
    // 但是从功能上来说最终它是会执行Fn这个函数的 
    // 而且指定this作为第一个参数的值

    $('#test')    //jQuery函数
    // 这个是jQuery语法
    // 括号的左边是函数，点的左边是对象，所以$是函数
    // 说白了jQuery从语法上是一个函数

    $.get('./test')     // jQuery函数对象
    // 这个是调用$(jQuery函数对象)的方法


    // 综上：我既可以将函数作为函数使用，也可以将函数作为对象使用
  </script>
</body>

</html>
~~~

## 两种类型的回调函数

> 不是所有的回调函数都是异步的，有的是同步的(`forEach`)，有的是异步的(`setTimeout`)

有3个条件同时满足才能算是回调函数：

* 你定义的
* 你没有调用
* 但是最终执行了 

### 同步回调

* 理解：立即执行，完全执行完了才结束，不会放入回调队列中

* 例子：数组遍历相关的回调函数/Promise的excutor函数

### 异步回调

* 理解：不会立即执行，会放入回调队列中将来执行
* 例子：`setTimeout`函数

~~~javascript
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>02_准备_回调函数的分类</title>
</head>

<body>
  <script>
    /*
    1). 同步回调:
      理解: 立即执行, 完全执行完了才结束, 不会放入回调队列中
      例子: 数组遍历相关的回调函数 / Promise的excutor函数
    2). 异步回调:
      理解: 不会立即执行, 会放入回调队列中将来执行
      例子: 定时器回调 / ajax回调 / Promise的成功|失败的回调
    */

    //  1.同步回调函数
    // const arr = [1, 3, 5]
    // arr.forEach(item => {
    //  同步回调函数，不会放入队列执行，一上来就要执行完 
    //   // 遍历的回调函数：每取出一个元素就调用一次
    //   console.log(item);
    //   // 先执行这个
    //   // 这个foreach内部是要把里面所有的元素都编译并且调用这个回调函数，才开始后面的代码
    //   // 所以这个函数是同步回调函数
    // })
    // console.log('forEach()之后');
    // 再执行这个

    //  2. 异步回调函数
    setTimeout(() => {
      console.log('timeout callback');
      // 这个后面才执行
      // 异步回调函数会放入队列中将来执行
    }, 0);
    console.log('setTimeout()之后');
    // 这个时候下面的先执行
  </script>
</body>

</html>
~~~

## JS的错误处理

[Error](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Error)

### 错误的类型

* Error：所有错误的父类型
* ReferenceError：引用的变量不存在
* TypeError：数据类型不正确的错误
* RangeError：数据值不在其所允许的范围内
* SyntaxError：语法错误

~~~javascript
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>JS的error处理</title>
</head>

<body>

  <script>
    /*
    目标: 进一步理解JS中的错误(Error)和错误处理
      1. 错误的类型
          Error: 所有错误的父类型
          ReferenceError: 引用的变量不存在
          TypeError: 数据类型不正确的错误
          RangeError: 数据值不在其所允许的范围内
          SyntaxError: 语法错误
      2. 错误处理
          捕获错误: try ... catch
          抛出错误: throw error
      3. 错误对象
          message属性: 错误相关信息
          stack属性: 函数调用栈记录信息
    */

    // 1.常见的内置错误
    //  1) ReferenceError: 引用的变量不存在
    // console.log(a);
    //Uncaught ReferenceError: a is not defined
    // Uncaught表示没有被处理，下面的输出-----不会被执行
    // 没有捕获error,下面的代码不会执行
    // console.log('------');

    // 2)TypeError: 数据类型不正确的错误
    // let b = null
    // console.log(b.xxx);
    // null是没有属性的
    // Uncaught TypeError: Cannot read property 'xxx' of null
    // 意思说你想要读取属性，你得是个对象

    // let c = {}
    // c.xxx()
    //Uncaught TypeError: c.xxx is not a function

    // 3)RangeError: 数据值不在其所允许的范围内
    // function fn() {
    //   fn()
    //   // 函数内部调用自己——递归调用
    //   // 正常的递归调用是有一定的限制的
    //   // 你这样调就是个死循环
    // }
    // fn()
    //Uncaught RangeError: Maximum call stack size exceeded
    // 函数里面调函数，嵌套层级是有一定的限制的(你只能调用多少次)
    // 因为你是死循环，无限次调用，所以就超出了这一限制

    // 4)SyntaxError: 语法错误
    // const c = """"
    // Uncaught SyntaxError: Unexpected string
  </script>
</body>

</html>
~~~

### 错误处理

> 你写代码肯定会遇到错误的，遇到错误如果不进行处理的话，程序就会卡在这里，没有办法继续往下执行。
>
> 讲的好啊！！我以前对抛出异常这块不太理解，现在算是彻彻底底的懂了，这老师讲的是真的好。

~~~javascript
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>JS的error处理</title>
</head>

<body>

  <script>
    /*
    目标: 进一步理解JS中的错误(Error)和错误处理
      mdn文档: https: //developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Error
  
      1. 错误的类型
          Error: 所有错误的父类型
          ReferenceError: 引用的变量不存在
          TypeError: 数据类型不正确的错误
          RangeError: 数据值不在其所允许的范围内
          SyntaxError: 语法错误
      2. 错误处理
          捕获错误: try ... catch
          抛出错误: throw error
      3. 错误对象
          message属性: 错误相关信息
          stack属性: 函数调用栈记录信息
    */

    // 2.错误处理
    // 2.1捕获错误(系统自己抛出错误)：try...catch
    // 把有可能出问题的代码塞在这个try...catch中的try里面
    try {
      let d
      console.log(d.xxx);
    } catch (error) {
      //具体catch到什么error我不用管，我就写个名字
      // 在JS里面也不用声明类型，可以这样写
      // console.log(error);
      // 这里error是一个对象(里面有一些属性)
      // TypeError: Cannot read property 'xxx' of undefined

      console.log(error.message);
      console.log(error.stack);
    }

    console.log('出错后还可以继续往下执行');
    // 因为错误已经被捕获处理了，所以出错后还可以继续往下执行

    // 2.2抛出错误: throw error
    function something() {
      // 我想做一件事情：
      // 如果当前时间是奇数，这个函数继续执行
      // 如果当前时间是偶数，则这个函数就停下来，不能做了
      // 但是不能做了需要外部进行一个提示，我自己不知道怎么提示
      if (Date.now() % 2 == 1) {
        console.log('当前时间为奇数，可以继续执行任务')
      } else {
        // 时间为偶数，我处理不了，由调用者来处理
        // 如果我内部可以决定怎么提示的话，就没有必要抛出异常了
        // 但是我处理不了，怎么提示我不知道，得由外部调用者来去决定
        // 你是打印输出，还是alert，还是弹个框，你自己来决定
        throw new Error('当前时间为偶数，无法执行任务')
        // 我们在抛出异常的时候，一般都用Error笼统的类型，而不用ReferenceError等具体的类型

      }
    }

    try {
      something()
      // 这个执行调用函数内部有可能抛出异常(时间为偶数时)
      // 所以我要捕获处理异常,要把这个可能出错的函数放到try...catch里

    } catch (error) {
      // 这个参数error随便叫什么都行
      alert(error.message)
      // 我可以选择打印输出，还可以选择alert等
    }
  </script>
</body>

</html>
~~~

![](Promise从入门到自定义/01.png)

# 第2章：Pormise的理解和使用

## Promise是什么(what)

### 理解

* 抽象表达
  * Promise是JS中进行异步编程的新的解决方案（旧的是谁？——纯回调形式[Promise里面也有回调形式]）
* 具体表达
  * 从语法上来说：Promise是一个构造函数(将来可以创建它的实例，一旦是构造函数了，肯定是它的实例去做什么事情。而一般的函数，那就是具体的那个函数去做什么事情了。)
  * 从功能上来说：**promise对象**用来封装一个异步操作**并**可以获取其结果

### Promise的状态改变

[这一次，彻底弄懂 Promise 原理](https://juejin.im/post/6844904063570542599)

* pending变为resolved
* pending变为rejected

说明：resolve和reject是函数名，resolved和rejected是状态名，而且状态改变只有这2种，且一个promise对象**只能改变一次状态**，无论变为成功还是失败，都会有一个结果数据。成功的结果数据一般称为vlaue，失败的结果数据一般称为reason。

### Promise的基本流程

![](Promise从入门到自定义/02.png)

### Promise的基本使用

~~~javascript
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Promise的基本使用</title>
</head>

<body>
    <script>
        // 1. 创建一个新的Promise对象
        const p = new Promise((resolve, reject) => {
         	 // 执行器函数，同步回调
            console.log('执行 excutor');
            // 写变量时尽量先用const，后面发现有改变的话再改成let

            // 这个回调函数传入的2个参数起的名字一般很固定：resolve和reject
            // 它们2个都是函数类型
            // 这个函数有一个统一的称谓，叫执行器函数：用来执行异步操作

            // 2.执行异步操作任务(有可能成功，有可能失败)
            // 使用setTimeout来模拟异步任务
            setTimeout(() => {
                const time = Date.now()
                // 设置：如果当前时间为偶数就代表成功，否则代表失败

                // 3.1如果成功了，调用resolve(value)函数
                if (time % 2 == 0) {
                    resolve('成功的数据,time=' + time)
                } else {
                    // 3.2如果失败了，调用reject(reason)函数 
                    reject('失败的数据,time=' + time)
                }
            }, 1000);

        })
				console.log('new Promise()之后');
        p.then(
            // 不是我主动去取数据，而是它交给我
            value => {
                // 接收得到成功的value数据  onResolved
                // 英文on:当什么什么的时候
                console.log('这是成功的回调', value);
            },
            reason => {
                // 接收得到失败的reason数据 onRejected
                console.log('这是失败的回调', reason);
            }
        )
    </script>
</body>

</html>
~~~

## 为什么要用Promise(why)

> 这节课没怎么听懂。

[关于js的回调、同步回调、异步回调](https://segmentfault.com/a/1190000009391074)

### 指定回调函数的方式更加灵活

* 旧的：必须在启动异步任务前指定
* promise：启动异步任务=>返回promie对象=>给promise对象绑定回调函
  数（甚至可以在异步任务结束后指定/多个）

### 支持链式调用，可以解决回调地狱问题

* 什么是回调地狱？
  * 回调函数嵌套调用，外部回调函数异步执行的结果是嵌套的回调执行的条件
* 回调地狱的缺点？
  * 不便于阅读，不便于异常处理
* 解决方案？
  * promise链式调用
* 终极解决方案？
  * async/await

~~~javascript
/* 
    1. 指定回调函数的方式更加灵活: 
      旧的: 必须在启动异步任务前指定
      promise: 启动异步任务 => 返回promie对象 => 给promise对象绑定回调函数(甚至可以在异步任务结束后指定)
*/
const p = new Promise((resolve, reject) => {
    console.log('执行 executor同步函数') 
    let time = Date.now();
    setTimeout(() => {
        if (time % 2 === 0) {
            resolve(time)
        } else {
            reject(time)
        }
    }, 1000)

})

setTimeout(() => {
    p.then(value => {
        console.log('value', value)
    }, reason => {
        console.log('reason', reason)
    })
}, 3000)
/* 2. 支持链式调用, 可以解决回调地狱问题
    什么是回调地狱? 回调函数嵌套调用, 外部回调函数异步执行的结果是嵌套的回调函数执行的条件
    回调地狱的缺点?  不便于阅读 / 不便于异常处理
    解决方案? promise链式调用
    终极解决方案? async/await
  */

//1、查出当前用户信息
//2、按照当前用户的id查出他的课程
//3、按照当前课程id查出分数
// 回调地狱：
$.ajax({
    url: "./mock/user.json",
    success(data) {
        console.log("查询用户：", data);
        $.ajax({
            url: `./mock/user_corse_${data.id}.json`,
            success(data) {
                console.log("查询到课程：", data);
                $.ajax({
                    url: `./mock/corse_score_${data.id}.json`,
                    success(data) {
                        console.log("查询到分数：", data);
                    },
                    error(error) {
                        console.log("出现异常了：" + error);
                    }
                });
            },
            error(error) {
                console.log("出现异常了：" + error);
            }
        });
    },
    error(error) {
        console.log("出现异常了：" + error);
    }
});

// promise调用方式
function get(url, data) {
    return new Promise((resolve, reject) => {
        $.ajax({
            url: url,
            data: data,
            success: function (data) {
                resolve(data);
            },
            error: function (err) {
                reject(err)
            }
        })
    });
}

//调用封装后的方法
get("./mock/user.json")
    .then((data) => {
        console.log("用户查询成功~~~:", data)
        return get(`./mock/user_corse_${data.id}.json`);
    })
    .then((data) => {
        console.log("课程查询成功~~~:", data)
        return get(`./mock/corse_score_${data.id}.json`);
    })
    .then((data) => {
        console.log("课程成绩查询成功~~~:", data)
    })
    .catch((err) => {
        console.log("出现异常", err)
    });
// Promise操作明显更加符合我们人类的习惯，类似于流水线式的操作,对于异常的处理更加友好
~~~

## 如何使用Promise(how)

### API

* Promise构造函数：`Promise（excutor）{}`
* 

# 第3章：自定义(手写)Promise

# 第4章：async与await

# 第5章：JS异步之宏队列与微队列

# 第6章：Promise相关面试题