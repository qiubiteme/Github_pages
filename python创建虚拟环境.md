





# ConteOS7 中的 python创建虚拟环境

这个简单的笔记是在,ConteOS7 安装下的,前提条件是配置好python3环境,conteOS默认安装的是python2

## 通过pip安装virtualenv

```
pip install virtualenv
```

## 创建python3虚拟环境 

前提是配置好python3环境,

```
python3 -m venv (环境名称)
```
### 进入虚拟环境

```
source (环境名称)/bin/activate
```

### 查看python环境信息

```
 python -V
```

### 退出虚拟环境 到正常环境

```
deactivate
```

### 列举所有的环境。 

```
lsvirtualenv
```



#### 选择某个虚拟环境命令：

```
 workon (环境名称)
```



### 查看当前虚拟环境

```
 workon 
```



### 删除环境,只需要删除指定环境的目录即可

```
rm -r (环境的目录,文件夹)
```

### 停止服务器

```
kill gunicorn
```