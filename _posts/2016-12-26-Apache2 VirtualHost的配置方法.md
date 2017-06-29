---
layout: post
title: Apache2 VirtualHost的配置方法
category: Apache
tags: [Apache]
---

## apache2.conf的配置

开发时经常需要配置多个站点，并经常进行切换。
以前的做法是在httpd.conf里include所有的配置文件，不需要的时候进行注释，例如：

```shell
include conf/site.conf
#include conf/default.conf
include conf/spider.conf
```

这样需要先定位到`httpd.conf`的目录，然后使用编辑器打开、修改、然后保存，比较麻烦。
现在可以在`apache2.conf`里include所有的配置文件。  
![apache2.conf](http://pro.topblog.top/pic/20161226_apache2_1.png)

##  a2ensite和a2dissite的使用

另外Apache还提供了方便的工具来管理配置文件，就是`a2ensite`和`a2dissite`，它们都在`apache2-common`包里。
`/etc/apache2/sites-available` 目录下存放可用的VirtualHost配置文件  
 ![sites-available目录](http://pro.topblog.top/pic/20161226_apache2_2.png)  

`/etc/apache2/sites-enable`  目录下存放已经生效的VirtualHost配置文件的符号链接(Symbolic Link)，也就是常说的快捷方式啦，该链接指向sites-available下的同名文件。

![sites-enable目录](http://pro.topblog.top/pic/20161226_apache2_3.png)  

使用命令`a2ensite`可以将`sites-available`目录下的配置文件生效，并且生效后会自动在`sites-enable`目录下创建同名链接。
使用命令`a2dissite`可以将`sites-enable`目录下的配置文件链接失效并自动删除该链接。
通过`a2dissite`和`a2ensite`，我们可以快速激活/屏蔽站点，加快开发和部署效率。

##  实例：配置基于域名的虚拟主机方法

1. `sites-available`目录下新建VirtualHost配置文件  
![新建VirtualHost配置文件](http://pro.topblog.top/pic/20161226_apache2_4.png)
2. 使用`a2dissite`命令来使原有的VirtualHost配置失效  
![使用a2dissite命令](http://pro.topblog.top/pic/20161226_apache2_5.png)
3. 使用`a2ensite`命令来使新的VirtualHost配置生效  
![使用a2ensite命令](http://pro.topblog.top/pic/20161226_apache2_6.png)
4. 重启apache2服务  
![重启apache2服务](http://pro.topblog.top/pic/20161226_apache2_7.png)
