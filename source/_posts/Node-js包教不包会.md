---
title: Node.js包教不包会
date: 2020-10-18 22:53:34
tags: Node.js
categories: 前端理论
---

(注1：这是Github上的一个关于Node.js的一个实战项目课程，[项目地址](https://github.com/alsotang/node-lessons)，和前面看的理论课程可以起到一个互补的作用，我准备起码把Node.js的视频看完了再来弄这个，大体看了一下，作者推荐使用Linux或者Mac去完成这一系列课程，用Windows可能会发生一些无法预料的兼容性bug问题，那到时候我就开虚拟机用Linux好了。)

(注2：现在是2020年12月16日，我Node.js的视频还没有看完，只看了一半，学到Express了，不过学着学着总感觉很虚，学了以后感觉跟没学一样，总感觉悬在半山腰一样，Node.js不是那么好学啊。)

# 第0课：搭建 Node.js 开发环境

本课程假设大家都是在 Linux 或者 Mac 下面。至于使用 Windows 并坚持玩新技术的同学，我坚信他们一定有着过人的、甚至是不可告人的兼容性 bug 处理能力，所以这部分同学麻烦在课程无法继续时，自行兼容一下。

> 我现在也没时间弄Linux了，我的Linux版本是Debian，没有界面，本来操作就不熟悉，用Linux学Node花的时间肯定更多，那就在Windows下面弄吧，这个作者感觉有点厌恶Windows啊？

不久前公司刚发一台新 Mac 给我，所以我对于在新环境中安装 Node.js 的过程还是记忆犹新的。

其实这过程特别简单:

## 先安装一个[nvm]( https://github.com/creationix/nvm )

~~~shell
$ curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.25.2/install.sh | bash
~~~

nvm 的全称是 **Node Version Manager**，之所以需要这个工具，是因为 Node.js 的各种特性都没有稳定下来，所以我们经常由于老项目或尝新的原因，需要切换各种版本。

安装完成后，你的 shell 里面应该就有个 nvm 命令了，调用它试试

