---
layout:     post   				    # 使用的布局（不需要改）
title:      github网页无法访问问题的解决（github服务器响应时间过长 ，错误提示 ERR_CONNECTION_TIMED_OUT） 	# 标题 
subtitle:   网络问题解决 #副标题
date:       2020-12-13				# 时间
author:     Yuyao 						# 作者
header-img: img/post-bg-desk.jpg 	#这篇文章标题背景图片
catalog: true 						# 是否归档
tags:								#标签
    - 实用Tips
---

# 1. 问题描述

这几天在折腾这个github page 的 Blog，由于修改了 hellocode.ink 这个网址的 DNS解析，导致访问该网站极其缓慢，经过查阅资料得到以下解决访问，感谢 [https://blog.csdn.net/amnesiagreen/article/details/108493456](https://blog.csdn.net/amnesiagreen/article/details/108493456) 提供的解决方案！

## 2. 问题分析

我们访问网站一般是通过域名来访问的（如 [https://github.com/](https://github.com/)），但是在后台是需要经过域名服务器（ DNS 服务器）查询域名所对应的 IP 地址再访问的。浏览器在查询过一次之后会将域名对应的 IP 地址储存在本地，如果再次访问就不同通过域名服务器查询 IP 地址了。
但是这样会有一个问题，如果域名对应的 IP 地址发生了变化，根据本地储存的 IP 地址就找不到我们想要访问的网页了，这时可以通过删除浏览器浏览记录来清除本地缓存。

对应于Chorme 的操作为：在输入网址的地方输入 [chrome://net-internals/#dns](chrome://net-internals/#dns) ,点击Clear cache 
注意，点击后没有任何提示，但是一般都会清理成功。
  
然后再次访问该站，速度恢复正常！
