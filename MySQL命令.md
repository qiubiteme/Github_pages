



# MySQL命令

### mysql区域语言编码设置

用于解决乱码问题,和

#### 查看当前区域语言编码

```
SELECT @@lc_time_names;
```

#### 查看mysql编码格式

```
SHOW VARIABLES LIKE 'char%';
```

### 数据库编码格式错误的问题解决 三种方法




## 检测系统是否安装 MySQL 

```
rpm -qa | grep mysql
```

## yun 安装mysql57

**1-下载rpm源**

```
wget https://dev.mysql.com/get/mysql57-community-release-el7-9.noarch.rpm
```

**2- 加载rpm源到本地**

```

rpm -ivh mysql57-community-release-el7-9.noarch.rpm

```

**3- 安装mysql服务**

```
yum install mysql-server
```

## 启动 MySQL： 

```
systemctl start mysqld
```

## 查看 MySQL 运行状态： 

```
systemctl status mysqld
```

## 查看mysql版本和系统信息

```
mysqladmin --version
```

## 登录mysql

```
mysql -u root -p;
Enter password:*******
```

设置密码

```
SET PASSWORD FOR 'root'@'localhost' = 'root';
```



##  重启MySQL 

```
service mysqld restart  
```



| auth_group                 |
| auth_group_permissions     |
| auth_permission            |
| auth_user                  |
| auth_user_groups           |
| auth_user_user_permissions |
| comment_comment            |
| django_admin_log           |
| django_content_type        |
| django_migrations          |
| django_session             |
| front_category             |
| front_options              |
| front_posts                |
| front_tag                  |
| front_users                |
+----------------------------+

ALTER TABLE auth_group_permissions     CONVERT TO CHARACTER SET utf8mb4; 

```
CREATE DATABASE bloger CHARACTER SET utf8;
```

show variables like 'char%';

## 重置密码 

**1- 编辑MySQL配置文件/etc/my.cnf** 

```
在最后添加一行
skip-grant-tables   
```

2. **重启MySQL** 

   ```
   service mysqld restart  
   ```

   3. **root用户登录MySQL，提示密码,直接回车免密登录** 

      

```
mysql -uroot -p  
```

4. 选择数据库

   ```
   use mysql;
   ```

5. **修改root密码，并刷新权限** 

```
update user set authentication_string=password('root') where user='root' ; 
```

**执行**
```
flush privileges; 
```

****5-退出MySQL**

```
quit;
```

**6-，编辑MySQL配置文件/etc/my.cnf** 

```
在最后一行,删除,或者注释
skip-grant-tables   
```



**7重启MySQL** 

```
service mysqld restart  
```

然后就可以正常使用密码登录了

8、当你登陆mysql之后你会发现，执行命令时会出现

```
ERROR 1820 (HY000): You must reset your password using ALTER USER statement；1
```

这是提示你需要修改密码

当你执行了

```
SET PASSWORD = PASSWORD('wert23456');
```

## 如果执行成功后面的就不要看了，纯属浪费时间！

如果出现：

```
ERROR 1819 (HY000): Your password does not satisfy the current policy requirements1
```

你需要执行两个参数来把mysql默认的密码强度的取消了才行

```
set global validate_password_policy=0; set global validate_password_mixed_case_count=2;1
```

这时你再执行

```
SET PASSWORD = PASSWORD('wroot');
```



SET lc_time_names = 'zh_CN '; 

## Centos7 修改mysql默认字符

在MySQL配置文件下添加

```
[mysqld] 

    character-set-server=utf8 

    init_connect = 'SET NAMES utf8' 

    collation-server=utf8_general_ci 

[client]

     default-character-set=utf8 

```

## 重启MySQL

```
service mysqld restart  
```

**有可能你进行了上述设置，但还是遇到如下错误** 

```
ERROR 1366 (HY000): Incorrect string value1
```

**有可能是你的数据库字符集已经更改了，但是表的默认字符集还没更改，这时候可以直接使用如下命令直接更改表的默认字符集就可以了。** 


```
alter table testtb convert to charset utf8;
```

## drop 命令删除数据库

**drop 命令格式：**

```
drop database <数据库名>;
```
# ubuntu下mysql的使用

### 安装mysql 服务

```
sudo apt-get install mysql-server
```

#### 安装mysql客户端

```
sudo apt install mysql-client
```

#### 安装mysql libmysqlclient

```
sudo apt install libmysqlclient-dev
```

　　**安装成功后可以通过下面的命令测试是否安装成功：**

```
sudo netstat -tap | grep mysql
```

**如下输出安装成功**

```

tcp        0      0 localhost.localdo:mysql *:*                     LISTEN      9020/mysqld

```

#### 登录mysql 

```
mysql -u root -p
```

### 配置mysql

**在 /etc/mysql/mysql.conf.d  下编辑 mysqld.cnf** 



```
在[client]下配置：
default-character-set=utf8

在[mysqld]下配置：
default-character-set=utf8
init_connect=’SET NAMES utf8′
 
注意：新版MySQL(如：5.5）或MariaDB等，mysqld启动时可能会遇到“[ERROR] /usr/libexec/mysqld: unknown variable ‘default_character_set=utf8’”的错误；就应该在[mysqld]中用 character_set_server=utf8 替换掉 default_character_set=utf8 。
 
2.如果还没有解决，那么就得删掉原来建的DB，重新建并制定字符集为utf8，如：CREATE DATABASE jay_db DEFAULT CHARACTER SET utf8 COLLATE utf8_general_ci;

```





## ubuntu卸载mysql 

```
sudo apt-get remove mysql-common
```

##### 首先删除

```
sudo apt-get remove mysql-* 
```

##### 然后清理残留的数据

```
 dpkg -l |grep ^rc|awk '{print $2}' |sudo xargs dpkg -P
```

 它会跳出一个对话框，你选择yes就好了
 然后安装mysql
 `sudo apt-get install mysql-client mysql-server`

安装过程中会提示,输入两次密码

记住你的密码就好