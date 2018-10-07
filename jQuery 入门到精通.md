# jQuery 入门



## jQuery 教程

**jQuery 是一个 JavaScript 库。**

**jQuery 极大地简化了 JavaScript 编程。**

**jQuery 很容易学习。**

### 每一章中用到的实例

```
<html>
<head>
<script type="text/javascript" src="jquery.js"></script>
<script type="text/javascript">
$(document).ready(function(){
  $("p").click(function(){
  $(this).hide();
  });
});
</script>
</head>

<body>
<p>If you click on me, I will disappear.</p>
</body>

</html> 
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_hide)

通过点击 "TIY" 按钮来看看它是如何运行的。

### 您将学到什么

在本教程中，您将通过教程以及许多在线实例，学到如何通过使用 jQuery 应用 JavaScript 效果。

jQuery 是一个“写的更少，但做的更多”的轻量级 JavaScript 库。

基本上，您将学习到如何选取 HTML 元素，以及如何对它们执行类似隐藏、移动以及操作其内容等任务。

### 您需要具备的基础知识

在您开始学习 jQuery 之前，您应该对以下知识有基本的了解：

- HTML
- CSS
- JavaScript

如果您需要首先学习这些科目，请在我们的 [首页](http://www.w3school.com.cn/index.html) 查找这些教程。

### jQuery 实例

通过实例来学习！在 W3School，您将找到许多可以在线编辑并测试的 jQuery 实例。

[jQuery 实例](http://www.w3school.com.cn/jquery/jquery_examples.asp)

### jQuery 参考手册

在 W3School，您将找到包含所有 jQuery 对象和函数的完整参考手册。

[jQuery 参考手册](http://www.w3school.com.cn/jquery/jquery_reference.asp)

## jQuery 简介



**jQuery 库可以通过一行简单的标记被添加到网页中。**

### jQuery 库 - 特性

jQuery 是一个 JavaScript 函数库。

jQuery 库包含以下特性：

- HTML 元素选取
- HTML 元素操作
- CSS 操作
- HTML 事件函数
- JavaScript 特效和动画
- HTML DOM 遍历和修改
- AJAX
- Utilities

### 向您的页面添加 jQuery 库

jQuery 库位于一个 JavaScript 文件中，其中包含了所有的 jQuery 函数。

可以通过下面的标记把 jQuery 添加到网页中：

```
<head>
<script type="text/javascript" src="jquery.js"></script>
</head>
```

请注意，<script> 标签应该位于页面的 <head> 部分。

### 基础 jQuery 实例

下面的例子演示了 jQuery 的 hide() 函数，隐藏了 HTML 文档中所有的 <p> 元素。

**实例**

```
<html>
<head>
<script type="text/javascript" src="jquery.js"></script>
<script type="text/javascript">
$(document).ready(function(){
$("button").click(function(){
$("p").hide();
});
});
</script>
</head>

<body>
<h2>This is a heading</h2>
<p>This is a paragraph.</p>
<p>This is another paragraph.</p>
<button type="button">Click me</button>
</body>
</html>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_hide_p)

### 下载 jQuery

共有两个版本的 jQuery 可供下载：一份是精简过的，另一份是未压缩的（供调试或阅读）。

这两个版本都可从 [jQuery.com](http://docs.jquery.com/Downloading_jQuery#Download_jQuery) 下载。

### 库的替代

Google 和 Microsoft 对 jQuery 的支持都很好。

如果您不愿意在自己的计算机上存放 jQuery 库，那么可以从 Google 或 Microsoft 加载 CDN jQuery 核心文件。

### 使用 Google 的 CDN

```
<head>
<script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs
/jquery/1.4.0/jquery.min.js"></script>
</head>
```

### 使用 Microsoft 的 CDN

```
<head>
<script type="text/javascript" src="http://ajax.microsoft.com/ajax/jquery
/jquery-1.4.min.js"></script>
</head>
```

## jQuery 安装



### 把 jQuery 添加到您的网页

如需使用 jQuery，您需要下载 jQuery 库（会在下面为您讲解），然后把它包含在希望使用的网页中。

jQuery 库是一个 JavaScript 文件，您可以使用 HTML 的 <script> 标签引用它：

```
<head>
<script src="jquery.js"></script>
</head>
```

请注意，<script> 标签应该位于页面的 <head> 部分。

提示：您是否很疑惑为什么我们没有在 <script> 标签中使用 type="text/javascript" ？

在 HTML5 中，不必那样做了。JavaScript 是 HTML5 以及所有现代浏览器中的默认脚本语言！

### 下载 jQuery

有两个版本的 jQuery 可供下载：

- Production version - 用于实际的网站中，已被精简和压缩。
- Development version - 用于测试和开发（未压缩，是可读的代码）

这两个版本都可以从 [jQuery.com](http://jquery.com/download/) 下载。

提示：您可以把下载文件放到与页面相同的目录中，这样更方便使用。

### 替代方案

如果您不希望下载并存放 jQuery，那么也可以通过 CDN（内容分发网络） 引用它。

谷歌和微软的服务器都存有 jQuery 。

如需从谷歌或微软引用 jQuery，请使用以下代码之一：

### Google CDN:

```
<head>
<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.8.0/jquery.min.js">
</script>
</head>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_lib_google)

提示：通过 Google CDN 来获得最新可用的版本：

如果您观察上什么的 Google URL - 在 URL 中规定了 jQuery 版本 (1.8.0)。如果您希望使用最新版本的 jQuery，也可以从版本字符串的末尾（比如本例 1.8）删除一个数字，谷歌会返回 1.8 系列中最新的可用版本（1.8.0、1.8.1 等等），或者也可以只剩第一个数字，那么谷歌会返回 1 系列中最新的可用版本（从 1.1.0 到 1.9.9）。

### Microsoft CDN:

```
<head>
<script src="http://ajax.aspnetcdn.com/ajax/jQuery/jquery-1.8.0.js">
</script>
</head>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_lib_microsoft)

提示：使用谷歌或微软的 jQuery，有一个很大的优势：

许多用户在访问其他站点时，已经从谷歌或微软加载过 jQuery。所有结果是，当他们访问您的站点时，会从缓存中加载 jQuery，这样可以减少加载时间。同时，大多数 CDN 都可以确保当用户向其请求文件时，会从离用户最近的服务器上返回响应，这样也可以提高加载速度。

- 
    

## jQuery 语法



**通过 jQuery，您可以选取（查询，query） HTML 元素，并对它们执行“操作”（actions）。**

### jQuery 语法实例

- [$(this).hide()](http://www.w3school.com.cn/tiy/t.asp?f=jquery_hide_this)

  演示 jQuery hide() 函数，隐藏当前的 HTML 元素。

- [$("#test").hide()](http://www.w3school.com.cn/tiy/t.asp?f=jquery_hide_id)

  演示 jQuery hide() 函数，隐藏 id="test" 的元素。

- [$("p").hide()](http://www.w3school.com.cn/tiy/t.asp?f=jquery_hide_p)

  演示 jQuery hide() 函数，隐藏所有 <p> 元素。

- [$(".test").hide()](http://www.w3school.com.cn/tiy/t.asp?f=jquery_hide_class)

  演示 jQuery hide() 函数，隐藏所有 class="test" 的元素。

### jQuery 语法

jQuery 语法是为 HTML 元素的选取编制的，可以对元素执行某些操作。

基础语法是：*$(selector).action()*

- 美元符号定义 jQuery
- 选择符（selector）“查询”和“查找” HTML 元素
- jQuery 的 action() 执行对元素的操作

**示例**

$(this).hide() - 隐藏当前元素

$("p").hide() - 隐藏所有段落

$(".test").hide() - 隐藏所有 class="test" 的所有元素

$("#test").hide() - 隐藏所有 id="test" 的元素

提示：jQuery 使用的语法是 XPath 与 CSS 选择器语法的组合。在本教程接下来的章节，您将学习到更多有关选择器的语法。

### 文档就绪函数

您也许已经注意到在我们的实例中的所有 jQuery 函数位于一个 document ready 函数中：

```
$(document).ready(function(){

--- jQuery functions go here ----

});
```

这是为了防止文档在完全加载（就绪）之前运行 jQuery 代码。

如果在文档没有完全加载之前就运行函数，操作可能失败。下面是两个具体的例子：

- 试图隐藏一个不存在的元素
- 获得未完全加载的图像的大小

## jQuery 选择器



**选择器允许您对元素组或单个元素进行操作。**

### jQuery 选择器

在前面的章节中，我们展示了一些有关如何选取 HTML 元素的实例。

关键点是学习 jQuery 选择器是如何准确地选取您希望应用效果的元素。

jQuery 元素选择器和属性选择器允许您通过标签名、属性名或内容对 HTML 元素进行选择。

选择器允许您对 HTML 元素组或单个元素进行操作。

在 HTML DOM 术语中：

选择器允许您对 DOM 元素组或单个 DOM 节点进行操作。

### jQuery 元素选择器

jQuery 使用 CSS 选择器来选取 HTML 元素。

$("p") 选取 <p> 元素。

$("p.intro") 选取所有 class="intro" 的 <p> 元素。

$("p#demo") 选取所有 id="demo" 的 <p> 元素。

### jQuery 属性选择器

jQuery 使用 XPath 表达式来选择带有给定属性的元素。

$("[href]") 选取所有带有 href 属性的元素。

$("[href='#']") 选取所有带有 href 值等于 "#" 的元素。

$("[href!='#']") 选取所有带有 href 值不等于 "#" 的元素。

$("[href$='.jpg']") 选取所有 href 值以 ".jpg" 结尾的元素。

### jQuery CSS 选择器

jQuery CSS 选择器可用于改变 HTML 元素的 CSS 属性。

下面的例子把所有 p 元素的背景颜色更改为红色：

实例

```
$("p").css("background-color","red");
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_css_change_p)

### 更多的选择器实例

| 语法                 | 描述                                                 |
| -------------------- | ---------------------------------------------------- |
| $(this)              | 当前 HTML 元素                                       |
| $("p")               | 所有 <p> 元素                                        |
| $("p.intro")         | 所有 class="intro" 的 <p> 元素                       |
| $(".intro")          | 所有 class="intro" 的元素                            |
| $("#intro")          | id="intro" 的元素                                    |
| $("ul li:first")     | 每个 <ul> 的第一个 <li> 元素                         |
| $("[href$='.jpg']")  | 所有带有以 ".jpg" 结尾的属性值的 href 属性           |
| $("div#intro .head") | id="intro" 的 <div> 元素中的所有 class="head" 的元素 |

如需完整的参考手册，请访问我们的 [jQuery 选择器参考手册](http://www.w3school.com.cn/jquery/jquery_ref_selectors.asp)。

### jQuery 选择器参考手册

| 选择器                                                       | 实例                       | 选取                                       |
| ------------------------------------------------------------ | -------------------------- | ------------------------------------------ |
| [*](http://www.w3school.com.cn/jquery/selector_all.asp)      | $("*")                     | 所有元素                                   |
| [#*id*](http://www.w3school.com.cn/jquery/selector_id.asp)   | $("#lastname")             | id="lastname" 的元素                       |
| [.*class*](http://www.w3school.com.cn/jquery/selector_class.asp) | $(".intro")                | 所有 class="intro" 的元素                  |
| [*element*](http://www.w3school.com.cn/jquery/selector_element.asp) | $("p")                     | 所有 <p> 元素                              |
| .*class*.*class*                                             | $(".intro.demo")           | 所有 class="intro" 且 class="demo" 的元素  |
|                                                              |                            |                                            |
| [:first](http://www.w3school.com.cn/jquery/selector_first.asp) | $("p:first")               | 第一个 <p> 元素                            |
| [:last](http://www.w3school.com.cn/jquery/selector_last.asp) | $("p:last")                | 最后一个 <p> 元素                          |
| [:even](http://www.w3school.com.cn/jquery/selector_even.asp) | $("tr:even")               | 所有偶数 <tr> 元素                         |
| [:odd](http://www.w3school.com.cn/jquery/selector_odd.asp)   | $("tr:odd")                | 所有奇数 <tr> 元素                         |
|                                                              |                            |                                            |
| [:eq(*index*)](http://www.w3school.com.cn/jquery/selector_eq.asp) | $("ul li:eq(3)")           | 列表中的第四个元素（index 从 0 开始）      |
| [:gt(*no*)](http://www.w3school.com.cn/jquery/selector_gt.asp) | $("ul li:gt(3)")           | 列出 index 大于 3 的元素                   |
| [:lt(*no*)](http://www.w3school.com.cn/jquery/selector_lt.asp) | $("ul li:lt(3)")           | 列出 index 小于 3 的元素                   |
| :not(*selector*)                                             | $("input:not(:empty)")     | 所有不为空的 input 元素                    |
|                                                              |                            |                                            |
| [:header](http://www.w3school.com.cn/jquery/selector_header.asp) | $(":header")               | 所有标题元素 <h1> - <h6>                   |
| [:animated](http://www.w3school.com.cn/jquery/selector_animated.asp) |                            | 所有动画元素                               |
|                                                              |                            |                                            |
| [:contains(*text*)](http://www.w3school.com.cn/jquery/selector_contains.asp) | $(":contains('W3School')") | 包含指定字符串的所有元素                   |
| [:empty](http://www.w3school.com.cn/jquery/selector_empty.asp) | $(":empty")                | 无子（元素）节点的所有元素                 |
| :hidden                                                      | $("p:hidden")              | 所有隐藏的 <p> 元素                        |
| [:visible](http://www.w3school.com.cn/jquery/selector_visible.asp) | $("table:visible")         | 所有可见的表格                             |
|                                                              |                            |                                            |
| s1,s2,s3                                                     | $("th,td,.intro")          | 所有带有匹配选择的元素                     |
|                                                              |                            |                                            |
| [[*attribute*\]](http://www.w3school.com.cn/jquery/selector_attribute.asp) | $("[href]")                | 所有带有 href 属性的元素                   |
| [[*attribute*=*value*\]](http://www.w3school.com.cn/jquery/selector_attribute_equal_value.asp) | $("[href='#']")            | 所有 href 属性的值等于 "#" 的元素          |
| [[*attribute*!=*value*\]](http://www.w3school.com.cn/jquery/selector_attribute_notequal_value.asp) | $("[href!='#']")           | 所有 href 属性的值不等于 "#" 的元素        |
| [[*attribute*$=*value*\]](http://www.w3school.com.cn/jquery/selector_attribute_end_value.asp) | $("[href$='.jpg']")        | 所有 href 属性的值包含以 ".jpg" 结尾的元素 |
|                                                              |                            |                                            |
| [:input](http://www.w3school.com.cn/jquery/selector_input.asp) | $(":input")                | 所有 <input> 元素                          |
| [:text](http://www.w3school.com.cn/jquery/selector_input_text.asp) | $(":text")                 | 所有 type="text" 的 <input> 元素           |
| [:password](http://www.w3school.com.cn/jquery/selector_input_password.asp) | $(":password")             | 所有 type="password" 的 <input> 元素       |
| [:radio](http://www.w3school.com.cn/jquery/selector_input_radio.asp) | $(":radio")                | 所有 type="radio" 的 <input> 元素          |
| [:checkbox](http://www.w3school.com.cn/jquery/selector_input_checkbox.asp) | $(":checkbox")             | 所有 type="checkbox" 的 <input> 元素       |
| [:submit](http://www.w3school.com.cn/jquery/selector_input_submit.asp) | $(":submit")               | 所有 type="submit" 的 <input> 元素         |
| [:reset](http://www.w3school.com.cn/jquery/selector_input_reset.asp) | $(":reset")                | 所有 type="reset" 的 <input> 元素          |
| [:button](http://www.w3school.com.cn/jquery/selector_input_button.asp) | $(":button")               | 所有 type="button" 的 <input> 元素         |
| [:image](http://www.w3school.com.cn/jquery/selector_input_image.asp) | $(":image")                | 所有 type="image" 的 <input> 元素          |
| [:file](http://www.w3school.com.cn/jquery/selector_input_file.asp) | $(":file")                 | 所有 type="file" 的 <input> 元素           |
|                                                              |                            |                                            |
| [:enabled](http://www.w3school.com.cn/jquery/selector_input_enabled.asp) | $(":enabled")              | 所有激活的 input 元素                      |
| [:disabled](http://www.w3school.com.cn/jquery/selector_input_disabled.asp) | $(":disabled")             | 所有禁用的 input 元素                      |
| [:selected](http://www.w3school.com.cn/jquery/selector_input_selected.asp) | $(":selected")             | 所有被选取的 input 元素                    |
| [:checked](http://www.w3school.com.cn/jquery/selector_input_checked.asp) | $(":checked")              | 所有被选中的 input 元素                    |

## jQuery 事件

**jQuery 是为事件处理特别设计的。**

### jQuery 事件函数

jQuery 事件处理方法是 jQuery 中的核心函数。

事件处理程序指的是当 HTML 中发生某些事件时所调用的方法。术语由事件“触发”（或“激发”）经常会被使用。

通常会把 jQuery 代码放到 <head>部分的事件处理方法中：

**实例**

```
<html>
<head>
<script type="text/javascript" src="jquery.js"></script>
<script type="text/javascript">
$(document).ready(function(){
  $("button").click(function(){
    $("p").hide();
  });
});
</script>
</head>

<body>
<h2>This is a heading</h2>
<p>This is a paragraph.</p>
<p>This is another paragraph.</p>
<button>Click me</button>
</body>

</html>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_hide_p)

在上面的例子中，当按钮的点击事件被触发时会调用一个函数：

```
$("button").click(function() {..some code... } )
```

该方法隐藏所有 <p> 元素：

```
$("p").hide();
```

## 单独文件中的函数

如果您的网站包含许多页面，并且您希望您的 jQuery 函数易于维护，那么请把您的 jQuery 函数放到独立的 .js 文件中。

当我们在教程中演示 jQuery 时，会将函数直接添加到 <head> 部分中。不过，把它们放到一个单独的文件中会更好，就像这样（通过 src 属性来引用文件）：

### 实例

```
<head>
<script type="text/javascript" src="jquery.js"></script>
<script type="text/javascript" src="my_jquery_functions.js"></script>
</head>
```

### jQuery 名称冲突

jQuery 使用 $ 符号作为 jQuery 的简介方式。

某些其他 JavaScript 库中的函数（比如 Prototype）同样使用 $ 符号。

jQuery 使用名为 noConflict() 的方法来解决该问题。

*var jq=jQuery.noConflict()*，帮助您使用自己的名称（比如 jq）来代替 $ 符号。

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_noconflict)

### 结论

由于 jQuery 是为处理 HTML 事件而特别设计的，那么当您遵循以下原则时，您的代码会更恰当且更易维护：

- 把所有 jQuery 代码置于事件处理函数中
- 把所有事件处理函数置于文档就绪事件处理器中
- 把 jQuery 代码置于单独的 .js 文件中
- 如果存在名称冲突，则重命名 jQuery 库

### jQuery 事件

下面是 jQuery 中事件方法的一些例子：

| Event 函数                      | 绑定函数至                                     |
| ------------------------------- | ---------------------------------------------- |
| $(document).ready(function)     | 将函数绑定到文档的就绪事件（当文档完成加载时） |
| $(selector).click(function)     | 触发或将函数绑定到被选元素的点击事件           |
| $(selector).dblclick(function)  | 触发或将函数绑定到被选元素的双击事件           |
| $(selector).focus(function)     | 触发或将函数绑定到被选元素的获得焦点事件       |
| $(selector).mouseover(function) | 触发或将函数绑定到被选元素的鼠标悬停事件       |

如需完整的参考手册，请访问我们的 [jQuery 事件参考手册](http://www.w3school.com.cn/jquery/jquery_ref_events.asp)。

### [jQuery 事件参考手册](http://www.w3school.com.cn/jquery/jquery_ref_events.asp)

| 方法                                                         | 描述                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| [bind()](http://www.w3school.com.cn/jquery/event_bind.asp)   | 向匹配元素附加一个或更多事件处理器                           |
| [blur()](http://www.w3school.com.cn/jquery/event_blur.asp)   | 触发、或将函数绑定到指定元素的 blur 事件                     |
| [change()](http://www.w3school.com.cn/jquery/event_change.asp) | 触发、或将函数绑定到指定元素的 change 事件                   |
| [click()](http://www.w3school.com.cn/jquery/event_click.asp) | 触发、或将函数绑定到指定元素的 click 事件                    |
| [dblclick()](http://www.w3school.com.cn/jquery/event_dblclick.asp) | 触发、或将函数绑定到指定元素的 double click 事件             |
| [delegate()](http://www.w3school.com.cn/jquery/event_delegate.asp) | 向匹配元素的当前或未来的子元素附加一个或多个事件处理器       |
| [die()](http://www.w3school.com.cn/jquery/event_die.asp)     | 移除所有通过 live() 函数添加的事件处理程序。                 |
| [error()](http://www.w3school.com.cn/jquery/event_error.asp) | 触发、或将函数绑定到指定元素的 error 事件                    |
| [event.isDefaultPrevented()](http://www.w3school.com.cn/jquery/event_isdefaultprevented.asp) | 返回 event 对象上是否调用了 event.preventDefault()。         |
| [event.pageX](http://www.w3school.com.cn/jquery/event_pagex.asp) | 相对于文档左边缘的鼠标位置。                                 |
| [event.pageY](http://www.w3school.com.cn/jquery/event_pagey.asp) | 相对于文档上边缘的鼠标位置。                                 |
| [event.preventDefault()](http://www.w3school.com.cn/jquery/event_preventdefault.asp) | 阻止事件的默认动作。                                         |
| [event.result](http://www.w3school.com.cn/jquery/event_result.asp) | 包含由被指定事件触发的事件处理器返回的最后一个值。           |
| [event.target](http://www.w3school.com.cn/jquery/event_target.asp) | 触发该事件的 DOM 元素。                                      |
| [event.timeStamp](http://www.w3school.com.cn/jquery/event_timeStamp.asp) | 该属性返回从 1970 年 1 月 1 日到事件发生时的毫秒数。         |
| [event.type](http://www.w3school.com.cn/jquery/event_type.asp) | 描述事件的类型。                                             |
| [event.which](http://www.w3school.com.cn/jquery/event_which.asp) | 指示按了哪个键或按钮。                                       |
| [focus()](http://www.w3school.com.cn/jquery/event_focus.asp) | 触发、或将函数绑定到指定元素的 focus 事件                    |
| [keydown()](http://www.w3school.com.cn/jquery/event_keydown.asp) | 触发、或将函数绑定到指定元素的 key down 事件                 |
| [keypress()](http://www.w3school.com.cn/jquery/event_keypress.asp) | 触发、或将函数绑定到指定元素的 key press 事件                |
| [keyup()](http://www.w3school.com.cn/jquery/event_keyup.asp) | 触发、或将函数绑定到指定元素的 key up 事件                   |
| [live()](http://www.w3school.com.cn/jquery/event_live.asp)   | 为当前或未来的匹配元素添加一个或多个事件处理器               |
| [load()](http://www.w3school.com.cn/jquery/event_load.asp)   | 触发、或将函数绑定到指定元素的 load 事件                     |
| [mousedown()](http://www.w3school.com.cn/jquery/event_mousedown.asp) | 触发、或将函数绑定到指定元素的 mouse down 事件               |
| [mouseenter()](http://www.w3school.com.cn/jquery/event_mouseenter.asp) | 触发、或将函数绑定到指定元素的 mouse enter 事件              |
| [mouseleave()](http://www.w3school.com.cn/jquery/event_mouseleave.asp) | 触发、或将函数绑定到指定元素的 mouse leave 事件              |
| [mousemove()](http://www.w3school.com.cn/jquery/event_mousemove.asp) | 触发、或将函数绑定到指定元素的 mouse move 事件               |
| [mouseout()](http://www.w3school.com.cn/jquery/event_mouseout.asp) | 触发、或将函数绑定到指定元素的 mouse out 事件                |
| [mouseover()](http://www.w3school.com.cn/jquery/event_mouseover.asp) | 触发、或将函数绑定到指定元素的 mouse over 事件               |
| [mouseup()](http://www.w3school.com.cn/jquery/event_mouseup.asp) | 触发、或将函数绑定到指定元素的 mouse up 事件                 |
| [one()](http://www.w3school.com.cn/jquery/event_one.asp)     | 向匹配元素添加事件处理器。每个元素只能触发一次该处理器。     |
| [ready()](http://www.w3school.com.cn/jquery/event_ready.asp) | 文档就绪事件（当 HTML 文档就绪可用时）                       |
| [resize()](http://www.w3school.com.cn/jquery/event_resize.asp) | 触发、或将函数绑定到指定元素的 resize 事件                   |
| [scroll()](http://www.w3school.com.cn/jquery/event_scroll.asp) | 触发、或将函数绑定到指定元素的 scroll 事件                   |
| [select()](http://www.w3school.com.cn/jquery/event_select.asp) | 触发、或将函数绑定到指定元素的 select 事件                   |
| [submit()](http://www.w3school.com.cn/jquery/event_submit.asp) | 触发、或将函数绑定到指定元素的 submit 事件                   |
| [toggle()](http://www.w3school.com.cn/jquery/event_toggle.asp) | 绑定两个或多个事件处理器函数，当发生轮流的 click 事件时执行。 |
| [trigger()](http://www.w3school.com.cn/jquery/event_trigger.asp) | 所有匹配元素的指定事件                                       |
| [triggerHandler()](http://www.w3school.com.cn/jquery/event_triggerhandler.asp) | 第一个被匹配元素的指定事件                                   |
| [unbind()](http://www.w3school.com.cn/jquery/event_unbind.asp) | 从匹配元素移除一个被添加的事件处理器                         |
| [undelegate()](http://www.w3school.com.cn/jquery/event_undelegate.asp) | 从匹配元素移除一个被添加的事件处理器，现在或将来             |
| [unload()](http://www.w3school.com.cn/jquery/event_unload.asp) | 触发、或将函数绑定到指定元素的 unload 事件                   |



# jQuery 效果 

## jQuery 效果参考手册

### jQuery 效果函数

| 方法                                                         | 描述                                         |
| ------------------------------------------------------------ | -------------------------------------------- |
| [animate()](http://www.w3school.com.cn/jquery/effect_animate.asp) | 对被选元素应用“自定义”的动画                 |
| [clearQueue()](http://www.w3school.com.cn/jquery/effect_clearqueue.asp) | 对被选元素移除所有排队的函数（仍未运行的）   |
| delay()                                                      | 对被选元素的所有排队函数（仍未运行）设置延迟 |
| dequeue()                                                    | 运行被选元素的下一个排队函数                 |
| [fadeIn()](http://www.w3school.com.cn/jquery/effect_fadein.asp) | 逐渐改变被选元素的不透明度，从隐藏到可见     |
| [fadeOut()](http://www.w3school.com.cn/jquery/effect_fadeout.asp) | 逐渐改变被选元素的不透明度，从可见到隐藏     |
| [fadeTo()](http://www.w3school.com.cn/jquery/effect_fadeto.asp) | 把被选元素逐渐改变至给定的不透明度           |
| [hide()](http://www.w3school.com.cn/jquery/effect_hide.asp)  | 隐藏被选的元素                               |
| queue()                                                      | 显示被选元素的排队函数                       |
| [show()](http://www.w3school.com.cn/jquery/effect_show.asp)  | 显示被选的元素                               |
| [slideDown()](http://www.w3school.com.cn/jquery/effect_slidedown.asp) | 通过调整高度来滑动显示被选元素               |
| [slideToggle()](http://www.w3school.com.cn/jquery/effect_slidetoggle.asp) | 对被选元素进行滑动隐藏和滑动显示的切换       |
| [slideUp()](http://www.w3school.com.cn/jquery/effect_slideup.asp) | 通过调整高度来滑动隐藏被选元素               |
| [stop()](http://www.w3school.com.cn/jquery/effect_stop.asp)  | 停止在被选元素上运行动画                     |
| [toggle()](http://www.w3school.com.cn/jquery/effect_toggle.asp) | 对被选元素进行隐藏和显示的切换               |



##  隐藏和显示



**隐藏、显示、切换，滑动，淡入淡出，以及动画，哇哦！**

### 效果演示

点击这里，隐藏/显示面板

### 实例

- [jQuery hide()](http://www.w3school.com.cn/tiy/t.asp?f=jquery_hide)

  演示一个简单的 jQuery hide() 方法。

- [jQuery hide()](http://www.w3school.com.cn/tiy/t.asp?f=jquery_hide_explanations)

  另一个 hide() 演示。如何隐藏部分文本。

### jQuery hide() 和 show()

通过 jQuery，您可以使用 hide() 和 show() 方法来隐藏和显示 HTML 元素：

```
$("#hide").click(function(){
  $("p").hide();
});

$("#show").click(function(){
  $("p").show();
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_hide_show)

### 语法：

```
$(selector).hide(speed,callback);

$(selector).show(speed,callback);
```

可选的 speed 参数规定隐藏/显示的速度，可以取以下值："slow"、"fast" 或毫秒。

可选的 callback 参数是隐藏或显示完成后所执行的函数名称。

下面的例子演示了带有 speed 参数的 hide() 方法：

**实例**

```
$("button").click(function(){
  $("p").hide(1000);
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_hide_slow)

### jQuery toggle()

通过 jQuery，您可以使用 toggle() 方法来切换 hide() 和 show() 方法。

显示被隐藏的元素，并隐藏已显示的元素：

### 实例

```
$("button").click(function(){
  $("p").toggle();
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_toggle)

### 语法：

```
$(selector).toggle(speed,callback);
```

可选的 speed 参数规定隐藏/显示的速度，可以取以下值："slow"、"fast" 或毫秒。

可选的 callback 参数是 toggle() 方法完成后所执行的函数名称。





##  淡入淡出

**通过 jQuery，您可以实现元素的淡入淡出效果。**

### 效果演示

点击这里，隐藏/显示面板

**实例**

- [jQuery fadeIn()](http://www.w3school.com.cn/tiy/t.asp?f=jquery_fadein)

  演示 jQuery fadeIn() 方法。

- [jQuery fadeOut()](http://www.w3school.com.cn/tiy/t.asp?f=jquery_fadeout)

  演示 jQuery fadeOut() 方法。

- [jQuery fadeToggle()](http://www.w3school.com.cn/tiy/t.asp?f=jquery_fadetoggle)

  演示 jQuery fadeToggle() 方法。

- [jQuery fadeTo()](http://www.w3school.com.cn/tiy/t.asp?f=jquery_fadeto)

  演示 jQuery fadeTo() 方法。

### jQuery Fading 方法

通过 jQuery，您可以实现元素的淡入淡出效果。

jQuery 拥有下面四种 fade 方法：

- fadeIn()
- fadeOut()
- fadeToggle()
- fadeTo()

### jQuery fadeIn() 方法

jQuery fadeIn() 用于淡入已隐藏的元素。

**语法**：

```
$(selector).fadeIn(speed,callback);
```

可选的 speed 参数规定效果的时长。它可以取以下值："slow"、"fast" 或毫秒。

可选的 callback 参数是 fading 完成后所执行的函数名称。

下面的例子演示了带有不同参数的 fadeIn() 方法：

**实例**

```
$("button").click(function(){
  $("#div1").fadeIn();
  $("#div2").fadeIn("slow");
  $("#div3").fadeIn(3000);
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_fadein)

### jQuery fadeOut() 方法

jQuery fadeOut() 方法用于淡出可见元素。

**语法**：

```
$(selector).fadeOut(speed,callback);
```

可选的 speed 参数规定效果的时长。它可以取以下值："slow"、"fast" 或毫秒。

可选的 callback 参数是 fading 完成后所执行的函数名称。

下面的例子演示了带有不同参数的 fadeOut() 方法：

**实例**

```
$("button").click(function(){
  $("#div1").fadeOut();
  $("#div2").fadeOut("slow");
  $("#div3").fadeOut(3000);
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_fadeout)

### jQuery fadeToggle() 方法

jQuery fadeToggle() 方法可以在 fadeIn() 与 fadeOut() 方法之间进行切换。

如果元素已淡出，则 fadeToggle() 会向元素添加淡入效果。

如果元素已淡入，则 fadeToggle() 会向元素添加淡出效果。

**语法**：

```
$(selector).fadeToggle(speed,callback);
```

可选的 speed 参数规定效果的时长。它可以取以下值："slow"、"fast" 或毫秒。

可选的 callback 参数是 fading 完成后所执行的函数名称。

下面的例子演示了带有不同参数的 fadeToggle() 方法：

**实例**

```
$("button").click(function(){
  $("#div1").fadeToggle();
  $("#div2").fadeToggle("slow");
  $("#div3").fadeToggle(3000);
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_fadetoggle)

### jQuery fadeTo() 方法

jQuery fadeTo() 方法允许渐变为给定的不透明度（值介于 0 与 1 之间）。

**语法**：

```
$(selector).fadeTo(speed,opacity,callback);
```

必需的 speed 参数规定效果的时长。它可以取以下值："slow"、"fast" 或毫秒。

fadeTo() 方法中必需的 opacity 参数将淡入淡出效果设置为给定的不透明度（值介于 0 与 1 之间）。

可选的 callback 参数是该函数完成后所执行的函数名称。

下面的例子演示了带有不同参数的 fadeTo() 方法：

**实例**

```
$("button").click(function(){
  $("#div1").fadeTo("slow",0.15);
  $("#div2").fadeTo("slow",0.4);
  $("#div3").fadeTo("slow",0.7);
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_fadeto)

## 滑动

**jQuery 滑动方法可使元素上下滑动。**

### 效果演示

点击这里，隐藏/显示面板

一寸光阴一寸金，因此，我们为您提供快捷易懂的学习内容。

在这里，您可以通过一种易懂的便利的模式获得您需要的任何知识。

**实例**

- [jQuery slideDown()](http://www.w3school.com.cn/tiy/t.asp?f=jquery_slide_down)

  演示 jQuery slideDown() 方法。

- [jQuery slideUp()](http://www.w3school.com.cn/tiy/t.asp?f=jquery_slide_up)

  演示 jQuery slideUp() 方法。

- [jQuery slideToggle()](http://www.w3school.com.cn/tiy/t.asp?f=jquery_slide_toggle)

  演示 jQuery slideToggle() 方法。

### jQuery 滑动方法

通过 jQuery，您可以在元素上创建滑动效果。

jQuery 拥有以下滑动方法：

- slideDown()
- slideUp()
- slideToggle()

### jQuery slideDown() 方法

jQuery slideDown() 方法用于向下滑动元素。

**语法**：

```
$(selector).slideDown(speed,callback);
```

可选的 speed 参数规定效果的时长。它可以取以下值："slow"、"fast" 或毫秒。

可选的 callback 参数是滑动完成后所执行的函数名称。

下面的例子演示了 slideDown() 方法：

**实例**

```
$("#flip").click(function(){
  $("#panel").slideDown();
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_slide_down)

### jQuery slideUp() 方法

jQuery slideUp() 方法用于向上滑动元素。

**语法**：

```
$(selector).slideUp(speed,callback);
```

可选的 speed 参数规定效果的时长。它可以取以下值："slow"、"fast" 或毫秒。

可选的 callback 参数是滑动完成后所执行的函数名称。

下面的例子演示了 slideUp() 方法：

**实例**

```
$("#flip").click(function(){
  $("#panel").slideUp();
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_slide_up)

### jQuery slideToggle() 方法

jQuery slideToggle() 方法可以在 slideDown() 与 slideUp() 方法之间进行切换。

如果元素向下滑动，则 slideToggle() 可向上滑动它们。

如果元素向上滑动，则 slideToggle() 可向下滑动它们。

```
$(selector).slideToggle(speed,callback);
```

可选的 speed 参数规定效果的时长。它可以取以下值："slow"、"fast" 或毫秒。

可选的 callback 参数是滑动完成后所执行的函数名称。

下面的例子演示了 slideToggle() 方法：

**实例**

```
$("#flip").click(function(){
  $("#panel").slideToggle();
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_slide_toggle)

##  动画

**jQuery animate() 方法允许您创建自定义的动画。**

### 效果演示

jQuery

### jQuery 动画 - animate() 方法

jQuery animate() 方法用于创建自定义动画。

**语法**：

```
$(selector).animate({params},speed,callback);
```

必需的 params 参数定义形成动画的 CSS 属性。

可选的 speed 参数规定效果的时长。它可以取以下值："slow"、"fast" 或毫秒。

可选的 callback 参数是动画完成后所执行的函数名称。

下面的例子演示 animate() 方法的简单应用；它把 <div> 元素移动到左边，直到 left 属性等于 250 像素为止：

**实例**

```
$("button").click(function(){
  $("div").animate({left:'250px'});
}); 
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_animation1)

提示：默认地，所有 HTML 元素都有一个静态位置，且无法移动。

如需对位置进行操作，要记得首先把元素的 CSS position 属性设置为 relative、fixed 或 absolute！

### jQuery animate() - 操作多个属性

请注意，生成动画的过程中可同时使用多个属性：

**实例**

```
$("button").click(function(){
  $("div").animate({
    left:'250px',
    opacity:'0.5',
    height:'150px',
    width:'150px'
  });
}); 
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_animation1_multicss)

提示：可以用 animate() 方法来操作所有 CSS 属性吗？

是的，几乎可以！不过，需要记住一件重要的事情：当使用 animate() 时，必须使用 Camel 标记法书写所有的属性名，比如，必须使用 paddingLeft 而不是 padding-left，使用 marginRight 而不是 margin-right，等等。

同时，色彩动画并不包含在核心 jQuery 库中。

如果需要生成颜色动画，您需要从 jQuery.com 下载 Color Animations 插件。

### jQuery animate() - 使用相对值

也可以定义相对值（该值相对于元素的当前值）。需要在值的前面加上 += 或 -=：

**实例**

```
$("button").click(function(){
  $("div").animate({
    left:'250px',
    height:'+=150px',
    width:'+=150px'
  });
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_animation1_relative)

### jQuery animate() - 使用预定义的值

您甚至可以把属性的动画值设置为 "show"、"hide" 或 "toggle"：

**实例**

```
$("button").click(function(){
  $("div").animate({
    height:'toggle'
  });
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_animation1_toggle)

### jQuery animate() - 使用队列功能

默认地，jQuery 提供针对动画的队列功能。

这意味着如果您在彼此之后编写多个 animate() 调用，jQuery 会创建包含这些方法调用的“内部”队列。然后逐一运行这些 animate 调用。

**实例 1**

隐藏，如果您希望在彼此之后执行不同的动画，那么我们要利用队列功能：

```
$("button").click(function(){
  var div=$("div");
  div.animate({height:'300px',opacity:'0.4'},"slow");
  div.animate({width:'300px',opacity:'0.8'},"slow");
  div.animate({height:'100px',opacity:'0.4'},"slow");
  div.animate({width:'100px',opacity:'0.8'},"slow");
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_animation)

**实例 2**

下面的例子把 <div> 元素移动到右边，然后增加文本的字号：

```
$("button").click(function(){
  var div=$("div");
  div.animate({left:'100px'},"slow");
  div.animate({fontSize:'3em'},"slow");
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_animation2)

## 停止动画



**jQuery stop() 方法用于在动画或效果完成前对它们进行停止。**

### 效果演示

点击这里，向上/向下滑动面板

**实例**

- [jQuery stop() 滑动](http://www.w3school.com.cn/tiy/t.asp?f=jquery_stop_slide)

  演示 jQuery stop() 方法。

- [jQuery stop() 动画（带有参数）](http://www.w3school.com.cn/tiy/t.asp?f=jquery_stop_params)

  演示 jQuery stop() 方法。

### jQuery stop() 方法

jQuery stop() 方法用于停止动画或效果，在它们完成之前。

stop() 方法适用于所有 jQuery 效果函数，包括滑动、淡入淡出和自定义动画。

**语法**

```
$(selector).stop(stopAll,goToEnd);
```

可选的 stopAll 参数规定是否应该清除动画队列。默认是 false，即仅停止活动的动画，允许任何排入队列的动画向后执行。

可选的 goToEnd 参数规定是否立即完成当前动画。默认是 false。

因此，默认地，stop() 会清除在被选元素上指定的当前动画。

下面的例子演示 stop() 方法，不带参数：

**实例**

```
$("#stop").click(function(){
  $("#panel").stop();
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_stop_slide)

## Callback 函数



**Callback 函数在当前动画 100% 完成之后执行。**

### jQuery 动画的问题

许多 jQuery 函数涉及动画。这些函数也许会将 *speed* 或 *duration* 作为可选参数。

例子：*$("p").hide("slow")*

*speed* 或 *duration* 参数可以设置许多不同的值，比如 "slow", "fast", "normal" 或毫秒。

**实例**

```
$("button").click(function(){
$("p").hide(1000);
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_hide_slow)

由于 JavaScript 语句（指令）是逐一执行的 - 按照次序，动画之后的语句可能会产生错误或页面冲突，因为动画还没有完成。

为了避免这个情况，您可以以参数的形式添加 Callback 函数。

### jQuery Callback 函数

当动画 100% 完成后，即调用 Callback 函数。

**典型的语法：**

```
$(selector).hide(speed,callback)
```

*callback* 参数是一个在 hide 操作完成后被执行的函数。

### 错误（没有 callback）

```
$("p").hide(1000);
alert("The paragraph is now hidden");
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_hide_slow_wrong)

### 正确（有 callback）

```
$("p").hide(1000,function(){
alert("The paragraph is now hidden");
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_hide_slow_right)

结论：如果您希望在一个涉及动画的函数之后来执行语句，请使用 callback 函数。

## Chaining

**通过 jQuery，您可以把动作/方法链接起来。**

**Chaining 允许我们在一条语句中允许多个 jQuery 方法（在相同的元素上）。**

### jQuery 方法链接

直到现在，我们都是一次写一条 jQuery 语句（一条接着另一条）。

不过，有一种名为链接（chaining）的技术，允许我们在相同的元素上运行多条 jQuery 命令，一条接着另一条。

提示：这样的话，浏览器就不必多次查找相同的元素。

如需链接一个动作，您只需简单地把该动作追加到之前的动作上。

**例子** 1

下面的例子把 css(), slideUp(), and slideDown() 链接在一起。"p1" 元素首先会变为红色，然后向上滑动，然后向下滑动：

```
$("#p1").css("color","red").slideUp(2000).slideDown(2000);
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_chaining)

如果需要，我们也可以添加多个方法调用。

提示：当进行链接时，代码行会变得很差。不过，jQuery 在语法上不是很严格；您可以按照希望的格式来写，包含折行和缩进。

**例子** 2

这样写也可以运行：

```
$("#p1").css("color","red")
  .slideUp(2000)
  .slideDown(2000);
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_chaining2)

jQuery 会抛掉多余的空格，并按照一行长代码来执行上面的代码行。  

# jQuery HTML操作

## jQuery HTML 参考手册

如需有关 jQuery HTML 方法的完整内容，请访问以下参考手册：

### jQuery 文档操作方法

这些方法对于 XML 文档和 HTML 文档均是适用的，除了：html()。

| 方法                                                         | 描述                                                   |
| ------------------------------------------------------------ | ------------------------------------------------------ |
| [addClass()](http://www.w3school.com.cn/jquery/attributes_addclass.asp) | 向匹配的元素添加指定的类名。                           |
| [after()](http://www.w3school.com.cn/jquery/manipulation_after.asp) | 在匹配的元素之后插入内容。                             |
| [append()](http://www.w3school.com.cn/jquery/manipulation_append.asp) | 向匹配元素集合中的每个元素结尾插入由参数指定的内容。   |
| [appendTo()](http://www.w3school.com.cn/jquery/manipulation_appendto.asp) | 向目标结尾插入匹配元素集合中的每个元素。               |
| [attr()](http://www.w3school.com.cn/jquery/attributes_attr.asp) | 设置或返回匹配元素的属性和值。                         |
| [before()](http://www.w3school.com.cn/jquery/manipulation_before.asp) | 在每个匹配的元素之前插入内容。                         |
| [clone()](http://www.w3school.com.cn/jquery/manipulation_clone.asp) | 创建匹配元素集合的副本。                               |
| [detach()](http://www.w3school.com.cn/jquery/manipulation_detach.asp) | 从 DOM 中移除匹配元素集合。                            |
| [empty()](http://www.w3school.com.cn/jquery/manipulation_empty.asp) | 删除匹配的元素集合中所有的子节点。                     |
| [hasClass()](http://www.w3school.com.cn/jquery/attributes_hasclass.asp) | 检查匹配的元素是否拥有指定的类。                       |
| [html()](http://www.w3school.com.cn/jquery/manipulation_html.asp) | 设置或返回匹配的元素集合中的 HTML 内容。               |
| [insertAfter()](http://www.w3school.com.cn/jquery/manipulation_insertafter.asp) | 把匹配的元素插入到另一个指定的元素集合的后面。         |
| [insertBefore()](http://www.w3school.com.cn/jquery/manipulation_insertbefore.asp) | 把匹配的元素插入到另一个指定的元素集合的前面。         |
| [prepend()](http://www.w3school.com.cn/jquery/manipulation_prepend.asp) | 向匹配元素集合中的每个元素开头插入由参数指定的内容。   |
| [prependTo()](http://www.w3school.com.cn/jquery/manipulation_perpendto.asp) | 向目标开头插入匹配元素集合中的每个元素。               |
| [remove()](http://www.w3school.com.cn/jquery/manipulation_remove.asp) | 移除所有匹配的元素。                                   |
| [removeAttr()](http://www.w3school.com.cn/jquery/attributes_removeattr.asp) | 从所有匹配的元素中移除指定的属性。                     |
| [removeClass()](http://www.w3school.com.cn/jquery/attributes_removeclass.asp) | 从所有匹配的元素中删除全部或者指定的类。               |
| [replaceAll()](http://www.w3school.com.cn/jquery/manipulation_replaceall.asp) | 用匹配的元素替换所有匹配到的元素。                     |
| [replaceWith()](http://www.w3school.com.cn/jquery/manipulation_replacewith.asp) | 用新内容替换匹配的元素。                               |
| [text()](http://www.w3school.com.cn/jquery/manipulation_text.asp) | 设置或返回匹配元素的内容。                             |
| [toggleClass()](http://www.w3school.com.cn/jquery/attributes_toggleclass.asp) | 从匹配的元素中添加或删除一个类。                       |
| [unwrap()](http://www.w3school.com.cn/jquery/manipulation_unwrap.asp) | 移除并替换指定元素的父元素。                           |
| [val()](http://www.w3school.com.cn/jquery/attributes_val.asp) | 设置或返回匹配元素的值。                               |
| [wrap()](http://www.w3school.com.cn/jquery/manipulation_wrap.asp) | 把匹配的元素用指定的内容或元素包裹起来。               |
| [wrapAll()](http://www.w3school.com.cn/jquery/manipulation_wrapall.asp) | 把所有匹配的元素用指定的内容或元素包裹起来。           |
| [wrapinner()](http://www.w3school.com.cn/jquery/manipulation_wrapinner.asp) | 将每一个匹配的元素的子内容用指定的内容或元素包裹起来。 |

### jQuery 属性操作方法

下面列出的这些方法获得或设置元素的 DOM 属性。

这些方法对于 XML 文档和 HTML 文档均是适用的，除了：html()。

| 方法                                                         | 描述                                     |
| ------------------------------------------------------------ | ---------------------------------------- |
| [addClass()](http://www.w3school.com.cn/jquery/attributes_addclass.asp) | 向匹配的元素添加指定的类名。             |
| [attr()](http://www.w3school.com.cn/jquery/attributes_attr.asp) | 设置或返回匹配元素的属性和值。           |
| [hasClass()](http://www.w3school.com.cn/jquery/attributes_hasclass.asp) | 检查匹配的元素是否拥有指定的类。         |
| [html()](http://www.w3school.com.cn/jquery/manipulation_html.asp) | 设置或返回匹配的元素集合中的 HTML 内容。 |
| [removeAttr()](http://www.w3school.com.cn/jquery/attributes_removeattr.asp) | 从所有匹配的元素中移除指定的属性。       |
| [removeClass()](http://www.w3school.com.cn/jquery/attributes_removeclass.asp) | 从所有匹配的元素中删除全部或者指定的类。 |
| [toggleClass()](http://www.w3school.com.cn/jquery/attributes_toggleclass.asp) | 从匹配的元素中添加或删除一个类。         |
| [val()](http://www.w3school.com.cn/jquery/attributes_val.asp) | 设置或返回匹配元素的值。                 |

注释：[jQuery 文档操作参考手册](http://www.w3school.com.cn/jquery/jquery_ref_manipulation.asp)中也列出了以上方法。本参考页的作用是方便用户单独查阅有关属性操作方面的方法。

### jQuery CSS 操作函数

下面列出的这些方法设置或返回元素的 CSS 相关属性。

| CSS 属性                                                     | 描述                                     |
| ------------------------------------------------------------ | ---------------------------------------- |
| [css()](http://www.w3school.com.cn/jquery/css_css.asp)       | 设置或返回匹配元素的样式属性。           |
| [height()](http://www.w3school.com.cn/jquery/css_height.asp) | 设置或返回匹配元素的高度。               |
| [offset()](http://www.w3school.com.cn/jquery/css_offset.asp) | 返回第一个匹配元素相对于文档的位置。     |
| [offsetParent()](http://www.w3school.com.cn/jquery/css_offsetparent.asp) | 返回最近的定位祖先元素。                 |
| [position()](http://www.w3school.com.cn/jquery/css_position.asp) | 返回第一个匹配元素相对于父元素的位置。   |
| [scrollLeft()](http://www.w3school.com.cn/jquery/css_scrollleft.asp) | 设置或返回匹配元素相对滚动条左侧的偏移。 |
| [scrollTop()](http://www.w3school.com.cn/jquery/css_scrolltop.asp) | 设置或返回匹配元素相对滚动条顶部的偏移。 |
| [width()](http://www.w3school.com.cn/jquery/css_width.asp)   | 设置或返回匹配元素的宽度。               |

## jQuery DOM 获取操作

jQuery 中非常重要的部分，就是操作 DOM 的能力。

jQuery 提供一系列与 DOM 相关的方法，这使访问和操作元素和属性变得很容易。

提示：DOM = Document Object Model（文档对象模型）

DOM 定义访问 HTML 和 XML 文档的标准：

“W3C 文档对象模型独立于平台和语言的界面，允许程序和脚本动态访问和更新文档的内容、结构以及样式。”

### 获得内容 - text()、html() 以及 val()

三个简单实用的用于 DOM 操作的 jQuery 方法：

- text() - 设置或返回所选元素的文本内容
- html() - 设置或返回所选元素的内容（包括 HTML 标记）
- val() - 设置或返回表单字段的值

下面的例子演示如何通过 jQuery text() 和 html() 方法来获得内容：

**实例**

```
$("#btn1").click(function(){
  alert("Text: " + $("#test").text());
});
$("#btn2").click(function(){
  alert("HTML: " + $("#test").html());
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_dom_html_get)

下面的例子演示如何通过 jQuery val() 方法获得输入字段的值：

**实例**

```
$("#btn1").click(function(){
  alert("Value: " + $("#test").val());
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_dom_val_get)

### 获取属性 - attr()

jQuery attr() 方法用于获取属性值。

下面的例子演示如何获得链接中 href 属性的值：

**实例**

```
$("button").click(function(){
  alert($("#w3s").attr("href"));
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_dom_attr_get)

下一章会讲解如何设置（改变）内容和属性值。

##   jQuery - 设置内容和属性

### 设置内容 - text()、html() 以及 val()

我们将使用前一章中的三个相同的方法来设置内容：

- text() - 设置或返回所选元素的文本内容
- html() - 设置或返回所选元素的内容（包括 HTML 标记）
- val() - 设置或返回表单字段的值

下面的例子演示如何通过 text()、html() 以及 val() 方法来设置内容：

**实例**

```
$("#btn1").click(function(){
  $("#test1").text("Hello world!");
});
$("#btn2").click(function(){
  $("#test2").html("<b>Hello world!</b>");
});
$("#btn3").click(function(){
  $("#test3").val("Dolly Duck");
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_dom_html_set)

### text()、html() 以及 val() 的回调函数

上面的三个 jQuery 方法：text()、html() 以及 val()，同样拥有回调函数。回调函数由两个参数：被选元素列表中当前元素的下标，以及原始（旧的）值。然后以函数新值返回您希望使用的字符串。

下面的例子演示带有回调函数的 text() 和 html()：

**实例**

```
$("#btn1").click(function(){
  $("#test1").text(function(i,origText){
    return "Old text: " + origText + " New text: Hello world!
    (index: " + i + ")";
  });
});

$("#btn2").click(function(){
  $("#test2").html(function(i,origText){
    return "Old html: " + origText + " New html: Hello <b>world!</b>
    (index: " + i + ")";
  });
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_dom_html_callback)

### 设置属性 - attr()

jQuery attr() 方法也用于设置/改变属性值。

下面的例子演示如何改变（设置）链接中 href 属性的值：

**实例**

```
$("button").click(function(){
  $("#w3s").attr("href","http://www.w3school.com.cn/jquery");
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_dom_attr_set)

attr() 方法也允许您同时设置多个属性。

下面的例子演示如何同时设置 href 和 title 属性：

**实例**

```
$("button").click(function(){
  $("#w3s").attr({
    "href" : "http://www.w3school.com.cn/jquery",
    "title" : "W3School jQuery Tutorial"
  });
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_dom_attr_set2)

### attr() 的回调函数

jQuery 方法 attr()，也提供回调函数。回调函数由两个参数：被选元素列表中当前元素的下标，以及原始（旧的）值。然后以函数新值返回您希望使用的字符串。

下面的例子演示带有回调函数的 attr() 方法：

**实例**

```
$("button").click(function(){
  $("#w3s").attr("href", function(i,origValue){
    return origValue + "/jquery";
  });
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_dom_attr_callback)

## jQuery - 添加元素



**通过 jQuery，可以很容易地添加新元素/内容。**

### 添加新的 HTML 内容

我们将学习用于添加新内容的四个 jQuery 方法：

- append() - 在被选元素的结尾插入内容
- prepend() - 在被选元素的开头插入内容
- after() - 在被选元素之后插入内容
- before() - 在被选元素之前插入内容

### jQuery append() 方法

jQuery append() 方法在被选元素的结尾插入内容。

**实例**

```
$("p").append("Some appended text.");
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_html_append)

### jQuery prepend() 方法

jQuery prepend() 方法在被选元素的开头插入内容。

**实例**

```
$("p").prepend("Some prepended text.");
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_html_prepend)

### 通过 append() 和 prepend() 方法添加若干新元素

在上面的例子中，我们只在被选元素的开头/结尾插入文本/HTML。

不过，append() 和 prepend() 方法能够通过参数接收无限数量的新元素。可以通过 jQuery 来生成文本/HTML（就像上面的例子那样），或者通过 JavaScript 代码和 DOM 元素。

在下面的例子中，我们创建若干个新元素。这些元素可以通过 text/HTML、jQuery 或者 JavaScript/DOM 来创建。然后我们通过 append() 方法把这些新元素追加到文本中（对 prepend() 同样有效）：

**实例**

```
function appendText()
{
var txt1="<p>Text.</p>";               // 以 HTML 创建新元素
var txt2=$("<p></p>").text("Text.");   // 以 jQuery 创建新元素
var txt3=document.createElement("p");  // 以 DOM 创建新元素
txt3.innerHTML="Text.";
$("p").append(txt1,txt2,txt3);         // 追加新元素
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_html_append2)

### jQuery after() 和 before() 方法

jQuery after() 方法在被选元素之后插入内容。

jQuery before() 方法在被选元素之前插入内容。

**实例**

```
$("img").after("Some text after");

$("img").before("Some text before");
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_html_after)

### 通过 after() 和 before() 方法添加若干新元素

after() 和 before() 方法能够通过参数接收无限数量的新元素。可以通过 text/HTML、jQuery 或者 JavaScript/DOM 来创建新元素。

在下面的例子中，我们创建若干新元素。这些元素可以通过 text/HTML、jQuery 或者 JavaScript/DOM 来创建。然后我们通过 after() 方法把这些新元素插到文本中（对 before() 同样有效）：

**实例**

```
function afterText()
{
var txt1="<b>I </b>";                    // 以 HTML 创建新元素
var txt2=$("<i></i>").text("love ");     // 通过 jQuery 创建新元素
var txt3=document.createElement("big");  // 通过 DOM 创建新元素
txt3.innerHTML="jQuery!";
$("img").after(txt1,txt2,txt3);          // 在 img 之后插入新元素
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_html_after2)

## jQuery - 删除元素



**通过 jQuery，可以很容易地删除已有的 HTML 元素。**

### 删除元素/内容

如需删除元素和内容，一般可使用以下两个 jQuery 方法：

- remove() - 删除被选元素（及其子元素）
- empty() - 从被选元素中删除子元素

### jQuery remove() 方法

jQuery remove() 方法删除被选元素及其子元素。

**实例**

```
$("#div1").remove();
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_dom_remove)

### jQuery empty() 方法

jQuery empty() 方法删除被选元素的子元素。

**实例**

```
$("#div1").empty();
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_dom_empty)

### 过滤被删除的元素

jQuery remove() 方法也可接受一个参数，允许您对被删元素进行过滤。

该参数可以是任何 jQuery 选择器的语法。

下面的例子删除 class="italic" 的所有 <p> 元素：

**实例**

```
$("p").remove(".italic");
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_dom_remove2)

## jQuery - 获取并设置 CSS 类

**通过 jQuery，可以很容易地对 CSS 元素进行操作。**

### jQuery 操作 CSS

jQuery 拥有若干进行 CSS 操作的方法。我们将学习下面这些：

- addClass() - 向被选元素添加一个或多个类
- removeClass() - 从被选元素删除一个或多个类
- toggleClass() - 对被选元素进行添加/删除类的切换操作
- css() - 设置或返回样式属性

### 实例样式表

下面的样式表将用于本页的所有例子：

```
.important
{
font-weight:bold;
font-size:xx-large;
}

.blue
{
color:blue;
}
```

### jQuery addClass() 方法

下面的例子展示如何向不同的元素添加 class 属性。当然，在添加类时，您也可以选取多个元素：

**实例**

```
$("button").click(function(){
  $("h1,h2,p").addClass("blue");
  $("div").addClass("important");
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_dom_addclass)

您也可以在 addClass() 方法中规定多个类：

**实例**

```
$("button").click(function(){
  $("#div1").addClass("important blue");
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_dom_addclass2)

### jQuery removeClass() 方法

下面的例子演示如何不同的元素中删除指定的 class 属性：

**实例**

```
$("button").click(function(){
  $("h1,h2,p").removeClass("blue");
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_dom_removeclass)

### jQuery toggleClass() 方法

下面的例子将展示如何使用 jQuery toggleClass() 方法。该方法对被选元素进行添加/删除类的切换操作：

**实例**

```
$("button").click(function(){
  $("h1,h2,p").toggleClass("blue");
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_dom_toggleclass)

## jQuery - css() 方法

### jQuery css() 方法

css() 方法设置或返回被选元素的一个或多个样式属性。

### 返回 CSS 属性

如需返回指定的 CSS 属性的值，请使用如下语法：

```
css("propertyname");
```

下面的例子将返回首个匹配元素的 background-color 值：

**实例**

```
$("p").css("background-color");
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_css_getcolor)

### 设置 CSS 属性

如需设置指定的 CSS 属性，请使用如下语法：

```
css("propertyname","value");
```

下面的例子将为所有匹配元素设置 background-color 值：

**实例**

```
$("p").css("background-color","yellow");
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_css_setcolor)

### 设置多个 CSS 属性

如需设置多个 CSS 属性，请使用如下语法：

```
css({"propertyname":"value","propertyname":"value",...});
```

下面的例子将为所有匹配元素设置 background-color 和 font-size：

**实例**

```
$("p").css({"background-color":"yellow","font-size":"200%"});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_css_set_multiple)

## jQuery - 尺寸

**通过 jQuery，很容易处理元素和浏览器窗口的尺寸。**

### jQuery 尺寸 方法

jQuery 提供多个处理尺寸的重要方法：

- width()
- height()
- innerWidth()
- innerHeight()
- outerWidth()
- outerHeight()

### jQuery width() 和 height() 方法

width() 方法设置或返回元素的宽度（不包括内边距、边框或外边距）。

height() 方法设置或返回元素的高度（不包括内边距、边框或外边距）。

下面的例子返回指定的 <div> 元素的宽度和高度：

**实例**

```
$("button").click(function(){
  var txt="";
  txt+="Width: " + $("#div1").width() + "</br>";
  txt+="Height: " + $("#div1").height();
  $("#div1").html(txt);
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_dim_width_height)

### jQuery innerWidth() 和 innerHeight() 方法

innerWidth() 方法返回元素的宽度（包括内边距）。

innerHeight() 方法返回元素的高度（包括内边距）。

下面的例子返回指定的 <div> 元素的 inner-width/height：

**实例**

```
$("button").click(function(){
  var txt="";
  txt+="Inner width: " + $("#div1").innerWidth() + "</br>";
  txt+="Inner height: " + $("#div1").innerHeight();
  $("#div1").html(txt);
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_dim_innerwidth_innerheight)

### jQuery outerWidth() 和 outerHeight() 方法

outerWidth() 方法返回元素的宽度（包括内边距和边框）。

outerHeight() 方法返回元素的高度（包括内边距和边框）。

下面的例子返回指定的 <div> 元素的 outer-width/height：

**实例**

```
$("button").click(function(){
  var txt="";
  txt+="Outer width: " + $("#div1").outerWidth() + "</br>";
  txt+="Outer height: " + $("#div1").outerHeight();
  $("#div1").html(txt);
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_dim_outerwidth_outerheight)

outerWidth(true) 方法返回元素的宽度（包括内边距、边框和外边距）。

outerHeight(true) 方法返回元素的高度（包括内边距、边框和外边距）。

**实例**

```
$("button").click(function(){
  var txt="";
  txt+="Outer width (+margin): " + $("#div1").outerWidth(true) + "</br>";
  txt+="Outer height (+margin): " + $("#div1").outerHeight(true);
  $("#div1").html(txt);
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_dim_outerwidth_outerheight2)

### jQuery - 更多的 width() 和 height()

下面的例子返回文档（HTML 文档）和窗口（浏览器视口）的宽度和高度：

**实例**

```
$("button").click(function(){
  var txt="";
  txt+="Document width/height: " + $(document).width();
  txt+="x" + $(document).height() + "\n";
  txt+="Window width/height: " + $(window).width();
  txt+="x" + $(window).height();
  alert(txt);
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_dim_width_height2)

下面的例子设置指定的 <div> 元素的宽度和高度：

**实例**

```
$("button").click(function(){
  $("#div1").width(500).height(500);
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_dim_width_height_set)

# jQuery 遍历

## jQuery 遍历简介

### 什么是遍历？

jQuery 遍历，意为“移动”，用于根据其相对于其他元素的关系来“查找”（或选取）HTML 元素。以某项选择开始，并沿着这个选择移动，直到抵达您期望的元素为止。

下图展示了一个家族树。通过 jQuery 遍历，您能够从被选（当前的）元素开始，轻松地在家族树中向上移动（祖先），向下移动（子孙），水平移动（同胞）。这种移动被称为对 DOM 进行遍历。

### 图示解释：

![遍历 DOM 树](http://www.w3school.com.cn/i/dom_tree.gif)

- <div> 元素是 <ul> 的父元素，同时是其中所有内容的祖先。
- <ul> 元素是 <li> 元素的父元素，同时是 <div> 的子元素
- 左边的 <li> 元素是 <span> 的父元素，<ul> 的子元素，同时是 <div> 的后代。
- <span> 元素是 <li> 的子元素，同时是 <ul> 和 <div> 的后代。
- 两个 <li> 元素是同胞（拥有相同的父元素）。
- 右边的 <li> 元素是 <b> 的父元素，<ul> 的子元素，同时是 <div> 的后代。
- <b> 元素是右边的 <li> 的子元素，同时是 <ul> 和 <div> 的后代。

提示：祖先是父、祖父、曾祖父等等。后代是子、孙、曾孙等等。同胞拥有相同的父。

### 遍历 DOM

jQuery 提供了多种遍历 DOM 的方法。

遍历方法中最大的种类是树遍历（tree-traversal）。

下一章会讲解如何在 DOM 树中向上、下以及同级移动。

## jQuery 遍历参考手册

如需了解所有的 jQuery 遍历方法，请访问我们的 [jQuery 遍历参考手册](http://www.w3school.com.cn/jquery/jquery_ref_traversing.asp)。

### jQuery 遍历函数

jQuery 遍历函数包括了用于筛选、查找和串联元素的方法。

| 函数                                                         | 描述                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| [.add()](http://www.w3school.com.cn/jquery/traversing_add.asp) | 将元素添加到匹配元素的集合中。                               |
| [.andSelf()](http://www.w3school.com.cn/jquery/traversing_andSelf.asp) | 把堆栈中之前的元素集添加到当前集合中。                       |
| [.children()](http://www.w3school.com.cn/jquery/traversing_children.asp) | 获得匹配元素集合中每个元素的所有子元素。                     |
| [.closest()](http://www.w3school.com.cn/jquery/traversing_closest.asp) | 从元素本身开始，逐级向上级元素匹配，并返回最先匹配的祖先元素。 |
| [.contents()](http://www.w3school.com.cn/jquery/traversing_contents.asp) | 获得匹配元素集合中每个元素的子元素，包括文本和注释节点。     |
| [.each()](http://www.w3school.com.cn/jquery/traversing_each.asp) | 对 jQuery 对象进行迭代，为每个匹配元素执行函数。             |
| [.end()](http://www.w3school.com.cn/jquery/traversing_end.asp) | 结束当前链中最近的一次筛选操作，并将匹配元素集合返回到前一次的状态。 |
| [.eq()](http://www.w3school.com.cn/jquery/traversing_eq.asp) | 将匹配元素集合缩减为位于指定索引的新元素。                   |
| [.filter()](http://www.w3school.com.cn/jquery/traversing_filter.asp) | 将匹配元素集合缩减为匹配选择器或匹配函数返回值的新元素。     |
| [.find()](http://www.w3school.com.cn/jquery/traversing_find.asp) | 获得当前匹配元素集合中每个元素的后代，由选择器进行筛选。     |
| [.first()](http://www.w3school.com.cn/jquery/traversing_first.asp) | 将匹配元素集合缩减为集合中的第一个元素。                     |
| [.has()](http://www.w3school.com.cn/jquery/traversing_has.asp) | 将匹配元素集合缩减为包含特定元素的后代的集合。               |
| [.is()](http://www.w3school.com.cn/jquery/traversing_is.asp) | 根据选择器检查当前匹配元素集合，如果存在至少一个匹配元素，则返回 true。 |
| [.last()](http://www.w3school.com.cn/jquery/traversing_last.asp) | 将匹配元素集合缩减为集合中的最后一个元素。                   |
| [.map()](http://www.w3school.com.cn/jquery/traversing_map.asp) | 把当前匹配集合中的每个元素传递给函数，产生包含返回值的新 jQuery 对象。 |
| [.next()](http://www.w3school.com.cn/jquery/traversing_next.asp) | 获得匹配元素集合中每个元素紧邻的同辈元素。                   |
| [.nextAll()](http://www.w3school.com.cn/jquery/traversing_nextall.asp) | 获得匹配元素集合中每个元素之后的所有同辈元素，由选择器进行筛选（可选）。 |
| [.nextUntil()](http://www.w3school.com.cn/jquery/traversing_nextuntil.asp) | 获得每个元素之后所有的同辈元素，直到遇到匹配选择器的元素为止。 |
| [.not()](http://www.w3school.com.cn/jquery/traversing_not.asp) | 从匹配元素集合中删除元素。                                   |
| [.offsetParent()](http://www.w3school.com.cn/jquery/traversing_offsetparent.asp) | 获得用于定位的第一个父元素。                                 |
| [.parent()](http://www.w3school.com.cn/jquery/traversing_parent.asp) | 获得当前匹配元素集合中每个元素的父元素，由选择器筛选（可选）。 |
| [.parents()](http://www.w3school.com.cn/jquery/traversing_parents.asp) | 获得当前匹配元素集合中每个元素的祖先元素，由选择器筛选（可选）。 |
| [.parentsUntil()](http://www.w3school.com.cn/jquery/traversing_parentsuntil.asp) | 获得当前匹配元素集合中每个元素的祖先元素，直到遇到匹配选择器的元素为止。 |
| [.prev()](http://www.w3school.com.cn/jquery/traversing_prev.asp) | 获得匹配元素集合中每个元素紧邻的前一个同辈元素，由选择器筛选（可选）。 |
| [.prevAll()](http://www.w3school.com.cn/jquery/traversing_prevall.asp) | 获得匹配元素集合中每个元素之前的所有同辈元素，由选择器进行筛选（可选）。 |
| [.prevUntil()](http://www.w3school.com.cn/jquery/traversing_prevuntil.asp) | 获得每个元素之前所有的同辈元素，直到遇到匹配选择器的元素为止。 |
| [.siblings()](http://www.w3school.com.cn/jquery/traversing_siblings.asp) | 获得匹配元素集合中所有元素的同辈元素，由选择器筛选（可选）。 |
| [.slice()](http://www.w3school.com.cn/jquery/traversing_slice.asp) | 将匹配元素集合缩减为指定范围的子集。                         |

## jQuery 遍历 - 祖先

祖先是父、祖父或曾祖父等等。

通过 jQuery，您能够向上遍历 DOM 树，以查找元素的祖先。

### 向上遍历 DOM 树

这些 jQuery 方法很有用，它们用于向上遍历 DOM 树：

- parent()
- parents()
- parentsUntil()

### jQuery parent() 方法

parent() 方法返回被选元素的直接父元素。

该方法只会向上一级对 DOM 树进行遍历。

下面的例子返回每个 <span> 元素的的直接父元素：

**实例**

```
$(document).ready(function(){
  $("span").parent();
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_parent)

### jQuery parents() 方法

parents() 方法返回被选元素的所有祖先元素，它一路向上直到文档的根元素 (<html>)。

下面的例子返回所有 <span> 元素的所有祖先：

**实例**

```
$(document).ready(function(){
  $("span").parents();
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_parents)

您也可以使用可选参数来过滤对祖先元素的搜索。

下面的例子返回所有 <span> 元素的所有祖先，并且它是 <ul> 元素：

**实例**

```
$(document).ready(function(){
  $("span").parents("ul");
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_parents2)

### jQuery parentsUntil() 方法

parentsUntil() 方法返回介于两个给定元素之间的所有祖先元素。

下面的例子返回介于 <span> 与 <div> 元素之间的所有祖先元素：

**实例**

```
$(document).ready(function(){
  $("span").parentsUntil("div");
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_parentsuntil)

## jQuery 遍历 - 后代



后代是子、孙、曾孙等等。

通过 jQuery，您能够向下遍历 DOM 树，以查找元素的后代。

### 向下遍历 DOM 树

下面是两个用于向下遍历 DOM 树的 jQuery 方法：

- children()
- find()

### jQuery children() 方法

children() 方法返回被选元素的所有直接子元素。

该方法只会向下一级对 DOM 树进行遍历。

下面的例子返回每个 <div> 元素的所有直接子元素：

**实例**

```
$(document).ready(function(){
  $("div").children();
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_children)

您也可以使用可选参数来过滤对子元素的搜索。

下面的例子返回类名为 "1" 的所有 <p> 元素，并且它们是 <div> 的直接子元素：

**实例**

```
$(document).ready(function(){
  $("div").children("p.1");
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_children2)

### jQuery find() 方法

find() 方法返回被选元素的后代元素，一路向下直到最后一个后代。

下面的例子返回属于 <div> 后代的所有 <span> 元素：

**实例**

```
$(document).ready(function(){
  $("div").find("span");
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_find)

下面的例子返回 <div> 的所有后代：

**实例**

```
$(document).ready(function(){
  $("div").find("*");
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_find2)

##   jQuery 遍历 - 同胞

- [jQuery 后代](http://www.w3school.com.cn/jquery/jquery_traversing_descendants.asp)
- [jQuery 过滤](http://www.w3school.com.cn/jquery/jquery_traversing_filtering.asp)

同胞拥有相同的父元素。

通过 jQuery，您能够在 DOM 树中遍历元素的同胞元素。

### 在 DOM 树中水平遍历

有许多有用的方法让我们在 DOM 树进行水平遍历：

- siblings()
- next()
- nextAll()
- nextUntil()
- prev()
- prevAll()
- prevUntil()

### jQuery siblings() 方法

siblings() 方法返回被选元素的所有同胞元素。

下面的例子返回 <h2> 的所有同胞元素：

**实例**

```
$(document).ready(function(){
  $("h2").siblings();
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_siblings)

您也可以使用可选参数来过滤对同胞元素的搜索。

下面的例子返回属于 <h2> 的同胞元素的所有 <p> 元素：

**实例**

```
$(document).ready(function(){
  $("h2").siblings("p");
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_siblings2)

### jQuery next() 方法

next() 方法返回被选元素的下一个同胞元素。

该方法只返回一个元素。

下面的例子返回 <h2> 的下一个同胞元素：

**实例**

```
$(document).ready(function(){
  $("h2").next();
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_next)

### jQuery nextAll() 方法

nextAll() 方法返回被选元素的所有跟随的同胞元素。

下面的例子返回 <h2> 的所有跟随的同胞元素：

**实例**

```
$(document).ready(function(){
  $("h2").nextAll();
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_nextall)

### jQuery nextUntil() 方法

nextUntil() 方法返回介于两个给定参数之间的所有跟随的同胞元素。

下面的例子返回介于 <h2> 与 <h6> 元素之间的所有同胞元素：

**实例**

```
$(document).ready(function(){
  $("h2").nextUntil("h6");
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_nextuntil)

### jQuery prev(), prevAll() & prevUntil() 方法

prev(), prevAll() 以及 prevUntil() 方法的工作方式与上面的方法类似，只不过方向相反而已：它们返回的是前面的同胞元素（在 DOM 树中沿着同胞元素向后遍历，而不是向前）。

## jQuery 遍历 - 过滤

### 缩写搜索元素的范围

三个最基本的过滤方法是：first(), last() 和 eq()，它们允许您基于其在一组元素中的位置来选择一个特定的元素。

其他过滤方法，比如 filter() 和 not() 允许您选取匹配或不匹配某项指定标准的元素。

### jQuery first() 方法

first() 方法返回被选元素的首个元素。

下面的例子选取首个 <div> 元素内部的第一个 <p> 元素：

实例

```
$(document).ready(function(){
  $("div p").first();
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_first)

### jQuery last() 方法

last() 方法返回被选元素的最后一个元素。

下面的例子选择最后一个 <div> 元素中的最后一个 <p> 元素：

**实例**

```
$(document).ready(function(){
  $("div p").last();
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_last)

### jQuery eq() 方法

eq() 方法返回被选元素中带有指定索引号的元素。

索引号从 0 开始，因此首个元素的索引号是 0 而不是 1。下面的例子选取第二个 <p> 元素（索引号 1）：

**实例**

```
$(document).ready(function(){
  $("p").eq(1);
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_eq)

### jQuery filter() 方法

filter() 方法允许您规定一个标准。不匹配这个标准的元素会被从集合中删除，匹配的元素会被返回。

下面的例子返回带有类名 "intro" 的所有 <p> 元素：

**实例**

```
$(document).ready(function(){
  $("p").filter(".intro");
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_filter)

### jQuery not() 方法

not() 方法返回不匹配标准的所有元素。

提示：not() 方法与 filter() 相反。

下面的例子返回不带有类名 "intro" 的所有 <p> 元素：

**实例**

```
$(document).ready(function(){
  $("p").not(".intro");
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_not)

# jQuery - AJAX 

## jQuery - AJAX 简介



**AJAX 是与服务器交换数据的艺术，它在不重载全部页面的情况下，实现了对部分网页的更新。**

### jQuery AJAX 实例

**请点击下面的按钮，通过 jQuery AJAX 改变这段文本。**

 

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_ajax_load)

### 什么是 AJAX？

AJAX = 异步 JavaScript 和 XML（Asynchronous JavaScript and XML）。

简短地说，在不重载整个网页的情况下，AJAX 通过后台加载数据，并在网页上进行显示。

使用 AJAX 的应用程序案例：谷歌地图、腾讯微博、优酷视频、人人网等等。

您可以在我们的 [AJAX 教程](http://www.w3school.com.cn/ajax/index.asp)中学到更多有关 AJAX 的知识。

### 关于 jQuery 与 AJAX

jQuery 提供多个与 AJAX 有关的方法。

通过 jQuery AJAX 方法，您能够使用 HTTP Get 和 HTTP Post 从远程服务器上请求文本、HTML、XML 或 JSON - 同时您能够把这些外部数据直接载入网页的被选元素中。

提示：如果没有 jQuery，AJAX 编程还是有些难度的。

编写常规的 AJAX 代码并不容易，因为不同的浏览器对 AJAX 的实现并不相同。这意味着您必须编写额外的代码对浏览器进行测试。不过，jQuery 团队为我们解决了这个难题，我们只需要一行简单的代码，就可以实现 AJAX 功能。

## jQuery AJAX 参考手册

如需完整的 AJAX 方法参考，请访问我们的 [jQuery AJAX 参考手册](http://www.w3school.com.cn/jquery/jquery_ref_ajax.asp)。

## jQuery Ajax 操作函数

jQuery 库拥有完整的 Ajax 兼容套件。其中的函数和方法允许我们在不刷新浏览器的情况下从服务器加载数据。

| 函数                                                         | 描述                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| [jQuery.ajax()](http://www.w3school.com.cn/jquery/ajax_ajax.asp) | 执行异步 HTTP (Ajax) 请求。                                  |
| [.ajaxComplete()](http://www.w3school.com.cn/jquery/ajax_ajaxcomplete.asp) | 当 Ajax 请求完成时注册要调用的处理程序。这是一个 Ajax 事件。 |
| [.ajaxError()](http://www.w3school.com.cn/jquery/ajax_ajaxerror.asp) | 当 Ajax 请求完成且出现错误时注册要调用的处理程序。这是一个 Ajax 事件。 |
| [.ajaxSend()](http://www.w3school.com.cn/jquery/ajax_ajaxsend.asp) | 在 Ajax 请求发送之前显示一条消息。                           |
| [jQuery.ajaxSetup()](http://www.w3school.com.cn/jquery/ajax_ajaxsetup.asp) | 设置将来的 Ajax 请求的默认值。                               |
| [.ajaxStart()](http://www.w3school.com.cn/jquery/ajax_ajaxstart.asp) | 当首个 Ajax 请求完成开始时注册要调用的处理程序。这是一个 Ajax 事件。 |
| [.ajaxStop()](http://www.w3school.com.cn/jquery/ajax_ajaxstop.asp) | 当所有 Ajax 请求完成时注册要调用的处理程序。这是一个 Ajax 事件。 |
| [.ajaxSuccess()](http://www.w3school.com.cn/jquery/ajax_ajaxsuccess.asp) | 当 Ajax 请求成功完成时显示一条消息。                         |
| [jQuery.get()](http://www.w3school.com.cn/jquery/ajax_get.asp) | 使用 HTTP GET 请求从服务器加载数据。                         |
| [jQuery.getJSON()](http://www.w3school.com.cn/jquery/ajax_getjson.asp) | 使用 HTTP GET 请求从服务器加载 JSON 编码数据。               |
| [jQuery.getScript()](http://www.w3school.com.cn/jquery/ajax_getscript.asp) | 使用 HTTP GET 请求从服务器加载 JavaScript 文件，然后执行该文件。 |
| [.load()](http://www.w3school.com.cn/jquery/ajax_load.asp)   | 从服务器加载数据，然后把返回到 HTML 放入匹配元素。           |
| [jQuery.param()](http://www.w3school.com.cn/jquery/ajax_param.asp) | 创建数组或对象的序列化表示，适合在 URL 查询字符串或 Ajax 请求中使用。 |
| [jQuery.post()](http://www.w3school.com.cn/jquery/ajax_post.asp) | 使用 HTTP POST 请求从服务器加载数据。                        |
| [.serialize()](http://www.w3school.com.cn/jquery/ajax_serialize.asp) | 将表单内容序列化为字符串。                                   |
| [.serializeArray()](http://www.w3school.com.cn/jquery/ajax_serializearray.asp) | 序列化表单元素，返回 JSON 数据结构数据。                     |

## jQuery - AJAX load() 方法



### jQuery load() 方法

jQuery load() 方法是简单但强大的 AJAX 方法。

load() 方法从服务器加载数据，并把返回的数据放入被选元素中。

**语法**：

```
$(selector).load(URL,data,callback);
```

必需的 *URL* 参数规定您希望加载的 URL。

可选的 *data* 参数规定与请求一同发送的查询字符串键/值对集合。

可选的 *callback* 参数是 load() 方法完成后所执行的函数名称。

这是示例文件（"demo_test.txt"）的内容：

```
<h2>jQuery and AJAX is FUN!!!</h2>
<p id="p1">This is some text in a paragraph.</p>
```

下面的例子会把文件 "demo_test.txt" 的内容加载到指定的 <div> 元素中：

**示例**

```
$("#div1").load("demo_test.txt");
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_ajax_load)

也可以把 jQuery 选择器添加到 URL 参数。

下面的例子把 "demo_test.txt" 文件中 id="p1" 的元素的内容，加载到指定的 <div> 元素中：

**实例**

```
$("#div1").load("demo_test.txt #p1");
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_ajax_load2)

可选的 callback 参数规定当 load() 方法完成后所要允许的回调函数。回调函数可以设置不同的参数：

- *responseTxt* - 包含调用成功时的结果内容
- *statusTXT* - 包含调用的状态
- *xhr* - 包含 XMLHttpRequest 对象

下面的例子会在 load() 方法完成后显示一个提示框。如果 load() 方法已成功，则显示“外部内容加载成功！”，而如果失败，则显示错误消息：

**实例**

```
$("button").click(function(){
  $("#div1").load("demo_test.txt",function(responseTxt,statusTxt,xhr){
    if(statusTxt=="success")
      alert("外部内容加载成功！");
    if(statusTxt=="error")
      alert("Error: "+xhr.status+": "+xhr.statusText);
  });
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_ajax_load_callback)

## jQuery - AJAX get() 和 post() 方法



**jQuery get() 和 post() 方法用于通过 HTTP GET 或 POST 请求从服务器请求数据。**

### HTTP 请求：GET vs. POST

两种在客户端和服务器端进行请求-响应的常用方法是：GET 和 POST。

- *GET* - 从指定的资源请求数据
- *POST* - 向指定的资源提交要处理的数据

GET 基本上用于从服务器获得（取回）数据。注释：GET 方法可能返回缓存数据。

POST 也可用于从服务器获取数据。不过，POST 方法不会缓存数据，并且常用于连同请求一起发送数据。

如需学习更多有关 GET 和 POST 以及两方法差异的知识，请阅读我们的 [HTTP 方法 - GET 对比 POST](http://www.w3school.com.cn/tags/html_ref_httpmethods.asp)。

### jQuery $.get() 方法

$.get() 方法通过 HTTP GET 请求从服务器上请求数据。

**语法**：

```
$.get(URL,callback);
```

必需的 *URL* 参数规定您希望请求的 URL。

可选的 *callback* 参数是请求成功后所执行的函数名。

下面的例子使用 $.get() 方法从服务器上的一个文件中取回数据：

**实例**

```
$("button").click(function(){
  $.get("demo_test.asp",function(data,status){
    alert("Data: " + data + "\nStatus: " + status);
  });
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_ajax_get)

$.get() 的第一个参数是我们希望请求的 URL（"demo_test.asp"）。

第二个参数是回调函数。第一个回调参数存有被请求页面的内容，第二个回调参数存有请求的状态。

提示：这个 ASP 文件 ("demo_test.asp") 类似这样：

```
<%
response.write("This is some text from an external ASP file.")
%>
```

### jQuery $.post() 方法

$.post() 方法通过 HTTP POST 请求从服务器上请求数据。

**语法**：

```
$.post(URL,data,callback);
```

必需的 *URL* 参数规定您希望请求的 URL。

可选的 *data* 参数规定连同请求发送的数据。

可选的 *callback* 参数是请求成功后所执行的函数名。

下面的例子使用 $.post() 连同请求一起发送数据：

**实例**

```
$("button").click(function(){
  $.post("demo_test_post.asp",
  {
    name:"Donald Duck",
    city:"Duckburg"
  },
  function(data,status){
    alert("Data: " + data + "\nStatus: " + status);
  });
});
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jquery_ajax_post)

$.post() 的第一个参数是我们希望请求的 URL ("demo_test_post.asp")。

然后我们连同请求（name 和 city）一起发送数据。

"demo_test_post.asp" 中的 ASP 脚本读取这些参数，对它们进行处理，然后返回结果。

第三个参数是回调函数。第一个回调参数存有被请求页面的内容，而第二个参数存有请求的状态。

提示：这个 ASP 文件 ("demo_test_post.asp") 类似这样：

```
<%
dim fname,city
fname=Request.Form("name")
city=Request.Form("city")
Response.Write("Dear " & fname & ". ")
Response.Write("Hope you live well in " & city & ".")
%>
```