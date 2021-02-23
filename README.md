

博客的搭建教程修改自 [Hux](https://github.com/Huxpro/huxpro.github.io) 以及 [qiubaiying](https://github.com/qiubaiying/qiubaiying.github.io)，感谢二位大神！
 
更为详细的教程戳这 [《利用 GitHub Pages 快速搭建个人博客》](http://www.jianshu.com/p/e68fba58f75c) 或 [wiki](https://github.com/qiubaiying/qiubaiying.github.io/wiki/%E5%8D%9A%E5%AE%A2%E6%90%AD%E5%BB%BA%E8%AF%A6%E7%BB%86%E6%95%99%E7%A8%8B)

快速搭建简单、简洁、美观的个人博客~

[![](img/website-capture.png)](https://hellocode.ink/)

>
### [查看博客戳这里 👆](https://hellocode.ink/)


## 使用

* 开始
	* [开始](#开始)
	* [撰写博文](#撰写博文)
	* [绑定域名](#绑定域名)
* 组件
	* [侧边栏](#侧边栏)
	* [社交账号](#社交账号)
	* [好友链接](#friends)
* 评论与 Google/Baidu Analytics
	* [评论](#comment)
	* [网站分析](#analytics) 
* 高级部分
    * [访问统计](#访问统计)

### 开始

你可以通用修改 `_config.yml`文件来轻松的开始搭建自己的博客:

```
# Site settings
title: Yuyao's Blog                   # 你的博客网站标题
SEOTitle: Yuyao的博客 | Yuyao's Blog		# SEO 标题
description: "越努力越幸运"	   	   # 随便说点，描述一下

# SNS settings      
zhihu_username:     ma-yu-yao-31
github_username:    Ma-Yuyao    

# Build settings
# paginate: 10              # 一页你准备放几篇文章
```

Jekyll官方网站还有很多的参数可以调，比如设置文章的链接形式...网址在这里：[Jekyll - Official Site](http://jekyllrb.com/) 中文版的在这里：[Jekyll中文](http://jekyllcn.com/).

### 撰写博文

要发表的文章一般以 **Markdown** 的格式放在这里`_posts/`，你只要看看这篇模板里的文章你就立刻明白该如何设置。

yaml 头文件长这样:

```
---
layout:     post   				    # 使用的布局（不需要改）
title:      记一次全网搜索不到的Android Studio模拟器BUG解决方案 - Android 10.0+ BUG 	# 标题 
subtitle:   Android 10.0+ BUG #副标题
date:       2020-12-15				# 时间
author:     Yuyao 						# 作者
header-img: img/post-bg-desk.jpg 	#这篇文章标题背景图片
catalog: true 						# 是否归档
tags:								#标签
    - 实用Tips

---

```

### 绑定域名

关于绑定域名网上有许多教程，这里提供本人参考的一篇 [《Github个人主页绑定域名实操》](https://blog.csdn.net/qq_34487996/article/details/81604976)
### 侧边栏

侧边栏设置是在 `_config.yml`文件里面的`Sidebar settings`那块。

```
# Sidebar settings
sidebar: true                           # whether or not using Sidebar.
sidebar-about-description: "一流吃货，热爱生活"
sidebar-avatar: /img/profilepicture.jpg
```

侧边栏是响应式布局的，当屏幕尺寸小于992px的时候，侧边栏就会移动到底部。具体请见bootstrap栅格系统 <http://v3.bootcss.com/css/>

### 社交账号

在下面输入的社交账号，没有的添加的不会显示在侧边框中。新加入了[简书](https:/www.jianshu.com)链接, <http://www.jianshu.com/u/e71990ada2fd>

	# SNS settings
    RSS: false
    weibo_username:     username
    zhihu_username:     username
    github_username:    Ma-Yuyao    
    facebook_username:  username
    jianshu_username:   username
    twitter_username:   username

### Friends

好友链接部分。这会在全部页面显示。

设置是在 `_config.yml`文件里面的`Friends`那块，自己加吧。

```
# Friends
friends: [
    {
        title: "BY Blog",
        href: "https://qiubaiying.github.io/"
    },
    {
        title: "Apple",
        href: "https://apple.com/"
    }
]
```

### Comment

博客使用 [Gitalk](https://gitalk.github.io/) 评论系统，[支持 Markdwon 语法](https://guides.github.com/features/mastering-markdown/)，cool~

#### Gitalk

优点：界面干净简洁，利用 Github issue API 做的评论插件，使用 Github 帐号进行登录和评论，最喜欢的支持 Markdown 语法，对于程序员来说真是太 cool 了。

缺点：配置比较繁琐，每篇文章的评论都需要初始化。

**使用：**

参考我的这篇文章：[《为博客添加 Gitalk 评论插件》](http://qiubaiying.top/2017/12/19/%E4%B8%BA%E5%8D%9A%E5%AE%A2%E6%B7%BB%E5%8A%A0-Gitalk-%E8%AF%84%E8%AE%BA%E6%8F%92%E4%BB%B6/)


### Analytics

网站分析，现在支持百度统计和Google Analytics。需要去官方网站注册一下，然后将返回的code贴在下面：

```
# Baidu Analytics
ba_track_id: 4cc1f2d8f3067386cc5cdb626a202900

# Google Analytics
ga_track_id: 'UA-49627206-1'            # 你用Google账号去注册一个就会给你一个这样的id
ga_domain: huangxuan.me			# 默认的是 auto, 这里我是自定义了的域名，你如果没有自己的域名，需要改成auto。
```

### 访问统计

新增访问统计功能，使用 [不蒜子](http://ibruce.info/2015/04/04/busuanzi/)。

网站页脚的访问统计在 `_include\footer.html` 中，每个页面的访问统计在`_include\intro-header.html`中修改，也可以根据个人的不同需要按需修改哦。


希望大家喜欢这个主题，也感谢各位开源作者做出的贡献~ Hope you all enjoy it!

修改于 2021-2-23，作者：Yuyao-Ma