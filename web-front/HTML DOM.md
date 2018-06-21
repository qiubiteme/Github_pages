[TOC]

# HTML DOM

# DOM 教程

HTML DOM 定义了访问和操作 HTML 文档的标准方法。

DOM 将 HTML 文档表达为树结构。

[开始学习 HTML DOM](http://www.w3school.com.cn/htmldom/dom_intro.asp)！

## HTML DOM 树

![](http://www.w3school.com.cn/i/ct_htmltree.gif)

## HTML DOM 实例

学习 100 个实例！通过我们的在线编辑器，您能够编辑 HTML 代码，然后点击“亲自试一试”按钮来查看结果。

[HTML DOM 实例](http://www.w3school.com.cn/example/hdom_examples.asp)

## HTML DOM 参考手册

在 W3School，我们提供包含大量实例的完整 HTML DOM 参考手册。

[HTML DOM 参考手册](http://www.w3school.com.cn/jsref/index.asp)



# DOM 简介

**HTML DOM 定义了访问和操作 HTML 文档的标准。**

## 您应该具备的基础知识

在您继续学习之前，您需要对以下内容拥有基本的了解：

- HTML
- CSS
- JavaScript

如果您需要首先学习这些项目，请访问我们的[首页](http://www.w3school.com.cn/index.html)。

## 什么是 DOM？

DOM 是 W3C（万维网联盟）的标准。

DOM 定义了访问 HTML 和 XML 文档的标准：

> “W3C 文档对象模型 （DOM） 是中立于平台和语言的接口，它允许程序和脚本动态地访问和更新文档的内容、结构和样式。”

W3C DOM 标准被分为 3 个不同的部分：

- 核心 DOM - 针对任何结构化文档的标准模型
- XML DOM - 针对 XML 文档的标准模型
- HTML DOM - 针对 HTML 文档的标准模型

编者注：DOM 是 Document Object Model（文档对象模型）的缩写。

## 什么是 XML DOM？

XML DOM 定义了所有 XML 元素的*对象*和*属性*，以及访问它们的*方法*。

如果您需要学习 XML DOM，请访问我们的 [XML DOM 教程](http://www.w3school.com.cn/xmldom/index.asp)。

## 什么是 HTML DOM？

HTML DOM 是：

- HTML 的标准对象模型
- HTML 的标准编程接口
- W3C 标准

HTML DOM 定义了所有 HTML 元素的*对象*和*属性*，以及访问它们的*方法*。

*换言之，HTML DOM 是关于如何获取、修改、添加或删除 HTML 元素的标准。*



# DOM 节点

**在 HTML DOM 中，所有事物都是节点。DOM 是被视为节点树的 HTML。**

## DOM 节点

根据 W3C 的 HTML DOM 标准，HTML 文档中的所有内容都是节点：

- 整个文档是一个文档节点
- 每个 HTML 元素是元素节点
- HTML 元素内的文本是文本节点
- 每个 HTML 属性是属性节点
- 注释是注释节点

## HTML DOM 节点树

HTML DOM 将 HTML 文档视作树结构。这种结构被称为*节点树*：

### HTML DOM Tree 实例

![](http://www.w3school.com.cn/i/ct_htmltree.gif)

通过 HTML DOM，树中的所有节点均可通过 JavaScript 进行访问。所有 HTML 元素（节点）均可被修改，也可以创建或删除节点。

## 节点父、子和同胞

节点树中的节点彼此拥有层级关系。

父（parent）、子（child）和同胞（sibling）等术语用于描述这些关系。父节点拥有子节点。同级的子节点被称为同胞（兄弟或姐妹）。

- 在节点树中，顶端节点被称为根（root）
- 每个节点都有父节点、除了根（它没有父节点）
- 一个节点可拥有任意数量的子
- 同胞是拥有相同父节点的节点

下面的图片展示了节点树的一部分，以及节点之间的关系：

![](http://www.w3school.com.cn/i/dom_navigate.gif)

## 请看下面的 HTML 片段：

```
<html>
  <head>
    <title>DOM 教程</title>
  </head>
  <body>
    <h1>DOM 第一课</h1>
    <p>Hello world!</p>
  </body>
</html>
```

从上面的 HTML 中：

- <html> 节点没有父节点；它是根节点
- <head> 和 <body> 的父节点是 <html> 节点
- 文本节点 "Hello world!" 的父节点是 <p> 节点

并且：

- <html> 节点拥有两个子节点：<head> 和 <body>
- <head> 节点拥有一个子节点：<title> 节点
- <title> 节点也拥有一个子节点：文本节点 "DOM 教程"
- <h1> 和 <p> 节点是同胞节点，同时也是 <body> 的子节点

并且：

- <head> 元素是 <html> 元素的首个子节点
- <body> 元素是 <html> 元素的最后一个子节点
- <h1> 元素是 <body> 元素的首个子节点
- <p> 元素是 <body> 元素的最后一个子节点

## 警告！

DOM 处理中的常见错误是希望元素节点包含文本。

在本例中：*<title>DOM 教程</title>*，元素节点 <title>，包含值为 "DOM 教程" 的*文本节点*。

可通过节点的 *innerHTML* 属性来访问文本节点的值。

您将在稍后的章节中学习更多有关 innerHTML 属性的知识。

# DOM 方法

方法是我们可以在节点（HTML 元素）上执行的动作。

## 编程接口

可通过 JavaScript （以及其他编程语言）对 HTML DOM 进行访问。

所有 HTML 元素被定义为对象，而编程接口则是对象方法和对象属性。

方法是您能够执行的动作（比如添加或修改元素）。

属性是您能够获取或设置的值（比如节点的名称或内容）。

## getElementById() 方法

getElementById() 方法返回带有指定 ID 的元素：

**例子**

```
<p id="intro">Hello World!</p>
<p>本例演示 <b>getElementById</b> 方法！</p>

<script>
    x=document.getElementById("intro");
    document.write("来自 intro 段落的文本：" + x.innerHTML);
</script>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=dom_getelementbyid)

## HTML DOM 对象 - 方法和属性

**一些常用的 HTML DOM 方法：**

- getElementById(id) - 获取带有指定 id 的节点（元素）
- appendChild(node) - 插入新的子节点（元素）
- removeChild(node) - 删除子节点（元素）

**一些常用的 HTML DOM 属性：**

- innerHTML - 节点（元素）的文本值
- parentNode - 节点（元素）的父节点
- childNodes - 节点（元素）的子节点
- attributes - 节点（元素）的属性节点

您将在本教程的下一章中学到更多有关属性的知识。

## 现实生活中的对象

某个人是一个对象。

人的方法可能是 eat(), sleep(), work(), play() 等等。

所有人都有这些方法，但会在不同时间执行它们。

一个人的属性包括姓名、身高、体重、年龄、性别等等。

所有人都有这些属性，但它们的值因人而异。

## 一些 DOM 对象方法

这里提供一些您将在本教程中学到的常用方法：

| 方法                     | 描述                                                         |
| ------------------------ | ------------------------------------------------------------ |
| getElementById()         | 返回带有指定 ID 的元素。                                     |
| getElementsByTagName()   | 返回包含带有指定标签名称的所有元素的节点列表（集合/节点数组）。 |
| getElementsByClassName() | 返回包含带有指定类名的所有元素的节点列表。                   |
| appendChild()            | 把新的子节点添加到指定节点。                                 |
| removeChild()            | 删除子节点。                                                 |
| replaceChild()           | 替换子节点。                                                 |
| insertBefore()           | 在指定的子节点前面插入新的子节点。                           |
| createAttribute()        | 创建属性节点。                                               |
| createElement()          | 创建元素节点。                                               |
| createTextNode()         | 创建文本节点。                                               |
| getAttribute()           | 返回指定的属性值。                                           |
| setAttribute()           | 把指定属性设置或修改为指定的值。                             |

# DOM 属性

属性是节点（HTML 元素）的值，您能够获取或设置。

## 编程接口

可通过 JavaScript （以及其他编程语言）对 HTML DOM 进行访问。

所有 HTML 元素被定义为对象，而编程接口则是对象方法和对象属性。

方法是您能够执行的动作（比如添加或修改元素）。

属性是您能够获取或设置的值（比如节点的名称或内容）。

## innerHTML 属性

获取元素内容的最简单方法是使用 innerHTML 属性。

innerHTML 属性对于获取或替换 HTML 元素的内容很有用。

**实例**

下面的代码获取 id="intro" 的 <p> 元素的 innerHTML：

**实例**

```
<p id="intro">Hello World!</p>
<script>
    var txt=document.getElementById("intro").innerHTML;
    document.write(txt);
</script>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=dom_innerhtml)

在上面的例子中，getElementById 是一个方法，而 innerHTML 是属性。

innerHTML 属性可用于获取或改变任意 HTML 元素，包括 <html> 和 <body>。

## nodeName 属性

nodeName 属性规定节点的名称。

- nodeName 是只读的
- 元素节点的 nodeName 与标签名相同
- 属性节点的 nodeName 与属性名相同
- 文本节点的 nodeName 始终是 #text
- 文档节点的 nodeName 始终是 #document

注释：nodeName 始终包含 HTML 元素的大写字母标签名。

## nodeValue 属性

nodeValue 属性规定节点的值。

- 元素节点的 nodeValue 是 undefined 或 null
- 文本节点的 nodeValue 是文本本身
- 属性节点的 nodeValue 是属性值

## 获取元素的值

下面的例子会取回 <p id="intro"> 标签的文本节点值：

**实例**

```
<p id="intro">Hello World!</p>
<script type="text/javascript">
    x=document.getElementById("intro");
    document.write(x.firstChild.nodeValue);
</script>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=dom_firstchild_nodevalue)

## nodeType 属性

nodeType 属性返回节点的类型。nodeType 是只读的。

比较重要的节点类型有：

| 元素类型 | NodeType |
| -------- | -------- |
| 元素     | 1        |
| 属性     | 2        |
| 文本     | 3        |
| 注释     | 8        |
| 文档     | 9        |



# DOM 访问

访问 HTML DOM - 查找 HTML 元素。

## 访问 HTML 元素（节点）

访问 HTML 元素等同于访问节点

您能够以不同的方式来访问 HTML 元素：

- 通过使用 getElementById() 方法
- 通过使用 getElementsByTagName() 方法
- 通过使用 getElementsByClassName() 方法

## getElementById() 方法

getElementById() 方法返回带有指定 ID 的元素：

**语法**

```
node.getElementById("id");
```

下面的例子获取 id="intro" 的元素：

**实例**

```
<p id="intro">Hello World!</p>
<p>本例演示 <b>getElementById</b> 方法！</p>

<script>
    x = document.getElementById("intro");
    document.write("<p>来自 intro 段落的文本：" + x.innerHTML + "</p>");
</script>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=dom_getelementbyid)

## getElementsByTagName() 方法

getElementsByTagName() 返回带有指定标签名的所有元素。

**语法**

```
node.getElementsByTagName("tagname");
```

下面的例子返回包含文档中所有 <p> 元素的列表：

**实例 1**

```
<p>Hello World!</p>
<p>DOM 很有用！</p>
<p>本例演示 <b>getElementsByTagName</b> 方法。</p>

<script>
    x = document.getElementsByTagName("p");
    document.write("第1段的文本: " + x[0].innerHTML);
    document.write("第2段的文本: " + x[1].innerHTML);
</script>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=dom_getelementsbytagname)

下面的例子返回包含文档中所有 <p> 元素的列表，并且这些 <p> 元素应该是 id="main" 的元素的后代（子、孙等等）：

**实例 2**

```
<p>Hello World!</p>

<div id="main">
    <p>DOM 很有用！</p>
    <p>本例演示 <b>getElementsByTagName</b> 方法。</p>
</div>

<script>
    x = document.getElementById("main").getElementsByTagName("p");
    document.write("div 中的第一段的文本: " + x[0].innerHTML);
    document.write("div 中的第2段的文本: " + x[1].innerHTML);
</script>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=dom_getelementsbytagname2)

## getElementsByClassName() 方法

如果您希望查找带有相同类名的所有 HTML 元素，请使用这个方法：

```
document.getElementsByClassName("intro");
```

上面的例子返回包含 class="intro" 的所有元素的一个列表：

注释：getElementsByClassName() 在 Internet Explorer 5,6,7,8 中无效。

## querySelector() 方法

返回文档中匹配指定 CSS 选择器的一个元素。 

**注意：** querySelector() 方法仅仅返回匹配指定选择器的第一个元素。如果你需要返回所有的元素，请使用 querySelectorAll() 方法替代。

更多 CSS 选择器，请访问我们的 [CSS 选择器教程](http://www.runoob.com/css/css-selectors.html) 和我们的 [CSS 选择器参考手册](http://www.runoob.com/cssref/css-selectors.html)。

------

**浏览器支持**

表格中的数字表示支持该方法的第一个浏览器的版本号。

| 方法            |      |      |      |      |      |
| --------------- | ---- | ---- | ---- | ---- | ---- |
| querySelector() | 4.0  | 8.0  | 3.5  | 3.1  | 10.0 |

# DOM - 修改HTML内容

修改 HTML = 改变元素、属性、样式和事件。

## 修改 HTML 元素

修改 HTML DOM 意味着许多不同的方面：

- 改变 HTML 内容
- 改变 CSS 样式
- 改变 HTML 属性
- 创建新的 HTML 元素
- 删除已有的 HTML 元素
- 改变事件（处理程序）

在接下来的章节，我们会深入学习修改 HTML DOM 的常用方法。

## 创建 HTML 内容

改变元素内容的最简答的方法是使用 innerHTML 属性。

下面的例子改变一个 <p> 元素的 HTML 内容：

**实例**

```
<p id="p1">Hello World!</p>
<script>
    document.getElementById("p1").innerHTML = "New text!";
</script> 
<p>上面的段落被一段脚本改变了。</p>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=dom_changetext)

提示：我们将在下面的章节为您解释例子中的细节。

## 改变 HTML 样式

通过 HTML DOM，您能够访问 HTML 元素的样式对象。

下面的例子改变一个段落的 HTML 样式：

**实例**

```
<p id="p1">Hello world!</p>
<p id="p2">Hello world!</p>

<script>
    document.getElementById("p2").style.color = "blue";
    document.getElementById("p2").style.fontFamily = "Arial";
    document.getElementById("p2").style.fontSize = "50px";
</script>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=dom_changestyle)

## 创建新的 HTML 元素

如需向 HTML DOM 添加新元素，您首先必须创建该元素（元素节点），然后把它追加到已有的元素上。

**实例**

```
<div id="div1">
    <p id="p1">This is a paragraph.</p>
    <p id="p2">This is another paragraph.</p>
</div>
<script>
	//创建元素节点
    var para = document.createElement("p");
    //创建文本节点
    var node = document.createTextNode("This is new.");
    //添加节点
    para.appendChild(node);
    var element = document.getElementById("div1");
    element.appendChild(para);
</script>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=dom_elementcreate)



## 使用事件

HTML DOM 允许您在事件发生时执行代码。

当 HTML 元素”有事情发生“时，浏览器就会生成事件：

- 在元素上点击
- 加载页面
- 改变输入字段

你可以在下一章学习更多有关事件的内容。

下面两个例子在按钮被点击时改变 <body> 元素的背景色：

**实例**

```
<input type="button" onclick="document.body.style.backgroundColor='lavender';"
value="Change background color" />
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=dom_changebackground)

在本例中，由函数执行相同的代码：

**实例**

```
<script>
    function ChangeBackground() {
        document.body.style.backgroundColor = "lavender";
    }
</script>

<input type="button" onclick="ChangeBackground()"
       value="Change background color"/>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=dom_changebackground2)

下面的例子在按钮被点击时改变 <p> 元素的文本：

**实例**

```
<p id="p1">Hello world!</p>

<script>
    function ChangeText() {
        document.getElementById("p1").innerHTML = "New text!";
    }
</script>

<input type="button" onclick="ChangeText()" value="改变文本"/>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=dom_changetext2)



# DOM - 元素

添加、删除和替换 HTML 元素。

## 创建新的 HTML 元素 - appendChild()

如需向 HTML DOM 添加新元素，您首先必须创建该元素，然后把它追加到已有的元素上。

**实例**

```
<div id="div1">
    <p id="p1">This is a paragraph.</p>
    <p id="p2">This is another paragraph.</p>
</div>

<script>
    var para = document.createElement("p");
    var node = document.createTextNode("This is new.");
    para.appendChild(node);

    var element = document.getElementById("div1");
    element.appendChild(para);
</script>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=dom_elementcreate)

**例子解释**

这段代码创建了一个新的 <p> 元素：

```
var para=document.createElement("p");
```

如需向 <p> 元素添加文本，您首先必须创建文本节点。这段代码创建文本节点：

```
var node=document.createTextNode("This is a new paragraph.");
```

然后您必须向 <p> 元素追加文本节点：

```
para.appendChild(node);
```

最后，您必须向已有元素追加这个新元素。

这段代码查找到一个已有的元素：

```
var element=document.getElementById("div1");
```

这段代码向这个已存在的元素追加新元素：

```
element.appendChild(para);
```

## 创建新的 HTML 元素 - insertBefore()

上一个例子中的 appendChild() 方法，将新元素作为父元素的最后一个子元素进行添加。

如果不希望如此，您可以使用 insertBefore() 方法：插入到指定的位置

**实例**

```
<div id="div1">
    <p id="p1">This is a paragraph.</p>
    <p id="p2">This is another paragraph.</p>
</div>

<script>
	//创建元素
    var para = document.createElement("p");
    //创建文本节点
    var node = document.createTextNode("This is new.");
    //给指定元素追加文本节点
    para.appendChild(node);
    var element = document.getElementById("div1");
    var child = document.getElementById("p2");
    //插入到指定元素前面
    element.insertBefore(para, child);
</script>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=dom_elementcreate2)

## 删除已有的 HTML 元素

如需删除 HTML 元素，您必须清楚该元素的父元素：

**实例**

```
<div id="div1">
    <p id="p1">This is a paragraph.</p>
    <p id="p2">This is another paragraph.</p>
</div>
<script>
    var parent = document.getElementById("div1");
    var child = document.getElementById("p1");
    parent.removeChild(child);
</script>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=dom_elementremove)

**例子解释**

这个 HTML 文档包含一个带有两个子节点（两个 <p> 元素）的 <div> 元素：

```
<div id="div1">
<p id="p1">This is a paragraph.</p>
<p id="p2">This is another paragraph.</p>
</div>
```

查找 id="div1" 的元素：

```
var parent=document.getElementById("div1");
```

查找 id="p1" 的 <p> 元素：

```
var child=document.getElementById("p1");
```

从父元素中删除子元素：

```
parent.removeChild(child);
```

提示：能否在不引用父元素的情况下删除某个元素？

很抱歉。DOM 需要了解您需要删除的元素，以及它的父元素。

这里提供一个常用的解决方法：找到您需要删除的子元素，然后使用 parentNode 属性来查找其父元素：

```
var child=document.getElementById("p1");
//获取父元素
child.parentNode.removeChild(child);
```

## 替换 HTML 元素

如需替换 HTML DOM 中的元素，请使用 replaceChild() 方法：

**实例**

```
<div id="div1">
    <p id="p1">This is a paragraph.</p>
    <p id="p2">This is another paragraph.</p>
</div>
<script>
    var para = document.createElement("p");
    var node = document.createTextNode("This is new.");
    para.appendChild(node);

    var parent = document.getElementById("div1");
    var child = document.getElementById("p1");
    //替换 HTML 元素
    parent.replaceChild(para, child);
</script>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=dom_elementreplace)



# DOM - 事件

HTML DOM 允许 JavaScript 对 HTML 事件作出反应。。

## 对事件作出反应

当事件发生时，可以执行 JavaScript，比如当用户点击一个 HTML 元素时。

如需在用户点击某个元素时执行代码，请把 JavaScript 代码添加到 HTML 事件属性中：

```
onclick=JavaScript
```

HTML 事件的例子：

- 当用户点击鼠标时
- 当网页已加载时
- 当图片已加载时
- 当鼠标移动到元素上时
- 当输入字段被改变时
- 当 HTML 表单被提交时
- 当用户触发按键时

在本例中，当用户点击时，会改变 <h1> 元素的内容：

**实例**

```
<h1 onclick="this.innerHTML='hello!'">请点击这段文本!</h1>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=dom_event_onclick)

在本例中，会从事件处理程序中调用函数：

**实例**

```
<script>
    function changetext(id) {
        id.innerHTML = "hello!";
    }
</script>
<h1 onclick="changetext(this)">请点击这段文本!</h1>

```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=dom_event_onclick2)

## HTML 事件属性

如需向 HTML 元素分配事件，您可以使用事件属性。

**实例**

向 button 元素分配一个 onclick 事件：

```
<p>点击按钮来执行 <b>displayDate()</b> 函数。</p>
<button onclick="displayDate()">试一试</button>
<script>
    function displayDate() {
        document.getElementById("demo").innerHTML = Date();
    }
</script>
<p id="demo"></p>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=dom_event)

在上面的例子中，当点击按钮时，会执行名为 displayDate 的函数。

## 使用 HTML DOM 来分配事件

HTML DOM 允许您使用 JavaScript 向 HTML 元素分配事件：

**实例**

为 button 元素分配 onclick 事件：

```
<p>点击按钮来执行 <b>displayDate()</b> 函数。</p>
<button id="myBtn">试一试</button>
<script>
    document.getElementById("myBtn").onclick = function () {
        displayDate()
    };
    function displayDate() {
        document.getElementById("demo").innerHTML = Date();
    }
</script>
<p id="demo"></p>
<script>
	//再次点击刷新时间
    document.getElementById("myBtn").onclick = function () {
        displayDate()
    };
</script>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=dom_event2)

在上面的例子中，名为 displayDate 的函数被分配给了 id=myButn" 的 HTML 元素。

当按钮被点击时，将执行函数。

## onload 和 onunload 事件

当用户进入或离开页面时，会触发 onload 和 onunload 事件。

onload 事件可用于检查访客的浏览器类型和版本，以便基于这些信息来加载不同版本的网页。

onload 和 onunload 事件可用于处理 cookies。

**实例**

```
<body onload="checkCookies()">
<script>
    function checkCookies() {
        if (navigator.cookieEnabled == true) {
            alert("Cookies are enabled")
        }
        else {
            alert("Cookies are not enabled")
        }
    }
</script>
<p>弹出的提示框会告诉你浏览器是否已启用 cookie。</p>
</body>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=dom_event_onload)

## onchange 事件

onchange 事件常用于输入字段的验证。

下面的例子展示了如何使用 onchange。当用户改变输入字段的内容时，将调用 upperCase() 函数。

**实例**

```
<script>
    function myFunction() {
        var x = document.getElementById("fname");
        x.value = x.value.toUpperCase();
    }
</script>
</head>
<body>
请输入你的英文名：<input type="text" id="fname" onchange="myFunction()">
<p>当你离开输入框时，被触发的函数会把你输入的文本转换为大写字母。</p>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=dom_event_onchange)

## onmouseover 和 onmouseout 事件

onmouseover 和 onmouseout 事件可用于在鼠标指针移动到或离开元素时触发函数。

**实例**

一个简单的 onmouseover-onmouseout 例子：

```
<div onmouseover="mOver(this)" onmouseout="mOut(this)">
	Mouse Over Me
</div>
<script>
    function mOver(obj) {
        obj.innerHTML = "谢谢你"
    }
    function mOut(obj) {
        obj.innerHTML = "把鼠标指针移动到上面"
    }
</script>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=dom_event_onmouseover)

## onmousedown、onmouseup 以及 onclick 事件

onmousedown、onmouseup 以及 onclick 事件是鼠标点击的全部过程。首先当某个鼠标按钮被点击时，触发 onmousedown 事件，然后，当鼠标按钮被松开时，会触发 onmouseup 事件，最后，当鼠标点击完成时，触发 onclick 事件。

**实例**

一个简单的 onmousedown-onmouseup 实例：

```
<div
        onmousedown="mDown(this)"
        onmouseup="mUp(this)"
        onclick="mEnd(this)"
        style="background-color:orange;width:200px;height:50px;padding-top:25px;text-align:center;">
    点击这里
</div>
<script>
    function mDown(obj) {
        obj.style.backgroundColor = "blue";
        obj.innerHTML = "点击鼠标改变颜色"
    }
    function mUp(obj) {
        obj.style.backgroundColor = "red";
        obj.innerHTML = "松开鼠标改变颜色"
    }
    function mEnd(obj){
        obj.style.backgroundColor = "greenyellow";
        obj.innerHTML = "事件结束改变颜色"
    }
</script>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=dom_event_onmousedown)

## HTML DOM 事件对象参考手册

如需每个事件的完整描述和例子，请访问我们的 [HTML DOM 参考手册](http://www.w3school.com.cn/jsref/index.asp)。



# DOM - 导航

通过 HTML DOM，您能够使用节点关系在节点树中导航。

## HTML DOM 节点列表

getElementsByTagName() 方法返回*节点列表*。节点列表是一个节点数组。

下面的代码选取文档中的所有 <p> 节点：

**实例**

```
var x=document.getElementsByTagName("p");
```

可以通过下标号访问这些节点。如需访问第二个 <p>，您可以这么写：

```
<p>Hello World!</p>
<p>DOM 很有用！</p>
<script>
    x = document.getElementsByTagName("p");
    document.write("第二段的 innerHTML 是: " + x[1].innerHTML);
</script>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=dom_nodelist)

注释：下标号从 0 开始。

## HTML DOM 节点列表长度

length 属性定义节点列表中节点的数量。

您可以使用 length 属性来循环节点列表：

**实例**

```
<p>Hello World!</p>
<p>DOM 很有用！</p>
<p>本例演示 <b>length</b> 属性。</p>
<script>
    x = document.getElementsByTagName("p");
    for (i = 0; i < x.length; i++) {
        document.write(x[i].innerHTML);
        document.write("<br>");
    }
</script>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=dom_nodelist_length)

**例子解释：**

- 获取所有 <p> 元素节点
- 输出每个 <p> 元素的文本节点的值

## 导航节点关系

您能够使用三个节点属性：parentNode、firstChild 以及 lastChild ，在文档结构中进行导航。

请看下面的 HTML 片段：

```
<html>
    <body>
        <p>Hello World!</p>
        <div>
          <p>DOM 很有用!</p>
          <p>本例演示节点关系。</p>
        </div>
    </body>
</html>
```

- 首个 <p> 元素是 <body> 元素的首个子元素（firstChild）
- <div> 元素是 <body> 元素的最后一个子元素（lastChild）
- <body> 元素是首个 <p> 元素和 <div> 元素的父节点（parentNode）

firstChild 属性可用于访问元素的文本：

### 实例

```
<html>
    <body>
    <p id="intro">Hello World!</p>
    <script>
        x = document.getElementById("intro");
        document.write(x.firstChild.nodeValue);
    </script>
    </body>
</html>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=dom_firstchild)

## DOM 根节点

这里有两个特殊的属性，可以访问全部文档：

- document.documentElement - 全部文档
- document.body - 文档的主体

**实例 document.body - 文档的主体**

```
<p>Hello World!</p>
<div>
    <p>DOM 很有用!</p>
    <p>本例演示 <b>document.body</b> 属性。</p>
</div>

<script>
    alert(document.body.innerHTML);
</script>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=dom_root)

**实例document.documentElement - 全部文档**

全部文档节点,不包含HTML根节点

```
<p>Hello World!</p>
<div>
    <p>DOM 很有用!</p>
    <p>本例演示 <b>document.body</b> 属性。</p>
</div>

<script>
    alert(document.documentElement .innerHTML);
</script>
```



## childNodes 和 nodeValue

除了 innerHTML 属性，您也可以使用 childNodes 和 nodeValue 属性来获取元素的内容。

下面的代码获取 id="intro" 的 <p> 元素的值：

### 实例

```
<p id="intro">Hello World!</p>

<script>
    var txt = document.getElementById("intro").childNodes[0].nodeValue;
    document.write(txt);
</script>

```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=dom_childnodes_nodevalue)

在上面的例子中，getElementById 是一个方法，而 childNodes 和 nodeValue 是属性。

在本教程中，我们将使用 innerHTML 属性。不过，学习上面的方法有助于对 DOM 树结构和导航的理解。

# DOM Style 对象

## Style 对象

Style 对象代表一个单独的样式声明。可从应用样式的文档或元素访问 Style 对象。

### 使用 Style 对象属性的语法：

```
document.getElementById("id").style.property="值"
```

## Style 对象的属性：

- [背景](http://www.w3school.com.cn/jsref/dom_obj_style.asp#background)
- [边框和边距](http://www.w3school.com.cn/jsref/dom_obj_style.asp#border)
- [布局](http://www.w3school.com.cn/jsref/dom_obj_style.asp#layout)
- [列表](http://www.w3school.com.cn/jsref/dom_obj_style.asp#list)
- [杂项](http://www.w3school.com.cn/jsref/dom_obj_style.asp#misc)
- [定位](http://www.w3school.com.cn/jsref/dom_obj_style.asp#positioning)
- [打印](http://www.w3school.com.cn/jsref/dom_obj_style.asp#printing)
- [滚动条](http://www.w3school.com.cn/jsref/dom_obj_style.asp#scrollbar)
- [表格](http://www.w3school.com.cn/jsref/dom_obj_style.asp#table)
- [文本](http://www.w3school.com.cn/jsref/dom_obj_style.asp#text)
- [规范](http://www.w3school.com.cn/jsref/dom_obj_style.asp#std)

### Background 属性

| 属性                                                         | 描述                              |
| ------------------------------------------------------------ | --------------------------------- |
| [background](http://www.w3school.com.cn/jsref/prop_style_background.asp) | 在一行中设置所有的背景属性        |
| [backgroundAttachment](http://www.w3school.com.cn/jsref/prop_style_backgroundattachment.asp) | 设置背景图像是否固定或随页面滚动  |
| [backgroundColor](http://www.w3school.com.cn/jsref/prop_style_backgroundcolor.asp) | 设置元素的背景颜色                |
| [backgroundImage](http://www.w3school.com.cn/jsref/prop_style_backgroundimage.asp) | 设置元素的背景图像                |
| [backgroundPosition](http://www.w3school.com.cn/jsref/prop_style_backgroundposition.asp) | 设置背景图像的起始位置            |
| [backgroundPositionX](http://www.w3school.com.cn/jsref/prop_style_backgroundpositionx.asp) | 设置backgroundPosition属性的X坐标 |
| [backgroundPositionY](http://www.w3school.com.cn/jsref/prop_style_backgroundpositiony.asp) | 设置backgroundPosition属性的Y坐标 |
| [backgroundRepeat](http://www.w3school.com.cn/jsref/prop_style_backgroundrepeat.asp) | 设置是否及如何重复背景图像        |

### Border 和 Margin 属性

| 属性                                                         | 描述                                    |
| ------------------------------------------------------------ | --------------------------------------- |
| [border](http://www.w3school.com.cn/jsref/prop_style_border.asp) | 在一行设置四个边框的所有属性            |
| [borderBottom](http://www.w3school.com.cn/jsref/prop_style_borderbottom.asp) | 在一行设置底边框的所有属性              |
| [borderBottomColor](http://www.w3school.com.cn/jsref/prop_style_borderbottomcolor.asp) | 设置底边框的颜色                        |
| [borderBottomStyle](http://www.w3school.com.cn/jsref/prop_style_borderbottomstyle.asp) | 设置底边框的样式                        |
| [borderBottomWidth](http://www.w3school.com.cn/jsref/prop_style_borderbottomwidth.asp) | 设置底边框的宽度                        |
| [borderColor](http://www.w3school.com.cn/jsref/prop_style_bordercolor.asp) | 设置所有四个边框的颜色 (可设置四种颜色) |
| [borderLeft](http://www.w3school.com.cn/jsref/prop_style_borderleft.asp) | 在一行设置左边框的所有属性              |
| [borderLeftColor](http://www.w3school.com.cn/jsref/prop_style_borderleftcolor.asp) | 设置左边框的颜色                        |
| [borderLeftStyle](http://www.w3school.com.cn/jsref/prop_style_borderleftstyle.asp) | 设置左边框的样式                        |
| [borderLeftWidth](http://www.w3school.com.cn/jsref/prop_style_borderleftwidth.asp) | 设置左边框的宽度                        |
| [borderRight](http://www.w3school.com.cn/jsref/prop_style_borderright.asp) | 在一行设置右边框的所有属性              |
| [borderRightColor](http://www.w3school.com.cn/jsref/prop_style_borderrightcolor.asp) | 设置右边框的颜色                        |
| [borderRightStyle](http://www.w3school.com.cn/jsref/prop_style_borderrightstyle.asp) | 设置右边框的样式                        |
| [borderRightWidth](http://www.w3school.com.cn/jsref/prop_style_borderrightwidth.asp) | 设置右边框的宽度                        |
| [borderStyle](http://www.w3school.com.cn/jsref/prop_style_borderstyle.asp) | 设置所有四个边框的样式 (可设置四种样式) |
| [borderTop](http://www.w3school.com.cn/jsref/prop_style_bordertop.asp) | 在一行设置顶边框的所有属性              |
| [borderTopColor](http://www.w3school.com.cn/jsref/prop_style_bordertopcolor.asp) | 设置顶边框的颜色                        |
| [borderTopStyle](http://www.w3school.com.cn/jsref/prop_style_bordertopstyle.asp) | 设置顶边框的样式                        |
| [borderTopWidth](http://www.w3school.com.cn/jsref/prop_style_bordertopwidth.asp) | 设置顶边框的宽度                        |
| [borderWidth](http://www.w3school.com.cn/jsref/prop_style_borderwidth.asp) | 设置所有四条边框的宽度 (可设置四种宽度) |
| [margin](http://www.w3school.com.cn/jsref/prop_style_margin.asp) | 设置元素的边距 (可设置四个值)           |
| [marginBottom](http://www.w3school.com.cn/jsref/prop_style_marginbottom.asp) | 设置元素的底边距                        |
| [marginLeft](http://www.w3school.com.cn/jsref/prop_style_marginleft.asp) | 设置元素的左边距                        |
| [marginRight](http://www.w3school.com.cn/jsref/prop_style_marginright.asp) | 设置元素的右边据                        |
| [marginTop](http://www.w3school.com.cn/jsref/prop_style_margintop.asp) | 设置元素的顶边距                        |
| [outline](http://www.w3school.com.cn/jsref/prop_style_outline.asp) | 在一行设置所有的outline属性             |
| [outlineColor](http://www.w3school.com.cn/jsref/prop_style_outlinecolor.asp) | 设置围绕元素的轮廓颜色                  |
| [outlineStyle](http://www.w3school.com.cn/jsref/prop_style_outlinestyle.asp) | 设置围绕元素的轮廓样式                  |
| [outlineWidth](http://www.w3school.com.cn/jsref/prop_style_outlinewidth.asp) | 设置围绕元素的轮廓宽度                  |
| [padding](http://www.w3school.com.cn/jsref/prop_style_padding.asp) | 设置元素的填充 (可设置四个值)           |
| [paddingBottom](http://www.w3school.com.cn/jsref/prop_style_paddingbottom.asp) | 设置元素的下填充                        |
| [paddingLeft](http://www.w3school.com.cn/jsref/prop_style_paddingleft.asp) | 设置元素的左填充                        |
| [paddingRight](http://www.w3school.com.cn/jsref/prop_style_paddingright.asp) | 设置元素的右填充                        |
| [paddingTop](http://www.w3school.com.cn/jsref/prop_style_paddingtop.asp) | 设置元素的顶填充                        |

### Layout 属性

| 属性                                                         | 描述                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| [clear](http://www.w3school.com.cn/jsref/prop_style_clear.asp) | 设置在元素的哪边不允许其他的浮动元素                         |
| [clip](http://www.w3school.com.cn/jsref/prop_style_clip.asp) | 设置元素的形状                                               |
| [content](http://www.w3school.com.cn/jsref/prop_style_content.asp) | 设置元信息                                                   |
| counterIncrement                                             | 设置其后是正数的计数器名称的列表。其中整数指示每当元素出现时计数器的增量。默认是1。 |
| counterReset                                                 | 设置其后是正数的计数器名称的列表。其中整数指示每当元素出现时计数器被设置的值。默认是0。 |
| [cssFloat](http://www.w3school.com.cn/jsref/prop_style_cssfloat.asp) | 设置图像或文本将出现（浮动）在另一元素中的何处。             |
| [cursor](http://www.w3school.com.cn/jsref/prop_style_cursor.asp) | 设置显示的指针类型                                           |
| [direction](http://www.w3school.com.cn/jsref/prop_style_direction.asp) | 设置元素的文本方向                                           |
| [display](http://www.w3school.com.cn/jsref/prop_style_display.asp) | 设置元素如何被显示                                           |
| [height](http://www.w3school.com.cn/jsref/prop_style_height.asp) | 设置元素的高度                                               |
| markerOffset                                                 | 设置marker box的principal box距离其最近的边框边缘的距离      |
| marks                                                        | 设置是否cross marks或crop marks应仅仅被呈现于page box边缘之外 |
| [maxHeight](http://www.w3school.com.cn/jsref/prop_style_maxheight.asp) | 设置元素的最大高度                                           |
| [maxWidth](http://www.w3school.com.cn/jsref/prop_style_maxwidth.asp) | 设置元素的最大宽度                                           |
| [minHeight](http://www.w3school.com.cn/jsref/prop_style_minheight.asp) | 设置元素的最小高度                                           |
| [minWidth](http://www.w3school.com.cn/jsref/prop_style_minwidth.asp) | 设置元素的最小宽度                                           |
| [overflow](http://www.w3school.com.cn/jsref/prop_style_overflow.asp) | 规定如何处理不适合元素盒的内容                               |
| [verticalAlign](http://www.w3school.com.cn/jsref/prop_style_verticalalign.asp) | 设置对元素中的内容进行垂直排列                               |
| [visibility](http://www.w3school.com.cn/jsref/prop_style_visibility.asp) | 设置元素是否可见                                             |
| [width](http://www.w3school.com.cn/jsref/prop_style_width.asp) | 设置元素的宽度                                               |

### List 属性

| 属性                                                         | 描述                     |
| ------------------------------------------------------------ | ------------------------ |
| [listStyle](http://www.w3school.com.cn/jsref/prop_style_liststyle.asp) | 在一行设置列表的所有属性 |
| [listStyleImage](http://www.w3school.com.cn/jsref/prop_style_liststyleimage.asp) | 把图像设置为列表项标记   |
| [listStylePosition](http://www.w3school.com.cn/jsref/prop_style_liststyleposition.asp) | 改变列表项标记的位置     |
| [listStyleType](http://www.w3school.com.cn/jsref/prop_style_liststyletype.asp) | 设置列表项标记的类型     |

### Positioning 属性

| 属性                                                         | 描述                                                   |
| ------------------------------------------------------------ | ------------------------------------------------------ |
| [bottom](http://www.w3school.com.cn/jsref/prop_style_bottom.asp) | 设置元素的底边缘距离父元素底边缘的之上或之下的距离     |
| [left](http://www.w3school.com.cn/jsref/prop_style_left.asp) | 置元素的左边缘距离父元素左边缘的左边或右边的距离       |
| [position](http://www.w3school.com.cn/jsref/prop_style_position.asp) | 把元素放置在static, relative, absolute 或 fixed 的位置 |
| [right](http://www.w3school.com.cn/jsref/prop_style_right.asp) | 置元素的右边缘距离父元素右边缘的左边或右边的距离       |
| [top](http://www.w3school.com.cn/jsref/prop_style_top.asp)   | 设置元素的顶边缘距离父元素顶边缘的之上或之下的距离     |
| [zIndex](http://www.w3school.com.cn/jsref/prop_style_zindex.asp) | 设置元素的堆叠次序                                     |

### Printing 属性

| 属性                                                         | 描述                               |
| ------------------------------------------------------------ | ---------------------------------- |
| orphans                                                      | 设置段落留到页面底部的最小行数     |
| page                                                         | 设置显示某元素时使用的页面类型     |
| [pageBreakAfter](http://www.w3school.com.cn/jsref/prop_style_pagebreakafter.asp) | 设置某元素之后的分页行为           |
| [pageBreakBefore](http://www.w3school.com.cn/jsref/prop_style_pagebreakbefore.asp) | 设置某元素之前的分页行为           |
| [pageBreakInside](http://www.w3school.com.cn/jsref/prop_style_pagebreakinside.asp) | 设置某元素内部的分页行为           |
| size                                                         | 设置页面的方向和尺寸               |
| widows                                                       | 设置段落必须留到页面顶部的最小行数 |

### Scrollbar 属性 (IE-only)

| 属性                                                         | 描述                                               |
| ------------------------------------------------------------ | -------------------------------------------------- |
| [scrollbar3dLightColor](http://www.w3school.com.cn/jsref/prop_style_scrollbar3dlightcolor.asp) | 设置箭头和滚动条左侧和顶边的颜色                   |
| [scrollbarArrowColor](http://www.w3school.com.cn/jsref/prop_style_scrollbararrowcolor.asp) | 设置滚动条上的箭头颜色                             |
| [scrollbarBaseColor](http://www.w3school.com.cn/jsref/prop_style_scrollbarbasecolor.asp) | 设置滚动条的底色                                   |
| [scrollbarDarkShadowColor](http://www.w3school.com.cn/jsref/prop_style_scrollbardarkshadowcolor.asp) | 设置箭头和滚动条右侧和底边的颜色                   |
| [scrollbarFaceColor](http://www.w3school.com.cn/jsref/prop_style_scrollbarfacecolor.asp) | 设置滚动条的表色                                   |
| [scrollbarHighlightColor](http://www.w3school.com.cn/jsref/prop_style_scrollbarhighlightcolor.asp) | 设置箭头和滚动条左侧和顶边的颜色，以及滚动条的背景 |
| [scrollbarShadowColor](http://www.w3school.com.cn/jsref/prop_style_scrollbarshadowcolor.asp) | 设置箭头和滚动条右侧和底边的颜色                   |
| [scrollbarTrackColor](http://www.w3school.com.cn/jsref/prop_style_scrollbartrackcolor.asp) | 设置滚动条的背景色                                 |

### Table 属性

| 属性                                                         | 描述                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| [borderCollapse](http://www.w3school.com.cn/jsref/prop_style_bordercollapse.asp) | 设置表格边框是否合并为单边框，或者像在标准的HTML中那样分离。 |
| [borderSpacing](http://www.w3school.com.cn/jsref/prop_style_borderspacing.asp) | 设置分隔单元格边框的距离                                     |
| [captionSide](http://www.w3school.com.cn/jsref/prop_style_captionside.asp) | 设置表格标题的位置                                           |
| [emptyCells](http://www.w3school.com.cn/jsref/prop_style_emptycells.asp) | 设置是否显示表格中的空单元格                                 |
| [tableLayout](http://www.w3school.com.cn/jsref/prop_style_tablelayout.asp) | 设置用来显示表格单元格、行以及列的算法                       |

### Text 属性

| 属性                                                         | 描述                             |
| ------------------------------------------------------------ | -------------------------------- |
| [color](http://www.w3school.com.cn/jsref/prop_style_color.asp) | 设置文本的颜色                   |
| [font](http://www.w3school.com.cn/jsref/prop_style_font.asp) | 在一行设置所有的字体属性         |
| [fontFamily](http://www.w3school.com.cn/jsref/prop_style_fontfamily.asp) | 设置元素的字体系列。             |
| [fontSize](http://www.w3school.com.cn/jsref/prop_style_fontsize.asp) | 设置元素的字体大小。             |
| [fontSizeAdjust](http://www.w3school.com.cn/jsref/prop_style_fontsizeadjust.asp) | 设置/调整文本的尺寸              |
| [fontStretch](http://www.w3school.com.cn/jsref/prop_style_fontstretch.asp) | 设置如何紧缩或伸展字体           |
| [fontStyle](http://www.w3school.com.cn/jsref/prop_style_fontstyle.asp) | 设置元素的字体样式               |
| [fontVariant](http://www.w3school.com.cn/jsref/prop_style_fontvariant.asp) | 用小型大写字母字体来显示文本     |
| [fontWeight](http://www.w3school.com.cn/jsref/prop_style_fontweight.asp) | 设置字体的粗细                   |
| [letterSpacing](http://www.w3school.com.cn/jsref/prop_style_letterspacing.asp) | 设置字符间距                     |
| [lineHeight](http://www.w3school.com.cn/jsref/prop_style_lineheight.asp) | 设置行间距                       |
| [quotes](http://www.w3school.com.cn/jsref/prop_style_quotes.asp) | 设置在文本中使用哪种引号         |
| [textAlign](http://www.w3school.com.cn/jsref/prop_style_textalign.asp) | 排列文本                         |
| [textDecoration](http://www.w3school.com.cn/jsref/prop_style_textdecoration.asp) | 设置文本的修饰                   |
| [textIndent](http://www.w3school.com.cn/jsref/prop_style_textindent.asp) | 缩紧首行的文本                   |
| textShadow                                                   | 设置文本的阴影效果               |
| [textTransform](http://www.w3school.com.cn/jsref/prop_style_texttransform.asp) | 对文本设置大写效果               |
| unicodeBidi                                                  |                                  |
| [whiteSpace](http://www.w3school.com.cn/jsref/prop_style_whitespace.asp) | 设置如何设置文本中的折行和空白符 |
| [wordSpacing](http://www.w3school.com.cn/jsref/prop_style_wordspacing.asp) | 设置文本中的词间距               |

### 标准属性

| 属性                                                     | 描述                         |
| -------------------------------------------------------- | ---------------------------- |
| [dir](http://www.w3school.com.cn/jsref/prop_dir.asp)     | 设置或返回文本的方向         |
| [lang](http://www.w3school.com.cn/jsref/prop_lang.asp)   | 设置或返回元素的语言代码     |
| [title](http://www.w3school.com.cn/jsref/prop_title.asp) | 设置或返回元素的咨询性的标题 |

### cssText 属性

它是一组样式属性及其值的文本表示。这个文本格式化为一个 CSS 样式表，去掉了包围属性和值的元素选择器的花括号。

将这一属性设置为非法的值将会抛出一个代码为 SYNTAX_ERR 的 [DOMException 异常](http://www.w3school.com.cn/xmldom/dom_domexception.asp)。当 CSS2Properties 对象是只读的时候，试图设置这一属性将会抛出一个代码为 NO_MODIFICATION_ALLOWED_ERR 的 [DOMException 异常](http://www.w3school.com.cn/xmldom/dom_domexception.asp)。

## 关于 CSS2Properties 对象

CSS2Properties 对象表示一组 CSS 样式属性及其值。它为 CSS 规范定义的每一个 CSS 属性都定义一个 JavaScript 属性。

一个 HTMLElement 的 style 属性是一个可读可写的 CSS2Properties 对象，就好像 CSSRule 对象的 style 属性一样。不过，Window.getComputedStyle() 的返回值是一个 CSS2Properties 对象，其属性是只读的。

# DOM Event 对象

## 实例

[哪个鼠标按钮被点击？](http://www.w3school.com.cn/tiy/t.asp?f=hdom_event_button)

 

[光标的坐标是？](http://www.w3school.com.cn/tiy/t.asp?f=hdom_event_clientx)

 

[被按的按键的 unicode 是？](http://www.w3school.com.cn/tiy/t.asp?f=hdom_event_keycode)

 

[相对于屏幕，光标的坐标是？](http://www.w3school.com.cn/tiy/t.asp?f=hdom_event_screenxy)

 

[shift 键被按了吗？](http://www.w3school.com.cn/tiy/t.asp?f=hdom_event_shiftkey)

 

[哪个元素被点击了？](http://www.w3school.com.cn/tiy/t.asp?f=hdom_event_srcelement)

 

[哪个事件类型发生了？](http://www.w3school.com.cn/tiy/t.asp?f=hdom_event_type)

## Event 对象

Event 对象代表事件的状态，比如事件在其中发生的元素、键盘按键的状态、鼠标的位置、鼠标按钮的状态。

事件通常与函数结合使用，函数不会在事件发生前被执行！

## 事件句柄　(Event Handlers)

HTML 4.0 的新特性之一是能够使 HTML 事件触发浏览器中的行为，比如当用户点击某个 HTML 元素时启动一段 JavaScript。下面是一个属性列表，可将之插入 HTML 标签以定义事件的行为。

| 属性                                                         | 此事件发生在何时...                  |
| ------------------------------------------------------------ | ------------------------------------ |
| [onabort](http://www.w3school.com.cn/jsref/event_onabort.asp) | 图像的加载被中断。                   |
| [onblur](http://www.w3school.com.cn/jsref/event_onblur.asp)  | 元素失去焦点。                       |
| [onchange](http://www.w3school.com.cn/jsref/event_onchange.asp) | 域的内容被改变。                     |
| [onclick](http://www.w3school.com.cn/jsref/event_onclick.asp) | 当用户点击某个对象时调用的事件句柄。 |
| [ondblclick](http://www.w3school.com.cn/jsref/event_ondblclick.asp) | 当用户双击某个对象时调用的事件句柄。 |
| [onerror](http://www.w3school.com.cn/jsref/event_onerror.asp) | 在加载文档或图像时发生错误。         |
| [onfocus](http://www.w3school.com.cn/jsref/event_onfocus.asp) | 元素获得焦点。                       |
| [onkeydown](http://www.w3school.com.cn/jsref/event_onkeydown.asp) | 某个键盘按键被按下。                 |
| [onkeypress](http://www.w3school.com.cn/jsref/event_onkeypress.asp) | 某个键盘按键被按下并松开。           |
| [onkeyup](http://www.w3school.com.cn/jsref/event_onkeyup.asp) | 某个键盘按键被松开。                 |
| [onload](http://www.w3school.com.cn/jsref/event_onload.asp)  | 一张页面或一幅图像完成加载。         |
| [onmousedown](http://www.w3school.com.cn/jsref/event_onmousedown.asp) | 鼠标按钮被按下。                     |
| [onmousemove](http://www.w3school.com.cn/jsref/event_onmousemove.asp) | 鼠标被移动。                         |
| [onmouseout](http://www.w3school.com.cn/jsref/event_onmouseout.asp) | 鼠标从某元素移开。                   |
| [onmouseover](http://www.w3school.com.cn/jsref/event_onmouseover.asp) | 鼠标移到某元素之上。                 |
| [onmouseup](http://www.w3school.com.cn/jsref/event_onmouseup.asp) | 鼠标按键被松开。                     |
| [onreset](http://www.w3school.com.cn/jsref/event_onreset.asp) | 重置按钮被点击。                     |
| [onresize](http://www.w3school.com.cn/jsref/event_onresize.asp) | 窗口或框架被重新调整大小。           |
| [onselect](http://www.w3school.com.cn/jsref/event_onselect.asp) | 文本被选中。                         |
| [onsubmit](http://www.w3school.com.cn/jsref/event_onsubmit.asp) | 确认按钮被点击。                     |
| [onunload](http://www.w3school.com.cn/jsref/event_onunload.asp) | 用户退出页面。                       |

## 鼠标 / 键盘属性

| 属性                                                         | 描述                                         |
| ------------------------------------------------------------ | -------------------------------------------- |
| [altKey](http://www.w3school.com.cn/jsref/event_altkey.asp)  | 返回当事件被触发时，"ALT" 是否被按下。       |
| [button](http://www.w3school.com.cn/jsref/event_button.asp)  | 返回当事件被触发时，哪个鼠标按钮被点击。     |
| [clientX](http://www.w3school.com.cn/jsref/event_clientx.asp) | 返回当事件被触发时，鼠标指针的水平坐标。     |
| [clientY](http://www.w3school.com.cn/jsref/event_clienty.asp) | 返回当事件被触发时，鼠标指针的垂直坐标。     |
| [ctrlKey](http://www.w3school.com.cn/jsref/event_ctrlkey.asp) | 返回当事件被触发时，"CTRL" 键是否被按下。    |
| [metaKey](http://www.w3school.com.cn/jsref/event_metakey.asp) | 返回当事件被触发时，"meta" 键是否被按下。    |
| [relatedTarget](http://www.w3school.com.cn/jsref/event_relatedtarget.asp) | 返回与事件的目标节点相关的节点。             |
| [screenX](http://www.w3school.com.cn/jsref/event_screenx.asp) | 返回当某个事件被触发时，鼠标指针的水平坐标。 |
| [screenY](http://www.w3school.com.cn/jsref/event_screeny.asp) | 返回当某个事件被触发时，鼠标指针的垂直坐标。 |
| [shiftKey](http://www.w3school.com.cn/jsref/event_shiftkey.asp) | 返回当事件被触发时，"SHIFT" 键是否被按下。   |

## IE 属性

除了上面的鼠标/事件属性，IE 浏览器还支持下面的属性：

| 属性            | 描述                                                         |
| --------------- | ------------------------------------------------------------ |
| cancelBubble    | 如果事件句柄想阻止事件传播到包容对象，必须把该属性设为 true。 |
| fromElement     | 对于 mouseover 和 mouseout 事件，fromElement 引用移出鼠标的元素。 |
| keyCode         | 对于 keypress 事件，该属性声明了被敲击的键生成的 Unicode 字符码。对于 keydown 和 keyup 事件，它指定了被敲击的键的虚拟键盘码。虚拟键盘码可能和使用的键盘的布局相关。 |
| offsetX,offsetY | 发生事件的地点在事件源元素的坐标系统中的 x 坐标和 y 坐标。   |
| returnValue     | 如果设置了该属性，它的值比事件句柄的返回值优先级高。把这个属性设置为 fasle，可以取消发生事件的源元素的默认动作。 |
| srcElement      | 对于生成事件的 Window 对象、Document 对象或 Element 对象的引用。 |
| toElement       | 对于 mouseover 和 mouseout 事件，该属性引用移入鼠标的元素。  |
| x,y             | 事件发生的位置的 x 坐标和 y 坐标，它们相对于用CSS动态定位的最内层包容元素。 |

## 标准 Event 属性

下面列出了 2 级 DOM 事件标准定义的属性。

| 属性                                                         | 描述                                           |
| ------------------------------------------------------------ | ---------------------------------------------- |
| [bubbles](http://www.w3school.com.cn/jsref/event_bubbles.asp) | 返回布尔值，指示事件是否是起泡事件类型。       |
| [cancelable](http://www.w3school.com.cn/jsref/event_cancelable.asp) | 返回布尔值，指示事件是否可拥可取消的默认动作。 |
| [currentTarget](http://www.w3school.com.cn/jsref/event_currenttarget.asp) | 返回其事件监听器触发该事件的元素。             |
| [eventPhase](http://www.w3school.com.cn/jsref/event_eventphase.asp) | 返回事件传播的当前阶段。                       |
| [target](http://www.w3school.com.cn/jsref/event_target.asp)  | 返回触发此事件的元素（事件的目标节点）。       |
| [timeStamp](http://www.w3school.com.cn/jsref/event_timestamp.asp) | 返回事件生成的日期和时间。                     |
| [type](http://www.w3school.com.cn/jsref/event_type.asp)      | 返回当前 Event 对象表示的事件的名称。          |

## 标准 Event 方法

下面列出了 2 级 DOM 事件标准定义的方法。IE 的事件模型不支持这些方法：

| 方法                                                         | 描述                                     |
| ------------------------------------------------------------ | ---------------------------------------- |
| [initEvent()](http://www.w3school.com.cn/jsref/event_initevent.asp) | 初始化新创建的 Event 对象的属性。        |
| [preventDefault()](http://www.w3school.com.cn/jsref/event_preventdefault.asp) | 通知浏览器不要执行与事件关联的默认动作。 |
| [stopPropagation()](http://www.w3school.com.cn/jsref/event_stoppropagation.asp) | 不再派发事件。                           |

# HTML DOM 总结

本教程已经向您讲解了如何使用 HTML DOM 来增强网站的动态交互性。

您已经学会了如何操作 HTML 元素以响应不同的场景。

如需更多有关 HTML DOM 的信息，请访问我们的 [HTML DOM 实例](http://www.w3school.com.cn/example/hdom_examples.asp)和 [HTML DOM 参考手册](http://www.w3school.com.cn/jsref/index.asp)。

## 现在您已经学习了 HTML DOM，下一步呢？

在本教程中，我们已通过在客户端（在浏览器中）使用脚本来创建动态网页。

也可以通过在服务器上使用脚本来增加网页的动态性。

通过服务器端脚本，您能够编辑、添加或更改网页内容。您能够对提交自 HTML 表单的数据做出响应，访问数据或数据库，并向浏览器返回结果，为不同的用户定制页面。

在 W3School，您可以学习以下服务器端脚本教程：

[PHP 教程](http://www.w3school.com.cn/php/index.asp)

[ASP 教程](http://www.w3school.com.cn/asp/index.asp)

[.NET 教程](http://www.w3school.com.cn/aspnet/index.asp)

您也可以通过我们的服务器端脚本系列教程页面，快速了解各种不同的服务器端脚本技术。