---
title: 读书笔记：深入理解ES6
date: 2020-09-11 13:20:00
tags: ES6
categories: ES6
---

(注1：这本书跳着看。)

# 第七章：Set和Map

JS的大部分历史时期都只存在一种**集合类型**，也就是**数组类型**（尽管有人会争论说，所有非数组的对象都是键值对的集合，它们曾被用于与数组完全不同的用途）。数组在JS中的使用正如其他语言的数组一样，但缺少更多类型的集合导致数组也经常被当作队列与栈来使用。数组只使用了数值型的索引，而如果非数值型的索引是必要的，开发者便会使用非数组的对象。这种技巧引出了非数组对象的定制实现，即Set与Map。

Set是不包含重复值的列表。你一般不会像对待数组那样来访问Set中的某个项；相反更常见的是，只在Set中检查某个值是否存在。Map则是键与相对应的值的集合。因此，Map中的每个项都存储了两块数据，通过指定所需读取的键即可检索对应的值。Map常被用作缓存，存储数据以便此后快速检索。由于Set与Map并不正式存在于ES5中，开发者就只能使用非数组的对象。

ES6向JS添加了Set与Map，本章将论述这两种集合类型你所需了解的全部内容。首先，我会论述在ES6之前开发者为了实现Set与Map而采用的变通方法，并且这些方法为何是有问题的。在论述这些重要的背景之后，我会介绍Set与Map在ES6中如何工作。

## ES5 中的 Set 与 Map

在 ES5 中，开发者使用对象属性来模拟 Set 与 Map ，就像这样：

[Object.create()](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Object/create)

[Object.create()和new object()和{}的区别](https://www.cnblogs.com/leijee/p/7490822.html)

~~~javascript
let set = Object.create(null);
set.foo = true;

// 检查属性的存在性
if (set.foo) {
	// 一些操作
}
~~~

本例中的  set  变量是一个原型为  null  的对象，确保在此对象上没有继承属性。使用对象的属性作为需要检查的唯一值在 ES5 中是很常用的方法。当一个属性被添加到  set  对象时，它的值也被设为  true  ，因此条件判断语句（例如本例中的  if  语句）就可以简单判断出该值是否存在。

使用对象模拟 Set 与模拟 Map 之间唯一真正的区别是所存储的值。例如，以下例子将对象作为 Map 使用：

~~~javascript
let map = Object.create(null);
map.foo = "bar";

// 提取一个值
let value = map.foo;
console.log(value); // "bar"
~~~

此代码将字符串值  "bar"  存储在  foo  键上。与 Set 不同， Map 多数被用来提取数据，而不是仅检查键的存在性。