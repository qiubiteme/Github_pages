# linux命令

# 文件相关操作

## 查看目录里的所有文件

```
dir
```

## 切换目录

### 指定目录

```
cd (指定目录)
```

### 切换到一级目录

```
cd ..  (上一级目录)
```

### 下载文件

```
wget (下载的文件地址)
```

### 解压文件



```
tar -xvf (包名)
```

## 删除文件夹【rm】

### 使用rm -rf命令递归删除所有文件

直接rm就可以了，不过要加两个参数-rf 即：

```
rm -rf (目录名字)
```

-r 就是向下递归，不管有多少级目录，一并删除

-f 就是直接强行删除，不作任何提示的意思

## 卸载软件

```
yum remove (软件名)
```

### 查看软件是否卸载完全

```
which (软件名)
```

## 查看linux系统版本命令 

```
 cat /proc/version 
```

开启端口

```
iptables -A INPUT -ptcp --dport  443 -j ACCEPT
```



# 进程状态 

linux上进程有5种状态: 

  1. 运行(正在运行或在运行队列中等待) 
  2. 中断(休眠中, 受阻, 在等待某个条件的形成或接受到信号)  
  3. 不可中断(收到信号不唤醒和不可运行, 进程必须等待直到有中断发生)  4. 僵死(进程已终止, 但进程描述符存在, 直到父进程调用wait4()系统调用后释放)  5. 停止(进程收到SIGSTOP, SIGSTP, SIGTIN, SIGTOU信号后停止运行运行)  

ps工具标识进程的5种状态码: 

 D 不可中断 uninterruptible sleep (usually IO) 

 R 运行 runnable (on run queue)  

S 中断 sleeping  

## 查看进程状态

```
ps -aux
```

## 列出类似树的程序显示(显示进程下有哪些子进程)

```
ps -axjf
```

## 找出与 cron 与 syslog 这两个服务有关的 PID 号码

```
`ps aux | egrep '(cron|syslog)'`
```

# 查看端口号

n表示不查询dns

t表示tcp协议

u表示udp协议

p表示查询占用的程序

l表示查询正在监听的程序

```
netstat -ntupl
```

## 查看那个进程占用了xxx端口

```
lsof -i:xxx
```



## 查看进程号为xxx的进程在哪里

```
ps -ef|grep xxx
ps -ef |grep  程序名
netstat -nltp |grep 端口号或服务名
```

