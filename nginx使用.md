# nginx使用

## **nginx查看版本信息**

```
/usr/sbin/nginx -v
```

## 安装nginx

### Ubuntu下安装nginx 

```
apt-get install nginx 
```



### CentOS 下安装nginx

**使用yum安装nginx需要包括Nginx的库，安装Nginx的库** 

```
rpm -ivh http://nginx.org/packages/centos/7/noarch/RPMS/nginx-release-centos-7-0.el7.ngx.noarch.rpm 
```

#### 使用命令安装nginx 



```
yum install nginx 
```

### 启动Nginx 

```
service nginx start 
```

**或者**

```
systemctl start nginx.service 
```

### 重启nginx 

```
service nginx restart 
```
  ### 重新载入配置文件
```
nginx -s reload          
```


```
sudo ln -s firekylin/nginx.conf /etc/nginx/www.qiuyang.date.conf
```

### 停止 Nginx

```
nginx -s stop              
```



```
sudo ln -s /etc/nginx/nginx.conf
```





