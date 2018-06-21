

# python生成依赖文件

## **生成依赖文件**

使用如下命令自动生成，但可能会生成一些无关项目的依赖

```
pip freeze > requirements.txt
```

命令会在工程根目录下创建一个**requirements.txt**,在其中以如下格式输入依赖库

```
Django==2.0.6
pytz==2018.4
```

> 以上命令需要进入工程目录

## **使用依赖文件**

- 运行项目之前进入工程目录，在其中执行

```
pip install -r requirements.txt
```

以上代码会帮你自动安装所需所有依赖，

#	pip命令

## Commands:  命令

| **Commands:  命令**       | **描述:**      |
| :----------------------------- | ------------------ |
| **pip install                         (Install packages)** | **安装指定包**                      |
| **pip download                   ( Download packages)**  | **下载指定的包(后缀格式:none-any.whl)** |
| **pip uninstall                  ( Uninstall packages.)** | 卸载包 |
| **pip freeze           (Output installed packages in requirements format.)** | 以需求格式输出已安装的包。 |
| **pip list                            (List installed packages.)** | 安装包列表。 |
| pip show               (Show information about installed packages.) | 显示指定已安装包的信息。 |
| **pip check**             (Verify installed packages have compatible dependencies.) | 验证已安装的包是否具有兼容的依赖项 |
| **pip search**              (Search PyPI for packages.) | PyPI搜索包。 |
| **pip wheel**                 (Build wheels from your requirements.) | 根据您的需求构建轮子。 |
| **pip hash**                      ( Compute hashes of package archives.) | 计算包归档的散列。 |
| **pip completion**       (A helper command used for command completion.) | 用于命令完成的辅助命令。 |
| **pip help**                     (Show help for commands.) | 显示命令的帮助。 |
## General Options: 通用选项

|**General Options: 通用选项**		| **描述** |
| :----------------------------- | ------------------ |
|  -h, --help        |          Show help.  显示帮助。          |
| --isolated           | Run pip in an isolated mode, ignoring   environment variables and user configuration.      以隔离模式运行pip，忽略环境变量和用户配置。 |
| -v, --verbose      | Give more output. Option is additive, and can be       used up to 3 times.         提供更多的产出。选择是加性的，最多可以用三次。 |
| -V, --version      | Show version and exit.        显示版本并退出。      |
|-q, --quiet       | Give less output. Option is additive, and can be  used up to 3 times (corresponding to WARNING,   ERROR, and CRITICAL logging levels).  给更少的输出。选项是附加的，最多可使用3次(对应于警告、错误和临界日志级别)。 |
| --log <path>        |   Path to a verbose appending log.      详细附加日志的路径。   |
| --proxy <proxy>     | Specify a proxy in the form     [user:passwd@]proxy.server:port.     在表单[user:passwd@]proxy.server:port中指定代理。 |
| --retries <retries>   | Maximum number of retries each connection should       attempt (default 5 times).        每个连接尝试的最大重试次数(默认为5次)。   |
|  --timeout <sec>   | Set the socket timeout (default 15 seconds).    设置套接字超时(默认为15秒)。    |
|  --exists-action <action>      | Default action when a path already exists: (s)witch, (i)gnore, (w)ipe, (b)ackup, (a)bort.  当路径已经存在时的默认动作:(s)witch (i)gnore， (w)ipe， (b)ackup， (a)bort。 |
| --trusted-host <hostname>               | Mark this host as trusted, even though it does  not have valid or any HTTPS. 将此主机标记为受信任的，即使它没有有效的或任何HTTPS。     |
|  --cert <path>       |        Path to alternate CA bundle.  替换CA包的路径。        |
|  --client-cert <path>   | Path to SSL client certificate, a single file    containing the private key and the certificate         in PEM format.  SSL客户端证书的路径，一个包含私钥和PEM格式证书的文件。 |
|  --cache-dir <dir>    |    Store the cache data in <dir>.  将缓存数据存储在中。 |
|  --no-cache-dir       |       Disable the cache.  禁用缓存。     |
|  --disable-pip-version-check       |       Don't periodically check PyPI to determine whether a new version of pip is available for    download. Implied with --no-index.   不要定期检查PyPI，以确定是否可以下载新的pip版本。——没有索引的暗示。       |