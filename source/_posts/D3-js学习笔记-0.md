---
title: D3.js学习笔记
date: 2017-12-21 23:39:59
tags:
	- D3
---
项目中要用到 [D3.js](https://d3js.org/)，个人也比较感兴趣，于是在空闲的时间开始学习，目前 D3.js 已经更新到了4.0版本，这是在网上找的 [D3.js V4版本中文参考文档](https://github.com/xswei/d3js_doc)，里边的内容很详细。

但是如果是想找入门级基础教程的话，推荐极客学院的 [D3.js 入门教程](http://wiki.jikexueyuan.com/project/d3wiki/)，有实例和效果图，简单易懂，可以跟着自己实现一遍，不好的一点就是这个教程是 V3 版本的，其实最基础的部分都相差不多。如果调用的是 V4 版本的 js，可能会出现一些问题，大多是因为新版本的 api 变动。有些在网上找到了答案，有些没有。在此先把遇到的问题记录下来，后面有进展了再更新。
1. Axes
- V3：d3.svg.axis().scale(xScale).orient("bottom"); 
- V4：d3.axisBottom(xScale)

2.Transitions
- V3：d3.svg.transition().duration(2000).ease("bounce")
- V4：d3.svg.transition().duration(2000).ease(d3.easeBounce)
