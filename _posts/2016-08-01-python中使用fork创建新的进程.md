---
layout: post
title: python中使用fork创建新的进程
category: Python
tags: [Python]
---

## fork知识入门
　　python的os module中有fork()函数用于生成子进程，生成的子进程是父进程的镜像，但是它们有各自的地址空间，子进程复制一份父进程内存给自己，两个进程之间的执行是相互独立的，其执行顺序可以是不确定的、随机的、不可预测的，这点与多线程的执行顺序相似。

```python
import os
import time

try:
    forkpid = os.fork()
    time.sleep(3)
    print type(forkpid)
except OSError:
    sys.exit('Unable to fork.')
```

输出如下

```shell
wayne@Z-Beatles:~/python$ python demo
<type 'int'>
<type 'int'>
```

3秒后可见fork的返回值是两个int型数值
    
## python运行时创建进程
当python脚本运行，系统会生成一个新的进程。先看下面代码：

```python
from time import sleep
sleep(30)
```

因为代码执行完后，进程就会被销毁，所以这里睡眠30秒，方便看到效果。再执行这个脚本文件：

```shell
python testfork.py &
```

加上&符号，可以让程序在后台运行，不会占用终端。输入ps -l命令查看进程，在电脑上输出如下：

```shell
F S   UID    PID   PPID  C PRI  NI ADDR SZ WCHAN  TTY          TIME CMD
0 S  1000   5896   4353  0  80   0 -  7387 wait   pts/19   00:00:00 bash
0 S  1000   5922   5896  0  80   0 -  7906 poll_s pts/19   00:00:00 python
4 R  1000   5923   5896  0  80   0 -  8996 -      pts/19   00:00:00 ps
```

其中第二条记录就是刚才运行的python脚本了。

## 使用fork来创建一个新进程

使用fork创建一个新进程成功后，新进程会是原进程的子进程，原进程称为父进程。如果发生错误，则会抛出OSError异常。

```python
from time import sleep
import os
 
try:
    pid = os.fork()
except OSError, e:
    pass
 
sleep(30)
```

运行代码后查看进程，输出如下：

```shell
F S   UID    PID   PPID  C PRI  NI ADDR SZ WCHAN  TTY          TIME CMD
0 S  1000   5896   4353  0  80   0 -  7387 wait   pts/19   00:00:00 bash
0 S  1000   5956   5896  0  80   0 -  7906 poll_s pts/19   00:00:00 python
1 S  1000   5957   5956  0  80   0 -  7906 poll_s pts/19   00:00:00 python
4 R  1000   5958   5896  0  80   0 -  8996 -      pts/19   00:00:00 ps
```

可以看出第二条python进程就是第一条的子进程。

## fork进程后的程序流程

使用fork创建子进程后，子进程会复制父进程的数据信息，而后程序就分两个进程继续运行后面的程序，这也是fork（分叉）名字的含义了。在子进程内，这个方法会返回0；在父进程内，这个方法会返回子进程的编号PID。可以使用PID来区分两个进程：

```python
import os
from time import sleep

source = 10
 
try:
    pid = os.fork()
 
    if pid == 0:  #子进程
        source = source - 1
        sleep(4)
        print "this is child process.source is %d" %source
    else: 
        print "this is parent process.source is %d" %source
except OSError, e:
    pass
```

上面代码中，在子进程创建前，声明了一个变量source，然后在子进程中自减1，最后打印出source的值，显然父进程打印出来的值应该为10，4秒后子进程打印出来的值应该为9。

## 守护进程

既然子进程是父进程创建的，那么父进程退出之后，子进程会怎么样呢？此时，子进程会被PID为1的进程接管，就是init进程了。这样子进程就不会受终端退出影响了，使用这个特性就可以创建在后台执行的程序，俗称守护进程（daemon）。

### mark-守护进程

* [linux python守护进程编写](http://blog.csdn.net/mr_jj_lian/article/details/7252222)
* [Python实例浅谈之五Python守护进程和脚本单例运行](http://blog.csdn.net/taiyang1987912/article/details/44850999)
* [Linux守护进程设计规范及python实现](http://blog.csdn.net/dysj4099/article/details/18219411)

## Tips

* fork()函数用来创建新的进程
* os.fork() 会有两次返回值，分别是父进程和子进程的返回值
* 在父进程中，fork返回的值是子进程的PID；
* 子进程中，这个返回值为0
* 子进程会复制父进程的上下文
* 父子进程并不能确定执行顺序
* os.getpid()返回当前进程的ID，os.getppid()返回当前进程的父进程的ID
* os.fork() 之后，子进程一定要使用 exit() 或者 os._exit() 来退出子进程环境，建议使用 os._exit()
* 可以使用os.waitpid(pid,0)来使父进程等待子进程执行完再执行父进程


## waitpid()的使用

```python
import os
import sys
import time 

try :
    forkPID1 = os.fork()
except OSError : # 如果操作系统不能创建进程，osfork()将会发出一个OSError异常
    sys.exit('Unable to create first child.')

if forkPID1 != 0 :
    try :
        forkPID2 = os.fork() 
    except OSError :
        sys.exit('Unable to create first child.')

    if forkPID2 > 0 :
        print 'Parent waiting for child precesses ...\n' + \
            '\t tpid : %d , forkPID1 : %d , forkPID2 : %d' \
            % ( os.getpid() , forkPID1 , forkPID2)

        try :
            child2 = os.waitpid (forkPID2 , 0)[0]
        except OSError :
            sys.exit("No child process with pid %d." %(forkPID2) )

        print 'Parent Child %d finished.' % child2

    elif forkPID2 == 0 :
        print 'Chile2 sleeping fot 4 seconds ....\n' + \
            '\tpid : %d , forkPID1: %d , forkPID2: %d' \
            % (os.getpid() , forkPID1 , forkPID2 )
        time.sleep(4) #规定进程保持的休眠时间 ， 以秒为单位

elif forkPID1 == 0 :
    print 'Child1 sleeping for 2 seconds ....\n' + \
        '\tpid : %d , forkPID1: %d' \
        % (os.getpid() , forkPID1)
    time.sleep(2)
```
* 这里的'\'为‘反斜杠’or‘续航符’

**严格地讲, 在小括号, 方括号或大括号中的表达式 (如 定义一个 dictionary) 可以用或者不用续行符 (“\”) 分割成多行。甚至在不是必需的时候,也可以使用续行符,那可以让代码读起来更容易。使用续行符只是风格的问题。**

### 3个示范输出

```shell
Parent waiting for child precesses ...
     tpid : 2468 , forkPID1 : 2469 , forkPID2 : 2470
Child1 sleeping for 2 seconds ....
    pid : 2469 , forkPID1: 0
Chile2 sleeping fot 4 seconds ....
    pid : 2470 , forkPID1: 2469 , forkPID2: 0
Parent Child 2470 finished.

Parent waiting for child precesses ...
     tpid : 2465 , forkPID1 : 2466 , forkPID2 : 2467
Child1 sleeping for 2 seconds ....
Chile2 sleeping fot 4 seconds ....
    pid : 2466 , forkPID1: 0
    pid : 2467 , forkPID1: 2466 , forkPID2: 0
Parent Child 2467 finished.

Parent waiting for child precesses ...
     tpid : 2634 , forkPID1 : 2635 , forkPID2 : 2636
Child1 sleeping for 2 seconds ....
    pid : 2635 , forkPID1: 0
Chile2 sleeping fot 4 seconds ....
    pid : 2636 , forkPID1: 2635 , forkPID2: 0
Parent Child 2636 finished.
```


