

## 		pyChrome创建Django项目

**教程使用 windows10 ,python3.6.5 Django2.0.6** 其他版本仅供参考

首先你要配置好,开发环境,python2 python3,和对应的Django版本,

Django版本支持,可以去官网查看.

开发一般需要一个编辑器,俗称 IDE 推荐使用  **pycharm** **VisualStudio**

环境搭建好了就开撸

**pycharm** 新版本,可以直接创建,Dajngo项目,

Project Interpreter: New Virtualenv environment

### pycharm**创建项目**

为了简单我们直接使用**pycharm** 创建项目

**在Pycharmde 初始页面找到, Create New Project**

![](img/django-create-project1.png)

### **点击进入创建项目,基本配置选项:**

![](img/django-create-project2.png)

**Location: ** **G:\DjangoTest**

项目采访的目录和名字 (根据需要,自由选择)

演示使用的项目名字和目录,G盘,名字DjangoTest

**Project Interpreter: New Virtualenv environment** 选项

默认是选择,创建一个新的虚拟环境,(使用默认就好)

如果此选项没有列出python的环境,需要手动配置python环境

**点击后面的**     **. . .**   找到你的python安装目录添加上去

选择完毕后 **找到右下角,的 Create** 创建项目

### pychrom创建项目结构

点击左侧的 **Project** 就会显示项目结构

在底部好到, **Terminal** 点击展开,后续我们使用,命令行,就在这个,窗口

![](img/django-create-project3.png)

现在项目创建好了,就可以直接运行了,

在 **Terminal** 里面运行开发服务器

### **运行开发服务器**

```
python manage.py runserver
```

运行后查看效果http://127.0.0.1:8000/

### **在指定端口运行**

```
python manage.py runserver 8080
```

运行后查看效果http://127.0.0.1:8000/

用于开发的服务器在需要的情况下会对每一次的访问请求重新载入一遍 Python 代码。所以你不需要为了让修改的代码生效而频繁的重新启动服务器。然而，一些动作，比**如添加新文件**，将不会触发自动重新加载，这时你得自己手动重启服务器。 

