<div class="J_adv" data-view="true" data-mod="ad_popu_72" data-mtp="62" data-order="40" data-con="ad_content_2072">

<div id="layerd" style="position: fixed;bottom:0px;right:0px;line-height:0px;z-index:1000">

<div class="J_close layer_close" style="display:;background-color:#efefef;padding:0px;color:#333;font:12px/24px Helvetica,Tahoma,Arial,sans-serif;text-align:right;">关闭</div>

</div>

<script>document.getElementById("popuLayer_js_q").onload=function(){ var styObjd=styObj={width:"300px","height":parseInt(250)+28};window.CSDN.Layer.PopuLayer("#layerd",{storageName:"layerd",styleObj:styObjd,total:50,expoire:1000*60}); }</script> <script type="text/javascript">/*服务器频道首页置顶Banner960*90，创建于2014-7-3*/ (window.cproArray = window.cproArray || []).push({ id: "u2895327" });</script></div>

<div class="blog_left">

<div class="blog_l_c">

## xyh421的专栏

<div class="item_wrap">

<dl class="item_l">

<dt class="item">22</dt>

<dd class="item_name">原创</dd>

</dl>

<dl class="item_l">

<dt class="item">6</dt>

<dd class="item_name">转载</dd>

</dl>

<dl class="item_l">

<dt class="item">0</dt>

<dd class="item_name">译文</dd>

</dl>

<dl class="item_l">

<dt class="item">6</dt>

<dd class="item_name">评论</dd>

</dl>

<dl class="item_l">

<dt class="item">9783</dt>

<dd class="item_name">访问</dd>

</dl>

</div>

</div>

<div class="blog_copyright">

<span>京 ICP 证 070598 号</span>![img](http://static.blog.csdn.net/skin/skin2-template/images/copyright.png)

Copyright © 1999-2016,
CSDN.NET, All Rights Reserved

</div>

</div>

<div id="skin_m" class="skin_m">

<div id="skin_center" class="skin_center">

<div class="skin_center_t">

<div class="skin_list">

<dl class="list_c clearfix detail_list">

<dt>

<div class="date">

<div class="date_t"><span>2016</span>_八月_</div>

<div class="date_b">04</div>

</div>

</dt>

<dd>

<div class="skin_icon">[置](javascript:;)[原](javascript:;)</div>

### [Robot Framework +Appium的简单教程及实例](/xyh421/article/details/52119872)

<div class="list_c_Title">

<label><span>分类：</span>_automator test__appiumlibrary__robotframework_</label>

<label><span style="cursor:default">（4213）</span></label> <label><span style="cursor:default">（0）</span></label> <label><span>[编辑](http://write.blog.csdn.net/postedit/52119872)</span> </label><label class="delete_btn"><span onclick="javascript:deleteArticle(52119872);return false;">删除</span></label>

</div>

<div class="skin_detail" id="article_content">

# Robot Framework +Appium的简单教程

* * *

## <a target="_blank" name="t1" style="color:rgb(51,102,153)"></a>RF+Appium介绍

网上文章较多，不做赘述 
Robot Framework 
Appium

## <a target="_blank" name="t2" style="color:rgb(51,102,153)"></a>RF 的安装和配置

在使用 RF（Rebot framework）的时候需要 [Python](http://lib.csdn.net/base/python "Python知识库") 或 Jython 环境，具体可根据自己的需求来确定。本文以在有 Python 的环境的机器上安装和使用 RF 为例。 
在配置过程中需要安装如下包：python 2.7、wxPython、robot framework、robot framework ride、robot framework selenium library。

## <a target="_blank" name="t3" style="color:rgb(51,102,153)"></a>安装 Python 2.7

RF 框架是基于 Python 语言的，所以一定要有 Python 环境。可以通过下面的下载页面下载对应的 Python 版本。 
下载页面：[https://www.python.org/downloads/](https://www.python.org/downloads/)。 
下载完成后，选择默认项进行安装 
安装完后，需要设置环境变量：计算机—属性—高级系统设置—环境变量—系统变量—Path，写入 C:\Python27 和 C:\Python27\Scripts（更改为您指定路径即可）。 
同时我们也可以通过 DOS 环境来验证安装的 Python 信息。

## <a target="_blank" name="t4" style="color:rgb(51,102,153)"></a>安装 WxPython

下载页面： [http://wxpython.org/download.php#stable](http://wxpython.org/download.php#stable)。 
在选择版本下载的时候要注意选择与 Python 版本对应的版本，并且选择 unicode 版本，比如版本：wxPython2.8-win32-unicode-py26.exe，否则安装完成后不能支持中文。 
下载完成后，选择默认项进行安装即可。 
[https://sourceforge.net/projects/wxpython/files/wxPython/2.8.12.1/](https://sourceforge.net/projects/wxpython/files/wxPython/2.8.12.1/)

## <a target="_blank" name="t5" style="color:rgb(51,102,153)"></a>安装 PyCrypto

下载页面：[http://www.voidspace.org.uk/python/modules.shtml#pycrypto](http://www.voidspace.org.uk/python/modules.shtml#pycrypto)。 
选择对应的 pycrypto installer 版本，进行默认安装。需要在安装库（如 SHHLibrary）之前进行安装，否则会出现 错误“Can’t find vcvarsal.bat”。

## <a target="_blank" name="t6" style="color:rgb(51,102,153)"></a>安装 Robot Framwork

进入 Python 的安装路径，执行命令“pip install robotframework”或者通过下载页面[https://pypi.python.org/pypi/robotframework](https://pypi.python.org/pypi/robotframework)下载源码。 
解压后，执行命令“python setup.py install”进行安装。进入 Python 的安装路径，执行命令“pip install robotframework”。 
pip install robotframework 
easy_install robotframework （3.0）

## <a target="_blank" name="t7" style="color:rgb(51,102,153)"></a>安装 robotframework-ride

进入 Python 的安装路径，执行命令“pip install robotframework-ride”。

## <a target="_blank" name="t8" style="color:rgb(51,102,153)"></a>安装需要的 Library

如selenium2library ,appiumlibrary,archivelibrary,SSHLibrary ,ftplibrary 等。

### <a target="_blank" name="t9" style="color:rgb(51,102,153)"></a>进入 Python 的安装路径，分别执行以下命令：

<div>pip install robotframework-appiumlibrary
</div>

pip install robotframework-selenium2library 
pip install robotframework-archivelibrary 
pip install robotframework-SSHLibrary 
ip install robotframework-ftplibrary

<span style="">ps:</span>如果pip install不行就用easy_install

## <a target="_blank" name="t10" style="color:rgb(51,102,153)"></a>安装和配置appium

官网下载appium的windows安装包

官网：[https://bitbucket.org/appium/appium.app/downloads/](https://bitbucket.org/appium/appium.app/downloads/)

打开appium，如图所示配置，最后一步点击Launch打开Appium Socket Server 
图 0.Appium配置图 
![image](http://imglf1.nosdn.127.net/img/bS9RU1VmT1M3bWtscUNRaHQrY1FHTkREM1hhazRSaFRrdWZxSzhpc0RRT0p1d3N3SlhFUVR3PT0.png?imageView&thumbnail=500x0&quality=96&stripmeta=0&type=jpg) 
完成以上步骤后，RobotFramework+Appium 的安装和配置工作已经完成，可以通过执行命令“pip list”查看已经安装的产品，如图 1 所示： 
图 1.RobotFramework 安装产品列表 
![image](http://imglf.nosdn.127.net/img/bS9RU1VmT1M3bWtscUNRaHQrY1FHRUpTUklwNDg5aHNOR016dGJVdFVkd1NCL09tR3FuMSt3PT0.png?imageView&thumbnail=500x0&quality=96&stripmeta=0&type=jpg)

## <a target="_blank" name="t11" style="color:rgb(51,102,153)"></a>RIDE 编辑器介绍

### <a target="_blank" name="t12" style="color:rgb(51,102,153)"></a>官方文档

[http://robotframework.org/robotframework/#user-guide](http://robotframework.org/robotframework/#user-guide)

### <a target="_blank" name="t13" style="color:rgb(51,102,153)"></a>打开RIDE

RF 是通过 RIDE 编辑器进行工作的，安装成功后，执行命令“[PythonDir]\Scripts\ride.py”，就可以打开 RIDE 编辑器，如图 2 所示。打开之后就可以进行创建测试项目，创建测试用例等操作，在后面的实例讲解中有具体步骤。 
图 2.RIDE 编辑器启动界面

### <a target="_blank" name="t14" style="color:rgb(51,102,153)"></a>创建测试项目

选择菜单栏 File —>New Project，输入项目名称，选择 Directory type，选择目录。 
图 3\. 创建测试项目 
![image](http://imglf2.nosdn.127.net/img/bS9RU1VmT1M3bWtscUNRaHQrY1FHQ0lNYSt2ME42WGpkNDJlOFdQZHFlWHNQSHN6VWdHY1JnPT0.png?imageView&thumbnail=500x0&quality=96&stripmeta=0&type=jpg)

### <a target="_blank" name="t15" style="color:rgb(51,102,153)"></a>创建测试套件

右键点击刚创建的测试项目，选择 New Suit，输入 name , 选择 File type。 
图 4\. 创建测试套件 
![image](http://imglf.nosdn.127.net/img/bS9RU1VmT1M3bWtscUNRaHQrY1FHTm5Vb2NXWnM5cVlVbEFpSURna1FWeFk5cWV5RzdPZzZRPT0.png?imageView&thumbnail=500x0&quality=96&stripmeta=0&type=jpg)

### <a target="_blank" name="t16" style="color:rgb(51,102,153)"></a>创建测试用例

右键点击刚创建的测试套件，选择 New TestCase，输入名称。 
图 5\. 创建测试用例 
![image](http://imglf.nosdn.127.net/img/bS9RU1VmT1M3bWtscUNRaHQrY1FHQnZ5QzJtSHNoL090a21PZkt5cmJhZUVibytwOXhCR3F3PT0.png?imageView&thumbnail=500x0&quality=96&stripmeta=0&type=jpg)

### <a target="_blank" name="t17" style="color:rgb(51,102,153)"></a>导入库

在实际项目中，我们需要运用 RF 框架编写基于 web 的测试用例，我们需要 Selenium 的库支持。所以，我们在使用的过程中需要加载 selenium2library 库。 
图 6\. 导入测试库 
![image](http://imglf2.nosdn.127.net/img/bS9RU1VmT1M3bWtscUNRaHQrY1FHTU1RSGZhZGtmcDY0T3ljdlZickhFM0RhZEc4ckNqVlRnPT0.png?imageView&thumbnail=500x0&quality=96&stripmeta=0&type=jpg) 
在“测试套件”的 Edit 标签页，点击“Library”按钮，弹出输入框，Name 输入：AppiumLibrary，点击 OK 完成。 
如果导入的库显示为红色，表示导入的库不存在。如果是黑色则表示导入成功。

### <a target="_blank" name="t18" style="color:rgb(51,102,153)"></a>编写测试用例

可以通过快捷键 F5 来查询脚本的关键字。以打开浏览器为例，输入关键字“open”进行搜索，查询到一个“Open Browser”的关键字，点击这个关键字，就出现了它的用法和说明，如图 7。 
图 7.Search Keywords 
![image](http://imglf1.nosdn.127.net/img/bS9RU1VmT1M3bWtscUNRaHQrY1FHRDdYRktBQ0JtT0NoMVBzcURleVh4VERHTXRxL3NxdnVnPT0.png?imageView&thumbnail=500x0&quality=96&stripmeta=0&type=jpg) 
熟悉这个关键字用法之后，可以在 test case 里面进行尝试。“Open Application”显示蓝色，说明它是一个合法的关键字，后面为红色说明需要输入一个参数，从其用法可知，需要输入 URL。更多关键字的用法可以熟悉 API 文件。 
图 8.keywords 实例 
![image](http://imglf1.nosdn.127.net/img/bS9RU1VmT1M3bWtscUNRaHQrY1FHRm04d0RQcUFGa1kxQURqQnI3R2JXYkdVN0RXclFvMERBPT0.png?imageView&thumbnail=500x0&quality=96&stripmeta=0&type=jpg) 
编写测试用例的时候还可以选择添加变量。变量是 RF 的常用的功能，它能在测试数据的大多数地方使用。主要有以下几种： 
标量变量：语法 <span class="MathJax_Preview" style="color:rgb(136,136,136)"></span><span class="MathJax" id="MathJax-Element-1-Frame" style="display:inline; line-height:normal; font-size:14px; word-spacing:normal; word-wrap:normal; white-space:nowrap; float:none; direction:ltr; max-width:none; max-height:none; min-width:0px; min-height:0px; border:0px; padding:0px; margin:0px"><nobr style="border:0px; padding:0px; margin:0px; max-width:none; max-height:none; min-width:0px; min-height:0px; vertical-align:0px"><span class="math" id="MathJax-Span-1" style="display:inline-block; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; width:91.908em"><span style="display:inline-block; position:relative; border:0px; padding:0px; margin:0px; vertical-align:0px; width:76.551em; height:0px; font-size:16.8px"><span style="position:absolute; border:0px; padding:0px; margin:0px; vertical-align:0px; top:-2.14em; left:0.003em"><span class="mrow" id="MathJax-Span-2" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="texatom" id="MathJax-Span-3" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-4" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mi" id="MathJax-Span-5" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">s</span><span class="mi" id="MathJax-Span-6" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">c</span><span class="mi" id="MathJax-Span-7" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">a</span><span class="mi" id="MathJax-Span-8" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">l</span><span class="mi" id="MathJax-Span-9" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">a</span><span class="mi" id="MathJax-Span-10" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">r</span></span></span><span class="texatom" id="MathJax-Span-11" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-12" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-13" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">。</span></span></span></span><span class="texatom" id="MathJax-Span-14" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-15" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-16" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">当</span></span></span></span><span class="texatom" id="MathJax-Span-17" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-18" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-19" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">在</span></span></span></span><span class="texatom" id="MathJax-Span-20" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-21" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-22" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">测</span></span></span></span><span class="texatom" id="MathJax-Span-23" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-24" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-25" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">试</span></span></span></span><span class="texatom" id="MathJax-Span-26" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-27" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-28" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">数</span></span></span></span><span class="texatom" id="MathJax-Span-29" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-30" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-31" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">据</span></span></span></span><span class="texatom" id="MathJax-Span-32" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-33" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-34" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">中</span></span></span></span><span class="texatom" id="MathJax-Span-35" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-36" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-37" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">使</span></span></span></span><span class="texatom" id="MathJax-Span-38" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-39" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-40" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">用</span></span></span></span><span class="texatom" id="MathJax-Span-41" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-42" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-43" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">标</span></span></span></span><span class="texatom" id="MathJax-Span-44" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-45" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-46" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">量</span></span></span></span><span class="texatom" id="MathJax-Span-47" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-48" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-49" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">变</span></span></span></span><span class="texatom" id="MathJax-Span-50" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-51" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-52" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">量</span></span></span></span><span class="texatom" id="MathJax-Span-53" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-54" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-55" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">时</span></span></span></span><span class="texatom" id="MathJax-Span-56" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-57" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-58" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">，</span></span></span></span><span class="texatom" id="MathJax-Span-59" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-60" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-61" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">它</span></span></span></span><span class="texatom" id="MathJax-Span-62" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-63" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-64" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">们</span></span></span></span><span class="texatom" id="MathJax-Span-65" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-66" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-67" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">将</span></span></span></span><span class="texatom" id="MathJax-Span-68" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-69" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-70" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">被</span></span></span></span><span class="texatom" id="MathJax-Span-71" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-72" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-73" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">分</span></span></span></span><span class="texatom" id="MathJax-Span-74" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-75" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-76" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">配</span></span></span></span><span class="texatom" id="MathJax-Span-77" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-78" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-79" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">的</span></span></span></span><span class="texatom" id="MathJax-Span-80" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-81" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-82" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">值</span></span></span></span><span class="texatom" id="MathJax-Span-83" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-84" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-85" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">所</span></span></span></span><span class="texatom" id="MathJax-Span-86" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-87" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-88" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">代</span></span></span></span><span class="texatom" id="MathJax-Span-89" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-90" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-91" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">替</span></span></span></span><span class="texatom" id="MathJax-Span-92" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-93" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-94" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">。</span></span></span></span><span class="texatom" id="MathJax-Span-95" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-96" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-97" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">列</span></span></span></span><span class="texatom" id="MathJax-Span-98" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-99" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-100" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">表</span></span></span></span><span class="texatom" id="MathJax-Span-101" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-102" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-103" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">变</span></span></span></span><span class="texatom" id="MathJax-Span-104" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-105" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-106" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">量</span></span></span></span><span class="texatom" id="MathJax-Span-107" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-108" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-109" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">：</span></span></span></span><span class="texatom" id="MathJax-Span-110" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-111" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-112" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">语</span></span></span></span><span class="texatom" id="MathJax-Span-113" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-114" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-115" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">法</span></span></span></span><span class="texatom" id="MathJax-Span-116" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-117" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-118" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Main">@</span></span></span><span class="texatom" id="MathJax-Span-119" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-120" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mi" id="MathJax-Span-121" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">L</span><span class="mi" id="MathJax-Span-122" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">I<span style="display:inline-block; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; overflow:hidden; height:1px; width:0.063em"></span></span><span class="mi" id="MathJax-Span-123" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">S<span style="display:inline-block; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; overflow:hidden; height:1px; width:0.063em"></span></span><span class="mi" id="MathJax-Span-124" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">T<span style="display:inline-block; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; overflow:hidden; height:1px; width:0.122em"></span></span></span></span><span class="texatom" id="MathJax-Span-125" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-126" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-127" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">。</span></span></span></span><span class="texatom" id="MathJax-Span-128" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-129" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-130" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">列</span></span></span></span><span class="texatom" id="MathJax-Span-131" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-132" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-133" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">表</span></span></span></span><span class="texatom" id="MathJax-Span-134" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-135" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-136" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">变</span></span></span></span><span class="texatom" id="MathJax-Span-137" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-138" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-139" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">量</span></span></span></span><span class="texatom" id="MathJax-Span-140" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-141" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-142" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">是</span></span></span></span><span class="texatom" id="MathJax-Span-143" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-144" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-145" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">复</span></span></span></span><span class="texatom" id="MathJax-Span-146" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-147" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-148" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">合</span></span></span></span><span class="texatom" id="MathJax-Span-149" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-150" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-151" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">变</span></span></span></span><span class="texatom" id="MathJax-Span-152" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-153" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-154" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">量</span></span></span></span><span class="texatom" id="MathJax-Span-155" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-156" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-157" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">，</span></span></span></span><span class="texatom" id="MathJax-Span-158" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-159" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-160" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">可</span></span></span></span><span class="texatom" id="MathJax-Span-161" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-162" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-163" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">以</span></span></span></span><span class="texatom" id="MathJax-Span-164" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-165" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-166" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">分</span></span></span></span><span class="texatom" id="MathJax-Span-167" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-168" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-169" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">配</span></span></span></span><span class="texatom" id="MathJax-Span-170" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-171" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-172" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">多</span></span></span></span><span class="texatom" id="MathJax-Span-173" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-174" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-175" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">个</span></span></span></span><span class="texatom" id="MathJax-Span-176" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-177" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-178" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">值</span></span></span></span><span class="texatom" id="MathJax-Span-179" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-180" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-181" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">给</span></span></span></span><span class="texatom" id="MathJax-Span-182" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-183" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-184" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">它</span></span></span></span><span class="texatom" id="MathJax-Span-185" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-186" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-187" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">。</span></span></span></span><span class="texatom" id="MathJax-Span-188" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-189" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-190" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">数</span></span></span></span><span class="texatom" id="MathJax-Span-191" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-192" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-193" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">字</span></span></span></span><span class="texatom" id="MathJax-Span-194" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-195" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-196" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">变</span></span></span></span><span class="texatom" id="MathJax-Span-197" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-198" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-199" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">量</span></span></span></span><span class="texatom" id="MathJax-Span-200" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-201" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-202" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">：</span></span></span></span><span class="texatom" id="MathJax-Span-203" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-204" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-205" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">变</span></span></span></span><span class="texatom" id="MathJax-Span-206" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-207" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-208" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">量</span></span></span></span><span class="texatom" id="MathJax-Span-209" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-210" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-211" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">语</span></span></span></span><span class="texatom" id="MathJax-Span-212" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-213" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-214" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">法</span></span></span></span><span class="texatom" id="MathJax-Span-215" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-216" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-217" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">可</span></span></span></span><span class="texatom" id="MathJax-Span-218" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-219" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-220" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">以</span></span></span></span><span class="texatom" id="MathJax-Span-221" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-222" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-223" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">用</span></span></span></span><span class="texatom" id="MathJax-Span-224" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-225" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-226" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">来</span></span></span></span><span class="texatom" id="MathJax-Span-227" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-228" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-229" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">创</span></span></span></span><span class="texatom" id="MathJax-Span-230" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-231" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-232" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">建</span></span></span></span><span class="texatom" id="MathJax-Span-233" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-234" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-235" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">一</span></span></span></span><span class="texatom" id="MathJax-Span-236" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-237" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-238" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">个</span></span></span></span><span class="texatom" id="MathJax-Span-239" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-240" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-241" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">全</span></span></span></span><span class="texatom" id="MathJax-Span-242" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-243" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-244" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">是</span></span></span></span><span class="texatom" id="MathJax-Span-245" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-246" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-247" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">整</span></span></span></span><span class="texatom" id="MathJax-Span-248" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-249" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-250" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">型</span></span></span></span><span class="texatom" id="MathJax-Span-251" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-252" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-253" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">和</span></span></span></span><span class="texatom" id="MathJax-Span-254" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-255" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-256" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">浮</span></span></span></span><span class="texatom" id="MathJax-Span-257" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-258" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-259" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">点</span></span></span></span><span class="texatom" id="MathJax-Span-260" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-261" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-262" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">型</span></span></span></span><span class="texatom" id="MathJax-Span-263" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-264" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-265" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">的</span></span></span></span><span class="texatom" id="MathJax-Span-266" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-267" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-268" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">数</span></span></span></span><span class="texatom" id="MathJax-Span-269" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-270" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-271" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">字</span></span></span></span><span class="texatom" id="MathJax-Span-272" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-273" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-274" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">：</span></span></span></span><span class="texatom" id="MathJax-Span-275" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-276" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-277" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">整</span></span></span></span><span class="texatom" id="MathJax-Span-278" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-279" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-280" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">型</span></span></span></span></span><span style="display:inline-block; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; width:0px; height:2.146em"></span></span></span><span style="display:inline-block; position:static; border-width:0px 0px 0px 0.004em; border-left-style:solid; border-color:initial; padding:0px; margin:0px; vertical-align:-0.282em; overflow:hidden; width:0px; height:1.361em; color:rgb(255,255,255)"></span></span></nobr></span>{80}、浮点型<span class="MathJax_Preview" style="color:rgb(136,136,136)"></span><span class="MathJax" id="MathJax-Element-2-Frame" style="display:inline; line-height:normal; font-size:14px; word-spacing:normal; word-wrap:normal; white-space:nowrap; float:none; direction:ltr; max-width:none; max-height:none; min-width:0px; min-height:0px; border:0px; padding:0px; margin:0px"><nobr style="border:0px; padding:0px; margin:0px; max-width:none; max-height:none; min-width:0px; min-height:0px; vertical-align:0px"><span class="math" id="MathJax-Span-281" style="display:inline-block; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; width:10.301em"><span style="display:inline-block; position:relative; border:0px; padding:0px; margin:0px; vertical-align:0px; width:8.574em; height:0px; font-size:16.8px"><span style="position:absolute; border:0px; padding:0px; margin:0px; vertical-align:0px; top:-2.14em; left:0.003em"><span class="mrow" id="MathJax-Span-282" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="texatom" id="MathJax-Span-283" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-284" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mn" id="MathJax-Span-285" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Main">3.14</span></span></span><span class="texatom" id="MathJax-Span-286" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-287" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-288" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">。</span></span></span></span><span class="mi" id="MathJax-Span-289" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">B</span><span class="mi" id="MathJax-Span-290" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">o</span><span class="mi" id="MathJax-Span-291" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">o</span><span class="mi" id="MathJax-Span-292" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">l</span><span class="mi" id="MathJax-Span-293" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">e</span><span class="mi" id="MathJax-Span-294" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">a</span><span class="mi" id="MathJax-Span-295" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">n</span><span class="texatom" id="MathJax-Span-296" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-297" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-298" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">变</span></span></span></span><span class="texatom" id="MathJax-Span-299" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-300" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-301" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">量</span></span></span></span><span class="texatom" id="MathJax-Span-302" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-303" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-304" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">：</span></span></span></span></span><span style="display:inline-block; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; width:0px; height:2.146em"></span></span></span><span style="display:inline-block; position:static; border-width:0px 0px 0px 0.004em; border-left-style:solid; border-color:initial; padding:0px; margin:0px; vertical-align:-0.282em; overflow:hidden; width:0px; height:1.361em; color:rgb(255,255,255)"></span></span></nobr></span>{true/false}。 
Null/None 变量：<span class="MathJax_Preview" style="color:rgb(136,136,136)"></span><span class="MathJax" id="MathJax-Element-3-Frame" style="display:inline; line-height:normal; font-size:14px; word-spacing:normal; word-wrap:normal; white-space:nowrap; float:none; direction:ltr; max-width:none; max-height:none; min-width:0px; min-height:0px; border:0px; padding:0px; margin:0px"><nobr style="border:0px; padding:0px; margin:0px; max-width:none; max-height:none; min-width:0px; min-height:0px; vertical-align:0px"><span class="math" id="MathJax-Span-305" style="display:inline-block; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; width:8.396em"><span style="display:inline-block; position:relative; border:0px; padding:0px; margin:0px; vertical-align:0px; width:6.967em; height:0px; font-size:16.8px"><span style="position:absolute; border:0px; padding:0px; margin:0px; vertical-align:0px; top:-2.14em; left:0.003em"><span class="mrow" id="MathJax-Span-306" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="texatom" id="MathJax-Span-307" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-308" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mi" id="MathJax-Span-309" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">n</span><span class="mi" id="MathJax-Span-310" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">u</span><span class="mi" id="MathJax-Span-311" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">l</span><span class="mi" id="MathJax-Span-312" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">l</span><span class="texatom" id="MathJax-Span-313" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-314" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-315" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Main">/</span></span></span><span class="mi" id="MathJax-Span-316" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">N<span style="display:inline-block; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; overflow:hidden; height:1px; width:0.063em"></span></span><span class="mi" id="MathJax-Span-317" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">o</span><span class="mi" id="MathJax-Span-318" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">n</span><span class="mi" id="MathJax-Span-319" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">e</span></span></span><span class="texatom" id="MathJax-Span-320" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-321" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-322" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">。</span></span></span></span><span class="texatom" id="MathJax-Span-323" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-324" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-325" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">空</span></span></span></span><span class="texatom" id="MathJax-Span-326" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-327" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-328" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">格</span></span></span></span></span><span style="display:inline-block; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; width:0px; height:2.146em"></span></span></span><span style="display:inline-block; position:static; border-width:0px 0px 0px 0.004em; border-left-style:solid; border-color:initial; padding:0px; margin:0px; vertical-align:-0.354em; overflow:hidden; width:0px; height:1.432em; color:rgb(255,255,255)"></span></span></nobr></span>{SPACE} 和空${EMPTY} 变量等。 
图 9\. 添加变量 
![](http://imglf0.nosdn.127.net/img/bS9RU1VmT1M3bWtscUNRaHQrY1FHSWZhZzRZekkyRkFneVVHVVM5d0NxNTlZL0NWQ3VGbGZ3PT0.png?imageView&thumbnail=500x0&quality=96&stripmeta=0&type=jpg) 
<span style="">Demo：</span> 
Open Application Calculator：打开手机自带的计算器 
<span style="">Edit</span> 
![](http://imglf0.nosdn.127.net/img/bS9RU1VmT1M3bWtscUNRaHQrY1FHSDJnTFlrZHpYZTA2ZjYxRzBQcGp1UThiejZ5eFNjZHdRPT0.png?imageView&thumbnail=500x0&quality=96&stripmeta=0&type=jpg) 
<span style="">Text Edit</span> 
![](http://imglf2.nosdn.127.net/img/bS9RU1VmT1M3bWtscUNRaHQrY1FHQ0dDS1FraERuTXFxcTRuUWlEc1ZlMFFnMzN1c0xjVkR3PT0.png?imageView&thumbnail=500x0&quality=96&stripmeta=0&type=jpg) 
<span style="">PS</span>：第六行是一行，没有第七行 
<span style="">说明</span> 
“Open Application”：Keywords，方法,后面的全是参数。 
[http://localhost:4723/wd/hub](http://localhost:4723/wd/hub) ，手机的url，这里一般固定不变 
platformName，平台名称，[Android](http://lib.csdn.net/base/android "Android知识库")或者[iOS](http://lib.csdn.net/base/ios "iOS知识库") 
platformVersion，平台版本，也就是Android的版本号 
deviceName，设备名称，就是运行中的模拟器的名称，如果不知道，可以通过在命令行中输入adb devices指令取得。 
appPackage，app的包名，UiautomatorView可以获取 
appActivity，app打开首页activity name，获取命令 
`adb logcat ActivityManager:I *:s` 

[adb logcat 查看日志](http://blog.csdn.net/xyz_lmn/article/details/7004710):[http://blog.csdn.net/xyz_lmn/article/details/7004710](http://blog.csdn.net/xyz_lmn/article/details/7004710)
如下图是华为setting的activity 
![](http://imglf.nosdn.127.net/img/bS9RU1VmT1M3bWtscUNRaHQrY1FHQWZMT1FQSW9zU2hrK3hneWcrc3MrRU10cXFtdy9lSUtBPT0.png?imageView&thumbnail=500x0&quality=96&stripmeta=0&type=jpg)

logcat 详细使用说明：http://blog.csdn.net/xyz_lmn/article/details/7004710

### <a target="_blank" name="t19" style="color:rgb(51,102,153)"></a>运行测试用例

以上几步完成后，就可以在 Run 页面，进行运行，并查看结果，具体如图 10 所示： 
在运行完测试之后，也可以进行查看 log 文件等操作。 
图 10\. 运行测试用例 
![](http://imglf.nosdn.127.net/img/bS9RU1VmT1M3bWtscUNRaHQrY1FHRnlMbDlYYmtpWTJIN0lkeXFBQnhZZUVKWEhKeGZ0SkRRPT0.png?imageView&thumbnail=500x0&quality=96&stripmeta=0&type=jpg)

## <a target="_blank" name="t20" style="color:rgb(51,102,153)"></a>简单的测试用例的编写

安装完成 RF 之后，通过 RIDE 编辑器的介绍，对 RF 的工作原理有一定了解之后，在这一部分主要给大家介绍一个简单的实例：从服务器上下载指定的文件。 
首先按照上面的步骤来进行：创建项目—->创建 Test Suite—->创建 Test Case。 
创建项目 
菜单 File -> New Project，在弹出“New Project”对话框选择 Type 为 Directory，然后填写 Name，点击 OK 按钮。 
创建 Test Suite 
在已创建的项目上点击鼠标右键，选择 New Suite，在弹出“Add Suite”对话框中选择 Type 为 File，然后填写 Name，点击 OK 按钮。 
添加所需的库文件，选定 Suite 然后点击右边 Library 按钮，在弹出对话框的 Name 后输入 FtpLibrary 并点击 OK 按钮，添加其他 Library 也是如此，具体如图 11 所示： 
图 11\. 添加 Library 
![](http://imglf2.nosdn.127.net/img/bS9RU1VmT1M3bWtscUNRaHQrY1FHTFlrQUxZVFR4cEVsUHlIa2F5SzJSNHhtMUx4SGFrV1RBPT0.png?imageView&thumbnail=500x0&quality=96&stripmeta=0&type=jpg) 
点击查看大图 
添加所需的变量，选定 Suite 然后点击右边 Add Scalar 按钮，在弹出对话框的 Name 后输入变量名，注意变量的结构是${name}or @{name}，在 Value 后输入变量的值。 
图 12\. 添加变量 
![](http://imglf2.nosdn.127.net/img/bS9RU1VmT1M3bWtscUNRaHQrY1FHTWxvTlNBVjk4cVhjS0h1TXJOTzgvLzVVYnMweGpMUTB3PT0.png?imageView&thumbnail=500x0&quality=96&stripmeta=0&type=jpg) 
点击查看大图 
创建 Test Case 
在已创建的 suite 点击鼠标右键选择 New Test Case，在弹出对话框的 Name 填写 Name，点击 OK 按钮。 
至此，项目已经创建好了，Suite 创建了也添加了所需要的 Library，Test Case 也创建好了，接下来就可以在 Test Case 里编写测试用例了，也就是在表格输入关键字和参数或变量。 
图 13.TestCase 实例 
![](http://imglf.nosdn.127.net/img/bS9RU1VmT1M3bWtscUNRaHQrY1FHTUxDS3oxMjdNY29YQ1JhQUhhMUhrRzJoZ3NUcEZ6V213PT0.png?imageView&thumbnail=500x0&quality=96&stripmeta=0&type=jpg) 
点击查看大图 
注：在图中表格里的蓝色字体是库中的关键字，绿色字体是变量，黑色字体是系统自带关键字。 
下面对 OnPremise 这个 test case 进行解释。 
图 14.OnPremise–连接 FTP 服务器 
![](http://imglf.nosdn.127.net/img/bS9RU1VmT1M3bWtscUNRaHQrY1FHTTJyUkc2dVVENnR4NG1LTW1XZHJNZjNrYS8yY3hScjlnPT0.png?imageView&thumbnail=500x0&quality=96&stripmeta=0&type=jpg) 
点击查看大图 
目的：连接 FTP 服务器。 
通过关键字 ftp connect 以及参数，包括用户名<span class="MathJax_Preview" style="color:rgb(136,136,136)"></span><span class="MathJax" id="MathJax-Element-4-Frame" style="display:inline; line-height:normal; font-size:14px; word-spacing:normal; word-wrap:normal; white-space:nowrap; float:none; direction:ltr; max-width:none; max-height:none; min-width:0px; min-height:0px; border:0px; padding:0px; margin:0px"><nobr style="border:0px; padding:0px; margin:0px; max-width:none; max-height:none; min-width:0px; min-height:0px; vertical-align:0px"><span class="math" id="MathJax-Span-329" style="display:inline-block; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; width:11.074em"><span style="display:inline-block; position:relative; border:0px; padding:0px; margin:0px; vertical-align:0px; width:9.229em; height:0px; font-size:16.8px"><span style="position:absolute; border:0px; padding:0px; margin:0px; vertical-align:0px; top:-1.961em; left:0.003em"><span class="mrow" id="MathJax-Span-330" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="texatom" id="MathJax-Span-331" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-332" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mi" id="MathJax-Span-333" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">u</span><span class="mi" id="MathJax-Span-334" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">n</span><span class="mi" id="MathJax-Span-335" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">a</span><span class="mi" id="MathJax-Span-336" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">m</span><span class="msubsup" id="MathJax-Span-337" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="display:inline-block; position:relative; border:0px; padding:0px; margin:0px; vertical-align:0px; width:0.836em; height:0px"><span style="position:absolute; border:0px; padding:0px; margin:0px; vertical-align:0px; top:-1.961em; left:0.003em"><span class="mi" id="MathJax-Span-338" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">e</span><span style="display:inline-block; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; width:0px; height:1.967em"></span></span><span style="position:absolute; border:0px; padding:0px; margin:0px; vertical-align:0px; top:-1.545em; left:0.42em"><span class="mi" id="MathJax-Span-339" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-size:11.8776px; font-family:MathJax_Math-italic">f<span style="display:inline-block; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; overflow:hidden; height:1px; width:0.063em"></span></span><span style="display:inline-block; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; width:0px; height:1.729em"></span></span></span></span><span class="mi" id="MathJax-Span-340" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">t</span><span class="msubsup" id="MathJax-Span-341" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="display:inline-block; position:relative; border:0px; padding:0px; margin:0px; vertical-align:0px; width:0.836em; height:0px"><span style="position:absolute; border:0px; padding:0px; margin:0px; vertical-align:0px; top:-1.961em; left:0.003em"><span class="mi" id="MathJax-Span-342" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">p</span><span style="display:inline-block; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; width:0px; height:1.967em"></span></span><span style="position:absolute; border:0px; padding:0px; margin:0px; vertical-align:0px; top:-1.485em; left:0.479em"><span class="mi" id="MathJax-Span-343" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-size:11.8776px; font-family:MathJax_Math-italic">s</span><span style="display:inline-block; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; width:0px; height:1.729em"></span></span></span></span><span class="mi" id="MathJax-Span-344" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">e</span><span class="mi" id="MathJax-Span-345" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">r</span><span class="mi" id="MathJax-Span-346" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">v</span><span class="mi" id="MathJax-Span-347" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">e</span><span class="mi" id="MathJax-Span-348" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">r</span></span></span><span class="texatom" id="MathJax-Span-349" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-350" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-351" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">和</span></span></span></span><span class="texatom" id="MathJax-Span-352" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-353" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-354" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">密</span></span></span></span><span class="texatom" id="MathJax-Span-355" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-356" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-357" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">码</span></span></span></span></span><span style="display:inline-block; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; width:0px; height:1.967em"></span></span></span><span style="display:inline-block; position:static; border-width:0px 0px 0px 0.004em; border-left-style:solid; border-color:initial; padding:0px; margin:0px; vertical-align:-0.425em; overflow:hidden; width:0px; height:1.432em; color:rgb(255,255,255)"></span></span></nobr></span>{pwd_ftp_sever}，来连接 FTP 服务器${build_ftp_sever}，并设定超时时间为 300 秒。 
图 15.OnPremise–记录当前路径 
![](http://imglf1.nosdn.127.net/img/bS9RU1VmT1M3bWtscUNRaHQrY1FHUEw5dytJdS9NTkxKNm1Ca2JjSHhSc3E5eFlnUk5xZkhnPT0.png?imageView&thumbnail=500x0&quality=96&stripmeta=0&type=jpg) 
目的：记录当前路径。 
Cwd 关键字切换并进入所需路径<span class="MathJax_Preview" style="color:rgb(136,136,136)"></span><span class="MathJax" id="MathJax-Element-5-Frame" style="display:inline; line-height:normal; font-size:14px; word-spacing:normal; word-wrap:normal; white-space:nowrap; float:none; direction:ltr; max-width:none; max-height:none; min-width:0px; min-height:0px; border:0px; padding:0px; margin:0px"><nobr style="border:0px; padding:0px; margin:0px; max-width:none; max-height:none; min-width:0px; min-height:0px; vertical-align:0px"><span class="math" id="MathJax-Span-358" style="display:inline-block; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; width:25.836em"><span style="display:inline-block; position:relative; border:0px; padding:0px; margin:0px; vertical-align:0px; width:21.491em; height:0px; font-size:16.8px"><span style="position:absolute; border:0px; padding:0px; margin:0px; vertical-align:0px; top:-1.961em; left:0.003em"><span class="mrow" id="MathJax-Span-359" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="texatom" id="MathJax-Span-360" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-361" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mi" id="MathJax-Span-362" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">p</span><span class="mi" id="MathJax-Span-363" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">a</span><span class="mi" id="MathJax-Span-364" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">t</span><span class="msubsup" id="MathJax-Span-365" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="display:inline-block; position:relative; border:0px; padding:0px; margin:0px; vertical-align:0px; width:0.955em; height:0px"><span style="position:absolute; border:0px; padding:0px; margin:0px; vertical-align:0px; top:-1.961em; left:0.003em"><span class="mi" id="MathJax-Span-366" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">h</span><span style="display:inline-block; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; width:0px; height:1.967em"></span></span><span style="position:absolute; border:0px; padding:0px; margin:0px; vertical-align:0px; top:-1.545em; left:0.539em"><span class="mi" id="MathJax-Span-367" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-size:11.8776px; font-family:MathJax_Math-italic">f<span style="display:inline-block; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; overflow:hidden; height:1px; width:0.063em"></span></span><span style="display:inline-block; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; width:0px; height:1.729em"></span></span></span></span><span class="mi" id="MathJax-Span-368" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">t</span><span class="msubsup" id="MathJax-Span-369" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="display:inline-block; position:relative; border:0px; padding:0px; margin:0px; vertical-align:0px; width:0.836em; height:0px"><span style="position:absolute; border:0px; padding:0px; margin:0px; vertical-align:0px; top:-1.961em; left:0.003em"><span class="mi" id="MathJax-Span-370" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">p</span><span style="display:inline-block; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; width:0px; height:1.967em"></span></span><span style="position:absolute; border:0px; padding:0px; margin:0px; vertical-align:0px; top:-1.485em; left:0.479em"><span class="mi" id="MathJax-Span-371" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-size:11.8776px; font-family:MathJax_Math-italic">s</span><span style="display:inline-block; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; width:0px; height:1.729em"></span></span></span></span><span class="mi" id="MathJax-Span-372" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">e</span><span class="mi" id="MathJax-Span-373" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">r</span><span class="mi" id="MathJax-Span-374" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">v</span><span class="mi" id="MathJax-Span-375" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">e</span><span class="mi" id="MathJax-Span-376" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">r</span></span></span><span class="texatom" id="MathJax-Span-377" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-378" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-379" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">，</span></span></span></span><span class="texatom" id="MathJax-Span-380" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-381" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-382" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">然</span></span></span></span><span class="texatom" id="MathJax-Span-383" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-384" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-385" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">后</span></span></span></span><span class="texatom" id="MathJax-Span-386" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-387" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-388" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">通</span></span></span></span><span class="texatom" id="MathJax-Span-389" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-390" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-391" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">过</span></span></span></span><span class="mi" id="MathJax-Span-392" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">P<span style="display:inline-block; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; overflow:hidden; height:1px; width:0.122em"></span></span><span class="mi" id="MathJax-Span-393" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">w</span><span class="mi" id="MathJax-Span-394" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">d<span style="display:inline-block; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; overflow:hidden; height:1px; width:0.003em"></span></span><span class="texatom" id="MathJax-Span-395" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-396" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-397" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">输</span></span></span></span><span class="texatom" id="MathJax-Span-398" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-399" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-400" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">出</span></span></span></span><span class="texatom" id="MathJax-Span-401" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-402" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-403" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">当</span></span></span></span><span class="texatom" id="MathJax-Span-404" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-405" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-406" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">前</span></span></span></span><span class="texatom" id="MathJax-Span-407" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-408" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-409" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">路</span></span></span></span><span class="texatom" id="MathJax-Span-410" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-411" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-412" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">径</span></span></span></span><span class="texatom" id="MathJax-Span-413" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-414" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-415" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">并</span></span></span></span><span class="texatom" id="MathJax-Span-416" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-417" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-418" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">保</span></span></span></span><span class="texatom" id="MathJax-Span-419" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-420" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-421" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">存</span></span></span></span><span class="texatom" id="MathJax-Span-422" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-423" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-424" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">到</span></span></span></span><span class="texatom" id="MathJax-Span-425" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-426" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-427" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">变</span></span></span></span><span class="texatom" id="MathJax-Span-428" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-429" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-430" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">量</span></span></span></span></span><span style="display:inline-block; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; width:0px; height:1.967em"></span></span></span><span style="display:inline-block; position:static; border-width:0px 0px 0px 0.004em; border-left-style:solid; border-color:initial; padding:0px; margin:0px; vertical-align:-0.425em; overflow:hidden; width:0px; height:1.432em; color:rgb(255,255,255)"></span></span></nobr></span>{output} 中。 
图 16.OnPremise–创建本地文件夹 
![](http://imglf.nosdn.127.net/img/bS9RU1VmT1M3bWtscUNRaHQrY1FHRW11TEdmOUxlRE9vMzZwa3dFbEE3MUlSdzlXTWsvT3J3PT0.png?imageView&thumbnail=500x0&quality=96&stripmeta=0&type=jpg) 
点击查看大图 
目的：创建本地文件夹，用来存放下载的文件。 
由于服务器路径目录是以日期结束，将此通过 Split String From Right 关键字分离出来并保存到<span class="MathJax_Preview" style="color:rgb(136,136,136)"></span><span class="MathJax" id="MathJax-Element-6-Frame" style="display:inline; line-height:normal; font-size:14px; word-spacing:normal; word-wrap:normal; white-space:nowrap; float:none; direction:ltr; max-width:none; max-height:none; min-width:0px; min-height:0px; border:0px; padding:0px; margin:0px"><nobr style="border:0px; padding:0px; margin:0px; max-width:none; max-height:none; min-width:0px; min-height:0px; vertical-align:0px"><span class="math" id="MathJax-Span-431" style="display:inline-block; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; width:18.217em"><span style="display:inline-block; position:relative; border:0px; padding:0px; margin:0px; vertical-align:0px; width:15.182em; height:0px; font-size:16.8px"><span style="position:absolute; border:0px; padding:0px; margin:0px; vertical-align:0px; top:-1.961em; left:0.003em"><span class="mrow" id="MathJax-Span-432" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="texatom" id="MathJax-Span-433" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-434" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mi" id="MathJax-Span-435" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">c</span><span class="mi" id="MathJax-Span-436" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">u</span><span class="mi" id="MathJax-Span-437" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">r</span><span class="mi" id="MathJax-Span-438" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">r</span><span class="mi" id="MathJax-Span-439" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">e</span><span class="mi" id="MathJax-Span-440" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">n</span><span class="mi" id="MathJax-Span-441" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">t</span><span class="mi" id="MathJax-Span-442" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">B</span><span class="mi" id="MathJax-Span-443" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">u</span><span class="mi" id="MathJax-Span-444" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">i</span><span class="mi" id="MathJax-Span-445" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">l</span><span class="mi" id="MathJax-Span-446" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">d<span style="display:inline-block; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; overflow:hidden; height:1px; width:0.003em"></span></span><span class="mi" id="MathJax-Span-447" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">L</span><span class="mi" id="MathJax-Span-448" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">e</span><span class="mi" id="MathJax-Span-449" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">v</span><span class="mi" id="MathJax-Span-450" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">e</span><span class="mi" id="MathJax-Span-451" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:MathJax_Math-italic">l</span></span></span><span class="texatom" id="MathJax-Span-452" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-453" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-454" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">，</span></span></span></span><span class="texatom" id="MathJax-Span-455" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-456" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-457" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">最</span></span></span></span><span class="texatom" id="MathJax-Span-458" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-459" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-460" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">后</span></span></span></span><span class="texatom" id="MathJax-Span-461" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-462" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-463" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">生</span></span></span></span><span class="texatom" id="MathJax-Span-464" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-465" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-466" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">成</span></span></span></span><span class="texatom" id="MathJax-Span-467" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-468" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-469" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">完</span></span></span></span><span class="texatom" id="MathJax-Span-470" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-471" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-472" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">整</span></span></span></span><span class="texatom" id="MathJax-Span-473" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-474" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-475" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">路</span></span></span></span><span class="texatom" id="MathJax-Span-476" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mrow" id="MathJax-Span-477" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span class="mo" id="MathJax-Span-478" style="display:inline; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px"><span style="position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; font-family:STIXGeneral,'Arial Unicode MS',serif; font-size:13.944px">径</span></span></span></span></span><span style="display:inline-block; position:static; border:0px; padding:0px; margin:0px; vertical-align:0px; width:0px; height:1.967em"></span></span></span><span style="display:inline-block; position:static; border-width:0px 0px 0px 0.004em; border-left-style:solid; border-color:initial; padding:0px; margin:0px; vertical-align:-0.282em; overflow:hidden; width:0px; height:1.361em; color:rgb(255,255,255)"></span></span></nobr></span>{currentDestination}，并通过 Create Directory 关键字来创建目标文件夹。 
图 17.OnPremise–下载所有所需的文件 
![](http://imglf0.nosdn.127.net/img/bS9RU1VmT1M3bWtscUNRaHQrY1FHQzVXWFNKaFJPdWhuOXFWamlvcDRWSWIwUmZFSGJibXd3PT0.png?imageView&thumbnail=500x0&quality=96&stripmeta=0&type=jpg) 
点击查看大图 
目的：下载所有所需的文件。 
需要下载的文件不止一个，可通过 FOR 循环在列表变量 @{targetFiles} 中分别取出目标文件名，再通过 Download File 关键字来逐一下载并保存到${currentDestination} 路径下。 
回页首 
总结 
Robot framework 关键字自动化框架，它拥有强大而丰富的 Library，以及简单易用的关键字方式的使用，可以很好地支持全球化测试部门的测试工作，从而减少编写代码的时间同时也大大地提高了工作效率。相信通过对 Robot framework 关键字自动化框架更深的使用和了解，将不仅仅只是帮助自动下载文件，也会在更多更广的方面带来越来越多的益处。

## <a target="_blank" name="t21" style="color:rgb(51,102,153)"></a>知识点：

1.  Robotframework 的基本使用，掌握buildin的方法 
    Log，Run keyword if以及数据类型等等
2.  Uiautomatorview获取app元素
3.  Appium 元素的定位和click,swipe点击操作。

## <a target="_blank" name="t22" style="color:rgb(51,102,153)"></a>参考资料

<span style="">Robotframework官网</span>

> [Robotframework-首页 ](http://robotframework.org/)
> [Robotframework-user guide](http://robotframework.org/robotframework/#user-guide)

<span style="">github地址</span>

> [Selenium2Library](https://github.com/robotframework/Selenium2Library) 
> [robotframework-appiumlibrary](https://github.com/piaoransk/robotframework-appiumlibrary)

## <a target="_blank" name="t23" style="color:rgb(51,102,153)"></a>FAQ

<span style="">1\. Pip安装失败，连接不上服务器</span> 
使用镜像的方法可以在每次执行pip的时候加上参数”-i [http://e.pypi.python.org/simple](http://e.pypi.python.org/simple)“即可， 
或者也可以在本地配置，这样就不用每次都加上参数了，应用Cheer Xiao的配置（[http://blog.makto.me/post/2012-11-01/pypi-mirror](http://blog.makto.me/post/2012-11-01/pypi-mirror)）： 
`[global] 
index-url=http://mirrors.tuna.tsinghua.edu.cn/pypi/simple` 
<span style="">2\. 问题异常: ‘ascii’ codec can’t encode characters</span> 
“C:\Python27\lib\site-packages\pip-8.1.2-py2.7.egg\pip_vendor\colorama\ansitowin32.py”, line 174, in write_plain_text 
self.wrapped.write(text[start:end]) 
UnicodeEncodeError: ‘ascii’ codec can’t encode character u’\u258a’ in position 8: ordinal not in range(128) 
解决办法： 
字符集的问题，在文件前加两句话： 
reload(sys) 
sys.setdefaultencoding( “utf-8” ) 
完美解决，ok 
<span style="">ps</span> 当字符串里有 \n、\t、\r时，json.loads()失效，异常，要去掉 
<span style="">3\. pip的安装</span> 
先安装setuptools 
<span style="">4\. 出现Unable to find vcvarsall.bat问题</span> 
安装vs2008或者更新新版本都可以 
[http://stackoverflow.com/questions/2817869/error-unable-to-find-vcvarsall-bat](http://stackoverflow.com/questions/2817869/error-unable-to-find-vcvarsall-bat) 
[http://blog.csdn.net/secretx/article/details/17472107](http://blog.csdn.net/secretx/article/details/17472107) 
<span style="">5\. 如何开发系统关键字</span> 
[http://note.youdao.com/noteshare?id=32cb67775f6ee73642c4ff768b581853](http://note.youdao.com/noteshare?id=32cb67775f6ee73642c4ff768b581853) 
<span style="">6\. 如何定位元素</span> 
[http://note.youdao.com/noteshare?id=3842ebf1411a12f1fc49e2e2e5bc49c9](http://note.youdao.com/noteshare?id=3842ebf1411a12f1fc49e2e2e5bc49c9) 
<span style="">7\. 多个元素如何定位</span> 
利用xpath 
<span style="">8\. 用pybot命令有3种执行RF用例的方式：</span> 
http://note.youdao.com/noteshare?id=b1d1f4b6c1739c74fff7da24b16bfda7 
<span style="">9.更多分享</span> 
[http://note.youdao.com/noteshare?id=d33942274ccaaa9cb4e07440c9fd0136](http://note.youdao.com/noteshare?id=d33942274ccaaa9cb4e07440c9fd0136)

<link rel="stylesheet" href="http://static.blog.csdn.net/public/res-min/markdown_views.css?v=1.0"></div>

</dd>

</dl>

</div>

<div class="skin_nav">

<div class="skin_edit">

<div class="nav_list nav_list_edit">[文章列表](/xyh421)</div>

</div>

<div class="skin_edit">

<div class="nav_list nav_list_edit">[写博文](http://write.blog.csdn.net/postedit)</div>

</div>

<div class="skin_set">

<div class="nav_list nav_list_edit">[管理博客](http://write.blog.csdn.net/postlist)</div>

</div>

</div>

<div class="rssFix">[](http://blog.csdn.net/xyh421/rss/list)</div>

</div>

<div class="detail_b">

版权声明：本文为博主原创文章，未经博主允许不得转载。

## <label id="digg" articleid="52119872" onclick="btndigga();"><span id="btnDigg">顶</span>_2_</label> <label id="bury" onclick="btnburya();"><span id="btnBury">踩</span>_0_</label>

<div class="tracking-ad" data-mod="popu_222">[ ](javascript:void(0);)</div>

<div class="tracking-ad" data-mod="popu_223">[ ](javascript:void(0);)</div>

<script type="text/javascript">function btndigga() { $(".tracking-ad[data-mod='popu_222'] a").click(); } function btnburya() { $(".tracking-ad[data-mod='popu_223'] a").click(); } $(function () { if ($(".markdown_views").length > 0) { if($("#fromjs").length==0) { $('pre.prettyprint code').each(function () { var lines = $(this).text().split('\n').length; var $numbering = $('<ul/>').addClass('pre-numbering').hide(); $(this).addClass('has-numbering').parent().append($numbering); for (i = 1; i <= lines; i++) { $numbering.append($('<li/>').text(i)); }; $numbering.fadeIn(1700); }); } } else { $("#article_content pre").each(function () { var $this = $(this); if ($this.attr("class") != undefined) { if ($this.attr("class").indexOf("brush:") != -1) { var lang = $this.attr("class").split(';')[0].split(':')[1]; $this.attr('name', 'code'); $this.attr('class', lang); } if ($this.attr("class")) { $this.attr('name', 'code'); } } }); $('#article_content textarea[name=code]').each(function () { var $this = $(this); if ($this.attr("class").indexOf(":") != -1) { $this.attr("class", $this.attr("class").split(':')[0]); } }); dp.SyntaxHighlighter.HighlightAll('code'); $('.highlighter').addClass('dp-highlighter'); if (!window.clipboardData) { setTimeout("setCopyBtn()", 500); } function __get_code_toolbar(snippet_id) { return $("<span class='tracking-ad' data-mod='popu_167'>[![在CODE上查看代码片](https://code.csdn.net/assets/CODE_ico.png)](https://code.csdn.net/snippets/ "在CODE上查看代码片")</span>" + "<span class='tracking-ad' data-mod='popu_170'>[![派生到我的代码片](https://code.csdn.net/assets/ico_fork.svg)](https://code.csdn.net/snippets/ "派生到我的代码片")</span>"); } $("[code_snippet_id]").each(function () { __s_id = $(this).attr("code_snippet_id"); if (__s_id != null && __s_id != "" && __s_id != 0 && parseInt(__s_id) > 70020) { __code_tool = __get_code_toolbar(__s_id); $(this).prev().find(".tools").append(__code_tool); } }); $(".bar").show(); } });</script>

<div class="blog_share">

<div class="bdsharebuttonbox tracking-ad" style="float: right;" data-mod="popu_172">[](#)[](# "分享到QQ空间")[](# "分享到新浪微博")[](# "分享到腾讯微博")[](# "分享到人人网")[](# "分享到微信")</div>

<script>window._bd_share_config = { "common": { "bdSnsKey": {}, "bdText": "", "bdMini": "1", "bdMiniList": false, "bdPic": "", "bdStyle": "0", "bdSize": "16" }, "share": {} }; with (document) 0[(getElementsByTagName('head')[0] || body).appendChild(createElement('script')).src = 'http://bdimg.share.baidu.com/static/api/js/share.js?v=89860593.js?cdnversion=' + ~(-new Date() / 36e5)];</script></div>

<div class="forward_back">

<div class="back fl">[<span></span>_UnicodeEncodeError: 'ascii' codec can't encode characters in position 9-14_](javascript:void(0);)</div>

<div class="forward fr">[_AppiumLibrary 1.3.5英文api文档_<span></span>](javascript:void(0);)</div>

</div>

<div><script type="text/javascript">/*博客内容页下方Banner-728*90，创建于2014-7-3*/ var cpro_id = "u1607657";</script></div>

<div class="comment" id="comment_form">

<div id="commentsbmitarear">

## 发表评论

<dl class="publish_comment clearfix" id="commentbox">

<dt>[![](http://avatar.csdn.net/5/F/9/1_xyh421.jpg)](http://my.csdn.net/xyh421)</dt>

<dd>

<form action="/xyh421/comment/submit?id=52119872" method="post" onsubmit="return subform(this);" id="commentform"><textarea class="publish_txt" id="comment_content"></textarea>

<div class="publish clearfix"><input type="hidden" id="comment_replyId" name="comment_replyId"> <input type="hidden" id="comment_userId" name="comment_userId" value=""> <input type="hidden" id="commentId" name="commentId" value=""> [ 发表评论](javascript:void(0);)  <span id="tip_comment" style="color: Red; display: none;"></span>

<div class="comment-code-pop J_lang_list" id="lang_list" code="code">[HTML/XML](#html)[objective-c](#objc)[Delphi](#delphi)[Ruby](#ruby)[PHP](#php)[C#](#csharp)[C++](#cpp)[JavaScript](#javascript)[Visual Basic](#vb)[Python](#python)[Java](#java)[CSS](#css)[SQL](#sql)[其它](#plain)<span class="arrb"></span></div>

</div>

</form>

</dd>

</dl>

</div>

<a name="comments"></a></div>

</div>

</div>

</div>

<div class="skin_right">

<div id="skin_r_wrap" class="skin_r_wrap">

<div id="skin_r" class="skin_r">

<div class="mess">[![img](http://avatar.csdn.net/5/F/9/1_xyh421.jpg)](http://my.csdn.net/xyh421)

xyh421

<div class="grade">

<span>等级：</span>![](http://c.csdnimg.cn/jifen/images/xunzhang/jianzhang/blog2.png)

<span>排名：</span><span>千里之外</span>

</div>

<div class="blog_medal">[](http://blog.csdn.net/experts/rule.html)

<div class="attention">[<span>加关注</span>](javascript:void(0);) [<span>发私信</span>](javascript:void(0);)</div>

</div>

</div>

<div class="classify">

<dl class="classify_list">

<div class="article_search">

<div class="article_search_c">

<form id="frmSearch" action="http://so.csdn.net/search" class="form_search csdn-tracking-statistics" target="_blank" data-mod="popu_306"><input type="text" id="inputSearch" placeholder="文章搜索"></form>

</div>

</div>

</dl>

<script type="text/javascript">$(function () { $("#btnSubmit").unbind("click"); $("#btnSubmit").click(function () { search(); }); $("#frmSearch").submit(function () { search(); return false; }); function search() { if ($("#inputSearch").val() == "") { alert("请录入搜索关键词！"); return false; } //var url = "http://so.csdn.net/so/search/s.do?q=" + encodeURIComponent($("#inputSearch").val()) + "&u=" + username + "&t=blog"; var url = "https://www.baidu.com/s?wd=" + encodeURIComponent($("#inputSearch").val()) + "%20site%3Ablog.csdn.net" window.location.href = url; } });</script>

<dl class="classify_list">

<dt>[博客专栏](/xyh421/blog/column)</dt>

</dl>

<dl class="classify_list js_list">

<dt>

<div class="js_column_wrap"><span class="column">文章分类</span></div>

*   [Python](/xyh421/article/category/6346559)<span>（7）</span>
*   [automator test](/xyh421/article/category/6348263)<span>（2）</span>
*   [appiumlibrary](/xyh421/article/category/6360616)<span>（2）</span>
*   [robotframework](/xyh421/article/category/6360617)<span>（9）</span>
*   [Selenium2Library](/xyh421/article/category/6552367)<span>（3）</span>
*   [chromedriver](/xyh421/article/category/6728938)<span>（1）</span>
*   [AutoItLibrary](/xyh421/article/category/6763772)<span>（1）</span>
*   [com_error](/xyh421/article/category/6763773)<span>（0）</span>
*   [gerrit安装](/xyh421/article/category/6846231)<span>（0）</span>
*   [atom](/xyh421/article/category/6854415)<span>（1）</span>
*   [Ubuntu](/xyh421/article/category/6872098)<span>（6）</span>
*   [sikuli](/xyh421/article/category/6872099)<span>（5）</span>
*   [Xvfb](/xyh421/article/category/6908130)<span>（2）</span>
*   [chrome version](/xyh421/article/category/6959533)<span>（1）</span>
*   [chrome](/xyh421/article/category/6960275)<span>（1）</span>

</dt>

<dd style="display:none">[](#)</dd>

</dl>

<dl class="classify_list js_list">

<dt>

<div class="js_column_wrap"><span class="column">文章存档</span></div>

*   [2017年06月](/xyh421/article/month/2017/06)<span>(6)</span>
*   [2017年05月](/xyh421/article/month/2017/05)<span>(2)</span>
*   [2017年04月](/xyh421/article/month/2017/04)<span>(6)</span>
*   [2017年03月](/xyh421/article/month/2017/03)<span>(5)</span>
*   [2017年02月](/xyh421/article/month/2017/02)<span>(1)</span>
*   [2016年12月](/xyh421/article/month/2016/12)<span>(1)</span>
*   [2016年11月](/xyh421/article/month/2016/11)<span>(2)</span>
*   [2016年08月](/xyh421/article/month/2016/08)<span>(5)</span>

</dt>

</dl>

<dl class="classify_list js_list">

<dt>

<div class="js_column_wrap"><span class="column">阅读排行</span></div>

*   [Robot Framework +Appium的简单教程及实例](/xyh421/article/details/52119872)<span>（4195）</span>
*   [QA 这个职位在中国有前途么？转自知乎](/xyh421/article/details/52241385)<span>（657）</span>
*   [AppiumLibrary 1.3.5英文api文档](/xyh421/article/details/52183287)<span>（553）</span>
*   [selenium之 chromedriver与chrome版本映射表(更新至v2.27)](/xyh421/article/details/55258630)<span>（459）</span>
*   [selenium2library 如何定位伪元素,比如::before](/xyh421/article/details/68067575)<span>（430）</span>
*   [关于Python的面试题 （github）](/xyh421/article/details/53172761)<span>（391）</span>
*   [解决appiumlibrary中click a point 点击无效](/xyh421/article/details/64453518)<span>（361）</span>
*   [解决import _tkinter时提示ImportError: DLL load failed: %1 不是有效的 Win32 应用程序。](/xyh421/article/details/64166423)<span>（291）</span>
*   [解决问题:"Pyperclip could not find a copy/paste mechanism for your system. "](/xyh421/article/details/70154320)<span>（291）</span>
*   [解决问题：Initializing test library 'AutoItLibrary' with no arguments failed: com_error: (-2147221164, '\](/xyh421/article/details/60141804)<span>（287）</span>

</dt>

</dl>

<dl class="classify_list js_list">

<dt>

<div class="js_column_wrap"><span class="column">评论排行</span></div>

*   [解决appiumlibrary中click a point 点击无效](/xyh421/article/details/64453518)<span>（2）</span>
*   [selenium2library 如何定位伪元素,比如::before](/xyh421/article/details/68067575)<span>（2）</span>
*   [如何用vncview查看xvfb里面的画面呢](/xyh421/article/details/73378124)<span>（2）</span>
*   [解决问题：Initializing test library 'AutoItLibrary' with no arguments failed: com_error: (-2147221164, '\](/xyh421/article/details/60141804)<span>（0）</span>
*   [selenium之 chromedriver与chrome版本映射表(更新至v2.27)](/xyh421/article/details/55258630)<span>（0）</span>
*   [Selenium2Library 英文api](/xyh421/article/details/53432572)<span>（0）</span>
*   [RobotFramework+SeleniumLibrary 安装及简单使用方法使用（未完成）](/xyh421/article/details/53333648)<span>（0）</span>
*   [关于Python的面试题 （github）](/xyh421/article/details/53172761)<span>（0）</span>
*   [Python 模块功能paramiko SSH 远程执行及远程下载(可以使用)](/xyh421/article/details/52289012)<span>（0）</span>
*   [AppiumLibrary 1.3.5英文api文档](/xyh421/article/details/52183287)<span>（0）</span>

</dt>

</dl>

<dl class="classify_list js_list">

<dt>

<div class="js_column_wrap"><span class="column">推荐文章</span></div>

*   [* CSDN日报20170628——《实习，背后的选择？》](http://blog.csdn.net/blogdevteam/article/details/73840694)
*   [* 【Java高级开发工程师】近一个月的面试总结](http://blog.csdn.net/pistolove/article/details/73610588)
*   [* 一个文科生的工程师之路](http://blog.csdn.net/reboot123/article/details/73266776)
*   [* JavaWeb 与 MySQL 人鬼情未了](http://blog.csdn.net/lqw_student/article/details/73646768)
*   [* PermissionsDispatcher、RxPermissions和easypermissions的使用和对比](http://blog.csdn.net/totond/article/details/73648103)
*   [* 每周荐书：架构、Scratch、增长黑客（评论送书）](http://blog.csdn.net/broadview2006/article/details/73550412)

</dt>

</dl>

<dl class="classify_list js_list">

<dt>

<div class="js_column_wrap"><span class="column">最新评论</span></div>

*   [如何用vncview查看xvfb里面的画面呢](/xyh421/article/details/73378124)

    [xyh421](/xyh421)<span>回复：</span>

    _@brucedai003:教授,能不要在这里撩我麽._

*   [如何用vncview查看xvfb里面的画面呢]()

    [brucedai003](/brucedai003)<span>回复：</span>

    _啊大牛啊_

*   [解决appiumlibrary中click a point 点击无效](/xyh421/article/details/64453518)

    [xyh421](/xyh421)<span>回复：</span>

    _@u010961363:我当时是这样解决的,你试一下吧.手机开启显示按钮,可以看到是否点击了.我之前..._

*   [解决appiumlibrary中click a point 点击无效]()

    [u010961363](/u010961363)<span>回复：</span>

    _我也有同样的问题，非要升级才能解决吗？_

*   [selenium2library 如何定位伪元素,比如::before](/xyh421/article/details/68067575)

    [xyh421](/xyh421)<span>回复：</span>

    _对的,一样的,调试一下就好了_

*   [selenium2library 如何定位伪元素,比如::before]()

    [qq_34055364](/qq_34055364)<span>回复：</span>

    _你好 你这个伪元素现在可以点击了是吗 driver.findElement(By.cssSele..._

</dt>

</dl>

</div>

</div>

</div>

</div>

<div id="skin_right_small" class="skin_right_small">

<div class="skin_r_small">

<div class="head_small">[![img](http://avatar.csdn.net/5/F/9/1_xyh421.jpg)](http://my.csdn.net/xyh421)</div>

*   [博客专栏](/xyh421/blog/column)
*   [文章分类](#)
*   [文章存档](#)
*   [阅读排行](#)
*   [评论排行](#)
*   [推荐文章](#)
*   [最新评论](#)

</div>

</div>

<style type="text/css">#popup_mask { position: absolute; width: 100%; height: 100%; background: #000; z-index: 9999; left: 0px; top: 0px; opacity: 0.3; filter: alpha(opacity=30); display: none; } .skin_list dl dd div ol { margin-left:15px; } .skin_list dl dd div ol li { display:list-item;list-style-type:decimal;margin-left:15px; }</style>

<div id="a52b5334d" style="width: 1px; height: 1px; display: none;"><script>document.getElementById("adJs52b5334").src = "http://ads.csdn.net/js/opt/52b5334.js?t=" + Math.random();</script></div>

<link rel="stylesheet" href="http://static.blog.csdn.net/css/blog_code.css">   <script type="text/javascript">var fromjs=$("#fromjs"); if(fromjs.length>0) { $("#fromjs .markdown_views pre").addClass("prettyprint"); prettyPrint(); $('pre.prettyprint code').each(function () { var lines = $(this).text().split('\n').length; var $numbering = $('<ul/>').addClass('pre-numbering').hide(); $(this).addClass('has-numbering').parent().append($numbering); for (i = 1; i <= lines; i++) { $numbering.append($('<li/>').text(i)); }; $numbering.fadeIn(1700); }); $('.pre-numbering li').css("color","#999"); } $(function(){ setTimeout(function(){ $(".math").each(function(index,value){$(this).find("span").last().css("color","#fff"); }) },500); });</script>
