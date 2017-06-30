---
layout: post
title: 在VPS上搭建shadowsocks来科学上网
category: shadowsocks
tags: [shadowsocks]
---

之前一直在使用免费的ss，但是访问外网的速度实在是不可恭维，索性决定自己搭建VPS来翻墙。本来准备在[搬瓦工](https://bandwagonhost.com/)购买，不过最低配置也要$19.9/Y。  

后来意外发现 GitHub Education 有面向学生的福利，一旦成功申请到Github Student pack，就可以获得$50，加上充值的$5和小伙伴给的邀请链接$10,此时账户一共有$65，对于最低配置的VPS $5一个月，可以使用一年啊！！直到毕业之前都一直有Promo Code赠送，那就远远不止免费一年了。

推荐有能力，爱折腾，有科学上网需要的小伙伴食用此教程。
这是得到Student Developer Pack时Git发来的邮件的部分内容：

> Spread the word: we love giving educational discounts to students, teachers, administrators, and researchers! Please send them to:  
        https://education.github.com 

真是暖心啊~~~业界良心！！！
具体过程参考以下内容：

## 获取Student Developer Pack

如果你不是学生，请跳过第一步。如果你是学生的话，首先你要 [注册GitGub帐号](https://github.com/)，然后前往 [GitHub Education](https://education.github.com/)获取Student Developer Pack，点击 I am a student 填写学生验证信息， Verify academic status 一栏选择 I don't have a school-issued email （第一次我使用学校的 edu 邮箱提交申请当天就被拒绝了，貌似国内edu邮箱没有公信力），然后上传你的学生证照片或者能证明你是学生即可。剩下的就是漫长的等待了，不过这点等待还是很值得的（本人等了接近2天终于收到确认信件）~~~

![这里写图片描述](http://img.blog.csdn.net/20160816164348813)

![这里写图片描述](http://img.blog.csdn.net/20160816164637677)

##  DigitalOcean

### 注册DO帐号

首先注册DigitalOcean账号。可以点击我的[邀请链接](https://m.do.co/c/6d3c33c4b39e)注册，激活后就会收到$10的奖励，但是仅仅这样还是无法在DigitalOcean上创建虚拟主机。你需要绑定信用卡或者使用PayPal添加银行卡，作为国内用户建议不要使用国内信用卡，有说会不成功，导致账号直接废了。通过paypal充值的方法验证账户的好处是如果有纠纷可以通过paypal纠纷申请退款，并且paypal资金安全性要好于信用卡绑定。PayPal需要支付$5才能完成注册流程。我是在paypal账号上绑定了一张银联的卡来付款的，$5按汇率大概￥33多一点吧。

![这里写图片描述](http://img.blog.csdn.net/20160816161413413)

* 如果你已经获得了了第一步的Student Developer Pack，那么可以在注册成功后在Settings->Billing下找到Promo Code，输入你在Student Developer Pack获得的学生优惠码，价值50刀，这对于屌丝学生来说可是笔不小的数目。

### 创建VPS

注册成功之后就可以登录DigitalOcean并创建你的VPS了。操作系统的话，我选择的是ubuntu的，看个人喜好选择吧。服务器选择 $5/mon 的最低端的配置就够了，如有你有建站或者其他需求的话另行选择。经过测试在国内使用Singapore的机房是最优的选择，而其他的的机房延迟都很高。最后点击Create创建。

Tips:贴一个测速地址，请根据测速结果选择最合适的机房。 [Digitalocean服务器测速-新加坡节点](http://speedtest-sgp1.digitalocean.com/)

## ShadowSocks

### SS介绍

[ShadowSocks](https://github.com/shadowsocks)是科学上网的利器，在 Github 上接近1.4W的 Star，使用的人极多、影响极深。而且它对各个平台的支持也非常好，目前我在Windows/Android平台上都完成了科学上网环境的搭建。

### 配置shadowsocks服务端

创建成功后，在你的 droplets 控制面板上的服务器名后点击下拉 more ，再点击 accessv console 进入远程终端的连接。
![这里写图片描述](http://img.blog.csdn.net/20160816163553145)

*  Tips:记下你的服务器IP地址，配置SS客户端会用到。

![这里写图片描述](http://img.blog.csdn.net/20160816163154280)

初次进入需要输入原始的账号密码，账号是root，密码会在注册邮箱中找到（创建完 droplet 后发送至邮箱，注意有可能在邮件垃圾箱里），然后输入Username 和 Password回车确认( Tips:输入密码时不会有暗文 "********" 显示，尽管输入然后回车确定就好。而且初始密码有点长，需要有点耐心。^-^)，系统会让你再次输入原始的密码（current）UNIX password, 然后Enter new UNIX password 输入新密码，然后 Retype 确认密码。至此，VPS远程登陆成功。

### 在VPS上安装shadowsocks

输入以下命令安装shadowsocks：

```shell
apt-get update
apt-get install python-pip
# 询问是否Continue，输入y确认
pip install shadowsocks
```

### 创建配置文件

```shell
sudo vim /etc/shadowsocks.json
```

按a键进入编辑模式，输入以下配置项

```json
{
    "port_password":{
        "443":"yourpassword"
    },
    "method":"aes-256-cfb",
    "timeout":600
}
```

然后按esc键退出编辑模式，输入  **:wq**  保存配置文件

### 启动SS服务

后台启动ss服务

```shell
sudo ssserver -c /etc/shadowsocks.json -d start 
```

关闭ss服务

```shell
sudo ssserver -d stop
```

或者直接在启动时加入相关配置参数，无需配置启动文件

```shell
sudo ssserver -p 443 -k yourpassword -m aes-256-cfb --user nobody -d start
```

###  SS客户端下载

前往GitHub托管的[ShadowSocks](https://github.com/shadowsocks)项目下载相应客户端。  

这里仅贴出windows版本：[下载地址](https://github.com/shadowsocks/shadowsocks-windows/releases)

###  客户端配置

客户端栏目填入以下项:

```shell
服务器地址：你的服务器IP
服务器端口：443    # 或者自定义端口，注意与开放的端口要一致
密码： "yourpassword"
加密： "aes-256-cfb"
```

配置完成后在记得托盘图标里勾选启动系统代理，就可以访问外网，获取你所需要的资源了。

贴张图表示下 ---> YouTube 1080P 毫无压力

![youtube](http://img.blog.csdn.net/20160819235904373)


> 如有疑问请留言或者给我来信。 E-mail:  yuhuixu@yuhuixu.cn

