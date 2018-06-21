

# DjangoStudyNote 

笔记学习从Django的2,0 开始学习:

主要分为,

​	1-基本命令,

​	2-应用基本配置,数据库,

​	3-视图

​	4-url网址路由

​	5-模型

​	6-模板

​	7-管理界面,

​	8-表单

## 基本命令

### **查看Django的版本**

```
python -m django --version
```

### **创建项目**

```
django-admin startproject bloger
```



## 更新pip



```
python -m pip install --upgrade pip
```



### 生成依赖

```
pip freeze > requirements.txt
```

### 安装依赖

```
pip install -r requirements.txt
```

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

### 生成应用模型数据库表结构

```
python manage.py makemigrations
```

生成应用指定模型文件映射的数据库表结构

```
python manage.py makemigrations front
```

### 将模型映射数据结构,迁移到数据库

```
python manage.py migrate
```

**将指定应用的模型映射数据结构,迁移到数据库**

多次修改,生成的数据结构不同,对应文件不同

```
python manage.py sqlmigrate front 0001
```

## 创建博客的前端应用模块

```
 python manage.py startapp front
```

### 配置应用

**在front应用中的view.py中添加视图响应函数**

```
from django.http import HttpResponse
from django.shortcuts import render


# Create your views here.
def index(request):
    return HttpResponse("hello world")
```

注意导包问题

**在 fron应用t中创建(urls.py) 网址路由并添加如下代码**

```
from django.urls import path

from front import views

urlpatterns = [
    path('', views.index, name='index'),
]
```

**把front的应用路由添加到bloger项目的urls.py中,代码如下:**

```
from django.contrib import admin
from django.urls import path, include

urlpatterns = [
    path('',include('front.urls')),
    path('admin/', admin.site.urls),

]
```

访问http://127.0.0.1:8000/查看效果

#### **更改时区**为中国  

 在bloger/settings.py中找到  **TIME_ZONE**

```
TIME_ZONE = 'Asia/Shanghai'
```

#### 更改默认语言为中文

 在bloger/settings.py中找到  **LANGUAGE_CODE**

```
# 中文支持
LANGUAGE_CODE = 'zh-hans'
```

### 数据库配置

暂时使用默认的**SQLite数据库**

#### 数据库中创建表 

**` 创建更改的模型文件`映射**

```
python manage.py makemigrations
```

**将生成的py文件应用到数据库**

```
python manage.py migrate
```

#### 创建模型

**Django字段模型详解**

https://www.cnblogs.com/lhj588/archive/2012/05/24/2516040.html

**django 关系类型字段**

http://www.liujiangblog.com/course/django/96

**创建模型主要分两种**

##### 1-根据模型生成数据库表

根据文档,编辑,模型结构

##### 2-根据数据库表生成模型

主要有两个命令

**这个命令直接在命令行,打印出模型**

```
python manage.py inspectdb 
```

**在当前目录创建一个,models.py文件** 

```
python manage.py inspectdb > models.py 
```

**Django 数据库表生成的 Models 的建议**

[集成已有的数据库和应用](https://link.jianshu.com/?t=http://djangobook.py3k.cn/2.0/chapter18/)

#### 配置创建的应用模块

##### 配置模块

在 **bloger\settings.py** 的 **INSTALLED_APPS**添加

```
INSTALLED_APPS = [
    # 添加创建的应用模块
    'front.apps.FrontConfig',

    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
]
```

在模型中添加 ,便于在后台查看数据

```
    def __str__(self):
        return self.name
```



## Django 管理页面

### 创建一个管理员账号[¶](https://docs.djangoproject.com/zh-hans/2.0/intro/tutorial02/#creating-an-admin-user)

首先，我们得创建一个能登录管理页面的用户。请运行下面的命令：

```
python manage.py createsuperuser
```

键入你想要使用的用户名，然后按下回车键：

```
Username: admin
```

然后提示你输入想要使用的邮件地址：

```
Email address: admin@example.com
```

最后一步是输入密码。你会被要求输入两次密码，第二次的目的是为了确认第一次输入的确实是你想要的密码。

```
Password: **********
Password (again): *********
Superuser created successfully.
```

### 启动开发服务器[¶](https://docs.djangoproject.com/zh-hans/2.0/intro/tutorial02/#start-the-development-server)

Django 的管理界面默认就是启用的。让我们启动开发服务器，看看它到底是什么样的。

如果开发服务器未启动，用以下命令启动它：

```
 python manage.py runserver
```

现在，打开浏览器，转到你本地域名的 "/admin/" 目录， -- 比如 "<http://127.0.0.1:8000/admin/>" 。你应该会看见管理员登录界面：

因为 [翻译](https://docs.djangoproject.com/zh-hans/2.0/topics/i18n/translation/) 功能默认是开着的，所以登录界面可能会使用你的语言，取决于你浏览器的设置和 Django 是否拥有你语言的翻译。

### **进入管理站点页面**[¶](https://docs.djangoproject.com/zh-hans/2.0/intro/tutorial02/#enter-the-admin-site)

现在，试着使用你在上一步中创建的超级用户来登录。然后你将会看到 Django 管理页面的索引页：

![](https://docs.djangoproject.com/zh-hans/2.0/_images/admin02.png' %})

你将会看到几种可编辑的内容：组和用户。它们是由 [`django.contrib.auth`](https://docs.djangoproject.com/zh-hans/2.0/topics/auth/#module-django.contrib.auth) 提供的，这是 Django 开发的认证框架。

### 向管理页面中加入博客前端应用[¶](https://docs.djangoproject.com/zh-hans/2.0/intro/tutorial02/#make-the-poll-app-modifiable-in-the-admin)

只需要做一件事：我们得告诉管理页面，问题 `front应用的模型` 对象需要被管理。打开 front/admin.py` 文件，把它编辑成下面这样：**记住导包**

front/admin.py

```
from django.contrib import admin

# Register your models here.
from front.models import Options, Users, Category, Posts, Comment

admin.site.register(Options)
admin.site.register(Users)
admin.site.register(Category)
admin.site.register(Posts)
admin.site.register(Comment)
```

### 体验便捷的管理功能[¶](https://docs.djangoproject.com/zh-hans/2.0/intro/tutorial02/#explore-the-free-admin-functionality)

现在我们向管理页面注册用户,添加分类,文章,站点,评论。Django 知道它应该被显示哪个页面：



### **快捷函数： render()**

静态文件,生产环境在,每个应用模块创建static文件,后面跟应用文件

**例如  **

uadmin\static\uadmin 

这种结构官方推荐,

静态文件要在django模板中加载需要

```
 在head标签前,添加
 {% load static %}
 在需要引入的地方
  <link rel="stylesheet" href="{% static 'uadmin/assets/css/admin.css' %}">
  关键代码 {%static '在应用static中的路径'%}
  {% static 'uadmin/assets/css/admin.css' %

```







