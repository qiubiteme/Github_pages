# CSS速查笔记

## CSS 概述

- CSS 指层叠样式表 (*C*ascading *S*tyle *S*heets)
- 样式定义*如何显示* HTML 元素
- 样式通常存储在*样式表*中
- 把样式添加到 HTML 4.0 中，是为了*解决内容与表现分离的问题*
- *外部样式表*可以极大提高工作效率
- 外部样式表通常存储在 *CSS 文件*中
- 多个样式定义可*层叠*为一



## CSS样式表创建

### 外部样式表

当样式需要应用于很多页面时，外部样式表将是理想的选择。在使用外部样式表的情况下，你可以通过改变一个文件来改变整个站点的外观。每个页面使用 <link> 标签链接到样式表。<link> 标签在（文档的）头部： 

``` css
<head>
<link rel="stylesheet" type="text/css" href="mystyle.css" />
</head>
```

### 内部样式表

当单个文档需要特殊的样式时，就应该使用内部样式表。你可以使用 <style> 标签在文档头部定义内部样式表，就像这样: 

```css
<head>
<style type="text/css">
  hr {color: sienna;}
  p {margin-left: 20px;}
  body {background-image: url("images/back40.gif");}
</style>
</head>
```

### 内联样式

由于要将表现和内容混杂在一起，内联样式会损失掉样式表的许多优势。请慎用这种方法，例如当样式仅需要在一个元素上应用一次时。

要使用内联样式，你需要在相关的标签内使用样式（style）属性。Style 属性可以包含任何 CSS 属性。本例展示如何改变段落的颜色和左外边距：

```css
<p style="color: sienna; margin-left: 20px">
This is a paragraph
</p>
```

## 样式层叠

样式表允许以多种方式规定样式信息。样式可以规定在单个的 HTML 元素中，在 HTML 页的头元素中，或在一个外部的 CSS 文件中。甚至可以在同一个 HTML 文档内部引用多个外部样式表。

**层叠次序**

**当同一个 HTML 元素被不止一个样式定义时，会使用哪个样式呢？**

一般而言，所有的样式会根据下面的规则层叠于一个新的虚拟样式表中，其中数字 4 拥有最高的优先权。

1. 浏览器缺省设置
2. 外部样式表
3. 内部样式表（位于 <head> 标签内部）
4. 内联样式（在 HTML 元素内部）

因此，内联样式（在 HTML 元素内部）拥有最高的优先权，这意味着它将优先于以下的样式声明：<head> 标签中的样式声明，外部样式表中的样式声明，或者浏览器中的样式声明（缺省值）。

## CSS 基础语法

````css
选择器{
    属性名 : 属性值;
}
````

## CSS 选择器

### 标签选择器（元素选择器）

标签选择器是指用HTML标签名称作为选择器，按标签名称分类

``` css 
div{
    color : red;
}
```



### 类选择器

类选择器使用“.”（英文点号）进行标识，后面紧跟类名，其基本语法格式如下：

``` css
.hello{
    color : red;
}
```



### id选择器

id选择器使用“#”进行标识，后面紧跟id名，其基本语法格式如下：

```
#id名{属性1:属性值1; 属性2:属性值2; 属性3:属性值3; }
```

### 组选择器

我们可以选择器,标签,类名,id一起组合为一个选择器,组内的选择器,使用同样的样式

```css
h1,h2,h3,h4,h5,h6,.red {
  color: red;
  }
```

### 后代选择器

后代选择器,根据选择器的顺序.过滤到不匹配的选择器内容

这个后代选择器,只会对页面中,div下的p标签起作用

``` css
div p{
    color : red;
}
```

### 通配符选择器

通配符   选择器用“*”号表示，他是所有选择器中作用范围最广的，能匹配页面中所有的元素。其基本语法格式如下：

``` css
*{
    color : red;
}
```

### 属性选择器

下面的例子为带有 title 属性的所有元素设置样式：

```css
[title]
{
color:red;
}
```

### 属性和值选择器

下面的例子为 title="W3School" 的所有元素设置样式：

``` css
[title=W3School]
{
border:5px solid blue;
}
```

**设置表单的样式**

属性选择器在为不带有 class 或 id 的表单设置样式时特别有用：

``` css
input[type="text"]
{
  width:150px;
  display:block;
  margin-bottom:10px;
  background-color:yellow;
  font-family: Verdana, Arial;
}

input[type="button"]
{
  width:120px;
  margin-left:35px;
  display:block;
  font-family: Verdana, Arial;
}
```
### CSS 子元素选择器

如果您不希望选择任意的后代元素，而是希望缩小范围，只选择某个元素的子元素，请使用子元素选择器（Child selector）。

例如，如果您希望选择只作为 h1 元素子元素的 strong 元素，可以这样写：

```css
h1 > strong {color:red;}
```

### CSS 相邻兄弟选择器

如果需要选择紧接在另一个元素后的元素，而且二者有相同的父元素，可以使用相邻兄弟选择器（Adjacent sibling selector）。

例如，如果要增加紧接在 h1 元素后出现的段落的上边距，可以这样写：

```css
h1 + p {margin-top:50px;}
```

## CSS 背景

**CSS 背景属性**

| 属性                                                         | 描述                                         |
| ------------------------------------------------------------ | -------------------------------------------- |
| [background](http://www.w3school.com.cn/cssref/pr_background.asp) | 简写属性，作用是将背景属性设置在一个声明中。 |
| [background-attachment](http://www.w3school.com.cn/cssref/pr_background-attachment.asp) | 背景图像是否固定或者随着页面的其余部分滚动。 |
| [background-color](http://www.w3school.com.cn/cssref/pr_background-color.asp) | 设置元素的背景颜色。                         |
| [background-image](http://www.w3school.com.cn/cssref/pr_background-image.asp) | 把图像设置为背景。                           |
| [background-position](http://www.w3school.com.cn/cssref/pr_background-position.asp) | 设置背景图像的起始位置。                     |
| [background-repeat](http://www.w3school.com.cn/cssref/pr_background-repeat.asp) | 设置背景图像是否及如何重复。                 |

**CSS 允许应用纯色作为背景，也允许使用背景图像创建相当复杂的效果。**

**CSS 在这方面的能力远远在 HTML 之上。**

### 背景色background-color

可以使用 [background-color 属性](http://www.w3school.com.cn/cssref/pr_background-color.asp)为元素设置背景色。这个属性接受任何合法的颜色值。

这条规则把元素的背景设置为灰色：

```css
p {background-color: gray;}
```

### 背景图像background-image 

要把图像放入背景，需要使用 [background-image 属性](http://www.w3school.com.cn/cssref/pr_background-image.asp)。background-image  属性的默认值是 none，表示背景上没有放置任何图像。

如果需要设置一个背景图像，必须为这个属性设置一个 URL 值：

```css
body {background-image: url(/i/eg_bg_04.gif);}
```

大多数背景都应用到 body 元素，不过并不仅限于此。 

### 背景重复background-repeat

如果需要在页面上对背景图像进行平铺，可以使用 [background-repeat 属性](http://www.w3school.com.cn/cssref/pr_background-repeat.asp)。

属性值 repeat 导致图像在水平垂直方向上都平铺，就像以往背景图像的通常做法一样。repeat-x 和 repeat-y 分别导致图像只在水平或垂直方向上重复，no-repeat 则不允许图像在任何方向上平铺。

默认地，背景图像将从一个元素的左上角开始。请看下面的例子：

```css
body{ 
  background-image: url(/i/eg_bg_03.gif);
  background-repeat: repeat-y;
  }
```

### 背景定位background-position

可以利用 [background-position 属性](http://www.w3school.com.cn/cssref/pr_background-position.asp)改变图像在背景中的位置。

下面的例子在 body 元素中将一个背景图像居中放置：

```css
body{ 
    background-image:url('/i/eg_bg_03.gif');
    background-repeat:no-repeat;
    background-position:center;
  }
```
为 background-position 属性提供值有很多方法。首先，可以使用一些关键字：top、bottom、left、right 和 center。通常，这些关键字会成对出现，不过也不总是这样。还可以使用长度值，如 100px 或 5cm，最后也可以使用百分数值。不同类型的值对于背景图像的放置稍有差异。 

## CSS 文本

**CSS 文本属性可定义文本的外观。**

**通过文本属性，您可以改变文本的颜色、字符间距，对齐文本，装饰文本，对文本进行缩进，等等。**

### **CSS 文本属性**

| 属性                                                         | 描述                                                        |
| ------------------------------------------------------------ | ----------------------------------------------------------- |
| [color](http://www.w3school.com.cn/cssref/pr_text_color.asp) | 设置文本颜色                                                |
| [direction](http://www.w3school.com.cn/cssref/pr_text_direction.asp) | 设置文本方向。                                              |
| [line-height](http://www.w3school.com.cn/cssref/pr_dim_line-height.asp) | 设置行高。                                                  |
| [letter-spacing](http://www.w3school.com.cn/cssref/pr_text_letter-spacing.asp) | 设置字符间距。                                              |
| [text-align](http://www.w3school.com.cn/cssref/pr_text_text-align.asp) | 对齐元素中的文本。                                          |
| [text-decoration](http://www.w3school.com.cn/cssref/pr_text_text-decoration.asp) | 向文本添加修饰。                                            |
| [text-indent](http://www.w3school.com.cn/cssref/pr_text_text-indent.asp) | 缩进元素中文本的首行。                                      |
| text-shadow                                                  | 设置文本阴影。CSS2 包含该属性，但是 CSS2.1 没有保留该属性。 |
| [text-transform](http://www.w3school.com.cn/cssref/pr_text_text-transform.asp) | 控制元素中的字母。                                          |
| unicode-bidi                                                 | 设置文本方向。                                              |
| [white-space](http://www.w3school.com.cn/cssref/pr_text_white-space.asp) | 设置元素中空白的处理方式。                                  |
| [word-spacing](http://www.w3school.com.cn/cssref/pr_text_word-spacing.asp) | 设置字间距。                                                |

## CSS 字体

**CSS 字体属性定义文本的字体系列、大小、加粗、风格（如斜体）和变形（如小型大写字母）。**

**CSS 字体系列**

在 CSS 中，有两种不同类型的字体系列名称：

- 通用字体系列 - 拥有相似外观的字体系统组合（比如 "Serif" 或 "Monospace"）
- 特定字体系列 - 具体的字体系列（比如 "Times" 或 "Courier"）

除了各种特定的字体系列外，CSS 定义了 5 种通用字体系列：

- Serif 字体
- Sans-serif 字体
- Monospace 字体
- Cursive 字体
- Fantasy 字体

如果需要了解更多有关字体系列的知识，请阅读 [CSS 字体系列](http://www.w3school.com.cn/css/css_font-family.asp)。

### CSS 字体属性

| 属性                                                         | 描述                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| [font](http://www.w3school.com.cn/cssref/pr_font_font.asp)   | 简写属性。作用是把所有针对字体的属性设置在一个声明中。       |
| [font-family](http://www.w3school.com.cn/cssref/pr_font_font-family.asp) | 设置字体系列。                                               |
| [font-size](http://www.w3school.com.cn/cssref/pr_font_font-size.asp) | 设置字体的尺寸。                                             |
| [font-size-adjust](http://www.w3school.com.cn/cssref/pr_font_font-size-adjust.asp) | 当首选字体不可用时，对替换字体进行智能缩放。（CSS2.1 已删除该属性。） |
| [font-stretch](http://www.w3school.com.cn/cssref/pr_font_font-stretch.asp) | 对字体进行水平拉伸。（CSS2.1 已删除该属性。）                |
| [font-style](http://www.w3school.com.cn/cssref/pr_font_font-style.asp) | 设置字体风格。                                               |
| [font-variant](http://www.w3school.com.cn/cssref/pr_font_font-variant.asp) | 以小型大写字体或者正常字体显示文本。                         |
| [font-weight](http://www.w3school.com.cn/cssref/pr_font_weight.asp) | 设置字体的粗细。                                             |

## CSS 链接

链接在使用中,会设置,会根据需求设置各种样式

### 设置链接的样式

能够设置链接样式的 CSS 属性有很多种（例如 color, font-family, background 等等）。

链接的特殊性在于能够根据它们所处的状态来设置它们的样式。

链接的四种状态：

- a:link - 普通的、未被访问的链接
- a:visited - 用户已访问的链接
- a:hover - 鼠标指针位于链接的上方
- a:active - 链接被点击的时刻

**实例**

``` css
a:link {color:#FF0000;}		/* 未被访问的链接 */
a:visited {color:#00FF00;}	/* 已被访问的链接 */
a:hover {color:#FF00FF;}	/* 鼠标指针移动到链接上 */
a:active {color:#0000FF;}	/* 正在被点击的链接 */
```

当为链接的不同状态设置样式时，请按照以下次序规则：

- a:hover 必须位于 a:link 和 a:visited 之后
- a:active 必须位于 a:hover 之后

**实例**

``` css
a:link {color:#FF0000;}		/* 未被访问的链接 */
a:visited {color:#00FF00;}	/* 已被访问的链接 */
a:hover {color:#FF00FF;}	/* 鼠标指针移动到链接上 */
a:active {color:#0000FF;}	/* 正在被点击的链接 */
```

当为链接的不同状态设置样式时，请按照以下次序规则：

- a:hover 必须位于 a:link 和 a:visited 之后
- a:active 必须位于 a:hover 之后

**常见的链接样式**

在上面的例子中，链接根据其状态改变颜色。

让我们看看其他几种常见的设置链接样式的方法：

**文本修饰**

text-decoration 属性大多用于去掉链接中的下划线：

**实例**

``` css
a:link {text-decoration:none;}
a:visited {text-decoration:none;}
a:hover {text-decoration:underline;}
a:active {text-decoration:underline;}
```

**设置背景色**

background-color 属性规定链接的背景色：

实例

``` css
a:link {background-color:#B2FF99;}
a:visited {background-color:#FFFF85;}
a:hover {background-color:#FF704D;}
a:active {background-color:#FF704D;}
```



## CSS 列表

**CSS 列表属性允许你放置、改变列表项标志，或者将图像作为列表项标志。**

从某种意义上讲，不是描述性的文本的任何内容都可以认为是列表。人口普查、太阳系、家谱、参观菜单，甚至你的所有朋友都可以表示为一个列表或者是列表的列表。

由于列表如此多样，这使得列表相当重要，所以说，CSS 中列表样式不太丰富确实是一大憾事。

### CSS 列表属性(list)

| 属性                                                         | 描述                                                 |
| ------------------------------------------------------------ | ---------------------------------------------------- |
| [list-style](http://www.w3school.com.cn/cssref/pr_list-style.asp) | 简写属性。用于把所有用于列表的属性设置于一个声明中。 |
| [list-style-image](http://www.w3school.com.cn/cssref/pr_list-style-image.asp) | 将图象设置为列表项标志。                             |
| [list-style-position](http://www.w3school.com.cn/cssref/pr_list-style-position.asp) | 设置列表中列表项标志的位置。                         |
| [list-style-type](http://www.w3school.com.cn/cssref/pr_list-style-type.asp) | 设置列表项标志的类型。                               |
| marker-offset                                                |                                                      |

**list-style-type 属性设置列表项标记的类型。** 

| 值      | 描述                 |
| ------- | -------------------- |
| none    | 无标记。             |
| disc    | 默认。标记是实心圆。 |
| circle  | 标记是空心圆。       |
| square  | 标记是实心方块。     |
| decimal | 标记是数字。         |



## CSS 表格

**CSS 表格属性可以帮助您极大地改善表格的外观。**

### CSS Table 属性

| 属性                                                         | 描述                                 |
| ------------------------------------------------------------ | ------------------------------------ |
| [border-collapse](http://www.w3school.com.cn/cssref/pr_tab_border-collapse.asp) | 设置是否把表格边框合并为单一的边框。 |
| [border-spacing](http://www.w3school.com.cn/cssref/pr_tab_border-spacing.asp) | 设置分隔单元格边框的距离。           |
| [caption-side](http://www.w3school.com.cn/cssref/pr_tab_caption-side.asp) | 设置表格标题的位置。                 |
| [empty-cells](http://www.w3school.com.cn/cssref/pr_tab_empty-cells.asp) | 设置是否显示表格中的空单元格。       |
| [table-layout](http://www.w3school.com.cn/cssref/pr_tab_table-layout.asp) | 设置显示单元、行和列的算法。         |



## CSS 轮廓(描边)



**轮廓（outline）是绘制于元素周围的一条线，位于边框边缘的外围，可起到突出元素的作用。**

**CSS outline 属性规定元素轮廓的样式、颜色和宽度。**

### CSS轮廓(描边)属性

"CSS" 列中的数字指示哪个 CSS 版本定义了该属性。

| 属性                                                         | 描述                             | CSS  |
| ------------------------------------------------------------ | -------------------------------- | ---- |
| [outline](http://www.w3school.com.cn/cssref/pr_outline.asp)  | 在一个声明中设置所有的轮廓属性。 | 2    |
| [outline-color](http://www.w3school.com.cn/cssref/pr_outline-color.asp) | 设置轮廓的颜色。                 | 2    |
| [outline-style](http://www.w3school.com.cn/cssref/pr_outline-style.asp) | 设置轮廓的样式。                 | 2    |
| [outline-width](http://www.w3school.com.cn/cssref/pr_outline-width.asp) | 设置轮廓的宽度。                 | 2    |

## CSS 盒子模型概述

**CSS 盒子模型 (Box Model) 规定了元素框处理元素内容、内边距、边框 和 外边距 的方式。** 

我们把 padding 和 margin 统一地称为内边距和外边距。边框内的空白是内边距，边框外的空白是外边距，很容易记吧：） 

所谓盒子模型就是把HTML页面中的元素看作是一个矩形的盒子，也就是一个盛装内容的容器。每个矩形都由元素的内容、内边距（padding）、边框（border）和外边距（margin）组成。

### CSS 内边距

**元素的内边距在边框和内容区之间。控制该区域最简单的属性是 padding 属性。**

**CSS padding 属性定义元素边框与元素内容之间的空白区域。**

**CSS 内边距属性**

| 属性                                                         | 描述                                                 |
| ------------------------------------------------------------ | ---------------------------------------------------- |
| [padding](http://www.w3school.com.cn/cssref/pr_padding.asp)  | 简写属性。作用是在一个声明中设置元素的所内边距属性。 |
| [padding-bottom](http://www.w3school.com.cn/cssref/pr_padding-bottom.asp) | 设置元素的下内边距。                                 |
| [padding-left](http://www.w3school.com.cn/cssref/pr_padding-left.asp) | 设置元素的左内边距。                                 |
| [padding-right](http://www.w3school.com.cn/cssref/pr_padding-right.asp) | 设置元素的右内边距。                                 |
| [padding-top](http://www.w3school.com.cn/cssref/pr_padding-top.asp) | 设置元素的上内边距。                                 |

**注意简写属性**

简写属性的值,是按照,顺时针,排列实现的,上右下左

一个值代表:上下左右都一样.

两个值代表:第一个值代表上下,第二个值,代表左右

三个值代表::第一个值代表上,第二个值,代表左右,第三个值代表:下

四个值代表: 对应的上右下左

## CSS 边框

**元素的边框 (border) 是围绕元素内容和内边距的一条或多条线。**

**CSS border 属性允许你规定元素边框的样式、宽度和颜色。**

一般简写:

```css
border: 1px solid blank;
```



### CSS 边框属性

| 属性                                                         | 描述                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| [border](http://www.w3school.com.cn/cssref/pr_border.asp)    | 简写属性，用于把针对四个边的属性设置在一个声明。             |
| [border-style](http://www.w3school.com.cn/cssref/pr_border-style.asp) | 用于设置元素所有边框的样式，或者单独地为各边设置边框样式。   |
| [border-width](http://www.w3school.com.cn/cssref/pr_border-width.asp) | 简写属性，用于为元素的所有边框设置宽度，或者单独地为各边边框设置宽度。 |
| [border-color](http://www.w3school.com.cn/cssref/pr_border-color.asp) | 简写属性，设置元素的所有边框中可见部分的颜色，或为 4 个边分别设置颜色。 |
| [border-bottom](http://www.w3school.com.cn/cssref/pr_border-bottom.asp) | 简写属性，用于把下边框的所有属性设置到一个声明中。           |
| [border-bottom-color](http://www.w3school.com.cn/cssref/pr_border-bottom_color.asp) | 设置元素的下边框的颜色。                                     |
| [border-bottom-style](http://www.w3school.com.cn/cssref/pr_border-bottom_style.asp) | 设置元素的下边框的样式。                                     |
| [border-bottom-width](http://www.w3school.com.cn/cssref/pr_border-bottom_width.asp) | 设置元素的下边框的宽度。                                     |
| [border-left](http://www.w3school.com.cn/cssref/pr_border-left.asp) | 简写属性，用于把左边框的所有属性设置到一个声明中。           |
| [border-left-color](http://www.w3school.com.cn/cssref/pr_border-left_color.asp) | 设置元素的左边框的颜色。                                     |
| [border-left-style](http://www.w3school.com.cn/cssref/pr_border-left_style.asp) | 设置元素的左边框的样式。                                     |
| [border-left-width](http://www.w3school.com.cn/cssref/pr_border-left_width.asp) | 设置元素的左边框的宽度。                                     |
| [border-right](http://www.w3school.com.cn/cssref/pr_border-right.asp) | 简写属性，用于把右边框的所有属性设置到一个声明中。           |
| [border-right-color](http://www.w3school.com.cn/cssref/pr_border-right_color.asp) | 设置元素的右边框的颜色。                                     |
| [border-right-style](http://www.w3school.com.cn/cssref/pr_border-right_style.asp) | 设置元素的右边框的样式。                                     |
| [border-right-width](http://www.w3school.com.cn/cssref/pr_border-right_width.asp) | 设置元素的右边框的宽度。                                     |
| [border-top](http://www.w3school.com.cn/cssref/pr_border-top.asp) | 简写属性，用于把上边框的所有属性设置到一个声明中。           |
| [border-top-color](http://www.w3school.com.cn/cssref/pr_border-top_color.asp) | 设置元素的上边框的颜色。                                     |
| [border-top-style](http://www.w3school.com.cn/cssref/pr_border-top_style.asp) | 设置元素的上边框的样式。                                     |
| [border-top-width](http://www.w3school.com.cn/cssref/pr_border-top_width.asp) | 设置元素的上边框的宽度。                                     |

## CSS 外边距

**围绕在元素边框的空白区域是外边距。设置外边距会在元素外创建额外的“空白”。**

**设置外边距的最简单的方法就是使用 margin 属性，这个属性接受任何长度单位、百分数值甚至负值。**

设置外边距的最简单的方法就是使用 [margin 属性](http://www.w3school.com.cn/cssref/pr_margin.asp)。

margin 属性接受任何长度单位，可以是像素、英寸、毫米或 em。

### CSS 外边距属性

| 属性                                                         | 描述                                       |
| ------------------------------------------------------------ | ------------------------------------------ |
| [margin](http://www.w3school.com.cn/cssref/pr_margin.asp)    | 简写属性。在一个声明中设置所有外边距属性。 |
| [margin-bottom](http://www.w3school.com.cn/cssref/pr_margin-bottom.asp) | 设置元素的下外边距。                       |
| [margin-left](http://www.w3school.com.cn/cssref/pr_margin-left.asp) | 设置元素的左外边距。                       |
| [margin-right](http://www.w3school.com.cn/cssref/pr_margin-right.asp) | 设置元素的右外边距。                       |
| [margin-top](http://www.w3school.com.cn/cssref/pr_margin-top.asp) | 设置元素的上外边距。                       |

**简写的取值顺序跟内边距相同。**

### 外边距实现盒子居中

可以让一个盒子实现水平居中，需要满足一下两个条件：

1. 必须是块级元素。     
2. 盒子必须指定了宽度（width）

然后就给**左右的外边距都设置为auto**，就可使块级元素水平居中。

实际工作中常用这种方式进行网页布局，示例代码如下：

```css
.header{ width:960px; margin:0 auto;}
```

### 外边距合并

外边距合并（叠加）是一个相当简单的概念。但是，在实践中对网页进行布局时，它会造成许多混淆。

简单地说，外边距合并指的是，当两个垂直外边距相遇时，它们将形成一个外边距。合并后的外边距的高度等于两个发生合并的外边距的高度中的较大者。

## css盒子模型布局稳定性

开始学习盒子模型，同学们最大的困惑就是， 分不清内外边距的使用，什么情况下使用内边距，什么情况下使用外边距？

答案是：  其实他们大部分情况下是可以混用的。  就是说，你用内边距也可以，用外边距也可以。 你觉得哪个方便，就用哪个。

但是，总有一个最好用的吧，我们根据稳定性来分，建议如下：

按照 优先使用  宽度 （width）  其次 使用内边距（padding）    再次  外边距（margin）。   

```
  width >  padding  >   margin   

```

原因：

1. margin 会有外边距合并 还有 ie6下面margin 加倍的bug（讨厌）所以最后使用。

2. padding  会影响盒子大小， 需要进行加减计算（麻烦） 其次使用。

3. width   没有问题（嗨皮）我们经常使用宽度剩余法 高度剩余法来做。

   # CSS 定位 

## CSS 定位

CSS 有三种基本的定位机制：普通流、浮动和绝对定位。

除非专门指定，否则所有框都在普通流中定位。也就是说，普通流中的元素的位置由元素在 (X)HTML 中的位置决定。

块级框从上到下一个接一个地排列，框之间的垂直距离是由框的垂直外边距计算出来。

行内框在一行中水平布置。可以使用水平内边距、边框和外边距调整它们的间距。但是，垂直内边距、边框和外边距不影响行内框的高度。由一行形成的水平框称为*行框（Line Box）*，行框的高度总是足以容纳它包含的所有行内框。不过，设置行高可以增加这个框的高度

**语法:**

```css
box_position{
  position:absolute;
  left:100px;
  top:150px;
  }
```



### CSS 定位属性

CSS 定位属性允许你对元素进行定位。

| 属性                                                         | 描述                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| [position](http://www.w3school.com.cn/cssref/pr_class_position.asp) | 把元素放置到一个静态的、相对的、绝对的、或固定的位置中。     |
| [top](http://www.w3school.com.cn/cssref/pr_pos_top.asp)      | 定义了一个定位元素的上外边距边界与其包含块上边界之间的偏移。 |
| [right](http://www.w3school.com.cn/cssref/pr_pos_right.asp)  | 定义了定位元素右外边距边界与其包含块右边界之间的偏移。       |
| [bottom](http://www.w3school.com.cn/cssref/pr_pos_bottom.asp) | 定义了定位元素下外边距边界与其包含块下边界之间的偏移。       |
| [left](http://www.w3school.com.cn/cssref/pr_pos_left.asp)    | 定义了定位元素左外边距边界与其包含块左边界之间的偏移。       |
| [overflow](http://www.w3school.com.cn/cssref/pr_pos_overflow.asp) | 设置当元素的内容溢出其区域时发生的事情。                     |
| [clip](http://www.w3school.com.cn/cssref/pr_pos_clip.asp)    | 设置元素的形状。元素被剪入这个形状之中，然后显示出来。       |
| [vertical-align](http://www.w3school.com.cn/cssref/pr_pos_vertical-align.asp) | 设置元素的垂直对齐方式。                                     |
| [z-index](http://www.w3school.com.cn/cssref/pr_pos_z-index.asp) | 设置元素的堆叠顺序。                                         |

## CSS 浮动

**浮动的框可以向左或向右移动，直到它的外边缘碰到包含框或另一个浮动框的边框为止。**

**由于浮动框不在文档的普通流中，所以文档的普通流中的块框表现得就像浮动框不存在一样。**



浮动最早是用来控制图片，以便达到其他元素（特别是文字）实现“环绕”图片的效果。



后来，我们发现浮动有个很有意思的事情：就是让任何盒子可以一行排列,因此我们就慢慢的偏离主题，用浮动的特性来布局了。（CSS3已经我们真正意义上的网页布局，具体CSS3我们会详细解释）

**什么是浮动？**

元素的浮动是指设置了浮动属性的元素会脱离标准标准流的控制，移动到其父元素中指定位置的过程。

在CSS中，通过float属性来定义浮动，其基本语法格式如下：

```
选择器{float:属性值;}

```

| 属性值 | 描述                 |
| ------ | -------------------- |
| left   | 元素向左浮动         |
| right  | 元素向右浮动         |
| none   | 元素不浮动（默认值） |

## 浮动详细内幕特性

浮动脱离标准流，====脱标==== 不占位置，会影响标准流。浮动只有左右浮动。