## 配置mysql数据库默认字符集

对于使用默认MySQL字符集和排序规则（`latin1`， `latin1_swedish_ci`）存储数据的应用程序，不需要特殊配置。如果应用程序需要使用不同的字符集或排序规则进行数据存储，则可以通过多种方式配置字符集信息：

- 指定每个数据库的字符设置 例如，使用一个数据库的应用程序可能使用默认值 `latin1`，而使用另一个数据库的应用程序可能会使用`sjis`。
- 在服务器启动时指定字符设置。这会导致服务器对所有未进行其他安排的应用程序使用给定的设置。
- 如果从源构建MySQL，请在配置时指定字符设置。这会导致服务器将给定的设置用作所有应用程序的默认设置，而无需在服务器启动时指定它们。

当不同的应用程序需要不同的字符设置时，每数据库技术提供了很大的灵活性。如果大多数或所有应用程序使用相同的字符集，则在服务器启动或配置时指定字符设置可能是最方便的。

对于每数据库或服务器启动技术，设置控制数据存储的字符集。应用程序还必须告知服务器使用哪个字符集进行客户端/服务器通信，如以下说明中所述。

此处显示的示例假定在特定上下文中使用`utf8` 字符集和`utf8_general_ci`排序规则作为`latin1`和 的默认值的替代`latin1_swedish_ci`。

#### 源码安装时配置

**在MySQL配置时指定字符设置。**  要从源配置和构建MySQL，要选择字符集和排序规则，请使用[`DEFAULT_CHARSET`](https://dev.mysql.com/doc/refman/5.7/en/source-configuration-options.html#option_cmake_default_charset)和 **CMake**选项： [`DEFAULT_COLLATION`](https://dev.mysql.com/doc/refman/5.7/en/source-configuration-options.html#option_cmake_default_collation) 

```
cmake . -DDEFAULT_CHARSET=utf8 \
  -DDEFAULT_COLLATION=utf8_general_ci

```

#### 在服务器启动时指定字符设置

**在服务器启动时指定字符设置。**  要在服务器启动时选择字符集和排序规则，请使用 [`--character-set-server`](https://dev.mysql.com/doc/refman/5.7/en/server-options.html#option_mysqld_character-set-server)和[`--collation-server`](https://dev.mysql.com/doc/refman/5.7/en/server-options.html#option_mysqld_collation-server)选项。例如，要指定选项文件中的选项，请包括以下行：

```
[mysqld]
character-set-server=utf8
collation-server=utf8_general_ci
```

## 定每个数据库的字符设置

**指定每个数据库的字符设置**  要创建数据库，使其表使用给定的默认字符集和排序规则进行数据存储，请使用如下[`CREATE DATABASE`](https://dev.mysql.com/doc/refman/5.7/en/create-database.html)语句：

```
CREATE DATABASE mydb
  CHARACTER SET utf8
  COLLATE utf8_general_ci;
```