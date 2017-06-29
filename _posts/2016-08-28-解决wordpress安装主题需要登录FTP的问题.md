---
layout: post
title: 解决wordpress安装主题需要登录FTP的问题
category: Wordpress
tags: [Wordpress]
---

## 问题描述

wordpress安装主题时提示如下：   

**要执行请求的操作，WordPress需要访问您网页服务器的权限。 请输入您的FTP登录凭据以继续。 如果您忘记了您的登录凭据（如用户名、密码），请联系您的网站托管商。**


## 解决方案

设置wordpress文件夹的所有者及权限

```
sudo chown -R www-data /var/www/wordpress
sudo chmod -R 775 /var/www/wordpress
```
Tips:在debian/ubuntu上，www-data是默认运行web服务的用户/组，一般在通过apt安装web服务程序时生成。搭建web服务的文件夹/文件一般要设置成www-data的。  

不过，你也可以不用www-data，自己建一个新的用户和组，然后对apache/ngnix/lighttpd等web服务程序进行配置。不过这样比较麻烦。  

如果你是编译的，不会生成www-data用户/组，需要自己弄。

