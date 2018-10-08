# HTML入门到精通

# HTML入门

## HTML 简介

**实例**

```
<html>
<body>

<h1>我的第一个标题</h1>

<p>我的第一个段落。</p>

</body>
</html>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_intro)

### 什么是 HTML？

HTML 是用来描述网页的一种语言。

- HTML 指的是超文本标记语言 (**H**yper **T**ext **M**arkup **L**anguage)
- HTML 不是一种编程语言，而是一种*标记语言* (markup language)
- 标记语言是一套*标记标签* (markup tag)
- HTML 使用*标记标签*来描述网页

### HTML 标签

HTML 标记标签通常被称为 HTML 标签 (HTML tag)。

- HTML 标签是由*尖括号*包围的关键词，比如 <html>
- HTML 标签通常是*成对出现*的，比如 <b> 和 </b>
- 标签对中的第一个标签是*开始标签*，第二个标签是*结束标签*
- 开始和结束标签也被称为*开放标签*和*闭合标签*

### HTML 文档 = 网页

- HTML 文档*描述网页*
- HTML 文档*包含 HTML 标签*和纯文本
- HTML 文档也被称为*网页*

Web 浏览器的作用是读取 HTML 文档，并以网页的形式显示出它们。浏览器不会显示 HTML 标签，而是使用标签来解释页面的内容：

```
<html>
<body>

<h1>我的第一个标题</h1>

<p>我的第一个段落。</p>

</body>
</html>
```

### 例子解释

- <html> 与 </html> 之间的文本描述网页

- <body> 与 </body> 之间的文本是可见的页面内容

- h1 与 h1 之间的文本被显示为标题

- p 与 p 之间的文本被显示为段落

## HTML 编辑器



### 使用 Notepad 或 TextEdit 来编写 HTML

可以使用专业的 HTML 编辑器来编辑 HTML：

- Adobe Dreamweaver
- Microsoft Expression Web
- CoffeeCup HTML Editor

不过，我们同时推荐使用文本编辑器来学习 HTML，比如 Notepad (PC) 或 TextEdit (Mac)。我们相信，使用一款简单的文本编辑器是学习 HTML 的好方法。

通过记事本，依照以下四步来创建您的第一张网页。

### 步骤一：启动记事本

如何启动记事本：

开始
​    所有程序
​        附件
​            记事本

### 步骤二：用记事本来编辑 HTML

在记事本中键入 HTML 代码：

![记事本](http://www.w3school.com.cn/i/html_editor_notepad.gif)



### 步骤三：保存 HTML

在记事本的文件菜单选择“另存为”。

当您保存 HTML 文件时，既可以使用 .htm 也可以使用 .html 扩展名。两者没有区别，完全根据您的喜好。

在一个容易记忆的文件夹中保存这个文件，比如 w3school。

### 步骤四：在浏览器中运行这个 HTML 文件

启动您的浏览器，然后选择“文件”菜单的“打开文件”命令，或者直接在文件夹中双击您的 HTML 文件。

结果应该类似这样：

![在浏览器中查看](http://www.w3school.com.cn/i/html_editor_ie.gif)

##  HTML 基础标签 



**本章通过实例向您演示最常用的 HTML 标签。**

提示：不要担心本章中您还没有学过的例子，您将在下面的章节中学到它们。

提示：学习 HTML 最好的方式就是边学边做实验。我们为您准备了很好的 HTML 编辑器。使用这个编辑器，您可以任意编辑一段 HTML 源码，然后单击 TIY 按钮来查看结果。

### HTML 标题

HTML 标题（Heading）是通过 <h1> - <h6> 等标签进行定义的。

**实例**

```
<h1>This is a heading</h1>
<h2>This is a heading</h2>
<h3>This is a heading</h3>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_headers)

### HTML 段落

HTML 段落是通过 <p> 标签进行定义的。

**实例**

```
<p>This is a paragraph.</p>
<p>This is another paragraph.</p>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_paragraphs1)

### HTML 链接

HTML 链接是通过 <a> 标签进行定义的。

**实例**

```
<a href="http://www.w3school.com.cn">This is a link</a>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_basic_link)

注释：在 href 属性中指定链接的地址。

（您将在本教程稍后的章节中学习更多有关属性的知识）。

### HTML 图像

HTML 图像是通过 <img> 标签进行定义的。

**实例**

```
<img src="w3school.jpg" width="104" height="142" />
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_basic_img)

注释：图像的名称和尺寸是以属性的形式提供的。



## HTML 元素



**HTML 文档是由 HTML 元素定义的。**

### HTML 元素

HTML 元素指的是从开始标签（start tag）到结束标签（end tag）的所有代码。

| 开始标签                | 元素内容            | 结束标签 |
| ----------------------- | ------------------- | -------- |
| <p>                     | This is a paragraph | </p>     |
| <a href="default.htm" > | This is a link      | </a>     |
| <br />                  |                     |          |

注释：开始标签常被称为开放标签（opening tag），结束标签常称为闭合标签（closing tag）。

### HTML 元素语法

- HTML 元素以*开始标签*起始
- HTML 元素以*结束标签*终止
- *元素的内容*是开始标签与结束标签之间的内容
- 某些 HTML 元素具有*空内容（empty content）*
- 空元素*在开始标签中进行关闭*（以开始标签的结束而结束）
- 大多数 HTML 元素可拥有*属性*

提示：您将在本教程的下一章中学习更多有关属性的内容。

### 嵌套的 HTML 元素

大多数 HTML 元素可以嵌套（可以包含其他 HTML 元素）。

HTML 文档由嵌套的 HTML 元素构成。

### HTML 文档实例

```
<html>

<body>
<p>This is my first paragraph.</p>
</body>

</html>
```

上面的例子包含三个 HTML 元素。

### HTML 实例解释

**p 元素：**

```
<p>This is my first paragraph.</p>
```

这个 <p> 元素定义了 HTML 文档中的一个段落。

这个元素拥有一个开始标签 <p>，以及一个结束标签 </p>。

元素内容是：This is my first paragraph。

**body 元素：**

```
<body>
<p>This is my first paragraph.</p>
</body>
```

<body> 元素定义了 HTML 文档的主体。

这个元素拥有一个开始标签 <body>，以及一个结束标签 </body>。

元素内容是另一个 HTML 元素（p 元素）。

**html 元素：**

```
<html>

<body>
<p>This is my first paragraph.</p>
</body>

</html>
```

<html> 元素定义了整个 HTML 文档。

这个元素拥有一个开始标签 <html>，以及一个结束标签 </html>。

元素内容是另一个 HTML 元素（body 元素）。

### 不要忘记结束标签

即使您忘记了使用结束标签，大多数浏览器也会正确地显示 HTML：

```
<p>This is a paragraph
<p>This is a paragraph
```

上面的例子在大多数浏览器中都没问题，但不要依赖这种做法。忘记使用结束标签会产生不可预料的结果或错误。

注释：未来的 HTML 版本不允许省略结束标签。

### 空的 HTML 元素

没有内容的 HTML 元素被称为空元素。空元素是在开始标签中关闭的。

**br** 就是没有关闭标签的空元素（**br** 标签定义换行）。

在 XHTML、XML 以及未来版本的 HTML 中，所有元素都必须被关闭。

在开始标签中添加斜杠，比如 **br**，是关闭空元素的正确方法，HTML、XHTML 和 XML 都接受这种方式。

即使 **br** 在所有浏览器中都是有效的，但使用 **br** 其实是更长远的保障。

### HTML 提示：使用小写标签

HTML 标签对大小写不敏感：<P> 等同于 <p>。许多网站都使用大写的 HTML 标签。

W3School 使用的是小写标签，因为万维网联盟（W3C）在 HTML 4 中*推荐*使用小写，而在未来 (X)HTML 版本中*强制*使用小写。

## HTML 属性

**属性为 HTML 元素提供附加信息。**

### HTML 属性

HTML 标签可以拥有*属性*。属性提供了有关 HTML 元素的*更多的信息*。

属性总是以名称/值对的形式出现，比如：*name="value"*。

属性总是在 HTML 元素的*开始标签*中规定。

### 属性实例

HTML 链接由 <a> 标签定义。链接的地址在 href 属性中指定：

```
<a href="http://www.w3school.com.cn">This is a link</a>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_basic_link)

### 更多 HTML 属性实例

**属性例子 1:**

<h1> 定义标题的开始。

<h1 align="center"> 拥有关于对齐方式的附加信息。

[TIY : 居中排列标题](http://www.w3school.com.cn/tiy/t.asp?f=html_header)

**属性例子 2:**

<body> 定义 HTML 文档的主体。

<body bgcolor="yellow"> 拥有关于背景颜色的附加信息。

[TIY : 背景颜色](http://www.w3school.com.cn/tiy/t.asp?f=html_bgcolor)

**属性例子 3:**

<table> 定义 HTML 表格。（您将在稍后的章节学习到更多有关 HTML 表格的内容）

<table border="1"> 拥有关于表格边框的附加信息。

### HTML 提示：使用小写属性

属性和属性值对大小写*不敏感*。

不过，万维网联盟在其 HTML 4 推荐标准中推荐小写的属性/属性值。

而新版本的 (X)HTML 要求使用小写属性。

### 始终为属性值加引号

属性值应该始终被包括在引号内。双引号是最常用的，不过使用单引号也没有问题。

在某些个别的情况下，比如属性值本身就含有双引号，那么您必须使用单引号，例如：

```
name='Bill "HelloWorld" Gates'
```

### HTML 属性参考手册

我们的完整的 HTML 参考手册提供了每个 HTML 元素可使用的合法属性的完整列表：

[完整的 HTML 参考手册](http://www.w3school.com.cn/tags/index.asp)

下面列出了适用于大多数 HTML 元素的属性：

| 属性  | 值                 | 描述                                     |
| ----- | ------------------ | ---------------------------------------- |
| class | *classname*        | 规定元素的类名（classname）              |
| id    | *id*               | 规定元素的唯一 id                        |
| style | *style_definition* | 规定元素的行内样式（inline style）       |
| title | *text*             | 规定元素的额外信息（可在工具提示中显示） |

如需更多关于标准属性的信息，请访问：

[HTML 标准属性参考手册](http://www.w3school.com.cn/tags/html_ref_standardattributes.asp)  

##   HTML 标题

**在 HTML 文档中，标题很重要。**

标题（Heading）是通过 <h1> - <h6> 等标签进行定义的。

<h1> 定义最大的标题。<h6> 定义最小的标题。

**实例**

```
<h1>This is a heading</h1>
<h2>This is a heading</h2>
<h3>This is a heading</h3>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_headers)

注释：浏览器会自动地在标题的前后添加空行。

注释：默认情况下，HTML 会自动地在块级元素前后添加一个额外的空行，比如段落、标题元素前后。

### 标题很重要

请确保将 HTML heading 标签只用于标题。不要仅仅是为了产生粗体或大号的文本而使用标题。

搜索引擎使用标题为您的网页的结构和内容编制索引。

因为用户可以通过标题来快速浏览您的网页，所以用标题来呈现文档结构是很重要的。

应该将 h1 用作主标题（最重要的），其后是 h2（次重要的），再其次是 h3，以此类推。

### HTML 水平线

<hr /> 标签在 HTML 页面中创建水平线。

hr 元素可用于分隔内容。

**实例**

```
<p>This is a paragraph</p>
<hr />
<p>This is a paragraph</p>
<hr />
<p>This is a paragraph</p>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_hr)

提示：使用水平线 (<hr> 标签) 来分隔文章中的小节是一个办法（但并不是唯一的办法）。

### HTML 注释

可以将注释插入 HTML 代码中，这样可以提高其可读性，使代码更易被人理解。浏览器会忽略注释，也不会显示它们。

注释是这样写的：

**实例**

```
<!-- This is a comment -->
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_comment)

注释：开始括号之后（左边的括号）需要紧跟一个叹号，结束括号之前（右边的括号）不需要。

提示：合理地使用注释可以对未来的代码编辑工作产生帮助。

### HTML 提示 - 如何查看源代码

您一定曾经在看到某个网页时惊叹道 “WOW! 这是如何实现的？”

如果您想找到其中的奥秘，只需要单击右键，然后选择“查看源文件”（IE）或“查看页面源代码”（Firefox），其他浏览器的做法也是类似的。这么做会打开一个包含页面 HTML 代码的窗口。

### 来自本页的实例

- [标题](http://www.w3school.com.cn/tiy/t.asp?f=html_headers)

  如何在 HTML 文档中显示标题。

- [隐藏的注释](http://www.w3school.com.cn/tiy/t.asp?f=html_comment)

  如何在 HTML 源代码中插入注释。

- [水平线](http://www.w3school.com.cn/tiy/t.asp?f=html_hr)

  如何插入水平线。

### HTML 标签参考手册

W3School 的标签参考手册提供了有关这些标题及其属性的更多信息。

您将在本教程下面的章节中学到更多有关 HTML 标签和属性的知识。

| 标签                                                   | 描述             |
| ------------------------------------------------------ | ---------------- |
| [html](http://www.w3school.com.cn/tags/tag_html.asp)   | 定义 HTML 文档。 |
| [body](http://www.w3school.com.cn/tags/tag_body.asp)   | 定义文档的主体。 |
| [h1~ h6 ](http://www.w3school.com.cn/tags/tag_hn.asp)  | 定义 HTML 标题   |
| [hr](http://www.w3school.com.cn/tags/tag_hr.asp)       | 定义水平线。     |
| [!--](http://www.w3school.com.cn/tags/tag_comment.asp) | 定义注释。       |

## HTML 段落

**可以把 HTML 文档分割为若干段落。**

段落是通过 <p> 标签定义的。

**实例**

```
<p>This is a paragraph</p>
<p>This is another paragraph</p>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_paragraphs1)

注释：浏览器会自动地在段落的前后添加空行。（<p> 是块级元素）

提示：使用空的段落标记 <p></p> 去插入一个空行是个坏习惯。用 <br /> 标签代替它！（但是不要用 <br /> 标签去创建列表。不要着急，您将在稍后的篇幅学习到 HTML 列表。）

### 不要忘记结束标签

即使忘了使用结束标签，大多数浏览器也会正确地将 HTML 显示出来：

**实例**

```
<p>This is a paragraph
<p>This is another paragraph
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_paragraphs0)

上面的例子在大多数浏览器中都没问题，但不要依赖这种做法。忘记使用结束标签会产生意想不到的结果和错误。

注释：在未来的 HTML 版本中，不允许省略结束标签。

提示：通过结束标签来关闭 HTML 是一种经得起未来考验的 HTML 编写方法。清楚地标记某个元素在何处开始，并在何处结束，不论对您还是对浏览器来说，都会使代码更容易理解。

### HTML 折行

如果您希望在不产生一个新段落的情况下进行换行（新行），请使用 <br /> 标签：

```
<p>This is<br />a para<br />graph with line breaks</p>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_paragraphs)

<br /> 元素是一个空的 HTML 元素。由于关闭标签没有任何意义，因此它没有结束标签。

### &lt;br&gt;还是&lt; br /&gt;

您也许发现 &lt;br> 与 &lt;br /> 很相似。

在 XHTML、XML 以及未来的 HTML 版本中，不允许使用没有结束标签（闭合标签）的 HTML 元素。

即使 &lt;br> 在所有浏览器中的显示都没有问题，使用 &lt;br /> 也是*更长远的保障*。

### HTML 输出 - 有用的提示

我们无法确定 HTML 被显示的确切效果。屏幕的大小，以及对窗口的调整都可能导致不同的结果。

对于 HTML，您无法通过在 HTML 代码中添加额外的空格或换行来改变输出的效果。

当显示页面时，浏览器会移除*源代码中*多余的空格和空行。所有连续的空格或空行都会被算作一个空格。需要注意的是，HTML 代码中的所有连续的空行（换行）也被显示为一个空格。

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_poem)

（这个例子演示了一些 HTML 格式化方面的问题）

### 来自本页的实例

- [HTML 段落](http://www.w3school.com.cn/tiy/t.asp?f=html_paragraphs1)

  如何在浏览器中显示 HTML 段落。

- [换行](http://www.w3school.com.cn/tiy/t.asp?f=html_paragraphs)

  在 HTML 文档中使用换行。

- [在 HTML 代码中的排版一首唐诗](http://www.w3school.com.cn/tiy/t.asp?f=html_poem)

  浏览器在显示 HTML 时，会省略源代码中多余的空白字符（空格或回车等）。

### 更多实例

- [更多段落](http://www.w3school.com.cn/tiy/t.asp?f=html_paragraphs2)

  段落的默认行为。

### HTML 标签参考手册

W3School 的标签参考手册提供了有关 HTML 元素及其属性的更多信息。

| 标签                                              | 描述                   |
| ------------------------------------------------- | ---------------------- |
| [p](http://www.w3school.com.cn/tags/tag_p.asp)    | 定义段落。             |
| [br ](http://www.w3school.com.cn/tags/tag_br.asp) | 插入单个折行（换行）。 |

##   HTML 样式

style 属性用于改变 HTML 元素的样式。

```
This text is in Verdana and red

This text is in Times and blue

This text is 30 pixels high
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_styles)

### HTML 的 style 属性

style 属性的作用：

**提供了一种改变所有 HTML 元素的样式的通用方法。**

样式是 HTML 4 引入的，它是一种新的首选的改变 HTML 元素样式的方式。通过 HTML 样式，能够通过使用 style 属性直接将样式添加到 HTML 元素，或者间接地在独立的样式表中（CSS 文件）进行定义。

您可以在我们的 [CSS 教程](http://www.w3school.com.cn/css/index.asp)中学习关于样式和 CSS 的所有知识。

在我们的 HTML 教程中，我们将使用 style 属性向您讲解 HTML 样式。

### 不赞成使用的标签和属性

在 HTML 4 中，有若干的标签和属性是被废弃的。被废弃（Deprecated）的意思是在未来版本的 HTML 和 XHTML 中将不支持这些标签和属性。

这里传达的信息很明确：请避免使用这些被废弃的标签和属性！

### 应该避免使用下面这些标签和属性：

| 标签                 | 描述               |
| -------------------- | ------------------ |
| <center>             | 定义居中的内容。   |
| <font> 和 <basefont> | 定义 HTML 字体。   |
| <s> 和 <strike>      | 定义删除线文本     |
| <u>                  | 定义下划线文本     |
| 属性                 | 描述               |
| align                | 定义文本的对齐方式 |
| bgcolor              | 定义背景颜色       |
| color                | 定义文本颜色       |

对于以上这些标签和属性：请使用样式代替！

### HTML 样式实例 - 背景颜色

background-color 属性为元素定义了背景颜色：

```
<html>

<body style="background-color:yellow">
<h2 style="background-color:red">This is a heading</h2>
<p style="background-color:green">This is a paragraph.</p>
</body>

</html>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_bodybgstyle)

style 属性淘汰了“旧的” bgcolor 属性。

[亲自试一试：设置背景颜色的旧方法](http://www.w3school.com.cn/tiy/t.asp?f=html_bodybgcol)

### HTML 样式实例 - 字体、颜色和尺寸

font-family、color 以及 font-size 属性分别定义元素中文本的字体系列、颜色和字体尺寸：

```
<html>

<body>
<h1 style="font-family:verdana">A heading</h1>
<p style="font-family:arial;color:red;font-size:20px;">A paragraph.</p>
</body>

</html>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_newfont)

style 属性淘汰了旧的 <font> 标签。

[亲自试一试：设置字体的旧方法](http://www.w3school.com.cn/tiy/t.asp?f=html_font)

### HTML 样式实例 - 文本对齐

text-align 属性规定了元素中文本的水平对齐方式：

```
<html>

<body>
<h1 style="text-align:center">This is a heading</h1>
<p>The heading above is aligned to the center of this page.</p>
</body>

</html>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_headeralign)

style 属性淘汰了旧的 "align" 属性。

[亲自试一试：设置居中对齐的旧方法](http://www.w3school.com.cn/tiy/t.asp?f=html_header)

## HTML 文本格式化



**HTML 可定义很多供格式化输出的元素，比如粗体和斜体字。**

**下面有很多例子，您可以亲自试试：**

### HTML 文本格式化实例

- [文本格式化](http://www.w3school.com.cn/tiy/t.asp?f=html_textformatting)

  此例演示如何在一个 HTML 文件中对文本进行格式化

- [预格式文本](http://www.w3school.com.cn/tiy/t.asp?f=html_preformattedtext)

  此例演示如何使用 pre 标签对空行和空格进行控制。

- [“计算机输出”标签](http://www.w3school.com.cn/tiy/t.asp?f=html_computeroutput)

  此例演示不同的“计算机输出”标签的显示效果。

- [地址](http://www.w3school.com.cn/tiy/t.asp?f=html_address)

  此例演示如何在 HTML 文件中写地址。

- [缩写和首字母缩写](http://www.w3school.com.cn/tiy/t.asp?f=html_abbracronym)

  此例演示如何实现缩写或首字母缩写。

- [文字方向](http://www.w3school.com.cn/tiy/t.asp?f=html_bdo)

  此例演示如何改变文字的方向。

- [块引用](http://www.w3school.com.cn/tiy/t.asp?f=html_quotations)

  此例演示如何实现长短不一的引用语。

- [删除字效果和插入字效果](http://www.w3school.com.cn/tiy/t.asp?f=html_delins)

  此例演示如何标记删除文本和插入文本。

### 如何查看 HTML 源码

您是否有过这样的经历，当你看到一个很棒的站点，你会很想知道开发人员是如何将它实现的？

你有没有看过一些网页，并且想知道它是如何做出来的呢？

要揭示一个网站的技术秘密，其实很简单。单击浏览器的“查看”菜单，选择“查看源文件”即可。随后你会看到一个弹出的窗口，窗口内就是实际的 HTML 代码。

### 文本格式化标签

| 标签                                                         | 描述                                  |
| ------------------------------------------------------------ | ------------------------------------- |
| [b](http://www.w3school.com.cn/tags/tag_font_style.asp)      | 定义粗体文本。                        |
| [big](http://www.w3school.com.cn/tags/tag_font_style.asp)    | 定义大号字。                          |
| [em](http://www.w3school.com.cn/tags/tag_phrase_elements.asp) | 定义着重文字。                        |
| [i](http://www.w3school.com.cn/tags/tag_font_style.asp)      | 定义斜体字。                          |
| [small](http://www.w3school.com.cn/tags/tag_font_style.asp)  | 定义小号字。                          |
| [strong](http://www.w3school.com.cn/tags/tag_phrase_elements.asp) | 定义加重语气。                        |
| [sub](http://www.w3school.com.cn/tags/tag_sup.asp)           | 定义下标字。                          |
| [sup](http://www.w3school.com.cn/tags/tag_sup.asp)           | 定义上标字。                          |
| [ins](http://www.w3school.com.cn/tags/tag_ins.asp)           | 定义插入字。                          |
| [del](http://www.w3school.com.cn/tags/tag_del.asp)           | 定义删除字。                          |
| [s](http://www.w3school.com.cn/tags/tag_strike.asp)          | *不赞成使用。*使用 <del> 代替。       |
| [strike](http://www.w3school.com.cn/tags/tag_strike.asp)     | *不赞成使用。*使用 <del> 代替。       |
| [u](http://www.w3school.com.cn/tags/tag_u.asp)               | *不赞成使用。*使用样式（style）代替。 |

### “计算机输出”标签

| 标签                                                         | 描述                            |
| ------------------------------------------------------------ | ------------------------------- |
| [code](http://www.w3school.com.cn/tags/tag_phrase_elements.asp) | 定义计算机代码。                |
| [kbd](http://www.w3school.com.cn/tags/tag_phrase_elements.asp) | 定义键盘码。                    |
| [samp](http://www.w3school.com.cn/tags/tag_phrase_elements.asp) | 定义计算机代码样本。            |
| [tt](http://www.w3school.com.cn/tags/tag_font_style.asp)     | 定义打字机代码。                |
| [var](http://www.w3school.com.cn/tags/tag_phrase_elements.asp) | 定义变量。                      |
| [pre](http://www.w3school.com.cn/tags/tag_pre.asp)           | 定义预格式文本。                |
| listing                                                      | *不赞成使用。*使用 <pre> 代替。 |
| plaintext                                                    | *不赞成使用。*使用 <pre> 代替。 |
| xmp                                                          | *不赞成使用。*使用 <pre> 代替。 |

### 引用、引用和术语定义

| 标签                                                         | 描述               |
| ------------------------------------------------------------ | ------------------ |
| [abbr](http://www.w3school.com.cn/tags/tag_abbr.asp)         | 定义缩写。         |
| [acronym](http://www.w3school.com.cn/tags/tag_acronym.asp)   | 定义首字母缩写。   |
| [address](http://www.w3school.com.cn/tags/tag_address.asp)   | 定义地址。         |
| [bdo](http://www.w3school.com.cn/tags/tag_bdo.asp)           | 定义文字方向。     |
| [blockquote](http://www.w3school.com.cn/tags/tag_blockquote.asp) | 定义长的引用。     |
| [q](http://www.w3school.com.cn/tags/tag_q.asp)               | 定义短的引用语。   |
| [cit](http://www.w3school.com.cn/tags/tag_phrase_elements.asp) | 定义引用、引证。   |
| [dfn](http://www.w3school.com.cn/tags/tag_phrase_elements.asp) | 定义一个定义项目。 |

### 延伸阅读：

[改变文本的外观和含义](http://www.w3school.com.cn/html/html_style.asp)

## HTML 引用

### 引用（Quotation）

这是摘自 WWF 网站的引文：

> 五十年来，WWF 一直致力于保护自然界的未来。 世界领先的环保组织，WWF 工作于 100 个国家，并得到美国一百二十万会员及全球近五百万会员的支持。

### HTML &lt;q> 用于短的引用

HTML *<q>* 元素定义*短的引用*。

浏览器通常会为 <q> 元素包围*引号*。

**实例**

```
<p>WWF 的目标是：<q>构建人与自然和谐共存的世界。</q></p>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_quotation_q)

### 用于长引用的 HTML &lt;blockquote>

HTML *<blockquote>* 元素定义被引用的节。

浏览器通常会对 <blockquote> 元素进行*缩进*处理。

**实例**

```
<p>以下内容引用自 WWF 的网站：</p>
<blockquote cite="http://www.worldwildlife.org/who/index.html">
五十年来，WWF 一直致力于保护自然界的未来。
世界领先的环保组织，WWF 工作于 100 个国家，
并得到美国一百二十万会员及全球近五百万会员的支持。
</blockquote>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_quotation_blockquote)

### 用于缩略词的 HTML &lt;abbr>

HTML *<abbr>* 元素定义*缩写*或首字母缩略语。

对缩写进行标记能够为浏览器、翻译系统以及搜索引擎提供有用的信息。

**实例**

```
<p><abbr title="World Health Organization">WHO</abbr> 成立于 1948 年。</p>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_formatting_abbr)

### 用于定义的 HTML &lt;dfn>

HTML *<dfn>* 元素定义项目或缩写的*定义*。

<dfn> 的用法，按照 HTML5 标准中的描述，有点复杂：

\1. 如果设置了 <dfn> 元素的 title 属性，则定义项目：

**实例**

```
<p><dfn title="World Health Organization">WHO</dfn> 成立于 1948 年。</p>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_formatting_dfn)

\2. 如果 <dfn> 元素包含具有标题的 <abbr> 元素，则 title 定义项目：

**实例**

```
<p><dfn><abbr title="World Health Organization">WHO</abbr></dfn> 成立于 1948 年。</p>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_formatting_dfn_2)

\3. 否则，<dfn> 文本内容即是项目，并且父元素包含定义。

**实例**

```
<p><dfn>WHO</dfn> World Health Organization 成立于 1948 年。</p>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_formatting_dfn_3)

注释：如果您希望简而化之，请使用第一条，或使用 <abbr> 代替。

### 用于联系信息的 HTML &lt;address>

HTML *<address>* 元素定义文档或文章的联系信息（作者/拥有者）。

此元素通常以*斜体*显示。大多数浏览器会在此元素前后添加折行。

**实例**

```
<address>
Written by Donald Duck.<br> 
Visit us at:<br>
Example.com<br>
Box 564, Disneyland<br>
USA
</address>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_formatting_address)

### 用于著作标题的 HTML &lt;cite>

HTML *<cite>* 元素定义*著作的标题*。

浏览器通常会以斜体显示 <cite> 元素。

**实例**

```
<p><cite>The Scream</cite> by Edward Munch. Painted in 1893.</p>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_formatting_cite)

### 用于双向重写的 HTML &lt;bdo>

HTML *<bdo>* 元素定义双流向覆盖（bi-directional override）。

<bdo> 元素用于覆盖当前文本方向：

**实例**

```
<bdo dir="rtl">This text will be written from right to left</bdo>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_formatting_bdo)

### HTML 引文、引用和定义元素

| 标签         | 描述                             |
| ------------ | -------------------------------- |
| <abbr>       | 定义缩写或首字母缩略语。         |
| <address>    | 定义文档作者或拥有者的联系信息。 |
| <bdo>        | 定义文本方向。                   |
| <blockquote> | 定义从其他来源引用的节。         |
| <dfn>        | 定义项目或缩略词的定义。         |
| <q>          | 定义短的行内引用。               |
| <cite>       | 定义著作的标题。                 |

## HTML 计算机代码元素

**计算机代码**

```
var person = {
    firstName:"Bill",
    lastName:"Gates",
    age:50,
    eyeColor:"blue"
}
```

### HTML 计算机代码格式

通常，HTML 使用*可变*的字母尺寸，以及可变的字母间距。

在显示*计算机代码*示例时，并不需要如此。

*<kbd>*, *<samp>*, 以及 *<code>* 元素全都支持固定的字母尺寸和间距。

### HTML 键盘格式

HTML *<kbd>* 元素定义*键盘输入*：

**实例**

```
<p>To open a file, select:</p>

<p><kbd>File | Open...</kbd></p>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_formatting_kbd)

### HTML 样本格式

HTML *<samp>* 元素定义*计算机输出示例*：

**实例**

```
<samp>
demo.example.com login: Apr 12 09:10:17
Linux 2.6.10-grsec+gg3+e+fhs6b+nfs+gr0501+++p3+c4a+gr2b-reslog-v6.189
</samp>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_formatting_samp)

### HTML 代码格式

HTML *<code>* 元素定义*编程代码示例*：

**实例**

```
<code>
var person = { firstName:"Bill", lastName:"Gates", age:50, eyeColor:"blue" }
</code>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_formatting_code)

<code> 元素不保留多余的空格和折行：

**实例**

```
<p>Coding Example:</p>

<code>
var person = {
    firstName:"Bill",
    lastName:"Gates",
    age:50,
    eyeColor:"blue"
}
</code>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_formatting_codelines)

如需解决该问题，您必须在 <pre> 元素中包围代码：

**实例**

```
<p>Coding Example:</p>

<code>
<pre>
var person = {
    firstName:"Bill",
    lastName:"Gates",
    age:50,
    eyeColor:"blue"
}
</pre>
</code>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_formatting_codepre)

### HTML 变量格式化

HTML *<var>* 元素定义*数学变量*：

**实例**

```
<p>Einstein wrote:</p>

<p><var>E = m c<sup>2</sup></var></p>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_formatting_var)

### HTML 计算机代码元素

| 标签   | 描述               |
| ------ | ------------------ |
| <code> | 定义计算机代码文本 |
| <kbd>  | 定义键盘文本       |
| <samp> | 定义计算机代码示例 |
| <var>  | 定义变量           |
| <pre>  | 定义预格式化文本   |

## HTML 注释

**注释标签 <!-- 与 --> 用于在 HTML 插入注释。**

### HTML 注释标签

您能够通过如下语法向 HTML 源代码添加注释：

**实例**

```
<!-- 在此处写注释 -->
```

注释：在开始标签中有一个惊叹号，但是结束标签中没有。

浏览器不会显示注释，但是能够帮助记录您的 HTML 文档。

您可以利用注释在 HTML 中放置通知和提醒信息：

**实例**

```
<!-- 这是一段注释 -->

<p>这是一个段落。</p>

<!-- 记得在此处添加信息 -->
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_comment)

注释对于 HTML 纠错也大有帮助，因为您可以一次注释一行 HTML 代码，以搜索错误：

**实例**

```
<!-- 此刻不显示图片：
<img border="0" src="/i/tulip_ballade.jpg" alt="Tulip">
-->
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_comment2)

### 条件注释

您也许会在 HTML 中偶尔发现条件注释：

```
<!--[if IE 8]>
    .... some HTML here ....
<![endif]-->
```

条件注释定义只有 Internet Explorer 执行的 HTML 标签。

### 软件程序标签

各种 HTML 软件程序也能够生成 HTML 注释。

例如 <!--webbot bot--> 标签会被包围在由 FrontPage 和 Expression Web 创建的 HTML 注释中。

作为一项规则，这些标签的存在，有助于对创建这些标签的软件的支持。

##   HTML CSS

**通过使用 HTML4.0，所有的格式化代码均可移出 HTML 文档，然后移入一个独立的样式表。**

**实例**

- [HTML中的样式](http://www.w3school.com.cn/tiy/t.asp?f=html_style)

  本例演示如何使用添加到 <head> 部分的样式信息对 HTML 进行格式化。

- [没有下划线的链接](http://www.w3school.com.cn/tiy/t.asp?f=html_linknoline)

  本例演示如何使用样式属性做一个没有下划线的链接。

- [链接到一个外部样式表](http://www.w3school.com.cn/tiy/t.asp?f=html_link)

  本例演示如何 <link> 标签链接到一个外部样式表。

### 如何使用样式

当浏览器读到一个样式表，它就会按照这个样式表来对文档进行格式化。有以下三种方式来插入样式表：

**外部样式表**

当样式需要被应用到很多页面的时候，外部样式表将是理想的选择。使用外部样式表，你就可以通过更改一个文件来改变整个站点的外观。

```
<head>
<link rel="stylesheet" type="text/css" href="mystyle.css">
</head>
```

**内部样式表**

当单个文件需要特别样式时，就可以使用内部样式表。你可以在 head 部分通过 <style> 标签定义内部样式表。

```
<head>

<style type="text/css">
body {background-color: red}
p {margin-left: 20px}
</style>
</head>
```

**内联样式**

当特殊的样式需要应用到个别元素时，就可以使用内联样式。 使用内联样式的方法是在相关的标签中使用样式属性。样式属性可以包含任何 CSS 属性。以下实例显示出如何改变段落的颜色和左外边距。

```
<p style="color: red; margin-left: 20px">
This is a paragraph
</p>
```

访问我们的 [CSS 教程](http://www.w3school.com.cn/css/index.asp)，学习更多有关样式的知识。

| 标签                                                         | 描述                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| [style](http://www.w3school.com.cn/tags/tag_style.asp)       | 定义样式定义。                                               |
| [link](http://www.w3school.com.cn/tags/tag_link.asp)         | 定义资源引用。                                               |
| [div](http://www.w3school.com.cn/tags/tag_div.asp)           | 定义文档中的节或区域（块级）。                               |
| [span](http://www.w3school.com.cn/tags/tag_span.asp)         | 定义文档中的行内的小块或区域。                               |
| [font](http://www.w3school.com.cn/tags/tag_font.asp)         | 规定文本的字体、字体尺寸、字体颜色。不赞成使用。请使用样式。 |
| [basefont](http://www.w3school.com.cn/tags/tag_basefont.asp) | 定义基准字体。不赞成使用。请使用样式。                       |
| [center](http://www.w3school.com.cn/tags/tag_center.asp)     | 对文本进行水平居中。不赞成使用。请使用样式。                 |

## HTML 链接

**HTML 使用超级链接与网络上的另一个文档相连。**

**几乎可以在所有的网页中找到链接。点击链接可以从一张页面跳转到另一张页面。**

**实例**

- [创建超级链接](http://www.w3school.com.cn/tiy/t.asp?f=html_links)

  本例演示如何在 HTML 文档中创建链接。

- [将图像作为链接](http://www.w3school.com.cn/tiy/t.asp?f=html_imglink)

  本例演示如何使用图像作为链接。

（[可以在本页底端找到更多实例](http://www.w3school.com.cn/html/html_links.asp#more_examples)）

### HTML 超链接（链接）

超链接可以是一个字，一个词，或者一组词，也可以是一幅图像，您可以点击这些内容来跳转到新的文档或者当前文档中的某个部分。

当您把鼠标指针移动到网页中的某个链接上时，箭头会变为一只小手。

我们通过使用 <a> 标签在 HTML 中创建链接。

有两种使用 <a> 标签的方式：

1. 通过使用 href 属性 - 创建指向另一个文档的链接
2. 通过使用 name 属性 - 创建文档内的书签

延伸阅读：[什么是超文本？](http://www.w3school.com.cn/tags/tag_term_hypertext.asp)

### HTML 链接语法

链接的 HTML 代码很简单。它类似这样：

```
<a href="url">Link text</a>
```

href 属性规定链接的目标。

开始标签和结束标签之间的文字被作为超级链接来显示。

**实例**

```
<a href="http://www.w3school.com.cn/">Visit W3School</a>
```

上面这行代码显示为：[Visit W3School](http://www.w3school.com.cn/)

点击这个超链接会把用户带到 W3School 的首页。

提示："链接文本" 不必一定是文本。图片或其他 HTML 元素都可以成为链接。

### HTML 链接 - target 属性

使用 Target 属性，你可以定义被链接的文档在何处显示。

下面的这行会在新窗口打开文档：

```
<a href="http://www.w3school.com.cn/" target="_blank">Visit W3School!</a>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_link_target)

### HTML 链接 - name 属性

name 属性规定锚（anchor）的名称。

您可以使用 name 属性创建 HTML 页面中的书签。

书签不会以任何特殊方式显示，它对读者是不可见的。

当使用命名锚（named anchors）时，我们可以创建直接跳至该命名锚（比如页面中某个小节）的链接，这样使用者就无需不停地滚动页面来寻找他们需要的信息了。

### 命名锚的语法：

```
<a name="label">锚（显示在页面上的文本）</a>
```

提示：锚的名称可以是任何你喜欢的名字。

提示：您可以使用 id 属性来替代 name 属性，命名锚同样有效。

**实例**

首先，我们在 HTML 文档中对锚进行命名（创建一个书签）：

```
<a name="tips">基本的注意事项 - 有用的提示</a>
```

然后，我们在同一个文档中创建指向该锚的链接：

```
<a href="#tips">有用的提示</a>
```

您也可以在其他页面中创建指向该锚的链接：

```
<a href="http://www.w3school.com.cn/html/html_links.asp#tips">有用的提示</a>
```

在上面的代码中，我们将 # 符号和锚名称添加到 URL 的末端，就可以直接链接到 tips 这个命名锚了。

具体效果：[有用的提示](http://www.w3school.com.cn/html/html_links.asp#tips)

### 基本的注意事项 - 有用的提示：

注释：请始终将正斜杠添加到子文件夹。假如这样书写链接：href="http://www.w3school.com.cn/html"，就会向服务器产生两次 HTTP 请求。这是因为服务器会添加正斜杠到这个地址，然后创建一个新的请求，就像这样：href="http://www.w3school.com.cn/html/"。

提示：命名锚经常用于在大型文档开始位置上创建目录。可以为每个章节赋予一个命名锚，然后把链接到这些锚的链接放到文档的上部。如果您经常访问百度百科，您会发现其中几乎每个词条都采用这样的导航方式。

提示：假如浏览器找不到已定义的命名锚，那么就会定位到文档的顶端。不会有错误发生。

### 更多实例

- [在新的浏览器窗口打开链接](http://www.w3school.com.cn/tiy/t.asp?f=html_link_target)

  本例演示如何在新窗口打开一个页面，这样的话访问者就无需离开你的站点了。

- [链接到同一个页面的不同位置](http://www.w3school.com.cn/tiy/t.asp?f=html_link_locations)

  本例演示如何使用链接跳转至文档的另一个部分

- [跳出框架](http://www.w3school.com.cn/tiy/t.asp?f=html_frame_getfree)

  本例演示如何跳出框架，假如你的页面被固定在框架之内。

- [创建电子邮件链接](http://www.w3school.com.cn/tiy/t.asp?f=html_mailto)

  本例演示如何链接到一个邮件。（本例在安装邮件客户端程序后才能工作。）

- [创建电子邮件链接 2](http://www.w3school.com.cn/tiy/t.asp?f=html_mailto2)

  本例演示更加复杂的邮件链接。

### HTML 链接标签

| 标签                                           | 描述     |
| ---------------------------------------------- | -------- |
| [a](http://www.w3school.com.cn/tags/tag_a.asp) | 定义锚。 |

##   HTML 图像

**通过使用 HTML，可以在文档中显示图像。**

**实例**

- [插入图像](http://www.w3school.com.cn/tiy/t.asp?f=html_image)

  本例演示如何在网页中显示图像。

- [从不同的位置插入图片](http://www.w3school.com.cn/tiy/t.asp?f=html_image2)

  本例演示如何将其他文件夹或服务器的图片显示到网页中。

（[可以在本页底端找到更多实例](http://www.w3school.com.cn/html/html_images.asp#more_examples)。）

### 图像标签（&lt;img>）和源属性（Src）

在 HTML 中，图像由 <img> 标签定义。

<img> 是空标签，意思是说，它只包含属性，并且没有闭合标签。

要在页面上显示图像，你需要使用源属性（src）。src 指 "source"。源属性的值是图像的 URL 地址。

定义图像的语法是：

```
<img src="url" />
```

URL 指存储图像的位置。如果名为 "boat.gif" 的图像位于 www.w3school.com.cn 的 images 目录中，那么其 URL 为 http://www.w3school.com.cn/images/boat.gif。

浏览器将图像显示在文档中图像标签出现的地方。如果你将图像标签置于两个段落之间，那么浏览器会首先显示第一个段落，然后显示图片，最后显示第二段。

### 替换文本属性（Alt）

alt 属性用来为图像定义一串预备的可替换的文本。替换文本属性的值是用户定义的。

```
<img src="boat.gif" alt="Big Boat">
```

在浏览器无法载入图像时，替换文本属性告诉读者她们失去的信息。此时，浏览器将显示这个替代性的文本而不是图像。为页面上的图像都加上替换文本属性是个好习惯，这样有助于更好的显示信息，并且对于那些使用纯文本浏览器的人来说是非常有用的。

### 基本的注意事项 - 有用的提示：

假如某个 HTML 文件包含十个图像，那么为了正确显示这个页面，需要加载 11 个文件。加载图片是需要时间的，所以我们的建议是：慎用图片。

### 更多实例

- [背景图片](http://www.w3school.com.cn/tiy/t.asp?f=html_backgroundimage)

  本例演示如何向 HTML 页面添加背景图片。

- [排列图片](http://www.w3school.com.cn/tiy/t.asp?f=html_image_align)

  本例演示如何在文字中排列图像。

- [浮动图像](http://www.w3school.com.cn/tiy/t.asp?f=html_image_float)

  本例演示如何使图片浮动至段落的左边或右边。

- [调整图像尺寸](http://www.w3school.com.cn/tiy/t.asp?f=html_image_size)

  本例演示如何将图片调整到不同的尺寸。

- [为图片显示替换文本](http://www.w3school.com.cn/tiy/t.asp?f=html_image_alt)

  本例演示如何为图片显示替换文本。在浏览器无法载入图像时，替换文本属性告诉读者们失去的信息。为页面上的图像都加上替换文本属性是个好习惯。

- [制作图像链接](http://www.w3school.com.cn/tiy/t.asp?f=html_image_link)

  本例演示如何将图像作为一个链接使用。

- [创建图像映射](http://www.w3school.com.cn/tiy/t.asp?f=html_areamap)

  本例显示如何创建带有可供点击区域的图像地图。其中的每个区域都是一个超级链接。

- [把图像转换为图像映射](http://www.w3school.com.cn/tiy/t.asp?f=html_ismap)

  本例显示如何把一幅普通的图像设置为图像映射。

### 图像标签

| 标签                                                 | 描述                         |
| ---------------------------------------------------- | ---------------------------- |
| [img](http://www.w3school.com.cn/tags/tag_img.asp)   | 定义图像。                   |
| [map](http://www.w3school.com.cn/tags/tag_map.asp)   | 定义图像地图。               |
| [area](http://www.w3school.com.cn/tags/tag_area.asp) | 定义图像地图中的可点击区域。 |

## HTML 表格

**你可以使用 HTML 创建表格。**

**实例**

- [表格](http://www.w3school.com.cn/tiy/t.asp?f=html_tables)

  这个例子演示如何在 HTML 文档中创建表格。

- [表格边框](http://www.w3school.com.cn/tiy/t.asp?f=html_table_borders)

  本例演示各种类型的表格边框。

（[可以在本页底端找到更多实例](http://www.w3school.com.cn/html/html_tables.asp#more_examples)。）

### 表格

表格由 <table> 标签来定义。每个表格均有若干行（由 <tr> 标签定义），每行被分割为若干单元格（由 <td> 标签定义）。字母 td 指表格数据（table data），即数据单元格的内容。数据单元格可以包含文本、图片、列表、段落、表单、水平线、表格等等。

```
<table border="1">
<tr>
<td>row 1, cell 1</td>
<td>row 1, cell 2</td>
</tr>
<tr>
<td>row 2, cell 1</td>
<td>row 2, cell 2</td>
</tr>
</table>
```

在浏览器显示如下：

| row 1, cell 1 | row 1, cell 2 |
| ------------- | ------------- |
| row 2, cell 1 | row 2, cell 2 |

### 表格和边框属性

如果不定义边框属性，表格将不显示边框。有时这很有用，但是大多数时候，我们希望显示边框。

使用边框属性来显示一个带有边框的表格：

```
<table border="1">
<tr>
<td>Row 1, cell 1</td>
<td>Row 1, cell 2</td>
</tr>
</table>
```

### 表格的表头

表格的表头使用 <th> 标签进行定义。

大多数浏览器会把表头显示为粗体居中的文本：

```
<table border="1">
<tr>
<th>Heading</th>
<th>Another Heading</th>
</tr>
<tr>
<td>row 1, cell 1</td>
<td>row 1, cell 2</td>
</tr>
<tr>
<td>row 2, cell 1</td>
<td>row 2, cell 2</td>
</tr>
</table>
```

在浏览器显示如下：

| Heading       | Another Heading |
| ------------- | --------------- |
| row 1, cell 1 | row 1, cell 2   |
| row 2, cell 1 | row 2, cell 2   |

### 表格中的空单元格

在一些浏览器中，没有内容的表格单元显示得不太好。如果某个单元格是空的（没有内容），浏览器可能无法显示出这个单元格的边框。

```
<table border="1">
<tr>
<td>row 1, cell 1</td>
<td>row 1, cell 2</td>
</tr>
<tr>
<td></td>
<td>row 2, cell 2</td>
</tr>
</table>
```

浏览器可能会这样显示：

![表格中的空单元格](http://www.w3school.com.cn/i/table_td_empty.gif)

注意：这个空的单元格的边框没有被显示出来。为了避免这种情况，在空单元格中添加一个空格占位符，就可以将边框显示出来。

```
<table border="1">
<tr>
<td>row 1, cell 1</td>
<td>row 1, cell 2</td>
</tr>
<tr>
<td>&nbsp;</td>
<td>row 2, cell 2</td>
</tr>
</table>
```

在浏览器中显示如下：

| row 1, cell 1 | row 1, cell 2 |
| ------------- | ------------- |
|               | row 2, cell 2 |

### 更多实例

- [没有边框的表格](http://www.w3school.com.cn/tiy/t.asp?f=html_tables2)

  本例演示一个没有边框的表格。

- [表格中的表头(Heading)](http://www.w3school.com.cn/tiy/t.asp?f=html_table_headers)

  本例演示如何显示表格表头。

- [空单元格](http://www.w3school.com.cn/tiy/t.asp?f=html_table_nbsp)

  本例展示如何使用 "&nbsp;" 处理没有内容的单元格。

- [带有标题的表格](http://www.w3school.com.cn/tiy/t.asp?f=html_tables3)

  本例演示一个带标题 (caption) 的表格

- [跨行或跨列的表格单元格](http://www.w3school.com.cn/tiy/t.asp?f=html_table_span)

  本例演示如何定义跨行或跨列的表格单元格。

- [表格内的标签](http://www.w3school.com.cn/tiy/t.asp?f=html_table_elements)

  本例演示如何显示在不同的元素内显示元素。

- [单元格边距(Cell padding)](http://www.w3school.com.cn/tiy/t.asp?f=html_table_cellpadding)

  本例演示如何使用 Cell padding 来创建单元格内容与其边框之间的空白。

- [单元格间距(Cell spacing)](http://www.w3school.com.cn/tiy/t.asp?f=html_table_cellspacing)

  本例演示如何使用 Cell spacing 增加单元格之间的距离。

- [向表格添加背景颜色或背景图像](http://www.w3school.com.cn/tiy/t.asp?f=html_table_background)

  本例演示如何向表格添加背景。

- [向表格单元添加背景颜色或者背景图像](http://www.w3school.com.cn/tiy/t.asp?f=html_table_cellbackground)

  本例演示如何向一个或者更多表格单元添加背景。

- [在表格单元中排列内容](http://www.w3school.com.cn/tiy/t.asp?f=html_table_align)

  本例演示如何使用 "align" 属性排列单元格内容,以便创建一个美观的表格。

- [框架(frame)属性](http://www.w3school.com.cn/tiy/t.asp?f=html_table_frame)

  本例演示如何使用 "frame" 属性来控制围绕表格的边框。

### 表格标签

| 表格                                                       | 描述                   |
| ---------------------------------------------------------- | ---------------------- |
| [table](http://www.w3school.com.cn/tags/tag_table.asp)     | 定义表格               |
| [caption](http://www.w3school.com.cn/tags/tag_caption.asp) | 定义表格标题。         |
| [th](http://www.w3school.com.cn/tags/tag_th.asp)           | 定义表格的表头。       |
| tr                                                         | 定义表格的行。         |
| [td](http://www.w3school.com.cn/tags/tag_td.asp)           | 定义表格单元。         |
| thead                                                      | 定义表格的页眉。       |
| tbody                                                      | 定义表格的主体。       |
| tfoot                                                      | 定义表格的页脚。       |
| col                                                        | 定义用于表格列的属性。 |
| colgroup                                                   | 定义表格列的组。       |

## HTML 列表

**HTML 支持有序、无序和定义列表**

**实例**

- [无序列表](http://www.w3school.com.cn/tiy/t.asp?f=html_list_unordered)

  本例演示无序列表。

- [有序列表](http://www.w3school.com.cn/tiy/t.asp?f=html_list_ordered)

  本例演示有序列表。

（[可以在本页底端找到更多实例](http://www.w3school.com.cn/html/html_lists.asp#more_examples)。）

### 无序列表

无序列表是一个项目的列表，此列项目使用粗体圆点（典型的小黑圆圈）进行标记。

无序列表始于 <ul> 标签。每个列表项始于 <li>。

```
<ul>
<li>Coffee</li>
<li>Milk</li>
</ul>
```

浏览器显示如下：

- Coffee
- Milk

列表项内部可以使用段落、换行符、图片、链接以及其他列表等等。

### 有序列表

同样，有序列表也是一列项目，列表项目使用数字进行标记。

有序列表始于 <ol> 标签。每个列表项始于 <li> 标签。

```
<ol>
<li>Coffee</li>
<li>Milk</li>
</ol>
```

浏览器显示如下：

1. Coffee
2. Milk

列表项内部可以使用段落、换行符、图片、链接以及其他列表等等。

### 定义列表

自定义列表不仅仅是一列项目，而是项目及其注释的组合。

自定义列表以 <dl> 标签开始。每个自定义列表项以 <dt> 开始。每个自定义列表项的定义以 <dd> 开始。

```
<dl>
<dt>Coffee</dt>
<dd>Black hot drink</dd>
<dt>Milk</dt>
<dd>White cold drink</dd>
</dl>
```

浏览器显示如下：

- Coffee

  Black hot drink

- Milk

  White cold drink

定义列表的列表项内部可以使用段落、换行符、图片、链接以及其他列表等等。

### 更多实例

- [不同类型的无序列表](http://www.w3school.com.cn/tiy/t.asp?f=html_lists_unordered)

  本例演示一个无序列表。

- [不同类型的有序列表](http://www.w3school.com.cn/tiy/t.asp?f=html_lists_ordered)

  本例演示不同类型的有序列表。

- [嵌套列表](http://www.w3school.com.cn/tiy/t.asp?f=html_lists_nested)

  本例演示如何嵌套列表。

- [嵌套列表 2](http://www.w3school.com.cn/tiy/t.asp?f=html_lists_nested2)

  本例演示更复杂的嵌套列表。

- [定义列表](http://www.w3school.com.cn/tiy/t.asp?f=html_list_definition)

  本例演示一个定义列表。

### 列表标签

| 标签                                                 | 描述                       |
| ---------------------------------------------------- | -------------------------- |
| [ol](http://www.w3school.com.cn/tags/tag_ol.asp)     | 定义有序列表。             |
| [ul](http://www.w3school.com.cn/tags/tag_ul.asp)     | 定义无序列表。             |
| [li](http://www.w3school.com.cn/tags/tag_li.asp)     | 定义列表项。               |
| [dl](http://www.w3school.com.cn/tags/tag_dl.asp)     | 定义定义列表。             |
| [dt](http://www.w3school.com.cn/tags/tag_dt.asp)     | 定义定义项目。             |
| [dd](http://www.w3school.com.cn/tags/tag_dd.asp)     | 定义定义的描述。           |
| [dir](http://www.w3school.com.cn/tags/tag_dir.asp)   | 已废弃。使用 <ul> 代替它。 |
| [menu](http://www.w3school.com.cn/tags/tag_menu.asp) | 已废弃。使用 <ul> 代替它。 |

## HTML块元素

###  **&lt;div> 和 &lt;span>**

**可以通过 <div> 和 <span> 将 HTML 元素组合起来。**

大多数 HTML 元素被定义为块级元素或内联元素。

编者注：“块级元素”译为 block level element，“内联元素”译为 inline element。

块级元素在浏览器显示时，通常会以新行来开始（和结束）。

例子：<h1>, <p>, <ul>, <table>

### HTML 内联元素

内联元素在显示时通常不会以新行开始。

例子：<b>, <td>, <a>, <img>

### HTML &lt;div> 元素

HTML <div> 元素是块级元素，它是可用于组合其他 HTML 元素的容器。

<div> 元素没有特定的含义。除此之外，由于它属于块级元素，浏览器会在其前后显示折行。

如果与 CSS 一同使用，<div> 元素可用于对大的内容块设置样式属性。

<div> 元素的另一个常见的用途是文档布局。它取代了使用表格定义布局的老式方法。使用 <table> 元素进行文档布局不是表格的正确用法。<table> 元素的作用是显示表格化的数据。

### HTML &lt;span> 元素

HTML <span> 元素是内联元素，可用作文本的容器。

<span> 元素也没有特定的含义。

当与 CSS 一同使用时，<span> 元素可用于为部分文本设置样式属性。

### HTML 分组标签

| 标签                                                 | 描述                                       |
| ---------------------------------------------------- | ------------------------------------------ |
| [div](http://www.w3school.com.cn/tags/tag_div.asp)   | 定义文档中的分区或节（division/section）。 |
| [span](http://www.w3school.com.cn/tags/tag_span.asp) | 定义 span，用来组合文档中的行内元素。      |

## HTML 类

对 HTML 进行分类（设置类），使我们能够为元素的类定义 CSS 样式。

为相同的类设置相同的样式，或者为不同的类设置不同的样式。

<iframe src="http://www.w3school.com.cn/demo/html_classes_london.asp" width="500" height="330" style="margin: 0px; padding: 0px; border: 0px;"></iframe>

**实例**

```
<!DOCTYPE html>
<html>
<head>
<style>
.cities {
    background-color:black;
    color:white;
    margin:20px;
    padding:20px;
} 
</style>
</head>

<body>

<div class="cities">
<h2>London</h2>
<p>
London is the capital city of England. 
It is the most populous city in the United Kingdom, 
with a metropolitan area of over 13 million inhabitants.
</p>
</div> 

</body>
</html>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_classes_shanghai)

### 分类块级元素

HTML <div> 元素是*块级元素*。它能够用作其他 HTML 元素的容器。

设置 <div> 元素的类，使我们能够为相同的 <div> 元素设置相同的类：

<iframe src="http://www.w3school.com.cn/demo/html_classes_cities.asp" width="500" height="1020" style="margin: 0px; padding: 0px; border: 0px;"></iframe>

**实例**

```
<!DOCTYPE html>
<html>
<head>
<style>
.cities {
    background-color:black;
    color:white;
    margin:20px;
    padding:20px;
} 
</style>
</head>

<body>

<div class="cities">
<h2>London</h2>
<p>London is the capital city of England. 
It is the most populous city in the United Kingdom, 
with a metropolitan area of over 13 million inhabitants.</p>
</div>

<div class="cities">
<h2>Paris</h2>
<p>Paris is the capital and most populous city of France.</p>
</div>

<div class="cities">
<h2>Tokyo</h2>
<p>Tokyo is the capital of Japan, the center of the Greater Tokyo Area,
and the most populous metropolitan area in the world.</p>
</div>

</body>
</html>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_classes_cities)

### 分类行内元素

HTML <span> 元素是行内元素，能够用作文本的容器。

设置 <span> 元素的类，能够为相同的 <span> 元素设置相同的样式。

**实例**

```
<!DOCTYPE html>
<html>
<head>
<style>
  span.red {color:red;}
</style>
</head>
<body>

<h1>My <span class="red">Important</span> Heading</h1>

</body>
</html>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_classes_span)

## HTML 布局

网站常常以多列显示内容（就像杂志和报纸）。

<iframe src="http://www.w3school.com.cn/demo/html_layout_divs.asp" width="680" height="450" style="margin: 0px; padding: 0px; border: 0px;"></iframe>

### 使用 &lt;div> 元素的 HTML 布局

注释：<div> 元素常用作布局工具，因为能够轻松地通过 CSS 对其进行定位。

这个例子使用了四个 <div> 元素来创建多列布局：

**实例**

```
<body>

<div id="header">
<h1>City Gallery</h1>
</div>

<div id="nav">
London<br>
Paris<br>
Tokyo<br>
</div>

<div id="section">
<h1>London</h1>
<p>
London is the capital city of England. It is the most populous city in the United Kingdom,
with a metropolitan area of over 13 million inhabitants.
</p>
<p>
Standing on the River Thames, London has been a major settlement for two millennia,
its history going back to its founding by the Romans, who named it Londinium.
</p>
</div>

<div id="footer">
Copyright W3School.com.cn
</div>

</body>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_layout_divs)

**CSS：**

```
<style>
#header {
    background-color:black;
    color:white;
    text-align:center;
    padding:5px;
}
#nav {
    line-height:30px;
    background-color:#eeeeee;
    height:300px;
    width:100px;
    float:left;
    padding:5px; 
}
#section {
    width:350px;
    float:left;
    padding:10px; 
}
#footer {
    background-color:black;
    color:white;
    clear:both;
    text-align:center;
    padding:5px; 
}
</style>
```

### 使用 HTML5 的网站布局

HTML5 提供的新语义元素定义了网页的不同部分：

### HTML5 语义元素

| header  | 定义文档或节的页眉             |
| ------- | ------------------------------ |
| nav     | 定义导航链接的容器             |
| section | 定义文档中的节                 |
| article | 定义独立的自包含文章           |
| aside   | 定义内容之外的内容（比如侧栏） |
| footer  | 定义文档或节的页脚             |
| details | 定义额外的细节                 |
| summary | 定义 details 元素的标题        |

这个例子使用 <header>, <nav>, <section>, 以及 <footer> 来创建多列布局：

**实例**

```
<body>

<header>
<h1>City Gallery</h1>
</header>

<nav>
London<br>
Paris<br>
Tokyo<br>
</nav>

<section>
<h1>London</h1>
<p>
London is the capital city of England. It is the most populous city in the United Kingdom,
with a metropolitan area of over 13 million inhabitants.
</p>
<p>
Standing on the River Thames, London has been a major settlement for two millennia,
its history going back to its founding by the Romans, who named it Londinium.
</p>
</section>

<footer>
Copyright W3School.com.cn
</footer>

</body>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_layout_semantic)

**CSS**

```
<style>
header {
    background-color:black;
    color:white;
    text-align:center;
    padding:5px; 
}
nav {
    line-height:30px;
    background-color:#eeeeee;
    height:300px;
    width:100px;
    float:left;
    padding:5px; 
}
section {
    width:350px;
    float:left;
    padding:10px; 
}
footer {
    background-color:black;
    color:white;
    clear:both;
    text-align:center;
    padding:5px; 
}
```

### 使用表格的 HTML 布局

注释：<table> 元素不是作为布局工具而设计的。

<table> 元素的作用是显示表格化的数据。

使用 <table> 元素能够取得布局效果，因为能够通过 CSS 设置表格元素的样式：

**实例**

```
<body>

<table class="lamp">
<tr>
  <th>
    <img src="/images/lamp.jpg" alt="Note" style="height:32px;width:32px">
  </th>
  <td>
    The table element was not designed to be a layout tool.
  </td>
</tr>
</table>

</body>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_layout_tables)

**CSS**

```
<style>
table.lamp {
    width:100%;
    border:1px solid #d4d4d4;
}
table.lamp th, td {
    padding:10px;
}
table.lamp td {
    width:40px;
}
</style>
```

##  HTML 响应式 Web 设计

### 什么是响应式 Web 设计？

- RWD 指的是响应式 Web 设计（Responsive Web Design）
- RWD 能够以可变尺寸传递网页
- RWD 对于平板和移动设备是必需的

### 创建您自己的响应式设计

创建响应式设计的一个方法，是自己来创建它：

```
<!DOCTYPE html>
<html lang="en-US">
<head>
<style>
.city {
float: left;
margin: 5px;
padding: 15px;
width: 300px;
height: 300px;
border: 1px solid black;
} 
</style>
</head>

<body>

<h1>W3School Demo</h1>
<h2>Resize this responsive page!</h2>
<br>

<div class="city">
<h2>London</h2>
<p>London is the capital city of England.</p>
<p>It is the most populous city in the United Kingdom,
with a metropolitan area of over 13 million inhabitants.</p>
</div>

<div class="city">
<h2>Paris</h2>
<p>Paris is the capital and most populous city of France.</p>
</div>

<div class="city">
<h2>Tokyo</h2>
<p>Tokyo is the capital of Japan, the center of the Greater Tokyo Area,
and the most populous metropolitan area in the world.</p>
</div>

</body>
</html>
```

[亲自试一试](http://www.w3school.com.cn/demo/demo_rwd_simple.html)

### 使用 Bootstrap

另一个创建响应式设计的方法，是使用现成的 CSS 框架。

Bootstrap 是最流行的开发响应式 web 的 HTML, CSS, 和 JS 框架。

Bootstrap 帮助您开发在任何尺寸都外观出众的站点：显示器、笔记本电脑、平板电脑或手机：

```
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link rel="stylesheet" 
  href="http://maxcdn.bootstrapcdn.com/bootstrap/3.2.0/css/bootstrap.min.css">
</head>

<body>

<div class="container">
<div class="jumbotron">
  <h1>W3School Demo</h1> 
  <p>Resize this responsive page!</p> 
</div>
</div>

<div class="container">
<div class="row">
  <div class="col-md-4">
    <h2>London</h2>
    <p>London is the capital city of England.</p>
    <p>It is the most populous city in the United Kingdom,
    with a metropolitan area of over 13 million inhabitants.</p>
  </div>
  <div class="col-md-4">
    <h2>Paris</h2>
    <p>Paris is the capital and most populous city of France.</p>
  </div>
  <div class="col-md-4">
    <h2>Tokyo</h2>
    <p>Tokyo is the capital of Japan, the center of the Greater Tokyo Area,
    and the most populous metropolitan area in the world.</p>
  </div>
</div>
</div>

</body>
</html>
```

[亲自试一试](http://www.w3school.com.cn/demo/demo_rwd_bootstrap.html)

如需学习更多有关 Bootstrap 的知识，请阅读我们的 Bootstrap 教程。

##   HTML 框架

**通过使用框架，你可以在同一个浏览器窗口中显示不止一个页面。**

**实例**

- [垂直框架](http://www.w3school.com.cn/tiy/t.asp?f=html_frame_cols)

  本例演示：如何使用三份不同的文档制作一个垂直框架。

- [水平框架](http://www.w3school.com.cn/tiy/t.asp?f=html_frame_rows)

  本例演示：如何使用三份不同的文档制作一个水平框架。

（[可以在本页底端找到更多实例](http://www.w3school.com.cn/html/html_frames.asp#more_examples)。）

### 框架

通过使用框架，你可以在同一个浏览器窗口中显示不止一个页面。每份HTML文档称为一个框架，并且每个框架都独立于其他的框架。

使用框架的坏处：

- 开发人员必须同时跟踪更多的HTML文档
- 很难打印整张页面

- 框架结构标签（<frameset>）

  框架结构标签（<frameset>）定义如何将窗口分割为框架每个 frameset 定义了一系列行*或*列rows/columns 的值规定了每行或每列占据屏幕的面积

编者注：frameset 标签也被某些文章和书籍译为框架集。

### 框架标签（Frame）

Frame 标签定义了放置在每个框架中的 HTML 文档。

在下面的这个例子中，我们设置了一个两列的框架集。第一列被设置为占据浏览器窗口的 25%。第二列被设置为占据浏览器窗口的 75%。HTML 文档 "frame_a.htm" 被置于第一个列中，而 HTML 文档 "frame_b.htm" 被置于第二个列中：

```
<frameset cols="25%,75%">
   <frame src="frame_a.htm">
   <frame src="frame_b.htm">
</frameset>
```

### 基本的注意事项 - 有用的提示：

假如一个框架有可见边框，用户可以拖动边框来改变它的大小。为了避免这种情况发生，可以在 <frame> 标签中加入：noresize="noresize"。

为不支持框架的浏览器添加 <noframes> 标签。

重要提示：不能将 <body></body> 标签与 <frameset></frameset> 标签同时使用！不过，假如你添加包含一段文本的 <noframes> 标签，就必须将这段文字嵌套于 <body></body> 标签内。（在下面的第一个实例中，可以查看它是如何实现的。）

### 更多实例

- [如何使用  标签](http://www.w3school.com.cn/tiy/t.asp?f=html_noframes)

  本例演示：如何使用 <noframes> 标签。

- [混合框架结构](http://www.w3school.com.cn/tiy/t.asp?f=html_frame_mix)

  本例演示如何制作含有三份文档的框架结构，同时将他们混合置于行和列之中。

- [含有 noresize="noresize" 属性的框架结构](http://www.w3school.com.cn/tiy/t.asp?f=html_frame_noresize)

  本例演示 noresize 属性。在本例中，框架是不可调整尺寸的。在框架间的边框上拖动鼠标，你会发现边框是无法移动的。

- [导航框架](http://www.w3school.com.cn/tiy/t.asp?f=html_frame_navigation)

  本例演示如何制作导航框架。导航框架包含一个将第二个框架作为目标的链接列表。名为 "contents.htm" 的文件包含三个链接。

- [内联框架](http://www.w3school.com.cn/tiy/t.asp?f=html_iframe)

  本例演示如何创建内联框架（HTML 页中的框架）。

- [跳转至框架内的一个指定的节](http://www.w3school.com.cn/tiy/t.asp?f=html_frame_jump)

  本例演示两个框架。其中的一个框架设置了指向另一个文件内指定的节的链接。这个"link.htm"文件内指定的节使用 <a name="C10"> 进行标识。

- [使用框架导航跳转至指定的节](http://www.w3school.com.cn/tiy/t.asp?f=html_frame_navigation2)

  本例演示两个框架。左侧的导航框架包含了一个链接列表，这些链接将第二个框架作为目标。第二个框架显示被链接的文档。导航框架其中的链接指向目标文件中指定的节。

##   HTML Iframe

**iframe 用于在网页内显示网页。**

<iframe src="http://www.w3school.com.cn/html/index.asp" height="300px" width="99%" style="margin: 15px 0px 0px; padding: 0px; border: 0px;"></iframe>

### 添加 iframe 的语法

```
<iframe src="URL"></iframe>
```

*URL* 指向隔离页面的位置。

### Iframe - 设置高度和宽度

height 和 width 属性用于规定 iframe 的高度和宽度。

属性值的默认单位是像素，但也可以用百分比来设定（比如 "80%"）。

**实例**

```
<iframe src="demo_iframe.htm" width="200" height="200"></iframe>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_iframe_height_width)

### Iframe - 删除边框

frameborder 属性规定是否显示 iframe 周围的边框。

设置属性值为 "0" 就可以移除边框：

**实例**

```
<iframe src="demo_iframe.htm" frameborder="0"></iframe>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_iframe_frameborder)

### 使用 iframe 作为链接的目标

iframe 可用作链接的目标（target）。

链接的 target 属性必须引用 iframe 的 name 属性：

**实例**

```
<iframe src="demo_iframe.htm" name="iframe_a"></iframe>
<p><a href="http://www.w3school.com.cn" target="iframe_a">W3School.com.cn</a></p>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_iframe_target)

### HTML iframe 标签

| 标签                                                     | 描述                     |
| -------------------------------------------------------- | ------------------------ |
| [iframe](http://www.w3school.com.cn/tags/tag_iframe.asp) | 定义内联的子窗口（框架） |

## HTML 背景

**好的背景使站点看上去特别棒。**

**实例**

- [搭配良好的背景和颜色](http://www.w3school.com.cn/tiy/t.asp?f=html_back_good)

  一个背景颜色和文字颜色搭配良好的例子，使页面中的文字易于阅读。

- [搭配得不好的背景和颜色](http://www.w3school.com.cn/tiy/t.asp?f=html_back_bad)

  一个背景颜色和文字颜色搭配得不好的例子，使页面中的文字难于阅读。

（[可以在本页底端找到更多实例](http://www.w3school.com.cn/html/html_backgrounds.asp#more_examples)。）

### 背景（Backgrounds）

&lt;body> 拥有两个配置背景的标签。背景可以是颜色或者图像。

### 背景颜色（Bgcolor）

背景颜色属性将背景设置为某种颜色。属性值可以是十六进制数、RGB 值或颜色名。

```
<body bgcolor="#000000">
<body bgcolor="rgb(0,0,0)">
<body bgcolor="black">
```

以上的代码均将背景颜色设置为黑色。

### 背景（Background）

背景属性将背景设置为图像。属性值为图像的URL。如果图像尺寸小于浏览器窗口，那么图像将在整个浏览器窗口进行复制。

```
<body background="clouds.gif">
<body background="http://www.w3school.com.cn/clouds.gif">
```

URL可以是相对地址，如第一行代码。也可以使绝对地址，如第二行代码。

提示：如果你打算使用背景图片，你需要紧记一下几点：

- 背景图像是否增加了页面的加载时间。小贴士：图像文件不应超过 10k。
- 背景图像是否与页面中的其他图象搭配良好。
- 背景图像是否与页面中的文字颜色搭配良好。
- 图像在页面中平铺后，看上去还可以吗？
- 对文字的注意力被背景图像喧宾夺主了吗？

### 基本的注意事项 - 有用的提示：

<body> 标签中的背景颜色（bgcolor）、背景（background）和文本（text）属性在最新的 HTML 标准（HTML4 和 XHTML）中已被废弃。W3C 在他们的推荐标准中已删除这些属性。

应该使用层叠样式表（CSS）来定义 HTML 元素的布局和显示属性。

### 更多实例

- [可用性强的背t景图像](http://www.w3school.com.cn/tiy/t.asp?f=html_back_img)

  背景图像和文字颜色使页面文本易于阅读的例子。

- [可用性强的背景图像 2](http://www.w3school.com.cn/tiy/t.asp?f=html_back_img2)

  另一个背景图像和文字颜色使页面文本易于阅读的例子。

- [可用性差的背景图像](http://www.w3school.com.cn/tiy/t.asp?f=html_back_imgbad)

  背景图像和文字颜色使页面文本不易阅读的例子。




## HTML 脚本

**JavaScript 使 HTML 页面具有更强的动态和交互性。。**

**实例**

- [插入一段脚本](http://www.w3school.com.cn/tiy/t.asp?f=html_script)

  如何将脚本插入 HTML 文档。

- [使用  标签](http://www.w3school.com.cn/tiy/t.asp?f=html_noscript)

  如何应对不支持脚本或禁用脚本的浏览器。

### HTML script 元素

<script> 标签用于定义客户端脚本，比如 JavaScript。

script 元素既可包含脚本语句，也可通过 src 属性指向外部脚本文件。

必需的 type 属性规定脚本的 MIME 类型。

JavaScript 最常用于图片操作、表单验证以及内容动态更新。

下面的脚本会向浏览器输出“Hello World!”：

```
<script type="text/javascript">
document.write("Hello World!")
</script>
```

提示：如果需要学习更多有关在 HTML 中编写脚本的知识，请访问我们的 [JavaScript 教程](http://www.w3school.com.cn/js/index.asp)。

### &lt;noscript> 标签

<noscript> 标签提供无法使用脚本时的替代内容，比方在浏览器禁用脚本时，或浏览器不支持客户端脚本时。

noscript 元素可包含普通 HTML 页面的 body 元素中能够找到的所有元素。

只有在浏览器不支持脚本或者禁用脚本时，才会显示 noscript 元素中的内容：

```
<script type="text/javascript">
document.write("Hello World!")
</script>
<noscript>Your browser does not support JavaScript!</noscript>
```

### 如何应付老式的浏览器

如果浏览器压根没法识别 <script> 标签，那么 <script> 标签所包含的内容将以文本方式显示在页面上。为了避免这种情况发生，你应该将脚本隐藏在注释标签当中。那些老的浏览器（无法识别 <script> 标签的浏览器）将忽略这些注释，所以不会将标签的内容显示到页面上。而那些新的浏览器将读懂这些脚本并执行它们，即使代码被嵌套在注释标签内。

**实例**

#### JavaScript:

```
<script type="text/javascript">
<!--
document.write("Hello World!")
//-->
</script>
```

#### VBScript:

```
<script type="text/vbscript">
<!--
document.write("Hello World!")
'-->
</script>
```

| 标签                                                         | 描述                                     |
| ------------------------------------------------------------ | ---------------------------------------- |
| [script](http://www.w3school.com.cn/tags/tag_script.asp)     | 定义客户端脚本。                         |
| [noscript](http://www.w3school.com.cn/tags/tag_noscript.asp) | 为不支持客户端脚本的浏览器定义替代内容。 |

## HTML 头部元素



### 亲自试一试 - 实例

- [文档的标题](http://www.w3school.com.cn/tiy/t.asp?f=html_title)

  <title> 标题定义文档的标题。

- [所有链接一个目标](http://www.w3school.com.cn/tiy/t.asp?f=html_base)

  如何使用 base 标签使页面中的所有标签在新窗口中打开。

- [文档描述](http://www.w3school.com.cn/tiy/t.asp?f=html_meta)

  使用 <meta> 元素来描述文档。

- [文档关键词](http://www.w3school.com.cn/tiy/t.asp?f=html_keywords)

  使用 <meta> 元素来定义文档的关键词。

- [重定向用户](http://www.w3school.com.cn/tiy/t.asp?f=html_redirect)

  如何把用户重定向到新的网址。

### HTML &lt;head> 元素

<head> 元素是所有头部元素的容器。<head> 内的元素可包含脚本，指示浏览器在何处可以找到样式表，提供元信息，等等。

以下标签都可以添加到 head 部分：<title>、<base>、<link>、<meta>、<script> 以及 <style>。

### HTML &lt;title> 元素

<title> 标签定义文档的标题。

title 元素在所有 HTML/XHTML 文档中都是必需的。

title 元素能够：

- 定义浏览器工具栏中的标题
- 提供页面被添加到收藏夹时显示的标题
- 显示在搜索引擎结果中的页面标题

一个简化的 HTML 文档：

```
<!DOCTYPE html>
<html>
<head>
<title>Title of the document</title>
</head>

<body>
The content of the document......
</body>

</html>
```

### HTML &lt;base> 元素

<base> 标签为页面上的所有链接规定默认地址或默认目标（target）：

```
<head>
<base href="http://www.w3school.com.cn/images/" />
<base target="_blank" />
</head>
```

### HTML &lt;link> 元素

<link> 标签定义文档与外部资源之间的关系。

<link> 标签最常用于连接样式表：

```
<head>
<link rel="stylesheet" type="text/css" href="mystyle.css" />
</head>
```

### HTML &lt;style> 元素

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

### HTML &lt;meta> 元素

元数据（metadata）是关于数据的信息。

<meta> 标签提供关于 HTML 文档的元数据。元数据不会显示在页面上，但是对于机器是可读的。

典型的情况是，meta 元素被用于规定页面的描述、关键词、文档的作者、最后修改时间以及其他元数据。

<meta> 标签始终位于 head 元素中。

元数据可用于浏览器（如何显示内容或重新加载页面），搜索引擎（关键词），或其他 web 服务。

### 针对搜索引擎的关键词

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

### HTML &lt;script> 元素

<script> 标签用于定义客户端脚本，比如 JavaScript。

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

## HTML 字符实体

**HTML 中的预留字符必须被替换为字符实体。**

### HTML 实体

在 HTML 中，某些字符是预留的。

在 HTML 中不能使用小于号（<）和大于号（>），这是因为浏览器会误认为它们是标签。

如果希望正确地显示预留字符，我们必须在 HTML 源代码中使用字符实体（character entities）。

字符实体类似这样：

```
&entity_name;

或者

&#entity_number;
```

如需显示小于号，我们必须这样写：&lt; 或 &#60;

提示：使用实体名而不是数字的好处是，名称易于记忆。不过坏处是，浏览器也许并不支持所有实体名称（对实体数字的支持却很好）。

### 不间断空格（non-breaking space）

HTML 中的常用字符实体是不间断空格(&nbsp;)。

浏览器总是会截短 HTML 页面中的空格。如果您在文本中写 10 个空格，在显示该页面之前，浏览器会删除它们中的 9 个。如需在页面中增加空格的数量，您需要使用 &nbsp; 字符实体。

### HTML 实例示例

用 HTML 实体符号做实验：[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_entities)

### HTML 中有用的字符实体

注释：实体名称对大小写敏感！

| 显示结果 | 描述              | 实体名称          | 实体编号 |
| -------- | ----------------- | ----------------- | -------- |
|          | 空格              | &nbsp;            | &#160;   |
| <        | 小于号            | &lt;              | &#60;    |
| >        | 大于号            | &gt;              | &#62;    |
| &        | 和号              | &amp;             | &#38;    |
| "        | 引号              | &quot;            | &#34;    |
| '        | 撇号              | &apos; (IE不支持) | &#39;    |
| ￠       | 分（cent）        | &cent;            | &#162;   |
| £        | 镑（pound）       | &pound;           | &#163;   |
| ¥        | 元（yen）         | &yen;             | &#165;   |
| €        | 欧元（euro）      | &euro;            | &#8364;  |
| §        | 小节              | &sect;            | &#167;   |
| ©        | 版权（copyright） | &copy;            | &#169;   |
| ®        | 注册商标          | &reg;             | &#174;   |
| ™        | 商标              | &trade;           | &#8482;  |
| ×        | 乘号              | &times;           | &#215;   |
| ÷        | 除号              | &divide;          | &#247;   |

如需完整的实体符号参考，请访问我们的 [HTML 实体符号参考手册](http://www.w3school.com.cn/tags/html_ref_entities.html)。

## HTML 统一资源定位器

URL 也被称为网址。

URL 可以由单词组成，比如 “w3school.com.cn”，或者是因特网协议（IP）地址：192.168.1.253。大多数人在网上冲浪时，会键入网址的域名，因为名称比数字容易记忆。

### URL - Uniform Resource Locator

当您点击 HTML 页面中的某个链接时，对应的 <a> 标签指向万维网上的一个地址。

统一资源定位器（URL）用于定位万维网上的文档（或其他数据）。

网址，比如 <http://www.w3school.com.cn/html/index.asp>，遵守以下的语法规则：

```
scheme://host.domain:port/path/filename
```

解释：

- scheme - 定义因特网服务的类型。最常见的类型是 http
- host - 定义域主机（http 的默认主机是 www）
- domain - 定义因特网域名，比如 w3school.com.cn
- :port - 定义主机上的端口号（http 的默认端口号是 80）
- path - 定义服务器上的路径（如果省略，则文档必须位于网站的根目录中）。
- filename - 定义文档/资源的名称

编者注：URL 的英文全称是 Uniform Resource Locator，中文也译为“统一资源定位符”。

### URL Schemes

以下是其中一些最流行的 scheme：

| Scheme | 访问               | 用于...                             |
| ------ | ------------------ | ----------------------------------- |
| http   | 超文本传输协议     | 以 http:// 开头的普通网页。不加密。 |
| https  | 安全超文本传输协议 | 安全网页。加密所有信息交换。        |
| ftp    | 文件传输协议       | 用于将文件下载或上传至网站。        |
| file   |                    | 您计算机上的文件。                  |

##   HTML URL 字符编码

**URL 编码会将字符转换为可通过因特网传输的格式。**

### URL - 统一资源定位器

Web 浏览器通过 URL 从 web 服务器请求页面。

URL 是网页的地址，比如 *http://www.w3school.com.cn*。

### URL 编码

URL 只能使用 [ASCII 字符集](http://www.w3school.com.cn/tags/html_ref_ascii.asp)来通过因特网进行发送。

由于 URL 常常会包含 ASCII 集合之外的字符，URL 必须转换为有效的 ASCII 格式。

URL 编码使用 "%" 其后跟随两位的十六进制数来替换非 ASCII 字符。

URL 不能包含空格。URL 编码通常使用 + 来替换空格。

### 亲自试一试

如果您点击下面的“提交”按钮，浏览器会在发送输入之前对其进行 URL 编码。服务器上的页面会显示出接收到的输入。

 

试着输入一些字符，然后再次点击提交按钮。

### URL 编码示例

| 字符 | URL 编码 |
| ---- | -------- |
| €    | %80      |
| £    | %A3      |
| ©    | %A9      |
| ®    | %AE      |
| À    | %C0      |
| Á    | %C1      |
| Â    | %C2      |
| Ã    | %C3      |
| Ä    | %C4      |
| Å    | %C5      |

如需完整的 URL 编码参考，请访问我们的 [URL 编码参考手册](http://www.w3school.com.cn/tags/html_ref_urlencode.html)。

##   HTML Web Server

**如果希望向世界发布您的网站，那么您必须把它存放在 web 服务器上。**

### 托管自己的网站

在自己的服务器上托管网站始终是一个选项。有几点需要考虑：

**硬件支出**

如果要运行“真正”的网站，您不得不购买强大的服务器硬件。不要指望低价的 PC 能够应付这些工作。您还需要稳定的（一天 24 小时）高速连接。

**软件支出**

请记住，服务器授权通常比客户端授权更昂贵。同时请注意，服务器授权也许有用户数量限制。

**人工费**

不要指望低廉的人工费用。您必须安装自己的硬件和软件。您同时要处理漏洞和病毒，以确保您的服务器时刻正常地运行于一个“任何事都可能发生”的环境中。

### 使用因特网服务提供商（ISP）

从 ISP 租用服务器也很常见。

大多数小公司会把网站存放到由 ISP 提供的服务器上。其优势有以下几点：

**连接速度**

大多数 ISP 都拥有连接因特网的高速连接。

**强大的硬件**

ISP 的 web 服务器通常强大到能够由若干网站分享资源。您还要看一下 ISP 是否提供高效的负载平衡，以及必要的备份服务器。

### 安全性和可靠性

ISP 是网站托管方面的专家。他们应该提供 99% 以上的在线时间，最新的软件补丁，以及最好的病毒防护。

### 选择 ISP 时的注意事项

**24** 小时支持

确保 ISP 提供 24 小时支持。不要使自己置于无法解决严重问题的尴尬境地，同时还必须等待第二个工作日。如果您不希望支付长途电话费，那么免费电话服务也是必要的。

**每日备份**

确保 ISP 会执行每日备份的例行工作，否则您有可能损失有价值的数据。

**流量**

研究一下 ISP 的流量限制。如果出现由于网站受欢迎而激增的不可预期的访问量，那么您要确保不会因此支付额外费用。

**带宽或内容限制**

研究一下 ISP 的带宽和内容限制。如果您计划发布图片或播出视频或音频，请确保您有此权限。

**E-mail 功能**

请确保 ISP 支持您需要的 e-mail 功能。

**数据库访问**

如果您计划使用网站数据库中的数据，那么请确保您的 ISP 支持您需要的数据库访问。

在您选取一家 ISP 之前，请务必阅读 W3School 的 [Web 主机教程](http://www.w3school.com.cn/hosting/index.asp)。

## HTML 颜色

**颜色由红色、绿色、蓝色混合而成。**

### 颜色值

颜色由一个十六进制符号来定义，这个符号由红色、绿色和蓝色的值组成（RGB）。

每种颜色的最小值是0（十六进制：#00）。最大值是255（十六进制：#FF）。

这个表格给出了由三种颜色混合而成的具体效果：

![](D:\ProjectList\Github_pages\media\color1.png)

### 颜色名

大多数的浏览器都支持颜色名集合。

提示：仅仅有 16 种颜色名被 W3C 的 HTML4.0 标准所支持。它们是：aqua, black, blue, fuchsia, gray, green, lime, maroon, navy, olive, purple, red, silver, teal, white, yellow。

如果需要使用其它的颜色，需要使用十六进制的颜色值。

![](D:\ProjectList\Github_pages\media\color2.png)

### Web安全色

数年以前，当大多数计算机仅支持 256 种颜色的时候，一系列 216 种 Web 安全色作为 Web 标准被建议使用。其中的原因是，微软和 Mac 操作系统使用了 40 种不同的保留的固定系统颜色（双方大约各使用 20 种）。

我们不确定如今这么做的意义有多大，因为越来越多的计算机有能力处理数百万种颜色，不过做选择还是你自己。

### 216 跨平台色

最初，216 跨平台 web 安全色被用来确保：当计算机使用 256 色调色板时，所有的计算机能够正确地显示所有的颜色。

![](D:\ProjectList\Github_pages\media\color3.png)

## HTML 颜色名



**本页提供了被大多数浏览器支持的颜色名。**

提示：仅有 16 种*颜色名*被 W3C 的 HTML 4.0 标准支持，它们是：aqua、black、blue、fuchsia、gray、green、lime、maroon、navy、olive、purple、red、silver、teal、white、yellow。

如果使用其它颜色的话，就应该使用*十六进制的颜色值*。

### 颜色名列表

单击一个颜色名或者 16 进制值，就可以查看与不同文字颜色搭配的背景颜色。

| 颜色名                                                       | 十六进制颜色值                                               | 颜色 |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ---- |
| [AliceBlue](http://www.w3school.com.cn/tiy/color.asp?color=AliceBlue) | [#F0F8FF](http://www.w3school.com.cn/tiy/color.asp?hex=F0F8FF) |      |
| [AntiqueWhite](http://www.w3school.com.cn/tiy/color.asp?color=AntiqueWhite) | [#FAEBD7](http://www.w3school.com.cn/tiy/color.asp?hex=FAEBD7) |      |
| [Aqua](http://www.w3school.com.cn/tiy/color.asp?color=Aqua)  | [#00FFFF](http://www.w3school.com.cn/tiy/color.asp?hex=00FFFF) |      |
| [Aquamarine](http://www.w3school.com.cn/tiy/color.asp?color=Aquamarine) | [#7FFFD4](http://www.w3school.com.cn/tiy/color.asp?hex=7FFFD4) |      |
| [Azure](http://www.w3school.com.cn/tiy/color.asp?color=Azure) | [#F0FFFF](http://www.w3school.com.cn/tiy/color.asp?hex=F0FFFF) |      |
| [Beige](http://www.w3school.com.cn/tiy/color.asp?color=Beige) | [#F5F5DC](http://www.w3school.com.cn/tiy/color.asp?hex=F5F5DC) |      |
| [Bisque](http://www.w3school.com.cn/tiy/color.asp?color=Bisque) | [#FFE4C4](http://www.w3school.com.cn/tiy/color.asp?hex=FFE4C4) |      |
| [Black](http://www.w3school.com.cn/tiy/color.asp?color=Black) | [#000000](http://www.w3school.com.cn/tiy/color.asp?hex=000000) |      |
| [BlanchedAlmond](http://www.w3school.com.cn/tiy/color.asp?color=BlanchedAlmond) | [#FFEBCD](http://www.w3school.com.cn/tiy/color.asp?hex=FFEBCD) |      |
| [Blue](http://www.w3school.com.cn/tiy/color.asp?color=Blue)  | [#0000FF](http://www.w3school.com.cn/tiy/color.asp?hex=0000FF) |      |
| [BlueViolet](http://www.w3school.com.cn/tiy/color.asp?color=BlueViolet) | [#8A2BE2](http://www.w3school.com.cn/tiy/color.asp?hex=8A2BE2) |      |
| [Brown](http://www.w3school.com.cn/tiy/color.asp?color=Brown) | [#A52A2A](http://www.w3school.com.cn/tiy/color.asp?hex=A52A2A) |      |
| [BurlyWood](http://www.w3school.com.cn/tiy/color.asp?color=BurlyWood) | [#DEB887](http://www.w3school.com.cn/tiy/color.asp?hex=DEB887) |      |
| [CadetBlue](http://www.w3school.com.cn/tiy/color.asp?color=CadetBlue) | [#5F9EA0](http://www.w3school.com.cn/tiy/color.asp?hex=5F9EA0) |      |
| [Chartreuse](http://www.w3school.com.cn/tiy/color.asp?color=Chartreuse) | [#7FFF00](http://www.w3school.com.cn/tiy/color.asp?hex=7FFF00) |      |
| [Chocolate](http://www.w3school.com.cn/tiy/color.asp?color=Chocolate) | [#D2691E](http://www.w3school.com.cn/tiy/color.asp?hex=D2691E) |      |
| [Coral](http://www.w3school.com.cn/tiy/color.asp?color=Coral) | [#FF7F50](http://www.w3school.com.cn/tiy/color.asp?hex=FF7F50) |      |
| [CornflowerBlue](http://www.w3school.com.cn/tiy/color.asp?color=CornflowerBlue) | [#6495ED](http://www.w3school.com.cn/tiy/color.asp?hex=6495ED) |      |
| [Cornsilk](http://www.w3school.com.cn/tiy/color.asp?color=Cornsilk) | [#FFF8DC](http://www.w3school.com.cn/tiy/color.asp?hex=FFF8DC) |      |
| [Crimson](http://www.w3school.com.cn/tiy/color.asp?color=Crimson) | [#DC143C](http://www.w3school.com.cn/tiy/color.asp?hex=DC143C) |      |
| [Cyan](http://www.w3school.com.cn/tiy/color.asp?color=Cyan)  | [#00FFFF](http://www.w3school.com.cn/tiy/color.asp?hex=00FFFF) |      |
| [DarkBlue](http://www.w3school.com.cn/tiy/color.asp?color=DarkBlue) | [#00008B](http://www.w3school.com.cn/tiy/color.asp?hex=00008B) |      |
| [DarkCyan](http://www.w3school.com.cn/tiy/color.asp?color=DarkCyan) | [#008B8B](http://www.w3school.com.cn/tiy/color.asp?hex=008B8B) |      |
| [DarkGoldenRod](http://www.w3school.com.cn/tiy/color.asp?color=DarkGoldenRod) | [#B8860B](http://www.w3school.com.cn/tiy/color.asp?hex=B8860B) |      |
| [DarkGray](http://www.w3school.com.cn/tiy/color.asp?color=DarkGray) | [#A9A9A9](http://www.w3school.com.cn/tiy/color.asp?hex=A9A9A9) |      |
| [DarkGreen](http://www.w3school.com.cn/tiy/color.asp?color=DarkGreen) | [#006400](http://www.w3school.com.cn/tiy/color.asp?hex=006400) |      |
| [DarkKhaki](http://www.w3school.com.cn/tiy/color.asp?color=DarkKhaki) | [#BDB76B](http://www.w3school.com.cn/tiy/color.asp?hex=BDB76B) |      |
| [DarkMagenta](http://www.w3school.com.cn/tiy/color.asp?color=DarkMagenta) | [#8B008B](http://www.w3school.com.cn/tiy/color.asp?hex=8B008B) |      |
| [DarkOliveGreen](http://www.w3school.com.cn/tiy/color.asp?color=DarkOliveGreen) | [#556B2F](http://www.w3school.com.cn/tiy/color.asp?hex=556B2F) |      |
| [Darkorange](http://www.w3school.com.cn/tiy/color.asp?color=Darkorange) | [#FF8C00](http://www.w3school.com.cn/tiy/color.asp?hex=FF8C00) |      |
| [DarkOrchid](http://www.w3school.com.cn/tiy/color.asp?color=DarkOrchid) | [#9932CC](http://www.w3school.com.cn/tiy/color.asp?hex=9932CC) |      |
| [DarkRed](http://www.w3school.com.cn/tiy/color.asp?color=DarkRed) | [#8B0000](http://www.w3school.com.cn/tiy/color.asp?hex=8B0000) |      |
| [DarkSalmon](http://www.w3school.com.cn/tiy/color.asp?color=DarkSalmon) | [#E9967A](http://www.w3school.com.cn/tiy/color.asp?hex=E9967A) |      |
| [DarkSeaGreen](http://www.w3school.com.cn/tiy/color.asp?color=DarkSeaGreen) | [#8FBC8F](http://www.w3school.com.cn/tiy/color.asp?hex=8FBC8F) |      |
| [DarkSlateBlue](http://www.w3school.com.cn/tiy/color.asp?color=DarkSlateBlue) | [#483D8B](http://www.w3school.com.cn/tiy/color.asp?hex=483D8B) |      |
| [DarkSlateGray](http://www.w3school.com.cn/tiy/color.asp?color=DarkSlateGray) | [#2F4F4F](http://www.w3school.com.cn/tiy/color.asp?hex=2F4F4F) |      |
| [DarkTurquoise](http://www.w3school.com.cn/tiy/color.asp?color=DarkTurquoise) | [#00CED1](http://www.w3school.com.cn/tiy/color.asp?hex=00CED1) |      |
| [DarkViolet](http://www.w3school.com.cn/tiy/color.asp?color=DarkViolet) | [#9400D3](http://www.w3school.com.cn/tiy/color.asp?hex=9400D3) |      |
| [DeepPink](http://www.w3school.com.cn/tiy/color.asp?color=DeepPink) | [#FF1493](http://www.w3school.com.cn/tiy/color.asp?hex=FF1493) |      |
| [DeepSkyBlue](http://www.w3school.com.cn/tiy/color.asp?color=DeepSkyBlue) | [#00BFFF](http://www.w3school.com.cn/tiy/color.asp?hex=00BFFF) |      |
| [DimGray](http://www.w3school.com.cn/tiy/color.asp?color=DimGray) | [#696969](http://www.w3school.com.cn/tiy/color.asp?hex=696969) |      |
| [DodgerBlue](http://www.w3school.com.cn/tiy/color.asp?color=DodgerBlue) | [#1E90FF](http://www.w3school.com.cn/tiy/color.asp?hex=1E90FF) |      |
| [Feldspar](http://www.w3school.com.cn/tiy/color.asp?color=Feldspar) | [#D19275](http://www.w3school.com.cn/tiy/color.asp?hex=D19275) |      |
| [FireBrick](http://www.w3school.com.cn/tiy/color.asp?color=FireBrick) | [#B22222](http://www.w3school.com.cn/tiy/color.asp?hex=B22222) |      |
| [FloralWhite](http://www.w3school.com.cn/tiy/color.asp?color=FloralWhite) | [#FFFAF0](http://www.w3school.com.cn/tiy/color.asp?hex=FFFAF0) |      |
| [ForestGreen](http://www.w3school.com.cn/tiy/color.asp?color=ForestGreen) | [#228B22](http://www.w3school.com.cn/tiy/color.asp?hex=228B22) |      |
| [Fuchsia](http://www.w3school.com.cn/tiy/color.asp?color=Fuchsia) | [#FF00FF](http://www.w3school.com.cn/tiy/color.asp?hex=FF00FF) |      |
| [Gainsboro](http://www.w3school.com.cn/tiy/color.asp?color=Gainsboro) | [#DCDCDC](http://www.w3school.com.cn/tiy/color.asp?hex=DCDCDC) |      |
| [GhostWhite](http://www.w3school.com.cn/tiy/color.asp?color=GhostWhite) | [#F8F8FF](http://www.w3school.com.cn/tiy/color.asp?hex=F8F8FF) |      |
| [Gold](http://www.w3school.com.cn/tiy/color.asp?color=Gold)  | [#FFD700](http://www.w3school.com.cn/tiy/color.asp?hex=FFD700) |      |
| [GoldenRod](http://www.w3school.com.cn/tiy/color.asp?color=GoldenRod) | [#DAA520](http://www.w3school.com.cn/tiy/color.asp?hex=DAA520) |      |
| [Gray](http://www.w3school.com.cn/tiy/color.asp?color=Gray)  | [#808080](http://www.w3school.com.cn/tiy/color.asp?hex=808080) |      |
| [Green](http://www.w3school.com.cn/tiy/color.asp?color=Green) | [#008000](http://www.w3school.com.cn/tiy/color.asp?hex=008000) |      |
| [GreenYellow](http://www.w3school.com.cn/tiy/color.asp?color=GreenYellow) | [#ADFF2F](http://www.w3school.com.cn/tiy/color.asp?hex=ADFF2F) |      |
| [HoneyDew](http://www.w3school.com.cn/tiy/color.asp?color=HoneyDew) | [#F0FFF0](http://www.w3school.com.cn/tiy/color.asp?hex=F0FFF0) |      |
| [HotPink](http://www.w3school.com.cn/tiy/color.asp?color=HotPink) | [#FF69B4](http://www.w3school.com.cn/tiy/color.asp?hex=FF69B4) |      |
| [IndianRed](http://www.w3school.com.cn/tiy/color.asp?color=IndianRed) | [#CD5C5C](http://www.w3school.com.cn/tiy/color.asp?hex=CD5C5C) |      |
| [Indigo](http://www.w3school.com.cn/tiy/color.asp?color=Indigo) | [#4B0082](http://www.w3school.com.cn/tiy/color.asp?hex=4B0082) |      |
| [Ivory](http://www.w3school.com.cn/tiy/color.asp?color=Ivory) | [#FFFFF0](http://www.w3school.com.cn/tiy/color.asp?hex=FFFFF0) |      |
| [Khaki](http://www.w3school.com.cn/tiy/color.asp?color=Khaki) | [#F0E68C](http://www.w3school.com.cn/tiy/color.asp?hex=F0E68C) |      |
| [Lavender](http://www.w3school.com.cn/tiy/color.asp?color=Lavender) | [#E6E6FA](http://www.w3school.com.cn/tiy/color.asp?hex=E6E6FA) |      |
| [LavenderBlush](http://www.w3school.com.cn/tiy/color.asp?color=LavenderBlush) | [#FFF0F5](http://www.w3school.com.cn/tiy/color.asp?hex=FFF0F5) |      |
| [LawnGreen](http://www.w3school.com.cn/tiy/color.asp?color=LawnGreen) | [#7CFC00](http://www.w3school.com.cn/tiy/color.asp?hex=7CFC00) |      |
| [LemonChiffon](http://www.w3school.com.cn/tiy/color.asp?color=LemonChiffon) | [#FFFACD](http://www.w3school.com.cn/tiy/color.asp?hex=FFFACD) |      |
| [LightBlue](http://www.w3school.com.cn/tiy/color.asp?color=LightBlue) | [#ADD8E6](http://www.w3school.com.cn/tiy/color.asp?hex=ADD8E6) |      |
| [LightCoral](http://www.w3school.com.cn/tiy/color.asp?color=LightCoral) | [#F08080](http://www.w3school.com.cn/tiy/color.asp?hex=F08080) |      |
| [LightCyan](http://www.w3school.com.cn/tiy/color.asp?color=LightCyan) | [#E0FFFF](http://www.w3school.com.cn/tiy/color.asp?hex=E0FFFF) |      |
| [LightGoldenRodYellow](http://www.w3school.com.cn/tiy/color.asp?color=LightGoldenRodYellow) | [#FAFAD2](http://www.w3school.com.cn/tiy/color.asp?hex=FAFAD2) |      |
| [LightGrey](http://www.w3school.com.cn/tiy/color.asp?color=LightGrey) | [#D3D3D3](http://www.w3school.com.cn/tiy/color.asp?hex=D3D3D3) |      |
| [LightGreen](http://www.w3school.com.cn/tiy/color.asp?color=LightGreen) | [#90EE90](http://www.w3school.com.cn/tiy/color.asp?hex=90EE90) |      |
| [LightPink](http://www.w3school.com.cn/tiy/color.asp?color=LightPink) | [#FFB6C1](http://www.w3school.com.cn/tiy/color.asp?hex=FFB6C1) |      |
| [LightSalmon](http://www.w3school.com.cn/tiy/color.asp?color=LightSalmon) | [#FFA07A](http://www.w3school.com.cn/tiy/color.asp?hex=FFA07A) |      |
| [LightSeaGreen](http://www.w3school.com.cn/tiy/color.asp?color=LightSeaGreen) | [#20B2AA](http://www.w3school.com.cn/tiy/color.asp?hex=20B2AA) |      |
| [LightSkyBlue](http://www.w3school.com.cn/tiy/color.asp?color=LightSkyBlue) | [#87CEFA](http://www.w3school.com.cn/tiy/color.asp?hex=87CEFA) |      |
| [LightSlateBlue](http://www.w3school.com.cn/tiy/color.asp?color=LightSlateBlue) | [#8470FF](http://www.w3school.com.cn/tiy/color.asp?hex=8470FF) |      |
| [LightSlateGray](http://www.w3school.com.cn/tiy/color.asp?color=LightSlateGray) | [#778899](http://www.w3school.com.cn/tiy/color.asp?hex=778899) |      |
| [LightSteelBlue](http://www.w3school.com.cn/tiy/color.asp?color=LightSteelBlue) | [#B0C4DE](http://www.w3school.com.cn/tiy/color.asp?hex=B0C4DE) |      |
| [LightYellow](http://www.w3school.com.cn/tiy/color.asp?color=LightYellow) | [#FFFFE0](http://www.w3school.com.cn/tiy/color.asp?hex=FFFFE0) |      |
| [Lime](http://www.w3school.com.cn/tiy/color.asp?color=Lime)  | [#00FF00](http://www.w3school.com.cn/tiy/color.asp?hex=00FF00) |      |
| [LimeGreen](http://www.w3school.com.cn/tiy/color.asp?color=LimeGreen) | [#32CD32](http://www.w3school.com.cn/tiy/color.asp?hex=32CD32) |      |
| [Linen](http://www.w3school.com.cn/tiy/color.asp?color=Linen) | [#FAF0E6](http://www.w3school.com.cn/tiy/color.asp?hex=FAF0E6) |      |
| [Magenta](http://www.w3school.com.cn/tiy/color.asp?color=Magenta) | [#FF00FF](http://www.w3school.com.cn/tiy/color.asp?hex=FF00FF) |      |
| [Maroon](http://www.w3school.com.cn/tiy/color.asp?color=Maroon) | [#800000](http://www.w3school.com.cn/tiy/color.asp?hex=800000) |      |
| [MediumAquaMarine](http://www.w3school.com.cn/tiy/color.asp?color=MediumAquaMarine) | [#66CDAA](http://www.w3school.com.cn/tiy/color.asp?hex=66CDAA) |      |
| [MediumBlue](http://www.w3school.com.cn/tiy/color.asp?color=MediumBlue) | [#0000CD](http://www.w3school.com.cn/tiy/color.asp?hex=0000CD) |      |
| [MediumOrchid](http://www.w3school.com.cn/tiy/color.asp?color=MediumOrchid) | [#BA55D3](http://www.w3school.com.cn/tiy/color.asp?hex=BA55D3) |      |
| [MediumPurple](http://www.w3school.com.cn/tiy/color.asp?color=MediumPurple) | [#9370D8](http://www.w3school.com.cn/tiy/color.asp?hex=9370D8) |      |
| [MediumSeaGreen](http://www.w3school.com.cn/tiy/color.asp?color=MediumSeaGreen) | [#3CB371](http://www.w3school.com.cn/tiy/color.asp?hex=3CB371) |      |
| [MediumSlateBlue](http://www.w3school.com.cn/tiy/color.asp?color=MediumSlateBlue) | [#7B68EE](http://www.w3school.com.cn/tiy/color.asp?hex=7B68EE) |      |
| [MediumSpringGreen](http://www.w3school.com.cn/tiy/color.asp?color=MediumSpringGreen) | [#00FA9A](http://www.w3school.com.cn/tiy/color.asp?hex=00FA9A) |      |
| [MediumTurquoise](http://www.w3school.com.cn/tiy/color.asp?color=MediumTurquoise) | [#48D1CC](http://www.w3school.com.cn/tiy/color.asp?hex=48D1CC) |      |
| [MediumVioletRed](http://www.w3school.com.cn/tiy/color.asp?color=MediumVioletRed) | [#C71585](http://www.w3school.com.cn/tiy/color.asp?hex=C71585) |      |
| [MidnightBlue](http://www.w3school.com.cn/tiy/color.asp?color=MidnightBlue) | [#191970](http://www.w3school.com.cn/tiy/color.asp?hex=191970) |      |
| [MintCream](http://www.w3school.com.cn/tiy/color.asp?color=MintCream) | [#F5FFFA](http://www.w3school.com.cn/tiy/color.asp?hex=F5FFFA) |      |
| [MistyRose](http://www.w3school.com.cn/tiy/color.asp?color=MistyRose) | [#FFE4E1](http://www.w3school.com.cn/tiy/color.asp?hex=FFE4E1) |      |
| [Moccasin](http://www.w3school.com.cn/tiy/color.asp?color=Moccasin) | [#FFE4B5](http://www.w3school.com.cn/tiy/color.asp?hex=FFE4B5) |      |
| [NavajoWhite](http://www.w3school.com.cn/tiy/color.asp?color=NavajoWhite) | [#FFDEAD](http://www.w3school.com.cn/tiy/color.asp?hex=FFDEAD) |      |
| [Navy](http://www.w3school.com.cn/tiy/color.asp?color=Navy)  | [#000080](http://www.w3school.com.cn/tiy/color.asp?hex=000080) |      |
| [OldLace](http://www.w3school.com.cn/tiy/color.asp?color=OldLace) | [#FDF5E6](http://www.w3school.com.cn/tiy/color.asp?hex=FDF5E6) |      |
| [Olive](http://www.w3school.com.cn/tiy/color.asp?color=Olive) | [#808000](http://www.w3school.com.cn/tiy/color.asp?hex=808000) |      |
| [OliveDrab](http://www.w3school.com.cn/tiy/color.asp?color=OliveDrab) | [#6B8E23](http://www.w3school.com.cn/tiy/color.asp?hex=6B8E23) |      |
| [Orange](http://www.w3school.com.cn/tiy/color.asp?color=Orange) | [#FFA500](http://www.w3school.com.cn/tiy/color.asp?hex=FFA500) |      |
| [OrangeRed](http://www.w3school.com.cn/tiy/color.asp?color=OrangeRed) | [#FF4500](http://www.w3school.com.cn/tiy/color.asp?hex=FF4500) |      |
| [Orchid](http://www.w3school.com.cn/tiy/color.asp?color=Orchid) | [#DA70D6](http://www.w3school.com.cn/tiy/color.asp?hex=DA70D6) |      |
| [PaleGoldenRod](http://www.w3school.com.cn/tiy/color.asp?color=PaleGoldenRod) | [#EEE8AA](http://www.w3school.com.cn/tiy/color.asp?hex=EEE8AA) |      |
| [PaleGreen](http://www.w3school.com.cn/tiy/color.asp?color=PaleGreen) | [#98FB98](http://www.w3school.com.cn/tiy/color.asp?hex=98FB98) |      |
| [PaleTurquoise](http://www.w3school.com.cn/tiy/color.asp?color=PaleTurquoise) | [#AFEEEE](http://www.w3school.com.cn/tiy/color.asp?hex=AFEEEE) |      |
| [PaleVioletRed](http://www.w3school.com.cn/tiy/color.asp?color=PaleVioletRed) | [#D87093](http://www.w3school.com.cn/tiy/color.asp?hex=D87093) |      |
| [PapayaWhip](http://www.w3school.com.cn/tiy/color.asp?color=PapayaWhip) | [#FFEFD5](http://www.w3school.com.cn/tiy/color.asp?hex=FFEFD5) |      |
| [PeachPuff](http://www.w3school.com.cn/tiy/color.asp?color=PeachPuff) | [#FFDAB9](http://www.w3school.com.cn/tiy/color.asp?hex=FFDAB9) |      |
| [Peru](http://www.w3school.com.cn/tiy/color.asp?color=Peru)  | [#CD853F](http://www.w3school.com.cn/tiy/color.asp?hex=CD853F) |      |
| [Pink](http://www.w3school.com.cn/tiy/color.asp?color=Pink)  | [#FFC0CB](http://www.w3school.com.cn/tiy/color.asp?hex=FFC0CB) |      |
| [Plum](http://www.w3school.com.cn/tiy/color.asp?color=Plum)  | [#DDA0DD](http://www.w3school.com.cn/tiy/color.asp?hex=DDA0DD) |      |
| [PowderBlue](http://www.w3school.com.cn/tiy/color.asp?color=PowderBlue) | [#B0E0E6](http://www.w3school.com.cn/tiy/color.asp?hex=B0E0E6) |      |
| [Purple](http://www.w3school.com.cn/tiy/color.asp?color=Purple) | [#800080](http://www.w3school.com.cn/tiy/color.asp?hex=800080) |      |
| [Red](http://www.w3school.com.cn/tiy/color.asp?color=Red)    | [#FF0000](http://www.w3school.com.cn/tiy/color.asp?hex=FF0000) |      |
| [RosyBrown](http://www.w3school.com.cn/tiy/color.asp?color=RosyBrown) | [#BC8F8F](http://www.w3school.com.cn/tiy/color.asp?hex=BC8F8F) |      |
| [RoyalBlue](http://www.w3school.com.cn/tiy/color.asp?color=RoyalBlue) | [#4169E1](http://www.w3school.com.cn/tiy/color.asp?hex=4169E1) |      |
| [SaddleBrown](http://www.w3school.com.cn/tiy/color.asp?color=SaddleBrown) | [#8B4513](http://www.w3school.com.cn/tiy/color.asp?hex=8B4513) |      |
| [Salmon](http://www.w3school.com.cn/tiy/color.asp?color=Salmon) | [#FA8072](http://www.w3school.com.cn/tiy/color.asp?hex=FA8072) |      |
| [SandyBrown](http://www.w3school.com.cn/tiy/color.asp?color=SandyBrown) | [#F4A460](http://www.w3school.com.cn/tiy/color.asp?hex=F4A460) |      |
| [SeaGreen](http://www.w3school.com.cn/tiy/color.asp?color=SeaGreen) | [#2E8B57](http://www.w3school.com.cn/tiy/color.asp?hex=2E8B57) |      |
| [SeaShell](http://www.w3school.com.cn/tiy/color.asp?color=SeaShell) | [#FFF5EE](http://www.w3school.com.cn/tiy/color.asp?hex=FFF5EE) |      |
| [Sienna](http://www.w3school.com.cn/tiy/color.asp?color=Sienna) | [#A0522D](http://www.w3school.com.cn/tiy/color.asp?hex=A0522D) |      |
| [Silver](http://www.w3school.com.cn/tiy/color.asp?color=Silver) | [#C0C0C0](http://www.w3school.com.cn/tiy/color.asp?hex=C0C0C0) |      |
| [SkyBlue](http://www.w3school.com.cn/tiy/color.asp?color=SkyBlue) | [#87CEEB](http://www.w3school.com.cn/tiy/color.asp?hex=87CEEB) |      |
| [SlateBlue](http://www.w3school.com.cn/tiy/color.asp?color=SlateBlue) | [#6A5ACD](http://www.w3school.com.cn/tiy/color.asp?hex=6A5ACD) |      |
| [SlateGray](http://www.w3school.com.cn/tiy/color.asp?color=SlateGray) | [#708090](http://www.w3school.com.cn/tiy/color.asp?hex=708090) |      |
| [Snow](http://www.w3school.com.cn/tiy/color.asp?color=Snow)  | [#FFFAFA](http://www.w3school.com.cn/tiy/color.asp?hex=FFFAFA) |      |
| [SpringGreen](http://www.w3school.com.cn/tiy/color.asp?color=SpringGreen) | [#00FF7F](http://www.w3school.com.cn/tiy/color.asp?hex=00FF7F) |      |
| [SteelBlue](http://www.w3school.com.cn/tiy/color.asp?color=SteelBlue) | [#4682B4](http://www.w3school.com.cn/tiy/color.asp?hex=4682B4) |      |
| [Tan](http://www.w3school.com.cn/tiy/color.asp?color=Tan)    | [#D2B48C](http://www.w3school.com.cn/tiy/color.asp?hex=D2B48C) |      |
| [Teal](http://www.w3school.com.cn/tiy/color.asp?color=Teal)  | [#008080](http://www.w3school.com.cn/tiy/color.asp?hex=008080) |      |
| [Thistle](http://www.w3school.com.cn/tiy/color.asp?color=Thistle) | [#D8BFD8](http://www.w3school.com.cn/tiy/color.asp?hex=D8BFD8) |      |
| [Tomato](http://www.w3school.com.cn/tiy/color.asp?color=Tomato) | [#FF6347](http://www.w3school.com.cn/tiy/color.asp?hex=FF6347) |      |
| [Turquoise](http://www.w3school.com.cn/tiy/color.asp?color=Turquoise) | [#40E0D0](http://www.w3school.com.cn/tiy/color.asp?hex=40E0D0) |      |
| [Violet](http://www.w3school.com.cn/tiy/color.asp?color=Violet) | [#EE82EE](http://www.w3school.com.cn/tiy/color.asp?hex=EE82EE) |      |
| [VioletRed](http://www.w3school.com.cn/tiy/color.asp?color=VioletRed) | [#D02090](http://www.w3school.com.cn/tiy/color.asp?hex=D02090) |      |
| [Wheat](http://www.w3school.com.cn/tiy/color.asp?color=Wheat) | [#F5DEB3](http://www.w3school.com.cn/tiy/color.asp?hex=F5DEB3) |      |
| [White](http://www.w3school.com.cn/tiy/color.asp?color=White) | [#FFFFFF](http://www.w3school.com.cn/tiy/color.asp?hex=FFFFFF) |      |
| [WhiteSmoke](http://www.w3school.com.cn/tiy/color.asp?color=WhiteSmoke) | [#F5F5F5](http://www.w3school.com.cn/tiy/color.asp?hex=F5F5F5) |      |
| [Yellow](http://www.w3school.com.cn/tiy/color.asp?color=Yellow) | [#FFFF00](http://www.w3school.com.cn/tiy/color.asp?hex=FFFF00) |      |
| [YellowGreen](http://www.w3school.com.cn/tiy/color.asp?color=YellowGreen) | [#9ACD32](http://www.w3school.com.cn/tiy/color.asp?hex=9ACD32) |      |

## HTML &lt;!DOCTYPE>

**<!DOCTYPE> 声明帮助浏览器正确地显示网页。**

### &lt;!DOCTYPE> 声明

Web 世界中存在许多不同的文档。只有了解文档的类型，浏览器才能正确地显示文档。

HTML 也有多个不同的版本，只有完全明白页面中使用的确切 HTML 版本，浏览器才能完全正确地显示出 HTML 页面。这就是 <!DOCTYPE> 的用处。

<!DOCTYPE> 不是 HTML 标签。它为浏览器提供一项信息（声明），即 HTML 是用什么版本编写的。

提示：W3School 即将升级为最新的 HTML5 文档类型。

**实例**

带有 HTML5 DOCTYPE 的 HTML 文档：

```
<!DOCTYPE html>
<html>
<head>
<title>Title of the document</title>
</head>

<body>
The content of the document......
</body>

</html>
```

### HTML 版本

从 Web 诞生早期至今，已经发展出多个 HTML 版本：

| 版本      | 年份 |
| --------- | ---- |
| HTML      | 1991 |
| HTML+     | 1993 |
| HTML 2.0  | 1995 |
| HTML 3.2  | 1997 |
| HTML 4.01 | 1999 |
| XHTML 1.0 | 2000 |
| HTML5     | 2012 |
| XHTML5    | 2013 |

### 常用的声明

**HTML5**

```
<!DOCTYPE html>
```

**HTML 4.01**

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN"
"http://www.w3.org/TR/html4/loose.dtd">
```

**XHTML 1.0**

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
```

如需完整的文档类型声明列表，请访问我们的 [DOCTYPE 参考手册](http://www.w3school.com.cn/tags/tag_doctype.asp)。

# XHTML

## XHTML 简介

- [HTML 速查手册](http://www.w3school.com.cn/html/html_quick.asp)
- [XHTML 元素](http://www.w3school.com.cn/html/html_xhtml_elements.asp)

**XHTML 是以 XML 格式编写的 HTML。**

### 什么是 XHTML？

- XHTML 指的是可扩展超文本标记语言
- XHTML 与 HTML 4.01 几乎是相同的
- XHTML 是更严格更纯净的 HTML 版本
- XHTML 是以 XML 应用的方式定义的 HTML
- XHTML 是 [2001 年 1 月](http://www.w3school.com.cn/w3c/w3c_xhtml.asp)发布的 W3C 推荐标准
- XHTML 得到所有主流浏览器的支持

### 为什么使用 XHTML？

因特网上的很多页面包含了“糟糕”的 HTML。

如果在浏览器中查看，下面的 HTML 代码运行起来非常正常（即使它并未遵守 HTML 规则）：

```
<html>
<head>
<title>This is bad HTML</title>
<body>
<h1>Bad HTML
<p>This is a paragraph
</body>
```

XML 是一种必须正确标记且格式良好的标记语言。

如果希望学习 XML，请阅读我们的 [XML 教程](http://www.w3school.com.cn/xml/index.asp)。

今日的科技界存在一些不同的浏览器技术。其中一些在计算机上运行，而另一些可能在移动电话或其他小型设备上运行。小型设备往往缺乏解释“糟糕”的标记语言的资源和能力。

所以 - 通过结合 XML 和 HTML 的长处，开发出了 XHTML。XHTML 是作为 XML 被重新设计的 HTML。

与 HTML 相比最重要的区别：

### 文档结构

- XHTML DOCTYPE 是*强制性的*
- <html> 中的 XML namespace 属性是*强制性的*
- <html>、<head>、<title> 以及 <body> 也是*强制性的*

### 元素语法

- XHTML 元素必须*正确嵌套*
- XHTML 元素必须始终*关闭*
- XHTML 元素必须*小写*
- XHTML 文档必须有*一个根元素*

### 属性语法

- XHTML 属性必须使用*小写*
- XHTML 属性值必须用*引号包围*
- XHTML 属性最小化也是*禁止的*

### &lt;!DOCTYPE ....> 是强制性的

XHTML 文档必须进行 XHTML 文档类型声明（XHTML DOCTYPE declaration）。

您可以在 W3School 的标签参考手册中找到完整的 [XHTML 文档类型](http://www.w3school.com.cn/tags/tag_doctype.asp)。

<html>、<head>、<title> 以及 <body> 元素也必须存在，并且必须使用 <html> 中的 xmlns 属性为文档规定 xml 命名空间。

下面的例子展示了带有最少的必需标签的 XHTML 文档：

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">

<html xmlns="http://www.w3.org/1999/xhtml">

<head>
<title>Title of document</title>
</head>

<body>
......
</body>

</html>
```

### 如何从 HTML 转换到 XHTML

1. 向每张页面的第一行添加 XHTML <!DOCTYPE>
2. 向每张页面的 html 元素添加 xmlns 属性
3. 把所有元素名改为小写
4. 关闭所有空元素
5. 把所有属性名改为小写
6. 为所有属性值加引号

### 用 W3C 验证器检验 XHTML

在下面的文本框中输入您的网址：





### XHTML 测验

该测验包含 20 道问题，且没有时间限制。

本测验是非正式的，它仅仅是了解您 XHTML 知识掌握程度的一个不错的途径。

每项正确答案可获得 1 分。在测试结束后，会显示您的总分。最高分为 20 分。

[开始 XHTML 测验](http://www.w3school.com.cn/xhtml/xhtml_quiz.asp)

## XHTML - 元素

**XHTML 元素是以 XML 格式编写的 HTML 元素。**

### XHTML 元素 - 语法规则

- XHTML 元素必须*正确嵌套*
- XHTML 元素必须始终*关闭*
- XHTML 元素必须*小写*
- XHTML 文档必须有*一个根元素*

### XHTML 元素必须正确嵌套

在 HTML 中，某些元素可以不正确地彼此嵌套在一起，就像这样：

```
<b><i>This text is bold and italic</b></i>
```

在 XHTML 中，所有元素必须正确地彼此嵌套，就像这样：

```
<b><i>This text is bold and italic</i></b>
```

### XHTML 元素必须始终关闭

这是错误的：

```
<p>This is a paragraph
<p>This is another paragraph
```

这是正确的：

```
<p>This is a paragraph</p>
<p>This is another paragraph</p>
```

### 空元素也必须关闭

这是错误的：

```
A break: <br>
A horizontal rule: <hr>
An image: <img src="happy.gif" alt="Happy face">
```

这是正确的：

```
A break: <br />
A horizontal rule: <hr />
An image: <img src="happy.gif" alt="Happy face" />
```

### XHTML 元素必须小写

这是错误的：

```
<BODY>
<P>This is a paragraph</P>
</BODY>
```

这是正确的：

```
<body>
<p>This is a paragraph</p>
</body>
```

## XHTML - 属性

**XHTML 属性是以 XML 格式编写的 HTML 属性。**

### XHTML 属性 - 语法规则

- XHTML 属性必须使用*小写*
- XHTML 属性值必须用*引号包围*
- XHTML 属性最小化也是*禁止的*

### XHTML 属性必须使用小写

这是错误的：

```
<table WIDTH="100%">
```

这是正确的：

```
<table width="100%">
```

### XHTML 属性值必须用引号包围

这是错误的：

```
<table width=100%>
```

这是正确的：

```
<table width="100%">
```

### 禁止属性简写

这是错误的：

```
<input checked>
<input readonly>
<input disabled>
<option selected>
```

这是正确的：

```
<input checked="checked" />
<input readonly="readonly" />
<input disabled="disabled" />
<option selected="selected" />
```

# HTML 表单

## HTML 表单

**HTML 表单用于搜集不同类型的用户输入。**

### &lt;form> 元素

HTML 表单用于收集用户输入。

<form> 元素定义 HTML 表单：

**实例**

```
<form>
 .
form elements
 .
</form>
```

### HTML 表单包含*表单元素*。

表单元素指的是不同类型的 input 元素、复选框、单选按钮、提交按钮等等。

### &lt;input> 元素

*<input>* 元素是最重要的*表单元素*。

<input> 元素有很多形态，根据不同的 *type* 属性。

这是本章中使用的类型：

| 类型   | 描述                                 |
| ------ | ------------------------------------ |
| text   | 定义常规文本输入。                   |
| radio  | 定义单选按钮输入（选择多个选择之一） |
| submit | 定义提交按钮（提交表单）             |

注释：您稍后将在本教程学到更多有关输入类型的知识。

### 文本输入

*<input type="text">* 定义用于*文本输入*的单行输入字段：

**实例**

```
<form>
 First name:<br>
<input type="text" name="firstname">
<br>
 Last name:<br>
<input type="text" name="lastname">
</form> 
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_form_text)

在浏览器中看起来是这样的：

First name:


Last name:

注释：表单本身并不可见。还要注意文本字段的默认宽度是 20 个字符。

### 单选按钮输入

*<input type="radio">* 定义*单选按钮*。

单选按钮允许用户在有限数量的选项中选择其中之一：

**实例**

```
<form>
<input type="radio" name="sex" value="male" checked>Male
<br>
<input type="radio" name="sex" value="female">Female
</form> 
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_form_radio)

单选按钮在浏览器看起来是这样的：

Male 

Female

### 提交按钮

*<input type="submit">* 定义用于向*表单处理程序*（form-handler）*提交*表单的按钮。

表单处理程序通常是包含用来处理输入数据的脚本的服务器页面。

表单处理程序在表单的 *action* 属性中指定：

**实例**

```
<form action="action_page.php">
First name:<br>
<input type="text" name="firstname" value="Mickey">
<br>
Last name:<br>
<input type="text" name="lastname" value="Mouse">
<br><br>
<input type="submit" value="Submit">
</form> 
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_form_submit)

在浏览器中看起来是这样的：

First name:


Last name:




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

### 何时使用 GET？

您能够使用 GET（默认方法）：

如果表单提交是被动的（比如搜索引擎查询），并且没有敏感信息。

当您使用 GET 时，表单数据在页面地址栏中是可见的：

```
action_page.php?firstname=Mickey&lastname=Mouse
```

注释：GET 最适合少量数据的提交。浏览器会设定容量限制。

### 何时使用 POST？

您应该使用 POST：

如果表单正在更新数据，或者包含敏感信息（例如密码）。

POST 的安全性更加，因为在页面地址栏中被提交的数据是不可见的。

### Name 属性

如果要正确地被提交，每个输入字段必须设置一个 name 属性。

本例只会提交 "Last name" 输入字段：

**实例**

```
<form action="action_page.php">
First name:<br>
<input type="text" value="Mickey">
<br>
Last name:<br>
<input type="text" name="lastname" value="Mouse">
<br><br>
<input type="submit" value="Submit">
</form> 
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_form_submit_id)

### 用 &lt;fieldset> 组合表单数据

*<fieldset>* 元素组合表单中的相关数据

*<legend>* 元素为 <fieldset> 元素定义标题。

**实例**

```
<form action="action_page.php">
<fieldset>
<legend>Personal information:</legend>
First name:<br>
<input type="text" name="firstname" value="Mickey">
<br>
Last name:<br>
<input type="text" name="lastname" value="Mouse">
<br><br>
<input type="submit" value="Submit"></fieldset>
</form> 
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_form_legend)

以上 HTML 代码在浏览器中看起来是这样的：

Personal information:
First name:


Last name:




### HTML Form 属性

HTML <form> 元素，已设置所有可能的属性，是这样的：

**实例**

```
<form action="action_page.php" method="GET" target="_blank" accept-charset="UTF-8"
ectype="application/x-www-form-urlencoded" autocomplete="off" novalidate>
.
form elements
 .
</form> 
```

下面是 <form> 属性的列表：

| 属性           | 描述                                                       |
| -------------- | ---------------------------------------------------------- |
| accept-charset | 规定在被提交表单中使用的字符集（默认：页面字符集）。       |
| action         | 规定向何处提交表单的地址（URL）（提交页面）。              |
| autocomplete   | 规定浏览器应该自动完成表单（默认：开启）。                 |
| enctype        | 规定被提交数据的编码（默认：url-encoded）。                |
| method         | 规定在提交表单时所用的 HTTP 方法（默认：GET）。            |
| name           | 规定识别表单的名称（对于 DOM 使用：document.forms.name）。 |
| novalidate     | 规定浏览器不验证表单。                                     |
| target         | 规定 action 属性中地址的目标（默认：_self）。              |

注释：您将在下面的章节学到更多关于属性的知识。

## HTML 输入类型

**本章描述 <input> 元素的输入类型。**

### 输入类型：text

*<input type="text">* 定义供*文本输入*的单行输入字段：

**实例**

```
<form>
 First name:<br>
<input type="text" name="firstname">
<br>
 Last name:<br>
<input type="text" name="lastname">
</form> 
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_text)

以上 HTML 代码在浏览器中看上去是这样的：

First name:


Last name:

### 输入类型：password

*<input type="password">* 定义*密码字段*：

**实例**

```
<form>
 User name:<br>
<input type="text" name="username">
<br>
 User password:<br>
<input type="password" name="psw">
</form> 
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_password)

以上 HTML 代码在浏览器中看上去是这样的：

User name:


User password:

注释：password 字段中的字符会被做掩码处理（显示为星号或实心圆）。

### 输入类型：submit

*<input type="submit">* 定义*提交*表单数据至*表单处理程序*的按钮。

表单处理程序（form-handler）通常是包含处理输入数据的脚本的服务器页面。

在表单的 action 属性中规定表单处理程序（form-handler）：

**实例**

```
<form action="action_page.php">
First name:<br>
<input type="text" name="firstname" value="Mickey">
<br>
Last name:<br>
<input type="text" name="lastname" value="Mouse">
<br><br>
<input type="submit" value="Submit">
</form> 
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_submit)

以上 HTML 代码在浏览器中看上去是这样的：

First name:


Last name:




如果您省略了提交按钮的 value 属性，那么该按钮将获得默认文本：

**实例**

```
<form action="action_page.php">
First name:<br>
<input type="text" name="firstname" value="Mickey">
<br>
Last name:<br>
<input type="text" name="lastname" value="Mouse">
<br><br>
<input type="submit">
</form> 
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_submit_nn)

### Input Type: radio

<input type="radio"> 定义单选按钮。

Radio buttons let a user select ONLY ONE of a limited number of choices:

**实例**

```
<form>
<input type="radio" name="sex" value="male" checked>Male
<br>
<input type="radio" name="sex" value="female">Female
</form> 
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_radio)

以上 HTML 代码在浏览器中看上去是这样的：

Male 

Female

### Input Type: checkbox

<input type="checkbox"> 定义复选框。

复选框允许用户在有限数量的选项中选择零个或多个选项。

**实例**

```
<form>
<input type="checkbox" name="vehicle" value="Bike">I have a bike
<br>
<input type="checkbox" name="vehicle" value="Car">I have a car 
</form> 
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_checkbox)

以上 HTML 代码在浏览器中看上去是这样的：

I have a bike 

I have a car

### Input Type: button

*<input type="button>* 定义*按钮*。

**实例**

```
<input type="button" onclick="alert('Hello World!')" value="Click Me!">
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_button)

以上 HTML 代码在浏览器中看上去是这样的：

### HTML5 输入类型

HTML5 增加了多个新的输入类型：

- color
- date
- datetime
- datetime-local
- email
- month
- number
- range
- search
- tel
- time
- url
- week

注释：老式 web 浏览器不支持的输入类型，会被视为输入类型 text。

### 输入类型：number

*<input type="number">* 用于应该包含数字值的输入字段。

您能够对数字做出限制。

根据浏览器支持，限制可应用到输入字段。

**实例**

```
<form>
  Quantity (between 1 and 5):
  <input type="number" name="quantity" min="1" max="5">
</form>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_number)

### 输入限制

这里列出了一些常用的输入限制（其中一些是 HTML5 中新增的）：

| 属性      | 描述                               |
| --------- | ---------------------------------- |
| disabled  | 规定输入字段应该被禁用。           |
| max       | 规定输入字段的最大值。             |
| maxlength | 规定输入字段的最大字符数。         |
| min       | 规定输入字段的最小值。             |
| pattern   | 规定通过其检查输入值的正则表达式。 |
| readonly  | 规定输入字段为只读（无法修改）。   |
| required  | 规定输入字段是必需的（必需填写）。 |
| size      | 规定输入字段的宽度（以字符计）。   |
| step      | 规定输入字段的合法数字间隔。       |
| value     | 规定输入字段的默认值。             |

您将在下一章学到更多有关输入限制的知识。

**实例**

```
<form>
  Quantity:
  <input type="number" name="points" min="0" max="100" step="10" value="30">
</form>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_number_step)

### 输入类型：date

*<input type="date">* 用于应该包含日期的输入字段。

根据浏览器支持，日期选择器会出现输入字段中。

**实例**

```
<form>
  Birthday:
  <input type="date" name="bday">
</form>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_date)

您可以向输入添加限制：

**实例**

```
<form>
  Enter a date before 1980-01-01:
  <input type="date" name="bday" max="1979-12-31"><br>
  Enter a date after 2000-01-01:
  <input type="date" name="bday" min="2000-01-02"><br>
</form>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_date_max_min)

### 输入类型：color

*<input type="color">* 用于应该包含颜色的输入字段。

根据浏览器支持，颜色选择器会出现输入字段中。

**实例**

```
<form>
  Select your favorite color:
  <input type="color" name="favcolor">
</form>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_color)

### 输入类型：range

*<input type="range">* 用于应该包含一定范围内的值的输入字段。

根据浏览器支持，输入字段能够显示为滑块控件。

**实例**

```
<form>
  <input type="range" name="points" min="0" max="10">
</form>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_range)

您能够使用如下属性来规定限制：min、max、step、value。

### 输入类型：month

*<input type="month">* 允许用户选择月份和年份。

根据浏览器支持，日期选择器会出现输入字段中。

**实例**

```
<form>
  Birthday (month and year):
  <input type="month" name="bdaymonth">
</form>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_month)

### 输入类型：week

*<input type="week">* 允许用户选择周和年。

根据浏览器支持，日期选择器会出现输入字段中。

**实例**

```
<form>
  Select a week:
  <input type="week" name="week_year">
</form>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_week)

### 输入类型：time

*<input type="time">* 允许用户选择时间（无时区）。

根据浏览器支持，时间选择器会出现输入字段中。

**实例**

```
<form>
  Select a time:
  <input type="time" name="usr_time">
</form>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_time)

### 输入类型：datetime

*<input type="datetime">* 允许用户选择日期和时间（有时区）。

根据浏览器支持，日期选择器会出现输入字段中。

**实例**

```
<form>
  Birthday (date and time):
  <input type="datetime" name="bdaytime">
</form>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_datetime)

### 输入类型：datetime-local

*<input type="datetime-local">* 允许用户选择日期和时间（无时区）。

根据浏览器支持，日期选择器会出现输入字段中。

**实例**

```
<form>
  Birthday (date and time):
  <input type="datetime-local" name="bdaytime">
</form>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_datetime-local)

### 输入类型：email

*<input type="email">* 用于应该包含电子邮件地址的输入字段。

根据浏览器支持，能够在被提交时自动对电子邮件地址进行验证。

某些智能手机会识别 email 类型，并在键盘增加 ".com" 以匹配电子邮件输入。

**实例**

```
<form>
  E-mail:
  <input type="email" name="email">
</form>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_email)

### 输入类型：search

*<input type="search">* 用于搜索字段（搜索字段的表现类似常规文本字段）。

**实例**

```
<form>
  Search Google:
  <input type="search" name="googlesearch">
</form>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_search)

### 输入类型：tel

*<input type="tel">* 用于应该包含电话号码的输入字段。

目前只有 Safari 8 支持 tel 类型。

**实例**

```
<form>
  Telephone:
  <input type="tel" name="usrtel">
</form>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_tel)

### 输入类型：url

*<input type="url">* 用于应该包含 URL 地址的输入字段。

根据浏览器支持，在提交时能够自动验证 url 字段。

某些智能手机识别 url 类型，并向键盘添加 ".com" 以匹配 url 输入。

**实例**

```
<form>
  Add your homepage:
  <input type="url" name="homepage">
</form>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_url)

## HTML Input 属性

### value 属性

*value* 属性规定输入字段的初始值：

**实例**

```
<form action="">
 First name:<br>
<input type="text" name="firstname" value="John">
<br>
 Last name:<br>
<input type="text" name="lastname">
</form> 
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_attributes_value)

### readonly 属性

*readonly* 属性规定输入字段为只读（不能修改）：

**实例**

```
<form action="">
 First name:<br>
<input type="text" name="firstname" value="John" readonly>
<br>
 Last name:<br>
<input type="text" name="lastname">
</form> 
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_attributes_readonly)

readonly 属性不需要值。它等同于 readonly="readonly"。

### disabled 属性

*disabled* 属性规定输入字段是禁用的。

被禁用的元素是不可用和不可点击的。

被禁用的元素不会被提交。

**实例**

```
<form action="">
 First name:<br>
<input type="text" name="firstname" value="John" disabled>
<br>
 Last name:<br>
<input type="text" name="lastname">
</form> 
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_attributes_disabled)

disabled 属性不需要值。它等同于 disabled="disabled"。

### size 属性

*size* 属性规定输入字段的尺寸（以字符计）：

**实例**

```
<form action="">
 First name:<br>
<input type="text" name="firstname" value="John" size="40">
<br>
 Last name:<br>
<input type="text" name="lastname">
</form> 
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_attributes_size)

### maxlength 属性

*maxlength* 属性规定输入字段允许的最大长度：

**实例**

```
<form action="">
 First name:<br>
<input type="text" name="firstname" maxlength="10">
<br>
 Last name:<br>
<input type="text" name="lastname">
</form> 
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_attributes_maxlength)

如设置 maxlength 属性，则输入控件不会接受超过所允许数的字符。

该属性不会提供任何反馈。如果需要提醒用户，则必须编写 JavaScript 代码。

注释：输入限制并非万无一失。JavaScript 提供了很多方法来增加非法输入。如需安全地限制输入，则接受者（服务器）必须同时对限制进行检查。

### HTML5 属性

HTML5 为 <input> 增加了如下属性：

- autocomplete
- autofocus
- form
- formaction
- formenctype
- formmethod
- formnovalidate
- formtarget
- height 和 width
- list
- min 和 max
- multiple
- pattern (regexp)
- placeholder
- required
- step

并为 <form> 增加如需属性：

- autocomplete
- novalidate

### autocomplete 属性

autocomplete 属性规定表单或输入字段是否应该自动完成。

当自动完成开启，浏览器会基于用户之前的输入值自动填写值。

提示：您可以把表单的 autocomplete 设置为 on，同时把特定的输入字段设置为 off，反之亦然。

autocomplete 属性适用于 <form> 以及如下 <input> 类型：text、search、url、tel、email、password、datepickers、range 以及 color。

**实例**

自动完成开启的 HTML 表单（某个输入字段为 off）：

```
<form action="action_page.php" autocomplete="on">
   First name:<input type="text" name="fname"><br>
   Last name: <input type="text" name="lname"><br>
   E-mail: <input type="email" name="email" autocomplete="off"><br>
   <input type="submit">
</form> 
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_input_autocomplete)

提示：在某些浏览器中，您也许需要手动启用自动完成功能。

### novalidate 属性

novalidate 属性属于 <form> 属性。

如果设置，则 novalidate 规定在提交表单时不对表单数据进行验证。

**实例**

指示表单在被提交时不进行验证：

```
<form action="action_page.php" novalidate>
   E-mail: <input type="email" name="user_email">
   <input type="submit">
</form> 
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_form_novalidate)

### autofocus 属性

autofocus 属性是布尔属性。

如果设置，则规定当页面加载时 <input> 元素应该自动获得焦点。

**实例**

使 "First name" 输入字段在页面加载时自动获得焦点：

```
First name:<input type="text" name="fname" autofocus>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_input_autofocus)

### form 属性

form 属性规定 <input> 元素所属的一个或多个表单。

提示：如需引用一个以上的表单，请使用空格分隔的表单 id 列表。

**实例**

输入字段位于 HTML 表单之外（但仍属表单）：

```
<form action="action_page.php" id="form1">
   First name: <input type="text" name="fname"><br>
   <input type="submit" value="Submit">
</form>

 Last name: <input type="text" name="lname" form="form1">
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_input_form)

### formaction 属性

formaction 属性规定当提交表单时处理该输入控件的文件的 URL。

formaction 属性覆盖 <form> 元素的 action 属性。

formaction 属性适用于 type="submit" 以及 type="image"。

**实例**

拥有两个两个提交按钮并对于不同动作的 HTML 表单：

```
<form action="action_page.php">
   First name: <input type="text" name="fname"><br>
   Last name: <input type="text" name="lname"><br>
   <input type="submit" value="Submit"><br>
   <input type="submit" formaction="demo_admin.asp"
   value="Submit as admin">
</form> 
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_input_formaction)

### formenctype 属性

formenctype 属性规定当把表单数据（form-data）提交至服务器时如何对其进行编码（仅针对 method="post" 的表单）。

formenctype 属性覆盖 <form> 元素的 enctype 属性。

formenctype 属性适用于 type="submit" 以及 type="image"。

**实例**

发送默认编码以及编码为 "multipart/form-data"（第二个提交按钮）的表单数据（form-data）：

```
<form action="demo_post_enctype.asp" method="post">
   First name: <input type="text" name="fname"><br>
   <input type="submit" value="Submit">
   <input type="submit" formenctype="multipart/form-data"
   value="Submit as Multipart/form-data">
</form> 
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_input_formenctype)

### formmethod 属性

formmethod 属性定义用以向 action URL 发送表单数据（form-data）的 HTTP 方法。

formmethod 属性覆盖 <form> 元素的 method 属性。

formmethod 属性适用于 type="submit" 以及 type="image"。

**实例**

第二个提交按钮覆盖表单的 HTTP 方法：

```
<form action="action_page.php" method="get">
   First name: <input type="text" name="fname"><br>
   Last name: <input type="text" name="lname"><br>
   <input type="submit" value="Submit">
   <input type="submit" formmethod="post" formaction="demo_post.asp"
   value="Submit using POST">
</form> 
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_input_formmethod)

### formnovalidate 属性

novalidate 属性是布尔属性。

如果设置，则规定在提交表单时不对 <input> 元素进行验证。

formnovalidate 属性覆盖 <form> 元素的 novalidate 属性。

formnovalidate 属性可用于 type="submit"。

**实例**

拥有两个提交按钮的表单（验证和不验证）：

```
<form action="action_page.php">
   E-mail: <input type="email" name="userid"><br>
   <input type="submit" value="Submit"><br>
   <input type="submit" formnovalidate value="Submit without validation">
</form> 
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_input_formnovalidate)

### formtarget 属性

formtarget 属性规定的名称或关键词指示提交表单后在何处显示接收到的响应。

formtarget 属性会覆盖 <form> 元素的 target 属性。

formtarget 属性可与 type="submit" 和 type="image" 使用。

**实例**

这个表单有两个提交按钮，对应不同的目标窗口：

```
<form action="action_page.php">
   First name: <input type="text" name="fname"><br>
   Last name: <input type="text" name="lname"><br>
   <input type="submit" value="Submit as normal">
   <input type="submit" formtarget="_blank"
   value="Submit to a new window">
</form> 
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_input_formtarget)

### height 和 width 属性

height 和 width 属性规定 <input> 元素的高度和宽度。

height 和 width 属性仅用于 <input type="image">。

注释：请始终规定图像的尺寸。如果浏览器不清楚图像尺寸，则页面会在图像加载时闪烁。

**实例**

把图像定义为提交按钮，并设置 height 和 width 属性：

```
<input type="image" src="img_submit.gif" alt="Submit" width="48" height="48">
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_input_height_width)

### list 属性

list 属性引用的 <datalist> 元素中包含了 <input> 元素的预定义选项。

**实例**

使用 <datalist> 设置预定义值的 <input> 元素：

```
<input list="browsers">

<datalist id="browsers">
   <option value="Internet Explorer">
   <option value="Firefox">
   <option value="Chrome">
   <option value="Opera">
   <option value="Safari">
</datalist> 
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_datalist)

### min 和 max 属性

min 和 max 属性规定 <input> 元素的最小值和最大值。

min 和 max 属性适用于如需输入类型：number、range、date、datetime、datetime-local、month、time 以及 week。

**实例**

具有最小和最大值的 <input> 元素：

```
Enter a date before 1980-01-01:
<input type="date" name="bday" max="1979-12-31">

 Enter a date after 2000-01-01:
<input type="date" name="bday" min="2000-01-02">

 Quantity (between 1 and 5):
<input type="number" name="quantity" min="1" max="5">
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_input_max_min)

### multiple 属性

multiple 属性是布尔属性。

如果设置，则规定允许用户在 <input> 元素中输入一个以上的值。

multiple 属性适用于以下输入类型：email 和 file。

**实例**

接受多个值的文件上传字段：

```
Select images: <input type="file" name="img" multiple>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_input_multiple)

### pattern 属性

pattern 属性规定用于检查 <input> 元素值的正则表达式。

pattern 属性适用于以下输入类型：text、search、url、tel、email、and password。

提示：请使用全局的 title 属性对模式进行描述以帮助用户。

提示：请在我们的 JavaScript 教程中学习更多有关正则表达式的知识。

**实例**

只能包含三个字母的输入字段（无数字或特殊字符）：

```
Country code: 
<input type="text" name="country_code" pattern="[A-Za-z]{3}" title="Three letter country code">
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_input_pattern)

### placeholder 属性

placeholder 属性规定用以描述输入字段预期值的提示（样本值或有关格式的简短描述）。

该提示会在用户输入值之前显示在输入字段中。

placeholder 属性适用于以下输入类型：text、search、url、tel、email 以及 password。

**实例**

拥有占位符文本的输入字段：

```
<input type="text" name="fname" placeholder="First name">
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_input_placeholder)

### required 属性

required 属性是布尔属性。

如果设置，则规定在提交表单之前必须填写输入字段。

required 属性适用于以下输入类型：text、search、url、tel、email、password、date pickers、number、checkbox、radio、and file.

**实例**

必填的输入字段：

```
Username: <input type="text" name="usrname" required>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_input_required)

### step 属性

step 属性规定 <input> 元素的合法数字间隔。

示例：如果 step="3"，则合法数字应该是 -3、0、3、6、等等。

提示：step 属性可与 max 以及 min 属性一同使用，来创建合法值的范围。

step 属性适用于以下输入类型：number、range、date、datetime、datetime-local、month、time 以及 week。

**示例**

拥有具体的合法数字间隔的输入字段：

```
<input type="number" name="points" step="3">
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_input_step)

# HTML5

## HTML5 简介

### 每一章中的 HTML5 示例

**实例**

```
<!DOCTYPE html>
<html>
<body>

<video width="420" controls>
  <source src="mov_bbb.mp4" type="video/mp4">
  <source src="mov_bbb.ogg" type="video/ogg">
 Your browser does not support the video tag.
</video>

</body>
</html>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_video_all)

点击“亲自试一试”来查看该例如何运行。

### 什么是 HTML5？

HTML5 是最新的 HTML 标准。

HTML5 是专门为承载丰富的 web 内容而设计的，并且无需额外插件。

HTML5 拥有新的语义、图形以及多媒体元素。

HTML5 提供的新元素和新的 API 简化了 web 应用程序的搭建。

HTML5 是跨平台的，被设计为在不同类型的硬件（PC、平板、手机、电视机等等）之上运行。

注释：在下面的章节中，您将学到如何“帮助”老版本的浏览器处理 HTML5。

### HTML5 中的新内容？

HTML5 的新的文档类型（DOCTYPE）声明非常简单：

```
<!DOCTYPE html>
The new character encoding (charset) declaration is also very simple:

<meta charset="UTF-8">
```

HTML5 实例：

```
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Title of the document</title>
</head>

<body>
Content of the document......
</body>

</html>
```

注释：HTML5 中默认的字符编码是 UTF-8。

### HTML5 - 新的属性语法

HTML5 标准允许 4 中不同的属性语法。

本例演示在 <input> 标签中使用的不同语法：

| 类型          | 示例                                          |
| ------------- | --------------------------------------------- |
| Empty         | <input type="text" value="John Doe" disabled> |
| Unquoted      | <input type="text" value=John Doe>            |
| Double-quoted | <input type="text" value="John Doe">          |
| Single-quoted | <input type="text" value='John Doe'>          |

在 HTML5 标准中，根据对属性的需求，可能会用到所有 4 种语法。

### HTML5 - 新特性

HTML5 的一些最有趣的新特性：

- 新的语义元素，比如 <header>, <footer>, <article>, and <section>。
- 新的表单控件，比如数字、日期、时间、日历和滑块。
- 强大的图像支持（借由 <canvas> 和 <svg>）
- 强大的多媒体支持（借由 <video> 和 <audio>）
- 强大的新 API，比如用本地存储取代 cookie。

### HTML5 - 被删元素

以下 HTML 4.01 元素已从 HTML5 中删除：

- <acronym>
- <applet>
- <basefont>
- <big>
- <center>
- <dir>
- <font>
- <frame>
- <frameset>
- <noframes>
- <strike>
- <tt>

## HTML5 浏览器支持



**您可以帮助老版本浏览器处理 HTML5。**

### HTML5 浏览器支持

所有现代浏览器都支持 HTML5。

此外，所有浏览器，不论新旧，都会自动把未识别元素当做行内元素来处理。

正因如此，您可以帮助老式浏览器处理”未知的“ HTML 元素。

注释：您甚至可以教授石器时代的 IE6 如何处理未知的 HTML 元素。

### 把 HTML5 元素定义为块级元素

HTML5 定义了八个新的*语义* HTML 元素。所有都是*块级*元素。

您可以把 CSS *display* 属性设置为 *block*，以确保老式浏览器中正确的行为：

**实例**

```
header, section, footer, aside, nav, main, article, figure {
    display: block; 
}
```

### 向 HTML 添加新元素

您可以通过浏览器 trick 向 HTML 添加任何新元素：

本例向 HTML 添加了一个名为 <myHero> 的新元素，并为其定义 display 样式：

**实例**

```
<!DOCTYPE html>
<html>

<head>
  <title>Creating an HTML Element</title>
  <script>document.createElement("myHero")</script>
  <style>
  myHero {
    display: block;
    background-color: #ddd;
    padding: 50px;
    font-size: 30px;
  } 
  </style> 
</head>

<body>

<h1>My First Heading</h1>

<p>My first paragraph.</p>

<myHero>My First Hero</myHero>

</body>
</html>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_browsers)

已添加的 JavaScript 语句 document.createElement("myHero")，仅适用于 IE。

### Internet Explorer 的问题

上述方案可用于所有新的 HTML5 元素，但是：

注意：Internet Explorer 8 以及更早的版本，不允许对未知元素添加样式。

幸运的是，Sjoerd Visscher 创造了 "HTML5 Enabling JavaScript", *"the shiv"*：

```
<!--[if lt IE 9]>
  <script src="http://html5shiv.googlecode.com/svn/trunk/html5.js"></script>
<![endif]-->
```

以上代码是一段注释，但是 IE9 的早期版本会读取它（并理解它）。

### 完整的 Shiv 解决方案

**实例**

```
<!DOCTYPE html>
<html>

<head>
  <title>Styling HTML5</title>
  <!--[if lt IE 9]>
  <script src="http://html5shiv.googlecode.com/svn/trunk/html5.js"></script>
  <![endif]-->
</head>

<body>

<h1>My First Article</h1>

<article>
London is the capital city of England. 
It is the most populous city in the United Kingdom, 
with a metropolitan area of over 13 million inhabitants.
</article>

</body>
</html>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_browsers_theshiv)

引用 shiv 代码的链接必须位于 <head> 元素中，因为 Internet Explorer 需要在读取之前认识所有新元素。

### HTML5 Skeleton

**实例**

```
<!DOCTYPE html>
<html lang="en">
<head>
<title>HTML5 Skeleton</title>
<meta charset="utf-8">

<!--[if lt IE 9]>
<script src="http://html5shiv.googlecode.com/svn/trunk/html5.js">
</script>
<![endif]-->

<style>
body {font-family: Verdana, sans-serif; font-size:0.8em;}
header,nav, section,article,footer
{border:1px solid grey; margin:5px; padding:8px;}
nav ul {margin:0; padding:0;}
nav ul li {display:inline; margin:5px;}
</style>
</head>

<body>

<header>
  <h1>HTML5 SKeleton</h1>
</header>

<nav>
<ul>
  <li><a href="html5_semantic_elements.asp">HTML5 Semantic</a></li>
  <li><a href="html5_geolocation.asp">HTML5 Geolocation</a></li>
  <li><a href="html5_canvas.asp">HTML5 Graphics</a></li>
</ul>
</nav>

<section>

<h1>Famous Cities</h1>

<article>
<h2>London</h2>
<p>London is the capital city of England. It is the most populous city in the United Kingdom,
with a metropolitan area of over 13 million inhabitants.</p>
</article>

<article>
<h2>Paris</h2>
<p>Paris is the capital and most populous city of France.</p>
</article>

<article>
<h2>Tokyo</h2>
<p>Tokyo is the capital of Japan, the center of the Greater Tokyo Area,
and the most populous metropolitan area in the world.</p>
</article>

</section>

<footer>
<p>© 2014 W3Schools. All rights reserved.</p>
</footer>

</body>
</html>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_html5_skeleton)

## HTML5 新元素

### HTML5 中的新元素

下面列出的 HTML5 的新元素，以及对它们的描述。

### 新的语义/结构元素

HTML5 提供的新元素可以构建更好的文档结构：

| 标签         | 描述                                                 |
| ------------ | ---------------------------------------------------- |
| <article>    | 定义文档内的文章。                                   |
| <aside>      | 定义页面内容之外的内容。                             |
| <bdi>        | 定义与其他文本不同的文本方向。                       |
| <details>    | 定义用户可查看或隐藏的额外细节。                     |
| <dialog>     | 定义对话框或窗口。                                   |
| <figcaption> | 定义 <figure> 元素的标题。                           |
| <figure>     | 定义自包含内容，比如图示、图表、照片、代码清单等等。 |
| <footer>     | 定义文档或节的页脚。                                 |
| <header>     | 定义文档或节的页眉。                                 |
| <main>       | 定义文档的主内容。                                   |
| <mark>       | 定义重要或强调的内容。                               |
| <menuitem>   | 定义用户能够从弹出菜单调用的命令/菜单项目。          |
| <meter>      | 定义已知范围（尺度）内的标量测量。                   |
| <nav>        | 定义文档内的导航链接。                               |
| <progress>   | 定义任务进度。                                       |
| <rp>         | 定义在不支持 ruby 注释的浏览器中显示什么。           |
| <rt>         | 定义关于字符的解释/发音（用于东亚字体）。            |
| <ruby>       | 定义 ruby 注释（用于东亚字体）。                     |
| <section>    | 定义文档中的节。                                     |
| <summary>    | 定义 <details> 元素的可见标题。                      |
| <time>       | 定义日期/时间。                                      |
| <wbr>        | 定义可能的折行（line-break）。                       |

阅读更多有关 [HTML5 语义](http://www.w3school.com.cn/html/html5_semantic_elements.asp)的内容。

### 新的表单元素

| 标签       | 描述                             |
| ---------- | -------------------------------- |
| <datalist> | 定义输入控件的预定义选项。       |
| <keygen>   | 定义键对生成器字段（用于表单）。 |
| <output>   | 定义计算结果。                   |

阅读更多有关 [HTML 表单元素](http://www.w3school.com.cn/html/html_form_elements.asp)中新老元素。

### 新的输入类型



![](D:\ProjectList\Github_pages\media\html5new.png)

学习 [HTML 输入类型](http://www.w3school.com.cn/html/html_form_input_types.asp)中的所有新老输入类型。

学习 [HTML 输入属性](http://www.w3school.com.cn/html/html_form_attributes.asp)中的所有输入属性。

### HTML5 - 新的属性语法

HTML5 允许四种不同的属性语法。

该例演示 <input> 标签中使用的不同语法：

| 标签          | 描述                                          |
| ------------- | --------------------------------------------- |
| Empty         | <input type="text" value="John Doe" disabled> |
| Unquoted      | <input type="text" value=John>                |
| Double-quoted | <input type="text" value="John Doe">          |
| Single-quoted | <input type="text" value='John Doe'>          |

在 HTML5 中，根据属性所需，可能会使用所有这四种语法。

### HTML5 图像

| 标签     | 描述                             |
| -------- | -------------------------------- |
| <canvas> | 定义使用 JavaScript 的图像绘制。 |
| <svg>    | 定义使用 SVG 的图像绘制。        |

阅读更多有关 [HTML5 Canvas](http://www.w3school.com.cn/html/html5_canvas.asp) 的内容。

阅读更多有关 [HTML5 SVG](http://www.w3school.com.cn/html/html5_svg.asp) 的内容。

### 新的媒介元素

| 标签     | 描述                                 |
| -------- | ------------------------------------ |
| <audio>  | 定义声音或音乐内容。                 |
| <embed>  | 定义外部应用程序的容器（比如插件）。 |
| <source> | 定义 <video> 和 <audio> 的来源。     |
| <track>  | 定义 <video> 和 <audio> 的轨道。     |
| <video>  | 定义视频或影片内容。                 |

阅读更多有关 [HTML5 视频](http://www.w3school.com.cn/html/html_video.asp)的内容。

阅读更多有关 [HTML5 音频](http://www.w3school.com.cn/html/html_audio.asp)的内容。

## HTML5 语义元素

**语义学（源自古希腊）可定义为对语言意义的研究。**

**语义元素是拥有语义的元素。**

### 什么是语义元素？

语义元素清楚地向浏览器和开发者描述其意义。

*非语义*元素的例子：<div> 和 <span> - 无法提供关于其内容的信息。

*语义*元素的例子：<form>、<table> 以及 <img> - 清晰地定义其内容。

### 浏览器支持

|      |      |      |      |      |
| ---- | ---- | ---- | ---- | ---- |
| Yes  | Yes  | Yes  | Yes  | Yes  |

所有现代浏览器均支持 HTML5 语义元素。

此外，您可以“帮助”老式浏览器处理“未知元素”。

在 HTML5 浏览器支持这一章学习更多知识。

### HTML5 中新的语义元素

许多网站包含了指示导航、页眉以及页脚的 HTML 代码，例如这些：<div id="nav"> <div class="header"> <div id="footer">。

HTML5 提供了定义页面不同部分的新语义元素：

- <article>
- <aside>
- <details>
- <figcaption>
- <figure>
- <footer>
- <header>
- <main>
- <mark>
- <nav>
- <section>
- <summary>
- <time>

### HTML5 语义元素



### HTML5 &lt;section> 元素

<section> 元素定义文档中的节。

根据 W3C 的 HTML 文献：“节（section）是有主题的内容组，通常具有标题”。

可以将网站首页划分为简介、内容、联系信息等节。

**实例**

```
<section>
   <h1>WWF</h1>
   <p>The World Wide Fund for Nature (WWF) is....</p>
</section> 
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_section)

### HTML5 &lt;article> 元素

<article> 元素规定独立的自包含内容。

文档有其自身的意义，并且可以独立于网站其他内容进行阅读。

<article> 元素的应用场景：

- 论坛
- 博客
- 新闻

**实例**

```
<article>
   <h1>What Does WWF Do?</h1>
   <p>WWF's mission is to stop the degradation of our planet's natural environment,
  and build a future in which humans live in harmony with nature.</p>
</article> 
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_article)

### 嵌套语义元素

在 HTML5 标准中，<article> 元素定义完整的相关元素自包含块。

<section> 元素被定义为相关元素块。

我们能够使用该定义来决定如何嵌套元素吗？不，我们不能！

在因特网上，您会发现 <section> 元素包含 <article> 元素的 HTML 页面，还有 <article> 元素包含 <sections> 元素的页面。

您还会发现 <section> 元素包含 <section> 元素，同时 <article> 元素包含 <article> 元素。

### HTML5 &lt;header> 元素

<header> 元素为文档或节规定页眉。

<header> 元素应该被用作介绍性内容的容器。

一个文档中可以有多个 <header> 元素。

下例为一篇文章定义了页眉：

**实例**

```
<article>
   <header>
     <h1>What Does WWF Do?</h1>
     <p>WWF's mission:</p>
   </header>
   <p>WWF's mission is to stop the degradation of our planet's natural environment,
  and build a future in which humans live in harmony with nature.</p>
</article> 
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_header)

### HTML5 &lt;footer> 元素

<footer> 元素为文档或节规定页脚。

<footer> 元素应该提供有关其包含元素的信息。

页脚通常包含文档的作者、版权信息、使用条款链接、联系信息等等。

您可以在一个文档中使用多个 <footer> 元素。

**实例**

```
<footer>
   <p>Posted by: Hege Refsnes</p>
   <p>Contact information: <a href="mailto:someone@example.com">
  someone@example.com</a>.</p>
</footer> 
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_footer)

### HTML5 &lt;nav> 元素

<nav> 元素定义导航链接集合。

<nav> 元素旨在定义大型的导航链接块。不过，并非文档中所有链接都应该位于 <nav> 元素中！

**实例**

```
<nav>
<a href="/html/">HTML</a> |
<a href="/css/">CSS</a> |
<a href="/js/">JavaScript</a> |
<a href="/jquery/">jQuery</a>
</nav> 
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_nav)

### HTML5 &lt;aside> 元素

<aside> 元素页面主内容之外的某些内容（比如侧栏）。

aside 内容应该与周围内容相关。

**实例**

```
<p>My family and I visited The Epcot center this summer.</p>

<aside>
   <h4>Epcot Center</h4>
   <p>The Epcot Center is a theme park in Disney World, Florida.</p>
</aside> 
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_aside)

## HTML5 <figure> 和 <figcaption> 元素

在书籍和报纸中，与图片搭配的标题很常见。

标题（caption）的作用是为图片添加可见的解释。

通过 HTML5，图片和标题能够被组合在 *<figure>* 元素中：

### 实例

```
<figure>
   <img src="pic_mountain.jpg" alt="The Pulpit Rock" width="304" height="228">
   <figcaption>Fig1. - The Pulpit Pock, Norway.</figcaption>
</figure> 
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_figcaption)

<img> 元素定义图像，<figcaption> 元素定义标题。

### 为何使用 HTML5 元素？

如果使用 HTML4 的话，开发者会使用他们喜爱的属性名来设置页面元素的样式：

header, top, bottom, footer, menu, navigation, main, container, content, article, sidebar, topnav, ...

如此，浏览器便无法识别正确的网页内容。

而通过 HTML5 元素，比如：<header> <footer> <nav> <section> <article>，此问题迎刃而解。

根据 W3C，语义网：

> “允许跨应用程序、企业和团体对数据进行分享和重用。”

### HTML5 中的语义元素

下面列出了以字母顺序排列的 HTML5 新语义元素。

这些链接指向完整的 HTML 参考手册。

| 标签         | 描述                                               |
| ------------ | -------------------------------------------------- |
| <article>    | 定义文章。                                         |
| <aside>      | 定义页面内容以外的内容。                           |
| <details>    | 定义用户能够查看或隐藏的额外细节。                 |
| <figcaption> | 定义 <figure> 元素的标题。                         |
| <figure>     | 规定自包含内容，比如图示、图表、照片、代码清单等。 |
| <footer>     | 定义文档或节的页脚。                               |
| <header>     | 规定文档或节的页眉。                               |
| <main>       | 规定文档的主内容。                                 |
| <mark>       | 定义重要的或强调的文本。                           |
| <nav>        | 定义导航链接。                                     |
| <section>    | 定义文档中的节。                                   |
| <summary>    | 定义 <details> 元素的可见标题。                    |
| <time>       | 定义日期/时间。                                    |

## HTML5 迁移

### 从 HTML4 迁移至 HTML5

本章讲解如何从一张典型的 HTML4 页面迁移至典型的 HTML5。

本章演示如何把一张已有的 HTML4 页面转换为 HTML5 页面，在不破坏如何原始内容和结构的情况下。

注释：您可以使用相同的技巧从 HTML4 以及 XHTML 迁移至 HTML5。

| 典型的 HTML4       | 典型的 HTML5 |
| ------------------ | ------------ |
| <div id="header">  | <header>     |
| <div id="menu">    | <nav>        |
| <div id="content"> | <section>    |
| <div id="post">    | <article>    |
| <div id="footer">  | <footer>     |

### 典型的 HTML4 页面

**实例**

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" 
"http://www.w3.org/TR/html4/loose.dtd">
<html lang="en">
<head>
<meta http-equiv="Content-Type" content="text/html;charset=utf-8">
<title>HTML4</title>
<style>
  body {font-family:Verdana,sans-serif;font-size:0.8em;}
  div#header,div#footer,div#content,div#post 
  {border:1px solid grey;margin:5px;margin-bottom:15px;padding:8px;background-color:white;}
  div#header,div#footer {color:white;background-color:#444;margin-bottom:5px;}
  div#content {background-color:#ddd;}
  div#menu ul {margin:0;padding:0;}
  div#menu ul li {display:inline; margin:5px;}
</style>
</head>
<body>

<div id="header">
  <h1>Monday Times</h1>
</div>

<div id="menu">
  <ul>
    <li>News</li>
    <li>Sports</li>
    <li>Weather</li>
  </ul>
</div>

<div id="content">
<h2>News Section</h2>

<div id="post">
  <h2>News Article</h2>
  <p>Ipsum lurum hurum turum ipsum lurum hurum turum ipsum lurum hurum turum ipsum 
  lurum hurum turum.</p>
  <p>Ipsum lurum hurum turum ipsum lurum hurum turum ipsum lurum hurum turum ipsum 
  lurum hurum turum.</p>
</div>

<div id="post">
  <h2>News Article</h2>
  <p>Ipsum lurum hurum turum ipsum lurum hurum turum ipsum lurum hurum turum ipsum 
  lurum hurum turum.</p>
  <p>Ipsum lurum hurum turum ipsum lurum hurum turum ipsum lurum hurum turum ipsum 
  lurum hurum turum.</p>
</div>

</div>

<div id="footer">
  <p>&copy; 2014 Monday Times. All rights reserved.</p>
</div>

</body>
</html>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_html4_skeleton)

### 更改为 HTML5 Doctype

修改文档类型，从 HTML4 doctype：

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" 
"http://www.w3.org/TR/html4/loose.dtd">
```

修改为 HTML5 doctype：

```
<!DOCTYPE html>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_html5_skeleton_1)

### 更改为 HTML5 编码

修改编码信息，从 HTML4：

```
<meta http-equiv="Content-Type" content="text/html;charset=utf-8">
```

改为 HTML5：

```
<meta charset="utf-8">
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_html5_skeleton_2)

### 添加 shiv

所有现代浏览器都支持 HTML5 语义元素。

此外，您可以“教授”老式浏览器如何处理“未知元素”。

为 Internet Explorer 支持而添加的 shiv：

```
<!--[if lt IE 9]>
  <script src="http://html5shiv.googlecode.com/svn/trunk/html5.js"></script>
<![endif]-->
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_html5_skeleton_3)

注释：请在 HTML5 浏览器支持中阅读更多有关 shiv 的知识。

### 为 HTML5 语义元素添加 CSS

请看已有的 CSS 样式：

```
div#header,div#footer,div#content,div#post {
    border:1px solid grey;margin:5px;margin-bottom:15px;padding:8px;background-color:white;
}
div#header,div#footer {
    color:white;background-color:#444;margin-bottom:5px;
}
div#content {
    background-color:#ddd;
}
div#menu ul {
    margin:0;padding:0;
}
div#menu ul li {
    display:inline; margin:5px;
}
Duplicate with equal CSS styles for HTML5 semantic elements:

header,footer,section,article {
    border:1px solid grey;margin:5px;margin-bottom:15px;padding:8px;background-color:white;
}
header,footer {
    color:white;background-color:#444;margin-bottom:5px;
}
section {
    background-color:#ddd;
}
nav ul  {
    margin:0;padding:0;
}
nav ul li {
    display:inline; margin:5px;
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_html5_skeleton_4)

### 更改为 HTML5 &lt;header> 和 &lt;footer>

把 id="header" 和 id="footer" 的 <div> 元素：

```
<div id="header">
  <h1>Monday Times</h1>
</div>
.
.
.
<div id="footer">
  <p>&copy; 2014 W3Schools. All rights reserved.</p>
</div>
```

修改为 HTML5 语义元素 <header> 和 <footer>：

```
<header>
  <h1>Monday Times</h1>
</header>
.
.
.
<footer>
  <p>© 2014 W3Schools. All rights reserved.</p>
</footer>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_html5_skeleton_5)

### 更改为 HTML5 &lt;nav>

把 id="menu" 的 <div> 元素：

```
<div id="menu">
  <ul>
    <li>News</li>
    <li>Sports</a></li>
    <li>Weather</li>
  </ul>
</div>
```

修改为 HTML5 语义元素 <nav>：

```
<nav>
  <ul>
    <li>News</li>
    <li>Sports</a></li>
    <li>Weather</li>
  </ul>
</nav>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_html5_skeleton_6)

### 更改为 HTML5 &lt;section>

把 id="content" 的 the <div> 元素：

```
<div id="content">
.
.
.
</div>
```

修改为 HTML5 语义元素 <section>：

```
<section>
.
.
.
</section>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_html5_skeleton_7)

### 更改为 HTML5 &lt;article>

把 class="post" 的所有 <div> 元素：

```
<div class="post">
  <h2>News Article</h2>
  <p>Ipsum lurum hurum turum ipsum lurum hurum turum ipsum lurum hurum turum ipsum 
  lurum hurum turum.</p>
</div>
```

修改为 HTML5 语义元素 <article>：

```
<article>
  <h2>News Article</h2>
  <p>Ipsum lurum hurum turum ipsum lurum hurum turum ipsum lurum hurum turum ipsum 
  lurum hurum turum.</p>
</article>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_html5_skeleton_8)

删除这些“不再需要的”样式：

```
div#header,div#footer,div#content,div#post {
    border:1px solid grey;margin:5px;margin-bottom:15px;padding:8px;background-color:white;
}
div#header,div#footer {
    color:white;background-color:#444;margin-bottom:5px;
}
div#content {
    background-color:#ddd;
}
div#menu ul {
    margin:0;padding:0;
}
div#menu ul li {
    display:inline; margin:5px;
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_html5_skeleton_9)

### 典型的 HTML5 页面

最后您可以删除 <head> 标签。HTML5 中不再需要它们：

**实例**

```
<!DOCTYPE html>
<html lang="en">
<title>HTML5</title>
<meta charset="utf-8">

<!--[if lt IE 9]>
<script src="http://html5shiv.googlecode.com/svn/trunk/html5.js">
</script>
<![endif]-->

<style>
body {
    font-family:Verdana,sans-serif;font-size:0.8em;
}
header,footer,section,article {
    border:1px solid grey;
    margin:5px;margin-bottom:15px;padding:8px;
    background-color:white;
}
header,footer {
    color:white;background-color:#444;margin-bottom:5px;
}
section {
    background-color:#ddd;
}
nav ul {
    margin:0;padding:0;
}
nav ul li {
    display:inline; margin:5px;
}
</style>
<body>

<header>
  <h1>Monday Times</h1>
</header>

<nav>
  <ul>
    <li>News</li>
    <li>Sports</li>
    <li>Weather</li>
  </ul>
</nav>

<section>
<h2>News Section</h2>

<div id="post">
  <h2>News Article</h2>
  <p>Ipsum lurum hurum turum ipsum lurum hurum turum ipsum lurum hurum turum ipsum 
  lurum hurum turum.</p>
  <p>Ipsum lurum hurum turum ipsum lurum hurum turum ipsum lurum hurum turum ipsum 
  lurum hurum turum.</p>
  <p>Ipsum lurum hurum turum ipsum lurum hurum turum ipsum lurum hurum turum ipsum 
  lurum hurum turum.</p>
</div>

<div id="post">
<h2>News Article</h2>
  <p>Ipsum lurum hurum turum ipsum lurum hurum turum ipsum lurum hurum turum ipsum 
  lurum hurum turum.</p>
  <p>Ipsum lurum hurum turum ipsum lurum hurum turum ipsum lurum hurum turum ipsum 
  lurum hurum turum.</p>
  <p>Ipsum lurum hurum turum ipsum lurum hurum turum ipsum lurum hurum turum ipsum 
  lurum hurum turum.</p>
</div>

</section>

<footer>
  <p>&copy; 2014 Monday Times. All rights reserved.</p>
</footer>

</body>
</html>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_html5_skeleton)

### &lt;article> &lt;section> 与 &lt;div> 之间的差异

在 HTML5 标准中，<article> <section> 与 <div> 之间的差异很小，令人困惑。

在 HTML5 标准中，<section> 元素被定位为相关元素的块。

<article> 元素被定义为相关元素的完整的自包含块。

<div> 元素被定义为子元素的块。

如何理解呢？

在上面的例子中，我们曾使用 <section> 作为相关 <articles> 的容器。

但是，我们也能够把 <article> 用作文章的容器。

下面是一些不同的例子：

```
<article> 中的 <article>：

<article>

<h2>Famous Cities</h2>

<article>
<h2>London</h2>
<p>London is the capital city of England. It is the most populous city in the United Kingdom,
with a metropolitan area of over 13 million inhabitants.</p>
</article>

<article>
<h2>Paris</h2>
<p>Paris is the capital and most populous city of France.</p>
</article>

<article>
<h2>Tokyo</h2>
<p>Tokyo is the capital of Japan, the center of the Greater Tokyo Area,
and the most populous metropolitan area in the world.</p>
</article>

</article>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_html5_skeleton_2)

```
<article> 中的 <div>：

<article>

<h2>Famous Cities</h2>

<div class="city">
<h2>London</h2>
<p>London is the capital city of England. It is the most populous city in the United Kingdom,
with a metropolitan area of over 13 million inhabitants.</p>
</div>

<div class="city">
<h2>Paris</h2>
<p>Paris is the capital and most populous city of France.</p>
</div>

<div class="city">
<h2>Tokyo</h2>
<p>Tokyo is the capital of Japan, the center of the Greater Tokyo Area,
and the most populous metropolitan area in the world.</p>
</div>

</article>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_html5_skeleton_3)

```
<article> 中的 <section> 中的 <div>：

<article>

<section>
<h2>Famous Cities</h2>

<div class="city">
<h2>London</h2>
<p>London is the capital city of England. It is the most populous city in the United Kingdom,
with a metropolitan area of over 13 million inhabitants.</p>
</div>

<div class="city">
<h2>Paris</h2>
<p>Paris is the capital and most populous city of France.</p>
</div>

<div class="city">
<h2>Tokyo</h2>
<p>Tokyo is the capital of Japan, the center of the Greater Tokyo Area,
and the most populous metropolitan area in the world.</p>
</div>
</section>

<section>
<h2>Famous Countries</h2>

<div class="country">
<h2>England</h2>
<p>London is the capital city of England. It is the most populous city in the United Kingdom,
with a metropolitan area of over 13 million inhabitants.</p>
</div>

<div class="country">
<h2>France</h2>
<p>Paris is the capital and most populous city of France.</p>
</div>

<div class="country">
<h2>Japan</h2>
<p>Tokyo is the capital of Japan, the center of the Greater Tokyo Area,
and the most populous metropolitan area in the world.</p>
</div>
</section>

</article>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_html5_skeleton_4)

## HTML(5) 样式指南和代码约定

### HTML 代码约定

web 开发者常常不确定在 HTML 中使用的代码样式和语法。

在 2000 年至 2010 年之间，许多 web 开发者从 HTML 转换为 XHTML。

通过 XHTML，开发者不得不编写有效的“格式良好的”代码。

HTML5 在代码验证时会更宽松一点。

通过 HTML5，您必须创建属于自己的*最佳实践、样式指南和代码约定*。

### 智能且有未来保证

对样式的合乎逻辑的使用，可以令其他人更容易理解和使用您的 HTML。

在未来，诸如 XML 阅读器之类的程序，也许需要阅读您的 HTML。

使用格式良好的“近似 XHTML 的”语法，能够更智能。

注释：请始终保持您的样式智能、整洁、纯净、格式良好。

### 请使用正确的文档类型

请始终在文档的首行声明文档类型：

```
<!DOCTYPE html>
```

如果您一贯坚持小写标签，那么可以使用：

```
<!doctype html>
```

### 请使用小写元素名

HTML5 允许在元素名中使用混合大小写字母。

我们推荐使用小写元素名：

- 混合大小写名称并不好
- 开发者习惯使用小写名（比如在 XHTML 中）
- 小写更起来更纯净
- 小写更易书写

不太好：

```
<SECTION> 
  <p>This is a paragraph.</p>
</SECTION>
```

很糟糕：

```
<Section> 
  <p>This is a paragraph.</p>
</SECTION>
```

还不错：

```
<section> 
  <p>This is a paragraph.</p>
</section>
```

### 关闭所有 HTML 元素

在 HTML5 中，您不必关闭所有元素（例如 <p> 元素）。

我们建议关闭所有 HTML 元素：

看起来不好：

```
<section>
  <p>This is a paragraph.
  <p>This is a paragraph.
</section>
```

看起来不错：

```
<section>
  <p>This is a paragraph.</p>
  <p>This is a paragraph.</p>
</section>
```

### 关闭空的 HTML 元素

在 HTML5 中，关闭空元素是可选的。

允许这样：

```
<meta charset="utf-8">
```

也允许这样：

```
<meta charset="utf-8" />
```

斜杠（/）在 XHTML 和 XML 中是必需的。

如果您期望 XML 软件来访问您的页面，保持这个习惯是个好主意。

### 使用小写属性名

HTML5 允许大小写混合的属性名。

我们建议使用小写属性名：

- 混合属性名并不好
- 开发者习惯于使用小写属性名（比如在 XHTML 中）
- 小写属性名看情况更纯净
- 小写属性名更易书写

看起来不好：

```
<div CLASS="menu">
```

看起来不错：

```
<div class="menu">
```

### 属性值加引号

HTML5 允许不加引号的属性值。

我们推荐属性值加引号：

- 如果属性值包含值，则必须使用引号
- 混合样式绝对不好
- 加引号的值更易阅读

这个属性值无效，因为值中包含空格：

```
<table class=table striped>
```

这样是有效的：

```
<table class="table striped">
```

### 必需的属性

请始终对图像使用 *alt* 属性。当图像无法显示时该属性很重要。

```
<img src="html5.gif" alt="HTML5" style="width:128px;height:128px">
```

请始终定义图像尺寸。这样做会减少闪烁，因为浏览器会在图像加载之前为图像预留空间。

```
<img src="html5.gif" alt="HTML5" style="width:128px;height:128px">
```

### 空格和等号

等号两边的空格是合法的：

```
<link rel = "stylesheet" href = "styles.css">
```

但是精简空格更易阅读， But space-less is easier to read, and groups entities better together:

```
<link rel="stylesheet" href="styles.css">
```

### 避免长代码行

当使用 HTML 编辑器时，通过左右滚动来阅读 HTML 代码很不方便。

请尽量避免代码行超过 80 个字符。

### 空行和缩进

请勿毫无理由地增加空行。

为了提高可读性，请增加空行来分隔大型或逻辑代码块。

为了提高可读性，请增加两个空格的缩进。请勿使用 TAB。

请勿使用没有必要的空行和缩进。没有必要在短的和相关项目之间使用空行，也没有必要缩进每个元素：

不必要：

```
<body>

  <h1>Famous Cities</1>

  <h2>Tokyo</h2>

  <p>
    Tokyo is the capital of Japan, the center of the Greater Tokyo Area,
    and the most populous metropolitan area in the world.
    It is the seat of the Japanese government and the Imperial Palace,
    and the home of the Japanese Imperial Family.
  </p>

</body>
```

更好：

```
<body>

<h1>Famous Cities</1>
<h2>Tokyo</h2>

<p>
Tokyo is the capital of Japan, the center of the Greater Tokyo Area,
and the most populous metropolitan area in the world.
It is the seat of the Japanese government and the Imperial Palace,
and the home of the Japanese Imperial Family.
</p>

</body>
```

表格示例：

```
<table>
  <tr>
    <th>Name</th>
    <th>Description</th>
  <tr>
  <tr>
    <td>A</td>
    <td>Description of A</td>
  <tr>
  <tr>
    <td>B</td>
    <td>Description of B</td>
  <tr>
</table>
```

列表示例：

```
<ol>
  <li>LondonA</li>
  <li>Paris</li>
  <li>Tokyo</li>
</ol>
```

## 省略 &lt;html> 和 &lt;body>？

在 HTML5 标准中，能够省略 <html> 标签和 <body> 标签。

以下代码作为 HTML5 进行验证：

**示例**

```
<!DOCTYPE html>
<head>
  <title>Page Title</title>
</head>

<h1>This is a heading</h1>
<p>This is a paragraph.</p>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_syntax_nobody)

**我们不推荐省略 <html> 和 <body> 标签。**

<html> 元素是文本的根元素。它是规定页面语言的理想位置。

```
<!DOCTYPE html>
<html lang="en-US">
```

对于可访问应用程序（屏幕阅读器）和搜索引擎，声明语言很重要。

省略 <html> 或 <body> c可令 DOM 和 XML 软件崩溃。

省略 <body> 会在老式浏览器（IE9）中产生错误。

### 省略 &lt;head>？

在 HTML5 标准中，<head> 标签也能够被省略。

默认地，浏览器会把 <body> 之前的所有元素添加到默认的 <head> 元素。

通过省略 <head> 标签，您能够降低 HTML 的复杂性：

**示例**

```
<!DOCTYPE html>
<html>
<title>Page Title</title>

<body>
  <h1>This is a heading</h1>
  <p>This is a paragraph.</p>
</body>

</html>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_syntax_nohead)

注释：对于 web 开发者，省略标签的做法是陌生的。建立规则需要时间。

### 元数据

<title> 元素在 HTML5 中是必需的。请尽可能制作有意义的标题。

```
<title>HTML5 Syntax and Coding Style</title>
```

为了确保恰当的解释，以及正确的搜索引擎索引，在文档中对语言和字符编码的定义越早越好：

```
<!DOCTYPE html>
<html lang="en-US">
<head>
  <meta charset="UTF-8">
  <title>HTML5 Syntax and Coding Style</title>
</head>
```

### HTML 注释

短注释应该在单行中书写，并在 <!-- 之后增加一个空格，在 <!-- 之前增加一个空格：

```
<!-- This is a comment -->
```

长注释，跨越多行，应该通过 <!-- 和 --> 在独立的行中书写：

```
<!-- 
  This is a long comment example. This is a long comment example. This is a long comment example.
  This is a long comment example. This is a long comment example. This is a long comment example.
-->
```

长注释更易观察，如果它们被缩进两个空格的话。

### 样式表

请使用简单的语法来链接样式表（type 属性不是必需的）：

```
<link rel="stylesheet" href="styles.css">
```

短规则可以压缩为一行，就像这样：

```
p.into {font-family:"Verdana"; font-size:16em;}
```

长规则应该分为多行：

```
body {
  background-color: lightgrey;
  font-family: "Arial Black", Helvetica, sans-serif;
  font-size: 16em;
  color: black;
}
```

- 开括号与选择器位于同一行
- 在开括号之前用一个空格
- 使用两个字符的缩进
- 在每个属性与其值之间使用冒号加一个空格
- 在每个逗号或分号之后使用空格
- 在每个属性值对（包括最后一个）之后使用分号
- 只在值包含空格时使用引号来包围值
- 把闭括号放在新的一行，之前不用空格
- 避免每行超过 80 个字符

注释：在逗号或分号之后添加空格，是所有书写类型的通用规则。

### 在 HTML 中加载 JavaScript

请使用简单的语法来加载外部脚本（type 属性不是必需的）：

```
<script src="myscript.js">
```

### 通过 JavaScript 访问 HTML 元素

使用“不整洁”的 HTML 样式的后果，是可能会导致 JavaScript 错误。

这两个 JavaScript 语句会产生不同的结果：

```
var obj = getElementById("Demo")

var obj = getElementById("demo")
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_syntax_javascript)

如果可能，请在 HTML 中使用（与 JavaScript）相同的命名约定。

请访问 JavaScript 样式指南。

### 使用小写文件名

大多数 web 服务器（Apache、Unix）对文件名的大小写敏感：

不能以 london.jpg 访问 London.jpg。

其他 web 服务器（微软，IIS）对大小写不敏感：

能够以 london.jpg 或 London.jpg 访问 London.jpg。

如果使用混合大小写，那么您必须保持高度的一致性。

如果您从对大小写不敏感的服务器转到一台对大小写敏感的服务器上，这些小错误将破坏您的网站。

为了避免这些问题，请始终使用小写文件名（如果可以的话）。

### 文件扩展名

HTML 文件名应该使用扩展名 *.html*（而不是 .htm）。

CSS 文件应该使用扩展名 *.css*。

JavaScript 文件应该使用扩展名 *.js*。

# HTML图形

## HTML5 Canvas

**canvas 元素用于在网页上绘制图形。**

### 什么是 Canvas？

HTML5 的 canvas 元素使用 JavaScript 在网页上绘制图像。

画布是一个矩形区域，您可以控制其每一像素。

canvas 拥有多种绘制路径、矩形、圆形、字符以及添加图像的方法。

### 创建 Canvas 元素

向 HTML5 页面添加 canvas 元素。

规定元素的 id、宽度和高度：

```
<canvas id="myCanvas" width="200" height="100"></canvas>
```

### 通过 JavaScript 来绘制

canvas 元素本身是没有绘图能力的。所有的绘制工作必须在 JavaScript 内部完成：

```
<script type="text/javascript">
var c=document.getElementById("myCanvas");
var cxt=c.getContext("2d");
cxt.fillStyle="#FF0000";
cxt.fillRect(0,0,150,75);
</script>
```

JavaScript 使用 id 来寻找 canvas 元素：

```
var c=document.getElementById("myCanvas");
```

然后，创建 context 对象：

```
var cxt=c.getContext("2d"); 
```

getContext("2d") 对象是内建的 HTML5 对象，拥有多种绘制路径、矩形、圆形、字符以及添加图像的方法。

下面的两行代码绘制一个红色的矩形：

```
cxt.fillStyle="#FF0000";
cxt.fillRect(0,0,150,75); 
```

fillStyle 方法将其染成红色，fillRect 方法规定了形状、位置和尺寸。

### 理解坐标

上面的 fillRect 方法拥有参数 (0,0,150,75)。

意思是：在画布上绘制 150x75 的矩形，从左上角开始 (0,0)。

如下图所示，画布的 X 和 Y 坐标用于在画布上对绘画进行定位。



 

[实例：把鼠标悬停在矩形上可以看到坐标](http://www.w3school.com.cn/tiy/t.asp?f=html5_canvas_coordinates)

### 更多 Canvas 实例

下面的在 canvas 元素上进行绘画的更多实例：

**实例 - 线条**

通过指定从何处开始，在何处结束，来绘制一条线：



JavaScript 代码：

```
<script type="text/javascript">

var c=document.getElementById("myCanvas");
var cxt=c.getContext("2d");
cxt.moveTo(10,10);
cxt.lineTo(150,50);
cxt.lineTo(10,50);
cxt.stroke();

</script>
```

canvas 元素：

```
<canvas id="myCanvas" width="200" height="100" style="border:1px solid #c3c3c3;">
Your browser does not support the canvas element.
</canvas>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_canvas_line)

**实例 - 圆形**

通过规定尺寸、颜色和位置，来绘制一个圆：



JavaScript 代码：

```
<script type="text/javascript">

var c=document.getElementById("myCanvas");
var cxt=c.getContext("2d");
cxt.fillStyle="#FF0000";
cxt.beginPath();
cxt.arc(70,18,15,0,Math.PI*2,true);
cxt.closePath();
cxt.fill();

</script>
```

canvas 元素：

```
<canvas id="myCanvas" width="200" height="100" style="border:1px solid #c3c3c3;">
Your browser does not support the canvas element.
</canvas>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_canvas_circle)

**实例 - 渐变**

使用您指定的颜色来绘制渐变背景：



JavaScript 代码：

```
<script type="text/javascript">

var c=document.getElementById("myCanvas");
var cxt=c.getContext("2d");
var grd=cxt.createLinearGradient(0,0,175,50);
grd.addColorStop(0,"#FF0000");
grd.addColorStop(1,"#00FF00");
cxt.fillStyle=grd;
cxt.fillRect(0,0,175,50);

</script>
```

canvas 元素：

```
<canvas id="myCanvas" width="200" height="100" style="border:1px solid #c3c3c3;">
Your browser does not support the canvas element.
</canvas>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_canvas_gradient)

**实例 - 图像**

把一幅图像放置到画布上：



JavaScript 代码：

```
<script type="text/javascript">

var c=document.getElementById("myCanvas");
var cxt=c.getContext("2d");
var img=new Image()
img.src="flower.png"
cxt.drawImage(img,0,0);

</script>
```

canvas 元素：

```
<canvas id="myCanvas" width="200" height="100" style="border:1px solid #c3c3c3;">
Your browser does not support the canvas element.
</canvas>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_canvas_image)

### 相关页面

参考手册：[HTML 5  标签](http://www.w3school.com.cn/tags/tag_canvas.asp)

参考手册：[HTML DOM Canvas 对象](http://www.w3school.com.cn/jsref/dom_obj_canvas.asp)

## HTML5 内联 SVG

**HTML5 支持内联 SVG。**

### 什么是SVG？

- SVG 指可伸缩矢量图形 (Scalable Vector Graphics)
- SVG 用于定义用于网络的基于矢量的图形
- SVG 使用 XML 格式定义图形
- SVG 图像在放大或改变尺寸的情况下其图形质量不会有损失
- SVG 是万维网联盟的标准

### SVG 的优势

与其他图像格式相比（比如 JPEG 和 GIF），使用 SVG 的优势在于：

- SVG 图像可通过文本编辑器来创建和修改
- SVG 图像可被搜索、索引、脚本化或压缩
- SVG 是可伸缩的
- SVG 图像可在任何的分辨率下被高质量地打印
- SVG 可在图像质量不下降的情况下被放大

### 浏览器支持

Internet Explorer 9、Firefox、Opera、Chrome 以及 Safari 支持内联 SVG。

### 把 SVG 直接嵌入 HTML 页面

在 HTML5 中，您能够将 SVG 元素直接嵌入 HTML 页面中：

**实例**

```
<!DOCTYPE html>
<html>
<body>

<svg xmlns="http://www.w3.org/2000/svg" version="1.1" height="190">
  <polygon points="100,10 40,180 190,60 10,60 160,180"
  style="fill:lime;stroke:purple;stroke-width:5;fill-rule:evenodd;" />
</svg>

</body>
</html>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_svg_ex)

结果：

<svg xmlns="http://www.w3.org/2000/svg" version="1.1" height="190"><polygon points="100,10 40,180 190,60 10,60 160,180" style="fill:red;stroke:blue;stroke-width:3;fill-rule:evenodd;"></polygon></svg>

如需学习更多有关 SVG 的知识，请阅读我们的 [SVG 教程](http://www.w3school.com.cn/svg/index.asp)。

## HTML 5 Canvas vs. SVG



**Canvas 和 SVG 都允许您在浏览器中创建图形，但是它们在根本上是不同的。**

### SVG

SVG 是一种使用 XML 描述 2D 图形的语言。

SVG 基于 XML，这意味着 SVG DOM 中的每个元素都是可用的。您可以为某个元素附加 JavaScript 事件处理器。

在 SVG 中，每个被绘制的图形均被视为对象。如果 SVG 对象的属性发生变化，那么浏览器能够自动重现图形。

### Canvas

Canvas 通过 JavaScript 来绘制 2D 图形。

Canvas 是逐像素进行渲染的。

在 canvas 中，一旦图形被绘制完成，它就不会继续得到浏览器的关注。如果其位置发生变化，那么整个场景也需要重新绘制，包括任何或许已被图形覆盖的对象。

### Canvas 与 SVG 的比较

下表列出了 canvas 与 SVG 之间的一些不同之处。

### **Canvas**

- 依赖分辨率
- 不支持事件处理器
- 弱的文本渲染能力
- 能够以 .png 或 .jpg 格式保存结果图像
- 最适合图像密集型的游戏，其中的许多对象会被频繁重绘

### SVG

- 不依赖分辨率
- 支持事件处理器
- 最适合带有大型渲染区域的应用程序（比如谷歌地图）
- 复杂度高会减慢渲染速度（任何过度使用 DOM 的应用都不快）
- 不适合游戏应用

#   HTML 媒体

##   HTML 多媒体媒体

#### 

**Web 上的多媒体指的是音效、音乐、视频和动画。**

**现代网络浏览器已支持很多多媒体格式。**

### 什么是多媒体？

多媒体来自多种不同的格式。它可以是您听到或看到的任何内容，文字、图片、音乐、音效、录音、电影、动画等等。

在因特网上，您会经常发现嵌入网页中的多媒体元素，现代浏览器已支持多种多媒体格式。

在本教程中，您将了解到不同的多媒体格式，以及如何在您的网页中使用它们。

### 浏览器支持

第一款因特网浏览器只支持文本，而且即使是对文本的支持也仅限于单一字体和单一颜色。随后诞生了支持颜色、字体和文本样式的浏览器，图片支持也被加入。

不同的浏览器以不同的方式处理对音效、动画和视频的支持。某些元素能够以内联的方式处理，而某些则需要额外的插件。

您将在下面的章节学习更多有关插件的知识。

### 多媒体格式

多媒体元素（比如视频和音频）存储于媒体文件中。

确定媒体类型的最常用的方法是查看文件扩展名。当浏览器得到文件扩展名 .htm 或 .html 时，它会假定该文件是 HTML 页面。.xml 扩展名指示 XML 文件，而 .css 扩展名指示样式表。图片格式则通过 .gif 或 .jpg 来识别。

多媒体元素元素也拥有带有不同扩展名的文件格式，比如 .swf、.wmv、.mp3 以及 .mp4。

### 视频格式

MP4 格式是一种新的即将普及的因特网视频格式。HTML5 、Flash 播放器以及优酷等视频网站均支持它。

| 格式      | 文件      | 描述                                                         |
| --------- | --------- | ------------------------------------------------------------ |
| AVI       | .avi      | AVI (Audio Video Interleave) 格式是由微软开发的。所有运行 Windows 的计算机都支持 AVI 格式。它是因特网上很常见的格式，但非 Windows 计算机并不总是能够播放。 |
| WMV       | .wmv      | Windows Media 格式是由微软开发的。Windows Media 在因特网上很常见，但是如果未安装额外的（免费）组件，就无法播放 Windows Media 电影。一些后期的 Windows Media 电影在所有非 Windows 计算机上都无法播放，因为没有合适的播放器。 |
| MPEG      | .mpg.mpeg | MPEG (Moving Pictures Expert Group) 格式是因特网上最流行的格式。它是跨平台的，得到了所有最流行的浏览器的支持。 |
| QuickTime | .mov      | QuickTime 格式是由苹果公司开发的。QuickTime 是因特网上常见的格式，但是 QuickTime 电影不能在没有安装额外的（免费）组件的 Windows 计算机上播放。 |
| RealVideo | .rm.ram   | RealVideo 格式是由 Real Media 针对因特网开发的。该格式允许低带宽条件下（在线视频、网络电视）的视频流。由于是低带宽优先的，质量常会降低。 |
| Flash     | .swf.flv  | Flash (Shockwave) 格式是由 Macromedia 开发的。Shockwave 格式需要额外的组件来播放。但是该组件会预装到 Firefox 或 IE 之类的浏览器上。 |
| Mpeg-4    | .mp4      | Mpeg-4 (with H.264 video compression) 是一种针对因特网的新格式。事实上，YouTube 推荐使用 MP4。YouTube 接收多种格式，然后全部转换为 .flv 或 .mp4 以供分发。越来越多的视频发布者转到 MP4，将其作为 Flash 播放器和 HTML5 的因特网共享格式。 |

### 声音格式

| 格式      | 文件      | 描述                                                         |
| --------- | --------- | ------------------------------------------------------------ |
| MIDI      | .mid.midi | MIDI (Musical Instrument Digital Interface) 是一种针对电子音乐设备（比如合成器和声卡）的格式。MIDI 文件不含有声音，但包含可被电子产品（比如声卡）播放的数字音乐指令。[点击这里播放 The Beatles](http://www.w3school.com.cn/i/beatles.mid)。因为 MIDI 格式仅包含指令，所以 MIDI 文件极其小巧。上面的例子只有 23k 的大小，但却能播放将近 5 分钟。MIDI 得到了广泛的平台上的大量软件的支持。大多数流行的网络浏览器都支持 MIDI。 |
| RealAudio | .rm.ram   | RealAudio 格式是由 Real Media 针对因特网开发的。该格式也支持视频。该格式允许低带宽条件下的音频流（在线音乐、网络音乐）。由于是低带宽优先的，质量常会降低。 |
| Wave      | .wav      | Wave (waveform) 格式是由 IBM 和微软开发的。所有运行 Windows 的计算机和所有网络浏览器（除了 Google Chrome）都支持它。 |
| WMA       | .wma      | WMA 格式 (Windows Media Audio)，质量优于 MP3，兼容大多数播放器，除了 iPod。WMA 文件可作为连续的数据流来传输，这使它对于网络电台或在线音乐很实用。 |
| MP3       | .mp3.mpga | MP3 文件实际上是 MPEG 文件的声音部分。MPEG 格式最初是由运动图像专家组开发的。MP3 是其中最受欢迎的针对音乐的声音格式。期待未来的软件系统都支持它。 |

### 使用哪种格式？

WAVE 是因特网上最受欢迎的*无压缩*声音格式，所有流行的浏览器都支持它。如果您需要未经压缩的声音（音乐或演讲），那么您应该使用 WAVE 格式。

MP3 是最新的*压缩*录制音乐格式。MP3 这个术语已经成为数字音乐的代名词。如果您的网址从事录制音乐，那么 MP3 是一个选项。

## HTML Object 元素

**<object> 的作用是支持 HTML 助手（插件）。**

### HTML 助手（插件）

辅助应用程序（helper application）是可由浏览器启动的程序。辅助应用程序也称为插件。

辅助程序可用于播放音频和视频（以及其他）。辅助程序是使用 <object> 标签来加载的。

使用辅助程序播放视频和音频的一个优势是，您能够允许用户来控制部分或全部播放设置。

大多数辅助应用程序允许对音量设置和播放功能（比如后退、暂停、停止和播放）的手工（或程序的）控制。

### 在 HTML 中播放视频的最好方式？

如需了解在 HTML 中包含音视频的最好方法，请参阅下一章节。

### 使用 QuickTime 来播放 Wave 音频

实例

```
<object width="420" height="360"
classid="clsid:02BF25D5-8C17-4B23-BC80-D3488ABDDC6B"
codebase="http://www.apple.com/qtactivex/qtplugin.cab">
<param name="src" value="bird.wav" />
<param name="controller" value="true" />
</object>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_object_qtaudio)

### 使用 QuickTime 来播放 MP4 视频

实例

```
<object width="420" height="360"
classid="clsid:02BF25D5-8C17-4B23-BC80-D3488ABDDC6B"
codebase="http://www.apple.com/qtactivex/qtplugin.cab">
<param name="src" value="movie.mp4" />
<param name="controller" value="true" />
</object>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_object_qtvideo)

### 使用 Flash 来播放 SWF 视频

实例

```
<object width="400" height="40"
classid="clsid:d27cdb6e-ae6d-11cf-96b8-444553540000"
codebase="http://fpdownload.macromedia.com/
pub/shockwave/cabs/flash/swflash.cab#version=8,0,0,0">
<param name="SRC" value="bookmark.swf">
<embed src="bookmark.swf" width="400" height="40"></embed>
</object>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_object_flash)

### 使用 Windows Media Player 来播放 WMV 影片

下面的例子展示用于播放 Windows 媒体文件的推荐代码：

实例

```
<object width="100%" height="100%"
type="video/x-ms-asf" url="3d.wmv" data="3d.wmv"
classid="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
<param name="url" value="3d.wmv">
<param name="filename" value="3d.wmv">
<param name="autostart" value="1">
<param name="uiMode" value="full" />
<param name="autosize" value="1">
<param name="playcount" value="1">
<embed type="application/x-mplayer2" src="3d.wmv" width="100%"
 height="100%" autostart="true" showcontrols="true" 
pluginspage="http://www.microsoft.com/Windows/MediaPlayer/"></embed>
</object>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_object_mplayer)

## HTML 音频

**在 HTML 中播放声音的方法有很多种。**

### 问题，问题，以及解决方法

在 HTML 中播放音频并不容易！

您需要谙熟大量技巧，以确保您的音频文件在所有浏览器中（Internet Explorer, Chrome, Firefox, Safari, Opera）和所有硬件上（PC, Mac , iPad, iPhone）都能够播放。

在本章，W3School 为您总结了问题和解决方法。

### 使用插件

浏览器插件是一种扩展浏览器标准功能的小型计算机程序。

插件有很多用途：播放音乐、显示地图、验证银行账号，控制输入等等。

可使用 <object> 或 <embed> 标签来将插件添加到 HTML 页面。

这些标签定义资源（通常非 HTML 资源）的容器，根据类型，它们即会由浏览器显示，也会由外部插件显示。

## 使用 &lt;embed> 元素

<embed> 标签定义外部（非 HTML）内容的容器。（这是一个 HTML5 标签，在 HTML4 中是非法的，但是所有浏览器中都有效）。

下面的代码片段能够显示嵌入网页中的 MP3 文件：

**实例**

```
<embed height="100" width="100" src="song.mp3" />
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_audio_embed)

**问题：**

- <embed> 标签在 HTML 4 中是无效的。页面无法通过 HTML 4 验证。
- 不同的浏览器对音频格式的支持也不同。
- 如果浏览器不支持该文件格式，没有插件的话就无法播放该音频。
- 如果用户的计算机未安装插件，无法播放音频。
- 如果把该文件转换为其他格式，仍然无法在所有浏览器中播放。

注释：使用 <!DOCTYPE html> (HTML5) 解决验证问题。

### 使用 &lt;object> 元素

<object tag> 标签也可以定义外部（非 HTML）内容的容器。

下面的代码片段能够显示嵌入网页中的 MP3 文件：

**实例**

```
<object height="100" width="100" data="song.mp3"></object>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_audio_object)

**问题**：

- 不同的浏览器对音频格式的支持也不同。
- 如果浏览器不支持该文件格式，没有插件的话就无法播放该音频。
- 如果用户的计算机未安装插件，无法播放音频。
- 如果把该文件转换为其他格式，仍然无法在所有浏览器中播放。

## 使用 HTML5 &lt;audio> 元素

<audio> 元素是一个 HTML5 元素，在 HTML 4 中是非法的，但在所有浏览器中都有效。

**实例**

```
<audio controls="controls">
  <source src="song.mp3" type="audio/mp3" />
  <source src="song.ogg" type="audio/ogg" />
Your browser does not support this audio format.
</audio>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_audio_html5)

上面的例子使用了一个 mp3 文件，这样它在 Internet Explorer、Chrome 以及 Safari 中是有效的。

为了使这段音频在 Firefox 和 Opera 中同样有效，添加了一个 ogg 类型的文件。如果失败，会显示错误消息。

**问题：**

- <audio> 标签在 HTML 4 中是无效的。您的页面无法通过 HTML 4 验证。
- 您必须把音频文件转换为不同的格式。
- <audio> 元素在老式浏览器中不起作用。

注释：使用 <!DOCTYPE html> (HTML5) 解决验证问题。

### 最好的 HTML 解决方法

**实例**

```
<audio controls="controls" height="100" width="100">
  <source src="song.mp3" type="audio/mp3" />
  <source src="song.ogg" type="audio/ogg" />
<embed height="100" width="100" src="song.mp3" />
</audio>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_audio_all)

上面的例子使用了两个不同的音频格式。HTML5 <audio> 元素会尝试以 mp3 或 ogg 来播放音频。如果失败，代码将回退尝试 <embed> 元素。

**问题**：

- 您必须把音频转换为不同的格式。
- <audio> 元素无法通过 HTML 4 和 XHTML 验证。
- <embed> 元素无法通过 HTML 4 和 XHTML 验证。
- <embed> 元素无法回退来显示错误消息。

注释：使用 <!DOCTYPE html> (HTML5) 解决验证问题。

### 向网站添加音频的最简单方法

向网页添加音频的最简单的方法是什么？

雅虎的媒体播放器绝对算其中之一。

使用雅虎媒体播放器是一个不同的途径。您只需简单地让雅虎来完成歌曲播放的工作就好了。

它能播放 mp3 以及一系列其他格式。通过一行简单的代码，您就可以把它添加到网页中，轻松地将 HTML 页面转变为专业的播放列表。

### 雅虎媒体播放器

**实例**

```
<a href="song.mp3">Play Sound</a>

<script type="text/javascript" src="http://mediaplayer.yahoo.com/js">
</script>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_audio_yahoo)

使用雅虎播放器是免费的。如需使用它，您需要把这段 JavaScript 插入网页底部：

```
<script type="text/javascript" src="http://mediaplayer.yahoo.com/js"></script>
```

然后只需简单地把 MP3 文件链接到您的 HTML 中，JavaScript 会自动地为每首歌创建播放按钮：

```
<a href="song1.mp3">Play Song 1</a>
<a href="song2.mp3">Play Song 2</a>
...
...
...
```

雅虎媒体播放器为您的用户提供的是一个小型的播放按钮，而不是完整的播放器。不过，当您点击该按钮，会弹出完整的播放器。

请注意，这个播放器始终停靠在窗框底部。只需点击它，就可将其滑出。

### 使用超链接

如果网页包含指向媒体文件的超链接，大多数浏览器会使用“辅助应用程序”来播放文件。

以下代码片段显示指向 mp3 文件的链接。如果用户点击该链接，浏览器会启动“辅助应用程序”来播放该文件：

**实例**

```
<a href="song.mp3">Play the sound</a>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_audio_link)

### 内联的声音

当您在网页中包含声音，或者作为网页的组成部分时，它被称为内联声音。

如果您打算在 web 应用程序中使用内联声音，您需要意识到很多人都觉得内联声音令人恼火。同时请注意，用户可能已经关闭了浏览器中的内联声音选项。

我们最好的建议是只在用户希望听到内联声音的地方包含它们。一个正面的例子是，在用户需要听到录音并点击某个链接时，会打开页面然后播放录音。

### HTML 4.01 多媒体标签

| 标签                                                     | 描述                                         |
| -------------------------------------------------------- | -------------------------------------------- |
| applet                                                   | 不赞成。定义内嵌 applet。                    |
| embed                                                    | HTML4 中不赞成，HTML5 中允许。定义内嵌对象。 |
| [object](http://www.w3school.com.cn/tags/tag_object.asp) | 定义内嵌对象。                               |
| [param](http://www.w3school.com.cn/tags/tag_param.asp)   | 定义对象的参数。                             |

### HTML 5 多媒体标签

| 标签                                                   | 描述                                 |
| ------------------------------------------------------ | ------------------------------------ |
| [audio](http://www.w3school.com.cn/tags/tag_audio.asp) | 标签定义声音，比如音乐或其他音频流。 |
| [embed](http://www.w3school.com.cn/tags/tag_embed.asp) | 标签定义嵌入的内容，比如插件。       |

## HTML 视频

**在 HTML 中播放视频的方法有很多种。**

**实例**

```
<video width="320" height="240" controls="controls">
  <source src="movie.mp4" type="video/mp4" />
  <source src="movie.ogg" type="video/ogg" />
  <source src="movie.webm" type="video/webm" />
  <object data="movie.mp4" width="320" height="240">
    <embed src="movie.swf" width="320" height="240" />
  </object>
</video>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_video)

### 问题，问题，以及解决方法

在 HTML 中播放视频并不容易！

您需要谙熟大量技巧，以确保您的视频文件在所有浏览器中（Internet Explorer, Chrome, Firefox, Safari, Opera）和所有硬件上（PC, Mac , iPad, iPhone）都能够播放。

在本章，W3School 为您总结了问题和解决方法。

### 使用 &lt;embed> 标签

<embed> 标签的作用是在 HTML 页面中嵌入多媒体元素。

下面的 HTML 代码显示嵌入网页的 Flash 视频：

**实例**

```
<embed src="movie.swf" height="200" width="200"/>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_video_embed)

**问题**

- HTML4 无法识别 <embed> 标签。您的页面无法通过验证。
- 如果浏览器不支持 Flash，那么视频将无法播放
- iPad 和 iPhone 不能显示 Flash 视频。
- 如果您将视频转换为其他格式，那么它仍然不能在所有浏览器中播放。

### 使用 &lt;object> 标签

<object> 标签的作用是在 HTML 页面中嵌入多媒体元素。

下面的 HTML 片段显示嵌入网页的一段 Flash 视频：

**实例**

```
<object data="movie.swf" height="200" width="200"/>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_video_object)

**问题**

- 如果浏览器不支持 Flash，将无法播放视频。
- iPad 和 iPhone 不能显示 Flash 视频。
- 如果您将视频转换为其他格式，那么它仍然不能在所有浏览器中播放。

### 使用 &lt;video> 标签

&lt;video> 是 HTML 5 中的新标签。

&lt;video> 标签的作用是在 HTML 页面中嵌入视频元素。

以下 HTML 片段会显示一段嵌入网页的 ogg、mp4 或 webm 格式的视频：

**实例**

```
<video width="320" height="240" controls="controls">
  <source src="movie.mp4" type="video/mp4" />
  <source src="movie.ogg" type="video/ogg" />
  <source src="movie.webm" type="video/webm" />
Your browser does not support the video tag.
</video>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_video_html5)

**问题**

- 您必须把视频转换为很多不同的格式。
- &lt;video> 元素在老式浏览器中无效。
- &lt;video> 元素无法通过 HTML 4 和 XHTML 验证。

### 最好的 HTML 解决方法

HTML 5 + <object> + <embed>

```
<video width="320" height="240" controls="controls">
  <source src="movie.mp4" type="video/mp4" />
  <source src="movie.ogg" type="video/ogg" />
  <source src="movie.webm" type="video/webm" />
  <object data="movie.mp4" width="320" height="240">
    <embed src="movie.swf" width="320" height="240" />
  </object>
</video>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_video)

上例中使用了 4 中不同的视频格式。HTML 5 <video> 元素会尝试播放以 mp4、ogg 或 webm 格式中的一种来播放视频。如果均失败，则回退到 <embed> 元素。

**问题**

- 您必须把视频转换为很多不同的格式
- &lt;video> 元素无法通过 HTML 4 和 XHTML 验证。
- &lt;embed> 元素无法通过 HTML 4 和 XHTML 验证。

注释：使用 <!DOCTYPE html> (HTML5) 解决验证问题。

### 优酷解决方案

在 HTML 中显示视频的最简单的方法是使用优酷等视频网站。

如果您希望在网页中播放视频，那么您可以把视频上传到优酷等视频网站，然后在您的网页中插入 HTML 代码即可播放视频：

```
<embed src="http://player.youku.com/player.php/sid/XMzI2NTc4NTMy/v.swf" 
width="480" height="400" 
type="application/x-shockwave-flash">
</embed>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_video_youku)

### 使用超链接

如果网页包含指向媒体文件的超链接，大多数浏览器会使用“辅助应用程序”来播放文件。

以下代码片段显示指向 AVI 文件的链接。如果用户点击该链接，浏览器会启动“辅助应用程序”，比如 Windows Media Player 来播放这个 AVI 文件：

**实例**

```
<a href="movie.swf">Play a video file</a>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_video_link)

### 关于内联视频的一段注释

当视频被包含在网页中时，它被称为内联视频。

如果您打算在 web 应用程序中使用内联视频，您需要意识到很多人都觉得内联视频令人恼火。

同时请注意，用户可能已经关闭了浏览器中的内联视频选项。

我们最好的建议是只在用户希望看到内联视频的地方包含它们。一个正面的例子是，在用户需要看到视频并点击某个链接时，会打开页面然后播放视频。

### HTML 4.01 多媒体标签

| 标签                                                     | 描述                                   |
| -------------------------------------------------------- | -------------------------------------- |
| [applet](http://www.w3school.com.cn/tags/tag_applet.asp) | 不赞成。定义内嵌 applet。              |
| embed                                                    | 不赞成。定义内嵌对象。（HTML5 中允许） |
| [object](http://www.w3school.com.cn/tags/tag_object.asp) | 定义内嵌对象。                         |
| [param](http://www.w3school.com.cn/tags/tag_param.asp)   | 定义对象的参数。                       |

### HTML 5 多媒体标签

| 标签                                                   | 描述                                 |
| ------------------------------------------------------ | ------------------------------------ |
| [video](http://www.w3school.com.cn/tags/tag_video.asp) | 标签定义声音，比如音乐或其他音频流。 |
| [embed](http://www.w3school.com.cn/tags/tag_embed.asp) | 标签定义嵌入的内容，比如插件。       |

# HTML API

## HTML5 地理定位

**HTML5 Geolocation（地理定位）用于定位用户的位置。**

[亲自试一试：在谷歌地图上显示您的位置](http://www.w3school.com.cn/tiy/t.asp?f=html5_geolocation_map_script)

### 定位用户的位置

HTML5 Geolocation API 用于获得用户的地理位置。

鉴于该特性可能侵犯用户的隐私，除非用户同意，否则用户位置信息是不可用的。

### 浏览器支持

Internet Explorer 9、Firefox、Chrome、Safari 以及 Opera 支持地理定位。

注释：对于拥有 GPS 的设备，比如 iPhone，地理定位更加精确。

### HTML5 - 使用地理定位

请使用 getCurrentPosition() 方法来获得用户的位置。

下例是一个简单的地理定位实例，可返回用户位置的经度和纬度。

**实例**

```
<script>
var x=document.getElementById("demo");
function getLocation()
  {
  if (navigator.geolocation)
    {
    navigator.geolocation.getCurrentPosition(showPosition);
    }
  else{x.innerHTML="Geolocation is not supported by this browser.";}
  }
function showPosition(position)
  {
  x.innerHTML="Latitude: " + position.coords.latitude +
  "<br />Longitude: " + position.coords.longitude;
  }
</script>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_geolocation)

例子解释：

- 检测是否支持地理定位
- 如果支持，则运行 getCurrentPosition() 方法。如果不支持，则向用户显示一段消息。
- 如果getCurrentPosition()运行成功，则向参数showPosition中规定的函数返回一个coordinates对象
- showPosition() 函数获得并显示经度和纬度

上面的例子是一个非常基础的地理定位脚本，不含错误处理。

### 处理错误和拒绝

getCurrentPosition() 方法的第二个参数用于处理错误。它规定当获取用户位置失败时运行的函数：

**实例**

```
function showError(error)
  {
  switch(error.code)
    {
    case error.PERMISSION_DENIED:
      x.innerHTML="User denied the request for Geolocation."
      break;
    case error.POSITION_UNAVAILABLE:
      x.innerHTML="Location information is unavailable."
      break;
    case error.TIMEOUT:
      x.innerHTML="The request to get user location timed out."
      break;
    case error.UNKNOWN_ERROR:
      x.innerHTML="An unknown error occurred."
      break;
    }
  }
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_geolocation_error)

错误代码：

- Permission denied - 用户不允许地理定位
- Position unavailable - 无法获取当前位置
- Timeout - 操作超时

### 在地图中显示结果

如需在地图中显示结果，您需要访问可使用经纬度的地图服务，比如谷歌地图或百度地图：

**实例**

```
function showPosition(position)
{
var latlon=position.coords.latitude+","+position.coords.longitude;

var img_url="http://maps.googleapis.com/maps/api/staticmap?center="
+latlon+"&zoom=14&size=400x300&sensor=false";

document.getElementById("mapholder").innerHTML="<img src='"+img_url+"' />";
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_geolocation_map)

在上例中，我们使用返回的经纬度数据在谷歌地图中显示位置（使用静态图像）。

[谷歌地图脚本](http://www.w3school.com.cn/tiy/t.asp?f=html5_geolocation_map_script)

上面的链接向您演示如何使用脚本来显示带有标记、缩放和拖曳选项的交互式地图。

### 给定位置的信息

本页演示的是如何在地图上显示用户的位置。不过，地理定位对于给定位置的信息同样很有用处。

案例：

- 更新本地信息
- 显示用户周围的兴趣点
- 交互式车载导航系统 (GPS)

### getCurrentPosition() 方法 - 返回数据

若成功，则 getCurrentPosition() 方法返回对象。始终会返回 latitude、longitude 以及 accuracy 属性。如果可用，则会返回其他下面的属性。

| 属性                    | 描述                   |
| ----------------------- | ---------------------- |
| coords.latitude         | 十进制数的纬度         |
| coords.longitude        | 十进制数的经度         |
| coords.accuracy         | 位置精度               |
| coords.altitude         | 海拔，海平面以上以米计 |
| coords.altitudeAccuracy | 位置的海拔精度         |
| coords.heading          | 方向，从正北开始以度计 |
| coords.speed            | 速度，以米/每秒计      |
| timestamp               | 响应的日期/时间        |

### Geolocation 对象 - 其他有趣的方法

watchPosition() - 返回用户的当前位置，并继续返回用户移动时的更新位置（就像汽车上的 GPS）。

clearWatch() - 停止 watchPosition() 方法

下面的例子展示 watchPosition() 方法。您需要一台精确的 GPS 设备来测试该例（比如 iPhone）：

**实例**

```
<script>
var x=document.getElementById("demo");
function getLocation()
  {
  if (navigator.geolocation)
    {
    navigator.geolocation.watchPosition(showPosition);
    }
  else{x.innerHTML="Geolocation is not supported by this browser.";}
  }
function showPosition(position)
  {
  x.innerHTML="Latitude: " + position.coords.latitude +
  "<br />Longitude: " + position.coords.longitude;
  }
</script>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_geolocation_watchposition)

## HTML5 拖放

[HTML5 拖放](http://www.w3school.com.cn/html/html5_draganddrop.asp)

![img](http://www.w3school.com.cn/i/eg_dragdrop_w3school.gif)



请把 W3School 图片拖到矩形中。

### 拖放

拖放（Drag 和 Drop）是很常见的特性。它指的是您抓取某物并拖入不同的位置。

拖放是 HTML5 标准的组成部分：任何元素都是可拖放的。

### 浏览器支持

表格中的数字指示了完全支持拖放的首个浏览器版本。

| API  |      |      |      |      |      |
| ---- | ---- | ---- | ---- | ---- | ---- |
| 拖放 | 4.0  | 9.0  | 3.5  | 6.0  | 12.0 |

### HTML 拖放实例

下列是关于拖放的简单例子：

**实例**

```
<!DOCTYPE HTML>
<html>
<head>
<script>
function allowDrop(ev) {
    ev.preventDefault();
}

function drag(ev) {
    ev.dataTransfer.setData("text", ev.target.id);
}

function drop(ev) {
    ev.preventDefault();
    var data = ev.dataTransfer.getData("text");
    ev.target.appendChild(document.getElementById(data));
}
</script>
</head>
<body>

<div id="div1" ondrop="drop(event)" ondragover="allowDrop(event)"></div>

<img id="drag1" src="img_logo.gif" draggable="true" ondragstart="drag(event)" width="336" height="69">

</body>
</html>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_draganddrop)

它也许看上去有点复杂，不过让我们研究一下拖放事件的所有不同部分。

### 把元素设置为可拖放

首先：为了把一个元素设置为可拖放，请把 draggable 属性设置为 true：

```
<img draggable="true">
```

### 拖放的内容 - ondragstart 和 setData()

然后，规定当元素被拖动时发生的事情。

在上面的例子中，ondragstart 属性调用了一个 drag(event) 函数，规定拖动什么数据。

dataTransfer.setData() 方法设置被拖动数据的数据类型和值：

```
function drag(ev) {
    ev.dataTransfer.setData("text", ev.target.id);
}
```

在本例中，数据类型是 "text"，而值是这个可拖动元素的 id ("drag1")。

### 拖到何处 - ondragover

ondragover 事件规定被拖动的数据能够被放置到何处。

默认地，数据/元素无法被放置到其他元素中。为了实现拖放，我们必须阻止元素的这种默认的处理方式。

这个任务由 ondragover 事件的 event.preventDefault() 方法完成：

```
event.preventDefault()
```

### 进行放置 - ondrop

当放开被拖数据时，会发生 drop 事件。

在上面的例子中，ondrop 属性调用了一个函数，drop(event)：

```
function drop(ev) {
    ev.preventDefault();
    var data = ev.dataTransfer.getData("text");
    ev.target.appendChild(document.getElementById(data));
}
```

### 代码解释：

- 调用 preventDefault() 来阻止数据的浏览器默认处理方式（drop 事件的默认行为是以链接形式打开）
- 通过 dataTransfer.getData() 方法获得被拖的数据。该方法将返回在 setData() 方法中设置为相同类型的任何数据
- 被拖数据是被拖元素的 id ("drag1")
- 把被拖元素追加到放置元素中

### 更多实例

### 来回拖放图片

如何在两个 <div> 元素之间来回拖放图像：

![img](http://www.w3school.com.cn/i/eg_dragdrop_w3school.gif)



请把 W3School 图片拖到矩形中。

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_draganddrop2)

##   HTML 本地存储

**HTML 本地存储：优于 cookies。**

### 什么是 HTML 本地存储？

通过本地存储（Local Storage），web 应用程序能够在用户浏览器中对数据进行本地的存储。

在 HTML5 之前，应用程序数据只能存储在 cookie 中，包括每个服务器请求。本地存储则更安全，并且可在不影响网站性能的前提下将大量数据存储于本地。

与 cookie 不同，存储限制要大得多（至少5MB），并且信息不会被传输到服务器。

本地存储经由起源地（origin）（经由域和协议）。所有页面，从起源地，能够存储和访问相同的数据。

### 浏览器支持

表格中的数组指示了完全支持本地存储的首个浏览器版本。

| API         |      |      |      |      |      |
| ----------- | ---- | ---- | ---- | ---- | ---- |
| Web Storage | 4.0  | 8.0  | 3.5  | 4.0  | 11.5 |

### HTML 本地存储对象

HTML 本地存储提供了两个在客户端存储数据的对象：

- window.localStorage - 存储没有截止日期的数据
- window.sessionStorage - 针对一个 session 来存储数据（当关闭浏览器标签页时数据会丢失）

在使用本地存储时，请检测 localStorage 和 sessionStorage 的浏览器支持：

```
if (typeof(Storage) !== "undefined") {
    // 针对 localStorage/sessionStorage 的代码
} else {
    // 抱歉！不支持 Web Storage ..
}
```

### localStorage 对象

localStorage 对象存储的是没有截止日期的数据。当浏览器被关闭时数据不会被删除，在下一天、周或年中，都是可用的。

**实例**

```
// 存储
localStorage.setItem("lastname", "Gates");
// 取回
document.getElementById("result").innerHTML = localStorage.getItem("lastname");
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_webstorage_local)

### 实例解释：

- 创建 localStorage 名称/值对，其中：name="lastname"，value="Gates"
- 取回 "lastname" 的值，并把它插到 id="result" 的元素中

上例也可这样写：

```
// 存储
localStorage.lastname = "Gates";
// 取回
document.getElementById("result").innerHTML = localStorage.lastname;
```

删除 "lastname" localStorage 项目的语法如下：

```
localStorage.removeItem("lastname");
```

注释：名称/值对始终存储为字符串。如果需要请记得把它们转换为其他格式！

下面的例子对用户点击按钮的次数进行计数。在代码中，值字符串被转换为数值，依次对计数进行递增：

**实例**

```
if (localStorage.clickcount) {
    localStorage.clickcount = Number(localStorage.clickcount) + 1;
} else {
    localStorage.clickcount = 1;
}
document.getElementById("result").innerHTML = "您已经点击这个按钮 " +
localStorage.clickcount + " 次。";
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_webstorage_local_clickcount)

### sessionStorage 对象

sessionStorage 对象等同 localStorage 对象，不同之处在于只对一个 session 存储数据。如果用户关闭具体的浏览器标签页，数据也会被删除。

下例在当前 session 中对用户点击按钮进行计数：

**实例**

```
if (sessionStorage.clickcount) {
    sessionStorage.clickcount = Number(sessionStorage.clickcount) + 1;
} else {
    sessionStorage.clickcount = 1;
}
document.getElementById("result").innerHTML = "在本 session 中，您已经点击这个按钮 " +
sessionStorage.clickcount + " 次。";
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_webstorage_session)

##   HTML5 应用程序缓存

**使用应用程序缓存，通过创建 cache manifest 文件，可轻松创建 web 应用的离线版本。**

### 什么是应用程序缓存？

HTML5 引入了应用程序缓存（Application Cache），这意味着可对 web 应用进行缓存，并可在没有因特网连接时进行访问。

应用程序缓存为应用带来三个优势：

1. 离线浏览 - 用户可在应用离线时使用它们
2. 速度 - 已缓存资源加载得更快
3. 减少服务器负载 - 浏览器将只从服务器下载更新过或更改过的资源

### 浏览器支持

表格中的数字指示完全支持应用程序缓存的首个浏览器版本。

| API               |      |      |      |      |      |
| ----------------- | ---- | ---- | ---- | ---- | ---- |
| Application Cache | 4.0  | 10.0 | 3.5  | 4.0  | 11.5 |

### HTML Cache Manifest 实例

下例展示了带有 cache manifest 的 HTML 文档（供离线浏览）：

**实例**

```
<!DOCTYPE HTML>
<html manifest="demo.appcache">

<body>
文档内容 ......
</body>

</html>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_html_manifest)

### Cache Manifest 基础

如需启用应用程序缓存，请在文档的 <html> 标签中包含 manifest 属性：

```
<!DOCTYPE HTML>
<html manifest="demo.appcache">
...
</html>
```

每个指定了 manifest 的页面在用户对其访问时都会被缓存。如果未指定 manifest 属性，则页面不会被缓存（除非在 manifest 文件中直接指定了该页面）。

manifest 文件的建议文件扩展名是：".appcache"。

注意：manifest 文件需要设置正确的 MIME-type，即 "text/cache-manifest"。必须在 web 服务器上进行配置。

### Manifest 文件

manifest 文件是简单的文本文件，它告知浏览器被缓存的内容（以及不缓存的内容）。

manifest 文件有三个部分：

- CACHE MANIFEST - 在此标题下列出的文件将在首次下载后进行缓存
- NETWORK - 在此标题下列出的文件需要与服务器的连接，且不会被缓存
- FALLBACK - 在此标题下列出的文件规定当页面无法访问时的回退页面（比如 404 页面）

### CACHE MANIFEST

第一行，CACHE MANIFEST，是必需的：

```
CACHE MANIFEST
/theme.css
/logo.gif
/main.js
```

上面的 manifest 文件列出了三个资源：一个 CSS 文件，一个 GIF 图像，以及一个 JavaScript 文件。当 manifest 文件被加载后，浏览器会从网站的根目录下载这三个文件。然后，无论用户何时与因特网断开连接，这些资源依然可用。

### NETWORK

下面的 NETWORK 部分规定文件 "login.php" 永远不会被缓存，且离线时是不可用的：

```
NETWORK:
login.asp
```

可以使用星号来指示所有其他其他资源/文件都需要因特网连接：

```
NETWORK:
*

FALLBACK
```

下面的 FALLBACK 部分规定如果无法建立因特网连接，则用 "offline.html" 替代 /html/ 目录中的所有文件：

```
FALLBACK:
/html/ /offline.html
```

注释：第一个 URI 是资源，第二个是替补。

### 更新缓存

一旦应用被缓存，它就会保持缓存直到发生下列情况：

- 用户清空浏览器缓存
- manifest 文件被修改（参阅下面的提示）
- 由程序来更新应用缓存

### 实例 - 完整的 Cache Manifest 文件

```
CACHE MANIFEST
# 2012-02-21 v1.0.0
/theme.css
/logo.gif
/main.js

NETWORK:
login.asp

FALLBACK:
/html/ /offline.html
```

提示：以 "#" 开头的是注释行，但也可满足其他用途。应用的缓存只会在其 manifest 文件改变时被更新。如果您编辑了一幅图像，或者修改了一个 JavaScript 函数，这些改变都不会被重新缓存。更新注释行中的日期和版本号是一种使浏览器重新缓存文件的办法。

### 关于应用程序缓存的注意事项

请留心缓存的内容。

一旦文件被缓存，则浏览器会继续展示已缓存的版本，即使您修改了服务器上的文件。为了确保浏览器更新缓存，您需要更新 manifest 文件。

注释：浏览器对缓存数据的容量限制可能不太一样（某些浏览器的限制是每个站点 5MB）。

##   HTML Web Workers

**Web worker 是运行在后台的 JavaScript，不会影响页面的性能。**

### 什么是 Web Worker？

当在 HTML 页面中执行脚本时，页面是不可响应的，直到脚本已完成。

Web worker 是运行在后台的 JavaScript，独立于其他脚本，不会影响页面的性能。您可以继续做任何愿意做的事情：点击、选取内容等等，而此时 web worker 运行在后台。

### 浏览器支持

表格中的数字指示完全支持 Web Worker 的首个浏览器版本。

| API        |      |      |      |      |      |
| ---------- | ---- | ---- | ---- | ---- | ---- |
| Web Worker | 4.0  | 10.0 | 3.5  | 4.0  | 11.5 |

### HTML Web Workers 实例

下面的例子创建了一个简单的 web worker，在后台计数：

计数：

启动 Worker 停止 Worker

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_webworker)

### 检测 Web Worker 支持

在创建 web worker 之前，请检测用户浏览器是否支持它：

```
if (typeof(Worker) !== "undefined") {
    // 是的！支持 Web worker！
    // 一些代码.....
} else {
    // 抱歉！不支持 Web Worker！
}
```

### 创建 Web Worker 文件

现在，让我们在一个外部 JavaScript 文件中创建我们的 web worker。

在此处，我们创建了计数脚本。该脚本存储于 "demo_workers.js" 文件中：

```
var i = 0;

function timedCount() {
    i = i + 1;
    postMessage(i);
    setTimeout("timedCount()",500);
}

timedCount();
```

以上代码中重要的部分是 postMessage() 方法 - 它用于向 HTML 页面传回一段消息。

注释: web worker 通常不用于如此简单的脚本，而是用于更耗费 CPU 资源的任务。

### 创建 Web Worker 对象

现在我们已经有了 web worker 文件，我们需要从 HTML 页面调用它。

下面的代码行检测是否存在 worker，如果不存在，- 它会创建一个新的 web worker 对象，然后运行 "demo_workers.js" 中的代码：

```
if (typeof(w) == "undefined") {
    w = new Worker("demo_workers.js");
}
```

然后我们就可以从 web worker 发生和接收消息了。

向 web worker 添加一个 "onmessage" 事件监听器：

```
w.onmessage = function(event){
    document.getElementById("result").innerHTML = event.data;
};
```

当 web worker 传送消息时，会执行事件监听器中的代码。来自 web worker 的数据会存储于 event.data 中。

### 终止 Web Worker

当创建 web worker 后，它会继续监听消息（即使在外部脚本完成后）直到其被终止为止。

如需终止 web worker，并释放浏览器/计算机资源，请使用 terminate() 方法：

```
w.terminate();
```

### 复用 Web Worker

如果您把 worker 变量设置为 undefined，在其被终止后，可以重复使用该代码：

```
w = undefined;
```

### 完整的 Web Worker 实例代码

我们已经看到了 .js 文件中的 Worker 代码。下面是 HTML 页面的代码：

**实例**

```
<!DOCTYPE html>
<html>
<body>

<p>Count numbers: <output id="result"></output></p>
<button onclick="startWorker()">Start Worker</button> 
<button onclick="stopWorker()">Stop Worker</button>
<br><br>

<script>
var w;

function startWorker() {
    if(typeof(Worker) !== "undefined") {
        if(typeof(w) == "undefined") {
            w = new Worker("demo_workers.js");
        }
        w.onmessage = function(event) {
            document.getElementById("result").innerHTML = event.data;
        };
    } else {
        document.getElementById("result").innerHTML = "Sorry! No Web Worker support.";
    }
}

function stopWorker() { 
    w.terminate();
    w = undefined;
}
</script>

</body>
</html>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_webworker)

### Web Worker 和 DOM

由于 web worker 位于外部文件中，它们无法访问下例 JavaScript 对象：

- window 对象
- document 对象
- parent 对象
  

## HTML Server-Sent 事件

**Server-Sent 事件允许网页从服务器获得更新。**

### Server-Sent 事件 - One Way Messaging

Server-Sent 事件指的是网页自动从服务器获得更新。

以前也可能做到这一点，前提是网页不得不询问是否有可用的更新。通过 Server-Sent 事件，更新能够自动到达。

例如：Facebook/Twitter 更新、股价更新、新的博文、赛事结果，等等。

### 浏览器支持

表格中的数字指示完全支持 server-sent 事件的首个浏览器。

| API  |      |        |      |      |      |
| ---- | ---- | ------ | ---- | ---- | ---- |
| SSE  | 6.0  | 不支持 | 6.0  | 5.0  | 11.5 |

### 接收 Server-Sent 事件通知

EventSource 对象用于接收服务器发送事件通知：

**实例**

```
var source = new EventSource("demo_sse.php");
source.onmessage = function(event) {
    document.getElementById("result").innerHTML += event.data + "<br>";
};
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html5_sse)

### 例子解释：

- 创建一个新的 EventSource 对象，然后规定发送更新的页面的 URL（本例中是 "demo_sse.php"）
- 每当接收到一次更新，就会发生 onmessage 事件
- 当 onmessage 事件发生时，把已接收的数据推入 id 为 "result" 的元素中

### 检测 Server-Sent 事件支持

在 TIY 实例中，我们编写了一段额外的代码来检测服务器发送事件的浏览器支持：

```
if(typeof(EventSource) !== "undefined") {
    // 是的！支持服务器发送事件！
    // 一些代码.....
} else {
    // 抱歉！不支持服务器发送事件！
}
```

### 服务器端代码实例

为了使上例运行，您需要能够发送数据更新的服务器（比如 PHP 或 ASP）。

服务器端事件流的语法非常简单。请把 "Content-Type" 报头设置为 "text/event-stream"。现在，您可以开始发送事件流了。

```
PHP 中的代码 (demo_sse.php)：

<?php
header('Content-Type: text/event-stream');
header('Cache-Control: no-cache');

$time = date('r');
echo "data: The server time is: {$time}\n\n";
flush();
?>

ASP 中的代码 (VB) (demo_sse.asp)：

<%
Response.ContentType = "text/event-stream"
Response.Expires = -1
Response.Write("data: The server time is: " & now())
Response.Flush()
%>
```

### 代码解释：

- 把报头 "Content-Type" 设置为 "text/event-stream"
- 规定不对页面进行缓存
- 输出要发送的日期（始终以 "data: " 开头）
- 向网页刷新输出数据

### EventSource 对象

在上例中，我们使用 onmessage 事件来获取消息。不过还可以使用其他事件：

| 事件      | 描述                     |
| --------- | ------------------------ |
| onopen    | 当通往服务器的连接被打开 |
| onmessage | 当接收到消息             |
| onerror   | 当发生错误               |



# 实例-测验-总结

## HTML 实例



### HTML 基础标签实例

- [一个简单的 HTML 文件](http://www.w3school.com.cn/tiy/t.asp?f=html_basic)

  这个例子是一个很简单的 HTML 文件，使用了尽可能少的 HTML 标签。它向您演示了 body 元素中的内容是如何被浏览器显示的。

- [简单的段落](http://www.w3school.com.cn/tiy/t.asp?f=html_paragraphs1)

  此例演示：段落元素中的文字如何被浏览器显示。

- [更多的段落](http://www.w3school.com.cn/tiy/t.asp?f=html_paragraphs2)

  本例演示段落元素的某些缺省的行为。

- [“诗歌”问题](http://www.w3school.com.cn/tiy/t.asp?f=html_poem)

  本例演示 HTML 格式化的某些问题。

- [折行](http://www.w3school.com.cn/tiy/t.asp?f=html_paragraphs)

  本例演示在 HTML 文档中折行的使用。

- [标题](http://www.w3school.com.cn/tiy/t.asp?f=html_headers)

  本例演示在 HTML 文档中显示标题的标签。

- [居中排列的标题](http://www.w3school.com.cn/tiy/t.asp?f=html_header)

  本例演示一个居中排列的标题。

- [水平线](http://www.w3school.com.cn/tiy/t.asp?f=html_hr)

  本例演示如何插入水平线。

- [隐藏的注释](http://www.w3school.com.cn/tiy/t.asp?f=html_comment)

  本例演示如何在 HTML 源代码中插入隐藏的注释。

- [背景颜色](http://www.w3school.com.cn/tiy/t.asp?f=html_bgcolor)

  本例演示如何为 HTML 页面添加背景颜色。

*例子解释*

### HTML 文本格式化实例

- [文本格式化](http://www.w3school.com.cn/tiy/t.asp?f=html_textformatting)

  此例演示如何在一个 HTML 文件中对文本进行格式化

- [预格式文本](http://www.w3school.com.cn/tiy/t.asp?f=html_preformattedtext)

  此例演示如何使用 pre 标签对空行和空格进行控制。

- [“计算机输出”标签](http://www.w3school.com.cn/tiy/t.asp?f=html_computeroutput)

  此例演示不同的“计算机输出”标签的显示效果。

- [地址](http://www.w3school.com.cn/tiy/t.asp?f=html_address)

  此例演示如何在 HTML 文件中写地址。

- [缩写和首字母缩写](http://www.w3school.com.cn/tiy/t.asp?f=html_abbracronym)

  此例演示如何实现缩写或首字母缩写。

- [文字方向](http://www.w3school.com.cn/tiy/t.asp?f=html_bdo)

  此例演示如何改变文字的方向。

- [块引用](http://www.w3school.com.cn/tiy/t.asp?f=html_quotations)

  此例演示如何实现长短不一的引用语。

- [删除字效果和插入字效果](http://www.w3school.com.cn/tiy/t.asp?f=html_delins)

  此例演示如何标记删除文本和插入文本。

*例子解释*

### HTML 链接实例

- [创建超级链接](http://www.w3school.com.cn/tiy/t.asp?f=html_links)

  本例演示如何在 HTML 文档中创建链接。

- [将图像作为链接](http://www.w3school.com.cn/tiy/t.asp?f=html_imglink)

  本例演示如何使用图像作为链接。

- [在新的浏览器窗口打开链接](http://www.w3school.com.cn/tiy/t.asp?f=html_link_target)

  本例演示如何在新窗口打开一个页面，这样的话访问者就无需离开你的站点了。

- [链接到同一个页面的不同位置](http://www.w3school.com.cn/tiy/t.asp?f=html_link_locations)

  本例演示如何使用链接跳转至文档的另一个部分

- [跳出框架](http://www.w3school.com.cn/tiy/t.asp?f=html_frame_getfree)

  本例演示如何跳出框架，假如你的页面被固定在框架之内。

- [创建电子邮件链接](http://www.w3school.com.cn/tiy/t.asp?f=html_mailto)

  本例演示如何如何链接到一个邮件。（本例在安装邮件客户端程序后才能工作。）

- [创建电子邮件链接 2](http://www.w3school.com.cn/tiy/t.asp?f=html_mailto2)

  本例演示更加复杂的邮件链接。

*例子解释*

### HTML 框架实例

- [垂直框架](http://www.w3school.com.cn/tiy/t.asp?f=html_frame_cols)

  本例演示：如何使用三份不同的文档制作一个垂直框架。

- [水平框架](http://www.w3school.com.cn/tiy/t.asp?f=html_frame_rows)

  本例演示：如何使用三份不同的文档制作一个水平框架。

- [如何使用  标签](http://www.w3school.com.cn/tiy/t.asp?f=html_noframes)

  本例演示：如何使用 <noframes> 标签。

- [混合框架结构](http://www.w3school.com.cn/tiy/t.asp?f=html_frame_mix)

  本例演示如何制作含有三份文档的框架结构，同时将他们混合置于行和列之中。

- [含有 noresize="noresize" 属性的框架结构](http://www.w3school.com.cn/tiy/t.asp?f=html_frame_noresize)

  本例演示 noresize 属性。在本例中，框架是不可调整尺寸的。在框架间的边框上拖动鼠标，你会发现边框是无法移动的。

- [导航框架](http://www.w3school.com.cn/tiy/t.asp?f=html_frame_navigation)

  本例演示如何制作导航框架。导航框架包含一个将第二个框架作为目标的链接列表。名为 "contents.htm" 的文件包含三个链接。

- [内联框架](http://www.w3school.com.cn/tiy/t.asp?f=html_iframe)

  本例演示如何创建内联框架（HTML 页中的框架）。

- [跳转至框架内的一个指定的节](http://www.w3school.com.cn/tiy/t.asp?f=html_frame_jump)

  本例演示两个框架。其中的一个框架设置了指向另一个文件内指定的节的链接。这个"link.htm"文件内指定的节使用 <a name="C10"> 进行标识。

- [使用框架导航跳转至指定的节](http://www.w3school.com.cn/tiy/t.asp?f=html_frame_navigation2)

  本例演示两个框架。左侧的导航框架包含了一个链接列表，这些链接将第二个框架作为目标。第二个框架显示被链接的文档。导航框架其中的链接指向目标文件中指定的节。

*例子解释*

### HTML 表格实例

- [表格](http://www.w3school.com.cn/tiy/t.asp?f=html_tables)

  这个例子演示如何在 HTML 文档中创建表格。

- [表格边框](http://www.w3school.com.cn/tiy/t.asp?f=html_table_borders)

  本例演示各种类型的表格边框。

- [没有边框的表格](http://www.w3school.com.cn/tiy/t.asp?f=html_tables2)

  本例演示一个没有边框的表格。

- [表格中的表头(Heading)](http://www.w3school.com.cn/tiy/t.asp?f=html_table_headers)

  本例演示如何显示表格表头。

- [空单元格](http://www.w3school.com.cn/tiy/t.asp?f=html_table_nbsp)

  本例展示如何使用 "&nbsp;" 处理没有内容的单元格。

- [带有标题的表格](http://www.w3school.com.cn/tiy/t.asp?f=html_tables3)

  本例演示一个带标题 (caption) 的表格

- [跨行或跨列的表格单元格](http://www.w3school.com.cn/tiy/t.asp?f=html_table_span)

  本例演示如何定义跨行或跨列的表格单元格。

- [表格内的标签](http://www.w3school.com.cn/tiy/t.asp?f=html_table_elements)

  本例演示如何显示在不同的元素内显示元素。

- [单元格边距(Cell padding)](http://www.w3school.com.cn/tiy/t.asp?f=html_table_cellpadding)

  本例演示如何使用 Cell padding 来创建单元格内容与其边框之间的空白。

- [单元格间距(Cell spacing)](http://www.w3school.com.cn/tiy/t.asp?f=html_table_cellspacing)

  本例演示如何使用 Cell spacing 增加单元格之间的距离。

- [向表格添加背景颜色或背景图像](http://www.w3school.com.cn/tiy/t.asp?f=html_table_background)

  本例演示如何向表格添加背景。

- [向表格单元添加背景颜色或者背景图像](http://www.w3school.com.cn/tiy/t.asp?f=html_table_cellbackground)

  本例演示如何向一个或者更多表格单元添加背景。

- [在表格单元中排列内容](http://www.w3school.com.cn/tiy/t.asp?f=html_table_align)

  本例演示如何使用 "align" 属性排列单元格内容,以便创建一个美观的表格。

- [框架(frame)属性](http://www.w3school.com.cn/tiy/t.asp?f=html_table_frame)

  本例演示如何使用 "frame" 属性来控制围绕表格的边框。

*例子解释*

### HTML 列表实例

- [无序列表](http://www.w3school.com.cn/tiy/t.asp?f=html_list_unordered)

  本例演示无序列表。

- [有序列表](http://www.w3school.com.cn/tiy/t.asp?f=html_list_ordered)

  本例演示有序列表。

- [不同类型的无序列表](http://www.w3school.com.cn/tiy/t.asp?f=html_lists_unordered)

  本例演示一个无序列表。

- [不同类型的有序列表](http://www.w3school.com.cn/tiy/t.asp?f=html_lists_ordered)

  本例演示不同类型的有序列表。

- [嵌套列表](http://www.w3school.com.cn/tiy/t.asp?f=html_lists_nested)

  本例演示如何嵌套列表。

- [嵌套列表 2](http://www.w3school.com.cn/tiy/t.asp?f=html_lists_nested2)

  本例演示更复杂的嵌套列表。

- [定义列表](http://www.w3school.com.cn/tiy/t.asp?f=html_list_definition)

  本例演示一个定义列表。

*例子解释*

### HTML 表单与输入实例

- [文本域(Text fields)](http://www.w3school.com.cn/tiy/t.asp?f=html_inputfields)

  本例演示如何在 HTML 页面创建文本域。用户可以在文本域中写入文本。

- [密码域](http://www.w3school.com.cn/tiy/t.asp?f=html_passwordfields)

  本例演示如何创建 HTML 的密码域。

- [复选框](http://www.w3school.com.cn/tiy/t.asp?f=html_checkboxes)

  本例演示如何在 HTML 页中创建复选框。用户可以选中或取消选取复选框。

- [单选按钮](http://www.w3school.com.cn/tiy/t.asp?f=html_radiobuttons)

  本例演示如何在 HTML 中创建单选按钮。

- [简单的下拉列表](http://www.w3school.com.cn/tiy/t.asp?f=html_dropdownbox)

  本例演示如何在 HTML 页面中创建简单的下拉列表框。下拉列表框是一个可选列表。

- [另一个下拉列表](http://www.w3school.com.cn/tiy/t.asp?f=html_dropdownbox2)

  本例演示如何创建一个简单的带有预选值的下拉列表。（译者注：预选值指预先指定的首选项。）

- [文本域(Textarea)](http://www.w3school.com.cn/tiy/s.asp?f=demo_html_textarea)

  本例演示如何创建一个文本域（多行文本输入控件）。用户可以在文本域中写入文本。在文本域中，可写入的字符字数不受限制。

- [创建按钮](http://www.w3school.com.cn/tiy/t.asp?f=html_button)

  本例演示如何创建按钮。你可以对按钮上的文字进行自定义。

- [Fieldset around data](http://www.w3school.com.cn/tiy/t.asp?f=html_fieldset)

  本例演示如何在数据周围绘制一个带标题的框。

### 表单实例

- [带有输入框和确认按钮的表单](http://www.w3school.com.cn/tiy/t.asp?f=html_form_submit)

  本例演示如何向页面添加表单。此表单包含两个输入框和一个确认按钮。

- [带有复选框的表单](http://www.w3school.com.cn/tiy/t.asp?f=html_form_checkbox)

  此表单包含两个复选框和一个确认按钮。

- [带有单选按钮的表单](http://www.w3school.com.cn/tiy/t.asp?f=html_form_radio)

  此表单包含两个单选框和一个确认按钮。

- [从表单发送电子邮件](http://www.w3school.com.cn/tiy/t.asp?f=html_form_mail)

  此例演示如何从表单发送电子邮件。

*例子解释*

### HTML 图像实例

- [插入图像](http://www.w3school.com.cn/tiy/t.asp?f=html_image)

  本例演示如何在网页中显示图像。

- [从不同的位置插入图片](http://www.w3school.com.cn/tiy/t.asp?f=html_image2)

  本例演示如何将其他文件夹或服务器的图片显示到网页中。

- [背景图片](http://www.w3school.com.cn/tiy/t.asp?f=html_backgroundimage)

  本例演示如何向 HTML 页面添加背景图片。

- [排列图片](http://www.w3school.com.cn/tiy/t.asp?f=html_image_align)

  本例演示如何在文字中排列图像。

- [浮动图像](http://www.w3school.com.cn/tiy/t.asp?f=html_image_float)

  本例演示如何使图片浮动至段落的左边或右边。

- [调整图像尺寸](http://www.w3school.com.cn/tiy/t.asp?f=html_image_size)

  本例演示如何将图片调整到不同的尺寸。

- [为图片显示替换文本](http://www.w3school.com.cn/tiy/t.asp?f=html_image_alt)

  本例演示如何为图片显示替换文本。在浏览器无法载入图像时，替换文本属性告诉读者们失去的信息。为页面上的图像都加上替换文本属性是个好习惯。

- [制作图像链接](http://www.w3school.com.cn/tiy/t.asp?f=html_image_link)

  本例演示如何将图像作为一个链接使用。

- [创建图像映射](http://www.w3school.com.cn/tiy/t.asp?f=html_areamap)

  本例显示如何创建带有可供点击区域的图像地图。其中的每个区域都是一个超级链接。

- [把图像转换为图像映射](http://www.w3school.com.cn/tiy/t.asp?f=html_ismap)

  本例显示如何把一幅普通的图像设置为图像映射。

*例子解释*

### HTML 背景实例

- [搭配良好的背景和颜色](http://www.w3school.com.cn/tiy/t.asp?f=html_back_good)

  一个背景颜色和文字颜色搭配良好的例子，使页面中的文字易于阅读。

- [搭配得不好的背景和颜色](http://www.w3school.com.cn/tiy/t.asp?f=html_back_bad)

  一个背景颜色和文字颜色搭配得不好的例子，使页面中的文字难于阅读。

- [可用性强的背景图像](http://www.w3school.com.cn/tiy/t.asp?f=html_back_img)

  背景图像和文字颜色使页面文本易于阅读的例子。

- [可用性强的背景图像 2](http://www.w3school.com.cn/tiy/t.asp?f=html_back_img2)

  另一个背景图像和文字颜色使页面文本易于阅读的例子。

- [可用性差的背景图像](http://www.w3school.com.cn/tiy/t.asp?f=html_back_imgbad)

  背景图像和文字颜色使页面文本不易阅读的例子。

*例子解释*

### HTML 样式 (style) 实例

- [HTML中的样式](http://www.w3school.com.cn/tiy/t.asp?f=html_style)

  本例演示如何使用添加到 <head> 部分的样式信息对 HTML 进行格式化。

- [没有下划线的链接](http://www.w3school.com.cn/tiy/t.asp?f=html_linknoline)

  本例演示如何使用样式属性做一个没有下划线的链接。

- [链接到一个外部样式表](http://www.w3school.com.cn/tiy/t.asp?f=html_link)

  本例演示如何 <link> 标签链接到一个外部样式表。

*例子解释*

### HTML 头部 (head) 实例

- [文档的标题](http://www.w3school.com.cn/tiy/t.asp?f=html_title)

  头元素内部的标题信息不会显示在浏览器窗口中。

- [一个 target，所有的链接](http://www.w3school.com.cn/tiy/t.asp?f=html_base)

  本例显示如何使用 base 标签使页面中的所有标签在新窗口中打开。

*例子解释*

### HTML 元信息 (meta) 实例

- [文档描述](http://www.w3school.com.cn/tiy/t.asp?f=html_meta)

  Meta 元素中的信息可以描述 HTML 文档。

- [文档关键字](http://www.w3school.com.cn/tiy/t.asp?f=html_keywords)

  Meta 元素中的信息可以描述文档的关键词。

- [重定向](http://www.w3school.com.cn/tiy/t.asp?f=html_redirect)

  这个例子演示：在网址已经变更的情况下，将用户重定向到另外一个地址。

*例子解释*

### HTML 脚本 (Script) 实例

- [插入一段脚本](http://www.w3school.com.cn/tiy/t.asp?f=html_script)

  本例演示如何将脚本插入 HTML 文档。

- [运行于不支持脚本的浏览器](http://www.w3school.com.cn/tiy/t.asp?f=html_noscript)

  本例演示如何对付不支持脚本的浏览器。

[**例子解释**](http://www.w3school.com.cn/html/html_scripts.asp)

## HTML 测验

**您可以通过 W3SCHOOL 的测验程序来测试您的 HTML 技能。**

### 关于本测验

本测验包含 20 道题，每道题的最长答题时间是 20 分钟（这是由于每个 session 的默认有效时间是20钟）。

本测验是非官方的测试，它仅仅提供了一个了解您对 HTML 的掌握程度的工具。

### 测验会被记分

每道题的分值是 1 分。在您完成全部的 20 道题之后，系统会为您的测验打分，并提供您做错的题目的正确答案。其中，绿色为正确答案，而红色为错误答案。

[现在就开始测验](http://www.w3school.com.cn/quiz/quiz.asp?quiz=html)！祝您好运。

## 总结

### 你已经将 HTML 教程学习完毕，下一步该学习什么呢？

### HTML 概要

本教程已教你如何使用 HTML 创建站点。

HTML 是一种在 Web 上使用的通用标记语言。HTML 允许你格式化文本，添加图片，创建链接、输入表单、框架和表格等等，并可将之存为文本文件，浏览器即可读取和显示。

HTML 的关键是标签，其作用是指示将出现的内容。

如需更多关于 HTML 的信息，请查看我们的 [HTML 实例](http://www.w3school.com.cn/example/html_examples.asp) 和 [HTML 参考手册](http://www.w3school.com.cn/tags/index.asp) 。

### 现在，你已学完HTML，接下来该学习什么呢？

下一步，你应该学习 XHTML 和 CSS 。

### XHTML

XHTML 是新的 HTML 。最新的HTML版本是 HTML 4.01，同时也是最终的版本。

HTML 将被 XHTML 取代，XHTML 是更严格且更纯净的 HTML 版本。

如需学习 XHTML，请访问我们的 [XHTML 教程](http://www.w3school.com.cn/xhtml/index.asp) 。

### CSS

CSS被用来同时控制多重网页的样式和布局。

通过使用 CSS，所有的格式化均可从 HTML 中剥离出来，并存储于一个独立的文件中。

CSS 给予你对布局的完全控制，同时不会弄乱文档内容。

如需学习如何创建样式表，请访问我们的 [CSS 教程](http://www.w3school.com.cn/css/index.asp) 。

### 选修课：HTML 5

HTML 5 是下一代的 HTML。

HTML5 仍处于完善之中。然而，大部分现代浏览器已经具备了某些 HTML5 支持。

在 W3School 的 HTML 5 教程中，您将了解 HTML5 中的新特性。

[现在就开始学习 HTML 5](http://www.w3school.com.cn/html5/index.asp) ！

