

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
