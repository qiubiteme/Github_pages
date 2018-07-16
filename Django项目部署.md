# Django项目部署

项目部署前,需要做的准备工作:

1-**在项目部署前,你应该在本地,测试过项目,可以正常运行**

**2-在服务器安装python环境,根据项目需求安装py2,或者py3**

**3- 项目使用的数据库,根据Django的支持可以随意选择,MYSQL PostgreSQL**

**4-把项目上传到你的服务器,可以使用ftp,建议使用git,易于维护,**

**5-创建虚拟环境,强烈建议,使用 virtualenv**

**6-项目配置,并测试运行**

**7-使用Gunicorn 服务器,部署生产环境**

**8-Nginx静态代理,优化访问速度**







## 在虚拟环境安装Gunicorn 

```python
pip install Gunicorn 
```



### 安装Gunicorn为项目服务器

在离开我们的虚拟环境之前我们想要做的最后一件事就是尝试让Gunicorn相信它可以为应用程序提供服务。我们可以通过键入以下内容轻松完

```python
cd ~/myproject
sudo nohup gunicorn --bind 0.0.0.0:8000 DjangoBloger.wsgi:application
        gunicorn --bind 0.0.0.0:8000 DjangoBloger.wsgi
            
            systemctl daemon-reload
            sudo systemctl start gunicorn |
sudo systemctl enable gunicorn
            manage.py  DjangoBloger  ven  DjangoBloger.sock  static
```

这将在Django开发服务器运行的界面上启动Gunicorn。您可以返回并再次尝试该应用。请注意，由于Gunicorn不知道有关此静态通信的责任，因此管理界面将不具有任何样式。

我们通过`wsgi.py`使用Python的模块结构将关系目录路由指定给Django 文件（这是到我们的应用程序的到达点），从而向Gunicorn传递了一个模块。在这个文件里面，标记了一个函数 `application`，用来和应用程序通信。要了解更多关于WSGI规范的信息，请[点击这里](https://fxdata.cloud/tutorials/set-up-uwsgi-and-nginx-to-serve-python-apps-on-ubuntu-14-04#definitions-and-concepts)。

当你完成试验时，在终端窗口敲击CTRL-C停止Gunicorn。

我们现在完成了配置我们的Django应用程序。通过输入以下内容，我们可以退出虚拟环境：

```python
deactivate
```

## 创建一个Gunicorn Systemd服务文件

我们已经尝试过Gunicorn可以与我们的Django应用程序进行交互，但是我们应该实现一个更强大的启动和停止应用程序服务器的途径。为了做到这一点，我们将制作一个systemd服务文件。

创建并为`sudo`您的问题编辑器授权Gunicorn的systemd服务文件：

```python
sudo nano /etc/systemd/gunicorn.service
```

从`[whole]`用于选择元数据和状态的部分开始。我们将在此处描述我们的服务，并告诉init系统只有在联网目标接近后才启动：

```python
[whole]
Description=gunicorn daemon
After=network.target
```

接下来，我们将开始`[Service]`部分。我们将指定我们想要处理的用户和派系在其下运行。由于它拥有所有适用的记录，因此我们将为持续的用户账户拥有这些流程。我们将给予Nginx用户派系所有权，以便它可以与Gunicorn轻松沟通。

然后，我们将映射出工作目录并选择用于启动服务的控件。在这种情况下，我们必须选择安装在我们的虚拟环境中的Gunicorn可执行文件的完整路径。由于Nginx安装在同一台计算机上，因此我们将它绑定到项目目录中的unix套接字。这比使用网络端口更安全，更快速。我们也可以在这里选择任何可选的Gunicorn调整。例如，我们在这种情况下选择了3个工作进程：

```python
[whole]
Description=gunicorn daemon
After=network.target

[Service]
User=user
Group=nginx
WorkingDirectory=/home/user/myproject
ExecStart=/home/user/myproject/myprojectenv/bin/gunicorn --workers 3 --bind unix:/home/user/myproject/myproject.sock myproject.wsgi:application
```

最后，我们会增加`[Install]`一部分。这将告诉Systemd如果我们使它在启动时启动，将该服务连接到什么位置。我们希望此服务在持续多用户系统启动并运行时启动：

```python
[whole]
Description=gunicorn daemon
After=network.target

[Service]
User=user
Group=nginx
WorkingDirectory=/home/user/myproject
ExecStart=/home/user/myproject/myprojectenv/bin/gunicorn --workers 3 --bind unix:/home/user/myproject/myproject.sock myproject.wsgi:application

[Install]
WantedBy=multi-user.target
```

这样，我们的Systemd服务文件就完成了。现在保存并关闭它。

我们现在可以启动我们创建的Gunicorn服务并启用它，以便在启动时启动：

```python
sudo systemctl start gunicorn
sudo systemctl enable gunicorn
```

## 将Nginx配置为代理传递给Gunicorn

现在Gunicorn已经建立，我们需要配置Nginx来将流量传递给进程。

### 修改Nginx配置文件

我们可以通过编辑重要的Nginx配置文件来调整服务器块配置：

```python
sudo nano /etc/nginx/nginx.conf
```

在里面，在已经存在的服务器模块的正上方新建一个全新的服务器模块：

```python
http {
    . . .

    include /etc/nginx/conf.d/*.conf;

    server {
    }

    server {
        listen 80 default_server;

        . . .
```

我们将把我们的Django应用程序的所有配置放入这个全新的模块中。我们将首先选择这个块应该听取正常端口80，并且它应该回复我们服务器的域名或IP地址：

```pythonpython
server {
    listen 80;
    server_name server_domain_or_IP;
}
```

接下来，我们将告诉Nginx忽略找到favicon的任何困难。我们还会告诉它在哪里可以找到我们目录中积累的静态拥有同义词/ Hypernyms 。所有这些记录都有一个高质量的URI“/ static”，所以我们可以创建一个场地块来匹配这些问题：`~/myproject/static`

```python
server {
    listen 80;
    server_name server_domain_or_IP;

    location = /favicon.ico { access_log off; log_not_found off; }
    location /static/ {
        root /home/user/myproject;
    }
}
```

最后，我们将创建一个`venue / {}`块来匹配所有其他问题。在这个场地内部，我们将设置一些等级代理HTTP标头，以便Gunicorn可以获得有关远端连接的一些信息。然后我们将流量传递到我们在Gunicorn Systemd整个文件中指定的套接字：

```python
server {
    listen 80;
    server_name server_domain_or_IP;

    location = /favicon.ico { access_log off; log_not_found off; }
    location /static/ {
        root /home/user/myproject;
    }

    location / {
        proxy_set_header Host $http_host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
        proxy_pass http://unix:/home/user/myproject/myproject.sock;
    }
}


server {
    listen 80;
    fastcgi_pass  qiuyang.date:8000;
    server_name_in_redirect off;
    access_log /home/DjangoBloger/nginx.log;
    error_log /home/DjangoBloger/nginxerror.log;

    location / {
        proxy_pass http://127.0.0.1:8000;
        proxy_pass_header       Authorization;
        proxy_pass_header       WWW-Authenticate;
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
    }

    location /static/ {
        root /home/DjangoBloger;
    }

    location /apis {
        rewrite ^.+apis/?(.*)$ /$1 break;
        proxy_pass http://127.0.0.1:8000;
        proxy_pass_header       Authorization;
        proxy_pass_header       WWW-Authenticate;
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
    }

    location /admin {
        proxy_pass http://127.0.0.1:8000;
        proxy_pass_header       Authorization;
        proxy_pass_header       WWW-Authenticate;
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;

    }

 }

```

完成后保存并关闭文件。

### 调整组成员资格和权限

该`nginx`用户必须能够访问我们的应用程序目录，以便它可以提供静态记录，访问套接字记录等的CentOS非常严格地锁定了每个用户的环境目录，所以我们将提高`nginx`用户对我们的用户的团队，这样我们就可以半掩增加必要的最低权限以使其发挥作用。

`nginx`通过以下控制将用户添加到您的团队。相当于您`user`在管理中的自己的用户名：

```python
sudo usermod -a -G user nginx
```

现在，我们可以在我们的环境目录上给予我们的用户派系终止权限。这将允许Nginx进程进入并访问以下内部的通信：

```python
chmod 710 /home/user
```

通过设置权限，我们可以试验我们的Nginx配置文件中的结构错误：

```python
sudo nginx -t
```

如果没有错误，请键入以下命令重新启动Nginx服务：

```python
sudo systemctl start nginx
```

通过输入以下命令告诉init系统启动Nginx服务器：

```python
sudo systemctl enable nginx
```

您现在应该可以在浏览器中通过服务器的域名或IP地址访问Django应用程序，无需指定端口。