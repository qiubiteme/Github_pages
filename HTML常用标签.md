# HTML常用标签及属性

## HTML标签

### 标题 h

HTML 标题（Heading）是通过 <h1> - <h6> 等标签进行定义的。

**标题很重要**

请确保将 HTML heading 标签只用于标题。不要仅仅是为了产生粗体或大号的文本而使用标题。

搜索引擎使用标题为您的网页的结构和内容编制索引。

因为用户可以通过标题来快速浏览您的网页，所以用标题来呈现文档结构是很重要的。

应该将 h1 用作主标题（最重要的），其后是 h2（次重要的），再其次是 h3，以此类推。

### 水平线 hr

<hr /> 标签在 HTML 页面中创建水平线。

hr 元素可用于分隔内容。

### 注释

可以将注释插入 HTML 代码中，这样可以提高其可读性，使代码更易被人理解。浏览器会忽略注释，也不会显示它们。

注释是这样写的：

```
<!-- 注释内容 -->
```

在开始标签中有一个惊叹号，但是结束标签中没有。

浏览器不会显示注释，但是能够帮助记录您的 HTML 文档。

### 条件注释

您也许会在 HTML 中偶尔发现条件注释：

```
<!--[if IE 8]>
    .... some HTML here ....
<![endif]-->
```

条件注释定义只有 Internet Explorer 8 执行的 HTML 标签。

### 段落 p

HTML 段落是通过 <p> 标签进行定义的。

### 换行 br

如果您希望在不产生一个新段落的情况下进行换行（新行），请使用 <br /> 标签：

### 链接 a

HTML 链接是通过 <a> 标签进行定义的。

1. 通过使用 href 属性 - 创建指向的链接

2. 通过使用 name 属性 - 创建文档内的书签,俗称锚点

   ```
   <h1>顶部</h1>
   <a href="#top" >锚点,回到顶部</a>
   ```

3. 使用 Target 属性，你可以定义被链接的文档打开方式。

   ```
   blank        在新窗口中打开被链接文档。         
   _self        默认。在相同的框架中打开被链接文档。 
   _parent      在父框架集中打开被链接文档。         
   _top         在整个窗口中打开被链接文档。         
   framename  在指定的框架中打开被链接文档。       
   ```



### 图像 img

HTML 图像是通过 <img> 标签进行定义的。

```
<img src="url" />
```

**src** 图像路径

**alt ** 替换文本

**align ** 对齐方式

| 标签                                                   | 描述                         |
| ------------------------------------------------------ | ---------------------------- |
| [<img>](http://www.w3school.com.cn/tags/tag_img.asp)   | 定义图像。                   |
| [<map>](http://www.w3school.com.cn/tags/tag_map.asp)   | 定义图像地图。               |
| [<area>](http://www.w3school.com.cn/tags/tag_area.asp) | 定义图像地图中的可点击区域。 |

### 表格tab

表格由 <table> 标签来定义。每个表格均有若干行（由 <tr> 标签定义），每行被分割为若干单元格（由 <td> 标签定义）。字母 td 指表格数据（table data），即数据单元格的内容。数据单元格可以包含文本、图片、列表、段落、表单、水平线、表格等等。

```

<table border="1">
    <caption>课程表</caption>
    <tr>
        <th>&nbsp;</th>
        <th>星期一</th>
        <th>星期二</th>
        <th>星期三</th>
        <th>星期四</th>
        <th>星期五</th>
        <th>星期六</th>
        <th>星期天</th>
    </tr>
    <tr>
        <td rowspan="2">上午/下午</td>
        <td>上班</td>
        <td>上班</td>
        <td>上班</td>
        <td>上班</td>
        <td>上班</td>
        <td colspan="2">休息</td>
    </tr>
    <tr>
        <td>上班</td>
        <td>上班</td>
        <td>上班</td>
        <td>上班</td>
        <td>上班</td>
        <td colspan="2">休息</td>
    </tr>
</table>
```

**表格标签**

| 表格     | 描述                                                     |
| -------- | -------------------------------------------------------- |
| tab      | 定义表格                                                 |
| caption  | 定义表格标题。                                           |
| th       | 定义表格的表头。大多数浏览器会把表头显示为粗体居中的文本 |
| tr       | 定义表格的行。                                           |
| td       | 定义表格单元。                                           |
| thead    | 定义表格的页眉。                                         |
| tbody    | 定义表格的主体。                                         |
| tfoot    | 定义表格的页脚。                                         |
| col      | 定义用于表格列的属性。                                   |
| colgroup | 定义表格列的组。                                         |

**表格中的空单元格**

使用字符实体,空格占位符 

**跨行或跨列的表格单元格**

属性 : colspan 跨行

	    rowspan 跨列

### 有序、无序和自定义列表

#### 无序列表

无序列表是一个项目的列表，此列项目使用粗体圆点（典型的小黑圆圈）进行标记。

无序列表始于 <ul> 标签。每个列表项始于 <li>。

**无序列表通过type定义列表前的符号 :** 

**disc**  实心圆点  

**circle**空心圆点 

 **square** 实心小方块

```
<ul type="disc">
     <li>苹果</li>
     <li>香蕉</li>
     <li>柠檬</li>
     <li>桔子</li>
</ul> 
```

列表项内部可以使用段落、换行符、图片、链接以及其他列表等等。

#### 有序列表

同样，有序列表也是一列项目，列表项目使用数字进行标记。

有序列表始于 <ol> 标签。每个列表项始于 <li> 标签。

**无序列表通过type定义列表前的符号 :** 

**默认**  数字列表

**A**  大写字母列表：

**a ** 小写字母列表：

**I**  大写罗马字母列表：

**i**  小写罗马字母列表：

```
<ol>
 <li>苹果</li>
 <li>香蕉</li>
 <li>柠檬</li>
 <li>桔子</li>
</ol>  
```

列表项内部可以使用段落、换行符、图片、链接以及其他列表等等。

#### 自定义列表

自定义列表不仅仅是一列项目，而是项目及其注释的组合。

自定义列表以 <dl> 标签开始。每个自定义列表项以 <dt> 开始。每个自定义列表项的定义以 <dd> 开始。

```
<dl>
   <dt>计算机</dt>
   <dd>用来计算的仪器 ... ...</dd>
   <dt>显示器</dt>
   <dd>以视觉方式显示信息的装置 ... ...</dd>
</dl>
```

定义列表的列表项内部可以使用段落、换行符、图片、链接以及其他列表等等。

### 块级元素

#### HTML 块元素

大多数 HTML 元素被定义为块级元素或内联元素。

编者注：“块级元素”译为 block level element，“内联元素”译为 inline element。

块级元素在浏览器显示时，通常会以新行来开始（和结束）。

例子：<h1>, <p>, <ul>, <table>

#### HTML 内联元素

内联元素在显示时通常不会以新行开始。

例子：<b>, <td>, <a>, <img>

#### div 元素

HTML <div> 元素是块级元素，它是可用于组合其他 HTML 元素的容器。

<div> 元素没有特定的含义。除此之外，由于它属于块级元素，浏览器会在其前后显示折行。

如果与 CSS 一同使用，<div> 元素可用于对大的内容块设置样式属性。

<div> 元素的另一个常见的用途是文档布局

#### span 元素

HTML <span> 元素是内联元素，可用作文本的容器。

<span> 元素也没有特定的含义。

当与 CSS 一同使用时，<span> 元素可用于为部分文本设置样式属性。

## HTML 与CSS样式表

**外部样式表**

当样式需要被应用到很多页面的时候，外部样式表将是理想的选择。使用外部样式表，你就可以通过更改一个文件来改变整个站点的外观

```
<link rel="stylesheet" href="css/base.css">
```

**内部样式表**

当单个文件需要特别样式时，就可以使用内部样式表。你可以在 head 部分通过 <style> 标签定义内部样式表。

```
<style type="text/css">
    body {background-color: red}
    p {margin-left: 20px}
</style>
```

**内联样式**

当特殊的样式需要应用到个别元素时，就可以使用内联样式。 使用内联样式的方法是在相关的标签中使用样式属性。样式属性可以包含任何 CSS 属性。以下实例显示出如何改变段落的颜色和左外边距。

```
<p style="color: red; margin-left: 20px">
This is a paragraph
</p>
```

## HTML 文本格式化标签

## 文本格式化标签

| 标签                                                         | 描述                                  |
| ------------------------------------------------------------ | ------------------------------------- |
| [<b>](http://www.w3school.com.cn/tags/tag_font_style.asp)    | 定义粗体文本。                        |
| [<big>](http://www.w3school.com.cn/tags/tag_font_style.asp)  | 定义大号字。                          |
| [<em>](http://www.w3school.com.cn/tags/tag_phrase_elements.asp) | 定义着重文字。                        |
| [<i>](http://www.w3school.com.cn/tags/tag_font_style.asp)    | 定义斜体字。                          |
| [<small>](http://www.w3school.com.cn/tags/tag_font_style.asp) | 定义小号字。                          |
| [<strong>](http://www.w3school.com.cn/tags/tag_phrase_elements.asp) | 定义加重语气。                        |
| [<sub>](http://www.w3school.com.cn/tags/tag_sup.asp)              | 定义下标字。                          |
| [<sup>](http://www.w3school.com.cn/tags/tag_sup.asp)              | 定义上标字。                          |
| [<ins>](http://www.w3school.com.cn/tags/tag_ins.asp)              | 定义插入字。                          |
| [<del>](http://www.w3school.com.cn/tags/tag_del.asp)              | 定义删除字。                          |
| [<s>](http://www.w3school.com.cn/tags/tag_strike.asp)           | *不赞成使用。*使用 <del> 代替。       |
| [<strike>](http://www.w3school.com.cn/tags/tag_strike.asp)           | *不赞成使用。*使用 <del> 代替。       |
| [<u>](http://www.w3school.com.cn/tags/tag_u.asp)                | *不赞成使用。*使用样式（style）代替。 |

## “计算机输出”标签

| 标签                                                        | 描述                            |
| ----------------------------------------------------------- | ------------------------------- |
| [<code>](http://www.w3school.com.cn/tags/tag_phrase_elements.asp) | 定义计算机代码。                |
| [<kbd>](http://www.w3school.com.cn/tags/tag_phrase_elements.asp) | 定义键盘码。                    |
| [<samp>](http://www.w3school.com.cn/tags/tag_phrase_elements.asp) | 定义计算机代码样本。            |
| [<tt>](http://www.w3school.com.cn/tags/tag_font_style.asp)      | 定义打字机代码。                |
| [<var>](http://www.w3school.com.cn/tags/tag_phrase_elements.asp) | 定义变量。                      |
| [<pre>](http://www.w3school.com.cn/tags/tag_pre.asp)             | 定义预格式文本。                |
| <listing>                                                   | *不赞成使用。*使用 <pre> 代替。 |
| <plaintext>                                                 | *不赞成使用。*使用 <pre> 代替。 |
| <xmp>                                                       | *不赞成使用。*使用 <pre> 代替。 |

## HTML 引文、引用和定义元素

| 标签         | 描述                             |
| ------------ | -------------------------------- |
| <abbr>       | 定义缩写或首字母缩略语。         |
| <address>    | 定义文档作者或拥有者的联系信息。 |
| <bdo>        | 定义文本方向。                   |
| <blockquote> | 定义从其他来源引用的节。         |
| <dfn>        | 定义项目或缩略词的定义。         |
| <q>          | 定义短的行内引用。               |
| <cite>       | 定义著作的标题。                 |

## HTML 属性

HTML 标签可以拥有*属性*。属性提供了有关 HTML 元素的*更多的信息*。

属性总是以名称/值对的形式出现，比如：*name="value"*。

属性总是在 HTML 元素的*开始标签*中规定。

例子

```
<h1 align="center"> 拥有关于对齐方式的附加信息。

居中排列标题
<body bgcolor="yellow"> 拥有关于背景颜色的附加信息。

 背景颜色
<table> 定义 HTML 表格。

<table border="1"> 拥有关于表格边框的附加信息。
```

适用于大多数 HTML 元素的属性：

| 属性  | 值                | 描述                                     |
| ----- | ----------------- | ---------------------------------------- |
| class | *classname*       | 规定元素的类名（classname）              |
| id    | *id*              | 规定元素的唯一 id                        |
| style | *style_definition | 用于改变 HTML 元素的行内样式。           |
| title | *text*            | 规定元素的额外信息（可在工具提示中显示） |

## HTML5 语义元素

HTML5 提供的新语义元素定义了网页的不同部分：

| header  | 定义文档或节的页眉             |
| ------- | ------------------------------ |
| nav     | 定义导航链接的容器             |
| section | 定义文档中的节                 |
| article | 定义独立的自包含文章           |
| aside   | 定义内容之外的内容（比如侧栏） |
| footer  | 定义文档或节的页脚             |
| details | 定义额外的细节                 |
| summary | 定义 details 元素的标题        |

## HTML 响应式 Web 设计

响应式设计,有两种方法

1. 自己创建响应式设计方案

2. 使用响应式框架 Bootstrap  等流行框架


## html 框架

通过使用框架，你可以在同一个浏览器窗口中显示不止一个页面。每份HTML文档称为一个框架，并且每个框架都独立于其他的框架。

使用框架的坏处：

开发人员必须同时跟踪更多的HTML文档

## head头部元素

- HTML <head> 元素

<head> 元素是所有头部元素的容器。<head> 内的元素可包含脚本，指示浏览器在何处可以找到样式表，提供元信息，等等。

以下标签都可以添加到 head 部分：<title>、<base>、<link>、<meta>、<script> 以及 <style>。

### HTML title 元

<title> 标签定义文档的标题。

title 元素在所有 HTML/XHTML 文档中都是必需的。

title 元素能够：

- 定义浏览器工具栏中的标题
- 提供页面被添加到收藏夹时显示的标题
- 显示在搜索引擎结果中的页面标题

一个简化的 HTML 文档：

###  base 元素

<base> 标签为页面上的所有链接规定默认地址或默认目标（target）：

```
<head>
    <base href="http://www.w3school.com.cn/images/" />
    <base target="_blank" />
</head>
```

### link 元素

<link> 标签定义文档与外部资源之间的关系。

<link> 标签最常用于连接样式表：

```
<head>
    <link rel="stylesheet" type="text/css" href="mystyle.css" />
</head>
```

### style 元素

<style> 标签用于为 HTML 文档定义样式信息。

您可以在 style 元素内规定 HTML 元素在浏览器中呈现的样式：

```
<head>
    <style type="text/css">
        body {background-color:yellow}
        p {color:blue}
    </style>
</head>
```

### meta 元素

元数据（metadata）是关于数据的信息。

meta 标签提供关于 HTML 文档的元数据。元数据不会显示在页面上，但是对于机器是可读的。

典型的情况是，meta 元素被用于规定页面的描述、关键词、文档的作者、最后修改时间以及其他元数据。

meta 标签始终位于 head 元素中。

元数据可用于浏览器（如何显示内容或重新加载页面），搜索引擎（关键词），或其他 web 服务。

#### 针对搜索引擎的关键词

一些搜索引擎会利用 meta 元素的 name 和 content 属性来索引您的页面。

下面的 meta 元素定义页面的描述：

```
<meta name="description" content="Free Web tutorials on HTML, CSS, XML" />
```

下面的 meta 元素定义页面的关键词：

```
<meta name="keywords" content="HTML, CSS, XML" />
```

name 和 content 属性的作用是描述页面的内容。

### script 元素

script 标签用于定义客户端脚本，比如 JavaScript。

我们会在稍后的章节讲解 script 元素。

### HTML 头部元素

| 标签                                                     | 描述                                     |
| -------------------------------------------------------- | ---------------------------------------- |
| [head](http://www.w3school.com.cn/tags/tag_head.asp)     | 定义关于文档的信息。                     |
| [title](http://www.w3school.com.cn/tags/tag_title.asp)   | 定义文档标题。                           |
| [base](http://www.w3school.com.cn/tags/tag_base.asp)     | 定义页面上所有链接的默认地址或默认目标。 |
| [link](http://www.w3school.com.cn/tags/tag_link.asp)     | 定义文档与外部资源之间的关系。           |
| [meta](http://www.w3school.com.cn/tags/tag_meta.asp)     | 定义关于 HTML 文档的元数据。             |
| [script](http://www.w3school.com.cn/tags/tag_script.asp) | 定义客户端脚本。                         |
| [style](http://www.w3school.com.cn/tags/tag_style.asp)   | 定义文档的样式信息。                     |

## HTML 中有用的字符实体

注释：实体名称对大小写敏感！

![](D:\ProjectList\javascript\Web-leading-end\前端笔记汇总\images\zifushiti.PNG)



## HTML 表单

**HTML 表单用于搜集不同类型的用户输入。**

HTML 表单用于收集用户输入。

### form 元素

HTML 表单用于收集用户输入。

<form> 元素定义 HTML 表单：

**实例**

```
<form>
    <input type="text" value="文本输入框,默认输入值"> <br>
    <input type="radio" name="sex">男 <br>
    <input type="radio" name="sex">女 <br>
    <input type="submit" value="提交">
</form>
```

**HTML 表单包含*表单元素*。**

表单元素指的是不同类型的 input 元素、复选框、单选按钮、提交按钮等等。

### input 元素

*<input>* 元素是最重要的*表单元素*。

<input> 元素有很多形态，根据不同的 *type* 属性。

这是本章中使用的类型：

| 类型   | 描述                                 |
| ------ | ------------------------------------ |
| text   | 定义常规文本输入。                   |
| radio  | 定义单选按钮输入（选择多个选择之一） |
| submit | 定义提交按钮（提交表单）             |

注释：您稍后将在本教程学到更多有关输入类型的知识。

### Action 属性

*action 属性*定义在提交表单时执行的动作。

向服务器提交表单的通常做法是使用提交按钮。

通常，表单会被提交到 web 服务器上的网页。

在上面的例子中，指定了某个服务器脚本来处理被提交表单：

```
<form action="action_page.php">
```

如果省略 action 属性，则 action 会被设置为当前页面。

### Method 属性

*method 属性*规定在提交表单时所用的 HTTP 方法（*GET* 或 *POST*）：

```
<form action="action_page.php" method="GET">
```

或：

```
<form action="action_page.php" method="POST">
```

### Name 属性

如果要正确地被提交，每个输入字段必须设置一个 name 属性。

name属性用于服务端获取,客户端提交的数据

**完整form示例**

```
<form action="action_page.php" method="GET" target="_blank" accept-charset="UTF-8"
ectype="application/x-www-form-urlencoded" autocomplete="off" novalidate>
</form>
```



### form 属性的列表：

| 属性           | 描述                                      |
| -------------- | ---------------------------------------------------------- |
| accept-charset | 规定在被提交表单中使用的字符集（默认：页面字符集）。       |
| action         | 规定向何处提交表单的地址（URL）（提交页面）。              |
| autocomplete   | 规定浏览器应该自动完成表单（默认：开启）。                 |
| enctype        | 规定被提交数据的编码（默认：url-encoded）。                |
| method         | 规定在提交表单时所用的 HTTP 方法（默认：GET）。            |
| name           | 规定识别表单的名称（对于 DOM 使用：document.forms.name）。 |
| novalidate     | 规定浏览器不验证表单。                                     |
| target         | 规定 action 属性中地址的目标（默认：_self）。              |

### select 元素（下拉列表）

*<select>* 元素定义*下拉列表*：

*<option>* 元素定义待选择的选项。

列表通常会把首个选项显示为被选选项。

您能够通过添加 selected 属性来定义预定义选项。

实例

```
<select name="fruits">
    <option value="苹果">苹果</option>
    <option value="香蕉" selected>香蕉</option>
    <option value="橘子">橘子</option>
</select>
```

### textarea 元素

*<textarea>* 元素定义多行输入字段（*文本域*）：

```
<textarea name="message" id="" cols="30" rows="10">
</textarea>
```

**属性:**

**cols** 每行显示字符数

**rows** 最多显示行数

### button 元素

*<button>* 元素定义可点击的*按钮*：

实例

```
<button type="button" onclick="alert('Hello World!')">Click Me!</button>
```

### 表单输入类型

**type 输入类型：**

	text 文本输入
	
	*password* 密码字段
	
	submit 表单提交按钮
	
	radio 单选按钮
	
	checkbox 复选框
	
	button 按钮

**HTML5 增加了多个新的输入类型：**

| 属性           | 描述                           |
| -------------- | ------------------------------ |
| color          | 颜色用于应该包含颜色的输入字段 |
| date           | 用于应该包含日期的输入字段     |
| datetime       |                                |
| datetime-local |                                |
| email          |                                |
| number         | 用于应该包含数字值的输入字段   |
| month          |                                |
| range          | 可显示为滑动控件。             |
| search         |                                |
| tel            |                                |
| time           |                                |
| url            |                                |
| week |                                |
| | |

## HTML5 表单元素

HTML5 增加了如下表单元素：

- datalist
- keygen
- output

注释：默认地，浏览器不会显示未知元素。新元素不会破坏您的页面。

### datalist 元素

*<datalist>* 元素为 <input> 元素规定预定义选项列表。

用户会在他们输入数据时看到预定义选项的下拉列表。

<input> 元素的 *list* 属性必须引用 <datalist> 元素的 *id* 属性。

实例

通过 <datalist> 设置预定义值的 <input> 元素：

```
<form action="action_page.php">
<input list="browsers">
<datalist id="browsers">
   <option value="Internet Explorer">
   <option value="Firefox">
   <option value="Chrome">
   <option value="Opera">
   <option value="Safari">
</datalist> 
</form>
```



