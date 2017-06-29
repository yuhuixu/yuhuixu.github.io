---
layout: post
title: 使用JuiceSSH玩转Linux与Windows
category: JuiceSSH
tags: [JuiceSSH]
---

## JuiceSSH

### Linux主机的管理

windows平台上我们可以使用XShell，Putty，SecureCRT等SSH终端软件。但是讲到移动端的终端软件， 那就不得不提到 JuiceSSH 了，它是我所使用的ssh安卓手机客户端上最满意的一款，无论从操作上都比 ConnectBot 及 VX ConnectBot 都方便许多。有了它，用手机管理 linux 服务器相当方便，可以作为系统管理员手机必备软件之一。  还能够满足Linux系统学习的需要，因为你可以在任何时间地点使用，只要你有一部能够上网的安卓手机即可。

![这里写图片描述](http://img.blog.csdn.net/20160926142344794)

特点：

 - 全彩色终端/SSH客户端
 - 弹出式键盘包含常用的字符
 - 可使用音量键快速调节字体大小
 - 支持外接键盘
 - 支持官方Mosh(一种在手机上的shell，适合网络不稳定的情况下使用，官网地址：http://mosh.mit.edu/)
 - Telnet支持
 - 支持安卓本地终端
 - 点击网址链接可直接调用浏览器打开
 - 会话中可复制、粘贴
 - 可保存人机命令交互信息到文件，并可分享到Dropbox或者Evernote、邮件及SD卡上(这功能方便，我很喜欢，貌似别的没有)
 - 支持UTF-8编码
 - 可以通过组分类管理你的SSh连接
 - 后端可以同时开启多个会话
 - 通过一键点击实现无缝连接其他SSH会话
 - 在打开App时能够快速与常用的SSH链接建立会话
 - 支持密码和OpenSSH私钥认证
 - 支持SSH 秘钥代理转发
 - 支持谷歌之类的双认证
 - 更新密码或秘钥等后，会话开启就直接使用新的密码秘钥连接
 - zlib要锁改善SSH会话在高延迟下的情况(这应该是Mosh更好)

具体Linux的操作我在这里就不详细说明了。

## Windows主机的管理

Windows提供了一些远程管理功能，比如强大的 [PowerShell](http://www.powershellserver.com/)，虽然只能允许同时连接一个人，毕竟windows只支持单用户登录。具体的功能配置以及使用请参考官方文档：[http://www.powershellserver.com/support/articles/getting-started/](http://www.powershellserver.com/support/articles/getting-started/)

Tips：由于天朝防火墙的原因，国外一些网站无法访问。如果你没有翻墙技能，你可以到本站资源分享专区获取对应的下载资源。或者加入我们内部群获取最新的SS翻墙帐号，免费提供~仅供学习使用！

### windows PowerShell服务的配置
好了，我们来下载一个： 

![这里写图片描述](http://img.blog.csdn.net/20160926151934540)

配置如下图，最后那个File Based Public Key就是你的客户端生成的那个公钥（我这里使用的是Xshell生成的一对密钥,你可以从不同渠道获得一对密钥。） 

![这里写图片描述](http://img.blog.csdn.net/20160926152838802)

我们改一下编码方式，改成简体中文就好，这样当我们使用JuiceSSH终端连接windows时就显示中文了 

![这里写图片描述](http://img.blog.csdn.net/20160926153142515)

### 移动端JuiceSSH的配置

接下配置JuiceSSH，填写Windows 外网IP地址、端口（默认22）以及认证（这里认证用户名可随意填写，私钥一定要选择与刚才公钥配对的密钥，否则无法认证！） 

<img class="aligncenter" title="" src="http://img.blog.csdn.net/20160926154643364" alt="这里写图片描述" width="380" height="633" />

注意：如果你使用的是内网ip （即使用了路由器），如果仅仅设置内网IP地址，比如：192.168.1.100。
那么只有当你的移动端也在该路由器管理下才能和Windows连接。
但是可能很多小伙伴可能并不满足只在局域网环境下管理你的windows主机，而是即使在不同的网络环境（比如移动端使用3G/4G网络）就能远程操作你的windows主机，那么你就需要在路由器中配置相应的转发规则了。
具体配置如下：
进入路由器管理界面，找到转发规则中的虚拟服务器选项。填写虚拟服务器配置： 

![这里写图片描述](http://img.blog.csdn.net/20161003220516486)

配置完毕后你就可以在JuiceSSH的主机地址一栏中填写你的外网IP地址了，如果你不知道你的外网IP，可以在路由器的WAN口状态中查看。或者直接百度搜索‘ip’，即可得到你的外网IP。

恭喜，到这一步你就可以移动端远程登录上你的windows主机了： 

<img class="aligncenter" title="" src="http://img.blog.csdn.net/20160926154810608" alt="这里写图片描述" width="380" height="633" />

你可以使用命令行远程操作你的windows主机：
比如关机、注销、重启，查看文件目录，查看、终止系统进程，打开QQ，打开音乐播放器等等常见操作都可以使用命令行的形式进行远程操作。

这里演示如何远程操作登录QQ以及打开音乐播放器：
首先配置系统环境变量：在path中添加你的QQ执行文件`QQ.exe` 的目录位置，比如我的在： `D:\QQ\Bin`。然后是网易云音乐的执行文件`cloudmusic.exe` 在目录`D:\CloudMusic` 下。Path中只要添加这样两条记录即可：`D:\QQ\Bin` 和`D:\CloudMusic`

然后你只要在命令行中输入`qq`，你就会惊奇的发现windows就会打开QQ登录程序，如果你设置了自动登录，那么你就实现了移动端远程操作登陆QQ。 

<img class="aligncenter" title="" src="http://img.blog.csdn.net/20160926160758419" alt="这里写图片描述" width="380" height="380" />  

![这里写图片描述](http://img.blog.csdn.net/20160926161123749)

同样如果输入`cloudmusic`，那么电脑就会打开网易云音乐，如果你设置了打开就自动播放，那么那么你就实现了移动端远程操作播放音乐。

最后，你躺在床上在手机上输入`shutdown /p`,你的电脑就自动关机了，是不是很方便呢。
更多功能自己脑洞吧~~ 比如别人在用我的电脑打游戏，我可以躲在角落在手机上输入`ps` 查看游戏进程ID，一个`kill` 命令结束掉游戏进程。然后`./tupian.jpg` 打开一张图片告诉他，这个游戏只能玩10分钟！！！相信你的小伙伴绝对是一脸懵逼，Ahhhhhh。

文章来自:  [拓扑部落（topblog.top）>>](http://www.topblog.top) [使用JuiceSSH玩转Linux与Windows](http://www.topblog.top/?p=507)
