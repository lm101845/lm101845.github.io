---
title: Vue源码入门
date: 2020-09-05 00:08:42
tags: Vue源码
categories: Vue
top:2008
---

(注1：网上找了一些资料，还是要尝试着去学学框架源码啊。"问渠那得清如许，为有源头活水来"，我们不止要会用框架，还要了解它内部的原理，看看尤雨溪是到底怎么开发出来的，对于今后的工作学习是十分有好处的啊。)

(注2：现阶段主要是搜集一些文字资料，看看别人是如何学习Vue源码的。)

(注3：等自己学到了一定的程度了，或者说看文字资料遇到了瓶颈了，就去网上找一些视频来看。我之前找过，感觉有点不好找，这个到时候再说了啊。)

(注4：但是我现在要明确一下学哪个版本的Vue源码啊，现在Vue3.0也出来了。)

(注5：现在是2021年3月1日，我现在真的要开始着手熟悉一下Vue的源码了，主要是通过看黄弈的视频以及GitHub上的这个[mini-vue](https://github.com/woai3c/mini-vue/tree/v0.1)这个项目进行学习，希望可以对Vue有更深层次的理解和熟练使用吧。)

[Vue源码阅读总结大会](https://zhuanlan.zhihu.com/p/53184632)

# 看过的Vue源码有关资料

[【Vue原理】响应式原理 - 白话版](https://mp.weixin.qq.com/s?__biz=MzUxNjQ1NjMwNw==&mid=2247483922&idx=1&sn=228ca8365d8566d59630d5bad4bf7d58&chksm=f9a6680eced1e118b628499600abd12d622083a0434673514cd5da4cc69a9325c555c051c147&scene=21#wechat_redirect)

[【Vue原理】Props - 白话版](https://zhuanlan.zhihu.com/p/53218851)

# 阅读源码前的准备

* **JavaScript 扎实基础**

* **看完《 JavaScript 设计模式》**

* **掌握 Vue 所有API**

我把 Vue 的所有 API 都详细研究使用过了一遍，而且尽量在项目中都有使用，让自己有深一点的体会

而且我对着官方文档，一个个做了详细的笔记，而且联想过了使用场景。

* **学会调试**

我很大胆地说，如果你不会调试，你看 Vue 源码，或者你会想死，你会出现这个场景："MMP，这个方法是怎么跳到 那个方法的，那个方法和 这个方法又是怎么联系起来的？"

也许你可以慢慢**使用函数名字**去寻找，但是无疑你会多消耗几倍时间，而且你会更烦。使用调试真的方便，以前我也真的不喜欢调试，觉得好像很难，更喜欢使用 `console.log`去打印信息。

是啊，我自己写项目的时候，我还是会使用` console.log `去调试，那是因为我自己代码，我知道怎么跑。你看别人的代码，还是超级抽象的框架，使用 `console.log` 的方式相信我，你会掉很多头发。

这里，我使用的是 **VSCode** 去调试，真的简单又方便，我当时也真的很难去让自己又要学一个东西,但是我咬咬牙，我还是学了，感谢自己。我可以保证，你从不懂到掌握，只要不到十分钟，简直就是现实版的十分钟精通到入门

# Vue 源码的简短总结

* **封装了很多常用的函数**

常用的**类型判断、 类型转换 、数据格式转换（数组转对象）**等等。主要目的是为了**复用**且**易维护**。

举个例子：

~~~javascript
function isObject(obj) {    return obj !== null && typeof obj === 'object'}
function isUndef(v) {    return v === undefined || v === null}
function isDef(v) {    return v !== undefined && v !== null}
function toString(val) {    
    return val == null ?    '' :    
    typeof val === 'object' ?    
    JSON.stringify(val, null, 2) :    String(val)
}
function toObject(arr) {    
    var res = {};    
    for (var i = 0; i < arr.length; i++) {        
        if (arr[i]) {
            extend(res, arr[i]);
        }
    }    return res
}
....
~~~

> 此段源码地址为：到时候找一下。

你说说不定过了几年，判断是否是一个对象，不再是什么`typeof obj == "object"`了。

如果没有封装，那岂不是所有代码涉及到的都要改一遍，且不说如果有很多个都变了，那你就头大了。

* **节点操作兼容函数**

**addClass ,removeClass，createElement，appendChild，removeChild**等。

举个例子：

~~~javascript
function addClass(el, cls) {    
    if (!cls || !(cls = cls.trim())) return
    if (el.classList) {        
        if (cls.indexOf(' ') > -1) {
            cls.split(/\s+/).forEach(function(c) { return el.classList.add(c); });
        } else {
            el.classList.add(cls);
        }

    } else {        
       var cur = " " + (el.getAttribute('class') || '') + " ";        
       if (cur.indexOf(' ' + cls + ' ') < 0) {
            el.setAttribute('class', (cur + cls).trim());
       }
    }
}
....
~~~

> 此段源码地址为：到时候找一下。

这些函数都很有用，所以我都记下来了，**毕竟是框架封装的，肯定是最完善的**。

* **真的用了很多设计模式**

就我看到的设计模式就有：观察者模式、状态模式、节流模式、 参与者模式、备忘录模式、单例模式 装饰者模式、组合继承模式、链模式等。我怀疑 Vue 把所有的设计模式都用完了。真的，如果你不懂设计模式，你真不会领悟到他这么写的精髓。(所以记得要把前面提到的书籍《 JavaScript 设计模式》看一遍啊)

我就选 Vue 常用的一个设计模式来讲：**参与者模式**。

Vue 封装的很多函数都是用了 参与者模式，也可以叫做**柯里化**。

先来简单解释下什么是参与者模式：首先保存第一次调用，传入参数。其次返回定制函数，函数内使用参数。

# 黄弈视频笔记

# mini-vue项目学习笔记

[mini-vue项目地址](https://github.com/woai3c/mini-vue/tree/v0.1)

我现在还不太会学习别人仓库里的东西，我先fork了一份，然后自己也建了一个空仓库[VueSourceCodeLearning](https://github.com/lm101845/VueSourceCodeLearning)，就打算跟着视频和这个项目从头开始写一遍Vue1.0的大体源码吧。







