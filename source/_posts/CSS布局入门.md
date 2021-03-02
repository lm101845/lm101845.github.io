---
title: CSS布局入门
date: 2021-02-26 17:18:41
tags: CSS布局
categories: CSS
---

(注1：现在是2021年2月26日，CSS布局目前我也只学了Flex布局，其他的，比如流式布局、rem布局、响应式等都还没看。现在就抓紧时间赶快进行一下查漏补缺吧。)

(注3：这个视频是黑马程序员刘晓强的课程，[视频链接](https://www.bilibili.com/video/BV1jJ41177aa?p=1))

[布局的几种方式（静态布局、自适应布局、流式布局、响应式布局、弹性布局）](https://www.cnblogs.com/zhuzhenwei918/p/7147303.html)

# 流式布局

## 目标

![](CSS布局入门/01.png)

## 目录

![](CSS布局入门/02.png)

## 移动端基础

### 浏览器现状

![](CSS布局入门/03.png)

### 手机屏幕现状

![](CSS布局入门/04.png)

### 常见移动端屏幕尺寸

![](CSS布局入门/05.png)

### 移动端调试方法

![](CSS布局入门/06.png)

### 总结

![](CSS布局入门/07.png)

## 视口

> 我们主要关注的是理想视口。

### 布局视口

![](CSS布局入门/08.png)

### 视觉视口

![](CSS布局入门/09.png)

### 理想视口

> 不需要用手捏着去看，也不需要左右滑动。以后移动端布局我们都是按照理想视口来设定的。理想视口是乔布斯发明的。

![](CSS布局入门/10.png)

### 总结

![](CSS布局入门/11.png)

### meta视口标签

> 如果不加`meta`视口标签，当你把网页放到移动端显示时，默认宽度是980px，那么字就会显得非常小。

![](CSS布局入门/12.png)

### 标准的viewport设置

![](CSS布局入门/13.png)

## 二倍图

### 物理像素&物理像素比

> 电脑端，1px就等于1物理像素，而手机端则不一定。比如iphone6,7,8中，1px = 2物理像素。(它们的屏幕宽为750物理像素，是375px。)

![](CSS布局入门/14.png)

![](CSS布局入门/15.png)

### 多倍图

![](CSS布局入门/16.png)

### 背景缩放

> 背景图片也是可以拉伸的。

![](CSS布局入门/17.png)

~~~html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        div{
            width: 500px;
            height: 500px;
            border: 2px solid red;
            background: url(images/logo.png) no-repeat;
            /* background-size: 图片的宽度 图片的高度; */

            /* 1.如果只写一个参数，肯定是宽度，并且高度会等比例缩放 */
            /* background-size: 500px; */

            /* 2.里面的单位可以跟%，百分比是相对于父盒子来说的 */
            /* background-size: 50%; */

            /* 3.cover：高度和宽度等比例拉伸，要完全覆盖div盒子，可能有部分背景图片显示不全*/
            /* background-size: cover; */

            /* 4.contain：高度和宽度等比例拉伸，当宽度或者高度铺满div盒子就不再进行拉伸了*/
            /* 造成的问题：可能有部分空白区域 */
            background-size: contain;
        }
    </style>
</head>
<body>
    <div></div>
</body>
</html>
~~~

### 多倍图切图神器cutterman

![](CSS布局入门/18.png)

##  移动端开发选择

### 移动端主流方案

![](CSS布局入门/19.png)

### 单独移动端页面（主流）



![](CSS布局入门/20.png)

### 响应式兼容PC移动端

![](CSS布局入门/21.png)

### 总结

![](CSS布局入门/22.png)

## 移动端技术解决方案

### 移动端浏览器

![](CSS布局入门/23.png)

###  CSS初始化 normalize.css

![](CSS布局入门/24.png)

### CSS3 盒子模型 box-sizing

![](CSS布局入门/25.png)

~~~html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        div:nth-child(1){
            /* 传统盒子模型=width+border+padding */
            width: 200px;
            height: 200px;
            background-color: pink;
            padding: 10px;
            box-sizing: content-box;
            /* 这个就是默认的传统的盒子模型 */
        }
        div:nth-child(2){
            width: 200px;
            height: 200px;
            background-color: purple;
            padding: 10px;
            border: 10px solid blue;
            /* 有了这句话就让盒子变成了CSS3盒子模型 */
            /* 这个盒子模型的宽度已经包含了border和padding */
            /* 从此以后，padding和border就不会再撑大盒子了 */
            /* 不过盒子模型是CSS3才有的，有兼容性问题 */
            box-sizing: border-box;

        }
    </style>
</head>
<body>
    <div></div>
    <div></div>
</body>
</html>
~~~

### 特殊样式

![](CSS布局入门/26.png)

## 移动端常见布局

### 移动端技术选型

![](CSS布局入门/27.png)

### 流式布局（百分比布局）

> 流式布局主要是设置元素的宽度为百分比，高度基本上不做限制，用px。

![](CSS布局入门/28.png)

~~~html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta http-equiv="X-UA-Compatible" content="IE=edge" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<title>Document</title>
		<style>
            *{
                margin: 0;
                padding: 0;
            }
            section{
                width: 100%;
                max-width: 980px;
                min-width: 320px;
                margin: 0 auto;
            }

            section div{
                width: 50%;
                /* 流式布局主要看的是宽度 */
                height: 400px;
                float: left;
            }

            section div:nth-child(1){
                background-color: pink;
            }

            section div:nth-child(2){
                background-color: purple;
            }
        </style>
	</head>
	<body>
		<section>
			<div></div>
			<div></div>
		</section>
	</body>
</html>
~~~

![](CSS布局入门/29.png)

![](CSS布局入门/30.png)

![](CSS布局入门/31.png)

![](CSS布局入门/32.png)

![](CSS布局入门/33.png)

![](CSS布局入门/34.png)

![](CSS布局入门/35.png)

![](CSS布局入门/36.png)

![](CSS布局入门/37.png)

![](CSS布局入门/38.png)

