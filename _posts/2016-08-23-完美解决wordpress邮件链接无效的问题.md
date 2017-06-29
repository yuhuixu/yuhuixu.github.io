---
layout: post
title: 完美解决wordpress邮件链接无效的问题
category: Wordpress
tags: [Wordpress]
---

**教程介绍**:解决wordpress新用户注册邮件链接无效以及重新设置密码链接无效的问题

## 解决流程

### 案例一、用户注册

当用户注册站点时，用户会收到如下注册信：

![这里写图片描述](http://img.blog.csdn.net/20160823174621928)

当用户点击链接时，却发现链接无效:

![这里写图片描述](http://img.blog.csdn.net/20160823175007883)

仔细观察设置密码的链接，会发现邮箱发送的链接地址后面多了个”>”号，本来是WordPress为了美观，前后加上了尖括号，结果适得其反，被邮箱解析到地址里面去了，点击后自然会是无效的了。

### 解决办法

#### 方法一

解决的方法很简单，把下面的代码加入当前主题的functions.php里面就可以了。

```java
function reset_password_message( $message, $key ) { if ( strpos($_POST['user_login'], '@') ) { $user_data = get_user_by('email', trim($_POST['user_login'])); } else { $login = trim($_POST['user_login']); $user_data = get_user_by('login', $login); } $user_login = $user_data->user_login; $msg = __('有人要求重设如下帐号的密码：'). "\r\n\r\n"; $msg .= network_site_url() . "\r\n\r\n"; $msg .= sprintf(__('用户名：%s'), $user_login) . "\r\n\r\n"; $msg .= __('若这不是您本人要求的，请忽略本邮件，一切如常。') . "\r\n\r\n"; $msg .= __('要重置您的密码，请打开下面的链接：'). "\r\n\r\n"; $msg .= network_site_url("wp-login.php?action=rp&key=$key&login=" . rawurlencode($user_login), 'login') ; return $msg; } add_filter('retrieve_password_message', reset_password_message, null, 2);
```

#### 方法二

通过修改WordPress根目录下wp-login.php文件可以解决这个问题。

找到如下代码（大约在第330行）：

```java
$message .= '<' . network_site_url("wp-login.php?action=rp&key=$key&login=" . rawurlencode($user_login), 'login') . ">\r\n";
```

修改为：

```java
$message .= network_site_url("wp-login.php?action=rp&key=$key&login=" . rawurlencode($user_login), 'login') ;
```

其实也就是把'<‘ .和. “>\r\n”去掉，但是这种方法在升级Wordpress后会失效，因为升级后wp-login.php会被替换，需要重新修改wp-login.php，所以推荐使用第一种方法。

修改后即用户可正常设置密码：

![这里写图片描述](http://img.blog.csdn.net/20160823181051845)  

### 案例二、用户修改、重置密码

当用户点击忘记密码选择重新修改密码时，用户会收到如下信件：

![这里写图片描述](http://img.blog.csdn.net/20160823180601795)

发现还是上面的情况类似，修改密码链接地址后面多了个”>”号。

### 解决办法

下载站点中wp-includes文件夹中的pluggable.php文件并打开
找到如下语句：

```java
$message .= '<'network_site_url("wp-login.php?action=rp&key=$key&login=" . rawurlencode($user_login), 'login')">\r\n\" ;
```

修改为：

```java
$message .= network_site_url("wp-login.php?action=rp&key=$key&login=" . rawurlencode($user->user_login), 'login') . "\r\n\r\n";
```

用户即可收到正常链接重置密码的邮件：

![这里写图片描述](http://img.blog.csdn.net/20160823181831565)
