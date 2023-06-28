---
title: hexo博客搭建踩坑记录
tags:
---
* valine评论api报错：net::ERR_NAME_NOT_RESOLVED（域名解析错误）
过程：  
在选择评论系统时，先是尝试了disqus，后来看资料国内用户可能无法进行评论，于是转而使用Valine.
根据[Valine官方文档](https://valine.js.org/quickstart.html)注册了LeanCloud并在hexo配置好之后，发现还是无法提交评论。打开控制台，报错如下：
![](企业微信20230612-200316@2x.png)
由于LeanCloud国内版进行域名备案，所以使用的是国际版。需要根据[Valine官方文档配置项](https://valine.js.org/configuration.html#serverURLs)，国际版不需要配置serverURLs，会自动检测。
解决：  

解决方案参考：
https://cloud.tencent.com/developer/article/2205930