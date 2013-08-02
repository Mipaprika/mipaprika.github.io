---
layout: post
title: 这个博客是怎样搭建的
category: life
---

上学的时候尝试过用Wordpress搭建了一个博客，当时完全不知道搭建一个独立博客需要什么东西，在网上一点一点查了出来。最后发现其实根本没有什么难度，不外乎是需要一个域名，一个空间以及Wordpress就可以了，写和发布文章跟普通的博客一模一样。

前段时间开始学Ruby，想要好好做点笔记，用的Blogger，但是编辑器实在难用，想起以前公司里的同事几乎都用的Github，于是又心痒痒的要自己搭建一个了，没想到却掉进了一个大坑里。

用[Github pages](http://pages.github.com/)倒是不用满世界去找免费空间，但是搭建的过程比我想象中要费劲许多，遇到了很多奇奇怪怪的问题。这里就把这个搭建的过程记录下来。

###0. Github pages是什么###

Github pages让你可以为自己Github上的项目建立介绍页面。想想看，当你看到对方扔过来的一堆项目源码的时候是多么的头疼，但是如果是一个介绍页面会轻松许多。而特意去为一个项目搭建网站显得有点鸡肋，如果Github能顺便给我们搭建一个该有多好。于是就有了Github pages。

Github还允许我们搭建唯一的一个用于私人用途而非项目用途的个人网站，只需要新建一个repository，并且命名为`username.github.io`或者`username.github.com`就可以了。所以我们的网站上的所有内容都将会放在Github上，什么样式文件啦，博文啦，都在里面。在本地用自己喜欢的编辑器写好一篇博文，push上去就算发表了。这篇文章就是讲如何搭建这个个人网站。

###1. 申请Github账号并创建好repository###

废话。然后新建一个repository，以我为例，命名为mipaprika.github.io。clone到本地。

如果不知道Git命令怎么用的，建议学习这本[Pro Git](http://git-scm.com/book)，有中文版，mobi，pdf，epub可供下载。另外还有个在线学习的地儿[Try Git](http://try.github.io/) 

###2. 从哪里入手及目录结构###

从哪里入手？当然我们首先需要一个主页。创建一个`index.html`在`mipaprika.github.io`目录下就可以了。怎样在本地看看效果如何？

####2.1 把该安装的安装齐全了####

为了能在本地运行，我们需要先安装Ruby(Windows用户[点此下载railsinstaller](http://rubyforge.org/frs/?group_id=167))，然后是[Jekyll](http://jekyllrb.com/)，使用命令`gem install jekyll`即可。

`jekyll server`，然后访问`localhost:4000`看看是不是已经能够看到主页了？

####2.2 目录结构####

由于使用的是Jekyll来搭建博客，按照它的规范来就可以生成html页面了。

生成Pygments css的命令：`pygmentize -S monokai -f html > syntax.css`