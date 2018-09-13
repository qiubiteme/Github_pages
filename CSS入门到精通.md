



# CSS入门

## CSS 简介



- CSS 指层叠样式表 (*C*ascading *S*tyle *S*heets)

- 样式定义*如何显示* HTML 元素

- 样式通常存储在*样式表*中

- 把样式添加到 HTML 4.0 中，是为了*解决内容与表现分离的问题*

- *外部样式表*可以极大提高工作效率

- 外部样式表通常存储在 *CSS 文件*中

- 多个样式定义可*层叠*为一


### 层叠次序

  **当同一个 HTML 元素被不止一个样式定义时，会使用哪个样式呢？**

  一般而言，所有的样式会根据下面的规则层叠于一个新的虚拟样式表中，其中数字 4 拥有最高的优先权。

  1. 浏览器缺省设置
  2. 外部样式表
  3. 内部样式表（位于 <head> 标签内部）
  4. 内联样式（在 HTML 元素内部）

  因此，内联样式（在 HTML 元素内部）拥有最高的优先权，这意味着它将优先于以下的样式声明：<head> 标签中的样式声明，外部样式表中的样式声明，或者浏览器中的样式声明（缺省值）。

### 插入样式表

#### 外部样式表

当样式需要应用于很多页面时，外部样式表将是理想的选择。在使用外部样式表的情况下，你可以通过改变一个文件来改变整个站点的外观。每个页面使用 <link> 标签链接到样式表。<link> 标签在（文档的）头部：

```
<head>
<link rel="stylesheet" type="text/css" href="mystyle.css" />
</head>
```

浏览器会从文件 mystyle.css 中读到样式声明，并根据它来格式文档。

外部样式表可以在任何文本编辑器中进行编辑。文件不能包含任何的 html 标签。样式表应该以 .css 扩展名进行保存。下面是一个样式表文件的例子：

```
hr {color: sienna;}
p {margin-left: 20px;}
body {background-image: url("images/back40.gif");}
```

不要在属性值与单位之间留有空格。假如你使用 “margin-left: 20 px” 而不是 “margin-left: 20px” ，它仅在 IE 6 中有效，但是在 Mozilla/Firefox 或 Netscape 中却无法正常工作。

#### 内部样式表

当单个文档需要特殊的样式时，就应该使用内部样式表。你可以使用 <style> 标签在文档头部定义内部样式表，就像这样:

```
<head>
<style type="text/css">
  hr {color: sienna;}
  p {margin-left: 20px;}
  body {background-image: url("images/back40.gif");}
</style>
</head>
```

#### 内联样式

由于要将表现和内容混杂在一起，内联样式会损失掉样式表的许多优势。请慎用这种方法，例如当样式仅需要在一个元素上应用一次时。

要使用内联样式，你需要在相关的标签内使用样式（style）属性。Style 属性可以包含任何 CSS 属性。本例展示如何改变段落的颜色和左外边距：

```
<p style="color: sienna; margin-left: 20px">
This is a paragraph
</p>
```

## CSS 基础语法

### CSS 语法

CSS 规则由两个主要的部分构成：选择器，以及一条或多条声明。

```
h1 {color:red; font-size:14px;}
```

选择器通常是您需要改变样式的 HTML 元素。

每条声明由一个属性和一个值组成。

属性（property）是您希望设置的样式属性（style attribute）。每个属性有一个值。属性和值被冒号分开。

下面这行代码的作用是将 h1 元素内的文字颜色定义为红色，同时将字体大小设置为 14 像素。

在这个例子中，h1 是选择器，color 和 font-size 是属性，red 和 14px 是值。

### 多重声明：

提示：如果要定义不止一个声明，则需要用分号将每个声明分开。下面的例子展示出如何定义一个红色文字的居中段落。最后一条规则是不需要加分号的，因为分号在英语中是一个分隔符号，不是结束符号。然而，大多数有经验的设计师会在每条声明的末尾都加上分号，这么做的好处是，当你从现有的规则中增减声明时，会尽可能地减少出错的可能性。就像这样：

你应该在每行只描述一个属性，这样可以增强样式定义的可读性，就像这样：

```
p {
  text-align: center;
  color: black;
  font-family: arial;
}
```

**空格和大小写**

大多数样式表包含不止一条规则，而大多数规则包含不止一个声明。多重声明和空格的使用使得样式表更容易被编辑：

是否包含空格不会影响 CSS 在浏览器的工作效果，同样，与 XHTML 不同，CSS 对大小写不敏感。不过存在一个例外：如果涉及到与 HTML 文档一起工作的话，class 和 id 名称对大小写是敏感的。

## CSS 高级语法

### 选择器的分组

你可以对选择器进行分组，这样，被分组的选择器就可以分享相同的声明。用逗号将需要分组的选择器分开。在下面的例子中，我们对所有的标题元素进行了分组。所有的标题元素都是绿色的。

```
h1,h2,h3,h4,h5,h6 {
  color: green;
  }
```

### 继承及其问题

根据 CSS，子元素从父元素继承属性。但是它并不总是按此方式工作。看看下面这条规则：

```
body {
     font-family: Verdana, sans-serif;
     }
```

根据上面这条规则，站点的 body 元素将使用 Verdana 字体（假如访问者的系统中存在该字体的话）。

通过 CSS 继承，子元素将继承最高级元素（在本例中是 body）所拥有的属性（这些子元素诸如 p, td, ul, ol, ul, li, dl, dt,和 dd）。不需要另外的规则，所有 body 的子元素都应该显示 Verdana 字体，子元素的子元素也一样。并且在大部分的现代浏览器中，也确实是这样的。

## CSS选择器

**通过依据元素在其位置的上下文关系来定义样式，你可以使标记更加简洁。**

在 CSS1 中，通过这种方式来应用规则的选择器被称为上下文选择器 (contextual selectors)，这是由于它们依赖于上下文关系来应用或者避免某项规则。在 CSS2 中，它们称为派生选择器，但是无论你如何称呼它们，它们的作用都是相同的。

派生选择器允许你根据文档的上下文关系来确定某个标签的样式。通过合理地使用派生选择器，我们可以使 HTML 代码变得更加整洁。

比方说，你希望列表中的 strong 元素变为斜体字，而不是通常的粗体字，可以这样定义一个派生选择器：

```
li p {
    color: red;
    height: 40px;
  }
```

### 后代选择器

根据上下文选择元素

我们可以定义后代选择器来创建一些规则，使这些规则在某些文档结构中起作用，而在另外一些结构中不起作用。

举例来说，如果您希望只对 h1 元素中的 em 元素应用样式，可以这样写：

```
h1 em {color:red;}
```

上面这个规则会把作为 h1 元素后代的 em 元素的文本变为 红色。其他 em 文本（如段落或块引用中的 em）则不会被这个规则选中：

**子元素选择器（Child selectors）只能选择作为某元素子元素的元素。**

### 子元素选择器

如果您不希望选择任意的后代元素，而是希望缩小范围，只选择某个元素的子元素，请使用子元素选择器（Child selector）。

例如，如果您希望选择只作为 h1 元素子元素的 strong 元素，可以这样写：

```
h1 > strong {color:red;}
```

这个规则会把第一个 h1 下面的两个 strong 元素变为红色，但是第二个 h1 中的 strong 不受影响：

**语法解释**

您应该已经注意到了，子选择器使用了大于号（子结合符）。

### 相邻兄弟选择器

如果需要选择紧接在另一个元素后的元素，而且二者有相同的父元素，可以使用相邻兄弟选择器（Adjacent sibling selector）。

例如，如果要增加紧接在 h1 元素后出现的段落的上边距，可以这样写：

```
h1 + p {margin-top:50px;}
```

这个选择器读作：“选择紧接在 h1 元素后出现的段落，h1 和 p 元素拥有共同的父元素”。

**语法解释**

相邻兄弟选择器使用了加号（+），即相邻兄弟结合符

### CSS id 选择器



**id 选择器可以为标有特定 id 的 HTML 元素指定特定的样式。**

**id 选择器以 "#" 来定义。**

下面的两个 id 选择器，第一个可以定义元素的颜色为红色，第二个定义元素的颜色为绿色：

```
#red {color:red;}
#green {color:green;}
```

下面的 HTML 代码中，id 属性为 red 的 p 元素显示为红色，而 id 属性为 green 的 p 元素显示为绿色。

```
<p id="red">这个段落是红色。</p>
<p id="green">这个段落是绿色。</p>
```

注意：id 属性只能在每个 HTML 文档中出现一次

**在现代布局中，id 选择器常常用于建组合。**

### CSS 类选择器

**在 CSS 中，类选择器以一个点号显示：**

```
.center {text-align: center}
```

在上面的例子中，所有拥有 center 类的 HTML 元素均为居中。

**注意：类名的第一个字符不能使用数字！它无法在 Mozilla 或 Firefox 中起作用。**

### 属性选择器

**对带有指定属性的 HTML 元素设置样式。**

可以为拥有指定属性的 HTML 元素设置样式，而不仅限于 class 和 id 属性。

注释：只有在规定了 !DOCTYPE 时，IE7 和 IE8 才支持属性选择器。在 IE6 及更低的版本中，不支持属性选择。

**属性选择器**

下面的例子为带有 title 属性的所有元素设置样式：

```
[title]
{
color:red;
}
```

**设置表单的样式**

**属性选择器在为不带有 class 或 id 的表单设置样式时特别有用：**

```
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

#### CSS 选择器参考手册

| 选择器                                                       | 描述                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| [[*attribute*\]](http://www.w3school.com.cn/cssref/selector_attribute.asp) | 用于选取带有指定属性的元素。                                 |
| [[*attribute*=*value*\]](http://www.w3school.com.cn/cssref/selector_attribute_value.asp) | 用于选取带有指定属性和值的元素。                             |
| [[*attribute*~=*value*\]](http://www.w3school.com.cn/cssref/selector_attribute_value_contain.asp) | 用于选取属性值中包含指定词汇的元素。                         |
| [[*attribute*\|=*value*\]](http://www.w3school.com.cn/cssref/selector_attribute_value_start.asp) | 用于选取带有以指定值开头的属性值的元素，该值必须是整个单词。 |
| [[*attribute*^=*value*\]](http://www.w3school.com.cn/cssref/selector_attr_begin.asp) | 匹配属性值以指定值开头的每个元素。                           |
| [[*attribute*$=*value*\]](http://www.w3school.com.cn/cssref/selector_attr_end.asp) | 匹配属性值以指定值结尾的每个元素。                           |
| [[*attribute**=*value*\]](http://www.w3school.com.cn/cssref/selector_attr_contain.asp) | 匹配属性值中包含指定值的每个元素。                           |

## CSS 背景

**CSS 允许应用纯色作为背景，也允许使用背景图像创建相当复杂的效果。**

**CSS 在这方面的能力远远在 HTML 之上。**

### 背景色

可以使用 [background-color 属性](http://www.w3school.com.cn/cssref/pr_background-color.asp)为元素设置背景色。这个属性接受任何合法的颜色值。

这条规则把元素的背景设置为灰色：

```
p {background-color: gray;}
```

**background-color 不能继承，其默认值是 transparent。transparent 有“透明”之意。也就是说，如果一个元素没有指定背景色，那么背景就是透明的，这样其祖先元素的背景才能可见。**

### 背景图像

要把图像放入背景，需要使用 [background-image 属性](http://www.w3school.com.cn/cssref/pr_background-image.asp)。background-image 属性的默认值是 none，表示背景上没有放置任何图像。

如果需要设置一个背景图像，必须为这个属性设置一个 URL 值：

```
body {background-image: url(/i/eg_bg_04.gif);}
```

大多数背景都应用到 body 元素，不过并不仅限于此。

### 背景重复

如果需要在页面上对背景图像进行平铺，可以使用 [background-repeat 属性](http://www.w3school.com.cn/cssref/pr_background-repeat.asp)。

属性值 repeat 导致图像在水平垂直方向上都平铺，就像以往背景图像的通常做法一样。repeat-x 和 repeat-y 分别导致图像只在水平或垂直方向上重复，no-repeat 则不允许图像在任何方向上平铺。

默认地，背景图像将从一个元素的左上角开始。请看下面的例子：

```
body
  { 
  background-image: url(/i/eg_bg_03.gif);
  background-repeat: repeat-y;
  }
```

### 背景定位

可以利用 [background-position 属性](http://www.w3school.com.cn/cssref/pr_background-position.asp)改变图像在背景中的位置。

下面的例子在 body 元素中将一个背景图像居中放置：

```
body
  { 
    background-image:url('/i/eg_bg_03.gif');
    background-repeat:no-repeat;
    background-position:center;
  }
```

为 background-position 属性提供值有很多方法。首先，可以使用一些关键字：top、bottom、left、right 和 center。通常，这些关键字会成对出现，不过也不总是这样。还可以使用长度值，如 100px 或 5cm，最后也可以使用百分数值。不同类型的值对于背景图像的放置稍有差异。

### 关键字

图像放置关键字最容易理解，其作用如其名称所表明的。例如，top right 使图像放置在元素内边距区的右上角。

根据规范，位置关键字可以按任何顺序出现，只要保证不超过两个关键字 - 一个对应水平方向，另一个对应垂直方向。

如果只出现一个关键字，则认为另一个关键字是 center。

所以，如果希望每个段落的中部上方出现一个图像，只需声明如下：

```
p
  { 
    background-image:url('bgimg.gif');
    background-repeat:no-repeat;
    background-position:top;
  }
```

下面是等价的位置关键字：

| 单一关键字 | 等价的关键字                   |
| ---------- | ------------------------------ |
| center     | center center                  |
| top        | top center 或 center top       |
| bottom     | bottom center 或 center bottom |
| right      | right center 或 center right   |
| left       | left center 或 center left     |

### 百分数值

百分数值的表现方式更为复杂。假设你希望用百分数值将图像在其元素中居中，这很容易：

```
body
  { 
    background-image:url('/i/eg_bg_03.gif');
    background-repeat:no-repeat;
    background-position:50% 50%;
  }
```

这会导致图像适当放置，其中心与其元素的中心对齐。**换句话说，百分数值同时应用于元素和图像。**也就是说，图像中描述为 50% 50% 的点（中心点）与元素中描述为 50% 50% 的点（中心点）对齐。

如果图像位于 0% 0%，其左上角将放在元素内边距区的左上角。如果图像位置是 100% 100%，会使图像的右下角放在右边距的右下角。

因此，如果你想把一个图像放在水平方向 2/3、垂直方向 1/3 处，可以这样声明：

```
body
  { 
    background-image:url('/i/eg_bg_03.gif');
    background-repeat:no-repeat;
    background-position:66% 33%;
  }
```

如果只提供一个百分数值，所提供的这个值将用作水平值，垂直值将假设为 50%。这一点与关键字类似。

background-position 的默认值是 0% 0%，在功能上相当于 top left。这就解释了背景图像为什么总是从元素内边距区的左上角开始平铺，除非您设置了不同的位置值。

### 长度值

长度值解释的是元素内边距区左上角的偏移。偏移点是图像的左上角。

比如，如果设置值为 50px 100px，图像的左上角将在元素内边距区左上角向右 50 像素、向下 100 像素的位置上：

```
body
  { 
    background-image:url('/i/eg_bg_03.gif');
    background-repeat:no-repeat;
    background-position:50px 100px;
  }
```

注意，这一点与百分数值不同，因为偏移只是从一个左上角到另一个左上角。也就是说，图像的左上角与 background-position 声明中的指定的点对齐。

### 背景关联

如果文档比较长，那么当文档向下滚动时，背景图像也会随之滚动。当文档滚动到超过图像的位置时，图像就会消失。

您可以通过 [background-attachment 属性](http://www.w3school.com.cn/cssref/pr_background-attachment.asp)防止这种滚动。通过这个属性，可以声明图像相对于可视区是固定的（fixed），因此不会受到滚动的影响：

```
body 
  {
  background-image:url(/i/eg_bg_02.gif);
  background-repeat:no-repeat;
  background-attachment:fixed
  }
```

如需查看上例的效果，可以[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_background-attachment)。



background-attachment 属性的默认值是 scroll，也就是说，在默认的情况下，背景会随文档滚动。

### CSS 背景属性

| 属性                                                         | 描述                                         |
| ------------------------------------------------------------ | -------------------------------------------- |
| [background](http://www.w3school.com.cn/cssref/pr_background.asp) | 简写属性，作用是将背景属性设置在一个声明中。 |
| [background-attachment](http://www.w3school.com.cn/cssref/pr_background-attachment.asp) | 背景图像是否固定或者随着页面的其余部分滚动。 |
| [background-color](http://www.w3school.com.cn/cssref/pr_background-color.asp) | 设置元素的背景颜色。                         |
| [background-image](http://www.w3school.com.cn/cssref/pr_background-image.asp) | 把图像设置为背景。                           |
| [background-position](http://www.w3school.com.cn/cssref/pr_background-position.asp) | 设置背景图像的起始位置。                     |
| [background-repeat](http://www.w3school.com.cn/cssref/pr_background-repeat.asp) | 设置背景图像是否及如何重复。                 |

## CSS 文本

**CSS 文本属性可定义文本的外观。**

**通过文本属性，您可以改变文本的颜色、字符间距，对齐文本，装饰文本，对文本进行缩进，等等。**

### 缩进文本

把 Web 页面上的段落的第一行缩进，这是一种最常用的文本格式化效果。

CSS 提供了 [text-indent 属性](http://www.w3school.com.cn/cssref/pr_text_text-indent.asp)，该属性可以方便地实现文本缩进。

通过使用 text-indent 属性，所有元素的第一行都可以缩进一个给定的长度，甚至该长度可以是负值。

这个属性最常见的用途是将段落的首行缩进，下面的规则会使所有段落的首行缩进 5 em：

```
p {text-indent: 5em;}
```

注意：一般来说，可以为所有块级元素应用 text-indent，但无法将该属性应用于行内元素，图像之类的替换元素上也无法应用 text-indent 属性。不过，如果一个块级元素（比如段落）的首行中有一个图像，它会随该行的其余文本移动。

提示：如果想把一个行内元素的第一行“缩进”，可以用左内边距或外边距创造这种效果。

#### 使用负值

text-indent 还可以设置为负值。利用这种技术，可以实现很多有趣的效果，比如“悬挂缩进”，即第一行悬挂在元素中余下部分的左边：

```
p {text-indent: -5em;}
```

不过在为 text-indent 设置负值时要当心，如果对一个段落设置了负值，那么首行的某些文本可能会超出浏览器窗口的左边界。为了避免出现这种显示问题，建议针对负缩进再设置一个外边距或一些内边距：

```
p {text-indent: -5em; padding-left: 5em;}
```

#### 使用百分比值

text-indent 可以使用所有长度单位，包括百分比值。

百分数要相对于缩进元素父元素的宽度。换句话说，如果将缩进值设置为 20%，所影响元素的第一行会缩进其父元素宽度的 20%。

在下例中，缩进值是父元素的 20%，即 100 个像素：

```
div {width: 500px;}
p {text-indent: 20%;}

<div>
<p>this is a paragragh</p>
</div>
```

#### 继承

text-indent 属性可以继承，请考虑如下标记：

### 水平对齐

[text-align](http://www.w3school.com.cn/cssref/pr_text_text-align.asp) 是一个基本的属性，它会影响一个元素中的*文本行*互相之间的对齐方式。它的前 3 个值相当直接，不过第 4 个和第 5 个则略有些复杂。

值 left、right 和 center 会导致元素中的文本分别左对齐、右对齐和居中。

西方语言都是从左向右读，所有 text-align 的默认值是 left。文本在左边界对齐，右边界呈锯齿状（称为“从左到右”文本）。对于希伯来语和阿拉伯语之类的的语言，text-align 则默认为 right，因为这些语言从右向左读。不出所料，center 会使每个文本行在元素中居中。

提示：将块级元素或表元素居中，要通过在这些元素上适当地设置左、右外边距来实现。

#### text-align:center 与 <CENTER>

您可能会认为 text-align:center 与 <CENTER> 元素的作用一样，但实际上二者大不相同。

<CENTER> 不仅影响文本，还会把整个元素居中。text-align 不会控制元素的对齐，而只影响内部内容。元素本身不会从一段移到另一端，只是其中的文本受影响。

#### justify

最后一个水平对齐属性是 justify。

在两端对齐文本中，文本行的左右两端都放在父元素的内边界上。然后，调整单词和字母间的间隔，使各行的长度恰好相等。您也许已经注意到了，两端对齐文本在打印领域很常见。

需要注意的是，要由用户代理（而不是 CSS）来确定两端对齐文本如何拉伸，以填满父元素左右边界之间的空间。如需了解详情，请参阅 [CSS text-align 属性参考页](http://www.w3school.com.cn/cssref/pr_text_text-align.asp)。

### 字符间隔

[word-spacing 属性](http://www.w3school.com.cn/cssref/pr_text_word-spacing.asp)可以改变字（单词）之间的标准间隔。其默认值 normal 与设置值为 0 是一样的。

word-spacing 属性接受一个正长度值或负长度值。如果提供一个正长度值，那么字之间的间隔就会增加。为 word-spacing 设置一个负值，会把它拉近：

```
p.spread {word-spacing: 30px;}
p.tight {word-spacing: -0.5em;}

<p class="spread">
This is a paragraph. The spaces between words will be increased.
</p>

<p class="tight">
This is a paragraph. The spaces between words will be decreased.
</p>
```

### 字母间隔

[letter-spacing 属性](http://www.w3school.com.cn/cssref/pr_text_letter-spacing.asp)与 word-spacing 的区别在于，字母间隔修改的是字符或字母之间的间隔。

与 word-spacing 属性一样，letter-spacing 属性的可取值包括所有长度。默认关键字是 normal（这与 letter-spacing:0 相同）。输入的长度值会使字母之间的间隔增加或减少指定的量：

```
h1 {letter-spacing: -0.5em}
h4 {letter-spacing: 20px}

<h1>This is header 1</h1>
<h4>This is header 4</h4>
```

### 字符转换

[text-transform 属性](http://www.w3school.com.cn/cssref/pr_text_text-transform.asp)处理文本的大小写。这个属性有 4 个值：

- none
- uppercase
- lowercase
- capitalize

默认值 none 对文本不做任何改动，将使用源文档中的原有大小写。顾名思义，uppercase 和 lowercase 将文本转换为全大写和全小写字符。最后，capitalize 只对每个单词的首字母大写。

作为一个属性，text-transform 可能无关紧要，不过如果您突然决定把所有 h1 元素变为大写，这个属性就很有用。不必单独地修改所有 h1 元素的内容，只需使用 text-transform 为你完成这个修改：

```
h1 {text-transform: uppercase}
```

使用 text-transform 有两方面的好处。首先，只需写一个简单的规则来完成这个修改，而无需修改 h1 元素本身。其次，如果您以后决定将所有大小写再切换为原来的大小写，可以更容易地完成修改。

### 文本装饰

接下来，我们讨论 [text-decoration 属性](http://www.w3school.com.cn/cssref/pr_text_text-decoration.asp)，这是一个很有意思的属性，它提供了很多非常有趣的行为。

text-decoration 有 5 个值：

- none
- underline
- overline
- line-through
- blink

不出所料，underline 会对元素加下划线，就像 HTML 中的 U 元素一样。overline 的作用恰好相反，会在文本的顶端画一个上划线。值 line-through 则在文本中间画一个贯穿线，等价于 HTML 中的 S 和 strike 元素。blink 会让文本闪烁，类似于 Netscape 支持的颇招非议的 blink 标记。

none 值会关闭原本应用到一个元素上的所有装饰。通常，无装饰的文本是默认外观，但也不总是这样。例如，链接默认地会有下划线。如果您希望去掉超链接的下划线，可以使用以下 CSS 来做到这一点：

```
a {text-decoration: none;}
```

注意：如果显式地用这样一个规则去掉链接的下划线，那么锚与正常文本之间在视觉上的唯一差别就是颜色（至少默认是这样的，不过也不能完全保证其颜色肯定有区别）。

还可以在一个规则中结合多种装饰。如果希望所有超链接既有下划线，又有上划线，则规则如下：

```
a:link a:visited {text-decoration: underline overline;}
```

不过要注意的是，如果两个不同的装饰都与同一元素匹配，胜出规则的值会完全取代另一个值。请考虑以下的规则：

```
h2.stricken {text-decoration: line-through;}
h2 {text-decoration: underline overline;}
```

对于给定的规则，所有 class 为 stricken 的 h2 元素都只有一个贯穿线装饰，而没有下划线和上划线，因为 *text-decoration 值会替换而不是累积起来*。

### 处理空白符

[white-space 属性](http://www.w3school.com.cn/cssref/pr_text_white-space.asp)会影响到用户代理对源文档中的空格、换行和 tab 字符的处理。

通过使用该属性，可以影响浏览器处理字之间和文本行之间的空白符的方式。从某种程度上讲，默认的 XHTML 处理已经完成了空白符处理：它会把所有空白符合并为一个空格。所以给定以下标记，它在 Web 浏览器中显示时，各个字之间只会显示一个空格，同时忽略元素中的换行：

```
<p>This     paragraph has    many
    spaces           in it.</p>
```

可以用以下声明显式地设置这种默认行为：

```
p {white-space: normal;}
```

上面的规则告诉浏览器按照平常的做法去处理：丢掉多余的空白符。如果给定这个值，换行字符（回车）会转换为空格，一行中多个空格的序列也会转换为一个空格。

#### 值 pre

不过，如果将 white-space 设置为 pre，受这个属性影响的元素中，空白符的处理就有所不同，其行为就像 XHTML 的 pre 元素一样；空白符不会被忽略。

如果 white-space 属性的值为 pre，浏览器将会注意额外的空格，甚至回车。在这个方面，而且仅在这个方面，任何元素都可以相当于一个 pre 元素。

注意：经测试，IE 7 以及更早版本的浏览器不支持该值，因此请使用非 IE 的浏览器来查看上面的实例。

#### 值 nowrap

与之相对的值是 nowrap，它会防止元素中的文本换行，除非使用了一个 br 元素。在 CSS 中使用 nowrap 非常类似于 HTML 4 中用 <td nowrap> 将一个表单元格设置为不能换行，不过 white-space 值可以应用到任何元素。

#### 值 pre-wrap 和 pre-line

CSS2.1 引入了值 pre-wrap 和 pre-line，这在以前版本的 CSS 中是没有的。这些值的作用是允许创作人员更好地控制空白符处理。

如果元素的 white-space 设置为 pre-wrap，那么该元素中的文本会保留空白符序列，但是文本行会正常地换行。如果设置为这个值，源文本中的行分隔符以及生成的行分隔符也会保留。pre-line 与 pre-wrap 相反，会像正常文本中一样合并空白符序列，但保留换行符。

注意：我们在 IE7 和 FireFox2.0 浏览器中测试了上面的两个实例，但是结果是，值 pre-wrap 和 pre-line 都没有得到很好的支持。

### 总结

下面的表格总结了 white-space 属性的行为：

| 值       | 空白符 | 换行符 | 自动换行 |
| -------- | ------ | ------ | -------- |
| pre-line | 合并   | 保留   | 允许     |
| normal   | 合并   | 忽略   | 允许     |
| nowrap   | 合并   | 忽略   | 不允许   |
| pre      | 保留   | 保留   | 不允许   |
| pre-wrap | 保留   | 保留   | 允许     |

### 文本方向

如果您阅读的是英文书籍，就会从左到右、从上到下地阅读，这就是英文的流方向。不过，并不是所有语言都如此。我们知道古汉语就是从右到左来阅读的，当然还包括希伯来语和阿拉伯语等等。CSS2 引入了一个属性来描述其方向性。

[direction 属性](http://www.w3school.com.cn/cssref/pr_text_direction.asp)影响块级元素中文本的书写方向、表中列布局的方向、内容水平填充其元素框的方向、以及两端对齐元素中最后一行的位置。

注释：对于行内元素，只有当 [unicode-bidi 属性](http://www.w3school.com.cn/cssref/pr_unicode-bidi.asp)设置为 embed 或 bidi-override 时才会应用 direction 属性。

direction 属性有两个值：ltr 和 rtl。大多数情况下，默认值是 ltr，显示从左到右的文本。如果显示从右到左的文本，应使用值 rtl。

### CSS 文本属性

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

### CSS 字体系列

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

### 指定字体系列

使用 [font-family 属性](http://www.w3school.com.cn/cssref/pr_font_font-family.asp) 定义文本的字体系列。

### 使用通用字体系列

如果你希望文档使用一种 sans-serif 字体，但是你并不关心是哪一种字体，以下就是一个合适的声明：

```
body {font-family: sans-serif;
```

这样用户代理就会从 sans-serif 字体系列中选择一个字体（如 Helvetica），并将其应用到 body 元素。因为有继承，这种字体选择还将应用到 body 元素中包含的所有元素，除非有一种更特定的选择器将其覆盖。

### 指定字体系列

除了使用通用的字体系列，您还可以通过 font-family 属性设置更具体的字体。

下面的例子为所有 h1 元素设置了 Georgia 字体：

```
h1 {font-family: Georgia;}
```

这样的规则同时会产生另外一个问题，如果用户代理上没有安装 Georgia 字体，就只能使用用户代理的默认字体来显示 h1 元素。

我们可以通过结合特定字体名和通用字体系列来解决这个问题：

```
h1 {font-family: Georgia, serif;}
```

如果读者没有安装 Georgia，但安装了 Times 字体（serif 字体系列中的一种字体），用户代理就可能对 h1 元素使用 Times。尽管 Times 与 Georgia 并不完全匹配，但至少足够接近。

因此，我们建议在所有 font-family 规则中都提供一个通用字体系列。这样就提供了一条后路，在用户代理无法提供与规则匹配的特定字体时，就可以选择一个候选字体。

如果您对字体非常熟悉，也可以为给定的元素指定一系列类似的字体。要做到这一点，需要把这些字体按照优先顺序排列，然后用逗号进行连接：

```
p {font-family: Times, TimesNR, 'New Century Schoolbook',
     Georgia, 'New York', serif;}
```

根据这个列表，用户代理会按所列的顺序查找这些字体。如果列出的所有字体都不可用，就会简单地选择一种可用的 serif 字体。

### 使用引号

您也许已经注意到了，上面的例子中使用了单引号。只有当字体名中有一个或多个空格（比如 New York），或者如果字体名包括 # 或 $ 之类的符号，才需要在 font-family 声明中加引号。

单引号或双引号都可以接受。但是，如果把一个 font-family 属性放在 HTML 的 style 属性中，则需要使用该属性本身未使用的那种引号：

```
<p style="font-family: Times, TimesNR, 'New Century Schoolbook', Georgia,
 'New York', serif;">...</p>
```

### 字体风格

[font-style 属性](http://www.w3school.com.cn/cssref/pr_font_font-style.asp)最常用于规定斜体文本。

该属性有三个值：

- normal - 文本正常显示
- italic - 文本斜体显示
- oblique - 文本倾斜显示

**实例**

```
p.normal {font-style:normal;}
p.italic {font-style:italic;}
p.oblique {font-style:oblique;}
```

### italic 和 oblique 的区别

font-style 非常简单：用于在 normal 文本、italic 文本和 oblique 文本之间选择。唯一有点复杂的是明确 italic 文本和 oblique 文本之间的差别。

斜体（italic）是一种简单的字体风格，对每个字母的结构有一些小改动，来反映变化的外观。与此不同，倾斜（oblique）文本则是正常竖直文本的一个倾斜版本。

通常情况下，italic 和 oblique 文本在 web 浏览器中看上去完全一样。

### 字体变形

[font-variant 属性](http://www.w3school.com.cn/cssref/pr_font_font-variant.asp)可以设定小型大写字母。

小型大写字母不是一般的大写字母，也不是小写字母，这种字母采用不同大小的大写字母。

**实例**

```
p {font-variant:small-caps;}
```

### 字体加粗

[font-weight 属性](http://www.w3school.com.cn/cssref/pr_font_weight.asp)设置文本的粗细。

使用 bold 关键字可以将文本设置为粗体。

关键字 100 ~ 900 为字体指定了 9 级加粗度。如果一个字体内置了这些加粗级别，那么这些数字就直接映射到预定义的级别，100 对应最细的字体变形，900 对应最粗的字体变形。数字 400 等价于 normal，而 700 等价于 bold。

如果将元素的加粗设置为 bolder，浏览器会设置比所继承值更粗的一个字体加粗。与此相反，关键词 lighter 会导致浏览器将加粗度下移而不是上移。

**实例**

```
p.normal {font-weight:normal;}
p.thick {font-weight:bold;}
p.thicker {font-weight:900;}
```

### 字体大小

[font-size 属性](http://www.w3school.com.cn/cssref/pr_font_font-size.asp)设置文本的大小。

有能力管理文本的大小在 web 设计领域很重要。但是，您不应当通过调整文本大小使段落看上去像标题，或者使标题看上去像段落。

请始终使用正确的 HTML 标题，比如使用 <h1> - <h6> 来标记标题，使用 <p> 来标记段落。

font-size 值可以是绝对或相对值。

绝对值：

- 将文本设置为指定的大小
- 不允许用户在所有浏览器中改变文本大小（不利于可用性）
- 绝对大小在确定了输出的物理尺寸时很有用

相对大小：

- 相对于周围的元素来设置大小
- 允许用户在浏览器改变文本大小

注意：如果您没有规定字体大小，普通文本（比如段落）的默认大小是 16 像素 (16px=1em)。

### 使用像素来设置字体大小

通过像素设置文本大小，可以对文本大小进行完全控制：

**实例**

```
h1 {font-size:60px;}
h2 {font-size:40px;}
p {font-size:14px;}
```

在 Firefox, Chrome, and Safari 中，可以重新调整以上例子的文本大小，但是在 Internet Explorer 中不行。

虽然可以通过浏览器的缩放工具调整文本大小，但是这实际上是对整个页面的调整，而不仅限于文本。

### 使用 em 来设置字体大小

如果要避免在 Internet Explorer 中无法调整文本的问题，许多开发者使用 em 单位代替 pixels。

W3C 推荐使用 em 尺寸单位。

1em 等于当前的字体尺寸。如果一个元素的 font-size 为 16 像素，那么对于该元素，1em 就等于 16 像素。在设置字体大小时，em 的值会相对于父元素的字体大小改变。

浏览器中默认的文本大小是 16 像素。因此 1em 的默认尺寸是 16 像素。

可以使用下面这个公式将像素转换为 em：*pixels*/16=*em*

（注：16 等于父元素的默认字体大小，假设父元素的 font-size 为 20px，那么公式需改为：*pixels*/20=*em*）

**实例**

```
h1 {font-size:3.75em;} /* 60px/16=3.75em */
h2 {font-size:2.5em;}  /* 40px/16=2.5em */
p {font-size:0.875em;} /* 14px/16=0.875em */
```

在上面的例子中，以 em 为单位的文本大小与前一个例子中以像素计的文本是相同的。不过，如果使用 em 单位，则可以在所有浏览器中调整文本大小。

不幸的是，在 IE 中仍存在问题。在重设文本大小时，会比正常的尺寸更大或更小。

### 结合使用百分比和 EM

在所有浏览器中均有效的方案是为 body 元素（父元素）以百分比设置默认的 font-size 值：

**实例**

```
body {font-size:100%;}
h1 {font-size:3.75em;}
h2 {font-size:2.5em;}
p {font-size:0.875em;}
```

我们的代码非常有效。在所有浏览器中，可以显示相同的文本大小，并允许所有浏览器缩放文本的大小。

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

**我们能够以不同的方法为链接设置样式。**

### 设置链接的样式

能够设置链接样式的 CSS 属性有很多种（例如 color, font-family, background 等等）。

链接的特殊性在于能够根据它们所处的状态来设置它们的样式。

链接的四种状态：

- a:link - 普通的、未被访问的链接
- a:visited - 用户已访问的链接
- a:hover - 鼠标指针位于链接的上方
- a:active - 链接被点击的时刻

**实例**

```
a:link {color:#FF0000;}		/* 未被访问的链接 */
a:visited {color:#00FF00;}	/* 已被访问的链接 */
a:hover {color:#FF00FF;}	/* 鼠标指针移动到链接上 */
a:active {color:#0000FF;}	/* 正在被点击的链接 */
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css_link)

当为链接的不同状态设置样式时，请按照以下次序规则：

- a:hover 必须位于 a:link 和 a:visited 之后
- a:active 必须位于 a:hover 之后

### 常见的链接样式

在上面的例子中，链接根据其状态改变颜色。

让我们看看其他几种常见的设置链接样式的方法：

#### 文本修饰

text-decoration 属性大多用于去掉链接中的下划线：

**实例**

```
a:link {text-decoration:none;}
a:visited {text-decoration:none;}
a:hover {text-decoration:underline;}
a:active {text-decoration:underline;}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css_link_decoration)

#### 背景色

background-color 属性规定链接的背景色：

**实例**

```
a:link {background-color:#B2FF99;}
a:visited {background-color:#FFFF85;}
a:hover {background-color:#FF704D;}
a:active {background-color:#FF704D;}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css_link_background)

**更多实例**

- [向链接添加不同的样式](http://www.w3school.com.cn/tiy/t.asp?f=css_link2)

  本例演示如何向链接添加其他样式。

- [高级 - 创建链接框](http://www.w3school.com.cn/tiy/t.asp?f=css_link_advanced)

  本例演示了更高级的示例，我们结合了若干种 CSS 属性，来把链接显示为方框。

## CSS 列表

**CSS 列表属性允许你放置、改变列表项标志，或者将图像作为列表项标志。**

### CSS 列表

从某种意义上讲，不是描述性的文本的任何内容都可以认为是列表。人口普查、太阳系、家谱、参观菜单，甚至你的所有朋友都可以表示为一个列表或者是列表的列表。

由于列表如此多样，这使得列表相当重要，所以说，CSS 中列表样式不太丰富确实是一大憾事。

#### 列表类型

要影响列表的样式，最简单（同时支持最充分）的办法就是改变其标志类型。

例如，在一个无序列表中，列表项的标志 (marker) 是出现在各列表项旁边的圆点。在有序列表中，标志可能是字母、数字或另外某种计数体系中的一个符号。

要修改用于列表项的标志类型，可以使用属性 [list-style-type](http://www.w3school.com.cn/cssref/pr_list-style-type.asp)：

```
ul {list-style-type : square}
```

上面的声明把无序列表中的列表项标志设置为方块。

### 列表项图像

有时，常规的标志是不够的。你可能想对各标志使用一个图像，这可以利用 [list-style-image](http://www.w3school.com.cn/cssref/pr_list-style-image.asp) 属性做到：

```
ul li {list-style-image : url(xxx.gif)}
```

只需要简单地使用一个 url() 值，就可以使用图像作为标志。

### 列表标志位置

CSS2.1 可以确定标志出现在列表项内容之外还是内容内部。这是利用 [list-style-position](http://www.w3school.com.cn/cssref/pr_list-style-position.asp) 完成的。

### 简写列表样式

为简单起见，可以将以上 3 个列表样式属性合并为一个方便的属性：[list-style](http://www.w3school.com.cn/cssref/pr_list-style.asp)，就像这样：

```
li {list-style : url(example.gif) square inside}
```

list-style 的值可以按任何顺序列出，而且这些值都可以忽略。只要提供了一个值，其它的就会填入其默认值。

### CSS 列表实例：

- [在无序列表中的不同类型的列表标记](http://www.w3school.com.cn/tiy/t.asp?f=csse_list-style-type)

  本例演示在CSS中不同类型的列表项标记。

- [在有序列表中不同类型的列表项标记](http://www.w3school.com.cn/tiy/t.asp?f=csse_list-style-type2)

  本例演示在CSS中不同类型的列表项标记。

- [所有的列表样式类型](http://www.w3school.com.cn/tiy/t.asp?f=csse_list-style-type_all)

  本例演示在CSS中所有不同类型的列表项标记。

- [将图像作为列表项标记](http://www.w3school.com.cn/tiy/t.asp?f=csse_list-style-image)

  本例演示如何将图像作为列表项标记。

- [放置列表标记](http://www.w3school.com.cn/tiy/t.asp?f=csse_list-style-position)

  本例演示在何处放置列表标记。

- [在一个声明中定义所有的列表属性](http://www.w3school.com.cn/tiy/t.asp?f=csse_list-style)

  本例演示将所有针对列表的属性设置于一个简写属性。

### CSS 列表属性(list)

| 属性                                                         | 描述                                                 |
| ------------------------------------------------------------ | ---------------------------------------------------- |
| [list-style](http://www.w3school.com.cn/cssref/pr_list-style.asp) | 简写属性。用于把所有用于列表的属性设置于一个声明中。 |
| [list-style-image](http://www.w3school.com.cn/cssref/pr_list-style-image.asp) | 将图象设置为列表项标志。                             |
| [list-style-position](http://www.w3school.com.cn/cssref/pr_list-style-position.asp) | 设置列表中列表项标志的位置。                         |
| [list-style-type](http://www.w3school.com.cn/cssref/pr_list-style-type.asp) | 设置列表项标志的类型。                               |
| marker-offset                                                |                                                      |

## CSS 表格



**CSS 表格属性可以帮助您极大地改善表格的外观。**

### 表格边框

如需在 CSS 中设置表格边框，请使用 border 属性。

下面的例子为 table、th 以及 td 设置了蓝色边框：

```
table, th, td
  {
  border: 1px solid blue;
  }
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_table_border)

请注意，上例中的表格具有双线条边框。这是由于 table、th 以及 td 元素都有独立的边框。

如果需要把表格显示为单线条边框，请使用 border-collapse 属性。

### 折叠边框

border-collapse 属性设置是否将表格边框折叠为单一边框：

```
table
  {
  border-collapse:collapse;
  }

table,th, td
  {
  border: 1px solid black;
  }
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_table_border-collapse)

### 表格宽度和高度

通过 width 和 height 属性定义表格的宽度和高度。

下面的例子将表格宽度设置为 100%，同时将 th 元素的高度设置为 50px：

```
table{
  width:100%;
}
th{
  height:50px;
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_table_width)

### 表格文本对齐

text-align 和 vertical-align 属性设置表格中文本的对齐方式。

text-align 属性设置水平对齐方式，比如左对齐、右对齐或者居中：

```
td
  {
  text-align:right;
  }
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_table_align)

vertical-align 属性设置垂直对齐方式，比如顶部对齐、底部对齐或居中对齐：

```
td
  {
  height:50px;
  vertical-align:bottom;
  }
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_table_vertical-align)

### 表格内边距

如需控制表格中内容与边框的距离，请为 td 和 th 元素设置 padding 属性：

```
td{
  padding:15px;
  }
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_table_padding)

### 表格颜色

下面的例子设置边框的颜色，以及 th 元素的文本和背景颜色：

```
table, td, th{
  border:1px solid green;
  }

th {
  background-color:green;
  color:white;
  }
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_table_color)

### CSS Table 属性

| 属性                                                         | 描述                                 |
| ------------------------------------------------------------ | ------------------------------------ |
| [border-collapse](http://www.w3school.com.cn/cssref/pr_tab_border-collapse.asp) | 设置是否把表格边框合并为单一的边框。 |
| [border-spacing](http://www.w3school.com.cn/cssref/pr_tab_border-spacing.asp) | 设置分隔单元格边框的距离。           |
| [caption-side](http://www.w3school.com.cn/cssref/pr_tab_caption-side.asp) | 设置表格标题的位置。                 |
| [empty-cells](http://www.w3school.com.cn/cssref/pr_tab_empty-cells.asp) | 设置是否显示表格中的空单元格。       |
| [table-layout](http://www.w3school.com.cn/cssref/pr_tab_table-layout.asp) | 设置显示单元、行和列的算法。         |

### 亲自试一试 - 更多实例

- [制作一个漂亮的表格](http://www.w3school.com.cn/tiy/t.asp?f=csse_table_fancy)

  本例演示如何创造一个漂亮的表格。

- [显示表格中的空单元](http://www.w3school.com.cn/tiy/t.asp?f=csse_table_empty-cells)

  本例演示是否显示表格中的空单元。

- [设置表格边框之间的空白](http://www.w3school.com.cn/tiy/t.asp?f=csse_table_border-spacing)

  本例演示如何设置单元格边框之间的距离。

- [设置表格标题的位置](http://www.w3school.com.cn/tiy/t.asp?f=csse_table_caption-side)

  本例演示如何定位表格的标题。

## CSS 轮廓

**轮廓（outline）是绘制于元素周围的一条线，位于边框边缘的外围，可起到突出元素的作用。**

**CSS outline 属性规定元素轮廓的样式、颜色和宽度。**

### 轮廓（Outline） 实例：

- [在元素周围画线](http://www.w3school.com.cn/tiy/t.asp?f=csse_outline)

  本例演示使用outline属性在元素周围画一条线。

- [设置轮廓的颜色](http://www.w3school.com.cn/tiy/t.asp?f=csse_outline-color)

  本例演示如何设置轮廓的颜色。

- [设置轮廓的样式](http://www.w3school.com.cn/tiy/t.asp?f=csse_outline-style)

  本例演示如何设置轮廓的样式。

- [设置轮廓的宽度](http://www.w3school.com.cn/tiy/t.asp?f=csse_outline-width)

  本例演示如何设置轮廓的宽度。

### CSS 边框属性

"CSS" 列中的数字指示哪个 CSS 版本定义了该属性。

| 属性                                                         | 描述                             | CSS  |
| ------------------------------------------------------------ | -------------------------------- | ---- |
| [outline](http://www.w3school.com.cn/cssref/pr_outline.asp)  | 在一个声明中设置所有的轮廓属性。 | 2    |
| [outline-color](http://www.w3school.com.cn/cssref/pr_outline-color.asp) | 设置轮廓的颜色。                 | 2    |
| [outline-style](http://www.w3school.com.cn/cssref/pr_outline-style.asp) | 设置轮廓的样式。                 | 2    |
| [outline-width](http://www.w3school.com.cn/cssref/pr_outline-width.asp) | 设置轮廓的宽度。                 | 2    |

# CSS 盒子模型



**CSS 框模型 (Box Model) 规定了元素框处理元素内容、内边距、边框 和 外边距 的方式。**

## CSS 框模型概述



元素框的最内部分是实际的内容，直接包围内容的是内边距。内边距呈现了元素的背景。内边距的边缘是边框。边框以外是外边距，外边距默认是透明的，因此不会遮挡其后的任何元素。

提示：背景应用于由内容和内边距、边框组成的区域。

内边距、边框和外边距都是可选的，默认值是零。但是，许多元素将由用户代理样式表设置外边距和内边距。可以通过将元素的 margin 和 padding 设置为零来覆盖这些浏览器样式。这可以分别进行，也可以使用通用选择器对所有元素进行设置：

```
* {
  margin: 0;
  padding: 0;
}
```

在 CSS 中，width 和 height 指的是内容区域的宽度和高度。增加内边距、边框和外边距不会影响内容区域的尺寸，但是会增加元素框的总尺寸。

假设框的每个边上有 10 个像素的外边距和 5 个像素的内边距。如果希望这个元素框达到 100 个像素，就需要将内容的宽度设置为 70 像素，请看下图：



```
#box {
  width: 70px;
  margin: 10px;
  padding: 5px;
}
```

提示：内边距、边框和外边距可以应用于一个元素的所有边，也可以应用于单独的边。

提示：外边距可以是负值，而且在很多情况下都要使用负值的外边距。

### 浏览器兼容性

一旦为页面设置了恰当的 DTD，大多数浏览器都会按照上面的图示来呈现内容。然而 IE 5 和 6 的呈现却是不正确的。根据 W3C 的规范，元素内容占据的空间是由 width 属性设置的，而内容周围的 padding 和 border 值是另外计算的。不幸的是，IE5.X 和 6 在怪异模式中使用自己的非标准模型。这些浏览器的 width 属性不是内容的宽度，而是内容、内边距和边框的宽度的总和。

虽然有方法解决这个问题。但是目前最好的解决方案是回避这个问题。也就是，不要给元素添加具有指定宽度的内边距，而是尝试将内边距或外边距添加到元素的父元素和子元素。

#### 术语翻译

- element : 元素。
- padding : 内边距，也有资料将其翻译为填充。
- border : 边框。
- margin : 外边距，也有资料将其翻译为空白或空白边。

在 w3school，我们把 padding 和 margin 统一地称为内边距和外边距。边框内的空白是内边距，边框外的空白是外边距，很容易记吧：）

## CSS 内边距



**元素的内边距在边框和内容区之间。控制该区域最简单的属性是 padding 属性。**

**CSS padding 属性定义元素边框与元素内容之间的空白区域。**

### CSS padding 属性

CSS padding 属性定义元素的内边距。padding 属性接受长度值或百分比值，但不允许使用负值。

例如，如果您希望所有 h1 元素的各边都有 10 像素的内边距，只需要这样：

```
h1 {padding: 10px;}
```

您还可以按照上、右、下、左的顺序分别设置各边的内边距，各边均可以使用不同的单位或百分比值：

```
h1 {padding: 10px 0.25em 2ex 20%;}
```

### 单边内边距属性

也通过使用下面四个单独的属性，分别设置上、右、下、左内边距：

- [padding-top](http://www.w3school.com.cn/cssref/pr_padding-top.asp)
- [padding-right](http://www.w3school.com.cn/cssref/pr_padding-right.asp)
- [padding-bottom](http://www.w3school.com.cn/cssref/pr_padding-bottom.asp)
- [padding-left](http://www.w3school.com.cn/cssref/pr_padding-left.asp)

您也许已经想到了，下面的规则实现的效果与上面的简写规则是完全相同的：

```
h1 {
  padding-top: 10px;
  padding-right: 0.25em;
  padding-bottom: 2ex;
  padding-left: 20%;
  }
```

### 内边距的百分比数值

前面提到过，可以为元素的内边距设置百分数值。百分数值是相对于其父元素的 width 计算的，这一点与外边距一样。所以，如果父元素的 width 改变，它们也会改变。

下面这条规则把段落的内边距设置为父元素 width 的 10%：

```
p {padding: 10%;}
```

例如：如果一个段落的父元素是 div 元素，那么它的内边距要根据 div 的 width 计算。

```
<div style="width: 200px;">
<p>This paragragh is contained within a DIV that has a width of 200 pixels.</p>
</div> 
```

注意：上下内边距与左右内边距一致；即上下内边距的百分数会相对于父元素宽度设置，而不是相对于高度。

### CSS 内边距实例：

- [所有内边距属性在一个声明中](http://www.w3school.com.cn/tiy/t.asp?f=csse_padding)

  本例演示使用简写属性将所有的内边距属性设置于一个声明中，可以有一到四个值。

- [设置下内边距 1](http://www.w3school.com.cn/tiy/t.asp?f=csse_padding-bottom)

  本例演示如何使用厘米值来设置单元格的下内边距。

- [设置下内边距 2](http://www.w3school.com.cn/tiy/t.asp?f=csse_padding-bottom_percent)

  本例演示如何使用百分比值来设置单元格的下内边距。

- [设置左内边距 1](http://www.w3school.com.cn/tiy/t.asp?f=csse_padding-left)

  本例演示如何使用厘米值来设置单元格的左内边距。

- [设置左内边距 2](http://www.w3school.com.cn/tiy/t.asp?f=csse_padding-left_percent)

  本例演示如何使用百分比值来设置单元格的左内边距。

- [设置右内边距 1](http://www.w3school.com.cn/tiy/t.asp?f=csse_padding-right)

  本例演示如何使用厘米值来设置单元格的右内边距。

- [设置右内边距 2](http://www.w3school.com.cn/tiy/t.asp?f=csse_padding-right_percent)

  本例演示如何使用百分比值来设置单元格的右内边距。

- [设置上内边距 1](http://www.w3school.com.cn/tiy/t.asp?f=csse_padding-top)

  本例演示如何使用厘米值来设置单元格的上内边距。

- [设置上内边距 2](http://www.w3school.com.cn/tiy/t.asp?f=csse_padding-top_percent)

  本例演示如何使用百分比值来设置单元格的上内边距。

### CSS 内边距属性

| 属性                                                         | 描述                                                 |
| ------------------------------------------------------------ | ---------------------------------------------------- |
| [padding](http://www.w3school.com.cn/cssref/pr_padding.asp)  | 简写属性。作用是在一个声明中设置元素的所内边距属性。 |
| [padding-bottom](http://www.w3school.com.cn/cssref/pr_padding-bottom.asp) | 设置元素的下内边距。                                 |
| [padding-left](http://www.w3school.com.cn/cssref/pr_padding-left.asp) | 设置元素的左内边距。                                 |
| [padding-right](http://www.w3school.com.cn/cssref/pr_padding-right.asp) | 设置元素的右内边距。                                 |
| [padding-top](http://www.w3school.com.cn/cssref/pr_padding-top.asp) | 设置元素的上内边距。                                 |

## CSS 边框

**元素的边框 (border) 是围绕元素内容和内边距的一条或多条线。**

**CSS border 属性允许你规定元素边框的样式、宽度和颜色。**

### CSS 边框

在 HTML 中，我们使用表格来创建文本周围的边框，但是通过使用 CSS 边框属性，我们可以创建出效果出色的边框，并且可以应用于任何元素。

元素外边距内就是元素的的边框 (border)。元素的边框就是围绕元素内容和内边据的一条或多条线。

每个边框有 3 个方面：宽度、样式，以及颜色。在下面的篇幅，我们会为您详细讲解这三个方面。

### 边框与背景

CSS 规范指出，边框绘制在“元素的背景之上”。这很重要，因为有些边框是“间断的”（例如，点线边框或虚线框），元素的背景应当出现在边框的可见部分之间。

CSS2 指出背景只延伸到内边距，而不是边框。后来 CSS2.1 进行了更正：元素的背景是内容、内边距和边框区的背景。大多数浏览器都遵循 CSS2.1 定义，不过一些较老的浏览器可能会有不同的表现。

### 边框的样式

样式是边框最重要的一个方面，这不是因为样式控制着边框的显示（当然，样式确实控制着边框的显示），而是因为如果没有样式，将根本没有边框。

CSS 的 [border-style 属性](http://www.w3school.com.cn/cssref/pr_border-style.asp)定义了 10 个不同的非 inherit 样式，包括 none。

例如，您可以为把一幅图片的边框定义为 outset，使之看上去像是“凸起按钮”：

```
a:link img {border-style: outset;}
```

#### 定义多种样式

您可以为一个边框定义多个样式，例如：

```
p.aside {border-style: solid dotted dashed double;}
```

上面这条规则为类名为 aside 的段落定义了四种边框样式：实线上边框、点线右边框、虚线下边框和一个双线左边框。

我们又看到了这里的值采用了 top-right-bottom-left 的顺序，讨论用多个值设置不同内边距时也见过这个顺序。

#### 定义单边样式

如果您希望为元素框的某一个边设置边框样式，而不是设置所有 4 个边的边框样式，可以使用下面的单边边框样式属性：

- [border-top-style](http://www.w3school.com.cn/cssref/pr_border-top_style.asp)
- [border-right-style](http://www.w3school.com.cn/cssref/pr_border-right_style.asp)
- [border-bottom-style](http://www.w3school.com.cn/cssref/pr_border-bottom_style.asp)
- [border-left-style](http://www.w3school.com.cn/cssref/pr_border-left_style.asp)

因此这两种方法是等价的：

```
p {border-style: solid solid solid none;}
p {border-style: solid; border-left-style: none;}
```

注意：如果要使用第二种方法，必须把单边属性放在简写属性之后。因为如果把单边属性放在 border-style 之前，简写属性的值就会覆盖单边值 none。

### 边框的宽度

您可以通过 [border-width 属性](http://www.w3school.com.cn/cssref/pr_border-width.asp)为边框指定宽度。

为边框指定宽度有两种方法：可以指定长度值，比如 2px 或 0.1em；或者使用 3 个关键字之一，它们分别是 thin 、medium（默认值） 和 thick。

注释：CSS 没有定义 3 个关键字的具体宽度，所以一个用户代理可能把 thin 、medium 和 thick 分别设置为等于 5px、3px 和 2px，而另一个用户代理则分别设置为 3px、2px 和 1px。

所以，我们可以这样设置边框的宽度：

```
p {border-style: solid; border-width: 5px;}
```

或者：

```
p {border-style: solid; border-width: thick;}
```

#### 定义单边宽度

您可以按照 top-right-bottom-left 的顺序设置元素的各边边框：

```
p {border-style: solid; border-width: 15px 5px 15px 5px;}
```

上面的例子也可以简写为（这样写法称为*值复制*）：

```
p {border-style: solid; border-width: 15px 5px;}
```

您也可以通过下列属性分别设置边框各边的宽度：

- [border-top-width](http://www.w3school.com.cn/cssref/pr_border-top_width.asp)
- [border-right-width](http://www.w3school.com.cn/cssref/pr_border-right_width.asp)
- [border-bottom-width](http://www.w3school.com.cn/cssref/pr_border-bottom_width.asp)
- [border-left-width](http://www.w3school.com.cn/cssref/pr_border-left_width.asp)

因此，下面的规则与上面的例子是等价的：

```
p {
  border-style: solid;
  border-top-width: 15px;
  border-right-width: 5px;
  border-bottom-width: 15px;
  border-left-width: 5px;
  }
```

#### 没有边框

在前面的例子中，您已经看到，如果希望显示某种边框，就必须设置边框样式，比如 solid 或 outset。

那么如果把 border-style 设置为 none 会出现什么情况：

```
p {border-style: none; border-width: 50px;}
```

尽管边框的宽度是 50px，但是边框样式设置为 none。在这种情况下，不仅边框的样式没有了，其宽度也会变成 0。边框消失了，为什么呢？

这是因为如果边框样式为 none，即边框根本不存在，那么边框就不可能有宽度，因此边框宽度自动设置为 0，而不论您原先定义的是什么。

记住这一点非常重要。事实上，忘记声明边框样式是一个常犯的错误。根据以下规则，所有 h1 元素都不会有任何边框，更不用说 20 像素宽了：

```
h1 {border-width: 20px;}
```

由于 border-style 的默认值是 none，如果没有声明样式，就相当于 border-style: none。**因此，如果您希望边框出现，就必须声明一个边框样式。**

### 边框的颜色

设置边框颜色非常简单。CSS 使用一个简单的 [border-color 属性](http://www.w3school.com.cn/cssref/pr_border-color.asp)，它一次可以接受最多 4 个颜色值。

可以使用任何类型的颜色值，例如可以是命名颜色，也可以是十六进制和 RGB 值：

```
p {
  border-style: solid;
  border-color: blue rgb(25%,35%,45%) #909090 red;
  }
```

如果颜色值小于 4 个，值复制就会起作用。例如下面的规则声明了段落的上下边框是蓝色，左右边框是红色：

```
p {
  border-style: solid;
  border-color: blue red;
  }
```

注释：默认的边框颜色是元素本身的前景色。如果没有为边框声明颜色，它将与元素的文本颜色相同。另一方面，如果元素没有任何文本，假设它是一个表格，其中只包含图像，那么该表的边框颜色就是其父元素的文本颜色（因为 color 可以继承）。这个父元素很可能是 body、div 或另一个 table。

#### 定义单边颜色

还有一些单边边框颜色属性。它们的原理与单边样式和宽度属性相同：

- [border-top-color](http://www.w3school.com.cn/cssref/pr_border-top_color.asp)
- [border-right-color](http://www.w3school.com.cn/cssref/pr_border-right_color.asp)
- [border-bottom-color](http://www.w3school.com.cn/cssref/pr_border-bottom_color.asp)
- [border-left-color](http://www.w3school.com.cn/cssref/pr_border-left_color.asp)

要为 h1 元素指定实线黑色边框，而右边框为实线红色，可以这样指定：

```
h1 {
  border-style: solid;
  border-color: black;
  border-right-color: red;
  }
```

#### 透明边框

我们刚才讲过，如果边框没有样式，就没有宽度。不过有些情况下您可能希望创建一个不可见的边框。

CSS2 引入了边框颜色值 transparent。这个值用于创建有宽度的不可见边框。请看下面的例子：

```
<a href="#">AAA</a>
<a href="#">BBB</a>
<a href="#">CCC</a>
```

我们为上面的链接定义了如下样式：

```
a:link, a:visited {
  border-style: solid;
  border-width: 5px;
  border-color: transparent;
  }
a:hover {border-color: gray;}
```

如需查看以上样式的效果，请点击：[TIY](http://www.w3school.com.cn/tiy/t.asp?f=csse_border_color_transparent)。

从某种意义上说，利用 transparent，使用边框就像是额外的内边距一样；此外还有一个好处，就是能在你需要的时候使其可见。这种透明边框相当于内边距，因为元素的背景会延伸到边框区域（如果有可见背景的话）。

重要事项：在 IE7 之前，IE/WIN 没有提供对 transparent 的支持。在以前的版本，IE 会根据元素的 color 值来设置边框颜色。

### CSS 边框实例：

- [所有边框属性在一个声明之中](http://www.w3school.com.cn/tiy/t.asp?f=csse_border)

  本例演示用简写属性来将所有四个边框属性设置于同一声明中。

- [设置四边框样式](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-style)

  本例演示如何设置四边框样式。

- [设置每一边的不同边框](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-style2)

  本例演示如何在元素的各边设置不同的边框。

- [所有边框宽度属性在一个声明之中](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-width)

  本例演示用简写属性来将所有边框宽度属性设置于同一声明中。

- [设置四个边框的颜色](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-color)

  本例演示如何设置四个边框的颜色。可以设置一到四个颜色。

- [所有下边框属性在一个声明中](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-bottom)

  本例演示用简写属性来将所有下边框属性设置在同一声明中。

- [设置下边框的颜色](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-bottom-color)

  本例演示如何设置下边框的颜色。

- [设置下边框的样式](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-bottom-style)

  本例演示如何设置下边框的样式。

- [设置下边框的宽度](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-bottom-width)

  本例演示如何设置下边框的宽度。

- [所有左边框属性在一个声明之中](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-left)

  所有左边框属性在一个声明之中

- [设置左边框的颜色](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-left-color)

  本例演示如何设置左边框的颜色。

- [设置左边框的样式](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-left-style)

  本例演示如何设置左边框的样式。

- [设置左边框的宽度](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-left-width)

  本例演示如何设置左边框的宽度。

- [所有右边框属性在一个声明之中](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-right)

  本例演示一个简写属性，用于把所有右边框属性设置在一条声明中。

- [设置右边框的颜色](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-right-color)

  本例演示如何设置右边框的颜色。

- [设置右边框的样式](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-right-style)

  本例演示如何设置右边框的样式。

- [设置右边框的宽度](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-right-width)

  本例演示如何设置右边框的宽度。

- [所有上边框属性在一个声明之中](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-top)

  本例演示用简写属性来将所有上边框属性设置于同一声明之中。

- [设置上边框的颜色](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-top-color)

  本例演示如何设置上边框的颜色。

- [设置上边框的样式](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-top-style)

  本例演示如何设置上边框的样式。

- [设置上边框的宽度](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-top-width)

  本例演示如何设置上边框的宽度。

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

### CSS margin 属性

设置外边距的最简单的方法就是使用 [margin 属性](http://www.w3school.com.cn/cssref/pr_margin.asp)。

margin 属性接受任何长度单位，可以是像素、英寸、毫米或 em。

margin 可以设置为 auto。更常见的做法是为外边距设置长度值。下面的声明在 h1 元素的各个边上设置了 1/4 英寸宽的空白：

```
h1 {margin : 0.25in;}
```

下面的例子为 h1 元素的四个边分别定义了不同的外边距，所使用的长度单位是像素 (px)：

```
h1 {margin : 10px 0px 15px 5px;}
```

与内边距的设置相同，这些值的顺序是从上外边距 (top) 开始围着元素顺时针旋转的：

```
margin: top right bottom left
```

另外，还可以为 margin 设置一个百分比数值：

```
p {margin : 10%;}
```

百分数是相对于父元素的 width 计算的。上面这个例子为 p 元素设置的外边距是其父元素的 width 的 10%。

margin 的默认值是 0，所以如果没有为 margin 声明一个值，就不会出现外边距。但是，在实际中，浏览器对许多元素已经提供了预定的样式，外边距也不例外。例如，在支持 CSS 的浏览器中，外边距会在每个段落元素的上面和下面生成“空行”。因此，如果没有为 p 元素声明外边距，浏览器可能会自己应用一个外边距。当然，只要你特别作了声明，就会覆盖默认样式。

### 值复制

还记得吗？我们曾经在前两节中提到过值复制。下面我们为您讲解如何使用值复制。

有时，我们会输入一些重复的值：

```
p {margin: 0.5em 1em 0.5em 1em;}
```

通过值复制，您可以不必重复地键入这对数字。上面的规则与下面的规则是等价的：

```
p {margin: 0.5em 1em;}
```

这两个值可以取代前面 4 个值。这是如何做到的呢？CSS 定义了一些规则，允许为外边距指定少于 4 个值。规则如下：

- 如果缺少左外边距的值，则使用右外边距的值。
- 如果缺少下外边距的值，则使用上外边距的值。
- 如果缺少右外边距的值，则使用上外边距的值。

下图提供了更直观的方法来了解这一点：



换句话说，如果为外边距指定了 3 个值，则第 4 个值（即左外边距）会从第 2 个值（右外边距）复制得到。如果给定了两个值，第 4 个值会从第 2 个值复制得到，第 3 个值（下外边距）会从第 1 个值（上外边距）复制得到。最后一个情况，如果只给定一个值，那么其他 3 个外边距都由这个值（上外边距）复制得到。

利用这个简单的机制，您只需指定必要的值，而不必全部都应用 4 个值，例如：

```
h1 {margin: 0.25em 1em 0.5em;}	/* 等价于 0.25em 1em 0.5em 1em */
h2 {margin: 0.5em 1em;}		/* 等价于 0.5em 1em 0.5em 1em */
p {margin: 1px;}			/* 等价于 1px 1px 1px 1px */
```

这种办法有一个小缺点，您最后肯定会遇到这个问题。假设希望把 p 元素的上外边距和左外边距设置为 20 像素，下外边距和右外边距设置为 30 像素。在这种情况下，必须写作：

```
p {margin: 20px 30px 30px 20px;}
```

这样才能得到您想要的结果。遗憾的是，在这种情况下，所需值的个数没有办法更少了。

再来看另外一个例子。如果希望除了左外边距以外所有其他外边距都是 auto（左外边距是 20px）：

```
p {margin: auto auto auto 20px;}
```

同样的，这样才能得到你想要的效果。问题在于，键入这些 auto 有些麻烦。如果您只是希望控制元素单边上的外边距，请使用单边外边距属性。

### 单边外边距属性

您可以使用单边外边距属性为元素单边上的外边距设置值。假设您希望把 p 元素的左外边距设置为 20px。不必使用 margin（需要键入很多 auto），而是可以采用以下方法：

```
p {margin-left: 20px;}
```

您可以使用下列任何一个属性来只设置相应上的外边距，而不会直接影响所有其他外边距：

- [margin-top](http://www.w3school.com.cn/cssref/pr_margin-top.asp)
- [margin-right](http://www.w3school.com.cn/cssref/pr_margin-right.asp)
- [margin-bottom](http://www.w3school.com.cn/cssref/pr_margin-bottom.asp)
- [margin-left](http://www.w3school.com.cn/cssref/pr_margin-left.asp)

一个规则中可以使用多个这种单边属性，例如：

```
h2 {
  margin-top: 20px;
  margin-right: 30px;
  margin-bottom: 30px;
  margin-left: 20px;
  }
```

当然，对于这种情况，使用 margin 可能更容易一些：

```
p {margin: 20px 30px 30px 20px;}
```

不论使用单边属性还是使用 margin，得到的结果都一样。一般来说，如果希望为多个边设置外边距，使用 margin 会更容易一些。不过，从文档显示的角度看，实际上使用哪种方法都不重要，所以应该选择对自己来说更容易的一种方法。

### 提示和注释

提示：Netscape 和 IE 对 body 标签定义的默认边距（margin）值是 8px。而 Opera 不是这样。相反地，Opera 将内部填充（padding）的默认值定义为 8px，因此如果希望对整个网站的边缘部分进行调整，并将之正确显示于 Opera 中，那么必须对 body 的 padding 进行自定义。

### CSS 外边距实例：

- [设置文本的左外边距](http://www.w3school.com.cn/tiy/t.asp?f=csse_margin-left)

  本例演示如何设置文本的左外边距。

- [设置文本的右外边距](http://www.w3school.com.cn/tiy/t.asp?f=csse_margin-right)

  本例演示如何设置文本的右外边距。

- [设置文本的上外边距](http://www.w3school.com.cn/tiy/t.asp?f=csse_margin-top)

  本例演示如何设置文本的上外边距。

- [设置文本的下外边距](http://www.w3school.com.cn/tiy/t.asp?f=csse_margin-bottom)

  本例演示如何设置文本的下外边距。

- [所有的外边距属性在一个声明中。](http://www.w3school.com.cn/tiy/t.asp?f=csse_margin)

  本例演示如何将所有的外边距属性设置于一个声明中。

### CSS 外边距属性

| 属性                                                         | 描述                                       |
| ------------------------------------------------------------ | ------------------------------------------ |
| [margin](http://www.w3school.com.cn/cssref/pr_margin.asp)    | 简写属性。在一个声明中设置所有外边距属性。 |
| [margin-bottom](http://www.w3school.com.cn/cssref/pr_margin-bottom.asp) | 设置元素的下外边距。                       |
| [margin-left](http://www.w3school.com.cn/cssref/pr_margin-left.asp) | 设置元素的左外边距。                       |
| [margin-right](http://www.w3school.com.cn/cssref/pr_margin-right.asp) | 设置元素的右外边距。                       |
| [margin-top](http://www.w3school.com.cn/cssref/pr_margin-top.asp) | 设置元素的上外边距。                       |

## CSS 外边距合并



**外边距合并指的是，当两个垂直外边距相遇时，它们将形成一个外边距。**

**合并后的外边距的高度等于两个发生合并的外边距的高度中的较大者。**

### 外边距合并

外边距合并（叠加）是一个相当简单的概念。但是，在实践中对网页进行布局时，它会造成许多混淆。

简单地说，外边距合并指的是，当两个垂直外边距相遇时，它们将形成一个外边距。合并后的外边距的高度等于两个发生合并的外边距的高度中的较大者。

当一个元素出现在另一个元素上面时，第一个元素的下外边距与第二个元素的上外边距会发生合并。请看下图：



 

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_margin_collapsing1)

当一个元素包含在另一个元素中时（假设没有内边距或边框把外边距分隔开），它们的上和/或下外边距也会发生合并。请看下图：



 

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_margin_collapsing2)

尽管看上去有些奇怪，但是外边距甚至可以与自身发生合并。

假设有一个空元素，它有外边距，但是没有边框或填充。在这种情况下，上外边距与下外边距就碰到了一起，它们会发生合并：



如果这个外边距遇到另一个元素的外边距，它还会发生合并：



这就是一系列的段落元素占用空间非常小的原因，因为它们的所有外边距都合并到一起，形成了一个小的外边距。

外边距合并初看上去可能有点奇怪，但是实际上，它是有意义的。以由几个段落组成的典型文本页面为例。第一个段落上面的空间等于段落的上外边距。如果没有外边距合并，后续所有段落之间的外边距都将是相邻上外边距和下外边距的和。这意味着段落之间的空间是页面顶部的两倍。如果发生外边距合并，段落之间的上外边距和下外边距就合并在一起，这样各处的距离就一致了。



注释：只有普通文档流中块框的垂直外边距才会发生外边距合并。行内框、浮动框或绝对定位之间的外边距不会合并。

# CSS 定位 (Positioning)



**CSS 定位 (Positioning) 属性允许你对元素进行定位。**

## CSS 定位和浮动

CSS 为定位和浮动提供了一些属性，利用这些属性，可以建立列式布局，将布局的一部分与另一部分重叠，还可以完成多年来通常需要使用多个表格才能完成的任务。

定位的基本思想很简单，它允许你定义元素框相对于其正常位置应该出现的位置，或者相对于父元素、另一个元素甚至浏览器窗口本身的位置。显然，这个功能非常强大，也很让人吃惊。要知道，用户代理对 CSS2 中定位的支持远胜于对其它方面的支持，对此不应感到奇怪。

另一方面，CSS1 中首次提出了浮动，它以 Netscape 在 Web 发展初期增加的一个功能为基础。浮动不完全是定位，不过，它当然也不是正常流布局。我们会在后面的章节中明确浮动的含义。

### 一切皆为框

div、h1 或 p 元素常常被称为块级元素。这意味着这些元素显示为*一块内容*，即“块框”。与之相反，span 和 strong 等元素称为“行内元素”，这是因为它们的内容显示在行中，即“行内框”。

您可以使用 [display 属性](http://www.w3school.com.cn/cssref/pr_class_display.asp)改变生成的框的类型。这意味着，通过将 display 属性设置为 block，可以让行内元素（比如 <a> 元素）表现得像块级元素一样。还可以通过把 display 设置为 none，让生成的元素根本没有框。这样的话，该框及其所有内容就不再显示，不占用文档中的空间。

但是在一种情况下，即使没有进行显式定义，也会创建块级元素。这种情况发生在把一些文本添加到一个块级元素（比如 div）的开头。即使没有把这些文本定义为段落，它也会被当作段落对待：

```
<div>
some text
<p>Some more text.</p>
</div>
```

在这种情况下，这个框称为无名块框，因为它不与专门定义的元素相关联。

块级元素的文本行也会发生类似的情况。假设有一个包含三行文本的段落。每行文本形成一个无名框。无法直接对无名块或行框应用样式，因为没有可以应用样式的地方（注意，行框和行内框是两个概念）。但是，这有助于理解在屏幕上看到的所有东西都形成某种框。

### CSS 定位机制

CSS 有三种基本的定位机制：普通流、浮动和绝对定位。

除非专门指定，否则所有框都在普通流中定位。也就是说，普通流中的元素的位置由元素在 (X)HTML 中的位置决定。

块级框从上到下一个接一个地排列，框之间的垂直距离是由框的垂直外边距计算出来。

行内框在一行中水平布置。可以使用水平内边距、边框和外边距调整它们的间距。但是，垂直内边距、边框和外边距不影响行内框的高度。由一行形成的水平框称为*行框（Line Box）*，行框的高度总是足以容纳它包含的所有行内框。不过，设置行高可以增加这个框的高度。

在下面的章节，我们会为您详细讲解相对定位、绝对定位和浮动。

### CSS position 属性

通过使用 [position 属性](http://www.w3school.com.cn/cssref/pr_class_position.asp)，我们可以选择 4 种不同类型的定位，这会影响元素框生成的方式。

position 属性值的含义：

- static

  元素框正常生成。块级元素生成一个矩形框，作为文档流的一部分，行内元素则会创建一个或多个行框，置于其父元素中。

- relative

  元素框偏移某个距离。元素仍保持其未定位前的形状，它原本所占的空间仍保留。

- absolute

  元素框从文档流完全删除，并相对于其包含块定位。包含块可能是文档中的另一个元素或者是初始包含块。元素原先在正常文档流中所占的空间会关闭，就好像元素原来不存在一样。元素定位后生成一个块级框，而不论原来它在正常流中生成何种类型的框。

- fixed

  元素框的表现类似于将 position 设置为 absolute，不过其包含块是视窗本身。

提示：相对定位实际上被看作普通流定位模型的一部分，因为元素的位置相对于它在普通流中的位置。

### 实例

- [定位：相对定位](http://www.w3school.com.cn/tiy/t.asp?f=csse_position_relative)

  本例演示如何相对于一个元素的正常位置来对其定位。

- [定位：绝对定位](http://www.w3school.com.cn/tiy/t.asp?f=csse_position_absolute)

  本例演示如何使用绝对值来对元素进行定位。

- [定位：固定定位](http://www.w3school.com.cn/tiy/t.asp?f=csse_position_fixed)

  本例演示如何相对于浏览器窗口来对元素进行定位。

- [使用固定值设置图像的上边缘](http://www.w3school.com.cn/tiy/t.asp?f=csse_position_top)

  本例演示如何使用固定值设置图像的上边缘。

- [使用百分比设置图像的上边缘](http://www.w3school.com.cn/tiy/t.asp?f=csse_position_top_percent)

  本例演示如何使用百分比值设置图像的上边缘。

- [使用像素值设置图像的底部边缘](http://www.w3school.com.cn/tiy/t.asp?f=csse_position_bottom)

  本例演示如何使用像素值设置图像的底部边缘。

- [使用百分比设置图像的底部边缘](http://www.w3school.com.cn/tiy/t.asp?f=csse_position_bottom_percent)

  本例演示如何使用百分比值设置图像的底部边缘。

- [使用固定值设置图像的左边缘](http://www.w3school.com.cn/tiy/t.asp?f=csse_position_left)

  本例演示如何使用固定值设置图像的左边缘。

- [使用百分比设置图像的左边缘](http://www.w3school.com.cn/tiy/t.asp?f=csse_position_left_percent)

  本例演示如何使用百分比值设置图像的左边缘。

- [使用固定值设置图像的右边缘](http://www.w3school.com.cn/tiy/t.asp?f=csse_position_right)

  本例演示如何使用固定值设置图像的右边缘。

- [使用百分比设置图像的右边缘](http://www.w3school.com.cn/tiy/t.asp?f=csse_position_right_percent)

  本例演示如何使用百分比值设置图像的右边缘。

- [如何使用滚动条来显示元素内溢出的内容](http://www.w3school.com.cn/tiy/t.asp?f=csse_overflow)

  本例演示当元素内容太大而超出规定区域时，如何设置溢出属性来规定相应的动作。

- [如何隐藏溢出元素中溢出的内容](http://www.w3school.com.cn/tiy/t.asp?f=csse_pos_overflow_hidden)

  本例演示在元素中的内容太大以至于无法适应指定的区域时，如何设置 overflow 属性来隐藏其内容。

- [如何设置浏览器来自动地处理溢出](http://www.w3school.com.cn/tiy/t.asp?f=csse_pos_overflow_auto)

  本例演示如何设置浏览器来自动地处理溢出。

- [设置元素的形状](http://www.w3school.com.cn/tiy/t.asp?f=csse_clip)

  本例演示如何设置元素的形状。此元素被剪裁到这个形状内，并显示出来。

- [垂直排列图象](http://www.w3school.com.cn/tiy/t.asp?f=csse_vertical-align)

  本例演示如何在文本中垂直排列图象。

- [Z-index](http://www.w3school.com.cn/tiy/t.asp?f=csse_zindex2)

  Z-index可被用于将在一个元素放置于另一元素之后。

- [Z-index](http://www.w3school.com.cn/tiy/t.asp?f=csse_zindex1)

  上面的例子中的元素已经更改了Z-index。

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

## CSS 相对定位



**设置为相对定位的元素框会偏移某个距离。元素仍然保持其未定位前的形状，它原本所占的空间仍保留。**

### CSS 相对定位

相对定位是一个非常容易掌握的概念。如果对一个元素进行相对定位，它将出现在它所在的位置上。然后，可以通过设置垂直或水平位置，让这个元素“相对于”它的起点进行移动。

如果将 top 设置为 20px，那么框将在原位置顶部下面 20 像素的地方。如果 left 设置为 30 像素，那么会在元素左边创建 30 像素的空间，也就是将元素向右移动。

```
#box_relative {
  position: relative;
  left: 30px;
  top: 20px;
}
```

如下图所示：



注意，在使用相对定位时，无论是否进行移动，元素仍然占据原来的空间。因此，移动元素会导致它覆盖其它框。

### CSS 相对定位实例

- [定位：相对定位](http://www.w3school.com.cn/tiy/t.asp?f=csse_position_relative)

  本例演示如何相对于一个元素的正常位置来对其定位。

## CSS 绝对定位



**设置为绝对定位的元素框从文档流完全删除，并相对于其包含块定位，包含块可能是文档中的另一个元素或者是初始包含块。元素原先在正常文档流中所占的空间会关闭，就好像该元素原来不存在一样。元素定位后生成一个块级框，而不论原来它在正常流中生成何种类型的框。**

### CSS 绝对定位

绝对定位使元素的位置与文档流无关，因此不占据空间。这一点与相对定位不同，相对定位实际上被看作普通流定位模型的一部分，因为元素的位置相对于它在普通流中的位置。

普通流中其它元素的布局就像绝对定位的元素不存在一样：

```
#box_relative {
  position: absolute;
  left: 30px;
  top: 20px;
}
```

如下图所示：



绝对定位的元素的位置相对于*最近的已定位祖先元素*，如果元素没有已定位的祖先元素，那么它的位置相对于*最初的包含块*。

对于定位的主要问题是要记住每种定位的意义。所以，现在让我们复习一下学过的知识吧：相对定位是“相对于”元素在文档中的初始位置，而绝对定位是“相对于”最近的已定位祖先元素，如果不存在已定位的祖先元素，那么“相对于”最初的包含块。

注释：根据用户代理的不同，最初的包含块可能是画布或 HTML 元素。

提示：因为绝对定位的框与文档流无关，所以它们可以覆盖页面上的其它元素。可以通过设置 [z-index 属性](http://www.w3school.com.cn/cssref/pr_pos_z-index.asp)来控制这些框的堆放次序。

### CSS 绝对定位实例

- [定位：绝对定位](http://www.w3school.com.cn/tiy/t.asp?f=csse_position_absolute)

  本例演示如何使用绝对值来对元素进行定位。

## CSS 浮动



**浮动的框可以向左或向右移动，直到它的外边缘碰到包含框或另一个浮动框的边框为止。**

**由于浮动框不在文档的普通流中，所以文档的普通流中的块框表现得就像浮动框不存在一样。**

### CSS 浮动

请看下图，当把框 1 向右浮动时，它脱离文档流并且向右移动，直到它的右边缘碰到包含框的右边缘：



再请看下图，当框 1 向左浮动时，它脱离文档流并且向左移动，直到它的左边缘碰到包含框的左边缘。因为它不再处于文档流中，所以它不占据空间，实际上覆盖住了框 2，使框 2 从视图中消失。

如果把所有三个框都向左移动，那么框 1 向左浮动直到碰到包含框，另外两个框向左浮动直到碰到前一个浮动框。



如下图所示，如果包含框太窄，无法容纳水平排列的三个浮动元素，那么其它浮动块向下移动，直到有足够的空间。如果浮动元素的高度不同，那么当它们向下移动时可能被其它浮动元素“卡住”：



### CSS float 属性

在 CSS 中，我们通过 float 属性实现元素的浮动。

如需更多有关 float 属性的知识，请访问参考手册：[CSS float 属性](http://www.w3school.com.cn/cssref/pr_class_float.asp)。

### 行框和清理

浮动框旁边的行框被缩短，从而给浮动框留出空间，行框围绕浮动框。

因此，创建浮动框可以使文本围绕图像：



要想阻止行框围绕浮动框，需要对该框应用 [clear 属性](http://www.w3school.com.cn/cssref/pr_class_clear.asp)。clear 属性的值可以是 left、right、both 或 none，它表示框的哪些边不应该挨着浮动框。

为了实现这种效果，在被清理的元素的*上外边距*上添加足够的空间，使元素的顶边缘垂直下降到浮动框下面：



这是一个有用的工具，它让周围的元素为浮动元素留出空间。

让我们更详细地看看浮动和清理。假设希望让一个图片浮动到文本块的左边，并且希望这幅图片和文本包含在另一个具有背景颜色和边框的元素中。您可能编写下面的代码：

```
.news {
  background-color: gray;
  border: solid 1px black;
  }

.news img {
  float: left;
  }

.news p {
  float: right;
  }

<div class="news">
<img src="news-pic.jpg" />
<p>some text</p>
</div>
```

这种情况下，出现了一个问题。因为浮动元素脱离了文档流，所以包围图片和文本的 div 不占据空间。

如何让包围元素在视觉上包围浮动元素呢？需要在这个元素中的某个地方应用 clear：



不幸的是出现了一个新的问题，由于没有现有的元素可以应用清理，所以我们只能添加一个空元素并且清理它。

```
.news {
  background-color: gray;
  border: solid 1px black;
  }

.news img {
  float: left;
  }

.news p {
  float: right;
  }

.clear {
  clear: both;
  }

<div class="news">
<img src="news-pic.jpg" />
<p>some text</p>
<div class="clear"></div>
</div>
```

这样可以实现我们希望的效果，但是需要添加多余的代码。常常有元素可以应用 clear，但是有时候不得不为了进行布局而添加无意义的标记。

不过我们还有另一种办法，那就是对容器 div 进行浮动：

```
.news {
  background-color: gray;
  border: solid 1px black;
  float: left;
  }

.news img {
  float: left;
  }

.news p {
  float: right;
  }

<div class="news">
<img src="news-pic.jpg" />
<p>some text</p>
</div>
```

这样会得到我们希望的效果。不幸的是，下一个元素会受到这个浮动元素的影响。为了解决这个问题，有些人选择对布局中的所有东西进行浮动，然后使用适当的有意义的元素（常常是站点的页脚）对这些浮动进行清理。这有助于减少或消除不必要的标记。

事实上，W3School 站点上的所有页面都采用了这种技术，如果您打开我们使用 CSS 文件，您会看到我们对页脚的 div 进行了清理，而页脚上面的三个 div 都向左浮动。

### CSS clear 属性

我们刚才详细讨论了 CSS 清理的工作原理和 clear 属性应用方法。如果您希望学习更多有关 clear 属性的知识，请访问参考手册：[CSS clear 属性](http://www.w3school.com.cn/cssref/pr_class_clear.asp)。

### 浮动和清理 实例

- [float 属性的简单应用](http://www.w3school.com.cn/tiy/t.asp?f=csse_float)

  使图像浮动于一个段落的右侧。

- [将带有边框和边界的图像浮动于段落的右侧](http://www.w3school.com.cn/tiy/t.asp?f=csse_float2)

  使图像浮动于段落的右侧。向图像添加边框和边界。

- [带标题的图像浮动于右侧](http://www.w3school.com.cn/tiy/t.asp?f=csse_float3)

  使带有标题的图像浮动于右侧

- [使段落的首字母浮动于左侧](http://www.w3school.com.cn/tiy/t.asp?f=csse_float4)

  使段落的首字母浮动于左侧，并向这个字母添加样式。

- [创建水平菜单](http://www.w3school.com.cn/tiy/t.asp?f=csse_float5)

  使用具有一栏超链接的浮动来创建水平菜单。

- [创建无表格的首页](http://www.w3school.com.cn/tiy/t.asp?f=csse_float6)

  使用浮动来创建拥有页眉、页脚、左侧目录和主体内容的首页。

- [清除元素的侧面](http://www.w3school.com.cn/tiy/t.asp?f=csse_class-clear)

  本例演示如何使用清除元素侧面的浮动元素。


# CSS 选择器详解



## CSS 元素选择器

最常见的 CSS 选择器是元素选择器。换句话说，文档的元素就是最基本的选择器。

如果设置 HTML 的样式，选择器通常将是某个 HTML 元素，比如 p、h1、em、a，甚至可以是 html 本身：

```
html {color:black;}
h1 {color:blue;}
h2 {color:silver;}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_selector_type_1)

可以将某个样式从一个元素切换到另一个元素。

假设您决定将上面的段落文本（而不是 h1 元素）设置为灰色。只需要把 h1 选择器改为 p：

```
html {color:black;}
p {color:gray;}
h2 {color:silver;}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_selector_type_2)

### 类型选择器

在 W3C 标准中，元素选择器又称为类型选择器（type selector）。

“类型选择器匹配文档语言元素类型的名称。类型选择器匹配文档树中该元素类型的每一个实例。”

下面的规则匹配文档树中所有 h1 元素：

```
h1 {font-family: sans-serif;}
```

因此，我们也可以为 XML 文档中的元素设置样式：

### XML 文档：

```
<?xml version="1.0" encoding="ISO-8859-1"?>
<?xml-stylesheet type="text/css" href="note.css"?>
<note>
<to>George</to>
<from>John</from>
<heading>Reminder</heading>
<body>Don't forget the meeting!</body>
</note>
```

### CSS 文档：

```
note{
  font-family:Verdana, Arial;
  margin-left:30px;
  }

to {
  font-size:28px;
  display: block;
  }

from {
  font-size:28px;
  display: block;
  }

heading{
  color: red;
  font-size:60px;
  display: block;
  }

body {
  color: blue;
  font-size:35px;
  display: block;
  }
```

[查看效果](http://www.w3school.com.cn/example/csse/note_css.xml)

通过上面的例子，您可以看到，CSS 元素选择器（类型选择器）可以设置 XML 文档中元素的样式。

如果您需要更多关于为 XML 文档添加样式的知识，请访问 w3school 的 [XML 教程](http://www.w3school.com.cn/xml/index.asp)。

## CSS 选择器分组

假设希望 h2 元素和段落都有灰色。为达到这个目的，最容易的做法是使用以下声明：

```
h2, p {color:gray;}
```

将 h2 和 p 选择器放在规则左边，然后用逗号分隔，就定义了一个规则。其右边的样式（color:gray;）将应用到这两个选择器所引用的元素。逗号告诉浏览器，规则中包含两个不同的选择器。如果没有这个逗号，那么规则的含义将完全不同。参见后代选择器。

可以将任意多个选择器分组在一起，对此没有任何限制。

例如，如果您想把很多元素显示为灰色，可以使用类似如下的规则：

```
body, h2, p, table, th, td, pre, strong, em {color:gray;}
```

提示：通过分组，创作者可以将某些类型的样式“压缩”在一起，这样就可以得到更简洁的样式表。

以下的两组规则能得到同样的结果，不过可以很清楚地看出哪一个写起来更容易：

```
/* no grouping */
h1 {color:blue;}
h2 {color:blue;}
h3 {color:blue;}
h4 {color:blue;}
h5 {color:blue;}
h6 {color:blue;}

/* grouping */
h1, h2, h3, h4, h5, h6 {color:blue;}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_grouping_selector)

分组提供了一些有意思的选择。例如，下例中的所有规则分组都是等价的，每个组只是展示了对选择器和声明分组的不同方法：

```
/* group 1 */
h1 {color:silver; background:white;}
h2 {color:silver; background:gray;}
h3 {color:white; background:gray;}
h4 {color:silver; background:white;}
b {color:gray; background:white;}

/* group 2 */
h1, h2, h4 {color:silver;}
h2, h3 {background:gray;}
h1, h4, b {background:white;}
h3 {color:white;}
b {color:gray;}

/* group 3 */
h1, h4 {color:silver; background:white;}
h2 {color:silver;}
h3 {color:white;}
h2, h3 {background:gray;}
b {color:gray; background:white;}
```

亲自试一试：

- [group 1](http://www.w3school.com.cn/tiy/t.asp?f=csse_grouping_selector_1)
- [group 2](http://www.w3school.com.cn/tiy/t.asp?f=csse_grouping_selector_2)
- [group 3](http://www.w3school.com.cn/tiy/t.asp?f=csse_grouping_selector_3)

请注意，group 3 中使用了“声明分组”。稍后我们会为您介绍“声明分组”。

### 通配符选择器

CSS2 引入了一种新的简单选择器 - 通配选择器（universal selector），显示为一个星号（*）。该选择器可以与任何元素匹配，就像是一个通配符。

例如，下面的规则可以使文档中的每个元素都为红色：

```
* {color:red;}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_grouping_selector_universal)

这个声明等价于列出了文档中所有元素的一个分组选择器。利用通配选择器，只需敲一次键（仅一个星号）就能使文档中所有元素的 color 属性值指定为 red。

### 声明分组

我们既可以对选择器进行分组，也可以对声明分组。

假设您希望所有 h1 元素都有红色背景，并使用 28 像素高的 Verdana 字体显示为蓝色文本，可以写以下样式：

```
h1 {font: 28px Verdana;}
h1 {color: blue;}
h1 {background: red;}
```

但是上面这种做法的效率并不高。尤其是当我们为一个有多个样式的元素创建这样一个列表时会很麻烦。相反，我们可以将声明分组在一起：

```
h1 {font: 28px Verdana; color: white; background: black;}
```

这与前面的 3 行样式表的效果完全相同。

注意，对声明分组，一定要在各个声明的最后使用分号，这很重要。浏览器会忽略样式表中的空白符。只要加了分号，就可以毫无顾忌地采用以下格式建立样式：

```
h1 {
  font: 28px Verdana;
  color: blue;
  background: red;
  }
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_grouping_declaration)

怎么样，上面这种写法的可读性是不是更强。

不过，如果忽略了第二个分号，用户代理就会把这个样式表解释如下：

```
h1 {
  font: 28px Verdana;
  color: blue background: red;
  }
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_grouping_declaration_error)

因为 background 对 color 来说不是一个合法值，而且由于只能为 color 指定一个关键字，所以用户代理会完全忽略这个 color 声明（包括 background: black 部分）。这样 h1 标题只会显示为蓝色，而没有红色背景，不过更有可能根本得不到蓝色的 h1。相反，这些标题只会显示为默认颜色（通常是黑色），而且根本没有背景色。font: 28px Verdana 声明仍能正常发挥作用，因为它确实正确地以一个分号结尾。

与选择器分组一样，声明分组也是一种便利的方法，可以缩短样式表，使之更清晰，也更易维护。

提示：在规则的最后一个声明后也加上分号是一个好习惯。在向规则增加另一个声明时，就不必担心忘记再插入一个分号。

### 结合选择器和声明的分组

我们可以在一个规则中结合选择器分组和声明分组，就可以使用很少的语句定义相对复杂的样式。

下面的规则为所有标题指定了一种复杂的样式：

```
h1, h2, h3, h4, h5, h6 {
  color:gray;
  background: white;
  padding: 10px;
  border: 1px solid black;
  font-family: Verdana;
  }
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_grouping)

上面这条规则将所有标题的样式定义为带有白色背景的灰色文本，其内边距是 10 像素，并带有 1 像素的实心边框，文本字体是 Verdana。



## CSS 类选择器详解



**类选择器允许以一种独立于文档元素的方式来指定样式。**

### CSS 类选择器

类选择器允许以一种独立于文档元素的方式来指定样式。

该选择器可以单独使用，也可以与其他元素结合使用。

提示：只有适当地标记文档后，才能使用这些选择器，所以使用这两种选择器通常需要先做一些构想和计划。

要应用样式而不考虑具体设计的元素，最常用的方法就是使用类选择器。

### 修改 HTML 代码

在使用类选择器之前，需要修改具体的文档标记，以便类选择器正常工作。

为了将类选择器的样式与元素关联，必须将 class 指定为一个适当的值。请看下面的 HTML 代码：

```
<h1 class="important">
This heading is very important.
</h1>

<p class="important">
This paragraph is very important.
</p>
```

在上面的代码中，两个元素的 class 都指定为 important：第一个标题（ h1 元素），第二个段落（p 元素）。

#### 语法

然后我们使用以下语法向这些归类的元素应用样式，即类名前有一个点号（.），然后结合通配选择器：

```
*.important {color:red;}
```

如果您只想选择所有类名相同的元素，可以在类选择器中忽略通配选择器，这没有任何不好的影响：

```
.important {color:red;}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_selector_class_1)

### 结合元素选择器

类选择器可以结合元素选择器来使用。

例如，您可能希望只有段落显示为红色文本：

```
p.important {color:red;}
```

选择器现在会匹配 class 属性包含 important 的所有 p 元素，但是其他任何类型的元素都不匹配，不论是否有此 class 属性。选择器 p.important 解释为：“其 class 属性值为 important 的所有段落”。 因为 h1 元素不是段落，这个规则的选择器与之不匹配，因此 h1 元素不会变成红色文本。

如果你确实希望为 h1 元素指定不同的样式，可以使用选择器 h1.important：

```
p.important {color:red;}
h1.important {color:blue;}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_selector_class_2)

### CSS 多类选择器

在上一节中，我们处理了 class 值中包含一个词的情况。在 HTML 中，一个 class 值中可能包含一个词列表，各个词之间用空格分隔。例如，如果希望将一个特定的元素同时标记为重要（important）和警告（warning），就可以写作：

```
<p class="important warning">
This paragraph is a very important warning.
</p>
```

这两个词的顺序无关紧要，写成 warning important 也可以。

我们假设 class 为 important 的所有元素都是粗体，而 class 为 warning 的所有元素为斜体，class 中同时包含 important 和 warning 的所有元素还有一个银色的背景 。就可以写作：

```
.important {font-weight:bold;}
.warning {font-style:italic;}
.important.warning {background:silver;}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_selector_class_multiple)

通过把两个类选择器链接在一起，仅可以选择*同时包含这些类名*的元素（类名的顺序不限）。

如果一个多类选择器包含类名列表中没有的一个类名，匹配就会失败。请看下面的规则：

```
.important.urgent {background:silver;}
```

不出所料，这个选择器将只匹配 class 属性中包含词 important 和 urgent 的 p 元素。因此，如果一个 p 元素的 class 属性中只有词 important 和 warning，将不能匹配。不过，它能匹配以下元素：

```
<p class="important urgent warning">
This paragraph is a very important and urgent warning.
</p>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_selector_class_multiple_2)

重要事项：在 IE7 之前的版本中，不同平台的 Internet Explorer 都不能正确地处理多类选择器。

## CSS ID 选择器详解

**ID 选择器允许以一种独立于文档元素的方式来指定样式。**

### CSS ID 选择器

在某些方面，ID 选择器类似于类选择器，不过也有一些重要差别。

#### 语法

首先，ID 选择器前面有一个 # 号 - 也称为棋盘号或井号。

请看下面的规则：

```
*#intro {font-weight:bold;}
```

与类选择器一样，ID 选择器中可以忽略通配选择器。前面的例子也可以写作：

```
#intro {font-weight:bold;}
```

这个选择器的效果将是一样的。

第二个区别是 ID 选择器不引用 class 属性的值，毫无疑问，它要引用 id 属性中的值。

以下是一个实际 ID 选择器的例子：

```
<p id="intro">This is a paragraph of introduction.</p>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_selector_id)

### 类选择器还是 ID 选择器？

在类选择器这一章中我们曾讲解过，可以为任意多个元素指定类。前一章中类名 important 被应用到 p 和 h1 元素，而且它还可以应用到更多元素。

#### 区别 1：只能在文档中使用一次

与类不同，在一个 HTML 文档中，ID 选择器会使用一次，而且仅一次。

#### 区别 2：不能使用 ID 词列表

不同于类选择器，ID 选择器不能结合使用，因为 ID 属性不允许有以空格分隔的词列表。

#### 区别 3：ID 能包含更多含义

类似于类，可以独立于元素来选择 ID。有些情况下，您知道文档中会出现某个特定 ID 值，但是并不知道它会出现在哪个元素上，所以您想声明独立的 ID 选择器。例如，您可能知道在一个给定的文档中会有一个 ID 值为 mostImportant 的元素。您不知道这个最重要的东西是一个段落、一个短语、一个列表项还是一个小节标题。您只知道每个文档都会有这么一个最重要的内容，它可能在任何元素中，而且只能出现一个。在这种情况下，可以编写如下规则：

```
#mostImportant {color:red; background:yellow;}
```

这个规则会与以下各个元素匹配（这些元素不能在同一个文档中同时出现，因为它们都有相同的 ID 值）：

```
<h1 id="mostImportant">This is important!</h1>
<em id="mostImportant">This is important!</em>
<ul id="mostImportant">This is important!</ul>
```

亲自试一试：

- [为 id 为 mostImportant 的 h1 元素设定样式](http://www.w3school.com.cn/tiy/t.asp?f=csse_selector_id_h1)
- [为 id 为 mostImportant 的 em 元素设定样式](http://www.w3school.com.cn/tiy/t.asp?f=csse_selector_id_em)
- [为 id 为 mostImportant 的 ul 元素设定样式](http://www.w3school.com.cn/tiy/t.asp?f=csse_selector_id_ul)

### 区分大小写

请注意，类选择器和 ID 选择器可能是区分大小写的。这取决于文档的语言。HTML 和 XHTML 将类和 ID 值定义为区分大小写，所以类和 ID 值的大小写必须与文档中的相应值匹配。

因此，对于以下的 CSS 和 HTML，元素不会变成粗体：

```
#intro {font-weight:bold;}

<p id="Intro">This is a paragraph of introduction.</p>
```

由于字母 i 的大小写不同，所以选择器不会匹配上面的元素。

## CSS 属性选择器详解



**CSS 2 引入了属性选择器。**

**属性选择器可以根据元素的属性及属性值来选择元素。**

### 简单属性选择

如果希望选择有某个属性的元素，而不论属性值是什么，可以使用简单属性选择器。

#### 例子 1

如果您希望把包含标题（title）的所有元素变为红色，可以写作：

```
*[title] {color:red;}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_selector_attribute_att)

#### 例子 2

与上面类似，可以只对有 href 属性的锚（a 元素）应用样式：

```
a[href] {color:red;}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_selector_attribute_att_2)

#### 例子 3

还可以根据多个属性进行选择，只需将属性选择器链接在一起即可。

例如，为了将同时有 href 和 title 属性的 HTML 超链接的文本设置为红色，可以这样写：

```
a[href][title] {color:red;}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_selector_attribute_att_3)

#### 例子 4

可以采用一些创造性的方法使用这个特性。

例如，可以对所有带有 alt 属性的图像应用样式，从而突出显示这些有效的图像：

```
img[alt] {border: 5px solid red;}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_selector_attribute_att_4)

提示：上面这个特例更适合用来诊断而不是设计，即用来确定图像是否确实有效。

#### 例子 5：为 XML 文档使用属性选择器

属性选择器在 XML 文档中相当有用，因为 XML 语言主张要针对元素和属性的用途指定元素名和属性名。

假设我们为描述太阳系行星设计了一个 XML 文档。如果我们想选择有 moons 属性的所有 planet 元素，使之显示为红色，以便能更关注有 moons 的行星，就可以这样写：

```
planet[moons] {color:red;}
```

这会让以下标记片段中的第二个和第三个元素的文本显示为红色，但第一个元素的文本不是红色：

```
<planet>Venus</planet>
<planet moons="1">Earth</planet>
<planet moons="2">Mars</planet>
```

[查看效果](http://www.w3school.com.cn/css/planetml_attselector_att.xml)

### 根据具体属性值选择

除了选择拥有某些属性的元素，还可以进一步缩小选择范围，只选择有特定属性值的元素。

#### 例子 1

例如，假设希望将指向 Web 服务器上某个指定文档的超链接变成红色，可以这样写：

```
a[href="http://www.w3school.com.cn/about_us.asp"] {color: red;}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_selector_attribute_value_1)

#### 例子 2

与简单属性选择器类似，可以把多个属性-值选择器链接在一起来选择一个文档。

```
a[href="http://www.w3school.com.cn/"][title="W3School"] {color: red;}
```

这会把以下标记中的第一个超链接的文本变为红色，但是第二个或第三个链接不受影响：

```
<a href="http://www.w3school.com.cn/" title="W3School">W3School</a>
<a href="http://www.w3school.com.cn/css/" title="CSS">CSS</a>
<a href="http://www.w3school.com.cn/html/" title="HTML">HTML</a>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_selector_attribute_value_2)

#### 例子 3

同样地，XML 语言也可以利用这种方法来设置样式。

下面我们再回到行星那个例子中。假设只希望选择 moons 属性值为 1 的那些 planet 元素：

```
planet[moons="1"] {color: red;}
```

上面的代码会把以下标记中的第二个元素变成红色，但第一个和第三个元素不受影响：

```
<planet>Venus</planet>
<planet moons="1">Earth</planet>
<planet moons="2">Mars</planet>
```

[查看效果](http://www.w3school.com.cn/css/planetml_attselector_val.xml)

#### 属性与属性值必须完全匹配

请注意，这种格式要求必须与属性值完全匹配。

如果属性值包含用空格分隔的值列表，匹配就可能出问题。

请考虑一下的标记片段：

```
<p class="important warning">This paragraph is a very important warning.</p>
```

如果写成 p[class="important"]，那么这个规则不能匹配示例标记。

要根据具体属性值来选择该元素，必须这样写：

```
p[class="important warning"] {color: red;}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_selector_attribute_value_3)

### 根据部分属性值选择

如果需要根据属性值中的词列表的某个词进行选择，则需要使用波浪号（~）。

假设您想选择 class 属性中包含 important 的元素，可以用下面这个选择器做到这一点：

```
p[class~="important"] {color: red;}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_selector_attribute_valuelist_space_1)

如果忽略了波浪号，则说明需要完成完全值匹配。

#### 部分值属性选择器与点号类名记法的区别

该选择器等价于我们在类选择器中讨论过的点号类名记法。

也就是说，p.important 和 p[class="important"] 应用到 HTML 文档时是等价的。

那么，为什么还要有 "~=" 属性选择器呢？因为它能用于任何属性，而不只是 class。

例如，可以有一个包含大量图像的文档，其中只有一部分是图片。对此，可以使用一个基于 title 文档的部分属性选择器，只选择这些图片：

```
img[title~="Figure"] {border: 1px solid gray;}
```

这个规则会选择 title 文本包含 "Figure" 的所有图像。没有 title 属性或者 title 属性中不包含 "Figure" 的图像都不会匹配。

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_selector_attribute_valuelist_space_2)

#### 子串匹配属性选择器

下面为您介绍一个更高级的选择器模块，它是 CSS2 完成之后发布的，其中包含了更多的部分值属性选择器。按照规范的说法，应该称之为“子串匹配属性选择器”。

很多现代浏览器都支持这些选择器，包括 IE7。

下表是对这些选择器的简单总结：

| 类型         | 描述                                       |
| ------------ | ------------------------------------------ |
| [abc^="def"] | 选择 abc 属性值以 "def" 开头的所有元素     |
| [abc$="def"] | 选择 abc 属性值以 "def" 结尾的所有元素     |
| [abc*="def"] | 选择 abc 属性值中包含子串 "def" 的所有元素 |

可以想到，这些选择有很多用途。

举例来说，如果希望对指向 W3School 的所有链接应用样式，不必为所有这些链接指定 class，再根据这个类编写样式，而只需编写以下规则：

```
a[href*="w3school.com.cn"] {color: red;}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_selector_attribute_substring_matching)

提示：任何属性都可以使用这些选择器。

### 特定属性选择类型

最后为您介绍特定属性选择器。请看下面的例子：

```
*[lang|="en"] {color: red;}
```

上面这个规则会选择 lang 属性等于 en 或以 en- 开头的所有元素。因此，以下示例标记中的前三个元素将被选中，而不会选择后两个元素：

```
<p lang="en">Hello!</p>
<p lang="en-us">Greetings!</p>
<p lang="en-au">G'day!</p>
<p lang="fr">Bonjour!</p>
<p lang="cy-en">Jrooana!</p>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_selector_attribute_valuelist_hyphen_1)

一般来说，[att|="val"] 可以用于任何属性及其值。

假设一个 HTML 文档中有一系列图片，其中每个图片的文件名都形如 *figure-1.jpg* 和 *figure-2.jpg*。就可以使用以下选择器匹配所有这些图像：

```
img[src|="figure"] {border: 1px solid gray;}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_selector_attribute_valuelist_hyphen_2)

当然，这种属性选择器最常见的用途还是匹配语言值。

### CSS 选择器参考手册

| 选择器                                                       | 描述                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| [[*attribute*\]](http://www.w3school.com.cn/cssref/selector_attribute.asp) | 用于选取带有指定属性的元素。                                 |
| [[*attribute*=*value*\]](http://www.w3school.com.cn/cssref/selector_attribute_value.asp) | 用于选取带有指定属性和值的元素。                             |
| [[*attribute*~=*value*\]](http://www.w3school.com.cn/cssref/selector_attribute_value_contain.asp) | 用于选取属性值中包含指定词汇的元素。                         |
| [[*attribute*\|=*value*\]](http://www.w3school.com.cn/cssref/selector_attribute_value_start.asp) | 用于选取带有以指定值开头的属性值的元素，该值必须是整个单词。 |
| [[*attribute*^=*value*\]](http://www.w3school.com.cn/cssref/selector_attr_begin.asp) | 匹配属性值以指定值开头的每个元素。                           |
| [[*attribute*$=*value*\]](http://www.w3school.com.cn/cssref/selector_attr_end.asp) | 匹配属性值以指定值结尾的每个元素。                           |
| [[*attribute**=*value*\]](http://www.w3school.com.cn/cssref/selector_attr_contain.asp) | 匹配属性值中包含指定值的每个元素。                           |

## CSS 后代选择器



**后代选择器（descendant selector）又称为包含选择器。**

**后代选择器可以选择作为某元素后代的元素。**

### 根据上下文选择元素

我们可以定义后代选择器来创建一些规则，使这些规则在某些文档结构中起作用，而在另外一些结构中不起作用。

举例来说，如果您希望只对 h1 元素中的 em 元素应用样式，可以这样写：

```
h1 em {color:red;}
```

上面这个规则会把作为 h1 元素后代的 em 元素的文本变为 红色。其他 em 文本（如段落或块引用中的 em）则不会被这个规则选中：

```
<h1>This is a <em>important</em> heading</h1>
<p>This is a <em>important</em> paragraph.</p>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_selector_descendant_1)

当然，您也可以在 h1 中找到的每个 em 元素上放一个 class 属性，但是显然，后代选择器的效率更高。

### 语法解释

在后代选择器中，规则左边的选择器一端包括两个或多个用空格分隔的选择器。选择器之间的空格是一种结合符（combinator）。每个空格结合符可以解释为“... 在 ... 找到”、“... 作为 ... 的一部分”、“... 作为 ... 的后代”，但是要求必须从右向左读选择器。

因此，h1 em 选择器可以解释为 “作为 h1 元素后代的任何 em 元素”。如果要从左向右读选择器，可以换成以下说法：“包含 em 的所有 h1 会把以下样式应用到该 em”。

### 具体应用

后代选择器的功能极其强大。有了它，可以使 HTML 中不可能实现的任务成为可能。

假设有一个文档，其中有一个边栏，还有一个主区。边栏的背景为蓝色，主区的背景为白色，这两个区都包含链接列表。不能把所有链接都设置为蓝色，因为这样一来边栏中的蓝色链接都无法看到。

解决方法是使用后代选择器。在这种情况下，可以为包含边栏的 div 指定值为 sidebar 的 class 属性，并把主区的 class 属性值设置为 maincontent。然后编写以下样式：

```
div.sidebar {background:blue;}
div.maincontent {background:white;}
div.sidebar a:link {color:white;}
div.maincontent a:link {color:blue;}
```

有关后代选择器有一个易被忽视的方面，即两个元素之间的层次间隔可以是无限的。

例如，如果写作 ul em，这个语法就会选择从 ul 元素继承的所有 em 元素，而不论 em 的嵌套层次多深。

因此，ul em 将会选择以下标记中的所有 em 元素：

```
<ul>
  <li>List item 1
    <ol>
      <li>List item 1-1</li>
      <li>List item 1-2</li>
      <li>List item 1-3
        <ol>
          <li>List item 1-3-1</li>
          <li>List item <em>1-3-2</em></li>
          <li>List item 1-3-3</li>
        </ol>
      </li>
      <li>List item 1-4</li>
    </ol>
  </li>
  <li>List item 2</li>
  <li>List item 3</li>
</ul>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_selector_descendant)



## CSS 子元素选择器

**与后代选择器相比，子元素选择器（Child selectors）只能选择作为某元素子元素的元素。**

### 选择子元素

如果您不希望选择任意的后代元素，而是希望缩小范围，只选择某个元素的子元素，请使用子元素选择器（Child selector）。

例如，如果您希望选择只作为 h1 元素子元素的 strong 元素，可以这样写：

```
h1 > strong {color:red;}
```

这个规则会把第一个 h1 下面的两个 strong 元素变为红色，但是第二个 h1 中的 strong 不受影响：

```
<h1>This is <strong>very</strong> <strong>very</strong> important.</h1>
<h1>This is <em>really <strong>very</strong></em> important.</h1>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_selector_child)

### 语法解释

您应该已经注意到了，子选择器使用了大于号（子结合符）。

子结合符两边可以有空白符，这是可选的。因此，以下写法都没有问题：

```
h1 > strong
h1> strong
h1 >strong
h1>strong
```

如果从右向左读，选择器 h1 > strong 可以解释为“选择作为 h1 元素子元素的所有 strong 元素”。

### 结合后代选择器和子选择器

请看下面这个选择器：

```
table.company td > p
```

上面的选择器会选择作为 td 元素子元素的所有 p 元素，这个 td 元素本身从 table 元素继承，该 table 元素有一个包含 company 的 class 属性。

## CSS 相邻兄弟选择器



**相邻兄弟选择器（Adjacent sibling selector）可选择紧接在另一元素后的元素，且二者有相同父元素。**

### 选择相邻兄弟

如果需要选择紧接在另一个元素后的元素，而且二者有相同的父元素，可以使用相邻兄弟选择器（Adjacent sibling selector）。

例如，如果要增加紧接在 h1 元素后出现的段落的上边距，可以这样写：

```
h1 + p {margin-top:50px;}
```

这个选择器读作：“选择紧接在 h1 元素后出现的段落，h1 和 p 元素拥有共同的父元素”。

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_selector_adjacent_sibling)

### 语法解释

相邻兄弟选择器使用了加号（+），即相邻兄弟结合符（Adjacent sibling combinator）。

注释：与子结合符一样，相邻兄弟结合符旁边可以有空白符。

请看下面这个文档树片段：

```
<div>
  <ul>
    <li>List item 1</li>
    <li>List item 2</li>
    <li>List item 3</li>
  </ul>
  <ol>
    <li>List item 1</li>
    <li>List item 2</li>
    <li>List item 3</li>
  </ol>
</div>
```

在上面的片段中，div 元素中包含两个列表：一个无序列表，一个有序列表，每个列表都包含三个列表项。这两个列表是相邻兄弟，列表项本身也是相邻兄弟。不过，第一个列表中的列表项与第二个列表中的列表项不是相邻兄弟，因为这两组列表项不属于同一父元素（最多只能算堂兄弟）。

请记住，用一个结合符只能选择两个相邻兄弟中的第二个元素。请看下面的选择器：

```
li + li {font-weight:bold;}
```

上面这个选择器只会把列表中的第二个和第三个列表项变为粗体。第一个列表项不受影响。

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_selector_adjacent_sibling_2)

### 结合其他选择器

相邻兄弟结合符还可以结合其他结合符：

```
html > body table + ul {margin-top:20px;}
```

这个选择器解释为：选择紧接在 table 元素后出现的所有兄弟 ul 元素，该 table 元素包含在一个 body 元素中，body 元素本身是 html 元素的子元素。



## CSS 伪类 (Pseudo-classes)



**CSS 伪类用于向某些选择器添加特殊的效果。**

### CSS 伪类 (Pseudo-classes)实例：

- [超链接](http://www.w3school.com.cn/tiy/t.asp?f=csse_link)

  本例演示如何向文档中的超链接添加不同的颜色。

- [超链接 2](http://www.w3school.com.cn/tiy/t.asp?f=csse_link2)

  本例演示如何向超链接添加其他样式。

- [超链接 - :focus 的使用](http://www.w3school.com.cn/tiy/t.asp?f=csse_link_focus)

  本例演示如何对超链接应用 :focus 伪类（无法在 IE 中工作）。

- [:first-child（首个子对象）](http://www.w3school.com.cn/tiy/t.asp?f=csse_first-child)

  本例演示 :first-child 伪类的用法。

- [:lang（语言）](http://www.w3school.com.cn/tiy/t.asp?f=csse_lang)

  本例演示 :lang 伪类的用法。

### 语法

伪类的语法：

```
selector : pseudo-class {property: value}
```

CSS 类也可与伪类搭配使用。

```
selector.class : pseudo-class {property: value}
```

### 锚伪类

在支持 CSS 的浏览器中，链接的不同状态都可以不同的方式显示，这些状态包括：活动状态，已被访问状态，未被访问状态，和鼠标悬停状态。

```
a:link {color: #FF0000}		/* 未访问的链接 */
a:visited {color: #00FF00}	/* 已访问的链接 */
a:hover {color: #FF00FF}	/* 鼠标移动到链接上 */
a:active {color: #0000FF}	/* 选定的链接 */
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_link)

提示：在 CSS 定义中，a:hover 必须被置于 a:link 和 a:visited 之后，才是有效的。

提示：在 CSS 定义中，a:active 必须被置于 a:hover 之后，才是有效的。

提示：伪类名称对大小写不敏感。

### 伪类与 CSS 类

伪类可以与 CSS 类配合使用：

```
a.red : visited {color: #FF0000}

<a class="red" href="css_syntax.asp">CSS Syntax</a>
```

假如上面的例子中的链接被访问过，那么它将显示为红色。

### CSS2 - :first-child 伪类

您可以使用 :first-child 伪类来选择元素的第一个子元素。这个特定伪类很容易遭到误解，所以有必要举例来说明。考虑以下标记：

```
<div>
<p>These are the necessary steps:</p>
<ul>
<li>Intert Key</li>
<li>Turn key <strong>clockwise</strong></li>
<li>Push accelerator</li>
</ul>
<p>Do <em>not</em> push the brake at the same time as the accelerator.</p>
</div>
```

在上面的例子中，作为第一个元素的元素包括第一个 p、第一个 li 和 strong 和 em 元素。

给定以下规则：

```
p:first-child {font-weight: bold;}
li:first-child {text-transform:uppercase;}
```

第一个规则将作为某元素第一个子元素的所有 p 元素设置为粗体。第二个规则将作为某个元素（在 HTML 中，这肯定是 ol 或 ul 元素）第一个子元素的所有 li 元素变成大写。

请访问该链接，来查看这个 [:first-child 实例](http://www.w3school.com.cn/tiy/t.asp?f=csse_first-child)的效果。

提示：最常见的错误是认为 p:first-child 之类的选择器会选择 p 元素的第一个子元素。

注释：必须声明 [](http://www.w3school.com.cn/tags/tag_doctype.asp)，这样 :first-child 才能在 IE 中生效。

为了使您更透彻地理解 :first-child 伪类，我们另外提供了 3 个例子：

#### 例子 1 - 匹配第一个 <p> 元素

在下面的例子中，选择器匹配作为任何元素的第一个子元素的 p 元素：

```
<html>
<head>
<style type="text/css">
p:first-child {
  color: red;
  } 
</style>
</head>

<body>
<p>some text</p>
<p>some text</p>
</body>
</html>
```

[TIY](http://www.w3school.com.cn/tiy/t.asp?f=csse_first-child_1)

#### 例子 2 - 匹配所有 <p> 元素中的第一个 <i> 元素

在下面的例子中，选择器匹配所有 <p> 元素中的第一个 <i> 元素：

```
<html>
<head>
<style type="text/css">
p > i:first-child {
  font-weight:bold;
  } 
</style>
</head>

<body>
<p>some <i>text</i>. some <i>text</i>.</p>
<p>some <i>text</i>. some <i>text</i>.</p>
</body>
</html>
```

[TIY](http://www.w3school.com.cn/tiy/t.asp?f=csse_first-child_2)

#### 例子 3 - 匹配所有作为第一个子元素的 <p> 元素中的所有 <i> 元素

在下面的例子中，选择器匹配所有作为元素的第一个子元素的 <p> 元素中的所有 <i> 元素：

```
<html>
<head>
<style type="text/css">
p:first-child i {
  color:blue;
  } 
</style>
</head>

<body>
<p>some <i>text</i>. some <i>text</i>.</p>
<p>some <i>text</i>. some <i>text</i>.</p>
</body>
</html>
```

[TIY](http://www.w3school.com.cn/tiy/t.asp?f=csse_first-child_3)

### CSS2 - :lang 伪类

:lang 伪类使你有能力为不同的语言定义特殊的规则。在下面的例子中，:lang 类为属性值为 no 的 q 元素定义引号的类型：

```
<html>
<head>

<style type="text/css">
q:lang(no) {
   quotes: "~" "~"
   }
</style>

</head>

<body>
<p>文字<q lang="no">段落中的引用的文字</q>文字</p>
</body></html>
```

### 伪类

*W3C*："W3C" 列指示出该属性在哪个 CSS 版本中定义（CSS1 还是 CSS2）。

| 属性                                                         | 描述                                     | CSS  |
| ------------------------------------------------------------ | ---------------------------------------- | ---- |
| [:active](http://www.w3school.com.cn/cssref/pr_pseudo_active.asp) | 向被激活的元素添加样式。                 | 1    |
| [:focus](http://www.w3school.com.cn/cssref/pr_pseudo_focus.asp) | 向拥有键盘输入焦点的元素添加样式。       | 2    |
| [:hover](http://www.w3school.com.cn/cssref/pr_pseudo_hover.asp) | 当鼠标悬浮在元素上方时，向元素添加样式。 | 1    |
| [:link](http://www.w3school.com.cn/cssref/pr_pseudo_link.asp) | 向未被访问的链接添加样式。               | 1    |
| [:visited](http://www.w3school.com.cn/cssref/pr_pseudo_visited.asp) | 向已被访问的链接添加样式。               | 1    |
| [:first-child](http://www.w3school.com.cn/cssref/pr_pseudo_first-child.asp) | 向元素的第一个子元素添加样式。           | 2    |
| [:lang](http://www.w3school.com.cn/cssref/pr_pseudo_lang.asp) | 向带有指定 lang 属性的元素添加样式。     | 2    |



## CSS 伪元素 (Pseudo-elements)



**CSS 伪元素用于向某些选择器设置特殊效果。**

### 语法

伪元素的语法：

```
selector:pseudo-element {property:value;}
```

CSS 类也可以与伪元素配合使用：

```
selector.class:pseudo-element {property:value;}
```

### :first-line 伪元素

"first-line" 伪元素用于向文本的首行设置特殊样式。

在下面的例子中，浏览器会根据 "first-line" 伪元素中的样式对 p 元素的第一行文本进行格式化：

#### 实例

```
p:first-line
  {
  color:#ff0000;
  font-variant:small-caps;
  }
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_firstline)

注释："first-line" 伪元素只能用于块级元素。

注释：下面的属性可应用于 "first-line" 伪元素：

- font
- color
- background
- word-spacing
- letter-spacing
- text-decoration
- vertical-align
- text-transform
- line-height
- clear

### :first-letter 伪元素

"first-letter" 伪元素用于向文本的首字母设置特殊样式：

```
p:first-letter
  {
  color:#ff0000;
  font-size:xx-large;
  }
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_firstletter)

注释："first-letter" 伪元素只能用于块级元素。

注释：下面的属性可应用于 "first-letter" 伪元素：

- font
- color
- background
- margin
- padding
- border
- text-decoration
- vertical-align (仅当 float 为 none 时)
- text-transform
- line-height
- float
- clear

### 伪元素和 CSS 类

伪元素可以与 CSS 类配合使用：

```
p.article:first-letter
  {
  color: #FF0000;
  }

<p class="article">This is a paragraph in an article。</p>
```

上面的例子会使所有 class 为 article 的段落的首字母变为红色。

### 多重伪元素

可以结合多个伪元素来使用。

在下面的例子中，段落的第一个字母将显示为红色，其字体大小为 xx-large。第一行中的其余文本将为蓝色，并以小型大写字母显示。段落中的其余文本将以默认字体大小和颜色来显示：

```
p:first-letter
  {
  color:#ff0000;
  font-size:xx-large;
  }

p:first-line
  {
  color:#0000ff;
  font-variant:small-caps;
  }
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_firstletter_firstline)

### CSS2 - :before 伪元素

":before" 伪元素可以在元素的内容前面插入新内容。

下面的例子在每个 <h1> 元素前面插入一幅图片：

```
h1:before
  {
  content:url(logo.gif);
  }
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_before)

### CSS2 - :after 伪元素

":after" 伪元素可以在元素的内容之后插入新内容。

下面的例子在每个 <h1> 元素后面插入一幅图片：

```
h1:after
  {
  content:url(logo.gif);
  }
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=csse_after)

### 伪元素

*W3C*："W3C" 列指示出该属性在哪个 CSS 版本中定义（CSS1 还是 CSS2）。

| 属性                                                         | 描述                             | CSS  |
| ------------------------------------------------------------ | -------------------------------- | ---- |
| [:first-letter](http://www.w3school.com.cn/cssref/pr_pseudo_first-letter.asp) | 向文本的第一个字母添加特殊样式。 | 1    |
| [:first-line](http://www.w3school.com.cn/cssref/pr_pseudo_first-line.asp) | 向文本的首行添加特殊样式。       | 1    |
| [:before](http://www.w3school.com.cn/cssref/pr_pseudo_before.asp) | 在元素之前添加内容。             | 2    |
| [:after](http://www.w3school.com.cn/cssref/pr_pseudo_after.asp) | 在元素之后添加内容。             | 2    |

css

















# CSS 精通

## CSS 水平对齐



在 CSS 中，可以使用多种属性来水平对齐元素。

### 对齐块元素

块元素指的是占据全部可用宽度的元素，并且在其前后都会换行。

块元素的例子：

```
<h1>
<p>
<div>
```

对于文本对齐，请参见 [CSS 文本](http://www.w3school.com.cn/css/css_text.asp)一章。

在本教程中，我们将向您展示出于布局目的如何水平对齐块级元素。

### 使用 margin 属性来水平对齐

可通过将左和右外边距设置为 "auto"，来对齐块元素。

注释：除非已经声明了 !DOCTYPE，否则使用 margin:auto 在 IE8 以及更早的版本中是无效的。

把左和右外边距设置为 auto，规定的是均等地分配可用的外边距。结果就是居中的元素：

#### 实例

```
.center
{
margin-left:auto;
margin-right:auto;
width:70%;
background-color:#b0e0e6;
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css_align_margin)

提示：如果宽度是 100%，则对齐没有效果。

注释：在 IE5 中，对于块元素存在一个外边距处理方面的 BUG。如需使上面的例子在 IE5 中有效，请添加一些额外的代码。[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css_align_margin_ie5)。

### 使用 position 属性进行左和右对齐

对齐元素的方法之一是使用绝对定位：

#### 实例

```
.right
{
position:absolute;
right:0px;
width:300px;
background-color:#b0e0e6;
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css_align_position)

注释：绝对定位元素会被从正常流中删除，并且能够交叠元素。

### 跨浏览器兼容性问题

当像这样对齐元素时，对 <body> 元素的外边距和内边距进行预定义是一个好主意。这样可以避免在不同的浏览器中出现可见的差异。

当使用 position 属性时，IE8 以及更早的版本存在一个问题。如果容器元素（在我们的案例中是 <div class="container">）设置了指定的宽度，并且省略了 !DOCTYPE 声明，那么 IE8 以及更早的版本会在右侧增加 17px 的外边距。这似乎是为滚动条预留的空间。当使用 position 属性时，请始终设置 !DOCTYPE 声明：

#### 实例

```
body
{
margin:0;
padding:0;
}
.container
{
position:relative;
width:100%;
}
.right
{
position:absolute;
right:0px;
width:300px;
background-color:#b0e0e6;
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css_align_position_crossbrowser)

### 使用 float 属性来进行左和右对齐

对齐元素的另一种方法是使用 float 属性：

#### 实例

```
.right
{
float:right;
width:300px;
background-color:#b0e0e6;
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css_align_float)

### 跨浏览器兼容性问题

当像这样对齐元素时，对 <body> 元素的外边距和内边距进行预定义是一个好主意。这样可以避免在不同的浏览器中出现可见的差异。

当使用 float 属性时，IE8 以及更早的版本存在一个问题。如果省略 !DOCTYPE 声明，那么 IE8 以及更早的版本会在右侧增加 17px 的外边距。这似乎是为滚动条预留的空间。当使用 float 属性时，请始终设置 !DOCTYPE 声明：

#### 实例

```
body
{
margin:0;
padding:0;
}

.right
{
float:right;
width:300px;
background-color:#b0e0e6;
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css_align_float_crossbrowser)

## CSS 尺寸 (Dimension)

**CSS 尺寸 (Dimension) 属性允许你控制元素的高度和宽度。同样，它允许你增加行间距。**

### CSS 尺寸实例：

- [使用像素值设置图像的高度](http://www.w3school.com.cn/tiy/t.asp?f=csse_dim_height)

  本例演示如何使用像素值设置元素的高度。

- [使用百分比设置图像的高度](http://www.w3school.com.cn/tiy/t.asp?f=csse_dim_height_percent)

  本例演示如何使用百分比值来设置元素的高度。

- [使用像素值来设置元素的宽度](http://www.w3school.com.cn/tiy/t.asp?f=csse_dim_width)

  本例演示如何使用像素值来设置元素的宽度。

- [使用百分比来设置元素的宽度](http://www.w3school.com.cn/tiy/t.asp?f=csse_dim_width_percent)

  本例演示如何使用百分比值来设置元素的宽度。

- [设置元素的最大高度](http://www.w3school.com.cn/tiy/t.asp?f=csse_dim_max-height)

  本例演示如何设置一个元素的最大高度。

- [使用像素值来设置元素的最大宽度](http://www.w3school.com.cn/tiy/t.asp?f=csse_dim_max-width)

  本例演示如何使用像素值来设置元素的最大高度。

- [使用百分比来设置元素的最大宽度](http://www.w3school.com.cn/tiy/t.asp?f=csse_dim_max-width_percent)

  本例演示如何使用百分比值来设置元素的最大高度。

- [使用像素值来设置元素的最小高度](http://www.w3school.com.cn/tiy/t.asp?f=csse_dim_min-height)

  本例演示如何使用像素值来设置元素的最小高度。

- [使用像素值来设置元素的最小宽度](http://www.w3school.com.cn/tiy/t.asp?f=csse_dim_min-width)

  本例演示如何使用像素值来设置元素的最小宽度。

- [使用百分比来设置元素的最小宽度](http://www.w3school.com.cn/tiy/t.asp?f=csse_dim_min-width_percent)

  本例演示如何使用百分比值来设置元素的最小宽度。

- [使用百分比设置行间距](http://www.w3school.com.cn/tiy/t.asp?f=csse_dim_line-height_percent)

  本例演示如何使用百分比值来设置段落中的行间距。

- [使用像素值设置行间距](http://www.w3school.com.cn/tiy/t.asp?f=csse_dim_line-height_pixel)

  本例演示如何使用像素值来设置段落中的行间距。

- [使用数值来设置行间距](http://www.w3school.com.cn/tiy/t.asp?f=csse_dim_line-height_number)

  本例演示如何使用一个数值来设置段落中的行间距。

### CSS 尺寸属性

CSS 尺寸属性允许你控制元素的高度和宽度。同样，还允许你增加行间距。

| 属性                                                         | 描述                 |
| ------------------------------------------------------------ | -------------------- |
| [height](http://www.w3school.com.cn/cssref/pr_dim_height.asp) | 设置元素的高度。     |
| [line-height](http://www.w3school.com.cn/cssref/pr_dim_line-height.asp) | 设置行高。           |
| [max-height](http://www.w3school.com.cn/cssref/pr_dim_max-height.asp) | 设置元素的最大高度。 |
| [max-width](http://www.w3school.com.cn/cssref/pr_dim_max-width.asp) | 设置元素的最大宽度。 |
| [min-height](http://www.w3school.com.cn/cssref/pr_dim_min-height.asp) | 设置元素的最小高度。 |
| [min-width](http://www.w3school.com.cn/cssref/pr_dim_min-width.asp) | 设置元素的最小宽度。 |
| [width](http://www.w3school.com.cn/cssref/pr_dim_width.asp)  | 设置元素的宽度。     |

## CSS 分类 (Classification)



**CSS 分类属性允许你规定如何以及在何处显示元素。**

### CSS分类(Classification)实例：

- [如何把元素显示为内联元素](http://www.w3school.com.cn/tiy/t.asp?f=csse_display)

  本例演示如何把元素显示为内联元素。

- [如何把元素显示为块级元素](http://www.w3school.com.cn/tiy/t.asp?f=csse_display_block)

  本例演示如何把元素显示为块级元素。

- [float 属性的简单应用](http://www.w3school.com.cn/tiy/t.asp?f=csse_float)

  使图像浮动于一个段落的右侧。

- [将带有边框和边界的图像浮动于段落的右侧](http://www.w3school.com.cn/tiy/t.asp?f=csse_float2)

  使图像浮动于段落的右侧。向图像添加边框和边界。

- [带标题的图像浮动于右侧](http://www.w3school.com.cn/tiy/t.asp?f=csse_float3)

  使带有标题的图像浮动于右侧

- [使段落的首字母浮动于左侧](http://www.w3school.com.cn/tiy/t.asp?f=csse_float4)

  使段落的首字母浮动于左侧，并向这个字母添加样式。

- [创建水平菜单](http://www.w3school.com.cn/tiy/t.asp?f=csse_float5)

  使用具有一栏超链接的浮动来创建水平菜单。

- [创建无表格的首页](http://www.w3school.com.cn/tiy/t.asp?f=csse_float6)

  使用浮动来创建拥有页眉、页脚、左侧目录和主体内容的首页。

- [定位：相对定位](http://www.w3school.com.cn/tiy/t.asp?f=csse_position_relative)

  本例演示如何相对于一个元素的正常位置来对其定位。

- [定位：绝对定位](http://www.w3school.com.cn/tiy/t.asp?f=csse_position_absolute)

  本例演示如何使用绝对值来对元素进行定位。

- [定位：固定定位](http://www.w3school.com.cn/tiy/t.asp?f=csse_position_fixed)

  本例演示如何相对于浏览器窗口来对元素进行定位。

- [如何使元素不可见](http://www.w3school.com.cn/tiy/t.asp?f=csse_visibility)

  本例演示如何使元素不可见。你希望元素被显示出来，还是不呢？

- [把表格元素设置为 collapse（请在非 IE 的浏览器中查看）](http://www.w3school.com.cn/tiy/t.asp?f=csse_visibility_collapse)

  本例演示如何使表格元素叠加？

- [改变光标](http://www.w3school.com.cn/tiy/t.asp?f=csse_cursor)

  本例演示如何改变光标。

- [清除元素的侧面](http://www.w3school.com.cn/tiy/t.asp?f=csse_class-clear)

  本例演示如何使用清除元素侧面的浮动元素。

### CSS 分类属性 (Classification)

CSS 分类属性允许你控制如何显示元素，设置图像显示于另一元素中的何处，相对于其正常位置来定位元素，使用绝对值来定位元素，以及元素的可见度。

| 属性                                                         | 描述                                                     |
| ------------------------------------------------------------ | -------------------------------------------------------- |
| [clear](http://www.w3school.com.cn/cssref/pr_class_clear.asp) | 设置一个元素的侧面是否允许其他的浮动元素。               |
| [cursor](http://www.w3school.com.cn/cssref/pr_class_cursor.asp) | 规定当指向某元素之上时显示的指针类型。                   |
| [display](http://www.w3school.com.cn/cssref/pr_class_display.asp) | 设置是否及如何显示元素。                                 |
| [float](http://www.w3school.com.cn/cssref/pr_class_float.asp) | 定义元素在哪个方向浮动。                                 |
| [position](http://www.w3school.com.cn/cssref/pr_class_position.asp) | 把元素放置到一个静态的、相对的、绝对的、或固定的位置中。 |
| [visibility](http://www.w3school.com.cn/cssref/pr_class_visibility.asp) | 设置元素是否可见或不可见。                               |

## CSS 导航条

### 演示：导航栏

- [HOME](http://www.w3school.com.cn/css/css_navbar.asp#)
- [NEWS](http://www.w3school.com.cn/css/css_navbar.asp#)
- [ARTICLES](http://www.w3school.com.cn/css/css_navbar.asp#)
- [FORUM](http://www.w3school.com.cn/css/css_navbar.asp#)
- [CONTACT](http://www.w3school.com.cn/css/css_navbar.asp#)
- [ABOUT](http://www.w3school.com.cn/css/css_navbar.asp#)



### 导航栏

拥有易用的导航条对于任何网站都很重要。

通过 CSS，您能够把乏味的 HTML 菜单转换为漂亮的导航栏。

### 导航栏 = 链接列表

导航栏需要标准的 HTML 作为基础。

在我们的例子中，将用标准的 HTML 列表来构建导航栏。

导航栏基本上是一个链接列表，因此使用 <ul> 和 <li> 元素是非常合适的：

#### 实例

```
<ul>
<li><a href="default.asp">Home</a></li>
<li><a href="news.asp">News</a></li>
<li><a href="contact.asp">Contact</a></li>
<li><a href="about.asp">About</a></li>
</ul>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css_navbar_basic_html)

现在，让我们从列表中去掉圆点和外边距：

#### 实例

```
ul
{
list-style-type:none;
margin:0;
padding:0;
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css_navbar_basic_css)

#### 例子解释：

- list-style-type:none - 删除圆点。导航栏不需要列表项标记。
- 把外边距和内边距设置为 0 可以去除浏览器的默认设定。

以上例子中的代码是用在垂直、水平导航栏中的标准代码。

### 垂直导航栏

如需构建垂直导航栏，我们只需要定义 <a> 元素的样式，除了上面的代码之外：

#### 实例

```
a{
display:block;
width:60px;
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css_navbar_vertical)

#### 例子解释：

- display:block - 把链接显示为块元素可使整个链接区域可点击（不仅仅是文本），同时也允许我们规定宽度。
- width:60px - 块元素默认占用全部可用宽度。我们需要规定 60 像素的宽度。

提示：请同时看一看我们[完整样式的导航栏实例](http://www.w3school.com.cn/tiy/t.asp?f=css_navbar_vertical_advanced)。

注释：请始终规定垂直导航栏中 <a> 元素的宽度。如果省略宽度，IE6 会产生意想不到的结果。

### 水平导航栏

有两种创建水平导航栏的方法。使用行内或浮动列表项。

两种方法都不错，但是如果您希望链接拥有相同的尺寸，就必须使用浮动方法。

### 行内列表项

除了上面的“标准”代码，构建水平导航栏的方法之一是将 <li> 元素规定为行内元素：

#### 实例

```
li{
display:inline;
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css_navbar_horizontal)

#### 例子解释：

display:inline; - 默认地，<li> 元素是块元素。在这里，我们去除了每个列表项前后的换行，以便让它们在一行中显示。

提示：请看一下我们[完整样式的水平导航栏实例](http://www.w3school.com.cn/tiy/t.asp?f=css_navbar_horizontal_advanced)。

### 对列表项进行浮动

在上面的例子中，链接的宽度是不同的。

为了让所有链接拥有相等的宽度，浮动 <li> 元素并规定 <a> 元素的宽度：

#### 实例

```
li{
float:left;
}
a{
display:block;
width:60px;
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css_navbar_horizontal_float)

#### 例子解释：

- float:left - 使用 float 来把块元素滑向彼此。
- display:block - 把链接显示为块元素可使整个链接区域可点击（不仅仅是文本），同时也允许我们规定宽度。
- width:60px - 由于块元素默认占用全部可用宽度，链接无法滑动至彼此相邻。我们需要规定 60 像素的宽度。

提示：请看一下我们[完整样式的水平导航栏实例](http://www.w3school.com.cn/tiy/t.asp?f=css_navbar_horizontal_float_advanced)。

## CSS 图片库

CSS 可用来创建图片库。

#### 演示：CSS 图片库

图片库

下面的图片库是由 CSS 创建的：

**实例**

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css_image_gallery)

## CSS 图像透明度



通过 CSS 创建透明图像是很容易的。

注释：CSS opacity 属性是 W3C CSS 推荐标准的一部分。

### 亲自试一试 - 实例

- [创建透明图像 - Hover 效果](http://www.w3school.com.cn/tiy/t.asp?f=css_image_transparency)

  在本例中，当用户将鼠标指针移动到图片上时，会改变图片的透明度。

- [创建文本在背景图像上的透明框](http://www.w3school.com.cn/tiy/t.asp?f=css_transparency)

  本例创建了一个包围文本的半透明框。

[更多示例](http://www.w3school.com.cn/css/css_image_transparency.asp)

### 相关页面

CSS 参考手册：[CSS3 opacity 属性](http://www.w3school.com.cn/cssref/pr_opacity.asp)

## CSS2 媒介类型

**媒介类型(Media Types)允许你定义以何种媒介来提交文档。文档可以被显示在显示器、纸媒介或者听觉浏览器等等。**

### 媒介类型

某些 CSS 属性仅仅被设计为针对某些媒介。比方说 "voice-family" 属性被设计为针对听觉用户终端。其他的属性可被用于不同的媒介。例如，"font-size" 属性可被用于显示器以及印刷媒介，但是也许会带有不同的值。显示器上面的显示的文档通常会需要比纸媒介文档更大的字号，同时，在显示器上，sans-serif 字体更易阅读，而在纸媒介上，serif 字体更易阅读。

### @media规则

@media 规则使你有能力在相同的样式表中，使用不同的样式规则来针对不同的媒介。

下面这个例子中的样式告知浏览器在显示器上显示 14 像素的 Verdana 字体。但是假如页面需要被打印，将使用 10 个像素的 Times 字体。注意：font-weight 被设置为粗体，不论显示器还是纸媒介：

```
<html>
<head>

<style>
@media screen
{
p.test {font-family:verdana,sans-serif; font-size:14px}
}

@media print
{
p.test {font-family:times,serif; font-size:10px}
}

@media screen,print
{
p.test {font-weight:bold}
}
</style>

</head>

<body>....</body>

</html>
```

### 不同的媒介类型

注释：媒介类型名称对大小写不敏感。

| 媒介类型   | 描述                                                   |
| ---------- | ------------------------------------------------------ |
| all        | 用于所有的媒介设备。                                   |
| aural      | 用于语音和音频合成器。                                 |
| braille    | 用于盲人用点字法触觉回馈设备。                         |
| embossed   | 用于分页的盲人用点字法打印机。                         |
| handheld   | 用于小的手持的设备。                                   |
| print      | 用于打印机。                                           |
| projection | 用于方案展示，比如幻灯片。                             |
| screen     | 用于电脑显示器。                                       |
| tty        | 用于使用固定密度字母栅格的媒介，比如电传打字机和终端。 |
| tv         | 用于电视机类型的设备。                                 |

# CSS 实例

- [CSS 总结](http://www.w3school.com.cn/css/css_summary.asp)
- [CSS 测验](http://www.w3school.com.cn/css/css_quiz.asp)

提示：以下例子中的 CSS 代码均位于 HTML 的 head 部分，这样做的目的是为了利于演示例子本身。在实际的开发中，使用 CSS 最好的方式是引用外部样式表。

## CSS 背景实例：

- [设置背景颜色](http://www.w3school.com.cn/tiy/t.asp?f=csse_background-color)

  本例演示如何为元素设置背景颜色。

- [设置文本的背景颜色](http://www.w3school.com.cn/tiy/t.asp?f=csse_text_background)

  本例颜色如何设置部分文本的背景颜色。

- [将图像设置为背景](http://www.w3school.com.cn/tiy/t.asp?f=csse_background-image)

  本例演示如何将图像设置为背景。

- [如何重复背景图像](http://www.w3school.com.cn/tiy/t.asp?f=csse_background-repeat)

  本例演示如何重复背景图像。

- [如何在垂直方向重复背景图像](http://www.w3school.com.cn/tiy/t.asp?f=csse_background-repeaty)

  本例演示如何垂直地重复背景图像。

- [如何在水平方向重复背景图像](http://www.w3school.com.cn/tiy/t.asp?f=csse_background-repeatx)

  本例演示如何水平地重复背景图像。

- [如何仅显示一次背景图像](http://www.w3school.com.cn/tiy/t.asp?f=csse_background-repeat_no-repeat)

  本例演示如何仅显示一次背景图像。

- [如何放置背景图像](http://www.w3school.com.cn/tiy/t.asp?f=csse_background-position)

  本例演示如何在页面上放置背景图像。

- [如何使用%来定位背景图像](http://www.w3school.com.cn/tiy/t.asp?f=csse_background-position_percent)

  本例演示如何使用百分比来在页面上定位背景图像。

- [如何使用像素来定位背景图像](http://www.w3school.com.cn/tiy/t.asp?f=csse_background-position_pixel)

  本例演示如何使用像素来在页面上定位背景图像。

- [如何设置固定的背景图像](http://www.w3school.com.cn/tiy/t.asp?f=csse_background-attachment)

  本例演示如何设置固定的背景图像。图像不会随着页面的其他部分滚动。

- [所有背景属性在一个声明之中](http://www.w3school.com.cn/tiy/t.asp?f=csse_background)

  本例演示如何使用简写属性来将所有背景属性设置在一个声明之中。

*例子解释*

## CSS 文本实例：

- [设置文本颜色](http://www.w3school.com.cn/tiy/t.asp?f=csse_color)

  本例演示如何设置文本的颜色。

- [设置文本的背景颜色](http://www.w3school.com.cn/tiy/t.asp?f=csse_text_background)

  本例颜色如何设置部分文本的背景颜色。

- [规定字符间距](http://www.w3school.com.cn/tiy/t.asp?f=csse_letter-spacing)

  本例演示如何增加或减少字符间距。

- [使用百分比设置行间距](http://www.w3school.com.cn/tiy/t.asp?f=csse_dim_line-height_percent)

  本例演示如何使用百分比值来设置段落中的行间距。

- [使用像素值设置行间距](http://www.w3school.com.cn/tiy/t.asp?f=csse_dim_line-height_pixel)

  本例演示如何使用像素值来设置段落中的行间距。

- [使用数值来设置行间距](http://www.w3school.com.cn/tiy/t.asp?f=csse_dim_line-height_number)

  本例演示如何使用一个数值来设置段落中的行间距。

- [对齐文本](http://www.w3school.com.cn/tiy/t.asp?f=csse_text-align)

  本例演示如何对齐文本。

- [修饰文本](http://www.w3school.com.cn/tiy/t.asp?f=csse_text-decoration)

  本例演示如何向文本添加修饰。

- [缩进文本](http://www.w3school.com.cn/tiy/t.asp?f=csse_text-indent)

  本例演示如何缩进文本首行。

- [控制文本中的字母](http://www.w3school.com.cn/tiy/t.asp?f=csse_text-transform)

  本例演示如何控制文本中的字母。

- [在元素中禁止文本折行](http://www.w3school.com.cn/tiy/t.asp?f=csse_text_white-space)

  本例演示如何禁止在元素中的文本折行。

- [增加单词间距](http://www.w3school.com.cn/tiy/t.asp?f=csse_text_word-spacing)

  本例演示如何增加段落中单词间的距离。

*例子解释*

## CSS 字体(font)实例：

- [设置文本的字体](http://www.w3school.com.cn/tiy/t.asp?f=csse_font-family)

  本例演示如何设置文本字体。

- [设置字体尺寸](http://www.w3school.com.cn/tiy/t.asp?f=csse_font-size)

  本例演示如何设置字体尺寸。

- [设置字体风格](http://www.w3school.com.cn/tiy/t.asp?f=csse_font-style)

  本例演示如何设置字体风格。

- [设置字体的异体](http://www.w3school.com.cn/tiy/t.asp?f=csse_font-variant)

  本例演示如何设置字体的异体。

- [设置字体的粗细](http://www.w3school.com.cn/tiy/t.asp?f=csse_font-weight)

  本例演示如何设置字体的粗细。

- [所有字体属性在一个声明之内](http://www.w3school.com.cn/tiy/t.asp?f=csse_font)

  本例演示如何使用简写属性将字体属性设置在一个声明之内。

*例子解释*

## CSS 边框(border)实例：

- [所有边框属性在一个声明之中](http://www.w3school.com.cn/tiy/t.asp?f=csse_border)

  本例演示用简写属性来将所有四个边框属性设置于同一声明中。

- [设置四边框样式](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-style)

  本例演示如何设置四边框样式。

- [设置每一边的不同边框](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-style2)

  本例演示如何在元素的各边设置不同的边框。

- [所有边框宽度属性在一个声明之中](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-width)

  本例演示用简写属性来将所有边框宽度属性设置于同一声明中。

- [设置四个边框的颜色](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-color)

  本例演示如何设置四个边框的颜色。可以设置一到四个颜色。

- [所有下边框属性在一个声明中](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-bottom)

  本例演示用简写属性来将所有下边框属性设置在同一声明中。

- [设置下边框的颜色](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-bottom-color)

  本例演示如何设置下边框的颜色。

- [设置下边框的样式](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-bottom-style)

  本例演示如何设置下边框的样式。

- [设置下边框的宽度](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-bottom-width)

  本例演示如何设置下边框的宽度。

- [所有左边框属性在一个声明之中](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-left)

  所有左边框属性在一个声明之中

- [设置左边框的颜色](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-left-color)

  本例演示如何设置左边框的颜色。

- [设置左边框的样式](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-left-style)

  本例演示如何设置左边框的样式。

- [设置左边框的宽度](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-left-width)

  本例演示如何设置左边框的宽度。

- [所有右边框属性在一个声明之中](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-right)

  本例演示一个简写属性，用于把所有右边框属性设置在一条声明中。

- [设置右边框的颜色](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-right-color)

  本例演示如何设置右边框的颜色。

- [设置右边框的样式](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-right-style)

  本例演示如何设置右边框的样式。

- [设置右边框的宽度](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-right-width)

  本例演示如何设置右边框的宽度。

- [所有上边框属性在一个声明之中](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-top)

  本例演示用简写属性来将所有上边框属性设置于同一声明之中。

- [设置上边框的颜色](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-top-color)

  本例演示如何设置上边框的颜色。

- [设置上边框的样式](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-top-style)

  本例演示如何设置上边框的样式。

- [设置上边框的宽度](http://www.w3school.com.cn/tiy/t.asp?f=csse_border-top-width)

  本例演示如何设置上边框的宽度。

*例子解释*

## CSS 外边距 (margin) 实例：

- [设置文本的左外边距](http://www.w3school.com.cn/tiy/t.asp?f=csse_margin-left)

  本例演示如何设置文本的左外边距。

- [设置文本的右外边距](http://www.w3school.com.cn/tiy/t.asp?f=csse_margin-right)

  本例演示如何设置文本的右外边距。

- [设置文本的上外边距](http://www.w3school.com.cn/tiy/t.asp?f=csse_margin-top)

  本例演示如何设置文本的上外边距。

- [设置文本的下外边距](http://www.w3school.com.cn/tiy/t.asp?f=csse_margin-bottom)

  本例演示如何设置文本的下外边距。

- [所有的外边距属性在一个声明中。](http://www.w3school.com.cn/tiy/t.asp?f=csse_margin)

  本例演示如何将所有的外边距属性设置于一个声明中。

*例子解释*

## CSS 内边距 (padding) 实例：

- [所有填充属性在一个声明中](http://www.w3school.com.cn/tiy/t.asp?f=csse_padding)

  本例演示使用简写属性将所有的填充属性设置于一个声明中，可以有一到四个值。

- [设置下内边距 1](http://www.w3school.com.cn/tiy/t.asp?f=csse_padding-bottom)

  本例演示如何使用厘米值来设置单元格的下内边距。

- [设置下内边距 2](http://www.w3school.com.cn/tiy/t.asp?f=csse_padding-bottom_percent)

  本例演示如何使用百分比值来设置单元格的下内边距。

- [设置左内边距 1](http://www.w3school.com.cn/tiy/t.asp?f=csse_padding-left)

  本例演示如何使用厘米值来设置单元格的左内边距。

- [设置左内边距 2](http://www.w3school.com.cn/tiy/t.asp?f=csse_padding-left_percent)

  本例演示如何使用百分比值来设置单元格的左内边距。

- [设置右内边距 1](http://www.w3school.com.cn/tiy/t.asp?f=csse_padding-right)

  本例演示如何使用厘米值来设置单元格的右内边距。

- [设置右内边距 2](http://www.w3school.com.cn/tiy/t.asp?f=csse_padding-right_percent)

  本例演示如何使用百分比值来设置单元格的右内边距。

- [设置上内边距 1](http://www.w3school.com.cn/tiy/t.asp?f=csse_padding-top)

  本例演示如何使用厘米值来设置单元格的上内边距。

- [设置上内边距 2](http://www.w3school.com.cn/tiy/t.asp?f=csse_padding-top_percent)

  本例演示如何使用百分比值来设置单元格的上内边距。

*例子解释*

## CSS 列表实例：

- [在无序列表中的不同类型的列表标记](http://www.w3school.com.cn/tiy/t.asp?f=csse_list-style-type)

  本例演示在CSS中不同类型的列表项标记。

- [在有序列表中不同类型的列表项标记](http://www.w3school.com.cn/tiy/t.asp?f=csse_list-style-type2)

  本例演示在CSS中不同类型的列表项标记。

- [所有的列表样式类型](http://www.w3school.com.cn/tiy/t.asp?f=csse_list-style-type_all)

  本例演示在CSS中所有不同类型的列表项标记。

- [将图像作为列表项标记](http://www.w3school.com.cn/tiy/t.asp?f=csse_list-style-image)

  本例演示如何将图像作为列表项标记。

- [放置列表标记](http://www.w3school.com.cn/tiy/t.asp?f=csse_list-style-position)

  本例演示在何处放置列表标记。

- [在一个声明中定义所有的列表属性](http://www.w3school.com.cn/tiy/t.asp?f=csse_list-style)

  本例演示将所有针对列表的属性设置于一个简写属性。

*例子解释*

## CSS 表格实例：

- [设置表格的布局](http://www.w3school.com.cn/tiy/t.asp?f=csse_table_table-layout)

  本例演示如何设置表格的布局。

- [显示表格中的空单元](http://www.w3school.com.cn/tiy/t.asp?f=csse_table_empty-cells)

  本例演示是否显示表格中的空单元。（请在非 IE 浏览器中浏览）

- [合并表格边框](http://www.w3school.com.cn/tiy/t.asp?f=csse_table_border-collapse)

  本例演示是否把表格边框显示为一条单独的边框，还是像标准的 HTML 中那样分开显示。

- [设置表格边框之间的空白](http://www.w3school.com.cn/tiy/t.asp?f=csse_table_border-spacing)

  本例演示如何设置单元格边框之间的距离。（请在非 IE 浏览器中浏览）

- [设置表格标题的位置](http://www.w3school.com.cn/tiy/t.asp?f=csse_table_caption-side)

  本例演示如何定位表格的标题。（请在非 IE 浏览器中浏览）

*例子解释*

## 轮廓（Outline） 实例：

- [在元素周围画线](http://www.w3school.com.cn/tiy/t.asp?f=csse_outline)

  本例演示使用outline属性在元素周围画一条线。

- [设置轮廓的颜色](http://www.w3school.com.cn/tiy/t.asp?f=csse_outline-color)

  本例演示如何设置轮廓的颜色。

- [设置轮廓的样式](http://www.w3school.com.cn/tiy/t.asp?f=csse_outline-style)

  本例演示如何设置轮廓的样式。

- [设置轮廓的宽度](http://www.w3school.com.cn/tiy/t.asp?f=csse_outline-width)

  本例演示如何设置轮廓的宽度。

## CSS 尺寸 (Dimension) 实例：

- [使用像素值设置图像的高度](http://www.w3school.com.cn/tiy/t.asp?f=csse_dim_height)

  本例演示如何使用像素值设置元素的高度。

- [使用百分比设置图像的高度](http://www.w3school.com.cn/tiy/t.asp?f=csse_dim_height_percent)

  本例演示如何使用百分比值来设置元素的高度。

- [使用像素值来设置元素的宽度](http://www.w3school.com.cn/tiy/t.asp?f=csse_dim_width)

  本例演示如何使用像素值来设置元素的宽度。

- [使用百分比来设置元素的宽度](http://www.w3school.com.cn/tiy/t.asp?f=csse_dim_width_percent)

  本例演示如何使用百分比值来设置元素的宽度。

- [设置元素的最大高度](http://www.w3school.com.cn/tiy/t.asp?f=csse_dim_max-height)

  本例演示如何设置一个元素的最大高度。

- [使用像素值来设置元素的最大宽度](http://www.w3school.com.cn/tiy/t.asp?f=csse_dim_max-width)

  本例演示如何使用像素值来设置元素的最大高度。

- [使用百分比来设置元素的最大宽度](http://www.w3school.com.cn/tiy/t.asp?f=csse_dim_max-width_percent)

  本例演示如何使用百分比值来设置元素的最大高度。

- [使用像素值来设置元素的最小高度](http://www.w3school.com.cn/tiy/t.asp?f=csse_dim_min-height)

  本例演示如何使用像素值来设置元素的最小高度。

- [使用像素值来设置元素的最小宽度](http://www.w3school.com.cn/tiy/t.asp?f=csse_dim_min-width)

  本例演示如何使用像素值来设置元素的最小宽度。

- [使用百分比来设置元素的最小宽度](http://www.w3school.com.cn/tiy/t.asp?f=csse_dim_min-width_percent)

  本例演示如何使用百分比值来设置元素的最小宽度。

- [使用百分比设置行间距](http://www.w3school.com.cn/tiy/t.asp?f=csse_dim_line-height_percent)

  本例演示如何使用百分比值来设置段落中的行间距。

- [使用像素值设置行间距](http://www.w3school.com.cn/tiy/t.asp?f=csse_dim_line-height_pixel)

  本例演示如何使用像素值来设置段落中的行间距。

- [使用数值来设置行间距](http://www.w3school.com.cn/tiy/t.asp?f=csse_dim_line-height_number)

  本例演示如何使用一个数值来设置段落中的行间距。

*例子解释*

## CSS 分类 (Classification) 实例：

- [如何把元素显示为内联元素](http://www.w3school.com.cn/tiy/t.asp?f=csse_display)

  本例演示如何把元素显示为内联元素。

- [如何把元素显示为块级元素](http://www.w3school.com.cn/tiy/t.asp?f=csse_display_block)

  本例演示如何把元素显示为块级元素。

- [浮动属性的简单应用](http://www.w3school.com.cn/tiy/t.asp?f=csse_float)

  使图像浮动于一个段落的右侧。

- [将带有边框和边界的图像浮动于段落的右侧](http://www.w3school.com.cn/tiy/t.asp?f=csse_float2)

  使图像浮动于段落的右侧。向图像添加边框和边界。

- [带标题的图像浮动于右侧](http://www.w3school.com.cn/tiy/t.asp?f=csse_float3)

  使带有标题的图像浮动于右侧

- [使段落的首字母浮动于左侧](http://www.w3school.com.cn/tiy/t.asp?f=csse_float4)

  使段落的首字母浮动于左侧，并向这个字母添加样式。

- [创建水平菜单](http://www.w3school.com.cn/tiy/t.asp?f=csse_float5)

  使用具有一栏超链接的浮动来创建水平菜单。

- [创建无表格的首页](http://www.w3school.com.cn/tiy/t.asp?f=csse_float6)

  使用浮动来创建拥有页眉、页脚、左侧目录和主体内容的首页。

- [定位：相对定位](http://www.w3school.com.cn/tiy/t.asp?f=csse_position_relative)

  本例演示如何相对于一个元素的正常位置来对其定位。

- [定位：绝对定位](http://www.w3school.com.cn/tiy/t.asp?f=csse_position_absolute)

  本例演示如何使用绝对值来对元素进行定位。

- [定位：固定定位](http://www.w3school.com.cn/tiy/t.asp?f=csse_position_fixed)

  本例演示如何相对于浏览器窗口来对元素进行定位。

- [如何使元素不可见](http://www.w3school.com.cn/tiy/t.asp?f=csse_visibility)

  本例演示如何使元素不可见。你希望元素被显示出来，还是不呢？

- [把表格元素设置为 collapse（请在非 IE 的浏览器中查看）](http://www.w3school.com.cn/tiy/t.asp?f=csse_visibility_collapse)

  本例演示如何使表格元素叠加？

- [改变光标](http://www.w3school.com.cn/tiy/t.asp?f=csse_cursor)

  本例演示如何改变光标。

- [清除元素的侧面](http://www.w3school.com.cn/tiy/t.asp?f=csse_class-clear)

  本例演示如何使用清除元素侧面的浮动元素。

*例子解释*

## CSS 定位 (Positioning) 实例：

- [定位：相对定位](http://www.w3school.com.cn/tiy/t.asp?f=csse_position_relative)

  本例演示如何相对于一个元素的正常位置来对其定位。

- [定位：绝对定位](http://www.w3school.com.cn/tiy/t.asp?f=csse_position_absolute)

  本例演示如何使用绝对值来对元素进行定位。

- [定位：固定定位](http://www.w3school.com.cn/tiy/t.asp?f=csse_position_fixed)

  本例演示如何相对于浏览器窗口来对元素进行定位。

- [设置元素的形状](http://www.w3school.com.cn/tiy/t.asp?f=csse_clip)

  本例演示如何设置元素的形状。此元素被剪裁到这个形状内，并显示出来。

- [如何使用滚动条来显示元素内溢出的内容](http://www.w3school.com.cn/tiy/t.asp?f=csse_overflow)

  本例演示当元素内容太大而超出规定区域时，如何设置溢出属性来规定相应的动作。

- [如何隐藏溢出元素中溢出的内容](http://www.w3school.com.cn/tiy/t.asp?f=csse_pos_overflow_hidden)

  本例演示在元素中的内容太大以至于无法适应指定的区域时，如何设置 overflow 属性来隐藏其内容。

- [如何设置浏览器来自动地处理溢出](http://www.w3school.com.cn/tiy/t.asp?f=csse_pos_overflow_auto)

  本例演示如何设置浏览器来自动地处理溢出。

- [垂直排列图象](http://www.w3school.com.cn/tiy/t.asp?f=csse_vertical-align)

  本例演示如何在文本中垂直排列图象。

- [Z-index](http://www.w3school.com.cn/tiy/t.asp?f=csse_zindex2)

  Z-index可被用于将在一个元素放置于另一元素之后。

- [Z-index](http://www.w3school.com.cn/tiy/t.asp?f=csse_zindex1)

  上面的例子中的元素已经更改了Z-index。

- [使用固定值设置图像的上边缘](http://www.w3school.com.cn/tiy/t.asp?f=csse_position_top)

  本例演示如何使用固定值设置图像的上边缘。

- [使用百分比设置图像的上边缘](http://www.w3school.com.cn/tiy/t.asp?f=csse_position_top_percent)

  本例演示如何使用百分比值设置图像的上边缘。

- [使用像素值设置图像的底部边缘](http://www.w3school.com.cn/tiy/t.asp?f=csse_position_bottom)

  本例演示如何使用像素值设置图像的底部边缘。

- [使用百分比设置图像的底部边缘](http://www.w3school.com.cn/tiy/t.asp?f=csse_position_bottom_percent)

  本例演示如何使用百分比值设置图像的底部边缘。

- [使用固定值设置图像的左边缘](http://www.w3school.com.cn/tiy/t.asp?f=csse_position_left)

  本例演示如何使用固定值设置图像的左边缘。

- [使用百分比设置图像的左边缘](http://www.w3school.com.cn/tiy/t.asp?f=csse_position_left_percent)

  本例演示如何使用百分比值设置图像的左边缘。

- [使用固定值设置图像的右边缘](http://www.w3school.com.cn/tiy/t.asp?f=csse_position_right)

  本例演示如何使用固定值设置图像的右边缘。

- [使用百分比设置图像的右边缘](http://www.w3school.com.cn/tiy/t.asp?f=csse_position_right_percent)

  本例演示如何使用百分比值设置图像的右边缘。

*例子解释*

## CSS 伪类 (Pseudo-classes)实例：

- [超链接](http://www.w3school.com.cn/tiy/t.asp?f=csse_link)

  本例演示如何向文档中的超链接添加不同的颜色。

- [超链接 2](http://www.w3school.com.cn/tiy/t.asp?f=csse_link2)

  本例演示如何向超链接添加其他样式。

- [超链接：:focus 的使用](http://www.w3school.com.cn/tiy/t.asp?f=csse_link_focus)

  本例演示如何使用 :focus 伪类（无法在 IE 中工作）。

- [:first-child（首个子对象）](http://www.w3school.com.cn/tiy/t.asp?f=csse_first-child)

  本例演示 :first-child 伪类的用法。

- [:lang（语言）](http://www.w3school.com.cn/tiy/t.asp?f=csse_lang)

  本例演示 :lang 伪类的用法。

*例子解释*

## CSS 伪元素 (Pseudo-elements)实例：

- [制作首字母特效](http://www.w3school.com.cn/tiy/t.asp?f=csse_firstletter)

  本例演示如何向文本的首字母添加特效。

- [制作首行特效](http://www.w3school.com.cn/tiy/t.asp?f=csse_firstline)

  本例演示如何向文本的首行添加特效。

*例子解释*

# CSS3新特性

## CSS3 边框

通过 CSS3，您能够创建圆角边框，向矩形添加阴影，使用图片来绘制边框 - 并且不需使用设计软件，比如 PhotoShop。

在本章中，您将学到以下边框属性：

- border-radius
- box-shadow
- border-image

### 浏览器支持

| 属性          | 浏览器支持 |      |      |      |      |
| ------------- | ---------- | ---- | ---- | ---- | ---- |
| border-radius |            |      |      |      |      |
| box-shadow    |            |      |      |      |      |
| border-image  |            |      |      |      |      |

Internet Explorer 9+ 支持 border-radius 和 box-shadow 属性。

Firefox、Chrome 以及 Safari 支持所有新的边框属性。

注释：对于 border-image，Safari 5 以及更老的版本需要前缀 -webkit-。

Opera 支持 border-radius 和 box-shadow 属性，但是对于 border-image 需要前缀 -o-。

### CSS3 圆角边框

在 CSS2 中添加圆角矩形需要技巧。我们必须为每个圆角使用不同的图片。

在 CSS3 中，创建圆角是非常容易的。

在 CSS3 中，border-radius 属性用于创建圆角：

这个矩形有圆角哦！

**实例**

向 div 元素添加圆角：

```
div
{
border:2px solid;
border-radius:25px;
-moz-border-radius:25px; /* Old Firefox */
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_border-radius)

### CSS3 边框阴影

在 CSS3 中，box-shadow 用于向方框添加阴影：

**实例**

向 div 元素添加方框阴影：

```
div
{
box-shadow: 10px 10px 5px #888888;
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_box-shadow)

### CSS3 边框图片

通过 CSS3 的 border-image 属性，您可以使用图片来创建边框：

border-image 属性允许您规定用于边框的图片！

用于创建上面的边框的原始图片：

**实例**

使用图片创建围绕 div 元素的边框：

```
div
{
border-image:url(border.png) 30 30 round;
-moz-border-image:url(border.png) 30 30 round; /* 老的 Firefox */
-webkit-border-image:url(border.png) 30 30 round; /* Safari 和 Chrome */
-o-border-image:url(border.png) 30 30 round; /* Opera */
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_border-image)

### 新的边框属性

| 属性                                                         | 描述                                          | CSS  |
| ------------------------------------------------------------ | --------------------------------------------- | ---- |
| [border-image](http://www.w3school.com.cn/cssref/pr_border-image.asp) | 设置所有 border-image-* 属性的简写属性。      | 3    |
| [border-radius](http://www.w3school.com.cn/cssref/pr_border-radius.asp) | 设置所有四个 border-*-radius 属性的简写属性。 | 3    |
| [box-shadow](http://www.w3school.com.cn/cssref/pr_box-shadow.asp) | 向方框添加一个或多个阴影。                    | 3    |

## CSS3 背景

CSS3 包含多个新的背景属性，它们提供了对背景更强大的控制。

在本章，您将学到以下背景属性：

- background-size
- background-origin

您也将学到如何使用多重背景图片。

### 浏览器支持

| 属性              | 浏览器支持 |      |      |      |      |
| ----------------- | ---------- | ---- | ---- | ---- | ---- |
| background-size   |            |      |      |      |      |
| background-origin |            |      |      |      |      |

Internet Explorer 9+、Firefox、Chrome、Safari 以及 Opera 支持新的背景属性。

### CSS3 background-size 属性

background-size 属性规定背景图片的尺寸。

在 CSS3 之前，背景图片的尺寸是由图片的实际尺寸决定的。在 CSS3 中，可以规定背景图片的尺寸，这就允许我们在不同的环境中重复使用背景图片。

您能够以像素或百分比规定尺寸。如果以百分比规定尺寸，那么尺寸相对于父元素的宽度和高度。

例子 **1**

调整背景图片的大小：

```
div
{
background:url(bg_flower.gif);
-moz-background-size:63px 100px; /* 老版本的 Firefox */
background-size:63px 100px;
background-repeat:no-repeat;
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_background-size)

**例子 2**

对背景图片进行拉伸，使其完成填充内容区域：

```
div
{
background:url(bg_flower.gif);
-moz-background-size:40% 100%; /* 老版本的 Firefox */
background-size:40% 100%;
background-repeat:no-repeat;
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_background-size2)

### CSS3 background-origin 属性

background-origin 属性规定背景图片的定位区域。

背景图片可以放置于 content-box、padding-box 或 border-box 区域。

**实例**

在 content-box 中定位背景图片：

```
div
{
background:url(bg_flower.gif);
background-repeat:no-repeat;
background-size:100% 100%;
-webkit-background-origin:content-box; /* Safari */
background-origin:content-box;
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_background-origin)

### CSS3 多重背景图片

CSS3 允许您为元素使用多个背景图像。

**实例**

为 body 元素设置两幅背景图片：

```
body
{ 
background-image:url(bg_flower.gif),url(bg_flower_2.gif);
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_background_multiple)

### 新的背景属性

| 属性                                                         | 描述                     | CSS  |
| ------------------------------------------------------------ | ------------------------ | ---- |
| [background-clip](http://www.w3school.com.cn/cssref/pr_background-clip.asp) | 规定背景的绘制区域。     | 3    |
| [background-origin](http://www.w3school.com.cn/cssref/pr_background-origin.asp) | 规定背景图片的定位区域。 | 3    |
| [background-size](http://www.w3school.com.cn/cssref/pr_background-size.asp) | 规定背景图片的尺寸。     | 3    |



## CSS3 文本效果



CSS3 包含多个新的文本特性。

在本章中，您将学到如下文本属性：

- text-shadow
- word-wrap

### 浏览器支持

| 属性        | 浏览器支持 |      |      |      |      |
| ----------- | ---------- | ---- | ---- | ---- | ---- |
| text-shadow |            |      |      |      |      |
| word-wrap   |            |      |      |      |      |

Internet Explorer 10、Firefox、Chrome、Safari 以及 Opera 支持 text-shadow 属性。

所有主流浏览器都支持 word-wrap 属性。

注释：Internet Explorer 9 以及更早的版本，不支持 text-shadow 属性。

### CSS3 文本阴影

在 CSS3 中，text-shadow 可向文本应用阴影。



您能够规定水平阴影、垂直阴影、模糊距离，以及阴影的颜色：

**实例**

向标题添加阴影：

```
h1{
text-shadow: 5px 5px 5px #FF0000;
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_text-shadow)

### CSS3 自动换行

单词太长的话就可能无法超出某个区域：

This paragraph contains a very long word: thisisaveryveryveryveryveryverylongword. The long word will break and wrap to the next line.

在 CSS3 中，word-wrap 属性允许您允许文本强制文本进行换行 - 即使这意味着会对单词进行拆分：

This paragraph contains a very long word: thisisaveryveryveryveryveryverylongword. The long word will break and wrap to the next line.

下面是 CSS 代码：

**实例**

允许对长单词进行拆分，并换行到下一行：

```
p {word-wrap:break-word;}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_word-wrap)

### 新的文本属性

| 属性                                                         | 描述                                                    | CSS  |
| ------------------------------------------------------------ | ------------------------------------------------------- | ---- |
| [hanging-punctuation](http://www.w3school.com.cn/cssref/pr_hanging-punctuation.asp) | 规定标点字符是否位于线框之外。                          | 3    |
| [punctuation-trim](http://www.w3school.com.cn/cssref/pr_punctuation-trim.asp) | 规定是否对标点字符进行修剪。                            | 3    |
| text-align-last                                              | 设置如何对齐最后一行或紧挨着强制换行符之前的行。        | 3    |
| [text-emphasis](http://www.w3school.com.cn/cssref/pr_text-emphasis.asp) | 向元素的文本应用重点标记以及重点标记的前景色。          | 3    |
| [text-justify](http://www.w3school.com.cn/cssref/pr_text-justify.asp) | 规定当 text-align 设置为 "justify" 时所使用的对齐方法。 | 3    |
| [text-outline](http://www.w3school.com.cn/cssref/pr_text-outline.asp) | 规定文本的轮廓。                                        | 3    |
| [text-overflow](http://www.w3school.com.cn/cssref/pr_text-overflow.asp) | 规定当文本溢出包含元素时发生的事情。                    | 3    |
| [text-shadow](http://www.w3school.com.cn/cssref/pr_text-shadow.asp) | 向文本添加阴影。                                        | 3    |
| [text-wrap](http://www.w3school.com.cn/cssref/pr_text-wrap.asp) | 规定文本的换行规则。                                    | 3    |
| [word-break](http://www.w3school.com.cn/cssref/pr_word-break.asp) | 规定非中日韩文本的换行规则。                            | 3    |
| [word-wrap](http://www.w3school.com.cn/cssref/pr_word-wrap.asp) | 允许对长的不可分割的单词进行分割并换行到下一行。        | 3    |

## CSS3 字体



![通过 CSS3，Web 设计师再也不必被迫使用“web-safe”字体了。](http://www.w3school.com.cn/i/css3_font.gif)

### CSS3 @font-face 规则

在 CSS3 之前，web 设计师必须使用已在用户计算机上安装好的字体。

通过 CSS3，web 设计师可以使用他们喜欢的任意字体。

当您您找到或购买到希望使用的字体时，可将该字体文件存放到 web 服务器上，它会在需要时被自动下载到用户的计算机上。

您“自己的”的字体是在 CSS3 @font-face 规则中定义的。

### 浏览器支持

| 属性       | 浏览器支持 |      |      |      |      |
| ---------- | ---------- | ---- | ---- | ---- | ---- |
| @font-face |            |      |      |      |      |

Firefox、Chrome、Safari 以及 Opera 支持 .ttf (True Type Fonts) 和 .otf (OpenType Fonts) 类型的字体。

Internet Explorer 9+ 支持新的 @font-face 规则，但是仅支持 .eot 类型的字体 (Embedded OpenType)。

注释：Internet Explorer 8 以及更早的版本不支持新的 @font-face 规则。

### 使用您需要的字体

在新的 @font-face 规则中，您必须首先定义字体的名称（比如 myFirstFont），然后指向该字体文件。

如需为 HTML 元素使用字体，请通过 font-family 属性来引用字体的名称 (myFirstFont)：

**实例**

```
<style> 
@font-face
{
font-family: myFirstFont;
src: url('Sansation_Light.ttf'),
     url('Sansation_Light.eot'); /* IE9+ */
}

div
{
font-family:myFirstFont;
}
</style>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_font-face_rule)

### 使用粗体字体

您必须为粗体文本添加另一个包含描述符的 @font-face：

**实例**

```
@font-face
{
font-family: myFirstFont;
src: url('Sansation_Bold.ttf'),
     url('Sansation_Bold.eot'); /* IE9+ */
font-weight:bold;
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_font-face_rule_bold)

文件 "Sansation_Bold.ttf" 是另一个字体文件，它包含了 Sansation 字体的粗体字符。

只要 font-family 为 "myFirstFont" 的文本需要显示为粗体，浏览器就会使用该字体。

通过这种方式，我们可以为相同的字体设置许多 @font-face 规则。

### CSS3 字体描述符

下面的表格列出了能够在 @font-face 规则中定义的所有字体描述符：

| 描述符        | 值                                                           | 描述                                                         |
| ------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| font-family   | *name*                                                       | 必需。规定字体的名称。                                       |
| src           | *URL*                                                        | 必需。定义字体文件的 URL。                                   |
| font-stretch  | normalcondensedultra-condensedextra-condensedsemi-condensedexpandedsemi-expandedextra-expandedultra-expanded | 可选。定义如何拉伸字体。默认是 "normal"。                    |
| font-style    | ormalitalicoblique                                           | 可选。定义字体的样式。默认是 "normal"。                      |
| font-weight   | normalbold100200300400500600700800900                        | 可选。定义字体的粗细。默认是 "normal"。                      |
| unicode-range | *unicode-range*                                              | 可选。定义字体支持的 UNICODE 字符范围。默认是 "U+0-10FFFF"。 |

## CSS3 2D 转换

### CSS3 转换

通过 CSS3 转换，我们能够对元素进行移动、缩放、转动、拉长或拉伸。

### 它如何工作？

转换是使元素改变形状、尺寸和位置的一种效果。

您可以使用 2D 或 3D 转换来转换您的元素。

**浏览器支持**

| 属性      | 浏览器支持 |      |      |      |      |
| --------- | ---------- | ---- | ---- | ---- | ---- |
| transform |            |      |      |      |      |

Internet Explorer 10、Firefox 以及 Opera 支持 transform 属性。

Chrome 和 Safari 需要前缀 -webkit-。

注释：Internet Explorer 9 需要前缀 -ms-。

### 2D 转换

在本章中，您将学到如下 2D 转换方法：

- translate()
- rotate()
- scale()
- skew()
- matrix()

您将在下一章学习 3D 转换。

**实例**

```
div{
transform: rotate(30deg);
-ms-transform: rotate(30deg);		/* IE 9 */
-webkit-transform: rotate(30deg);	/* Safari and Chrome */
-o-transform: rotate(30deg);		/* Opera */
-moz-transform: rotate(30deg);		/* Firefox */
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_transform)

以左下角为原点,旋转30度

### translate() 方法

通过 translate() 方法，元素从其当前位置移动，根据给定的 left（x 坐标） 和 top（y 坐标） 位置参数：

**实例**

```
div{
transform: translate(50px,100px);
-ms-transform: translate(50px,100px);		/* IE 9 */
-webkit-transform: translate(50px,100px);	/* Safari and Chrome */
-o-transform: translate(50px,100px);		/* Opera */
-moz-transform: translate(50px,100px);		/* Firefox */
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_transform_translate)

值 translate(50px,100px) 把元素从左侧平行移动 50 像素，从顶端平行移动 100 像素。

### rotate() 方法

通过 rotate() 方法，元素顺时针旋转给定的角度。允许负值，元素将逆时针旋转。

**实例**

```
div{
transform: rotate(30deg);
-ms-transform: rotate(30deg);		/* IE 9 */
-webkit-transform: rotate(30deg);	/* Safari and Chrome */
-o-transform: rotate(30deg);		/* Opera */
-moz-transform: rotate(30deg);		/* Firefox */
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_transform_rotate)

值 rotate(30deg) 把元素顺时针旋转 30 度。

### scale() 方法

通过 scale() 方法，元素的尺寸会增加或减少，根据给定的宽度（X 轴）和高度（Y 轴）参数：

### 实例

```
div
{
transform: scale(2,4);
-ms-transform: scale(2,4);	/* IE 9 */
-webkit-transform: scale(2,4);	/* Safari 和 Chrome */
-o-transform: scale(2,4);	/* Opera */
-moz-transform: scale(2,4);	/* Firefox */
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_transform_scale)

值 scale(2,4) 把宽度转换为原始尺寸的 2 倍，把高度转换为原始高度的 4 倍。

### skew() 方法

通过 skew() 方法，元素翻转给定的角度，根据给定的水平线（X 轴）和垂直线（Y 轴）参数：

**实例**

```
div
{
transform: skew(30deg,20deg);
-ms-transform: skew(30deg,20deg);	/* IE 9 */
-webkit-transform: skew(30deg,20deg);	/* Safari and Chrome */
-o-transform: skew(30deg,20deg);	/* Opera */
-moz-transform: skew(30deg,20deg);	/* Firefox */
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_transform_skew)

值 skew(30deg,20deg) 围绕 X 轴把元素翻转 30 度，围绕 Y 轴翻转 20 度。

### matrix() 方法

matrix() 方法把所有 2D 转换方法组合在一起。

matrix() 方法需要六个参数，包含数学函数，允许您：旋转、缩放、移动以及倾斜元素。

**实例**

如何使用 matrix 方法将 div 元素旋转 30 度：

```
div
{
transform:matrix(0.866,0.5,-0.5,0.866,0,0);
-ms-transform:matrix(0.866,0.5,-0.5,0.866,0,0);		/* IE 9 */
-moz-transform:matrix(0.866,0.5,-0.5,0.866,0,0);	/* Firefox */
-webkit-transform:matrix(0.866,0.5,-0.5,0.866,0,0);	/* Safari and Chrome */
-o-transform:matrix(0.866,0.5,-0.5,0.866,0,0);		/* Opera */
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_transform_matrix)

### 新的转换属性

下面的表格列出了所有的转换属性：

| 属性                                                         | 描述                         | CSS  |
| ------------------------------------------------------------ | ---------------------------- | ---- |
| [transform](http://www.w3school.com.cn/cssref/pr_transform.asp) | 向元素应用 2D 或 3D 转换。   | 3    |
| [transform-origin](http://www.w3school.com.cn/cssref/pr_transform-origin.asp) | 允许你改变被转换元素的位置。 | 3    |

### 2D Transform 方法

| 函数                            | 描述                                     |
| ------------------------------- | ---------------------------------------- |
| matrix(*n*,*n*,*n*,*n*,*n*,*n*) | 定义 2D 转换，使用六个值的矩阵。         |
| translate(*x*,*y*)              | 定义 2D 转换，沿着 X 和 Y 轴移动元素。   |
| translateX(*n*)                 | 定义 2D 转换，沿着 X 轴移动元素。        |
| translateY(*n*)                 | 定义 2D 转换，沿着 Y 轴移动元素。        |
| scale(*x*,*y*)                  | 定义 2D 缩放转换，改变元素的宽度和高度。 |
| scaleX(*n*)                     | 定义 2D 缩放转换，改变元素的宽度。       |
| scaleY(*n*)                     | 定义 2D 缩放转换，改变元素的高度。       |
| rotate(*angle*)                 | 定义 2D 旋转，在参数中规定角度。         |
| skew(*x-angle*,*y-angle*)       | 定义 2D 倾斜转换，沿着 X 和 Y 轴。       |
| skewX(*angle*)                  | 定义 2D 倾斜转换，沿着 X 轴。            |
| skewY(*angle*)                  | 定义 2D 倾斜转换，沿着 Y 轴。            |

## CSS3 3D 转换

### 3D 转换

CSS3 允许您使用 3D 转换来对元素进行格式化。

在本章中，您将学到其中的一些 3D 转换方法：

- rotateX()
- rotateY()

点击下面的元素，来查看 2D 转换与 3D 转换之间的不同之处：

2D 旋转

3D 旋转

### 它如何工作？

转换是使元素改变形状、尺寸和位置的一种效果。

您可以使用 2D 或 3D 转换来转换您的元素。

### 浏览器支持

| 属性      | 浏览器支持 |      |      |      |      |
| --------- | ---------- | ---- | ---- | ---- | ---- |
| transform |            |      |      |      |      |

Internet Explorer 10 和 Firefox 支持 3D 转换。

Chrome 和 Safari 需要前缀 -webkit-。

Opera 仍然不支持 3D 转换（它只支持 [2D 转换](http://www.w3school.com.cn/css3/css3_2dtransform.asp)）。

### rotateX() 方法

通过 rotateX() 方法，元素围绕其 X 轴以给定的度数进行旋转。

**实例**

```
div{
transform: rotateX(120deg);
-webkit-transform: rotateX(120deg);	/* Safari 和 Chrome */
-moz-transform: rotateX(120deg);	/* Firefox */
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_transform_rotateX)

### rotateY() 旋转

通过 rotateY() 方法，元素围绕其 Y 轴以给定的度数进行旋转。

**实例**

```
div{
transform: rotateY(130deg);
-webkit-transform: rotateY(130deg);	/* Safari 和 Chrome */
-moz-transform: rotateY(130deg);	/* Firefox */
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_transform_rotateY)

### 转换属性

下面的表格列出了所有的转换属性：

| 属性                                                         | 描述                                 | CSS  |
| ------------------------------------------------------------ | ------------------------------------ | ---- |
| [transform](http://www.w3school.com.cn/cssref/pr_transform.asp) | 向元素应用 2D 或 3D 转换。           | 3    |
| [transform-origin](http://www.w3school.com.cn/cssref/pr_transform-origin.asp) | 允许你改变被转换元素的位置。         | 3    |
| [transform-style](http://www.w3school.com.cn/cssref/pr_transform-style.asp) | 规定被嵌套元素如何在 3D 空间中显示。 | 3    |
| [perspective](http://www.w3school.com.cn/cssref/pr_perspective.asp) | 规定 3D 元素的透视效果。             | 3    |
| [perspective-origin](http://www.w3school.com.cn/cssref/pr_perspective-origin.asp) | 规定 3D 元素的底部位置。             | 3    |
| [backface-visibility](http://www.w3school.com.cn/cssref/pr_backface-visibility.asp) | 定义元素在不面对屏幕时是否可见。     | 3    |

### 2D Transform 方法

| 函数                                                         | 描述                                      |
| ------------------------------------------------------------ | ----------------------------------------- |
| matrix3d(*n*,*n*,*n*,*n*,*n*,*n*, *n*,*n*,*n*,*n*,*n*,*n*,*n*,*n*,*n*,*n*) | 定义 3D 转换，使用 16 个值的 4x4 矩阵。   |
| translate3d(*x*,*y*,*z*)                                     | 定义 3D 转化。                            |
| translateX(*x*)                                              | 定义 3D 转化，仅使用用于 X 轴的值。       |
| translateY(*y*)                                              | 定义 3D 转化，仅使用用于 Y 轴的值。       |
| translateZ(*z*)                                              | 定义 3D 转化，仅使用用于 Z 轴的值。       |
| scale3d(*x*,*y*,*z*)                                         | 定义 3D 缩放转换。                        |
| scaleX(*x*)                                                  | 定义 3D 缩放转换，通过给定一个 X 轴的值。 |
| scaleY(*y*)                                                  | 定义 3D 缩放转换，通过给定一个 Y 轴的值。 |
| scaleZ(*z*)                                                  | 定义 3D 缩放转换，通过给定一个 Z 轴的值。 |
| rotate3d(*x*,*y*,*z*,*angle*)                                | 定义 3D 旋转。                            |
| rotateX(*angle*)                                             | 定义沿 X 轴的 3D 旋转。                   |
| rotateY(*angle*)                                             | 定义沿 Y 轴的 3D 旋转。                   |
| rotateZ(*angle*)                                             | 定义沿 Z 轴的 3D 旋转。                   |
| perspective(*n*)                                             | 定义 3D 转换元素的透视视图。              |

## CSS3 过渡

通过 CSS3，我们可以在不使用 Flash 动画或 JavaScript 的情况下，当元素从一种样式变换为另一种样式时为元素添加效果。

### 浏览器支持

| 属性       | 浏览器支持 |      |      |      |      |
| ---------- | ---------- | ---- | ---- | ---- | ---- |
| transition |            |      |      |      |      |

Internet Explorer 10、Firefox、Chrome 以及 Opera 支持 transition 属性。

Safari 需要前缀 -webkit-。

注释：Internet Explorer 9 以及更早的版本，不支持 transition 属性。

注释：Chrome 25 以及更早的版本，需要前缀 -webkit-。

### 它如何工作？

CSS3 过渡是元素从一种样式逐渐改变为另一种的效果。

要实现这一点，必须规定两项内容：

- 规定您希望把效果添加到哪个 CSS 属性上
- 规定效果的时长

**实例**

应用于宽度属性的过渡效果，时长为 2 秒：

```
div
{
transition: width 2s;
-moz-transition: width 2s;	/* Firefox 4 */
-webkit-transition: width 2s;	/* Safari 和 Chrome */
-o-transition: width 2s;	/* Opera */
}
```

注释：如果时长未规定，则不会有过渡效果，因为默认值是 0。

效果开始于指定的 CSS 属性改变值时。CSS 属性改变的典型时间是鼠标指针位于元素上时：

**实例**

规定当鼠标指针悬浮于 <div> 元素上时：

```
div:hover{
width:300px;
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_transition1)

注释：当指针移出元素时，它会逐渐变回原来的样式。

### 多项改变

如需向多个样式添加过渡效果，请添加多个属性，由逗号隔开：

**实例**

向宽度、高度和转换添加过渡效果：

```
div{
width:100px;
height:100px;
background:yellow;
transition:width 2s, height 2s;
-moz-transition:width 2s, height 2s, -moz-transform 2s; /* Firefox 4 */
-webkit-transition:width 2s, height 2s, -webkit-transform 2s; /* Safari and Chrome */
-o-transition:width 2s, height 2s, -o-transform 2s; /* Opera */
}
div{
transition: width 2s, height 2s, transform 2s;
-moz-transition: width 2s, height 2s, -moz-transform 2s;
-webkit-transition: width 2s, height 2s, -webkit-transform 2s;
-o-transition: width 2s, height 2s,-o-transform 2s;
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_transition2)

### 过渡属性

下面的表格列出了所有的转换属性：

| 属性                                                         | 描述                                         | CSS  |
| ------------------------------------------------------------ | -------------------------------------------- | ---- |
| [transition](http://www.w3school.com.cn/cssref/pr_transition.asp) | 简写属性，用于在一个属性中设置四个过渡属性。 | 3    |
| [transition-property](http://www.w3school.com.cn/cssref/pr_transition-property.asp) | 规定应用过渡的 CSS 属性的名称。              | 3    |
| [transition-duration](http://www.w3school.com.cn/cssref/pr_transition-duration.asp) | 定义过渡效果花费的时间。默认是 0。           | 3    |
| [transition-timing-function](http://www.w3school.com.cn/cssref/pr_transition-timing-function.asp) | 规定过渡效果的时间曲线。默认是 "ease"。      | 3    |
| [transition-delay](http://www.w3school.com.cn/cssref/pr_transition-delay.asp) | 规定过渡效果何时开始。默认是 0。             | 3    |

下面的两个例子设置所有过渡属性：

**实例**

在一个例子中使用所有过渡属性：

```
div
{
transition-property: width;
transition-duration: 1s;
transition-timing-function: linear;
transition-delay: 2s;
/* Firefox 4 */
-moz-transition-property:width;
-moz-transition-duration:1s;
-moz-transition-timing-function:linear;
-moz-transition-delay:2s;
/* Safari 和 Chrome */
-webkit-transition-property:width;
-webkit-transition-duration:1s;
-webkit-transition-timing-function:linear;
-webkit-transition-delay:2s;
/* Opera */
-o-transition-property:width;
-o-transition-duration:1s;
-o-transition-timing-function:linear;
-o-transition-delay:2s;
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_transition3)

**实例**

与上面的例子相同的过渡效果，但是使用了简写的 transition 属性：

```
div
{
transition: width 1s linear 2s;
/* Firefox 4 */
-moz-transition:width 1s linear 2s;
/* Safari and Chrome */
-webkit-transition:width 1s linear 2s;
/* Opera */
-o-transition:width 1s linear 2s;
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_transition4)


  CSS3 动画

- [CSS3 过渡](http://www.w3school.com.cn/css3/css3_transition.asp)
- [CSS3 多列](http://www.w3school.com.cn/css3/css3_multiple_columns.asp)

## CSS3 动画

通过 CSS3，我们能够创建动画，这可以在许多网页中取代动画图片、Flash 动画以及 JavaScript。

CSS3 动画

### CSS3 @keyframes 规则

如需在 CSS3 中创建动画，您需要学习 @keyframes 规则。

@keyframes 规则用于创建动画。在 @keyframes 中规定某项 CSS 样式，就能创建由当前样式逐渐改为新样式的动画效果。

### 浏览器支持

| 属性       | 浏览器支持 |      |      |      |      |
| ---------- | ---------- | ---- | ---- | ---- | ---- |
| @keyframes |            |      |      |      |      |
| animation  |            |      |      |      |      |

Internet Explorer 10、Firefox 以及 Opera 支持 @keyframes 规则和 animation 属性。

Chrome 和 Safari 需要前缀 -webkit-。

注释：Internet Explorer 9，以及更早的版本，不支持 @keyframe 规则或 animation 属性。

**实例**

```
@keyframes myfirst
{
from {background: red;}
to {background: yellow;}
}

@-moz-keyframes myfirst /* Firefox */
{
from {background: red;}
to {background: yellow;}
}

@-webkit-keyframes myfirst /* Safari 和 Chrome */
{
from {background: red;}
to {background: yellow;}
}

@-o-keyframes myfirst /* Opera */
{
from {background: red;}
to {background: yellow;}
}
```

### CSS3 动画

当您在 @keyframes 中创建动画时，请把它捆绑到某个选择器，否则不会产生动画效果。

通过规定至少以下两项 CSS3 动画属性，即可将动画绑定到选择器：

- 规定动画的名称
- 规定动画的时长

**实例**

把 "myfirst" 动画捆绑到 div 元素，时长：5 秒：

```
div
{
animation: myfirst 5s;
-moz-animation: myfirst 5s;	/* Firefox */
-webkit-animation: myfirst 5s;	/* Safari 和 Chrome */
-o-animation: myfirst 5s;	/* Opera */
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_animation1)

注释：您必须定义动画的名称和时长。如果忽略时长，则动画不会允许，因为默认值是 0。

### 什么是 CSS3 中的动画？

动画是使元素从一种样式逐渐变化为另一种样式的效果。

您可以改变任意多的样式任意多的次数。

请用百分比来规定变化发生的时间，或用关键词 "from" 和 "to"，等同于 0% 和 100%。

0% 是动画的开始，100% 是动画的完成。

为了得到最佳的浏览器支持，您应该始终定义 0% 和 100% 选择器。

**实例**

当动画为 25% 及 50% 时改变背景色，然后当动画 100% 完成时再次改变：

```
@keyframes myfirst
{
0%   {background: red;}
25%  {background: yellow;}
50%  {background: blue;}
100% {background: green;}
}

@-moz-keyframes myfirst /* Firefox */
{
0%   {background: red;}
25%  {background: yellow;}
50%  {background: blue;}
100% {background: green;}
}

@-webkit-keyframes myfirst /* Safari 和 Chrome */
{
0%   {background: red;}
25%  {background: yellow;}
50%  {background: blue;}
100% {background: green;}
}

@-o-keyframes myfirst /* Opera */
{
0%   {background: red;}
25%  {background: yellow;}
50%  {background: blue;}
100% {background: green;}
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_animation2)

**实例**

改变背景色和位置：

```
@keyframes myfirst
{
0%   {background: red; left:0px; top:0px;}
25%  {background: yellow; left:200px; top:0px;}
50%  {background: blue; left:200px; top:200px;}
75%  {background: green; left:0px; top:200px;}
100% {background: red; left:0px; top:0px;}
}

@-moz-keyframes myfirst /* Firefox */
{
0%   {background: red; left:0px; top:0px;}
25%  {background: yellow; left:200px; top:0px;}
50%  {background: blue; left:200px; top:200px;}
75%  {background: green; left:0px; top:200px;}
100% {background: red; left:0px; top:0px;}
}

@-webkit-keyframes myfirst /* Safari 和 Chrome */
{
0%   {background: red; left:0px; top:0px;}
25%  {background: yellow; left:200px; top:0px;}
50%  {background: blue; left:200px; top:200px;}
75%  {background: green; left:0px; top:200px;}
100% {background: red; left:0px; top:0px;}
}

@-o-keyframes myfirst /* Opera */
{
0%   {background: red; left:0px; top:0px;}
25%  {background: yellow; left:200px; top:0px;}
50%  {background: blue; left:200px; top:200px;}
75%  {background: green; left:0px; top:200px;}
100% {background: red; left:0px; top:0px;}
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_animation3)

### CSS3 动画属性

下面的表格列出了 @keyframes 规则和所有动画属性：

| 属性                                                         | 描述                                                     | CSS  |
| ------------------------------------------------------------ | -------------------------------------------------------- | ---- |
| [@keyframes](http://www.w3school.com.cn/cssref/pr_keyframes.asp) | 规定动画。                                               | 3    |
| [animation](http://www.w3school.com.cn/cssref/pr_animation.asp) | 所有动画属性的简写属性，除了 animation-play-state 属性。 | 3    |
| [animation-name](http://www.w3school.com.cn/cssref/pr_animation-name.asp) | 规定 @keyframes 动画的名称。                             | 3    |
| [animation-duration](http://www.w3school.com.cn/cssref/pr_animation-duration.asp) | 规定动画完成一个周期所花费的秒或毫秒。默认是 0。         | 3    |
| [animation-timing-function](http://www.w3school.com.cn/cssref/pr_animation-timing-function.asp) | 规定动画的速度曲线。默认是 "ease"。                      | 3    |
| [animation-delay](http://www.w3school.com.cn/cssref/pr_animation-delay.asp) | 规定动画何时开始。默认是 0。                             | 3    |
| [animation-iteration-count](http://www.w3school.com.cn/cssref/pr_animation-iteration-count.asp) | 规定动画被播放的次数。默认是 1。                         | 3    |
| [animation-direction](http://www.w3school.com.cn/cssref/pr_animation-direction.asp) | 规定动画是否在下一周期逆向地播放。默认是 "normal"。      | 3    |
| [animation-play-state](http://www.w3school.com.cn/cssref/pr_animation-play-state.asp) | 规定动画是否正在运行或暂停。默认是 "running"。           | 3    |
| [animation-fill-mode](http://www.w3school.com.cn/cssref/pr_animation-fill-mode.asp) | 规定对象动画时间之外的状态。                             | 3    |

下面的两个例子设置了所有动画属性：

### 实例

运行名为 myfirst 的动画，其中设置了所有动画属性：

```
div
{
animation-name: myfirst;
animation-duration: 5s;
animation-timing-function: linear;
animation-delay: 2s;
animation-iteration-count: infinite;
animation-direction: alternate;
animation-play-state: running;
/* Firefox: */
-moz-animation-name: myfirst;
-moz-animation-duration: 5s;
-moz-animation-timing-function: linear;
-moz-animation-delay: 2s;
-moz-animation-iteration-count: infinite;
-moz-animation-direction: alternate;
-moz-animation-play-state: running;
/* Safari 和 Chrome: */
-webkit-animation-name: myfirst;
-webkit-animation-duration: 5s;
-webkit-animation-timing-function: linear;
-webkit-animation-delay: 2s;
-webkit-animation-iteration-count: infinite;
-webkit-animation-direction: alternate;
-webkit-animation-play-state: running;
/* Opera: */
-o-animation-name: myfirst;
-o-animation-duration: 5s;
-o-animation-timing-function: linear;
-o-animation-delay: 2s;
-o-animation-iteration-count: infinite;
-o-animation-direction: alternate;
-o-animation-play-state: running;
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_animation4)

### 实例

与上面的动画相同，但是使用了简写的动画 animation 属性：

```
div
{
animation: myfirst 5s linear 2s infinite alternate;
/* Firefox: */
-moz-animation: myfirst 5s linear 2s infinite alternate;
/* Safari 和 Chrome: */
-webkit-animation: myfirst 5s linear 2s infinite alternate;
/* Opera: */
-o-animation: myfirst 5s linear 2s infinite alternate;
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_animation5)

## CSS3 多列

通过 CSS3，您能够创建多个列来对文本进行布局 - 就像报纸那样！

在本章中，您将学习如下多列属性：

- column-count
- column-gap
- column-rule

### 浏览器支持

| 属性         | 浏览器支持 |      |      |      |      |
| ------------ | ---------- | ---- | ---- | ---- | ---- |
| column-count |            |      |      |      |      |
| column-gap   |            |      |      |      |      |
| column-rule  |            |      |      |      |      |

Internet Explorer 10 和 Opera 支持多列属性。

Firefox 需要前缀 -moz-。

Chrome 和 Safari 需要前缀 -webkit-。

注释：Internet Explorer 9 以及更早的版本不支持多列属性。

### CSS3 创建多列

column-count 属性规定元素应该被分隔的列数：

**实例**

把 div 元素中的文本分隔为三列：

```
div{
-moz-column-count:3; 	/* Firefox */
-webkit-column-count:3; /* Safari 和 Chrome */
column-count:3;
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_column-count)

### CSS3 规定列之间的间隔

column-gap 属性规定列之间的间隔：

**实例**

规定列之间 40 像素的间隔：

```
div
{
-moz-column-gap:40px;		/* Firefox */
-webkit-column-gap:40px;	/* Safari 和 Chrome */
column-gap:40px;
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_column-gap)

### CSS3 列规则

column-rule 属性设置列之间的宽度、样式和颜色规则。

**实例**

规定列之间的宽度、样式和颜色规则：

```
div
{
-moz-column-rule:3px outset #ff0000;	/* Firefox */
-webkit-column-rule:3px outset #ff0000;	/* Safari and Chrome */
column-rule:3px outset #ff0000;
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_column-rule)

### 新的多列属性

下面的表格列出了所有的转换属性：

| 属性                                                         | 描述                                               | CSS  |
| ------------------------------------------------------------ | -------------------------------------------------- | ---- |
| [column-count](http://www.w3school.com.cn/cssref/pr_column-count.asp) | 规定元素应该被分隔的列数。                         | 3    |
| [column-fill](http://www.w3school.com.cn/cssref/pr_column-fill.asp) | 规定如何填充列。                                   | 3    |
| [column-gap](http://www.w3school.com.cn/cssref/pr_column-gap.asp) | 规定列之间的间隔。                                 | 3    |
| [column-rule](http://www.w3school.com.cn/cssref/pr_column-rule.asp) | 设置所有 column-rule-* 属性的简写属性。            | 3    |
| [column-rule-color](http://www.w3school.com.cn/cssref/pr_column-rule-color.asp) | 规定列之间规则的颜色。                             | 3    |
| [column-rule-style](http://www.w3school.com.cn/cssref/pr_column-rule-style.asp) | 规定列之间规则的样式。                             | 3    |
| [column-rule-width](http://www.w3school.com.cn/cssref/pr_column-rule-width.asp) | 规定列之间规则的宽度。                             | 3    |
| [column-span](http://www.w3school.com.cn/cssref/pr_column-span.asp) | 规定元素应该横跨的列数。                           | 3    |
| [column-width](http://www.w3school.com.cn/cssref/pr_column-width.asp) | 规定列的宽度。                                     | 3    |
| [columns](http://www.w3school.com.cn/cssref/pr_columns.asp)  | 规定设置 column-width 和 column-count 的简写属性。 | 3    |

## CSS3 用户界面

在 CSS3 中，新的用户界面特性包括重设元素尺寸、盒尺寸以及轮廓等。

在本章中，您将学到以下用户界面属性：

- resize
- box-sizing
- outline-offset

### 浏览器支持

| 属性           | 浏览器支持 |      |      |      |      |
| -------------- | ---------- | ---- | ---- | ---- | ---- |
| resize         |            |      |      |      |      |
| box-sizing     |            |      |      |      |      |
| outline-offset |            |      |      |      |      |

Firefox、Chrome 以及 Safari 支持 resize 属性。

Internet Explorer、Chrome、Safari 以及 Opera 支持 box-sizing 属性。Firefox 需要前缀 -moz-。

所有主流浏览器都支持 outline-offset 属性，除了 Internet Explorer。

### CSS3 Resizing

在 CSS3，resize 属性规定是否可由用户调整元素尺寸。

这个 div 元素可由用户调整尺寸（在 Firefox 4+、Chrome 以及 Safari 中）。

CSS 代码如下：

**实例**

规定 div 元素可由用户调整大小：

```
div
{
resize:both;
overflow:auto;
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_resize)

### CSS3 Box Sizing

box-sizing 属性允许您以确切的方式定义适应某个区域的具体内容。

**实例**

规定两个并排的带边框方框：

```
div
{
box-sizing:border-box;
-moz-box-sizing:border-box;	/* Firefox */
-webkit-box-sizing:border-box;	/* Safari */
width:50%;
float:left;
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_box-sizing)

### CSS3 Outline Offset

outline-offset 属性对轮廓进行偏移，并在超出边框边缘的位置绘制轮廓。

轮廓与边框有两点不同：

- 轮廓不占用空间
- 轮廓可能是非矩形

这个 div 在边框之外 15 像素处有一个轮廓。

CSS 代码如下：

**实例**

规定边框边缘之外 15 像素处的轮廓：

```
div
{
border:2px solid black;
outline:2px solid red;
outline-offset:15px;
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_outline-offset)

### 新的用户界面属性

下面的表格列出了所有的转换属性：

| 属性                                                         | 描述                                               | CSS  |
| ------------------------------------------------------------ | -------------------------------------------------- | ---- |
| [appearance](http://www.w3school.com.cn/cssref/pr_appearance.asp) | 允许您将元素设置为标准用户界面元素的外观           | 3    |
| [box-sizing](http://www.w3school.com.cn/cssref/pr_box-sizing.asp) | 允许您以确切的方式定义适应某个区域的具体内容。     | 3    |
| [icon](http://www.w3school.com.cn/cssref/pr_icon.asp)        | 为创作者提供使用图标化等价物来设置元素样式的能力。 | 3    |
| [nav-down](http://www.w3school.com.cn/cssref/pr_nav-down.asp) | 规定在使用 arrow-down 导航键时向何处导航。         | 3    |
| [nav-index](http://www.w3school.com.cn/cssref/pr_nav-index.asp) | 设置元素的 tab 键控制次序。                        | 3    |
| [nav-left](http://www.w3school.com.cn/cssref/pr_nav-left.asp) | 规定在使用 arrow-left 导航键时向何处导航。         | 3    |
| [nav-right](http://www.w3school.com.cn/cssref/pr_nav-right.asp) | 规定在使用 arrow-right 导航键时向何处导航。        | 3    |
| [nav-up](http://www.w3school.com.cn/cssref/pr_nav-up.asp)    | 规定在使用 arrow-up 导航键时向何处导航。           | 3    |
| [outline-offset](http://www.w3school.com.cn/cssref/pr_outline-offset.asp) | 对轮廓进行偏移，并在超出边框边缘的位置绘制轮廓。   | 3    |
| [resize](http://www.w3school.com.cn/cssref/pr_resize.asp)    | 规定是否可由用户对元素的尺寸进行调整。             | 3    |

# CSS 参考手册



W3School 的 CSS 参考手册定期通过所有主流浏览器进行测试。

## CSS 属性

CSS 属性组：

- [动画](http://www.w3school.com.cn/cssref/index.asp#animation)
- [背景](http://www.w3school.com.cn/cssref/index.asp#background)
- [边框和轮廓](http://www.w3school.com.cn/cssref/index.asp#border)
- [盒（框）](http://www.w3school.com.cn/cssref/index.asp#box)
- [颜色](http://www.w3school.com.cn/cssref/index.asp#color)
- [内容分页媒体](http://www.w3school.com.cn/cssref/index.asp#contentpm)
- [定位](http://www.w3school.com.cn/cssref/index.asp#dimension)
- [可伸缩框](http://www.w3school.com.cn/cssref/index.asp#flexbox)
- [字体](http://www.w3school.com.cn/cssref/index.asp#font)
- [生成内容](http://www.w3school.com.cn/cssref/index.asp#generatedcontent)
- [网格](http://www.w3school.com.cn/cssref/index.asp#grid)
- [超链接](http://www.w3school.com.cn/cssref/index.asp#hyperlink)
- 行框
- [列表](http://www.w3school.com.cn/cssref/index.asp#list)
- [外边距](http://www.w3school.com.cn/cssref/index.asp#margin)
- [Marquee](http://www.w3school.com.cn/cssref/index.asp#marquee)
- [多列](http://www.w3school.com.cn/cssref/index.asp#multicolumn)
- [内边距](http://www.w3school.com.cn/cssref/index.asp#padding)
- [分页媒体](http://www.w3school.com.cn/cssref/index.asp#pagedmedia)
- [定位](http://www.w3school.com.cn/cssref/index.asp#positioning)
- [打印](http://www.w3school.com.cn/cssref/index.asp#print)
- Ruby
- 语音
- [表格](http://www.w3school.com.cn/cssref/index.asp#table)
- [文本](http://www.w3school.com.cn/cssref/index.asp#text)
- [2D/3D 转换](http://www.w3school.com.cn/cssref/index.asp#transform)
- [过渡](http://www.w3school.com.cn/cssref/index.asp#transition)
- [用户界面](http://www.w3school.com.cn/cssref/index.asp#userinterface)

"CSS" 列指示该属性是在哪个 CSS 版本（CSS1、CSS2 或 CSS3）中定义的。

## CSS3 动画属性（Animation）

| 属性                                                         | 描述                                                     | CSS  |
| ------------------------------------------------------------ | -------------------------------------------------------- | ---- |
| [@keyframes](http://www.w3school.com.cn/cssref/pr_keyframes.asp) | 规定动画。                                               | 3    |
| [animation](http://www.w3school.com.cn/cssref/pr_animation.asp) | 所有动画属性的简写属性，除了 animation-play-state 属性。 | 3    |
| [animation-name](http://www.w3school.com.cn/cssref/pr_animation-name.asp) | 规定 @keyframes 动画的名称。                             | 3    |
| [animation-duration](http://www.w3school.com.cn/cssref/pr_animation-duration.asp) | 规定动画完成一个周期所花费的秒或毫秒。                   | 3    |
| [animation-timing-function](http://www.w3school.com.cn/cssref/pr_animation-timing-function.asp) | 规定动画的速度曲线。                                     | 3    |
| [animation-delay](http://www.w3school.com.cn/cssref/pr_animation-delay.asp) | 规定动画何时开始。                                       | 3    |
| [animation-iteration-count](http://www.w3school.com.cn/cssref/pr_animation-iteration-count.asp) | 规定动画被播放的次数。                                   | 3    |
| [animation-direction](http://www.w3school.com.cn/cssref/pr_animation-direction.asp) | 规定动画是否在下一周期逆向地播放。                       | 3    |
| [animation-play-state](http://www.w3school.com.cn/cssref/pr_animation-play-state.asp) | 规定动画是否正在运行或暂停。                             | 3    |
| [animation-fill-mode](http://www.w3school.com.cn/cssref/pr_animation-fill-mode.asp) | 规定对象动画时间之外的状态。                             | 3    |

## CSS 背景属性（Background）

| 属性                                                         | 描述                                             | CSS  |
| ------------------------------------------------------------ | ------------------------------------------------ | ---- |
| [background](http://www.w3school.com.cn/cssref/pr_background.asp) | 在一个声明中设置所有的背景属性。                 | 1    |
| [background-attachment](http://www.w3school.com.cn/cssref/pr_background-attachment.asp) | 设置背景图像是否固定或者随着页面的其余部分滚动。 | 1    |
| [background-color](http://www.w3school.com.cn/cssref/pr_background-color.asp) | 设置元素的背景颜色。                             | 1    |
| [background-image](http://www.w3school.com.cn/cssref/pr_background-image.asp) | 设置元素的背景图像。                             | 1    |
| [background-position](http://www.w3school.com.cn/cssref/pr_background-position.asp) | 设置背景图像的开始位置。                         | 1    |
| [background-repeat](http://www.w3school.com.cn/cssref/pr_background-repeat.asp) | 设置是否及如何重复背景图像。                     | 1    |
| [background-clip](http://www.w3school.com.cn/cssref/pr_background-clip.asp) | 规定背景的绘制区域。                             | 3    |
| [background-origin](http://www.w3school.com.cn/cssref/pr_background-origin.asp) | 规定背景图片的定位区域。                         | 3    |
| [background-size](http://www.w3school.com.cn/cssref/pr_background-size.asp) | 规定背景图片的尺寸。                             | 3    |

## CSS 边框属性（Border 和 Outline）

| 属性                                                         | 描述                                                         | CSS  |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ---- |
| [border](http://www.w3school.com.cn/cssref/pr_border.asp)    | 在一个声明中设置所有的边框属性。                             | 1    |
| [border-bottom](http://www.w3school.com.cn/cssref/pr_border-bottom.asp) | 在一个声明中设置所有的下边框属性。                           | 1    |
| [border-bottom-color](http://www.w3school.com.cn/cssref/pr_border-bottom_color.asp) | 设置下边框的颜色。                                           | 2    |
| [border-bottom-style](http://www.w3school.com.cn/cssref/pr_border-bottom_style.asp) | 设置下边框的样式。                                           | 2    |
| [border-bottom-width](http://www.w3school.com.cn/cssref/pr_border-bottom_width.asp) | 设置下边框的宽度。                                           | 1    |
| [border-color](http://www.w3school.com.cn/cssref/pr_border-color.asp) | 设置四条边框的颜色。                                         | 1    |
| [border-left](http://www.w3school.com.cn/cssref/pr_border-left.asp) | 在一个声明中设置所有的左边框属性。                           | 1    |
| [border-left-color](http://www.w3school.com.cn/cssref/pr_border-left_color.asp) | 设置左边框的颜色。                                           | 2    |
| [border-left-style](http://www.w3school.com.cn/cssref/pr_border-left_style.asp) | 设置左边框的样式。                                           | 2    |
| [border-left-width](http://www.w3school.com.cn/cssref/pr_border-left_width.asp) | 设置左边框的宽度。                                           | 1    |
| [border-right](http://www.w3school.com.cn/cssref/pr_border-right.asp) | 在一个声明中设置所有的右边框属性。                           | 1    |
| [border-right-color](http://www.w3school.com.cn/cssref/pr_border-right_color.asp) | 设置右边框的颜色。                                           | 2    |
| [border-right-style](http://www.w3school.com.cn/cssref/pr_border-right_style.asp) | 设置右边框的样式。                                           | 2    |
| [border-right-width](http://www.w3school.com.cn/cssref/pr_border-right_width.asp) | 设置右边框的宽度。                                           | 1    |
| [border-style](http://www.w3school.com.cn/cssref/pr_border-style.asp) | 设置四条边框的样式。                                         | 1    |
| [border-top](http://www.w3school.com.cn/cssref/pr_border-top.asp) | 在一个声明中设置所有的上边框属性。                           | 1    |
| [border-top-color](http://www.w3school.com.cn/cssref/pr_border-top_color.asp) | 设置上边框的颜色。                                           | 2    |
| [border-top-style](http://www.w3school.com.cn/cssref/pr_border-top_style.asp) | 设置上边框的样式。                                           | 2    |
| [border-top-width](http://www.w3school.com.cn/cssref/pr_border-top_width.asp) | 设置上边框的宽度。                                           | 1    |
| [border-width](http://www.w3school.com.cn/cssref/pr_border-width.asp) | 设置四条边框的宽度。                                         | 1    |
| [outline](http://www.w3school.com.cn/cssref/pr_outline.asp)  | 在一个声明中设置所有的轮廓属性。                             | 2    |
| [outline-color](http://www.w3school.com.cn/cssref/pr_outline-color.asp) | 设置轮廓的颜色。                                             | 2    |
| [outline-style](http://www.w3school.com.cn/cssref/pr_outline-style.asp) | 设置轮廓的样式。                                             | 2    |
| [outline-width](http://www.w3school.com.cn/cssref/pr_outline-width.asp) | 设置轮廓的宽度。                                             | 2    |
| [border-bottom-left-radius](http://www.w3school.com.cn/cssref/pr_border-bottom-left-radius.asp) | 定义边框左下角的形状。                                       | 3    |
| [border-bottom-right-radius](http://www.w3school.com.cn/cssref/pr_border-bottom-right-radius.asp) | 定义边框右下角的形状。                                       | 3    |
| [border-image](http://www.w3school.com.cn/cssref/pr_border-image.asp) | 简写属性，设置所有 border-image-* 属性。                     | 3    |
| [border-image-outset](http://www.w3school.com.cn/cssref/pr_border-image-outset.asp) | 规定边框图像区域超出边框的量。                               | 3    |
| [border-image-repeat](http://www.w3school.com.cn/cssref/pr_border-image-repeat.asp) | 图像边框是否应平铺(repeated)、铺满(rounded)或拉伸(stretched)。 | 3    |
| [border-image-slice](http://www.w3school.com.cn/cssref/pr_border-image-slice.asp) | 规定图像边框的向内偏移。                                     | 3    |
| [border-image-source](http://www.w3school.com.cn/cssref/pr_border-image-source.asp) | 规定用作边框的图片。                                         | 3    |
| [border-image-width](http://www.w3school.com.cn/cssref/pr_border-image-width.asp) | 规定图片边框的宽度。                                         | 3    |
| [border-radius](http://www.w3school.com.cn/cssref/pr_border-radius.asp) | 简写属性，设置所有四个 border-*-radius 属性。                | 3    |
| [border-top-left-radius](http://www.w3school.com.cn/cssref/pr_border-top-left-radius.asp) | 定义边框左上角的形状。                                       | 3    |
| [border-top-right-radius](http://www.w3school.com.cn/cssref/pr_border-top-right-radius.asp) | 定义边框右下角的形状。                                       | 3    |
| box-decoration-break                                         |                                                              | 3    |
| [box-shadow](http://www.w3school.com.cn/cssref/pr_box-shadow.asp) | 向方框添加一个或多个阴影。                                   | 3    |

## Box 属性

| 属性                                                         | 描述                                                        | CSS  |
| ------------------------------------------------------------ | ----------------------------------------------------------- | ---- |
| [overflow-x](http://www.w3school.com.cn/cssref/pr_overflow-x.asp) | 如果内容溢出了元素内容区域，是否对内容的左/右边缘进行裁剪。 | 3    |
| [overflow-y](http://www.w3school.com.cn/cssref/pr_overflow-y.asp) | 如果内容溢出了元素内容区域，是否对内容的上/下边缘进行裁剪。 | 3    |
| [overflow-style](http://www.w3school.com.cn/cssref/pr_overflow-style.asp) | 规定溢出元素的首选滚动方法。                                | 3    |
| [rotation](http://www.w3school.com.cn/cssref/pr_rotation.asp) | 围绕由 rotation-point 属性定义的点对元素进行旋转。          | 3    |
| [rotation-point](http://www.w3school.com.cn/cssref/pr_rotation-point.asp) | 定义距离上左边框边缘的偏移点。                              | 3    |

## Color 属性

| 属性                                                        | 描述                                           | CSS  |
| ----------------------------------------------------------- | ---------------------------------------------- | ---- |
| color-profile                                               | 允许使用源的颜色配置文件的默认以外的规范。     | 3    |
| [opacity](http://www.w3school.com.cn/cssref/pr_opacity.asp) | 规定元素的不透明级别。                         | 3    |
| rendering-intent                                            | 允许使用颜色配置文件渲染意图的默认以外的规范。 | 3    |

## Content for Paged Media 属性

| 属性                | 描述                                                   | CSS  |
| ------------------- | ------------------------------------------------------ | ---- |
| bookmark-label      | 规定书签的标记。                                       | 3    |
| bookmark-level      | 规定书签的级别。                                       | 3    |
| bookmark-target     | 规定书签链接的目标。                                   | 3    |
| float-offset        | 将元素放在 float 属性通常放置的位置的相反方向。        | 3    |
| hyphenate-after     | 规定连字单词中连字符之后的最小字符数。                 | 3    |
| hyphenate-before    | 规定连字单词中连字符之前的最小字符数。                 | 3    |
| hyphenate-character | 规定当发生断字时显示的字符串。                         | 3    |
| hyphenate-lines     | 指示元素中连续断字连线的最大数。                       | 3    |
| hyphenate-resource  | 规定帮助浏览器确定断字点的外部资源（逗号分隔的列表）。 | 3    |
| hyphens             | 设置如何对单词进行拆分，以改善段落的布局。             | 3    |
| image-resolution    | 规定图像的正确分辨率。                                 | 3    |
| marks               | 向文档添加裁切标记或十字标记。                         | 3    |
| string-set          |                                                        | 3    |

## CSS 尺寸属性（Dimension）

| 属性                                                         | 描述                 | CSS  |
| ------------------------------------------------------------ | -------------------- | ---- |
| [height](http://www.w3school.com.cn/cssref/pr_dim_height.asp) | 设置元素高度。       | 1    |
| [max-height](http://www.w3school.com.cn/cssref/pr_dim_max-height.asp) | 设置元素的最大高度。 | 2    |
| [max-width](http://www.w3school.com.cn/cssref/pr_dim_max-width.asp) | 设置元素的最大宽度。 | 2    |
| [min-height](http://www.w3school.com.cn/cssref/pr_dim_min-height.asp) | 设置元素的最小高度。 | 2    |
| [min-width](http://www.w3school.com.cn/cssref/pr_dim_min-width.asp) | 设置元素的最小宽度。 | 2    |
| [width](http://www.w3school.com.cn/cssref/pr_dim_width.asp)  | 设置元素的宽度。     | 1    |

## 可伸缩框属性（Flexible Box）

| 属性                                                         | 描述                                           | CSS  |
| ------------------------------------------------------------ | ---------------------------------------------- | ---- |
| [box-align](http://www.w3school.com.cn/cssref/pr_box-align.asp) | 规定如何对齐框的子元素。                       | 3    |
| [box-direction](http://www.w3school.com.cn/cssref/pr_box-direction.asp) | 规定框的子元素的显示方向。                     | 3    |
| [box-flex](http://www.w3school.com.cn/cssref/pr_box-flex.asp) | 规定框的子元素是否可伸缩。                     | 3    |
| [box-flex-group](http://www.w3school.com.cn/cssref/pr_box-flex-group.asp) | 将可伸缩元素分配到柔性分组。                   | 3    |
| [box-lines](http://www.w3school.com.cn/cssref/pr_box-lines.asp) | 规定当超出父元素框的空间时，是否换行显示。     | 3    |
| [box-ordinal-group](http://www.w3school.com.cn/cssref/pr_box-ordinal-group.asp) | 规定框的子元素的显示次序。                     | 3    |
| [box-orient](http://www.w3school.com.cn/cssref/pr_box-orient.asp) | 规定框的子元素是否应水平或垂直排列。           | 3    |
| [box-pack](http://www.w3school.com.cn/cssref/pr_box-pack.asp) | 规定水平框中的水平位置或者垂直框中的垂直位置。 | 3    |

## CSS 字体属性（Font）

| 属性                                                         | 描述                                   | CSS  |
| ------------------------------------------------------------ | -------------------------------------- | ---- |
| [font](http://www.w3school.com.cn/cssref/pr_font_font.asp)   | 在一个声明中设置所有字体属性。         | 1    |
| [font-family](http://www.w3school.com.cn/cssref/pr_font_font-family.asp) | 规定文本的字体系列。                   | 1    |
| [font-size](http://www.w3school.com.cn/cssref/pr_font_font-size.asp) | 规定文本的字体尺寸。                   | 1    |
| [font-size-adjust](http://www.w3school.com.cn/cssref/pr_font_font-size-adjust.asp) | 为元素规定 aspect 值。                 | 2    |
| [font-stretch](http://www.w3school.com.cn/cssref/pr_font_font-stretch.asp) | 收缩或拉伸当前的字体系列。             | 2    |
| [font-style](http://www.w3school.com.cn/cssref/pr_font_font-style.asp) | 规定文本的字体样式。                   | 1    |
| [font-variant](http://www.w3school.com.cn/cssref/pr_font_font-variant.asp) | 规定是否以小型大写字母的字体显示文本。 | 1    |
| [font-weight](http://www.w3school.com.cn/cssref/pr_font_weight.asp) | 规定字体的粗细。                       | 1    |

## 内容生成（Generated Content）

| 属性                                                         | 描述                                                     | CSS  |
| ------------------------------------------------------------ | -------------------------------------------------------- | ---- |
| [content](http://www.w3school.com.cn/cssref/pr_gen_content.asp) | 与 :before 以及 :after 伪元素配合使用，来插入生成内容。  | 2    |
| [counter-increment](http://www.w3school.com.cn/cssref/pr_gen_counter-increment.asp) | 递增或递减一个或多个计数器。                             | 2    |
| [counter-reset](http://www.w3school.com.cn/cssref/pr_gen_counter-reset.asp) | 创建或重置一个或多个计数器。                             | 2    |
| [quotes](http://www.w3school.com.cn/cssref/pr_gen_quotes.asp) | 设置嵌套引用的引号类型。                                 | 2    |
| crop                                                         | 允许被替换元素仅仅是对象的矩形区域，而不是整个对象。     | 3    |
| move-to                                                      | 从流中删除元素，然后在文档中后面的点上重新插入。         | 3    |
| page-policy                                                  | 确定元素基于页面的 occurrence 应用于计数器还是字符串值。 | 3    |

## Grid 属性

| 属性                                                         | 描述                     | CSS  |
| ------------------------------------------------------------ | ------------------------ | ---- |
| [grid-columns](http://www.w3school.com.cn/cssref/pr_grid-columns.asp) | 规定网格中每个列的宽度。 | 3    |
| [grid-rows](http://www.w3school.com.cn/cssref/pr_grid-rows.asp) | 规定网格中每个列的高度。 | 3    |

## Hyperlink 属性

| 属性                                                         | 描述                                                         | CSS  |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ---- |
| [target](http://www.w3school.com.cn/cssref/pr_target.asp)    | 简写属性，设置target-name、target-new以及target-position属性。 | 3    |
| [target-name](http://www.w3school.com.cn/cssref/pr_target-name.asp) | 规定在何处打开链接（链接的目标）。                           | 3    |
| [target-new](http://www.w3school.com.cn/cssref/pr_target-new.asp) | 规定目标链接在新窗口还是在已有窗口的新标签页中打开。         | 3    |
| [target-position](http://www.w3school.com.cn/cssref/pr_target-position.asp) | 规定在何处放置新的目标链接。                                 | 3    |

## CSS 列表属性（List）

| 属性                                                         | 描述                             | CSS  |
| ------------------------------------------------------------ | -------------------------------- | ---- |
| [list-style](http://www.w3school.com.cn/cssref/pr_list-style.asp) | 在一个声明中设置所有的列表属性。 | 1    |
| [list-style-image](http://www.w3school.com.cn/cssref/pr_list-style-image.asp) | 将图象设置为列表项标记。         | 1    |
| [list-style-position](http://www.w3school.com.cn/cssref/pr_list-style-position.asp) | 设置列表项标记的放置位置。       | 1    |
| [list-style-type](http://www.w3school.com.cn/cssref/pr_list-style-type.asp) | 设置列表项标记的类型。           | 1    |
| marker-offset                                                |                                  | 2    |

## CSS 外边距属性（Margin）

| 属性                                                         | 描述                             | CSS  |
| ------------------------------------------------------------ | -------------------------------- | ---- |
| [margin](http://www.w3school.com.cn/cssref/pr_margin.asp)    | 在一个声明中设置所有外边距属性。 | 1    |
| [margin-bottom](http://www.w3school.com.cn/cssref/pr_margin-bottom.asp) | 设置元素的下外边距。             | 1    |
| [margin-left](http://www.w3school.com.cn/cssref/pr_margin-left.asp) | 设置元素的左外边距。             | 1    |
| [margin-right](http://www.w3school.com.cn/cssref/pr_margin-right.asp) | 设置元素的右外边距。             | 1    |
| [margin-top](http://www.w3school.com.cn/cssref/pr_margin-top.asp) | 设置元素的上外边距。             | 1    |

## Marquee 属性

| 属性               | 描述                 | CSS  |
| ------------------ | -------------------- | ---- |
| marquee-direction  | 设置移动内容的方向。 | 3    |
| marquee-play-count | 设置内容移动多少次。 | 3    |
| marquee-speed      | 设置内容滚动得多快。 | 3    |
| marquee-style      | 设置移动内容的样式。 | 3    |

## 多列属性（Multi-column）

| 属性                                                         | 描述                                               | CSS  |
| ------------------------------------------------------------ | -------------------------------------------------- | ---- |
| [column-count](http://www.w3school.com.cn/cssref/pr_column-count.asp) | 规定元素应该被分隔的列数。                         | 3    |
| [column-fill](http://www.w3school.com.cn/cssref/pr_column-fill.asp) | 规定如何填充列。                                   | 3    |
| [column-gap](http://www.w3school.com.cn/cssref/pr_column-gap.asp) | 规定列之间的间隔。                                 | 3    |
| [column-rule](http://www.w3school.com.cn/cssref/pr_column-rule.asp) | 设置所有 column-rule-* 属性的简写属性。            | 3    |
| [column-rule-color](http://www.w3school.com.cn/cssref/pr_column-rule-color.asp) | 规定列之间规则的颜色。                             | 3    |
| [column-rule-style](http://www.w3school.com.cn/cssref/pr_column-rule-style.asp) | 规定列之间规则的样式。                             | 3    |
| [column-rule-width](http://www.w3school.com.cn/cssref/pr_column-rule-width.asp) | 规定列之间规则的宽度。                             | 3    |
| [column-span](http://www.w3school.com.cn/cssref/pr_column-span.asp) | 规定元素应该横跨的列数。                           | 3    |
| [column-width](http://www.w3school.com.cn/cssref/pr_column-width.asp) | 规定列的宽度。                                     | 3    |
| [columns](http://www.w3school.com.cn/cssref/pr_columns.asp)  | 规定设置 column-width 和 column-count 的简写属性。 | 3    |

## CSS 内边距属性（Padding）

| 属性                                                         | 描述                             | CSS  |
| ------------------------------------------------------------ | -------------------------------- | ---- |
| [padding](http://www.w3school.com.cn/cssref/pr_padding.asp)  | 在一个声明中设置所有内边距属性。 | 1    |
| [padding-bottom](http://www.w3school.com.cn/cssref/pr_padding-bottom.asp) | 设置元素的下内边距。             | 1    |
| [padding-left](http://www.w3school.com.cn/cssref/pr_padding-left.asp) | 设置元素的左内边距。             | 1    |
| [padding-right](http://www.w3school.com.cn/cssref/pr_padding-right.asp) | 设置元素的右内边距。             | 1    |
| [padding-top](http://www.w3school.com.cn/cssref/pr_padding-top.asp) | 设置元素的上内边距。             | 1    |

## Paged Media 属性

| 属性              | 描述                                                        | CSS  |
| ----------------- | ----------------------------------------------------------- | ---- |
| fit               | 示意如何对width和height属性均不是auto的被替换元素进行缩放。 | 3    |
| fit-position      | 定义盒内对象的对齐方式。                                    | 3    |
| image-orientation | 规定用户代理应用于图像的顺时针方向旋转。                    | 3    |
| page              | 规定元素应该被显示的页面特定类型。                          | 3    |
| size              | 规定页面内容包含框的尺寸和方向。                            | 3    |

## CSS 定位属性（Positioning）

| 属性                                                         | 描述                                                   | CSS  |
| ------------------------------------------------------------ | ------------------------------------------------------ | ---- |
| [bottom](http://www.w3school.com.cn/cssref/pr_pos_bottom.asp) | 设置定位元素下外边距边界与其包含块下边界之间的偏移。   | 2    |
| [clear](http://www.w3school.com.cn/cssref/pr_class_clear.asp) | 规定元素的哪一侧不允许其他浮动元素。                   | 1    |
| [clip](http://www.w3school.com.cn/cssref/pr_pos_clip.asp)    | 剪裁绝对定位元素。                                     | 2    |
| [cursor](http://www.w3school.com.cn/cssref/pr_class_cursor.asp) | 规定要显示的光标的类型（形状）。                       | 2    |
| [display](http://www.w3school.com.cn/cssref/pr_class_display.asp) | 规定元素应该生成的框的类型。                           | 1    |
| [float](http://www.w3school.com.cn/cssref/pr_class_float.asp) | 规定框是否应该浮动。                                   | 1    |
| [left](http://www.w3school.com.cn/cssref/pr_pos_left.asp)    | 设置定位元素左外边距边界与其包含块左边界之间的偏移。   | 2    |
| [overflow](http://www.w3school.com.cn/cssref/pr_pos_overflow.asp) | 规定当内容溢出元素框时发生的事情。                     | 2    |
| [position](http://www.w3school.com.cn/cssref/pr_class_position.asp) | 规定元素的定位类型。                                   | 2    |
| [right](http://www.w3school.com.cn/cssref/pr_pos_right.asp)  | 设置定位元素右外边距边界与其包含块右边界之间的偏移。   | 2    |
| [top](http://www.w3school.com.cn/cssref/pr_pos_top.asp)      | 设置定位元素的上外边距边界与其包含块上边界之间的偏移。 | 2    |
| [vertical-align](http://www.w3school.com.cn/cssref/pr_pos_vertical-align.asp) | 设置元素的垂直对齐方式。                               | 1    |
| [visibility](http://www.w3school.com.cn/cssref/pr_class_visibility.asp) | 规定元素是否可见。                                     | 2    |
| [z-index](http://www.w3school.com.cn/cssref/pr_pos_z-index.asp) | 设置元素的堆叠顺序。                                   | 2    |

## CSS 打印属性（Print）

| 属性                                                         | 描述                                                   | CSS  |
| ------------------------------------------------------------ | ------------------------------------------------------ | ---- |
| orphans                                                      | 设置当元素内部发生分页时必须在页面底部保留的最少行数。 | 2    |
| [page-break-after](http://www.w3school.com.cn/cssref/pr_print_page-break-after.asp) | 设置元素后的分页行为。                                 | 2    |
| [page-break-before](http://www.w3school.com.cn/cssref/pr_print_page-break-before.asp) | 设置元素前的分页行为。                                 | 2    |
| [page-break-inside](http://www.w3school.com.cn/cssref/pr_print_page-break-inside.asp) | 设置元素内部的分页行为。                               | 2    |
| widows                                                       | 设置当元素内部发生分页时必须在页面顶部保留的最少行数。 | 2    |

## CSS 表格属性（Table）

| 属性                                                         | 描述                                         | CSS  |
| ------------------------------------------------------------ | -------------------------------------------- | ---- |
| [border-collapse](http://www.w3school.com.cn/cssref/pr_tab_border-collapse.asp) | 规定是否合并表格边框。                       | 2    |
| [border-spacing](http://www.w3school.com.cn/cssref/pr_tab_border-spacing.asp) | 规定相邻单元格边框之间的距离。               | 2    |
| [caption-side](http://www.w3school.com.cn/cssref/pr_tab_caption-side.asp) | 规定表格标题的位置。                         | 2    |
| [empty-cells](http://www.w3school.com.cn/cssref/pr_tab_empty-cells.asp) | 规定是否显示表格中的空单元格上的边框和背景。 | 2    |
| [table-layout](http://www.w3school.com.cn/cssref/pr_tab_table-layout.asp) | 设置用于表格的布局算法。                     | 2    |

## CSS 文本属性（Text）

| 属性                                                         | 描述                                                    | CSS  |
| ------------------------------------------------------------ | ------------------------------------------------------- | ---- |
| [color](http://www.w3school.com.cn/cssref/pr_text_color.asp) | 设置文本的颜色。                                        | 1    |
| [direction](http://www.w3school.com.cn/cssref/pr_text_direction.asp) | 规定文本的方向 / 书写方向。                             | 2    |
| [letter-spacing](http://www.w3school.com.cn/cssref/pr_text_letter-spacing.asp) | 设置字符间距。                                          | 1    |
| [line-height](http://www.w3school.com.cn/cssref/pr_dim_line-height.asp) | 设置行高。                                              | 1    |
| [text-align](http://www.w3school.com.cn/cssref/pr_text_text-align.asp) | 规定文本的水平对齐方式。                                | 1    |
| [text-decoration](http://www.w3school.com.cn/cssref/pr_text_text-decoration.asp) | 规定添加到文本的装饰效果。                              | 1    |
| [text-indent](http://www.w3school.com.cn/cssref/pr_text_text-indent.asp) | 规定文本块首行的缩进。                                  | 1    |
| text-shadow                                                  | 规定添加到文本的阴影效果。                              | 2    |
| [text-transform](http://www.w3school.com.cn/cssref/pr_text_text-transform.asp) | 控制文本的大小写。                                      | 1    |
| [unicode-bidi](http://www.w3school.com.cn/cssref/pr_unicode-bidi.asp) | 设置文本方向。                                          | 2    |
| [white-space](http://www.w3school.com.cn/cssref/pr_text_white-space.asp) | 规定如何处理元素中的空白。                              | 1    |
| [word-spacing](http://www.w3school.com.cn/cssref/pr_text_word-spacing.asp) | 设置单词间距。                                          | 1    |
| [hanging-punctuation](http://www.w3school.com.cn/cssref/pr_hanging-punctuation.asp) | 规定标点字符是否位于线框之外。                          | 3    |
| [punctuation-trim](http://www.w3school.com.cn/cssref/pr_punctuation-trim.asp) | 规定是否对标点字符进行修剪。                            | 3    |
| text-align-last                                              | 设置如何对齐最后一行或紧挨着强制换行符之前的行。        | 3    |
| [text-emphasis](http://www.w3school.com.cn/cssref/pr_text-emphasis.asp) | 向元素的文本应用重点标记以及重点标记的前景色。          | 3    |
| [text-justify](http://www.w3school.com.cn/cssref/pr_text-justify.asp) | 规定当 text-align 设置为 "justify" 时所使用的对齐方法。 | 3    |
| [text-outline](http://www.w3school.com.cn/cssref/pr_text-outline.asp) | 规定文本的轮廓。                                        | 3    |
| [text-overflow](http://www.w3school.com.cn/cssref/pr_text-overflow.asp) | 规定当文本溢出包含元素时发生的事情。                    | 3    |
| [text-shadow](http://www.w3school.com.cn/cssref/pr_text-shadow.asp) | 向文本添加阴影。                                        | 3    |
| [text-wrap](http://www.w3school.com.cn/cssref/pr_text-wrap.asp) | 规定文本的换行规则。                                    | 3    |
| [word-break](http://www.w3school.com.cn/cssref/pr_word-break.asp) | 规定非中日韩文本的换行规则。                            | 3    |
| [word-wrap](http://www.w3school.com.cn/cssref/pr_word-wrap.asp) | 允许对长的不可分割的单词进行分割并换行到下一行。        | 3    |

## 2D/3D 转换属性（Transform）

| 属性                                                         | 描述                                 | CSS  |
| ------------------------------------------------------------ | ------------------------------------ | ---- |
| [transform](http://www.w3school.com.cn/cssref/pr_transform.asp) | 向元素应用 2D 或 3D 转换。           | 3    |
| [transform-origin](http://www.w3school.com.cn/cssref/pr_transform-origin.asp) | 允许你改变被转换元素的位置。         | 3    |
| [transform-style](http://www.w3school.com.cn/cssref/pr_transform-style.asp) | 规定被嵌套元素如何在 3D 空间中显示。 | 3    |
| [perspective](http://www.w3school.com.cn/cssref/pr_perspective.asp) | 规定 3D 元素的透视效果。             | 3    |
| [perspective-origin](http://www.w3school.com.cn/cssref/pr_perspective-origin.asp) | 规定 3D 元素的底部位置。             | 3    |
| [backface-visibility](http://www.w3school.com.cn/cssref/pr_backface-visibility.asp) | 定义元素在不面对屏幕时是否可见。     | 3    |

## 过渡属性（Transition）

| 属性                                                         | 描述                                         | CSS  |
| ------------------------------------------------------------ | -------------------------------------------- | ---- |
| [transition](http://www.w3school.com.cn/cssref/pr_transition.asp) | 简写属性，用于在一个属性中设置四个过渡属性。 | 3    |
| [transition-property](http://www.w3school.com.cn/cssref/pr_transition-property.asp) | 规定应用过渡的 CSS 属性的名称。              | 3    |
| [transition-duration](http://www.w3school.com.cn/cssref/pr_transition-duration.asp) | 定义过渡效果花费的时间。                     | 3    |
| [transition-timing-function](http://www.w3school.com.cn/cssref/pr_transition-timing-function.asp) | 规定过渡效果的时间曲线。                     | 3    |
| [transition-delay](http://www.w3school.com.cn/cssref/pr_transition-delay.asp) | 规定过渡效果何时开始。                       | 3    |

## 用户界面属性（User-interface）

| 属性                                                         | 描述                                               | CSS  |
| ------------------------------------------------------------ | -------------------------------------------------- | ---- |
| [appearance](http://www.w3school.com.cn/cssref/pr_appearance.asp) | 允许您将元素设置为标准用户界面元素的外观           | 3    |
| [box-sizing](http://www.w3school.com.cn/cssref/pr_box-sizing.asp) | 允许您以确切的方式定义适应某个区域的具体内容。     | 3    |
| [icon](http://www.w3school.com.cn/cssref/pr_icon.asp)        | 为创作者提供使用图标化等价物来设置元素样式的能力。 | 3    |
| [nav-down](http://www.w3school.com.cn/cssref/pr_nav-down.asp) | 规定在使用 arrow-down 导航键时向何处导航。         | 3    |
| [nav-index](http://www.w3school.com.cn/cssref/pr_nav-index.asp) | 设置元素的 tab 键控制次序。                        | 3    |
| [nav-left](http://www.w3school.com.cn/cssref/pr_nav-left.asp) | 规定在使用 arrow-left 导航键时向何处导航。         | 3    |
| [nav-right](http://www.w3school.com.cn/cssref/pr_nav-right.asp) | 规定在使用 arrow-right 导航键时向何处导航。        | 3    |
| [nav-up](http://www.w3school.com.cn/cssref/pr_nav-up.asp)    | 规定在使用 arrow-up 导航键时向何处导航。           | 3    |
| [outline-offset](http://www.w3school.com.cn/cssref/pr_outline-offset.asp) | 对轮廓进行偏移，并在超出边框边缘的位置绘制轮廓。   | 3    |
| [resize](http://www.w3school.com.cn/cssref/pr_resize.asp)    | 规定是否可由用户对元素的尺寸进行调整。             | 3    |