[TOC]

# Web API

## Web API介绍

### API的概念

API（Application Programming Interface,应用程序编程接口）是一些预先定义的函数，目的是提供应用程序与开发人员基于某软件或硬件得以访问一组例程的能力，而又无需访问源码，或理解内部工作机制的细节。

- 任何开发语言都有自己的API
- API的特征输入和输出(I/O)
- API的使用方法(console.log())

### Web API的概念

浏览器提供的一套操作浏览器功能和页面元素的API(BOM和DOM)

此处的Web API特指浏览器提供的API(一组方法)，Web API在后面的课程中有其它含义

### 掌握常见的浏览器提供的API的调用方式

[MDN-Web API](https://developer.mozilla.org/zh-CN/docs/Web/API)

### JavaScript的组成

![1496912475691](/media/1496912475691.png)

#### ECMAScript - JavaScript的核心

定义了javascript的语法规范

JavaScript的核心，描述了语言的基本语法和数据类型，ECMAScript是一套标准，定义了一种语言的标准与具体实现无关

#### BOM - 浏览器对象模型

一套操作浏览器功能的API

通过BOM可以操作浏览器窗口，比如：弹出框、控制浏览器跳转、获取分辨率等

#### DOM - 文档对象模型

一套操作页面元素的API

DOM可以把HTML看做是文档树，通过DOM提供的API可以对树上的节点进行操作

## BOM

### BOM的概念

BOM(Browser Object Model) 是指浏览器对象模型，浏览器对象模型提供了独立于内容的、可以与浏览器窗口进行互动的对象结构。BOM由多个对象组成，其中代表浏览器窗口的Window对象是BOM的顶层对象，其他对象都是该对象的子对象。

我们在浏览器中的一些操作都可以使用BOM的方式进行编程处理，

比如：刷新浏览器、后退、前进、在浏览器中输入URL等

### BOM的顶级对象window

window是浏览器的顶级对象，当调用window下的属性和方法时，可以省略window
注意：window下一个特殊的属性 window.name

### 对话框

**警告框**

警告框经常用于确保用户可以得到某些信息。

当警告框出现后，用户需要点击确定按钮才能继续进行操作。

**语法：**

```
alert("文本")
```

**确认框**

确认框用于使用户可以验证或者接受某些信息。

当确认框出现后，用户需要点击确定或者取消按钮才能继续进行操作。

如果用户点击确认，那么返回值为 true。如果用户点击取消，那么返回值为 false。

**语法：**

```
confirm("文本")
```

**提示框**

提示框经常用于提示用户在进入页面前输入某个值。

当提示框出现后，用户需要输入某个值，然后点击确认或取消按钮才能继续操纵。

如果用户点击确认，那么返回值为输入的值。如果用户点击取消，那么返回值为 null。

**语法：**

```
prompt("文本","默认值")
```

### 页面加载事件

- **onload** **当页面加载完毕执行**

```javascript
window.onload = function () {
  // 当页面加载完成执行
  // 当页面完全加载所有内容（包括图像、脚本文件、CSS 文件等）执行
}
```

- **onunload** **当用户退出页面执行**

```javascript
window.onunload = function () {
  // 当用户退出页面时执行
}
```

### 定时器

**setTimeout()和clearTimeout() 只执行一次**

在指定的毫秒数到达之后执行指定的函数，只执行一次

```javascript
<input type="button" value="停止" id="btn"/>
<script>
// 创建一个定时器，1000毫秒后执行，返回定时器的标示
var timerId = setTimeout(function () {
  console.log('Hello World');
}, 1000);

// 取消定时器的执行
clearTimeout(timerId);
</script>
```

**setInterval()和clearInterval()**

定时调用的函数，可以按照给定的时间(单位毫秒)周期调用函数

```javascript
<input type="button" value="停止" id="btn"/>
<script>
    // 创建一个定时器，每隔1秒调用一次
var timerId = setInterval(function () {
  var date = new Date();
  console.log(date.toLocaleTimeString());
}, 1000);

// 取消定时器的执行
clearInterval(timerId);
</script>
```

### location对象

location对象是window对象下的一个属性，写的时候可以省略window对象

location可以获取或者设置浏览器地址栏的URL

**URL**

统一资源定位符 (Uniform Resource Locator, URL)

- URL的组成

```
scheme://host:port/path?query#fragment
scheme:通信协议
	常用的http,ftp,maito等
host:主机
	服务器(计算机)域名系统 (DNS) 主机名或 IP 地址。
port:端口号
	整数，可选，省略时使用方案的默认端口，如http的默认端口为80。
path:路径
	由零或多个'/'符号隔开的字符串，一般用来表示主机上的一个目录或文件地址。
query:查询
	可选，用于给动态网页传递参数，可有多个参数，用'&'符号隔开，每个参数的名和值用'='符号隔开。例如：name=zs
fragment:信息片断
	字符串，锚点.
```

**location有哪些成员？**

Location 对象包含有关当前 URL 的信息。

Location 对象是 Window 对象的一个部分，可通过 window.location 属性来访问。

**例子**

[把用户带到一个新的地址](http://www.w3school.com.cn/tiy/t.asp?f=hdom_location)

**Location 对象属性**

| 属性                                                         | 描述                                          |
| ------------------------------------------------------------ | --------------------------------------------- |
| [hash](http://www.w3school.com.cn/jsref/prop_loc_hash.asp)   | 设置或返回从井号 (#) 开始的 URL（锚）。       |
| [host](http://www.w3school.com.cn/jsref/prop_loc_host.asp)   | 设置或返回主机名和当前 URL 的端口号。         |
| [hostname](http://www.w3school.com.cn/jsref/prop_loc_hostname.asp) | 设置或返回当前 URL 的主机名。                 |
| [href](http://www.w3school.com.cn/jsref/prop_loc_href.asp)   | 设置或返回完整的 URL。                        |
| [pathname](http://www.w3school.com.cn/jsref/prop_loc_pathname.asp) | 设置或返回当前 URL 的路径部分。               |
| [port](http://www.w3school.com.cn/jsref/prop_loc_port.asp)   | 设置或返回当前 URL 的端口号。                 |
| [protocol](http://www.w3school.com.cn/jsref/prop_loc_protocol.asp) | 设置或返回当前 URL 的协议。                   |
| [search](http://www.w3school.com.cn/jsref/prop_loc_search.asp) | 设置或返回从问号 (?) 开始的 URL（查询部分）。 |

**Location 对象方法**

| 属性                                                         | 描述                     |
| ------------------------------------------------------------ | ------------------------ |
| [assign()](http://www.w3school.com.cn/jsref/met_loc_assign.asp) | 加载新的文档。           |
| [reload()](http://www.w3school.com.cn/jsref/met_loc_reload.asp) | 重新加载当前文档。       |
| [replace()](http://www.w3school.com.cn/jsref/met_loc_replace.asp) | 用新的文档替换当前文档。 |

#### 案例

解析URL中的query，并返回对象的形式

```javascript
function getQuery(queryStr) {
  var query = {};
  if (queryStr.indexOf('?') > -1) {
    var index = queryStr.indexOf('?');
    queryStr = queryStr.substr(index + 1);
    var array = queryStr.split('&');
    for (var i = 0; i < array.length; i++) {
      var tmpArr = array[i].split('=');
      if (tmpArr.length === 2) {
        query[tmpArr[0]] = tmpArr[1];
      }
    }
  }
  return query;
}
console.log(getQuery(location.search));
console.log(getQuery(location.href));
```

### 

### History 对象

History 对象包含用户（在浏览器窗口中）访问过的 URL。

History 对象是 window 对象的一部分，可通过 window.history 属性对其进行访问。

注释：没有应用于 History 对象的公开标准，不过所有浏览器都支持该对象。

**History 对象属性**

| 属性                                                         | 描述                              |
| ------------------------------------------------------------ | --------------------------------- |
| [length](http://www.w3school.com.cn/jsref/prop_his_length.asp) | 返回浏览器历史列表中的 URL 数量。 |

**History 对象方法**

| 方法                                                         | 描述                                |
| ------------------------------------------------------------ | ----------------------------------- |
| [back()](http://www.w3school.com.cn/jsref/met_his_back.asp)  | 加载 history 列表中的前一个 URL。   |
| [forward()](http://www.w3school.com.cn/jsref/met_his_forward.asp) | 加载 history 列表中的下一个 URL。   |
| [go()](http://www.w3school.com.cn/jsref/met_his_go.asp)      | 加载 history 列表中的某个具体页面。 |



**History 对象描述**

History 对象最初设计来表示窗口的浏览历史。但出于隐私方面的原因，History 对象不再允许脚本访问已经访问过的实际 URL。唯一保持使用的功能只有 [back()](http://www.w3school.com.cn/jsref/met_his_back.asp)、[forward()](http://www.w3school.com.cn/jsref/met_his_forward.asp) 和 [go()](http://www.w3school.com.cn/jsref/met_his_go.asp) 方法。

**例子**

下面一行代码执行的操作与单击后退按钮执行的操作一样：

```
history.back()
```

下面一行代码执行的操作与单击两次后退按钮执行的操作一样：

```
history.go(-2)
```

 

## Navigator 对象

Navigator 对象包含有关浏览器的信息。

注释：没有应用于 navigator 对象的公开标准，不过所有浏览器都支持该对象。

**Navigator 对象集合**

| 集合      | 描述                                                         |
| --------- | ------------------------------------------------------------ |
| plugins[] | 返回对文档中所有嵌入式对象的引用。该集合是一个 Plugin 对象的数组，其中的元素代表浏览器已经安装的插件。Plug-in 对象提供的是有关插件的信息，其中包括它所支持的 MIME 类型的列表。虽然 plugins[] 数组是由 IE 4 定义的，但是在 IE 4 中它却总是空的，因为 IE 4 不支持插件和 Plugin 对象。 |



**Navigator 对象属性**

| 属性                                                         | 描述                                           |
| ------------------------------------------------------------ | ---------------------------------------------- |
| [appCodeName](http://www.w3school.com.cn/jsref/prop_nav_appcodename.asp) | 返回浏览器的代码名。                           |
| [appMinorVersion](http://www.w3school.com.cn/jsref/prop_nav_appminorversion.asp) | 返回浏览器的次级版本。                         |
| [appName](http://www.w3school.com.cn/jsref/prop_nav_appname.asp) | 返回浏览器的名称。                             |
| [appVersion](http://www.w3school.com.cn/jsref/prop_nav_appversion.asp) | 返回浏览器的平台和版本信息。                   |
| [browserLanguage](http://www.w3school.com.cn/jsref/prop_nav_browserlanguage.asp) | 返回当前浏览器的语言。                         |
| [cookieEnabled](http://www.w3school.com.cn/jsref/prop_nav_cookieenabled.asp) | 返回指明浏览器中是否启用 cookie 的布尔值。     |
| [cpuClass](http://www.w3school.com.cn/jsref/prop_nav_cpuclass.asp) | 返回浏览器系统的 CPU 等级。                    |
| [onLine](http://www.w3school.com.cn/jsref/prop_nav_online.asp) | 返回指明系统是否处于脱机模式的布尔值。         |
| [platform](http://www.w3school.com.cn/jsref/prop_nav_platform.asp) | 返回运行浏览器的操作系统平台。                 |
| [systemLanguage](http://www.w3school.com.cn/jsref/prop_nav_systemlanguage.asp) | 返回 OS 使用的默认语言。                       |
| [userAgent](http://www.w3school.com.cn/jsref/prop_nav_useragent.asp) | 返回由客户机发送服务器的 user-agent 头部的值。 |
| [userLanguage](http://www.w3school.com.cn/jsref/prop_nav_userlanguage.asp) | 返回 OS 的自然语言设置。                       |



**Navigator 对象方法**

| 方法                                                         | 描述                                         |
| ------------------------------------------------------------ | -------------------------------------------- |
| [javaEnabled()](http://www.w3school.com.cn/jsref/met_nav_javaenabled.asp) | 规定浏览器是否启用 Java。                    |
| [taintEnabled()](http://www.w3school.com.cn/jsref/met_nav_taintenabled.asp) | 规定浏览器是否启用数据污点 (data tainting)。 |



**Navigator 对象描述**

Navigator 对象包含的属性描述了正在使用的浏览器。可以使用这些属性进行平台专用的配置。

虽然这个对象的名称显而易见的是 Netscape 的 Navigator 浏览器，但其他实现了 JavaScript 的浏览器也支持这个对象。

Navigator 对象的实例是唯一的，可以用 Window 对象的 navigator 属性来引用它。

### DOM的概念

文档对象模型（Document Object Model，简称DOM），是[W3C](http://baike.baidu.com/item/W3C)组织推荐的处理可扩展标志语言的标准编程接口。在网页上，组织页面（或文档）的对象被组织在一个树形结构中，用来表示文档中对象的标准模型就称为DOM。Document Object Model的历史可以追溯至1990年代后期微软与[Netscape](http://baike.baidu.com/item/Netscape)的“浏览器大战”，双方为了在[JavaScript](http://baike.baidu.com/item/JavaScript)与[JScript](http://baike.baidu.com/item/JScript)一决生死，于是大规模的赋予浏览器强大的功能。微软在网页技术上加入了不少专属事物，既有[VBScript](http://baike.baidu.com/item/VBScript)、[ActiveX](http://baike.baidu.com/item/ActiveX)、以及微软自家的[DHTML](http://baike.baidu.com/item/DHTML)格式等，使不少网页使用非微软平台及浏览器无法正常显示。DOM即是当时蕴酿出来的杰作。

DOM又称为文档树模型

![1497154623955](A:/2018%E6%9C%80%E6%96%B0%E4%BC%A0%E6%99%BA%E5%8D%9A%E5%AE%A2%E5%89%8D%E7%AB%AF36%E6%9C%9F/04webapi/01-JavaScript-WEB-API-%E7%AC%AC1%E5%A4%A9/01%E6%95%99%E5%AD%A6%E8%B5%84%E6%96%99/02-Web%20API/media/1497154623955.png)

- 文档：一个网页可以称为文档
- 节点：网页中的所有内容都是节点（标签、属性、文本、注释等）
- 元素：网页中的标签
- 属性：标签的属性

### 模拟文档树结构

![1497165666684](A:/2018%E6%9C%80%E6%96%B0%E4%BC%A0%E6%99%BA%E5%8D%9A%E5%AE%A2%E5%89%8D%E7%AB%AF36%E6%9C%9F/04webapi/01-JavaScript-WEB-API-%E7%AC%AC1%E5%A4%A9/01%E6%95%99%E5%AD%A6%E8%B5%84%E6%96%99/02-Web%20API/media/1497165666684.png)

```javascript
function Element(option) {
  this.id = option.id || '';
  this.nodeName = option.nodeName || '';
  this.nodeValue = option.nodeValue || '';
  this.nodeType = 1;
  this.children = option.children || [];
}

var doc = new Element({
  nodeName: 'html'
});
var head = new Element({
  nodeName: 'head'
});
var body = new Element({
  nodeName: 'body'
})
doc.children.push(head);
doc.children.push(body);

var div = new Element({
  nodeName: 'div',
  nodeValue: 'haha',
});

var p = new Element({
  nodeName: 'p',
  nodeValue: '段落'
})
body.children.push(div);
body.children.push(p);

function getChildren(ele) {
  for(var i = 0; i < ele.children.length; i++) {
    var child = ele.children[i];
    console.log(child.nodeName);
    getChildren(child);
  }
}
getChildren(doc);
```

### DOM经常进行的操作

- 获取元素
- 动态创建元素
- 对元素进行操作(设置其属性或调用其方法)
- 事件(什么时机做相应的操作)

## 获取页面元素

## 案例

1.点击按钮弹出对话框

```
<input type="button" value="弹出对话框" id="btn"/>
<script>
      //先有元素,才能获取,获取之后才能注册事件
      //根据id属性的值从文档中获取这个元素,
      var btnObj = document.getElementById("btn");
      //为当前的这个按钮元素(对象),注册点击事件,添加事件处理函数(匿名函数)
      btnObj.onclick = function () {
        //响应做的事情
        alert("弹出弹出对话框")
      };
</script>
```

2.点击按钮修改超链接的地址和热点文字

```
<input type="button" id="btn" value="点击按钮修改超链接的地址和热点文字">
<a href="https://www.baidu.com/" id="baidu">跳转到百度</a>
<script>
	////根据id获取a标签元素对象,
    var baiduObj = document.getElementById("baidu");
    document.getElementById("btn").onclick = function () {
    	//设置href属性
        baiduObj.href = "https://www.qq.com/";
        //设置文字内容
        baiduObj.innerText = "跳转到腾讯"
    }
```

3.点击(每个)图片弹出对话框

```
<img src="images/1.jpg" alt="" id="img1"/>
<img src="images/2.jpg" alt="" id="img2"/>
<img src="images/3.jpg" alt="" id="img3"/>
<script>
    //根据标签的名字获取图片标签,分别注册点击事件
    var imgObjs = document.getElementsByTagName("img");
    //循环遍历数组,获取每个图片标签,注册点击事件,添加事件处理函数
    for (var i = 0; i < imgObjs.length; i++) {
        imgObjs[i].onclick = function () {

            alert("被点击了" + this.id);
        };
    }
</script>
```

4.点击图片设置自身宽和高

```
<img src="images/1.jpg" alt="" id="img1"/>
<script>
    var imgObj = document.getElementById("img1");
    imgObj.onclick = function () {
        imgObj.style.width = "400px"
        imgObj.style.height = "400px"
    }
</script>
```

5.点击按钮修改图片的title属性

```
<img src="images/1.jpg" alt="" id="img1"/>
<img src="images/2.jpg" alt="" id="img2"/>
<img src="images/3.jpg" alt="" id="img3"/>
<script>
    var imgObjList = document.getElementsByTagName("img");
    for (i = 0; i < imgObjList.length; i++) {
        imgObjList[i].onclick = function () {
            this.style.width = "400px"
            this.style.height = "400px"
            this.title = (this.id)
        }
    }
</script>
```

6.点击按钮更改文本内容(排他功能)

```
<p>天才</p><p>天才</p><p>天才</p><p>天才</p>
<script>
    var pObjList = document.getElementsByTagName("p");
    for (i = 0; i < pObjList.length; i++) {
        pObjList[i].onclick = function () {
            for (var j = 0; j < pObjList.length; j++) {
                pObjList[j].innerText = "天才";
            }
            this.innerText = "疯子"
        }
    }
```

7.点击按钮显示和隐藏div

```
<input type="button" value="显示" id="btn"/>
<div id="div" style="width: 80px;height: 50px; background: gold">显示</div>
<script>
    var divObj = document.getElementById("div");
    var divText = divObj.innerText;
    document.getElementById("btn").onclick = function () {
        if (this.value == "显示") {
            this.value = "隐藏";
            divObj.style.display = "none";//隐藏
        } else {
            this.value = "显示";
            divObj.style.display = "block";//隐藏
        }
    }
```



8.显示和隐藏二维码

```

```

9.点击按钮修改所有p标签内容
10.点击按钮修改所有文本框内容
11.点击按钮切换图片
12.点击超链接停止跳转页面
13.点击小图显示大图
14.美女相册
15.点击按钮选中性别和兴趣
16.点击按钮禁用文本框

```
<input type="button" value="禁用文本框" id="btn"/>
<input type="text" value="文本框" id="txt"/>
<script>
    //先根据id获取按钮,为按钮注册点击事件,添加事件处理函数
    document.getElementById("btn").onclick = function () {
        //根据id获取文本框,设置disabled属性
        document.getElementById("txt").disabled = true;
    };
</script>
```
17.阻止超链接跳转

```
<a href="http://www.baidu.com" id="baidu">指向百度</a>
<script>
    document.getElementById("baidu").onclick = function () {
        // alert("阻止跳转")
        //阻止超链接的默认的跳转:return false,消耗掉事件
        return false;
    }
</script>
```

18.鼠标经过显示图片事件

```
<a href="#" id="a-img">鼠标经过显示二维码
    <img id="img" src="images/456.png" alt="" style="display: none"/>
</a>
<script>
    var aImgObg = document.getElementById("a-img");
    var imgObg = document.getElementById("img");
    aImgObg.onmouseover = function () {
        imgObg.style.display = "block";
    }
    aImgObg.onmouseout = function () {
        imgObg.style.display = "none";
    };
</script>
```





### 为什么要获取页面元素

例如：我们想要操作页面上的某部分(显示/隐藏，动画)，需要先获取到该部分对应的元素，才进行后续操作

### 根据id获取元素

```javascript
var div = document.getElementById('main');
console.log(div);

// 获取到的数据类型 HTMLDivElement，对象都是有类型的
// HTMLDivElement <-- HTMLElement <-- Element  <-- Node  <-- EventTarget
```

注意：由于id名具有唯一性，部分浏览器支持直接使用id名访问元素，但不是标准方式，不推荐使用。

### 根据标签名获取元素

```javascript
var divs = document.getElementsByTagName('div');
for (var i = 0; i < divs.length; i++) {
  var div = divs[i];
  console.log(div);
}
```

### 根据name获取元素*

```javascript
var inputs = document.getElementsByName('hobby');
for (var i = 0; i < inputs.length; i++) {
  var input = inputs[i];
  console.log(input);
}
```

### 根据类名获取元素

```javascript
var mains = document.getElementsByClassName('main');
for (var i = 0; i < mains.length; i++) {
  var main = mains[i];
  console.log(main);
}
```

### 根据选择器获取元素

```javascript
var text = document.querySelector('#text');
console.log(text);

var boxes = document.querySelectorAll('.box');
for (var i = 0; i < boxes.length; i++) {
  var box = boxes[i];
  console.log(box);
}
```

- 总结

```
  * 根据id属性的值获取元素,返回来的是一个元素对象
  * document.getElementById("id属性的值");
  *
  * 根据标签名字获取元素,返回来的是一个伪数组,里面保存了多个的DOM对象
  * document.getElementsByTagName("标签名字");
  *
  * 下面的几个,有的浏览器不支持
  *
  * 根据name属性的值获取元素,返回来的是一个伪数组,里面保存了多个的DOM对象
  * document.getElementsByName("name属性的值")
  * 根据类样式的名字来获取元素,返回来的是一个伪数组,里面保存了多个的DOM对象
  * document.getElementsByClassName("类样式的名字")
  * 根据选择器获取元素,返回来的是一个元素对象
  * document.querySelector("选择器的名字");
  *
  * 根据选择器获取元素,返回来的是一个伪数组,里面保存了多个的DOM对象
  * document.querySelectorAll("选择器的名字")
```

## 事件

事件：触发-响应机制

Event接口表示在DOM中发生的任何事件，一些是用户生成的（例如鼠标或键盘事件），而其他由API生成。

### 事件三要素

- 事件源:触发(被)事件的元素
- 事件类型:事件的触发方式(例如鼠标点击或键盘点击)
- 事件处理程序:事件触发后要执行的代码(函数形式)

### 事件的基本使用

```javascript
var box = document.getElementById('box');
box.onclick = function() {
  console.log('代码会在box被点击后执行');  
};
```

### 案例

- 点击按钮弹出提示框
- 点击按钮修改元素的样式

## 属性操作

### 非表单元素的属性

href、title、id、src、className

```javascript
var link = document.getElementById('link');
console.log(link.href);
console.log(link.title);

var pic = document.getElementById('pic');
console.log(pic.src);
```

案例：

​	点击按钮，切换img标签里的图片

​	点击按钮显示隐藏div

- innerHTML和innerText

```javascript
var box = document.getElementById('box');
box.innerHTML = '我是文本<p>我会生成为标签</p>';
console.log(box.innerHTML);
box.innerText = '我是文本<p>我不会生成为标签</p>';
console.log(box.innerText);
```

- HTML转义符

```
"		&quot;
‘		&apos;
&		&amp;
<		&lt;    //less than  小于
>		&gt;   // greater than  大于
空格	   &nbsp;
©		&copy;
```

- innerHTML和innerText的区别
- innerText的兼容性处理

### 表单元素属性

- value 用于大部分表单元素的内容获取(option除外)
- type 可以获取input标签的类型(输入框或复选框等)
- disabled 禁用属性
- checked 复选框选中属性
- selected 下拉菜单选中属性

### 案例

- 给文本框赋值，获取文本框的值
- 点击按钮禁用文本框
- 搜索文本框
- 检测用户名是否是3-6位，密码是否是6-8位，如果不满足要求高亮显示文本框
- 设置下拉框中的选中项
- 全选反选

### 自定义属性操作

- getAttribute() 获取标签行内属性
- setAttribute() 设置标签行内属性
- removeAttribute() 移除标签行内属性
- 与element.属性的区别: 上述三个方法用于获取任意的行内属性。

### 样式操作

- 使用style方式设置的样式显示在标签行内

```javascript
var box = document.getElementById('box');
box.style.width = '100px';
box.style.height = '100px';
box.style.backgroundColor = 'red';
```

- 注意

  通过样式属性设置宽高、位置的属性类型是字符串，需要加上px

### 类名操作

- 修改标签的className属性相当于直接修改标签的类名

```javascript
var box = document.getElementById('box');
box.className = 'clearfix';
```

### 案例

- 开关灯
- 点击按钮变色
- 图片切换二维码案例
- 当前输入的文本框高亮显示
- 点击按钮改变div的大小和位置
- 列表隔行变色、高亮显示
- 京东商品展示
- tab选项卡切换

## 创建元素的三种方式

### document.write()

```javascript
document.write('新设置的内容<p>标签也可以生成</p>');
```

### innerHTML

```javascript
var box = document.getElementById('box');
box.innerHTML = '新内容<p>新标签</p>';
```

### document.createElement()

```javascript
var div = document.createElement('div');
document.body.appendChild(div);
```

### 性能问题

- innerHTML方法由于会对字符串进行解析，需要避免在循环内多次使用。
- 可以借助字符串或数组的方式进行替换，再设置给innerHTML
- 优化后与document.createElement性能相近

### 案例

- 动态创建列表，高亮显示
- 根据数据动态创建表格
- 模拟百度搜索文本框

## 节点操作

```javascript
var body = document.body;
var div = document.createElement('div');
body.appendChild(div);

var firstEle = body.children[0];
body.insertBefore(div,firstEle);

body.removeChild(firstEle);

var text = document.createElement('p');
body.replaceChild(text, div);
```

案例：

​	权限选择

### 节点层级

重点讲父子属性，兄弟属性画图讲解

```javascript
var box = document.getElementById('box');
console.log(box.parentNode);
console.log(box.childNodes);
console.log(box.children);
console.log(box.nextSibling);
console.log(box.previousSibling);
console.log(box.firstChild);
console.log(box.lastChild);
```

- 注意

  childNodes和children的区别，childNodes获取的是子节点，children获取的是子元素

  nextSibling和previousSibling获取的是节点，获取元素对应的属性是nextElementSibling和previousElementSibling获取的是元素

  ​	nextElementSibling和previousElementSibling有兼容性问题，IE9以后才支持

- 总结

```
节点操作，方法
	appendChild()
	insertBefore()
	removeChild()
	replaceChild()
节点层次，属性
	parentNode
	childNodes
	children
	nextSibling/previousSibling
	firstChild/lastChild
```

## 事件详解



### 元素绑定事件

```javascript
    * 总结绑定事件的区别:
    * addEventListener();
    * attachEvent()
    * 相同点: 都可以为元素绑定事件
    * 不同点:
    * 1.方法名不一样
    * 2.参数个数不一样addEventListener三个参数,attachEvent两个参数
    * 3.addEventListener 谷歌,火狐,IE11支持,IE8不支持
    *   attachEvent 谷歌火狐不支持,IE11不支持,IE8支持
    * 4.this不同,addEventListener 中的this是当前绑定事件的对象
    *   attachEvent中的this是window
    * 5.addEventListener中事件的类型(事件的名字)没有on
    *  attachEvent中的事件的类型(事件的名字)有on
    *
    *  现在遇到的逆境,都是以后成长的阶梯


<input type="button" value="按钮" id="btn"/>
<script>
    //谷歌火狐支持,IE不支持
document.getElementById("btn").addEventListener("click", function (){
        console.log("addEventListener")
    }, false);
	//谷歌火狐不支持,IE支持
document.getElementById("btn").attachEvent("onclick", function () {
        console.log("attachEvent")
    });
</script>
```

**兼容代码**

```javascript
/**
 * 为任意一个元素绑定事件:元素,事件类型,事件处理函数
 * @param element
 * @param type
 * @param fn
 */
function addEventListener(element, type, fn) {
    if (element.addEventListener) {
        //支持
        element.addEventListener(type, fn, false);
    } else if (element.attachEvent) {
        element.attachEvent("on" + type, fn);
    } else {
        element["on" + type] = fn;
    }
}
```

### 元素解绑事件

**注意:用什么方式绑定事件,就应该用对应的方式解绑事件**

1.解绑事件

对象.on事件名字=事件处理函数--->绑定事件

对象.on事件名字=null;

2.解绑事件

对象.addEventListener("没有on的事件类型",命名函数,false);---绑定事件

对象.removeEventListener("没有on的事件类型",函数名字,false);

3.解绑事件

对象.attachEvent("on事件类型",命名函数);---绑定事件

对象.detachEvent("on事件类型",函数名字);



**兼容代码**

```

/**为任意的一个元素解绑某个事件:元素,事件类型,事件处理函数
 *
 * @param element
 * @param type
 * @param fn
 */
function removeEventListener(element, type, fn) {
    if (element.removeEventListener) {
        element.removeEventListener(type, fn, false);
    } else if (element.detachEvent) {
        element.detachEvent("on" + type, fn);
    } else {
        element["on" + type] = null;
    }
}
```



### 事件的三个阶段

1.事件捕获阶段  :从外向内

2.事件目标阶段  :最开始选择的那个

3.事件冒泡阶段  : 从里向外

* 为元素绑定事件
* addEventListener("没有on的事件类型",事件处理函数,控制事件阶段的)
* 事件触发的过程中,可能会出现事件冒泡的效果,为了阻止事件冒泡--->
* window.event.cancelBubble=true;谷歌,IE8支持,火狐不支持
* window.event就是一个对象,是IE中的标准
* e.stopPropagation();阻止事件冒泡---->谷歌和火狐支持
* window.event和e都是事件参数对象,一个是IE的标准,一个是火狐的标准
* 事件参数e在IE8的浏览器中是不存在,此时用window.event来代替
* addEventListener中第三个参数是控制事件阶段的
* 事件的阶段有三个:
* 通过e.eventPhase这个属性可以知道当前的事件是什么阶段你的
* 如果这个属性的值是:
* 1---->捕获阶段
* 2---->目标阶段
* 3---->冒泡
* 一般默认都是冒泡阶段,很少用捕获阶段
* 冒泡阶段:从里向外
* 捕获阶段:从外向内

1. 捕获阶段

2. 当前目标阶段

3. 冒泡阶段

   事件对象.eventPhase属性可以查看事件触发时所处的阶段

### 事件对象的属性和方法

- event.type 获取事件类型
- clientX/clientY     所有浏览器都支持，窗口位置
- pageX/pageY       IE8以前不支持，页面位置
- event.target || event.srcElement 用于获取触发事件的元素
- event.preventDefault() 取消默认行为

#### 案例

- 跟着鼠标飞的天使
- 鼠标点哪图片飞到哪里
- 获取鼠标在div内的坐标

### 阻止事件传播的方式

- 标准方式 event.stopPropagation();
- IE低版本 event.cancelBubble = true; 标准中已废弃

### 常用的鼠标和键盘事件

- onmouseup 鼠标按键放开时触发
- onmousedown 鼠标按键按下触发
- onmousemove 鼠标移动触发
- onkeyup 键盘按键按下触发
- onkeydown 键盘按键抬起触发

## 特效

### 偏移量

- offsetParent用于获取定位的父级元素

- offsetParent和parentNode的区别

  **offset系列:**

  offsetLeft:距离左边位置的值

  offsetTop:距离上面位置的值

  offsetWidth:元素的宽(有边框)

  offsetHeight:元素的高(有边框)

```javascript
var box = document.getElementById('box');
console.log(box.offsetParent);
console.log(box.offsetLeft);
console.log(box.offsetTop);
console.log(box.offsetWidth);
console.log(box.offsetHeight);
```

![1498743216279](A:/2018%E6%9C%80%E6%96%B0%E4%BC%A0%E6%99%BA%E5%8D%9A%E5%AE%A2%E5%89%8D%E7%AB%AF36%E6%9C%9F/04webapi/01-JavaScript-WEB-API-%E7%AC%AC1%E5%A4%A9/01%E6%95%99%E5%AD%A6%E8%B5%84%E6%96%99/02-Web%20API/media/1498743216279.png)

### 客户区大小

```javascript
var box = document.getElementById('box');
console.log(box.clientLeft);
console.log(box.clientTop);
console.log(box.clientWidth);
console.log(box.clientHeight);
```

![1498743269100](A:/2018%E6%9C%80%E6%96%B0%E4%BC%A0%E6%99%BA%E5%8D%9A%E5%AE%A2%E5%89%8D%E7%AB%AF36%E6%9C%9F/04webapi/01-JavaScript-WEB-API-%E7%AC%AC1%E5%A4%A9/01%E6%95%99%E5%AD%A6%E8%B5%84%E6%96%99/02-Web%20API/media/1498743269100.png)

### 滚动偏移

```javascript
var box = document.getElementById('box');
console.log(box.scrollLeft)
console.log(box.scrollTop)
console.log(box.scrollWidth)
console.log(box.scrollHeight)
```

![1498743288621](A:/2018%E6%9C%80%E6%96%B0%E4%BC%A0%E6%99%BA%E5%8D%9A%E5%AE%A2%E5%89%8D%E7%AB%AF36%E6%9C%9F/04webapi/01-JavaScript-WEB-API-%E7%AC%AC1%E5%A4%A9/01%E6%95%99%E5%AD%A6%E8%B5%84%E6%96%99/02-Web%20API/media/1498743288621.png)

### 案例

- 匀速动画函数
- 变速动画函数
- 回到顶部
- 无缝轮播图
- 模拟滚动条
- 拖拽案例
- 放大镜案例S

## 附录

### 元素的类型

