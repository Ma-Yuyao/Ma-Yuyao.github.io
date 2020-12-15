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

# BUG描述
在Android Studio中配置模拟器时SDK选择了Android 10.0+ ,然后在运行模拟器时，提示一下Error:

```java
Emulator: emulator: ERROR: Can't find 'Linux version ' string in kernel image file: 
C:\Users\******\AppData\Local\Android\Sdk\system-images\android-30\google_apis_playstore\x86\\kernel-ranchu-64
```
可以看到BUG在于路径中竟然是 `x86\\`，双`\`，当然无法找到文件了...

遇到该问题后尝试了百度/Google，未能发现对于该问题的描述和解决方案，所以决定在CSDN中贴出该问题及解决方案，希望能帮助到大家。

# 解决方案
1. 在`SDK Manager`中卸载 Android 10.0+
2. 卸载成功后安装低版本的SDK，实测Android 9.0 可以正常运行。

吐槽一下，这么基本的BUG能出在Android Studio上...Google的测试人员一言难尽啊...而且我朋友的机子上也出现了这个BUG，竟然还没有修复甚至在网上找不到相关的BUG汇报与解决方案...

发现这个BUG后报告给了Google，然而到今天了还是没有回复...
