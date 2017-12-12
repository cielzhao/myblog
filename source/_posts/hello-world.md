---
title: Hello World
tags:
	- 关于博客
---
一直想有一个自己的个人博客，虽然早早的申请了域名，写了一些静态页面，可自己不是设计出身，页面不是很好看，也就因此搁置了。直到前几天百度搜一个技术上遇到的问题，看到一个很好看的博客，就研究了一下，是用[GithubPages](https://github.com/)+[Hexo](https://hexo.io/)博客主题[Yilia](https://github.com/litten/hexo-theme-yilia)搭建的（请原谅我的无知，蓝朋友说他好几年前就知道hexo了😂）。进一步了解之后发现Hexo还有很多其他主题，一一看过之后觉得Yilia主题我个人更喜欢，这是作者的[博客地址](http://litten.me/)。

确定好主题之后就按照网上找的教程一步一步操作了，过程并不是很复杂，网上的教程已经足够详细，没打算再重新写一遍，我把我用到的教程列举如下：
- [廖雪峰的git教程](https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/)
- [github关联域名](https://jingyan.baidu.com/article/dca1fa6fa1e403f1a5405262.html)
- [hexo从零开始到搭建完整](http://www.cnblogs.com/visugar/p/6821777.html)

关于评论插件，之所以用[友言](http://www.uyan.cc/)，是因为没有其他选择了。其实更喜欢[畅言](http://changyan.kuaizhan.com/)的样式，yilia主题也支持配置，可无奈畅言需要域名备案，而阿里云上的域名备案需要买服务器，我是基于github搭建的，没打算买服务器，只能放弃。网上搜索其他方法，有人说可以随便找个已经备案的域名，通过审核之后再换成自己的就行，暂且不论是否可行，在未经许可的情况下用别人的备案域名总是不好的，于是放弃。后来发现有人用友言也可以配置成功，评论功能也还行，果断注册，不用域名备案，可以参考 [yilia添加友言评论功能](https://jingyan.baidu.com/article/4b52d702c8eb8dfc5d774b71.html)这篇文章添加评论功能。


搭建完成之后，运行命令
``` bash
$ hexo server
```
，在浏览器打开 http://localhost:4000 就能看到效果。
然后继续运行命令
``` bash
$ hexo clean
$ hexo generate
$ hexo deploy
```
（以上命令除了 hexo clean 之外都有简写，hexo加后一个单词的首字母即可）就可以同步到github，这时候打开域名就能看到完整效果。每次用命令同步到github上的文件只有yilia主题source目录下的文件：![image.png](http://upload-images.jianshu.io/upload_images/1657993-14ffaed82e5ef725.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

其中的CNAME不是自动生成的，要单独加进去，不然的话直接打开域名就找不到页面了。

我搭建博客的时候是在公司电脑上同步到github的，等回到家里想做一些修改的时候就遇到了问题，因为得在自己的电脑上重新安装一遍。这时候可以参考 [hexo：更换电脑，如何继续写博客](http://blog.csdn.net/eternity1118_/article/details/71194395?ref=myread)  和 [使用hexo，如果换了电脑怎么更新博客？](https://www.zhihu.com/question/21193762) 来解决问题。

我是在github上新建了一个myblog仓库来备份源文件，里边包含yilia主题仓库，因为对于一个仓库包含另一个仓库的问题并不是很了解，上传到github后主题yilia文件无法点击查看详情，在本地修改之后也push不上去，一直报错，刚开始以为是文件出了问题，最后居然傻到把整个库删了重建，结果还是一样。后来找到相关文章[【Git】子模块：一个仓库包含另一个仓库](http://www.jianshu.com/p/491609b1c426)，解决了我的困惑。

不过最后用了另外一种方法，先fork了[yilia主题](https://github.com/litten/hexo-theme-yilia)，然后在其基础上修改提交，但这么做的前提是自己的博客themes文件夹下clone的是自己frok过来的主题，而不是原作者的。我是因为不想在一个库里来回切换分支才这么做的，这是蓝朋友提出来的方法，在此非常感谢。

每次"HelloWorld"运行成功的时候，都是一个新的开始。一直想有一个自己的个人博客，虽然早早的申请了域名，写了一些静态页面，可自己不是设计出身，页面不是很好看，也就因此搁置了。直到前几天百度搜一个技术上遇到的问题，看到一个很好看的博客，就研究了一下，是用[GithubPages](https://github.com/)+[Hexo](https://hexo.io/)博客主题[Yilia](https://github.com/litten/hexo-theme-yilia)搭建的（请原谅我的无知，蓝朋友说他好几年前就知道hexo了😂）。进一步了解之后发现Hexo还有很多其他主题，一一看过之后觉得Yilia主题我个人更喜欢，这是作者的[博客地址](http://litten.me/)。

确定好主题之后就按照网上找的教程一步一步操作了，过程并不是很复杂，网上的教程已经足够详细，没打算再重新写一遍，我把我用到的教程列举如下：
- [廖雪峰的git教程](https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/)
- [github关联域名](https://jingyan.baidu.com/article/dca1fa6fa1e403f1a5405262.html)
- [hexo从零开始到搭建完整](http://www.cnblogs.com/visugar/p/6821777.html)

关于评论插件，之所以用[友言](http://www.uyan.cc/)，是因为没有其他选择了。其实更喜欢[畅言](http://changyan.kuaizhan.com/)的样式，yilia主题也支持配置，可无奈畅言需要域名备案，而阿里云上的域名备案需要买服务器，我是基于github搭建的，没打算买服务器，只能放弃。网上搜索其他方法，有人说可以随便找个已经备案的域名，通过审核之后再换成自己的就行，暂且不论是否可行，在未经许可的情况下用别人的备案域名总是不好的，于是放弃。后来发现有人用友言也可以配置成功，评论功能也还行，果断注册，不用域名备案，可以参考 [yilia添加友言评论功能](https://jingyan.baidu.com/article/4b52d702c8eb8dfc5d774b71.html)这篇文章添加评论功能。


搭建完成之后，运行命令
``` bash
$ hexo server
```
，在浏览器打开 http://localhost:4000 就能看到效果。
然后继续运行命令
``` bash
$ hexo clean
$ hexo generate
$ hexo deploy
```
（以上命令除了 hexo clean 之外都有简写，hexo加后一个单词的首字母即可）就可以同步到github，这时候打开域名就能看到完整效果。每次用命令同步到github上的文件只有yilia主题source目录下的文件：![image.png](http://upload-images.jianshu.io/upload_images/1657993-14ffaed82e5ef725.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

其中的CNAME不是自动生成的，要单独加进去，不然的话直接打开域名就找不到页面了。

我搭建博客的时候是在公司电脑上同步到github的，等回到家里想做一些修改的时候就遇到了问题，因为得在自己的电脑上重新安装一遍。这时候可以参考 [hexo：更换电脑，如何继续写博客](http://blog.csdn.net/eternity1118_/article/details/71194395?ref=myread)  和 [使用hexo，如果换了电脑怎么更新博客？](https://www.zhihu.com/question/21193762) 来解决问题。

我是在github上新建了一个myblog仓库来备份源文件，里边包含yilia主题仓库，因为对于一个仓库包含另一个仓库的问题并不是很了解，上传到github后主题yilia文件无法点击查看详情，在本地修改之后也push不上去，一直报错，刚开始以为是文件出了问题，最后居然傻到把整个库删了重建，结果还是一样。后来找到相关文章[【Git】子模块：一个仓库包含另一个仓库](http://www.jianshu.com/p/491609b1c426)，解决了我的困惑。

不过最后用了另外一种方法，先fork了[yilia主题](https://github.com/litten/hexo-theme-yilia)，然后在其基础上修改提交，但这么做的前提是自己的博客themes文件夹下clone的是自己frok过来的主题，而不是原作者的。我是因为不想在一个库里来回切换分支才这么做的，这是蓝朋友提出来的方法，在此非常感谢。

每次  "HelloWorld" 运行成功的时候，都是一个新的开始。
















