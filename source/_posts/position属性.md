---
title: position属性
date: 2017-12-18 21:34:25
tags: 
 - css
---
position 属性在页面布局定位元素的时候会经常用到，自以为已经运用的很熟练，直到有一天发现对 relative 的理解居然有错，于是在 [W3school](www.w3school.com.cn/cssref/pr_class_position.asp) 上重新看了一遍教程。在此记录一下自己的理解，加深印象。

position 属性规定元素的定位类型，可能的值有五个，分别是 static, inherit, relative, absolute, fixed。所有主流浏览器都支持 position 属性，但任何版本的 Internet Explorer （包括 IE8）都不支持属性值 "inherit"。
- static
static 有静止的意思，顾名思义就是元素
没有定位，这个属性值是 position 的默认值，一般很少给元素写出这个默认属性，但如果用 js 去获取 position 属性值的话会获取到值为 static。此时元素出现在正常的文档流中，top, bottom, left, right 或者 z-index 声明均会被忽略，没有效果。

- relative
生成相对定位的元素，相对于其正常位置进行定位。例如，"left:20" 会向元素的 left 位置添加 20 像素。

- absolute	
生成绝对定位的元素，相对于 static 定位以外的第一个父元素进行定位。元素的位置通过 "left", "top", "right" 以及 "bottom" 属性进行规定。

- fixed
生成绝对定位的元素，相对于浏览器窗口进行定位。元素的位置通过 "left", "top", "right" 以及 "bottom" 属性进行规定。

- inherit
规定应该从父元素继承 position 属性的值。

以上属性值对应的效果可以在 [codepen](https://codepen.io/cielzhao/pen/ppywmg) 上自己进行调试。