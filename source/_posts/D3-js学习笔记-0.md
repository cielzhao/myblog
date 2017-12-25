---
title: D3.js学习笔记
date: 2017-12-21 23:39:59
tags:
	- D3
---
项目中要用到 [D3.js](https://d3js.org/)，个人也比较感兴趣，于是在空闲的时间开始学习，目前 D3.js 已经更新到了4.0版本，这是在网上找的 [D3.js V4版本中文参考文档](https://github.com/xswei/d3js_doc)，还有这个[D3.js 4.x 中文手册](https://github.com/tianxuzhang/d3.v4-API-Translation#hierarchies)，里边的内容都很详细。

但是如果是想找入门级基础教程的话，推荐极客学院的 [D3.js 入门教程](http://wiki.jikexueyuan.com/project/d3wiki/)，有实例和效果图，简单易懂，可以跟着自己实现一遍，不好的一点就是这个教程是 V3 版本的，其实最基础的部分都相差不多。还有[十二月咖啡馆](http://d3.decembercafe.org/index.html)的这个教程。如果调用的是 V4 版本的 js，可能会出现一些问题，大多是因为新版本的 api 变动。有些在网上找到了答案，有些没有。在此先把遇到的问题记录下来，后面有进展了再更新。
1.API变动
- d3.svg.axis().scale(xScale).orient("bottom")  -> d3.axisBottom(xScale)
- ease("bounce") -> ease(d3.easeBounce)
- d3.layout.pie()  -> d3.pie()
- d3.svg.arc() -> d3.arc()
- d3.scale.category10() -> d3.scaleOrdinal(d3.schemeCategory10)
- d3.layout.force() -> d3.forceSimulation()

2.写法报错
 - attr({})一次赋值多个属性会报错，style({})一次修改多个样式的写法也会报错，挨个写不会出问题，attr().attr()；style().style()。
