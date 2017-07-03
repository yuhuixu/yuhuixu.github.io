首先,在server机器上,启动xvfb,这个我不想说,网上很多
然后到client端,启动vncviewer查看画面

    #ssh -L 5900:localhost:5900 root@172.16.10.26 'x11vnc -localhost -display :10'  
    #vncviewer localhost:5900  

说明:
ssh -L 端口号:localhost:端口号 服务器用户名@服务器地址 'x11vnc -localhost -display 服务器上的display设置(0:或者xxx:)'
这局命令比较重要,转发服务器到本地,然后本地就可以查看了
