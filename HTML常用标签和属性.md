## HTML常用标签和属性

### head 头部元素

head 元素是所有头部元素的容器。head 内的元素可包含脚本，

指示浏览器在何处可以找到样式表，提供元信息，等等。

以下标签都可以添加到 head 部分：title、base、link、meta、script以及 style。

hand用法介绍

``` html
<head>
    <meta charset="UTF-8">

    <meta name="description"content="在搜索引擎列表页显示的,网页介绍">

    <meta name="keywords"content="搜索引擎,搜索的关键词">
    <base href="http://www.w3school.com.cn/images/"/>
    <base target="_blank"/>
    <link rel="stylesheet" type="text/css" href="mystyle.css"/>
    <title>定义文档的标题。</title>
    <style type="text/css">
        body {
            background-color: yellow
        }

        p {
            color: blue
        }
    </style>
</head>
```



####  title 元素

title 元素能够：

- 定义浏览器工具栏中的标题

- 提供页面被添加到收藏夹时显示的标题

- 显示在搜索引擎结果中的页面标题

#### base 元素

  base 标签为页面上的所有链接规定默认地址或默认目标（target）：

#### link 元素

  link 标签定义文档与外部资源之间的关系。

  link 标签最常用于连接样式表：

####  style 元素

style 标签用于为 HTML 文档定义样式信息。

您可以在 style 元素内规定 HTML 元素在浏览器中呈现的样式：

####  meta 元素

元数据（metadata）是关于数据的信息。

meta 标签提供关于 HTML 文档的元数据。元数据不会显示在页面上，但是对于机器是可读的。

典型的情况是，meta 元素被用于规定页面的描述、关键词、文档的作者、最后修改时间以及其他元数据。

meta 标签始终位于 head 元素中。

元数据可用于浏览器（如何显示内容或重新加载页面），搜索引擎（关键词），或其他 web 服务。

**针对搜索引擎的关键词**

一些搜索引擎会利用 meta 元素的 name 和 content 属性来索引您的页面。

下面的 meta 元素定义页面的描述：

``` html
<meta name="description" content="HTML, CSS, XML" />
```

下面的 meta 元素定义页面的关键词：

``` html
<meta name="keywords" content="HTML, CSS, XML" />
```

name 和 content 属性的作用是描述页面的内容。

####  script 元素

script 标签用于定义客户端脚本，比如 JavaScript。

我们会在稍后的章节讲解 script 元素。



####  head元素

| 标签                                                     | 描述                                     |
| -------------------------------------------------------- | ---------------------------------------- |
| [head](http://www.w3school.com.cn/tags/tag_head.asp)     | 定义关于文档的信息。                     |
| [title](http://www.w3school.com.cn/tags/tag_title.asp)   | 定义文档标题。                           |
| [base](http://www.w3school.com.cn/tags/tag_base.asp)     | 定义页面上所有链接的默认地址或默认目标。 |
| [link](http://www.w3school.com.cn/tags/tag_link.asp)     | 定义文档与外部资源之间的关系。           |
| [meta](http://www.w3school.com.cn/tags/tag_meta.asp)     | 定义关于 HTML 文档的元数据。             |
| [script](http://www.w3school.com.cn/tags/tag_script.asp) | 定义客户端脚本。                         |
| [style](http://www.w3school.com.cn/tags/tag_style.asp)   | 定义文档的样式信息。                     |



### 标题标签

``` html
<h1>标题标签</h1>
<h2>标题标签</h2>
<h3>标题标签</h3>
<h4>标题标签</h4>
<h5>标题标签</h5>
<h6>标题标签</h6>
```

### 段落标签

``` html
<p>段落标签</p>
```

### 水平线标签

```
<hr/>
```

### 换行标签

```
<br/>
```

### 文本格式化标签

```
<b>文本格式化标签,加粗</b>
<strong>文本格式化标签,加粗,推荐使用</strong>
<i>斜体</i>
<em>斜体,推荐使用</em>
<s>删除线</s>
<del>删除线,推荐使用</del>
<u>下划线</u>
<ins>下划线,推荐使用</ins>
```



#### 文本格式化标签

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
| [s](http://www.w3school.com.cn/tags/tag_strike.asp)          | *不赞成使用。*使用 del 代替。         |
| [strike](http://www.w3school.com.cn/tags/tag_strike.asp)     | *不赞成使用。*使用 del 代替。         |
| [u](http://www.w3school.com.cn/tags/tag_u.asp)               | *不赞成使用。*使用样式（style）代替。 |

#### 计算机输出”标签

| 标签                                                         | 描述                          |
| ------------------------------------------------------------ | ----------------------------- |
| [code](http://www.w3school.com.cn/tags/tag_phrase_elements.asp) | 定义计算机代码。              |
| [kbd](http://www.w3school.com.cn/tags/tag_phrase_elements.asp) | 定义键盘码。                  |
| [samp](http://www.w3school.com.cn/tags/tag_phrase_elements.asp) | 定义计算机代码样本。          |
| [tt](http://www.w3school.com.cn/tags/tag_font_style.asp)     | 定义打字机代码。              |
| [var](http://www.w3school.com.cn/tags/tag_phrase_elements.asp) | 定义变量。                    |
| [pre](http://www.w3school.com.cn/tags/tag_pre.asp)           | 定义预格式文本。              |
| listing                                                      | *不赞成使用。*使用 pre 代替。 |
| plaintext                                                    | *不赞成使用。*使用 pre 代替。 |
| xmp                                                          | *不赞成使用。*使用 pre 代替。 |

#### 引用、引用和术语定义

| 标签                                                         | 描述               |
| ------------------------------------------------------------ | ------------------ |
| [abbr](http://www.w3school.com.cn/tags/tag_abbr.asp)         | 定义缩写。         |
| [acronym](http://www.w3school.com.cn/tags/tag_acronym.asp)   | 定义首字母缩写。   |
| [address](http://www.w3school.com.cn/tags/tag_address.asp)   | 定义地址。         |
| [bdo](http://www.w3school.com.cn/tags/tag_bdo.asp)           | 定义文字方向。     |
| [blockquote](http://www.w3school.com.cn/tags/tag_blockquote.asp) | 定义长的引用。     |
| [q](http://www.w3school.com.cn/tags/tag_q.asp)               | 定义短的引用语。   |
| [cite](http://www.w3school.com.cn/tags/tag_phrase_elements.asp) | 定义引用、引证。   |
| [dfn](http://www.w3school.com.cn/tags/tag_phrase_elements.asp) | 定义一个定义项目。 |



### style属性

```
<p style="font-family:verdana;color:red">一般卸载css文件中</P>
```
下面列出了适用于大多数 HTML 元素的属性：

| 属性  | 值                 | 描述                                     |
| ----- | ------------------ | ---------------------------------------- |
| class | *classname*        | 规定元素的类名（classname）              |
| id    | *id*               | 规定元素的唯一 id                        |
| style | *style_definition* | 规定元素的行内样式（inline style）       |
| title | *text*             | 规定元素的额外信息（可在工具提示中显示） |

**样式**

应该避免使用下面这些标签和属性：

| 标签             | 描述               |
| ---------------- | ------------------ |
| center           | 定义居中的内容。   |
| font 和 basefont | 定义 HTML 字体。   |
| s 和 strike      | 定义删除线文本     |
| u                | 定义下划线文本     |
| 属性             | 描述               |
| align            | 定义文本的对齐方式 |
| bgcolor          | 定义背景颜色       |
| color            | 定义文本颜色       |

对于以上这些标签和属性：请使用样式代替！

### 注释标签

HTML 注释标签

```
<!-- 在此处写注释 -->
```

### 超链接标签

```
<a href="url">Link text</a>
```

New : HTML5 中的新属性。

| 属性                                                         | 值                                | 描述                                                 |
| ------------------------------------------------------------ | --------------------------------- | ---------------------------------------------------- |
| [charset](http://www.w3school.com.cn/tags/att_a_charset.asp) | *char_encoding*                   | HTML5 中不支持。规定被链接文档的字符集。             |
| [coords](http://www.w3school.com.cn/tags/att_a_coords.asp)   | *coordinates*                     | HTML5 中不支持。规定链接的坐标。                     |
| [download](http://www.w3school.com.cn/tags/att_a_download.asp) | *filename*                        | 规定被下载的超链接目标。                             |
| [href](http://www.w3school.com.cn/tags/att_a_href.asp)       | *URL*                             | 规定链接指向的页面的 URL。                           |
| [hreflang](http://www.w3school.com.cn/tags/att_a_hreflang.asp) | *language_code*                   | 规定被链接文档的语言。                               |
| [media](http://www.w3school.com.cn/tags/att_a_media.asp)     | *media_query*                     | 规定被链接文档是为何种媒介/设备优化的。              |
| [name](http://www.w3school.com.cn/tags/att_a_name.asp)       | *section_name*                    | HTML5 中不支持。规定锚的名称。                       |
| [rel](http://www.w3school.com.cn/tags/att_a_rel.asp)         | *text*                            | 规定当前文档与被链接文档之间的关系。                 |
| [rev](http://www.w3school.com.cn/tags/att_a_rev.asp)         | *text*                            | HTML5 中不支持。规定被链接文档与当前文档之间的关系。 |
| [shape](http://www.w3school.com.cn/tags/att_a_shape.asp)     | defaultrectcirclepoly             | HTML5 中不支持。规定链接的形状。                     |
| [target](http://www.w3school.com.cn/tags/att_a_target.asp)   | _blank_parent_self_top*framename* | 规定在何处打开链接文档。                             |
| [type](http://www.w3school.com.cn/tags/att_a_type.asp)       | *MIME type*                       | 规定被链接文档的的 MIME 类型。                       |







### 图像标签

```
<img src="timg.jpg" alt="替换文本">
```

| 标签                                                 | 描述                         |
| ---------------------------------------------------- | ---------------------------- |
| [img](http://www.w3school.com.cn/tags/tag_img.asp)   | 定义图像。                   |
| [map](http://www.w3school.com.cn/tags/tag_map.asp)   | 定义图像地图。               |
| [area](http://www.w3school.com.cn/tags/tag_area.asp) | 定义图像地图中的可点击区域。 |

**必需的属性**

| 属性                                                   | 值     | 描述                 |
| ------------------------------------------------------ | ------ | -------------------- |
| [alt](http://www.w3school.com.cn/tags/att_img_alt.asp) | *text* | 规定图像的替代文本。 |
| [src](http://www.w3school.com.cn/tags/att_img_src.asp) | *URL*  | 规定显示图像的 URL。 |

**可选的属性**

| 属性                                                         | 值                       | 描述                                           |
| ------------------------------------------------------------ | ------------------------ | ---------------------------------------------- |
| [align](http://www.w3school.com.cn/tags/att_img_align.asp)   | topbottommiddleleftright | 不推荐使用。规定如何根据周围的文本来排列图像。 |
| [border](http://www.w3school.com.cn/tags/att_img_border.asp) | *pixels*                 | 不推荐使用。定义图像周围的边框。               |
| [height](http://www.w3school.com.cn/tags/att_img_height-width.asp) | *pixels**%*              | 定义图像的高度。                               |
| [hspace](http://www.w3school.com.cn/tags/att_img_hspace_vspace.asp) | *pixels*                 | 不推荐使用。定义图像左侧和右侧的空白。         |
| [ismap](http://www.w3school.com.cn/tags/att_img_ismap.asp)   | *URL*                    | 将图像定义为服务器端图像映射。                 |
| [longdesc](http://www.w3school.com.cn/tags/att_img_longdesc.asp) | *URL*                    | 指向包含长的图像描述文档的 URL。               |
| [usemap](http://www.w3school.com.cn/tags/att_img_usemap.asp) | *URL*                    | 将图像定义为客户器端图像映射。                 |
| [vspace](http://www.w3school.com.cn/tags/att_img_hspace_vspace.asp) | *pixels*                 | 不推荐使用。定义图像顶部和底部的空白。         |
| [width](http://www.w3school.com.cn/tags/att_img_height-width.asp) | *pixels**%*              | 设置图像的宽度。                               |

### table表格



#### 表格标签

| 表格                                                         | 描述                   |
| ------------------------------------------------------------ | ---------------------- |
| [table](http://www.w3school.com.cn/tags/tag_table.asp)     | 定义表格               |
| [caption](http://www.w3school.com.cn/tags/tag_caption.asp) | 定义表格标题。         |
| [th](http://www.w3school.com.cn/tags/tag_th.asp)           | 定义表格的表头。       |
| [tr](/tags/tag_tr.asp)                                     | 定义表格的行。         |
| [td](/tags/tag_td.asp)                                     | 定义表格单元。         |
| [thead](/tags/tag_thead.asp)                               | 定义表格的页眉。       |
| [tbody](/tags/tag_tbody.asp)                               | 定义表格的主体。       |
| [tfoot](/tags/tag_tfoot.asp)                               | 定义表格的页脚。       |
| [col](/tags/tag_col.asp)                                   | 定义用于表格列的属性。 |
| [colgroup](/tags/tag_colgroup.asp)                         | 定义表格列的组。       |
|| |

### 列表

**HTML 支持有序、无序和定义列表** 

#### 列表标签

| 标签                                                 | 描述                     |
| ---------------------------------------------------- | ------------------------ |
| [ol](http://www.w3school.com.cn/tags/tag_ol.asp)     | 定义有序列表。           |
| [ul](http://www.w3school.com.cn/tags/tag_ul.asp)     | 定义无序列表。           |
| [li](http://www.w3school.com.cn/tags/tag_li.asp)     | 定义列表项。             |
| [dl](http://www.w3school.com.cn/tags/tag_dl.asp)     | 定义定义列表。           |
| [dt](http://www.w3school.com.cn/tags/tag_dt.asp)     | 定义定义项目。           |
| [dd](http://www.w3school.com.cn/tags/tag_dd.asp)     | 定义定义的描述。         |
| [dir](http://www.w3school.com.cn/tags/tag_dir.asp)   | 已废弃。使用 ul 代替它。 |
| [menu](http://www.w3school.com.cn/tags/tag_menu.asp) | 已废弃。使用 ul 代替它。 |

###  div 和 span块级元素

```
<div>块级元素,主要用于盒子布局</div>
<span>块级元素,单行块级元素</span>
```

### HTML5 语义化元素

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



### HTML 中常用的字符实体

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



### HTML颜色

**颜色由红色、绿色、蓝色混合而成。**

#### 颜色值

颜色由一个十六进制符号来定义，这个符号由红色、绿色和蓝色的值组成（RGB）。

rgb(0,0,0)  

rgb 有三组数字组成.分别是,红绿蓝,值得大小.从 0~255,三组数字组合冲颜色

#### 颜色名

大多数的浏览器都支持颜色名集合。

提示：仅仅有 16 种颜色名被 W3C 的 HTML4.0 标准所支持。它们是：aqua, black, blue, fuchsia, gray, green, lime, maroon, navy, olive, purple, red, silver, teal, white, yellow。

如果需要使用其它的颜色，需要使用十六进制的颜色值

## form表单

form 元素

HTML 表单用于收集用户输入。

form 元素定义 HTML 表单：

HTML 表单包含*表单元素*。

表单元素指的是不同类型的 input 元素、复选框、单选按钮、提交按钮等等。

### input 元素

*input* 元素是最重要的*表单元素*。

input 元素有很多形态，根据不同的 *type* 属性。

这是本章中使用的类型：

| 类型   | 描述                                 |
| ------ | ------------------------------------ |
| text   | 定义常规文本输入。                   |
| radio  | 定义单选按钮输入（选择多个选择之一） |
| submit | 定义提交按钮（提交表单）             |

注意：表单本身并不可见。还要注意文本字段的默认宽度是 20 个字符。 

### 文本输入

 定义用于*文本输入*的单行输入字段：

```
<input type="text" name="firstname">
```

### 单选按钮输入

*input type="radio"* 定义*单选按钮*。

单选按钮允许用户在有限数量的选项中选择其中之一：

```
<form>
<input type="radio" name="sex" value="男" checked>男
<br>
<input type="radio" name="sex" value="女">女
</form> 
```

### 提交按钮

*input type="submit"* 定义用于向*表单处理程序*（form-handler）*提交*表单的按钮。

表单处理程序通常是包含用来处理输入数据的脚本的服务器页面。

表单处理程序在表单的 *action* 属性中指定：

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

### Action 属性

*action 属性*定义在提交表单时执行的动作。

向服务器提交表单的通常做法是使用提交按钮。

通常，表单会被提交到 web 服务器上的网页。



form 属性的列表：

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

## 表单元素

### input元素

最重要的表单元素是 *input* 元素。

input 元素根据不同的 *type* 属性，可以变化为多种形态。

注释：下一章讲解所有 HTML 输入类型。

### select 元素（下拉列表）

*select* 元素定义*下拉列表*：

实例

```
<select name="cars">
<option value="volvo">Volvo</option>
<option value="saab">Saab</option>
<option value="fiat">Fiat</option>
<option value="audi">Audi</option>
</select>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_elements_select)

*option* 元素定义待选择的选项。

列表通常会把首个选项显示为被选选项。

您能够通过添加 selected 属性来定义预定义选项。

实例

```
<textarea name="message" rows="10" cols="30">
The cat was playing in the garden.
</textarea>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_elements_select_pre)

### textarea元素

*textarea* 元素定义多行输入字段（*文本域*）：

实例

```
textarea name="message" rows="10" cols="30"
The cat was playing in the garden.
/textarea
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_headers)

以上 HTML 代码在浏览器中显示为：

```
The cat was playing in the garden.
```

### button 元素

*button* 元素定义可点击的*按钮*：

实例

```
<button type="button" onclick="alert('Hello World!')">Click Me!</button>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_elements_button)

以上 HTML 代码在浏览器中显示为：

### HTML5 表单元素

HTML5 增加了如下表单元素：

- datalist
- keygen
- output

注释：默认地，浏览器不会显示未知元素。新元素不会破坏您的页面。

### HTML5 datalist  元素

*datalist* 元素为 input 元素规定预定义选项列表。

用户会在他们输入数据时看到预定义选项的下拉列表。

input 元素的 *list* 属性必须引用 datalist 元素的 *id* 属性。

实例

通过 datalist 设置预定义值的 input 元素：

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

## HTML 输入类型

**本章描述 input 元素的输入类型。**

### 输入类型：text

*input type="text"* 定义供*文本输入*的单行输入字段：

实例

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

*input type="password"* 定义*密码字段*：

实例

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

*input type="submit"* 定义*提交*表单数据至*表单处理程序*的按钮。

表单处理程序（form-handler）通常是包含处理输入数据的脚本的服务器页面。

在表单的 action 属性中规定表单处理程序（form-handler）：

实例

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

实例

```
form action="action_page.php"
First name:br
input type="text" name="firstname" value="Mickey"
br
Last name:br
input type="text" name="lastname" value="Mouse"
brbr
input type="submit"
/form 
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_submit_nn)

### Input Type: radio

input type="radio" 定义单选按钮。

Radio buttons let a user select ONLY ONE of a limited number of choices:

实例

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

input type="checkbox" 定义复选框。

复选框允许用户在有限数量的选项中选择零个或多个选项。

实例

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

*input type="button* 定义*按钮*。

实例

```
<input type="button" onclick="alert('Hello World!')" value="Click Me!">
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_button)

以上 HTML 代码在浏览器中看上去是这样的：

## HTML5 输入类型

HTML5 增加了多个新的输入类型：

color	date		datetime		datetime-local		email

month		number		range		search	

tel		time		url		week

注释：老式 web 浏览器不支持的输入类型，会被视为输入类型 text。

### 输入类型：number

*input type="number"* 用于应该包含数字值的输入字段。

您能够对数字做出限制。

根据浏览器支持，限制可应用到输入字段。

实例

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

实例

```
form
  Quantity:
  input type="number" name="points" min="0" max="100" step="10" value="30"
/form
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_number_step)

### 输入类型：date

*input type="date"* 用于应该包含日期的输入字段。

根据浏览器支持，日期选择器会出现输入字段中。

实例

```
<form>
  Birthday:
  <input type="date" name="bday">
</form>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_date)

您可以向输入添加限制：

实例

```
form
  Enter a date before 1980-01-01:
  input type="date" name="bday" max="1979-12-31"br
  Enter a date after 2000-01-01:
  input type="date" name="bday" min="2000-01-02"br
/form
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_date_max_min)

### 输入类型：color

*input type="color"* 用于应该包含颜色的输入字段。

根据浏览器支持，颜色选择器会出现输入字段中。

实例

```
<form>
  Select your favorite color:
  <input type="color" name="favcolor">
</form>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_color)

### 输入类型：range

*input type="range"* 用于应该包含一定范围内的值的输入字段。

根据浏览器支持，输入字段能够显示为滑块控件。

实例

```
<form>
  <input type="range" name="points" min="0" max="10">
</form>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_range)

您能够使用如下属性来规定限制：min、max、step、value。

### 输入类型：month

*input type="month"* 允许用户选择月份和年份。

根据浏览器支持，日期选择器会出现输入字段中。

实例

```
<form>
  Birthday (month and year):
  <input type="month" name="bdaymonth">
</form>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_month)

### 输入类型：week

*input type="week"* 允许用户选择周和年。

根据浏览器支持，日期选择器会出现输入字段中。

实例

```
<form>
  Select a week:
  <input type="week" name="week_year">
</form>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_week)

### 输入类型：time

*input type="time"* 允许用户选择时间（无时区）。

根据浏览器支持，时间选择器会出现输入字段中。

实例

```
<form>
  Select a time:
  <input type="time" name="usr_time">
</form>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_time)

### 输入类型：datetime

*input type="datetime"* 允许用户选择日期和时间（有时区）。

根据浏览器支持，日期选择器会出现输入字段中。

实例

```
<form>
  Birthday (date and time):
  <input type="datetime" name="bdaytime">
</form>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_datetime)

### 输入类型：datetime-local

*input type="datetime-local"* 允许用户选择日期和时间（无时区）。

根据浏览器支持，日期选择器会出现输入字段中。

实例

```
<form>
  Birthday (date and time):
  <input type="datetime-local" name="bdaytime">
</form>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_datetime-local)

### 输入类型：email

*input type="email"* 用于应该包含电子邮件地址的输入字段。

根据浏览器支持，能够在被提交时自动对电子邮件地址进行验证。

某些智能手机会识别 email 类型，并在键盘增加 ".com" 以匹配电子邮件输入。

实例

```
<form>
  E-mail:
  <input type="email" name="email">
</form>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_email)

### 输入类型：search

*input type="search"* 用于搜索字段（搜索字段的表现类似常规文本字段）。

实例

```
<form>
  Search Google:
  <input type="search" name="googlesearch">
</form>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_search)

### 输入类型：tel

*input type="tel"* 用于应该包含电话号码的输入字段。

目前只有 Safari 8 支持 tel 类型。

实例

```
<form>
  Telephone:
  <input type="tel" name="usrtel">
</form>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=html_input_tel)

### 输入类型：url

*input type="url"* 用于应该包含 URL 地址的输入字段。

根据浏览器支持，在提交时能够自动验证 url 字段。

某些智能手机识别 url 类型，并向键盘添加 ".com" 以匹配 url 输入。

实例

```
form
  Add your homepage:
  input type="url" name="homepage"
/form
```