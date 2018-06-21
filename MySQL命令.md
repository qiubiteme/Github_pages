

# MySQL命令



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



##  重启MySQL 

```
service mysqld restart  
```



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
update user set authentication_string=password('wert123456') where user='root' ; 
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
SET PASSWORD = PASSWORD('wert23456');
```





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