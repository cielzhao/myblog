---
title: Hexo博客主题Yilia更换Gitment评论系统
date: 2017-12-25 23:38:27
tags:
	- 关于博客
---
搭建这个博客的时候本来用了友言评论系统，刚开始还可以使用，可是没过几天就打不开了，出现下面的报错信息，![error1.png](https://upload-images.jianshu.io/upload_images/1657993-662edf6ec4fd5164.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)在线客服联系不上，进到友言微博里看到很久没有更新过动态，也不知道有没有在继续维护。

还是稍微有些强迫症，总觉得没有评论的话这个博客不是很完整。于是又在网上搜了很多相关信息，找到了 [Gitment](https://github.com/imsun/gitment) 这个解决方案；虽然 Gitment 只能使用 GitHub 账号进行评论，但是基本可以满足需求。然后发现 yilia 主题的_config.yml文件里本来就有对应 Gitment 的配置项。。。应该是刚开始的时候没注意到这个地方，找到的教程时间比较早，当时 yilia 主题配置项里还没有加上 Gitment，所以教程里也没有对应的配置步骤。这个，，，真的是绕了一大圈啊😂。

Gitment 是作者实现的一款基于 GitHub Issues 的评论系统，这是[作者的个人博客](https://imsun.net/posts/gitment-introduction/)，里边有详细的使用教程和相关问题说明。因为是基于 GitHub Issues 的，所以需要注册 [OAuth Application](https://github.com/settings/applications/new) ，如果注册时对需要填写的信息不是特别清楚，可以参考 csdn 上的 [Gitment](https://blog.csdn.net/anttu/article/details/77688004) 这篇文章进行注册。整个过程非常简单，几分钟就能搞定。

最后放一个测试成功的截图吧。
![image.png](https://upload-images.jianshu.io/upload_images/1657993-ff1ff4b0e716dbfc.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)







