

# JavaScript 入门

## JavaScript 简介



**JavaScript 是世界上最流行的编程语言。**

**这门语言可用于 HTML 和 web，更可广泛用于服务器、PC、笔记本电脑、平板电脑和智能手机等设备。**

### JavaScript 是脚本语言

JavaScript 是一种轻量级的编程语言。

JavaScript 是可插入 HTML 页面的编程代码。

JavaScript 插入 HTML 页面后，可由所有的现代浏览器执行。

JavaScript 很容易学习。

### 您将学到什么

下面是您将在本教程中学到的主要内容。

### JavaScript：写入 HTML 输出

### 实例

```
document.write("<h1>This is a heading</h1>");
document.write("<p>This is a paragraph</p>");
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_intro_document_write)

提示：您只能在 HTML 输出中使用 document.write。如果您在文档加载后使用该方法，会覆盖整个文档。

### JavaScript：对事件作出反应

**实例**

```
<button type="button" onclick="alert('Welcome!')">点击这里</button>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_intro_alert)

alert() 函数在 JavaScript 中并不常用，但它对于代码测试非常方便。

onclick 事件只是您即将在本教程中学到的众多事件之一。

### JavaScript：改变 HTML 内容

使用 JavaScript 来处理 HTML 内容是非常强大的功能。

### 实例

```
x=document.getElementById("demo")  //查找元素
x.innerHTML="Hello JavaScript";    //改变内容
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_intro_inner_html)

您会经常看到 document.getElementByID("*some id*")。这个方法是 HTML DOM 中定义的。

DOM（文档对象模型）是用以访问 HTML 元素的正式 W3C 标准。

您将在本教程的多个章节中学到有关 HTML DOM 的知识。

### JavaScript：改变 HTML 图像

本例会动态地改变 HTML <image> 的来源 (src)：

The Light bulb

点击灯泡就可以打开或关闭这盏灯

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_lightbulb)

JavaScript 能够改变任意 HTML 元素的大多数属性，而不仅仅是图片。

### JavaScript：改变 HTML 样式

改变 HTML 元素的样式，属于改变 HTML 属性的变种。

**实例**

```
x=document.getElementById("demo")  //找到元素
x.style.color="#ff0000";           //改变样式
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_intro_style)

### JavaScript：验证输入

JavaScript 常用于验证用户的输入。

**实例**

```
if isNaN(x) {alert("Not Numeric")};
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_intro_validate)

### 您知道吗？

提示：JavaScript 与 Java 是两种完全不同的语言，无论在概念还是设计上。

Java（由 Sun 发明）是更复杂的编程语言。

ECMA-262 是 JavaScript 标准的官方名称。

JavaScript 由 Brendan Eich 发明。它于 1995 年出现在 Netscape 中（该浏览器已停止更新），并于 1997 年被 ECMA（一个标准协会）采纳。

## JavaScript 使用

**HTML 中的脚本必须位于 <script> 与 </script> 标签之间。**

**脚本可被放置在 HTML 页面的 <body> 和 <head> 部分中。**

### script 标签

如需在 HTML 页面中插入 JavaScript，请使用 <script> 标签。

<script> 和 </script> 会告诉 JavaScript 在何处开始和结束。

<script> 和 </script> 之间的代码行包含了 JavaScript：

```
<script>
alert("My First JavaScript");
</script>
```

您无需理解上面的代码。只需明白，浏览器会解释并执行位于 <script> 和 </script> 之间的 JavaScript。

那些老旧的实例可能会在 <script> 标签中使用 type="text/javascript"。现在已经不必这样做了。JavaScript 是所有现代浏览器以及 HTML5 中的默认脚本语言。

### body中的 JavaScript

在本例中，JavaScript 会在页面加载时向 HTML 的 <body> 写文本：

**实例**

```
<!DOCTYPE html>
<html>
<body>
.
.
<script>
document.write("<h1>This is a heading</h1>");
document.write("<p>This is a paragraph</p>");
</script>
.
.
</body>
</html>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_intro_document_write)

### JavaScript 函数和事件

上面例子中的 JavaScript 语句，会在页面加载时执行。

通常，我们需要在某个事件发生时执行代码，比如当用户点击按钮时。

如果我们把 JavaScript 代码放入函数中，就可以在事件发生时调用该函数。

您将在稍后的章节学到更多有关 JavaScript 函数和事件的知识。

### head 或 body 中的 JavaScript

您可以在 HTML 文档中放入不限数量的脚本。

脚本可位于 HTML 的 <body> 或 <head> 部分中，或者同时存在于两个部分中。

通常的做法是把函数放入 <head> 部分中，或者放在页面底部。这样就可以把它们安置到同一处位置，不会干扰页面的内容。

### head中的 JavaScript 函数

在本例中，我们把一个 JavaScript 函数放置到 HTML 页面的 <head> 部分。

该函数会在点击按钮时被调用：

**实例**

```
<!DOCTYPE html>
<html>

<head>
<script>
function myFunction()
{
document.getElementById("demo").innerHTML="My First JavaScript Function";
}
</script>
</head>

<body>

<h1>My Web Page</h1>

<p id="demo">A Paragraph</p>

<button type="button" onclick="myFunction()">Try it</button>

</body>
</html>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_whereto_head)

### body 中的 JavaScript 函数

在本例中，我们把一个 JavaScript 函数放置到 HTML 页面的 <body> 部分。

该函数会在点击按钮时被调用：

**实例**

```
<!DOCTYPE html>
<html>
<body>

<h1>My Web Page</h1>

<p id="demo">A Paragraph</p>

<button type="button" onclick="myFunction()">Try it</button>

<script>
function myFunction()
{
document.getElementById("demo").innerHTML="My First JavaScript Function";
}
</script>

</body>
</html>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_whereto_body)

提示：我们把 JavaScript 放到了页面代码的底部，这样就可以确保在 <p> 元素创建之后再执行脚本。

### 外部的 JavaScript

也可以把脚本保存到外部文件中。外部文件通常包含被多个网页使用的代码。

外部 JavaScript 文件的文件扩展名是 .js。

如需使用外部文件，请在 <script> 标签的 "src" 属性中设置该 .js 文件：

**实例**

```
<!DOCTYPE html>
<html>
<body>
<script src="myScript.js"></script>
</body>
</html>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_externalexample)

在 <head> 或 <body> 中引用脚本文件都是可以的。实际运行效果与您在 <script> 标签中编写脚本完全一致。

提示：外部脚本不能包含 <script> 标签。

## JavaScript 输出



**JavaScript 通常用于操作 HTML 元素。**

### 操作 HTML 元素

如需从 JavaScript 访问某个 HTML 元素，您可以使用 document.getElementById(*id*) 方法。

请使用 "id" 属性来标识 HTML 元素：

**例子**

通过指定的 id 来访问 HTML 元素，并改变其内容：

```
<!DOCTYPE html>
<html>
<body>

<h1>我的第一张网页</h1>

<p id="demo">我的第一个段落</p>

<script>
document.getElementById("demo").innerHTML="我的第一段 JavaScript";
</script>

</body>
</html>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_dom)

JavaScript 由 web 浏览器来执行。在这种情况下，浏览器将访问 id="demo" 的 HTML 元素，并把它的内容（innerHTML）替换为 "My First JavaScript"。

### 写到文档输出

下面的例子直接把 <p> 元素写到 HTML 文档输出中：

**实例**

```
<!DOCTYPE html>
<html>
<body>

<h1>我的第一张网页</h1>

<script>
document.write("<p>我的第一段 JavaScript</p>");
</script>

</body>
</html>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_write)

### 警告

请使用 document.write() 仅仅向文档输出写内容。

如果在文档已完成加载后执行 document.write，整个 HTML 页面将被覆盖：

**实例**

```
<!DOCTYPE html>
<html>
<body>

<h1>我的第一张网页</h1>

<p>我的第一个段落。</p>

<button onclick="myFunction()">点击这里</button>

<script>
function myFunction()
{
document.write("糟糕！文档消失了。");
}
</script>

</body>
</html>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_write_over)

### Windows 8 中的 JavaScript

提示：微软支持通过 JavaScript 创建 Windows 8 app。

对于因特网和视窗操作系统，JavaScript 都意味着未来。

## JavaScript 语句

**JavaScript 语句**

JavaScript 语句向浏览器发出的命令。语句的作用是告诉浏览器该做什么。

下面的 JavaScript 语句向 id="demo" 的 HTML 元素输出文本 "Hello World"：

```
document.getElementById("demo").innerHTML="Hello World";
```

### 分号 ;

分号用于分隔 JavaScript 语句。

通常我们在每条可执行的语句结尾添加分号。

使用分号的另一用处是在一行中编写多条语句。

提示：您也可能看到不带有分号的案例。

在 JavaScript 中，用分号来结束语句是可选的。

### JavaScript 代码

JavaScript 代码（或者只有 JavaScript）是 JavaScript 语句的序列。

浏览器会按照编写顺序来执行每条语句。

本例将操作两个 HTML 元素：

**实例**

```
document.getElementById("demo").innerHTML="Hello World";
document.getElementById("myDIV").innerHTML="How are you?";
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_statements)

### JavaScript 代码块

JavaScript 语句通过代码块的形式进行组合。

块由左花括号开始，由右花括号结束。

块的作用是使语句序列一起执行。

JavaScript 函数是将语句组合在块中的典型例子。

下面的例子将运行可操作两个 HTML 元素的函数：

**实例**

```
function myFunction()
{
document.getElementById("demo").innerHTML="Hello World";
document.getElementById("myDIV").innerHTML="How are you?";
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_blocks)

您将在稍后的章节学到更多有关函数的知识。

### JavaScript 对大小写敏感。

JavaScript 对大小写是敏感的。

当编写 JavaScript 语句时，请留意是否关闭大小写切换键。

函数 getElementById 与 getElementbyID 是不同的。

同样，变量 myVariable 与 MyVariable 也是不同的。

### 空格

JavaScript 会忽略多余的空格。您可以向脚本添加空格，来提高其可读性。下面的两行代码是等效的：

```
var name="Hello";
var name = "Hello";
```

### 对代码行进行折行

您可以在文本字符串中使用反斜杠对代码行进行换行。下面的例子会正确地显示：

```
document.write("Hello \
World!");
```

不过，您不能像这样折行：

```
document.write \
("Hello World!");
```

### 您知道吗？

提示：JavaScript 是脚本语言。浏览器会在读取代码时，逐行地执行脚本代码。而对于传统编程来说，会在执行前对所有代码进行编译。

## JavaScript 注释



**JavaScript 注释可用于提高代码的可读性。**

### JavaScript 注释

JavaScript 不会执行注释。

我们可以添加注释来对 JavaScript 进行解释，或者提高代码的可读性。

单行注释以 // 开头。

**例子**

下面的例子使用单行注释来解释代码：

```
// 输出标题：
document.getElementById("myH1").innerHTML="Welcome to my Homepage";
// 输出段落：
document.getElementById("myP").innerHTML="This is my first paragraph.";
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_comments1)

### JavaScript 多行注释

多行注释以 /* 开始，以 */ 结尾。

下面的例子使用多行注释来解释代码：

**例子**

```
/*
下面的这些代码会输出
一个标题和一个段落
并将代表主页的开始
*/
document.getElementById("myH1").innerHTML="Welcome to my Homepage";
document.getElementById("myP").innerHTML="This is my first paragraph.";
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_comments2)

### 使用注释来阻止执行

**例子 1**

在下面的例子中，注释用于阻止其中一条代码行的执行（可用于调试）：

```
//document.getElementById("myH1").innerHTML="Welcome to my Homepage";
document.getElementById("myP").innerHTML="This is my first paragraph.";
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_comments3)

**例子 2**

在下面的例子中，注释用于阻止代码块的执行（可用于调试）：

```
/*
document.getElementById("myH1").innerHTML="Welcome to my Homepage";
document.getElementById("myP").innerHTML="This is my first paragraph.";
*/
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_comments4)

### 在行末使用注释

在下面的例子中，我们把注释放到代码行的结尾处：

**例子**

```
var x=5;    // 声明 x 并把 5 赋值给它
var y=x+2;  // 声明 y 并把 x+2 赋值给它
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_comments5)




##   JavaScript 变量

**变量是存储信息的容器。**

**实例**

```
var x=2;
var y=3;
var z=x+y;
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_data1)

### 就像代数那样

```
x=2
y=3
z=x+y
```

在代数中，我们使用字母（比如 x）来保存值（比如 2）。

通过上面的表达式 z=x+y，我们能够计算出 z 的值为 5。

在 JavaScript 中，这些字母被称为变量。

提示：您可以把变量看做存储数据的容器。

### JavaScript 变量

与代数一样，JavaScript 变量可用于存放值（比如 x=2）和表达式（比如 z=x+y）。

变量可以使用短名称（比如 x 和 y），也可以使用描述性更好的名称（比如 age, sum, totalvolume）。

- 变量必须以字母开头
- 变量也能以 $ 和 _ 符号开头（不过我们不推荐这么做）
- 变量名称对大小写敏感（y 和 Y 是不同的变量）

提示：JavaScript 语句和 JavaScript 变量都对大小写敏感。

## JavaScript 数据类型

JavaScript 变量还能保存其他数据类型，比如文本值 (name="Bill Gates")。

在 JavaScript 中，类似 "Bill Gates" 这样一条文本被称为字符串。

JavaScript 变量有很多种类型，但是现在，我们只关注数字和字符串。

当您向变量分配文本值时，应该用双引号或单引号包围这个值。

当您向变量赋的值是数值时，不要使用引号。如果您用引号包围数值，该值会被作为文本来处理。

**例子**

```
var pi=3.14;
var name="Bill Gates";
var answer='Yes I am!';
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_data2)

### 声明（创建） JavaScript 变量

在 JavaScript 中创建变量通常称为“声明”变量。

我们使用 var 关键词来声明变量：

```
var carname;
```

变量声明之后，该变量是空的（它没有值）。

如需向变量赋值，请使用等号：

```
carname="Volvo";
```

不过，您也可以在声明变量时对其赋值：

```
var carname="Volvo";
```

**例子**

在下面的例子中，我们创建了名为 carname 的变量，并向其赋值 "Volvo"，然后把它放入 id="demo" 的 HTML 段落中：

```
<p id="demo"></p>
var carname="Volvo";
document.getElementById("demo").innerHTML=carname;
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_variables1)

提示：一个好的编程习惯是，在代码开始处，统一对需要的变量进行声明。

### 一条语句，多个变量

您可以在一条语句中声明很多变量。该语句以 var 开头，并使用逗号分隔变量即可：

```
var name="Gates", age=56, job="CEO";
```

声明也可横跨多行：

```
var name="Gates",
age=56,
job="CEO";
```

### Value = undefined

在计算机程序中，经常会声明无值的变量。未使用值来声明的变量，其值实际上是 undefined。

在执行过以下语句后，变量 carname 的值将是 undefined：

```
var carname;
```

### 重新声明 JavaScript 变量

如果重新声明 JavaScript 变量，该变量的值不会丢失：

在以下两条语句执行后，变量 carname 的值依然是 "Volvo"：

```
var carname="Volvo";
var carname;
```

### JavaScript 算数

您可以通过 JavaScript 变量来做算数，使用的是 = 和 + 这类运算符：

**例子**

```
y=5;
x=y+2;
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_oper_add)

您将在本教程稍后的章节学到更多有关 JavaScript 运算符的知识。

## JavaScript 数据类型



**字符串、数字、布尔、数组、对象、Null、Undefined**

### JavaScript 拥有动态类型

JavaScript 拥有动态类型。这意味着相同的变量可用作不同的类型：

**实例**

```
var x                // x 为 undefined
var x = 6;           // x 为数字
var x = "Bill";      // x 为字符串
```

### JavaScript 字符串

字符串是存储字符（比如 "Bill Gates"）的变量。

字符串可以是引号中的任意文本。您可以使用单引号或双引号：

**实例**

```
var carname="Bill Gates";
var carname='Bill Gates';
```

您可以在字符串中使用引号，只要不匹配包围字符串的引号即可：

**实例**

```
var answer="Nice to meet you!";
var answer="He is called 'Bill'";
var answer='He is called "Bill"';
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_datatypes_string)

您将在本教程的高级部分学到更多关于字符串的知识。

### JavaScript 数字

JavaScript 只有一种数字类型。数字可以带小数点，也可以不带：

**实例**

```
var x1=34.00;      //使用小数点来写
var x2=34;         //不使用小数点来写
```

极大或极小的数字可以通过科学（指数）计数法来书写：

**实例**

```
var y=123e5;      // 12300000
var z=123e-5;     // 0.00123
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_numbers)

您将在本教程的高级部分学到更多关于数字的知识。

### JavaScript 布尔

布尔（逻辑）只能有两个值：true 或 false。

```
var x=true
var y=false
```

布尔常用在条件测试中。您将在本教程稍后的章节中学到更多关于条件测试的知识。

### JavaScript 数组

下面的代码创建名为 cars 的数组：

```
var cars=new Array();
cars[0]="Audi";
cars[1]="BMW";
cars[2]="Volvo";
```

或者 (condensed array):

```
var cars=new Array("Audi","BMW","Volvo");
```

或者 (literal array):

**实例**

```
var cars=["Audi","BMW","Volvo"];
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_datatypes_array)

数组下标是基于零的，所以第一个项目是 [0]，第二个是 [1]，以此类推。

您将在本教程稍后的章节中学到更多关于数组的知识。

### JavaScript 对象

对象由花括号分隔。在括号内部，对象的属性以名称和值对的形式 (name : value) 来定义。属性由逗号分隔：

```
var person={firstname:"Bill", lastname:"Gates", id:5566};
```

上面例子中的对象 (person) 有三个属性：firstname、lastname 以及 id。

空格和折行无关紧要。声明可横跨多行：

```
var person={
firstname : "Bill",
lastname  : "Gates",
id        :  5566
};
```

对象属性有两种寻址方式：

**实例**

```
name=person.lastname;
name=person["lastname"];
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_datatypes_object)

您将在本教程稍后的章节中学到更多关于对象的知识。

### Undefined 和 Null

Undefined 这个值表示变量不含有值。

可以通过将变量的值设置为 null 来清空变量。

**实例**

```
cars=null;
person=null;
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_undefined)

### 声明变量类型

当您声明新变量时，可以使用关键词 "new" 来声明其类型：

```
var carname=new String;
var x=      new Number;
var y=      new Boolean;
var cars=   new Array;
var person= new Object;
```

JavaScript 变量均为对象。当您声明一个变量时，就创建了一个新的对象。



## JavaScript 对象



**JavaScript 中的所有事物都是对象：字符串、数字、数组、日期，等等。**

**在 JavaScript 中，对象是拥有属性和方法的数据。**

### 属性和方法

属性是与对象相关的值。

方法是能够在对象上执行的动作。

举例：汽车就是现实生活中的对象。

汽车的属性：

```
car.name=Fiat

car.model=500

car.weight=850kg

car.color=white 
```

汽车的方法：

```
car.start()

car.drive()

car.brake()
```

汽车的属性包括名称、型号、重量、颜色等。

所有汽车都有这些属性，但是每款车的属性都不尽相同。

汽车的方法可以是启动、驾驶、刹车等。

所有汽车都拥有这些方法，但是它们被执行的时间都不尽相同。

### JavaScript 中的对象

在 JavaScript 中，对象是数据（变量），拥有属性和方法。

当您像这样声明一个 JavaScript 变量时：

```
var txt = "Hello";
```

您实际上已经创建了一个 JavaScript 字符串对象。字符串对象拥有内建的属性 length。对于上面的字符串来说，length 的值是 5。字符串对象同时拥有若干个内建的方法。

属性：

```
txt.length=5
```

方法：

```
txt.indexOf()

txt.replace()

txt.search()
```

提示：在面向对象的语言中，属性和方法常被称为对象的成员。

在本教程稍后的章节中，您将学到有关字符串对象的更多属性和方法。

### 创建 JavaScript 对象

JavaScript 中的几乎所有事务都是对象：字符串、数字、数组、日期、函数，等等。

你也可以创建自己的对象。

本例创建名为 "person" 的对象，并为其添加了四个属性：

**实例**

```
person=new Object();
person.firstname="Bill";
person.lastname="Gates";
person.age=56;
person.eyecolor="blue";
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_create_object)

创建新 JavaScript 对象有很多不同的方法，并且您还可以向已存在的对象添加属性和方法。

您将在本教程稍后的章节学到更多相关的内容。

### 访问对象的属性

访问对象属性的语法是：

```
objectName.propertyName
```

本例使用 String 对象的 length 属性来查找字符串的长度：

```
var message="Hello World!";
var x=message.length;
```

在以上代码执行后，x 的值是：

```
12
```

### 访问对象的方法

您可以通过下面的语法调用方法：

```
objectName.methodName()
```

这个例子使用 String 对象的 toUpperCase() 方法来把文本转换为大写：

```
var message="Hello world!";
var x=message.toUpperCase();
```

在以上代码执行后，x 的值是：

```
HELLO WORLD!
```

### 您知道吗？

提示：在面向对象的语言中，使用 camel-case 标记法的函数是很常见的。您会经常看到 someMethod() 这样的函数名，而不是 some_method()。

##   JavaScript 函数



**函数是由事件驱动的或者当它被调用时执行的可重复使用的代码块。**

**实例**

```
<!DOCTYPE html>
<html>
<head>
<script>
function myFunction()
{
alert("Hello World!");
}
</script>
</head>

<body>
<button onclick="myFunction()">点击这里</button>
</body>
</html>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_function1)

### JavaScript 函数语法

函数就是包裹在花括号中的代码块，前面使用了关键词 function：

```
function functionname()
{
这里是要执行的代码
}
```

当调用该函数时，会执行函数内的代码。

可以在某事件发生时直接调用函数（比如当用户点击按钮时），并且可由 JavaScript 在任何位置进行调用。

提示：JavaScript 对大小写敏感。关键词 function 必须是小写的，并且必须以与函数名称相同的大小写来调用函数。

### 调用带参数的函数

在调用函数时，您可以向其传递值，这些值被称为参数。

这些参数可以在函数中使用。

您可以发送任意多的参数，由逗号 (,) 分隔：

```
myFunction(argument1,argument2)
```

当您声明函数时，请把参数作为变量来声明：

```
function myFunction(var1,var2)
{
这里是要执行的代码
}
```

变量和参数必须以一致的顺序出现。第一个变量就是第一个被传递的参数的给定的值，以此类推。

**实例**

```
<button onclick="myFunction('Bill Gates','CEO')">点击这里</button>

<script>
function myFunction(name,job)
{
alert("Welcome " + name + ", the " + job);
}
</script>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_function2)

上面的函数会当按钮被点击时提示 "Welcome Bill Gates, the CEO"。

函数很灵活，您可以使用不同的参数来调用该函数，这样就会给出不同的消息：

**实例**

```
<button onclick="myFunction('Harry Potter','Wizard')">点击这里</button>
<button onclick="myFunction('Bob','Builder')">点击这里</button>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_function3)

根据您点击的不同的按钮，上面的例子会提示 "Welcome Harry Potter, the Wizard" 或 "Welcome Bob, the Builder"。

### 带有返回值的函数

有时，我们会希望函数将值返回调用它的地方。

通过使用 return 语句就可以实现。

在使用 return 语句时，函数会停止执行，并返回指定的值。

### 语法

```
function myFunction()
{
var x=5;
return x;
}
```

上面的函数会返回值 5。

注释：整个 JavaScript 并不会停止执行，仅仅是函数。JavaScript 将继续执行代码，从调用函数的地方。

函数调用将被返回值取代：

```
var myVar=myFunction();
```

myVar 变量的值是 5，也就是函数 "myFunction()" 所返回的值。

即使不把它保存为变量，您也可以使用返回值：

```
document.getElementById("demo").innerHTML=myFunction();
```

"demo" 元素的 innerHTML 将成为 5，也就是函数 "myFunction()" 所返回的值。

您可以使返回值基于传递到函数中的参数：

**实例**

计算两个数字的乘积，并返回结果：

```
function myFunction(a,b)
{
return a*b;
}

document.getElementById("demo").innerHTML=myFunction(4,3);
```

"demo" 元素的 innerHTML 将是：

```
12
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_function_return)

在您仅仅希望退出函数时 ，也可使用 return 语句。返回值是可选的：

```
function myFunction(a,b)
{
if (a>b)
  {
  return;
  }
x=a+b
}
```

如果 a 大于 b，则上面的代码将退出函数，并不会计算 a 和 b 的总和。

### 局部 JavaScript 变量

在 JavaScript 函数内部声明的变量（使用 var）是*局部*变量，所以只能在函数内部访问它。（该变量的作用域是局部的）。

您可以在不同的函数中使用名称相同的局部变量，因为只有声明过该变量的函数才能识别出该变量。

只要函数运行完毕，本地变量就会被删除。

### 全局 JavaScript 变量

在函数外声明的变量是*全局*变量，网页上的所有脚本和函数都能访问它。

### JavaScript 变量的生存期

JavaScript 变量的生命期从它们被声明的时间开始。

局部变量会在函数运行以后被删除。

全局变量会在页面关闭后被删除。

### 向未声明的 JavaScript 变量来分配值

如果您把值赋给尚未声明的变量，该变量将被自动作为全局变量声明。

这条语句：

```
carname="Volvo";
```

将声明一个*全局*变量 carname，即使它在函数内执行。

## JavaScript 运算符



**运算符 = 用于赋值。**

**运算符 + 用于加值。**

运算符 = 用于给 JavaScript 变量赋值。

算术运算符 + 用于把值加起来。

```
y=5;
z=2;
x=y+z; 
```

在以上语句执行后，x 的值是 7。

### JavaScript 算术运算符

算术运算符用于执行变量与/或值之间的算术运算。

给定 *y=5*，下面的表格解释了这些算术运算符：

| 运算符 | 描述              | 例子  | 结果  |
| ------ | ----------------- | ----- | ----- |
| +      | 加                | x=y+2 | x=7   |
| -      | 减                | x=y-2 | x=3   |
| *      | 乘                | x=y*2 | x=10  |
| /      | 除                | x=y/2 | x=2.5 |
| %      | 求余数 (保留整数) | x=y%2 | x=1   |
| ++     | 累加              | x=++y | x=6   |
| --     | 递减              | x=--y | x=4   |

### JavaScript 赋值运算符

赋值运算符用于给 JavaScript 变量赋值。

给定 *x=10* 和 *y=5*，下面的表格解释了赋值运算符：

| 运算符 | 例子 | 等价于 | 结果 |
| ------ | ---- | ------ | ---- |
| =      | x=y  |        | x=5  |
| +=     | x+=y | x=x+y  | x=15 |
| -=     | x-=y | x=x-y  | x=5  |
| *=     | x*=y | x=x*y  | x=50 |
| /=     | x/=y | x=x/y  | x=2  |
| %=     | x%=y | x=x%y  | x=0  |

### 用于字符串的 + 运算符

\+ 运算符用于把文本值或字符串变量加起来（连接起来）。

如需把两个或多个字符串变量连接起来，请使用 + 运算符。

```
txt1="What a very";
txt2="nice day";
txt3=txt1+txt2;
```

在以上语句执行后，变量 txt3 包含的值是 "What a verynice day"。

要想在两个字符串之间增加空格，需要把空格插入一个字符串之中：

```
txt1="What a very ";
txt2="nice day";
txt3=txt1+txt2;
```

或者把空格插入表达式中：

```
txt1="What a very";
txt2="nice day";
txt3=txt1+" "+txt2;
```

在以上语句执行后，变量 txt3 包含的值是：

"What a very nice day"

### 对字符串和数字进行加法运算

请看这些例子：

```
x=5+5;
document.write(x);

x="5"+"5";
document.write(x);

x=5+"5";
document.write(x);

x="5"+5;
document.write(x);
```

[TIY](http://www.w3school.com.cn/tiy/t.asp?f=jseg_variables)

### 规则是：

**如果把数字与字符串相加，结果将成为字符串。**

## JavaScript 比较和逻辑运算符



**比较和逻辑运算符用于测试 true 或 false。**

### 比较运算符

比较运算符在逻辑语句中使用，以测定变量或值是否相等。

给定 x=5，下面的表格解释了比较运算符：

| 运算符 | 描述             | 例子                            |
| ------ | ---------------- | ------------------------------- |
| ==     | 等于             | x==8 为 false                   |
| ===    | 全等（值和类型） | x===5 为 true；x==="5" 为 false |
| !=     | 不等于           | x!=8 为 true                    |
| >      | 大于             | x>8 为 false                    |
| <      | 小于             | x<8 为 true                     |
| >=     | 大于或等于       | x>=8 为 false                   |
| <=     | 小于或等于       | x<=8 为 true                    |

### 如何使用

可以在条件语句中使用比较运算符对值进行比较，然后根据结果来采取行动：

```
if (age<18) document.write("Too young");
```

您将在本教程的下一节中学习更多有关条件语句的知识。

### 逻辑运算符

逻辑运算符用于测定变量或值之间的逻辑。

给定 x=6 以及 y=3，下表解释了逻辑运算符：

| 运算符 | 描述 | 例子                      |
| ------ | ---- | ------------------------- |
| &&     | and  | (x < 10 && y > 1) 为 true |
| \|\|   | or   | (x==5 \|\| y==5) 为 false |
| !      | not  | !(x==y) 为 true           |

### 条件运算符

JavaScript 还包含了基于某些条件对变量进行赋值的条件运算符。

### 语法

```
variablename=(condition)?value1:value2 
```

**例子**

```
greeting=(visitor=="PRES")?"Dear President ":"Dear ";
```

如果变量 visitor 中的值是 "PRES"，则向变量 greeting 赋值 "Dear President "，否则赋值 "Dear"。

## JavaScript If...Else 语句



**条件语句用于基于不同的条件来执行不同的动作。**

### 条件语句

通常在写代码时，您总是需要为不同的决定来执行不同的动作。您可以在代码中使用条件语句来完成该任务。

在 JavaScript 中，我们可使用以下条件语句：

- *if 语句* - 只有当指定条件为 true 时，使用该语句来执行代码
- *if...else 语句* - 当条件为 true 时执行代码，当条件为 false 时执行其他代码
- *if...else if....else 语句* - 使用该语句来选择多个代码块之一来执行
- *switch 语句* - 使用该语句来选择多个代码块之一来执行

### If 语句

只有当指定条件为 true 时，该语句才会执行代码。

### 语法

```
if (条件)
  {
  只有当条件为 true 时执行的代码
  }
```

注意：请使用小写的 if。使用大写字母（IF）会生成 JavaScript 错误！

**实例**

当时间小于 20:00 时，生成一个“Good day”问候：

```
if (time<20)
  {
  x="Good day";
  }
```

x 的结果是：

```
Good day
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_ifthen)

请注意，在这个语法中，没有 ..else..。您已经告诉浏览器只有在指定条件为 true 时才执行代码。

### If...else 语句

请使用 if....else 语句在条件为 true 时执行代码，在条件为 false 时执行其他代码。

### 语法

```
if (条件)
  {
  当条件为 true 时执行的代码
  }
else
  {
  当条件不为 true 时执行的代码
  }
```

**实例**

当时间小于 20:00 时，将得到问候 "Good day"，否则将得到问候 "Good evening"。

```
if (time<20)
  {
  x="Good day";
  }
else
  {
  x="Good evening";
  }
```

x 的结果是：

```
Good day
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_ifthenelse)

### If...else if...else 语句

使用 if....else if...else 语句来选择多个代码块之一来执行。

### 语法

```
if (条件 1)
  {
  当条件 1 为 true 时执行的代码
  }
else if (条件 2)
  {
  当条件 2 为 true 时执行的代码
  }
else
  {
  当条件 1 和 条件 2 都不为 true 时执行的代码
  }
```

**实例**

如果时间小于 10:00，则将发送问候 "Good morning"，否则如果时间小于 20:00，则发送问候 "Good day"，否则发送问候 "Good evening"：

```
if (time<10)
  {
  x="Good morning";
  }
else if (time<20)
  {
  x="Good day";
  }
else
  {
  x="Good evening";
  }
```

x 的结果是：

```
Good day
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_elseif)

### 更多实例

- 随机的链接

  本例将输出 W3School 或微软公司的链接。通过使用随机数，每个链接被输出的机会为 50%。

## JavaScript Switch 语句



**switch 语句用于基于不同的条件来执行不同的动作。**

### JavaScript Switch 语句

请使用 switch 语句来选择要执行的多个代码块之一。

### 语法

```
switch(n)
{
case 1:
  执行代码块 1
  break;
case 2:
  执行代码块 2
  break;
default:
  n 与 case 1 和 case 2 不同时执行的代码
}
```

工作原理：首先设置表达式 n（通常是一个变量）。随后表达式的值会与结构中的每个 case 的值做比较。如果存在匹配，则与该 case 关联的代码块会被执行。请使用 *break* 来阻止代码自动地向下一个 case 运行。

**实例**

显示今日的周名称。请注意 Sunday=0, Monday=1, Tuesday=2, 等等：

```
var day=new Date().getDay();
switch (day)
{
case 0:
  x="Today it's Sunday";
  break;
case 1:
  x="Today it's Monday";
  break;
case 2:
  x="Today it's Tuesday";
  break;
case 3:
  x="Today it's Wednesday";
  break;
case 4:
  x="Today it's Thursday";
  break;
case 5:
  x="Today it's Friday";
  break;
case 6:
  x="Today it's Saturday";
  break;
}
```

x 的结果：

```
Today it's Monday
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_switch)

### default 关键词

请使用 default 关键词来规定匹配不存在时做的事情：

**实例**

如果今天不是周六或周日，则会输出默认的消息：

```
var day=new Date().getDay();
switch (day)
{
case 6:
  x="Today it's Saturday";
  break;
case 0:
  x="Today it's Sunday";
  break;
default:
  x="Looking forward to the Weekend";
}
```

x 的结果：

```
Looking forward to the Weekend
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_switch2)

### JavaScript For 循环



**循环可以将代码块执行指定的次数。**

## JavaScript 循环

如果您希望一遍又一遍地运行相同的代码，并且每次的值都不同，那么使用循环是很方便的。

我们可以这样输出数组的值：

```
document.write(cars[0] + "<br>");
document.write(cars[1] + "<br>");
document.write(cars[2] + "<br>");
document.write(cars[3] + "<br>");
document.write(cars[4] + "<br>");
document.write(cars[5] + "<br>");
```

不过通常我们这样写：

```
for (var i=0;i<cars.length;i++)
{
document.write(cars[i] + "<br>");
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_loop_for)

### 不同类型的循环

JavaScript 支持不同类型的循环：

- *for* - 循环代码块一定的次数
- *for/in* - 循环遍历对象的属性
- *while* - 当指定的条件为 true 时循环指定的代码块
- *do/while* - 同样当指定的条件为 true 时循环指定的代码块

### For 循环

for 循环是您在希望创建循环时常会用到的工具。

下面是 for 循环的语法：

```
for (语句 1; 语句 2; 语句 3)
  {
  被执行的代码块
  }
```

*语句 1* 在循环（代码块）开始前执行

*语句 2* 定义运行循环（代码块）的条件

*语句 3* 在循环（代码块）已被执行之后执行

**实例**

```
for (var i=0; i<5; i++)
  {
  x=x + "The number is " + i + "<br>";
  }
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_loop_for2)

从上面的例子中，您可以看到：

Statement 1 在循环开始之前设置变量 (var i=0)。

Statement 2 定义循环运行的条件（i 必须小于 5）。

Statement 3 在每次代码块已被执行后增加一个值 (i++)。

#### 语句 1

通常我们会使用语句 1 初始化循环中所用的变量 (var i=0)。

语句 1 是可选的，也就是说不使用语句 1 也可以。

您可以在语句 1 中初始化任意（或者多个）值：

**实例**:

```
for (var i=0,len=cars.length; i<len; i++)
{
document.write(cars[i] + "<br>");
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_loop_for_s1)

同时您还可以省略语句 1（比如在循环开始前已经设置了值时）：

**实例**:

```
var i=2,len=cars.length;
for (; i<len; i++)
{
document.write(cars[i] + "<br>");
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_loop_for_s1_2)

#### 语句 2

通常语句 2 用于评估初始变量的条件。

语句 2 同样是可选的。

如果语句 2 返回 true，则循环再次开始，如果返回 false，则循环将结束。

提示：如果您省略了语句 2，那么必须在循环内提供 *break*。否则循环就无法停下来。这样有可能令浏览器崩溃。请在本教程稍后的章节阅读有关 break 的内容。

#### 语句 3

通常语句 3 会增加初始变量的值。

语句 3 也是可选的。

语句 3 有多种用法。增量可以是负数 (i--)，或者更大 (i=i+15)。

语句 3 也可以省略（比如当循环内部有相应的代码时）：

**实例**:

```
var i=0,len=cars.length;
for (; i<len; )
{
document.write(cars[i] + "<br>");
i++;
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_loop_for_s3)

### For/In 循环

JavaScript for/in 语句循环遍历对象的属性：

**实例**

```
var person={fname:"John",lname:"Doe",age:25};

for (x in person)
  {
  txt=txt + person[x];
  }
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_object_for_in)

您将在有关 JavaScript 对象的章节学到更多有关 for / in 循环的知识。



##   JavaScript While 循环

**只要指定条件为 true，循环就可以一直执行代码。**

### while 循环

While 循环会在指定条件为真时循环执行代码块。

#### 语法

```
while (条件)
  {
  需要执行的代码
  }
```

**实例**

本例中的循环将继续运行，只要变量 i 小于 5：

```
while (i<5)
  {
  x=x + "The number is " + i + "<br>";
  i++;
  }
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_while)

提示：如果您忘记增加条件中所用变量的值，该循环永远不会结束。该可能导致浏览器崩溃。

### do/while 循环

do/while 循环是 while 循环的变体。该循环会执行一次代码块，在检查条件是否为真之前，然后如果条件为真的话，就会重复这个循环。

#### 语法

```
do
  {
  需要执行的代码
  }
while (条件);
```

**实例**

下面的例子使用 do/while 循环。该循环至少会执行一次，即使条件是 false，隐藏代码块会在条件被测试前执行：

```
do
  {
  x=x + "The number is " + i + "<br>";
  i++;
  }
while (i<5);
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_dowhile)

别忘记增加条件中所用变量的值，否则循环永远不会结束！

### 比较 for 和 while

如果您已经阅读了前面那一章关于 for 循环的内容，您会发现 while 循环与 for 循环很像。

### for 语句实例

本例中的循环使用 for 循环来显示 cars 数组中的所有值：

```
cars=["BMW","Volvo","Saab","Ford"];
var i=0;
for (;cars[i];)
{
document.write(cars[i] + "<br>");
i++;
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_loop_for_cars)

### while 语句实例

本例中的循环使用使用 while 循环来显示 cars 数组中的所有值：

```
cars=["BMW","Volvo","Saab","Ford"];
var i=0;
while (cars[i])
{
document.write(cars[i] + "<br>");
i++;
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_loop_while_cars)

##   JavaScript Break 和 Continue 语句

**break 语句用于跳出循环。**

**continue 用于跳过循环中的一个迭代。**

### Break 语句

我们已经在本教程稍早的章节中见到过 break 语句。它用于跳出 switch() 语句。

break 语句可用于跳出循环。

break 语句跳出循环后，会继续执行该循环之后的代码（如果有的话）：

**实例**

```
for (i=0;i<10;i++)
  {
  if (i==3)
    {
    break;
    }
  x=x + "The number is " + i + "<br>";
  }
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_break)

由于这个 if 语句只有一行代码，所以可以省略花括号：

```
for (i=0;i<10;i++)
  {
  if (i==3) break;
  x=x + "The number is " + i + "<br>";
  }
```

### Continue 语句

continue 语句中断循环中的迭代，如果出现了指定的条件，然后继续循环中的下一个迭代。

该例子跳过了值 3：

**实例**

```
for (i=0;i<=10;i++)
 {
 if (i==3) continue;
  x=x + "The number is " + i + "<br>";
  }
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_continue)

### JavaScript 标签

正如您在 switch 语句那一章中看到的，可以对 JavaScript 语句进行标记。

如需标记 JavaScript 语句，请在语句之前加上冒号：

```
label:
语句
```

break 和 continue 语句仅仅是能够跳出代码块的语句。

### 语法

```
break labelname;

continue labelname;
```

continue 语句（带有或不带标签引用）只能用在循环中。

break 语句（不带标签引用），只能用在循环或 switch 中。

通过标签引用，break 语句可用于跳出任何 JavaScript 代码块：

**实例**

```
cars=["BMW","Volvo","Saab","Ford"];
list:
{
document.write(cars[0] + "<br>");
document.write(cars[1] + "<br>");
document.write(cars[2] + "<br>");
break list;
document.write(cars[3] + "<br>");
document.write(cars[4] + "<br>");
document.write(cars[5] + "<br>");
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_break_label)

## JavaScript 错误 - Throw、Try 和 Catch



*try* 语句测试代码块的错误。

*catch* 语句处理错误。

*throw* 语句创建自定义错误。

### 错误一定会发生

当 JavaScript 引擎执行 JavaScript 代码时，会发生各种错误：

可能是语法错误，通常是程序员造成的编码错误或错别字。

可能是拼写错误或语言中缺少的功能（可能由于浏览器差异）。

可能是由于来自服务器或用户的错误输出而导致的错误。

当然，也可能是由于许多其他不可预知的因素。

### JavaScript 抛出错误

当错误发生时，当事情出问题时，JavaScript 引擎通常会停止，并生成一个错误消息。

描述这种情况的技术术语是：JavaScript 将*抛出*一个错误。

### JavaScript 测试和捕捉

*try* 语句允许我们定义在执行时进行错误测试的代码块。

*catch* 语句允许我们定义当 try 代码块发生错误时，所执行的代码块。

JavaScript 语句 *try* 和 *catch* 是成对出现的。

#### 语法

```
try
  {
  //在这里运行代码
  }
catch(err)
  {
  //在这里处理错误
  }
```

**实例**

在下面的例子中，我们故意在 try 块的代码中写了一个错字。

catch 块会捕捉到 try 块中的错误，并执行代码来处理它。

```
<!DOCTYPE html>
<html>
<head>
<script>
var txt="";
function message()
{
try
  {
  adddlert("Welcome guest!");
  }
catch(err)
  {
  txt="There was an error on this page.\n\n";
  txt+="Error description: " + err.message + "\n\n";
  txt+="Click OK to continue.\n\n";
  alert(txt);
  }
}
</script>
</head>

<body>
<input type="button" value="View message" onclick="message()">
</body>

</html>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_try_catch)

### Throw 语句

throw 语句允许我们创建自定义错误。

正确的技术术语是：创建或*抛出异常*（exception）。

如果把 throw 与 try 和 catch 一起使用，那么您能够控制程序流，并生成自定义的错误消息。

#### 语法

```
throw exception
```

异常可以是 JavaScript 字符串、数字、逻辑值或对象。

**实例**

本例检测输入变量的值。如果值是错误的，会抛出一个异常（错误）。catch 会捕捉到这个错误，并显示一段自定义的错误消息：

```
<script>
function myFunction()
{
try
  {
  var x=document.getElementById("demo").value;
  if(x=="")    throw "empty";
  if(isNaN(x)) throw "not a number";
  if(x>10)     throw "too high";
  if(x<5)      throw "too low";
  }
catch(err)
  {
  var y=document.getElementById("mess");
  y.innerHTML="Error: " + err + ".";
  }
}
</script>

<h1>My First JavaScript</h1>
<p>Please input a number between 5 and 10:</p>
<input id="demo" type="text">
<button type="button" onclick="myFunction()">Test Input</button>
<p id="mess"></p>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_throw_error)

请注意，如果 getElementById 函数出错，上面的例子也会抛出一个错误。  

##   JavaScript 表单验证



**JavaScript 可用来在数据被送往服务器前对 HTML 表单中的这些输入数据进行验证。**

### JavaScript 表单验证

JavaScript 可用来在数据被送往服务器前对 HTML 表单中的这些输入数据进行验证。

被 JavaScript 验证的这些典型的表单数据有：

- 用户是否已填写表单中的必填项目？
- 用户输入的邮件地址是否合法？
- 用户是否已输入合法的日期？
- 用户是否在数据域 (numeric field) 中输入了文本？

### 必填（或必选）项目

下面的函数用来检查用户是否已填写表单中的必填（或必选）项目。假如必填或必选项为空，那么警告框会弹出，并且函数的返回值为 false，否则函数的返回值则为 true（意味着数据没有问题）：

```
function validate_required(field,alerttxt)
{
with (field)
{
if (value==null||value=="")
  {alert(alerttxt);return false}
else {return true}
}
}
```

下面是连同 HTML 表单的代码：

```
<html>
<head>
<script type="text/javascript">

function validate_required(field,alerttxt)
{
with (field)
  {
  if (value==null||value=="")
    {alert(alerttxt);return false}
  else {return true}
  }
}

function validate_form(thisform)
{
with (thisform)
  {
  if (validate_required(email,"Email must be filled out!")==false)
    {email.focus();return false}
  }
}
</script>
</head>

<body>
<form action="submitpage.htm" onsubmit="return validate_form(this)" method="post">
Email: <input type="text" name="email" size="30">
<input type="submit" value="Submit"> 
</form>
</body>

</html>
```

### E-mail 验证

下面的函数检查输入的数据是否符合电子邮件地址的基本语法。

意思就是说，输入的数据必须包含 @ 符号和点号(.)。同时，@ 不可以是邮件地址的首字符，并且 @ 之后需有至少一个点号：

```
function validate_email(field,alerttxt)
{
with (field)
{
apos=value.indexOf("@")
dotpos=value.lastIndexOf(".")
if (apos<1||dotpos-apos<2) 
  {alert(alerttxt);return false}
else {return true}
}
}
```

下面是连同 HTML 表单的完整代码：

```
<html>
<head>
<script type="text/javascript">
function validate_email(field,alerttxt)
{
with (field)
{
apos=value.indexOf("@")
dotpos=value.lastIndexOf(".")
if (apos<1||dotpos-apos<2) 
  {alert(alerttxt);return false}
else {return true}
}
}

function validate_form(thisform)
{
with (thisform)
{
if (validate_email(email,"Not a valid e-mail address!")==false)
  {email.focus();return false}
}
}
</script>
</head>

<body>
<form action="submitpage.htm"onsubmit="return validate_form(this);" method="post">
Email: <input type="text" name="email" size="30">
<input type="submit" value="Submit"> 
</form>
</body>

</html>
```

# JavaScript HTML DOM

## DOM简介

**通过 HTML DOM，可访问 JavaScript HTML 文档的所有元素。**

### HTML DOM （文档对象模型）

当网页被加载时，浏览器会创建页面的文档对象模型（Document Object Model）。

HTML DOM 模型被构造为对象的树。

### HTML DOM 树



通过可编程的对象模型，JavaScript 获得了足够的能力来创建动态的 HTML。

- JavaScript 能够改变页面中的所有 HTML 元素
- JavaScript 能够改变页面中的所有 HTML 属性
- JavaScript 能够改变页面中的所有 CSS 样式
- JavaScript 能够对页面中的所有事件做出反应

### 查找 HTML 元素

通常，通过 JavaScript，您需要操作 HTML 元素。

为了做到这件事情，您必须首先找到该元素。有三种方法来做这件事：

- 通过 id 找到 HTML 元素
- 通过标签名找到 HTML 元素
- 通过类名找到 HTML 元素

### 通过 id 查找 HTML 元素

在 DOM 中查找 HTML 元素的最简单的方法，是通过使用元素的 id。

**实例**

本例查找 id="intro" 元素：

```
var x=document.getElementById("intro");
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_dom_getelementbyid)

如果找到该元素，则该方法将以对象（在 x 中）的形式返回该元素。

如果未找到该元素，则 x 将包含 null。

### 通过标签名查找 HTML 元素

**实例**

本例查找 id="main" 的元素，然后查找 "main" 中的所有 <p> 元素：

```
var x=document.getElementById("main");
var y=x.getElementsByTagName("p");
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_dom_getelementsbytagname)

提示：通过类名查找 HTML 元素在 IE 5,6,7,8 中无效。

### HTML DOM 教程

在本教程接下来的篇幅中，您将学到：

- 如何改变 HTML 元素的内容 (innerHTML)

- 如何改变 HTML 元素的样式 (CSS)

- 如何对 HTML DOM 事件对做出反应

- 如何添加或删除 HTML 元素



  ## 改变 HTML

  **HTML DOM 允许 JavaScript 改变 HTML 元素的内容。**

  ### 改变 HTML 输出流

  JavaScript 能够创建动态的 HTML 内容：

  **今天的日期是：** Mon Sep 17 2018 11:21:35 GMT+0800 (中国标准时间)

  在 JavaScript 中，document.write() 可用于直接向 HTML 输出流写内容。

**实例**

  ```
  <!DOCTYPE html>
  <html>
  <body>
  
  <script>
  document.write(Date());
  </script>
  
  </body>
  </html>
  ```

  [亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_dom_change_html_output_stream)

  提示：绝不要使用在文档加载之后使用 document.write()。这会覆盖该文档。

  ### 改变 HTML 内容

  修改 HTML 内容的最简单的方法时使用 innerHTML 属性。

  如需改变 HTML 元素的内容，请使用这个语法：

  ```
  document.getElementById(id).innerHTML=new HTML
  ```

**实例**

  本例改变了 <p> 元素的内容：

  ```
  <html>
  <body>
  
  <p id="p1">Hello World!</p>
  
  <script>
  document.getElementById("p1").innerHTML="New text!";
  </script>
  
  </body>
  </html>
  ```

  [亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_dom_change_html_innerhtml)

**实例**

  本例改变了 <h1> 元素的内容：

  ```
  <!DOCTYPE html>
  <html>
  <body>
  
  <h1 id="header">Old Header</h1>
  
  <script>
  var element=document.getElementById("header");
  element.innerHTML="New Header";
  </script>
  
  </body>
  </html>
  ```

  [亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_dom_change_html_innerhtml2)

  例子解释：

  - 上面的 HTML 文档含有 id="header" 的 <h1> 元素
  - 我们使用 HTML DOM 来获得 id="header" 的元素
  - JavaScript 更改此元素的内容 (innerHTML)

  ### 改变 HTML 属性

  如需改变 HTML 元素的属性，请使用这个语法：

  ```
  document.getElementById(id).attribute=new value
  ```

**实例**

  本例改变了 <img> 元素的 src 属性：

  ```
  <!DOCTYPE html>
  <html>
  <body>
  
  <img id="image" src="smiley.gif">
  
  <script>
  document.getElementById("image").src="landscape.jpg";
  </script>
  
  </body>
  </html>
  ```

  [亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_dom_change_html_attribute)

  例子解释：

  - 上面的 HTML 文档含有 id="image" 的 <img> 元素
  - 我们使用 HTML DOM 来获得 id="image" 的元素
  - JavaScript 更改此元素的属性（把 "smiley.gif" 改为 "landscape.jpg"）


## 改变 CSS



**HTML DOM 允许 JavaScript 改变 HTML 元素的样式。**

### 改变 HTML 样式

如需改变 HTML 元素的样式，请使用这个语法：

```
document.getElementById(id).style.property=new style
```

**例子** 1

下面的例子会改变 <p> 元素的样式：

```
<p id="p2">Hello World!</p>

<script>
document.getElementById("p2").style.color="blue";
</script>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_change_style)

**例子** 2

本例改变了 id="id1" 的 HTML 元素的样式，当用户点击按钮时：

```
<h1 id="id1">My Heading 1</h1>

<button type="button" onclick="document.getElementById('id1').style.color='red'">
点击这里
</button>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_change_style2)

### 更多实例

- [Visibility](http://www.w3school.com.cn/tiy/t.asp?f=js_change_style_visibility)

  如何使元素不可见。您希望元素显示或消失吗？

### HTML DOM Style 对象参考手册

如需完整的 HTML DOM Style 对象属性，请参阅我们的 [HTML DOM Style 对象参考手册](http://www.w3school.com.cn/jsref/dom_obj_style.asp)。

## DOM 事件



**HTML DOM 使 JavaScript 有能力对 HTML 事件做出反应。**

**实例**查看

http://www.w3school.com.cn/js/js_htmldom_events.asp

把鼠标移到上面

点击这里

### 对事件做出反应

我们可以在事件发生时执行 JavaScript，比如当用户在 HTML 元素上点击时。

如需在用户点击某个元素时执行代码，请向一个 HTML 事件属性添加 JavaScript 代码：

```
onclick=JavaScript
```

HTML 事件的例子：

- 当用户点击鼠标时
- 当网页已加载时
- 当图像已加载时
- 当鼠标移动到元素上时
- 当输入字段被改变时
- 当提交 HTML 表单时
- 当用户触发按键时

**例子 1**

在本例中，当用户在 <h1> 元素上点击时，会改变其内容：

```
<h1 onclick="this.innerHTML='谢谢!'">请点击该文本</h1>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_dom_event_onclick1)

**例子 2**

本例从事件处理器调用一个函数：

```
<!DOCTYPE html>
<html>
<head>
<script>
function changetext(id)
{
id.innerHTML="谢谢!";
}
</script>
</head>
<body>
<h1 onclick="changetext(this)">请点击该文本</h1>
</body>
</html>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_dom_event_onclick2)

### HTML 事件属性

如需向 HTML 元素分配 事件，您可以使用事件属性。

**实例**

向 button 元素分配 onclick 事件：

```
<button onclick="displayDate()">点击这里</button>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_dom_event_onclick3)

在上面的例子中，名为 displayDate 的函数将在按钮被点击时执行。

### 使用 HTML DOM 来分配事件

HTML DOM 允许您通过使用 JavaScript 来向 HTML 元素分配事件：

**实例**

向 button 元素分配 onclick 事件：

```
<script>
document.getElementById("myBtn").onclick=function(){displayDate()};
</script>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_dom_event_onclick4)

在上面的例子中，名为 displayDate 的函数被分配给 id=myButn" 的 HTML 元素。

当按钮被点击时，会执行该函数。

### onload 和 onunload 事件

onload 和 onunload 事件会在用户进入或离开页面时被触发。

onload 事件可用于检测访问者的浏览器类型和浏览器版本，并基于这些信息来加载网页的正确版本。

onload 和 onunload 事件可用于处理 cookie。

**实例**

```
<body onload="checkCookies()">
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_dom_event_onload_onunload)

### onchange 事件

onchange 事件常结合对输入字段的验证来使用。

下面是一个如何使用 onchange 的例子。当用户改变输入字段的内容时，会调用 upperCase() 函数。

**实例**

```
<input type="text" id="fname" onchange="upperCase()">
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_dom_event_onchange)

### onmouseover 和 onmouseout 事件

onmouseover 和 onmouseout 事件可用于在用户的鼠标移至 HTML 元素上方或移出元素时触发函数。

**实例**

一个简单的 onmouseover-onmouseout 实例：

把鼠标移到上面

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_dom_event_onmouseover_onmouseout)

### onmousedown、onmouseup 以及 onclick 事件

onmousedown, onmouseup 以及 onclick 构成了鼠标点击事件的所有部分。首先当点击鼠标按钮时，会触发 onmousedown 事件，当释放鼠标按钮时，会触发 onmouseup 事件，最后，当完成鼠标点击时，会触发 onclick 事件。

**实例**

一个简单的 onmousedown-onmouseup 实例：

请点击这里

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_dom_event_onmousedown_onmouseup)

### 更多实例

- [onmousedown 和 onmouseup](http://www.w3school.com.cn/tiy/t.asp?f=js_dom_event_onmousedown_onmouseup2)

  当用户按下鼠标按钮时，更换一幅图像。

- [onload](http://www.w3school.com.cn/tiy/t.asp?f=js_dom_event_onload2)

  当页面完成加载时，显示一个提示框。

- [onfocus](http://www.w3school.com.cn/tiy/t.asp?f=js_dom_event_onfocus)

  当输入字段获得焦点时，改变其背景色。

- [鼠标事件](http://www.w3school.com.cn/tiy/t.asp?f=js_dom_event_onmouse)

  当指针移动到元素上方时，改变其颜色；当指针移出文本后，会再次改变其颜色。

### HTML DOM Event 对象参考手册

如需所有 HTML DOM 事件的完整列表，请参阅 W3School 提供的 [HTML DOM Event 对象参考手册](http://www.w3school.com.cn/jsref/dom_obj_event.asp)。

## DOM 元素（节点）



**添加和删除节点（HTML 元素）。**

### 创建新的 HTML 元素

如需向 HTML DOM 添加新元素，您必须首先创建该元素（元素节点），然后向一个已存在的元素追加该元素。

**实例**

```
<div id="div1">
<p id="p1">这是一个段落</p>
<p id="p2">这是另一个段落</p>
</div>

<script>
var para=document.createElement("p");
var node=document.createTextNode("这是新段落。");
para.appendChild(node);

var element=document.getElementById("div1");
element.appendChild(para);
</script>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_dom_elementcreate)

例子解释：

这段代码创建新的 <p> 元素：

```
var para=document.createElement("p");
```

如需向 <p> 元素添加文本，您必须首先创建文本节点。这段代码创建了一个文本节点：

```
var node=document.createTextNode("这是新段落。");
```

然后您必须向 <p> 元素追加这个文本节点：

```
para.appendChild(node);
```

最后您必须向一个已有的元素追加这个新元素。

这段代码找到一个已有的元素：

```
var element=document.getElementById("div1");
```

这段代码向这个已有的元素追加新元素：

```
element.appendChild(para);
```

### 删除已有的 HTML 元素

如需删除 HTML 元素，您必须首先获得该元素的父元素：

**实例**

```
<div id="div1">
<p id="p1">这是一个段落。</p>
<p id="p2">这是另一个段落。</p>
</div>

<script>
var parent=document.getElementById("div1");
var child=document.getElementById("p1");
parent.removeChild(child);
</script>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_dom_elementremove)

例子解释：

这个 HTML 文档含有拥有两个子节点（两个 <p> 元素）的 <div> 元素：

```
<div id="div1">
<p id="p1">这是一个段落。</p>
<p id="p2">这是另一个段落。</p>
</div>
```

找到 id="div1" 的元素：

```
var parent=document.getElementById("div1");
```

找到 id="p1" 的 <p> 元素：

```
var child=document.getElementById("p1");
```

从父元素中删除子元素：

```
parent.removeChild(child);
```

提示：如果能够在不引用父元素的情况下删除某个元素，就太好了。

不过很遗憾。DOM 需要清楚您需要删除的元素，以及它的父元素。

这是常用的解决方案：找到您希望删除的子元素，然后使用其 parentNode 属性来找到父元素：

```
var child=document.getElementById("p1");
child.parentNode.removeChild(child);
```

### HTML DOM 教程

在我们的 JavaScript 教程的 HTML DOM 部分，您已经学到了：

- 如何改变 HTML 元素的内容 (innerHTML)
- 如何改变 HTML 元素的样式 (CSS)
- 如何对 HTML DOM 事件作出反应
- 如何添加或删除 HTML 元素

如果您希望学到更多有关使用 JavaScript 访问 HTML DOM 的知识，请访问我们完整的 [HTML DOM 教程](http://www.w3school.com.cn/htmldom/index.asp)。


  JavaScript 对象

- [DOM 节点](http://www.w3school.com.cn/js/js_htmldom_elements.asp)
- [JS 数字](http://www.w3school.com.cn/js/js_obj_number.asp)

**JavaScript 中的所有事物都是对象：字符串、数值、数组、函数...**

**此外，JavaScript 允许自定义对象。**

# JavaScript 对象

## JavaScript 对象简介

JavaScript 提供多个*内建*对象，比如 String、Date、Array 等等。

对象只是带有*属性*和*方法*的特殊数据类型。

### 访问对象的属性

属性是与对象相关的值。

访问对象属性的语法是：

```
objectName.propertyName
```

这个例子使用了 String 对象的 length 属性来获得字符串的长度：

```
var message="Hello World!";
var x=message.length;
```

在以上代码执行后，x 的值将是：

```
12
```

### 访问对象的方法

方法是能够在对象上执行的动作。

您可以通过以下语法来调用方法：

```
objectName.methodName()
```

这个例子使用了 String 对象的 toUpperCase() 方法来将文本转换为大写：

```
var message="Hello world!";
var x=message.toUpperCase();
```

在以上代码执行后，x 的值将是：

```
HELLO WORLD!
```

### 创建 JavaScript 对象

通过 JavaScript，您能够定义并创建自己的对象。

创建新对象有两种不同的方法：

1. 定义并创建对象的实例
2. 使用函数来定义对象，然后创建新的对象实例

### 创建直接的实例

这个例子创建了对象的一个新实例，并向其添加了四个属性：

**实例**

```
person=new Object();
person.firstname="Bill";
person.lastname="Gates";
person.age=56;
person.eyecolor="blue";
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_create_object)

替代语法（使用对象 literals）：

**实例**

```
person={firstname:"John",lastname:"Doe",age:50,eyecolor:"blue"};
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_create_object1)

### 使用对象构造器

本例使用函数来构造对象：

**实例**

```
function person(firstname,lastname,age,eyecolor)
{
this.firstname=firstname;
this.lastname=lastname;
this.age=age;
this.eyecolor=eyecolor;
}
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_create_object2)

### 创建 JavaScript 对象实例

一旦您有了对象构造器，就可以创建新的对象实例，就像这样：

```
var myFather=new person("Bill","Gates",56,"blue");
var myMother=new person("Steve","Jobs",48,"green");
```

### 把属性添加到 JavaScript 对象

您可以通过为对象赋值，向已有对象添加新属性：

假设 personObj 已存在 - 您可以为其添加这些新属性：firstname、lastname、age 以及 eyecolor：

```
person.firstname="Bill";
person.lastname="Gates";
person.age=56;
person.eyecolor="blue";

x=person.firstname;
```

在以上代码执行后，x 的值将是：

```
Bill
```

### 把方法添加到 JavaScript 对象

方法只不过是附加在对象上的函数。

在构造器函数内部定义对象的方法：

```
function person(firstname,lastname,age,eyecolor)
{
this.firstname=firstname;
this.lastname=lastname;
this.age=age;
this.eyecolor=eyecolor;

this.changeName=changeName;
function changeName(name)
{
this.lastname=name;
}
}
```

changeName() 函数 name 的值赋给 person 的 lastname 属性。

现在您可以试一下：

```
myMother.changeName("Ballmer");
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_create_object3)

### JavaScript 类

JavaScript 是面向对象的语言，但 JavaScript 不使用类。

在 JavaScript 中，不会创建类，也不会通过类来创建对象（就像在其他面向对象的语言中那样）。

JavaScript 基于 prototype，而不是基于类的。

### JavaScript for...in 循环

JavaScript for...in 语句循环遍历对象的属性。

### 语法

```
for (对象中的变量){
  要执行的代码
  }
```

注释：for...in 循环中的代码块将针对每个属性执行一次。

**实例**

循环遍历对象的属性：

```
var person={fname:"Bill",lname:"Gates",age:56};

for (x in person){
  txt=txt + person[x];
  }
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_object_for_in)

### 课外书

如需更多有关 *JavaScript 对象*的知识，请阅读 JavaScript 高级教程中的相关内容：

- [ECMAScript 面向对象技术](http://www.w3school.com.cn/js/pro_js_object_oriented.asp)

  本节简要介绍了面向对象技术的术语、面向对象语言的要求以及对象的构成。

- [ECMAScript 对象应用](http://www.w3school.com.cn/js/pro_js_object_working_with.asp)

  本节讲解了如何声明和实例化对象，如何引用和废除对象，以及绑定的概念。

- [ECMAScript 对象类型](http://www.w3school.com.cn/js/pro_js_object_types.asp)

  本节介绍了 ECMAScript 的三种类型：本地对象、内置对象和宿主对象，并提供了指向相关参考手册的链接。

- [ECMAScript 对象作用域](http://www.w3school.com.cn/js/pro_js_object_scope.asp)

  本节讲解了 ECMAScript 作用域以及 this 关键字。

- [ECMAScript 定义类或对象](http://www.w3school.com.cn/js/pro_js_object_defining.asp)

  本节详细讲解了创建 ECMAScript 对象或类的各种方式。

- [ECMAScript 修改对象](http://www.w3school.com.cn/js/pro_js_object_modifying.asp)

  本节讲解了如何通过创建新方法或重定义已有方法来修改对象。

## Number 对象

### Number 对象描述

在 JavaScript 中，数字是一种基本的数据类型。JavaScript 还支持 Number 对象，该对象是原始数值的包装对象。在必要时，JavaScript 会自动地在原始数据和对象之间转换。在 JavaScript 1.1 中，可以用构造函数 Number() 明确地创建一个 Number 对象，尽管这样做并没有什么必要。

构造函数 Number() 可以不与运算符 new 一起使用，而直接作为转化函数来使用。以这种方式调用 Number() 时，它会把自己的参数转化成一个数字，然后返回转换后的原始数值（或 NaN）。

构造函数通常还用作 5 个有用的数字常量的占位符，这 5 个有用的数字常量分别是可表示的最大数、可表示的最小数、正无穷大、负无穷大和特殊的 NaN 值。 注意，这些值是构造函数 Number() 自身的属性，而不是单独的某个 Number 对象的属性。

比如这样使用属性 MAX_VALUE 是正确的：

```
var big = Number.MAX_VALUE
```

但是这样是错误的：

```
var n= new Number(2);
var big = n.MAX_VALUE
```

作为比较，我们看一下 toString() 和 Number 对象的其他方法，它们是每个 Number 对象的方法，而不是 Number() 构造函数的方法。前面提到过，在必要时，JavaScript 会自动地把原始数值转化成 Number 对象，调用 Number 方法的既可以是 Number 对象，也可以是原始数字值。

```
var n = 123;
var binary_value = n.toString(2);
```

Number 对象是原始数值的包装对象。

### 创建 Number 对象的语法：

```
var myNum=new Number(value);
var myNum=Number(value);
```

**参数**

参数 *value* 是要创建的 Number 对象的数值，或是要转换成数字的值。

**返回值**

当 Number() 和运算符 new 一起作为构造函数使用时，它返回一个新创建的 Number 对象。如果不用 new 运算符，把 Number() 作为一个函数来调用，它将把自己的参数转换成一个原始的数值，并且返回这个值（如果转换失败，则返回 NaN）。

### JavaScript 数字

JavaScript 数字可以使用也可以不使用小数点来书写：

**实例**

```
var pi=3.14;    // 使用小数点
var x=34;       // 不使用小数点
```

极大或极小的数字可通过科学（指数）计数法来写：

**实例**

```
var y=123e5;    // 12300000
var z=123e-5;   // 0.00123
```

### 所有 JavaScript 数字均为 64 位

JavaScript 不是类型语言。与许多其他编程语言不同，JavaScript 不定义不同类型的数字，比如整数、短、长、浮点等等。

JavaScript 中的所有数字都存储为根为 10 的 64 位（8 比特），浮点数。

### 精度

整数（不使用小数点或指数计数法）最多为 15 位。

小数的最大位数是 17，但是浮点运算并不总是 100% 准确：

**实例**

```
var x=0.2+0.1;
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_inaccurate)

### 八进制和十六进制

如果前缀为 0，则 JavaScript 会把数值常量解释为八进制数，如果前缀为 0 和 "x"，则解释为十六进制数。

**实例**

```
var y=0377;
var z=0xFF;
```

提示：绝不要在数字前面写零，除非您需要进行八进制转换。

### Number属性和方法

### Number 对象属性

| 属性                                                         | 描述                                   |
| ------------------------------------------------------------ | -------------------------------------- |
| [constructor](http://www.w3school.com.cn/jsref/jsref_constructor_number.asp) | 返回对创建此对象的 Number 函数的引用。 |
| [MAX_VALUE](http://www.w3school.com.cn/jsref/jsref_max_value.asp) | 可表示的最大的数。                     |
| [MIN_VALUE](http://www.w3school.com.cn/jsref/jsref_min_value.asp) | 可表示的最小的数。                     |
| [NaN](http://www.w3school.com.cn/jsref/jsref_nan_number.asp) | 非数字值。                             |
| [NEGATIVE_INFINITY](http://www.w3school.com.cn/jsref/jsref_negative_infinity.asp) | 负无穷大，溢出时返回该值。             |
| [POSITIVE_INFINITY](http://www.w3school.com.cn/jsref/jsref_positive_infinity.asp) | 正无穷大，溢出时返回该值。             |
| prototype                                                    | 使您有能力向对象添加属性和方法。       |

### Number 对象方法

| 方法                                                         | 描述                                                 |
| ------------------------------------------------------------ | ---------------------------------------------------- |
| [toString](http://www.w3school.com.cn/jsref/jsref_tostring_number.asp) | 把数字转换为字符串，使用指定的基数。                 |
| [toLocaleString](http://www.w3school.com.cn/jsref/jsref_tolocalestring_number.asp) | 把数字转换为字符串，使用本地数字格式顺序。           |
| [toFixed](http://www.w3school.com.cn/jsref/jsref_tofixed.asp) | 把数字转换为字符串，结果的小数点后有指定位数的数字。 |
| [toExponential](http://www.w3school.com.cn/jsref/jsref_toexponential.asp) | 把对象的值转换为指数计数法。                         |
| [toPrecision](http://www.w3school.com.cn/jsref/jsref_toprecision.asp) | 把数字格式化为指定的长度。                           |
| [valueOf](http://www.w3school.com.cn/jsref/jsref_valueof_number.asp) | 返回一个 Number 对象的基本数字值。                   |

 **[Number 对象参考手册](http://www.w3school.com.cn/jsref/jsref_obj_number.asp)**

如需更多信息，请阅读 JavaScript 高级教程中的相关内容：

- [ECMAScript 引用类型](http://www.w3school.com.cn/js/pro_js_referencetypes.asp)

  引用类型通常叫做类（class）或对象。本节讲解 ECMAScript 的预定义引用类型。

## 字符串(String)对象

### String 对象描述

字符串是 JavaScript 的一种基本的数据类型。

String 对象的 length 属性声明了该字符串中的字符数。

String 类定义了大量操作字符串的方法，例如从字符串中提取字符或子串，或者检索字符或子串。

需要注意的是，JavaScript 的字符串是不可变的（immutable），String 类定义的方法都不能改变字符串的内容。像 String.toUpperCase() 这样的方法，返回的是全新的字符串，而不是修改原始字符串。

在较早的 Netscape 代码基的 JavaScript 实现中（例如 Firefox 实现中），字符串的行为就像只读的字符数组。例如，从字符串 s 中提取第三个字符，可以用 s[2] 代替更加标准的 s.charAt(2)。此外，对字符串应用 for/in 循环时，它将枚举字符串中每个字符的数组下标（但要注意，ECMAScript 标准规定，不能枚举 length 属性）。因为字符串的数组行为不标准，所以应该避免使用它。

**String 对象用于处理文本（字符串）。**

### 创建 String 对象的语法：

```
new String(s);
String(s);
```

**参数**

参数 *s* 是要存储在 String 对象中或转换成原始字符串的值。

**返回值**

当 String() 和运算符 new 一起作为构造函数使用时，它返回一个新创建的 String 对象，存放的是字符串 *s* 或 *s* 的字符串表示。

当不用 new 运算符调用 String() 时，它只把 *s* 转换成原始的字符串，并返回转换后的值。

**例子：**

下面的例子使用字符串对象的长度属性来计算字符串的长度。

```
var txt="Hello world!"
document.write(txt.length)

```

上面的代码输出为：

```
12

```

下面的例子使用字符串对象的toUpperCase()方法将字符串转换为大写：

```
var txt="Hello world!"
document.write(txt.toUpperCase())

```

上面的代码输出为：

```
HELLO WORLD!

```

### JavaScript String（字符串）对象 实例

- [计算字符串的长度](http://www.w3school.com.cn/tiy/t.asp?f=jsrf_string_length)

  如何使用长度属性来计算字符串的长度。

- [为字符串添加样式](http://www.w3school.com.cn/tiy/t.asp?f=jsrf_string_style)

  如何为字符串添加样式。

- [indexOf() 方法](http://www.w3school.com.cn/tiy/t.asp?f=jsrf_string_indexof)

  如何使用 indexOf() 来定位字符串中某一个指定的字符首次出现的位置。

- [match() 方法](http://www.w3school.com.cn/tiy/t.asp?f=jsrf_string_match)

  如何使用 match() 来查找字符串中特定的字符，并且如果找到的话，则返回这个字符。

- [如何替换字符串中的字符 - replace()](http://www.w3school.com.cn/tiy/t.asp?f=jseg_replace_1)

  如何使用 replace() 方法在字符串中用某些字符替换另一些字符。

### 完整的 String 对象参考手册

请查看我们的 [JavaScript String 对象参考手册](http://www.w3school.com.cn/jsref/jsref_obj_string.asp)，其中提供了可以与字符串对象一同使用的所有的属性和方法。

这个手册包含的关于每个属性和方法的用法的详细描述和实例。

### String 对象属性

| 属性                                                         | 描述                       |
| ------------------------------------------------------------ | -------------------------- |
| constructor                                                  | 对创建该对象的函数的引用   |
| [length](http://www.w3school.com.cn/jsref/jsref_length_string.asp) | 字符串的长度               |
| prototype                                                    | 允许您向对象添加属性和方法 |

### String 对象方法

| 方法                                                         | 描述                                                 |
| ------------------------------------------------------------ | ---------------------------------------------------- |
| [anchor()](http://www.w3school.com.cn/jsref/jsref_anchor.asp) | 创建 HTML 锚。                                       |
| [big()](http://www.w3school.com.cn/jsref/jsref_big.asp)      | 用大号字体显示字符串。                               |
| [blink()](http://www.w3school.com.cn/jsref/jsref_blink.asp)  | 显示闪动字符串。                                     |
| [bold()](http://www.w3school.com.cn/jsref/jsref_bold.asp)    | 使用粗体显示字符串。                                 |
| [charAt()](http://www.w3school.com.cn/jsref/jsref_charAt.asp) | 返回在指定位置的字符。                               |
| [charCodeAt()](http://www.w3school.com.cn/jsref/jsref_charCodeAt.asp) | 返回在指定的位置的字符的 Unicode 编码。              |
| [concat()](http://www.w3school.com.cn/jsref/jsref_concat_string.asp) | 连接字符串。                                         |
| [fixed()](http://www.w3school.com.cn/jsref/jsref_fixed.asp)  | 以打字机文本显示字符串。                             |
| [fontcolor()](http://www.w3school.com.cn/jsref/jsref_fontcolor.asp) | 使用指定的颜色来显示字符串。                         |
| [fontsize()](http://www.w3school.com.cn/jsref/jsref_fontsize.asp) | 使用指定的尺寸来显示字符串。                         |
| [fromCharCode()](http://www.w3school.com.cn/jsref/jsref_fromCharCode.asp) | 从字符编码创建一个字符串。                           |
| [indexOf()](http://www.w3school.com.cn/jsref/jsref_indexOf.asp) | 检索字符串。                                         |
| [italics()](http://www.w3school.com.cn/jsref/jsref_italics.asp) | 使用斜体显示字符串。                                 |
| [lastIndexOf()](http://www.w3school.com.cn/jsref/jsref_lastIndexOf.asp) | 从后向前搜索字符串。                                 |
| [link()](http://www.w3school.com.cn/jsref/jsref_link.asp)    | 将字符串显示为链接。                                 |
| [localeCompare()](http://www.w3school.com.cn/jsref/jsref_localeCompare.asp) | 用本地特定的顺序来比较两个字符串。                   |
| [match()](http://www.w3school.com.cn/jsref/jsref_match.asp)  | 找到一个或多个正则表达式的匹配。                     |
| [replace()](http://www.w3school.com.cn/jsref/jsref_replace.asp) | 替换与正则表达式匹配的子串。                         |
| [search()](http://www.w3school.com.cn/jsref/jsref_search.asp) | 检索与正则表达式相匹配的值。                         |
| [slice()](http://www.w3school.com.cn/jsref/jsref_slice_string.asp) | 提取字符串的片断，并在新的字符串中返回被提取的部分。 |
| [small()](http://www.w3school.com.cn/jsref/jsref_small.asp)  | 使用小字号来显示字符串。                             |
| [split()](http://www.w3school.com.cn/jsref/jsref_split.asp)  | 把字符串分割为字符串数组。                           |
| [strike()](http://www.w3school.com.cn/jsref/jsref_strike.asp) | 使用删除线来显示字符串。                             |
| [sub()](http://www.w3school.com.cn/jsref/jsref_sub.asp)      | 把字符串显示为下标。                                 |
| [substr()](http://www.w3school.com.cn/jsref/jsref_substr.asp) | 从起始索引号提取字符串中指定数目的字符。             |
| [substring()](http://www.w3school.com.cn/jsref/jsref_substring.asp) | 提取字符串中两个指定的索引号之间的字符。             |
| [sup()](http://www.w3school.com.cn/jsref/jsref_sup.asp)      | 把字符串显示为上标。                                 |
| [toLocaleLowerCase()](http://www.w3school.com.cn/jsref/jsref_toLocaleLowerCase.asp) | 把字符串转换为小写。                                 |
| [toLocaleUpperCase()](http://www.w3school.com.cn/jsref/jsref_toLocaleUpperCase.asp) | 把字符串转换为大写。                                 |
| [toLowerCase()](http://www.w3school.com.cn/jsref/jsref_toLowerCase.asp) | 把字符串转换为小写。                                 |
| [toUpperCase()](http://www.w3school.com.cn/jsref/jsref_toUpperCase.asp) | 把字符串转换为大写。                                 |
| toSource()                                                   | 代表对象的源代码。                                   |
| [toString()](http://www.w3school.com.cn/jsref/jsref_toString_string.asp) | 返回字符串。                                         |
| [valueOf()](http://www.w3school.com.cn/jsref/jsref_valueOf_string.asp) | 返回某个字符串对象的原始值。                         |

### 相关参考页面

JavaScript 高级教程：[ECMAScript 类型转换](http://www.w3school.com.cn/js/pro_js_typeconversion.asp)

JavaScript 高级教程：[ECMAScript 引用类型](http://www.w3school.com.cn/js/pro_js_referencetypes.asp)

JavaScript 参考手册：[String 对象](http://www.w3school.com.cn/jsref/jsref_obj_string.asp)

##   Date（日期）对象

**Date 对象**

**Date 对象用于处理日期和时间。**

### 创建 Date 对象的语法：

Date 对象用于处理日期和时间。

可以通过 new 关键词来定义 Date 对象。以下代码定义了名为 myDate 的 Date 对象：

```
var myDate=new Date() 
```

注释：Date 对象自动使用当前的日期和时间作为其初始值。

### 操作日期

通过使用针对日期对象的方法，我们可以很容易地对日期进行操作。

在下面的例子中，我们为日期对象设置了一个特定的日期 (2008 年 8 月 9 日)：

```
var myDate=new Date()
myDate.setFullYear(2008,7,9)
```

注意：表示月份的参数介于 0 到 11 之间。也就是说，如果希望把月设置为 8 月，则参数应该是 7。

在下面的例子中，我们将日期对象设置为 5 天后的日期：

```
var myDate=new Date()
myDate.setDate(myDate.getDate()+5)
```

注意：如果增加天数会改变月份或者年份，那么日期对象会自动完成这种转换。

### 比较日期

日期对象也可用于比较两个日期。

下面的代码将当前日期与 2008 年 8 月 9 日做了比较：

```
var myDate=new Date();
myDate.setFullYear(2008,8,9);

var today = new Date();

if (myDate>today)
{
alert("Today is before 9th August 2008");
}
else
{
alert("Today is after 9th August 2008");
}
```

### JavaScript Date（日期）对象 实例

- [返回当日的日期和时间](http://www.w3school.com.cn/tiy/t.asp?f=jsrf_date)

  如何使用 Date() 方法获得当日的日期。

- [getTime()](http://www.w3school.com.cn/tiy/t.asp?f=jseg_date_gettime)

  getTime() 返回从 1970 年 1 月 1 日至今的毫秒数。

- [setFullYear()](http://www.w3school.com.cn/tiy/t.asp?f=jsrf_date_setfullyear2)

  如何使用 setFullYear() 设置具体的日期。

- [toUTCString()](http://www.w3school.com.cn/tiy/t.asp?f=jsrf_date_toutcstring)

  如何使用 toUTCString() 将当日的日期（根据 UTC）转换为字符串。

- [getDay()](http://www.w3school.com.cn/tiy/t.asp?f=jsrf_date_date_weekday)

  如何使用 getDay() 和数组来显示星期，而不仅仅是数字。

- [显示一个钟表](http://www.w3school.com.cn/tiy/t.asp?f=jsrf_date_timing_clock)

  如何在网页上显示一个钟表。

### 完整的 Date 对象参考手册

我们提供 [JavaScript Date 对象参考手册](http://www.w3school.com.cn/jsref/jsref_obj_date.asp)，其中包括所有可用于日期对象的属性和方法。

该手册包含了对每个属性和方法的详细描述以及相关实例。

### Date 对象属性

| 属性                                                         | 描述                                 |
| ------------------------------------------------------------ | ------------------------------------ |
| [constructor](http://www.w3school.com.cn/jsref/jsref_constructor_date.asp) | 返回对创建此对象的 Date 函数的引用。 |
| [prototype](http://www.w3school.com.cn/jsref/jsref_prototype_date.asp) | 使您有能力向对象添加属性和方法。     |

### Date 对象方法

| 方法                                                         | 描述                                                   |
| ------------------------------------------------------------ | ------------------------------------------------------ |
| [Date()](http://www.w3school.com.cn/jsref/jsref_Date.asp)    | 返回当日的日期和时间。                                 |
| [getDate()](http://www.w3school.com.cn/jsref/jsref_getDate.asp) | 从 Date 对象返回一个月中的某一天 (1 ~ 31)。            |
| [getDay()](http://www.w3school.com.cn/jsref/jsref_getDay.asp) | 从 Date 对象返回一周中的某一天 (0 ~ 6)。               |
| [getMonth()](http://www.w3school.com.cn/jsref/jsref_getMonth.asp) | 从 Date 对象返回月份 (0 ~ 11)。                        |
| [getFullYear()](http://www.w3school.com.cn/jsref/jsref_getFullYear.asp) | 从 Date 对象以四位数字返回年份。                       |
| [getYear()](http://www.w3school.com.cn/jsref/jsref_getYear.asp) | 请使用 getFullYear() 方法代替。                        |
| [getHours()](http://www.w3school.com.cn/jsref/jsref_getHours.asp) | 返回 Date 对象的小时 (0 ~ 23)。                        |
| [getMinutes()](http://www.w3school.com.cn/jsref/jsref_getMinutes.asp) | 返回 Date 对象的分钟 (0 ~ 59)。                        |
| [getSeconds()](http://www.w3school.com.cn/jsref/jsref_getSeconds.asp) | 返回 Date 对象的秒数 (0 ~ 59)。                        |
| [getMilliseconds()](http://www.w3school.com.cn/jsref/jsref_getMilliseconds.asp) | 返回 Date 对象的毫秒(0 ~ 999)。                        |
| [getTime()](http://www.w3school.com.cn/jsref/jsref_getTime.asp) | 返回 1970 年 1 月 1 日至今的毫秒数。                   |
| [getTimezoneOffset()](http://www.w3school.com.cn/jsref/jsref_getTimezoneOffset.asp) | 返回本地时间与格林威治标准时间 (GMT) 的分钟差。        |
| [getUTCDate()](http://www.w3school.com.cn/jsref/jsref_getUTCDate.asp) | 根据世界时从 Date 对象返回月中的一天 (1 ~ 31)。        |
| [getUTCDay()](http://www.w3school.com.cn/jsref/jsref_getUTCDay.asp) | 根据世界时从 Date 对象返回周中的一天 (0 ~ 6)。         |
| [getUTCMonth()](http://www.w3school.com.cn/jsref/jsref_getUTCMonth.asp) | 根据世界时从 Date 对象返回月份 (0 ~ 11)。              |
| [getUTCFullYear()](http://www.w3school.com.cn/jsref/jsref_getUTCFullYear.asp) | 根据世界时从 Date 对象返回四位数的年份。               |
| [getUTCHours()](http://www.w3school.com.cn/jsref/jsref_getUTCHours.asp) | 根据世界时返回 Date 对象的小时 (0 ~ 23)。              |
| [getUTCMinutes()](http://www.w3school.com.cn/jsref/jsref_getUTCMinutes.asp) | 根据世界时返回 Date 对象的分钟 (0 ~ 59)。              |
| [getUTCSeconds()](http://www.w3school.com.cn/jsref/jsref_getUTCSeconds.asp) | 根据世界时返回 Date 对象的秒钟 (0 ~ 59)。              |
| [getUTCMilliseconds()](http://www.w3school.com.cn/jsref/jsref_getUTCMilliseconds.asp) | 根据世界时返回 Date 对象的毫秒(0 ~ 999)。              |
| [parse()](http://www.w3school.com.cn/jsref/jsref_parse.asp)  | 返回1970年1月1日午夜到指定日期（字符串）的毫秒数。     |
| [setDate()](http://www.w3school.com.cn/jsref/jsref_setDate.asp) | 设置 Date 对象中月的某一天 (1 ~ 31)。                  |
| [setMonth()](http://www.w3school.com.cn/jsref/jsref_setMonth.asp) | 设置 Date 对象中月份 (0 ~ 11)。                        |
| [setFullYear()](http://www.w3school.com.cn/jsref/jsref_setFullYear.asp) | 设置 Date 对象中的年份（四位数字）。                   |
| [setYear()](http://www.w3school.com.cn/jsref/jsref_setYear.asp) | 请使用 setFullYear() 方法代替。                        |
| [setHours()](http://www.w3school.com.cn/jsref/jsref_setHours.asp) | 设置 Date 对象中的小时 (0 ~ 23)。                      |
| [setMinutes()](http://www.w3school.com.cn/jsref/jsref_setMinutes.asp) | 设置 Date 对象中的分钟 (0 ~ 59)。                      |
| [setSeconds()](http://www.w3school.com.cn/jsref/jsref_setSeconds.asp) | 设置 Date 对象中的秒钟 (0 ~ 59)。                      |
| [setMilliseconds()](http://www.w3school.com.cn/jsref/jsref_setMilliseconds.asp) | 设置 Date 对象中的毫秒 (0 ~ 999)。                     |
| [setTime()](http://www.w3school.com.cn/jsref/jsref_setTime.asp) | 以毫秒设置 Date 对象。                                 |
| [setUTCDate()](http://www.w3school.com.cn/jsref/jsref_setUTCDate.asp) | 根据世界时设置 Date 对象中月份的一天 (1 ~ 31)。        |
| [setUTCMonth()](http://www.w3school.com.cn/jsref/jsref_setUTCMonth.asp) | 根据世界时设置 Date 对象中的月份 (0 ~ 11)。            |
| [setUTCFullYear()](http://www.w3school.com.cn/jsref/jsref_setUTCFullYear.asp) | 根据世界时设置 Date 对象中的年份（四位数字）。         |
| [setUTCHours()](http://www.w3school.com.cn/jsref/jsref_setutchours.asp) | 根据世界时设置 Date 对象中的小时 (0 ~ 23)。            |
| [setUTCMinutes()](http://www.w3school.com.cn/jsref/jsref_setUTCMinutes.asp) | 根据世界时设置 Date 对象中的分钟 (0 ~ 59)。            |
| [setUTCSeconds()](http://www.w3school.com.cn/jsref/jsref_setUTCSeconds.asp) | 根据世界时设置 Date 对象中的秒钟 (0 ~ 59)。            |
| [setUTCMilliseconds()](http://www.w3school.com.cn/jsref/jsref_setUTCMilliseconds.asp) | 根据世界时设置 Date 对象中的毫秒 (0 ~ 999)。           |
| [toSource()](http://www.w3school.com.cn/jsref/jsref_tosource_boolean.asp) | 返回该对象的源代码。                                   |
| [toString()](http://www.w3school.com.cn/jsref/jsref_toString_date.asp) | 把 Date 对象转换为字符串。                             |
| [toTimeString()](http://www.w3school.com.cn/jsref/jsref_toTimeString.asp) | 把 Date 对象的时间部分转换为字符串。                   |
| [toDateString()](http://www.w3school.com.cn/jsref/jsref_toDateString.asp) | 把 Date 对象的日期部分转换为字符串。                   |
| [toGMTString()](http://www.w3school.com.cn/jsref/jsref_toGMTString.asp) | 请使用 toUTCString() 方法代替。                        |
| [toUTCString()](http://www.w3school.com.cn/jsref/jsref_toUTCString.asp) | 根据世界时，把 Date 对象转换为字符串。                 |
| [toLocaleString()](http://www.w3school.com.cn/jsref/jsref_toLocaleString.asp) | 根据本地时间格式，把 Date 对象转换为字符串。           |
| [toLocaleTimeString()](http://www.w3school.com.cn/jsref/jsref_toLocaleTimeString.asp) | 根据本地时间格式，把 Date 对象的时间部分转换为字符串。 |
| [toLocaleDateString()](http://www.w3school.com.cn/jsref/jsref_toLocaleDateString.asp) | 根据本地时间格式，把 Date 对象的日期部分转换为字符串。 |
| [UTC()](http://www.w3school.com.cn/jsref/jsref_utc.asp)      | 根据世界时返回 1970 年 1 月 1 日 到指定日期的毫秒数。  |
| [valueOf()](http://www.w3school.com.cn/jsref/jsref_valueOf_date.asp) | 返回 Date 对象的原始值。                               |

## Array（数组）对象



### Array 对象

Array 对象用于在单个的变量中存储多个值。

### 创建 Array 对象的语法：

```
new Array();
new Array(size);
new Array(element0, element1, ..., elementn);
var myArray=new Array()
```

**参数**

参数 *size* 是期望的数组元素个数。返回的数组，length 字段将被设为 *size* 的值。

参数 *element* ..., *elementn* 是参数列表。当使用这些参数来调用构造函数 Array() 时，新创建的数组的元素就会被初始化为这些值。它的 length 字段也会被设置为参数的个数。

**返回值**

返回新创建并被初始化了的数组。

如果调用构造函数 Array() 时没有使用参数，那么返回的数组为空，length 字段为 0。

当调用构造函数时只传递给它一个数字参数，该构造函数将返回具有指定个数、元素为 undefined 的数组。

当其他参数调用 Array() 时，该构造函数将用参数指定的值初始化数组。

当把构造函数作为函数调用，不使用 new 运算符时，它的行为与使用 new 运算符调用它时的行为完全一样。

### Array(数组)赋值

数组对象用来在单独的变量名中存储一系列的值。

我们使用关键词 new 来创建数组对象。下面的代码定义了一个名为 myArray 的数组对象：

```
var myArray=new Array()
```

有两种向数组赋值的方法（你可以添加任意多的值，就像你可以定义你需要的任意多的变量一样）。

**方法1:**

```
var mycars=new Array()
mycars[0]="Saab"
mycars[1]="Volvo"
mycars[2]="BMW"
```

也可以使用一个整数自变量来控制数组的容量：

```
var mycars=new Array(3)
mycars[0]="Saab"
mycars[1]="Volvo"
mycars[2]="BMW"
```

**方法2:**

```
var mycars=new Array("Saab","Volvo","BMW")
```

注意：如果你需要在数组内指定数值或者逻辑值，那么变量类型应该是数值变量或者布尔变量，而不是字符变量。

### 访问数组

通过指定数组名以及索引号码，你可以访问某个特定的元素。

下面是代码行：

```
document.write(mycars[0])
```

下面是输出：

```
Saab
```

### 修改已有数组中的值

如需修改已有数组中的值，只要向指定下标号添加一个新值即可：

```
mycars[0]="Opel";
```

现在，以上代码：

```
document.write(mycars[0]);
```

将输出：

```
Opel
```

### 演示实例

- [创建数组](http://www.w3school.com.cn/tiy/t.asp?f=jsrf_array)

  创建数组，为其赋值，然后输出这些值。

- [For...In 声明](http://www.w3school.com.cn/tiy/t.asp?f=jsrf_array_for_in)

  使用 for...in 声明来循环输出数组中的元素。

- [合并两个数组 - concat()](http://www.w3school.com.cn/tiy/t.asp?f=jseg_concat_2)

  如何使用 concat() 方法来合并两个数组。

- [用数组的元素组成字符串 - join()](http://www.w3school.com.cn/tiy/t.asp?f=jseg_join)

  如何使用 join() 方法将数组的所有元素组成一个字符串。

- [文字数组 - sort()](http://www.w3school.com.cn/tiy/t.asp?f=jseg_sort_1)

  如何使用 sort() 方法从字面上对数组进行排序。

- [数字数组 - sort()](http://www.w3school.com.cn/tiy/t.asp?f=jseg_sort_2)

  如何使用 sort() 方法从数值上对数组进行排序。

### 完整的 Array 对象参考手册

我们提供 [JavaScript Array 对象参考手册](http://www.w3school.com.cn/jsref/jsref_obj_array.asp)，其中包括所有可用于数组对象的属性和方法。

该手册包含了对每个属性和方法的详细描述以及相关实例。

### Array 对象属性

| 属性                                                         | 描述                               |
| ------------------------------------------------------------ | ---------------------------------- |
| [constructor](http://www.w3school.com.cn/jsref/jsref_constructor_array.asp) | 返回对创建此对象的数组函数的引用。 |
| [length](http://www.w3school.com.cn/jsref/jsref_length_array.asp) | 设置或返回数组中元素的数目。       |
| [prototype](http://www.w3school.com.cn/jsref/jsref_prototype_array.asp) | 使您有能力向对象添加属性和方法。   |

### Array 对象方法

| 方法                                                         | 描述                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| [concat()](http://www.w3school.com.cn/jsref/jsref_concat_array.asp) | 连接两个或更多的数组，并返回结果。                           |
| [join()](http://www.w3school.com.cn/jsref/jsref_join.asp)    | 把数组的所有元素放入一个字符串。元素通过指定的分隔符进行分隔。 |
| [pop()](http://www.w3school.com.cn/jsref/jsref_pop.asp)      | 删除并返回数组的最后一个元素                                 |
| [push()](http://www.w3school.com.cn/jsref/jsref_push.asp)    | 向数组的末尾添加一个或更多元素，并返回新的长度。             |
| [reverse()](http://www.w3school.com.cn/jsref/jsref_reverse.asp) | 颠倒数组中元素的顺序。                                       |
| [shift()](http://www.w3school.com.cn/jsref/jsref_shift.asp)  | 删除并返回数组的第一个元素                                   |
| [slice()](http://www.w3school.com.cn/jsref/jsref_slice_array.asp) | 从某个已有的数组返回选定的元素                               |
| [sort()](http://www.w3school.com.cn/jsref/jsref_sort.asp)    | 对数组的元素进行排序                                         |
| [splice()](http://www.w3school.com.cn/jsref/jsref_splice.asp) | 删除元素，并向数组添加新元素。                               |
| [toSource()](http://www.w3school.com.cn/jsref/jsref_tosource_array.asp) | 返回该对象的源代码。                                         |
| [toString()](http://www.w3school.com.cn/jsref/jsref_toString_array.asp) | 把数组转换为字符串，并返回结果。                             |
| [toLocaleString()](http://www.w3school.com.cn/jsref/jsref_toLocaleString_array.asp) | 把数组转换为本地数组，并返回结果。                           |
| [unshift()](http://www.w3school.com.cn/jsref/jsref_unshift.asp) | 向数组的开头添加一个或更多元素，并返回新的长度。             |
| [valueOf()](http://www.w3school.com.cn/jsref/jsref_valueof_array.asp) | 返回数组对象的原始值                                         |

## Boolean（逻辑）对象



### Boolean 对象描述

在 JavaScript 中，布尔值是一种基本的数据类型。Boolean 对象是一个将布尔值打包的布尔对象。Boolean 对象主要用于提供将布尔值转换成字符串的 toString() 方法。

当调用 toString() 方法将布尔值转换成字符串时（通常是由 JavaScript 隐式地调用），JavaScript 会内在地将这个布尔值转换成一个临时的 Boolean 对象，然后调用这个对象的 toString() 方法。

Boolean 对象表示两个值："true" 或 "false"。

### 创建 Boolean 对象的语法：

```
new Boolean(value);	//构造函数
Boolean(value);		//转换函数
```

**参数**

参数 *value* 由布尔对象存放的值或者要转换成布尔值的值。

**返回值**

当作为一个构造函数（带有运算符 new）调用时，Boolean() 将把它的参数转换成一个布尔值，并且返回一个包含该值的 Boolean 对象。

如果作为一个函数（不带有运算符 new）调用时，Boolean() 只将把它的参数转换成一个原始的布尔值，并且返回这个值。

**注释：**如果省略 value 参数，或者设置为 0、-0、null、""、false、undefined 或 NaN，则该对象设置为 false。否则设置为 true（即使 value 参数是字符串 "false"）。

**下面的所有的代码行均会创建初始值为 false 的 Boolean 对象。**

```
var myBoolean=new Boolean();
var myBoolean=new Boolean(0);
var myBoolean=new Boolean(null);
var myBoolean=new Boolean("");
var myBoolean=new Boolean(false);
var myBoolean=new Boolean(NaN);
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jseg_obj_boolean_create_false)



**下面的所有的代码行均会创初始值为 true 的 Boolean 对象：**

```
var myBoolean=new Boolean(1);
var myBoolean=new Boolean(true);
var myBoolean=new Boolean("true");
var myBoolean=new Boolean("false");
var myBoolean=new Boolean("Bill Gates");
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=jseg_obj_boolean_create_true)

**参考实例**

- [检查逻辑值](http://www.w3school.com.cn/tiy/t.asp?f=jsrf_boolean)

  检查逻辑对象是 true 还是 false。

### 完整的 Boolean 对象参考手册

我们提供 [JavaScript Boolean 对象参考手册](http://www.w3school.com.cn/jsref/jsref_obj_boolean.asp)，其中包括所有可用于逻辑对象的属性和方法。

该手册包含了对每个属性和方法的详细描述以及相关实例。

### Boolean 对象属性

| 属性                                                         | 描述                                  |
| ------------------------------------------------------------ | ------------------------------------- |
| [constructor](http://www.w3school.com.cn/jsref/jsref_constructor_boolean.asp) | 返回对创建此对象的 Boolean 函数的引用 |
| [prototype](http://www.w3school.com.cn/jsref/jsref_prototype_boolean.asp) | 使您有能力向对象添加属性和方法。      |

### Boolean 对象方法

| 方法                                                         | 描述                               |
| ------------------------------------------------------------ | ---------------------------------- |
| [toSource()](http://www.w3school.com.cn/jsref/jsref_tosource_boolean.asp) | 返回该对象的源代码。               |
| [toString()](http://www.w3school.com.cn/jsref/jsref_toString_boolean.asp) | 把逻辑值转换为字符串，并返回结果。 |
| [valueOf()](http://www.w3school.com.cn/jsref/jsref_valueOf_boolean.asp) | 返回 Boolean 对象的原始值。        |



### 相关参考页面

JavaScript 高级教程：[ECMAScript 引用类型](http://www.w3school.com.cn/js/pro_js_referencetypes.asp)

JavaScript 参考手册：[Boolean 对象](http://www.w3school.com.cn/jsref/jsref_obj_boolean.asp)

## Math（算数）对象



**Math（算数）对象的作用是：执行常见的算数任务。**

Math 对象提供多种算数值类型和函数。无需在使用这个对象之前对它进行定义。

### 算数值

JavaScript 提供 8 种可被 Math 对象访问的算数值：

- 常数
- 圆周率
- 2 的平方根
- 1/2 的平方根
- 2 的自然对数
- 10 的自然对数
- 以 2 为底的 e 的对数
- 以 10 为底的 e 的对数

这是在 Javascript 中使用这些值的方法：（与上面的算数值一一对应）

- Math.E
- Math.PI
- Math.SQRT2
- Math.SQRT1_2
- Math.LN2
- Math.LN10
- Math.LOG2E
- Math.LOG10E

### 算数方法

除了可被 Math 对象访问的算数值以外，还有几个函数（方法）可以使用。

**函数（方法）实例：**

下面的例子使用了 Math 对象的 round 方法对一个数进行四舍五入。

```
document.write(Math.round(4.7))

```

上面的代码输出为：

```
5

```

下面的例子使用了 Math 对象的 random() 方法来返回一个介于 0 和 1 之间的随机数：

```
document.write(Math.random())

```

上面的代码输出为：

```
0.9370844220218102

```

下面的例子使用了 Math 对象的 floor() 方法和 random() 来返回一个介于 0 和 10 之间的随机数：

```
document.write(Math.floor(Math.random()*11)) 

```

上面的代码输出为：

```
3
```

### 更多实例

- [round()](http://www.w3school.com.cn/tiy/t.asp?f=jsrf_math_round)

  如何使用 round()。

- [random()](http://www.w3school.com.cn/tiy/t.asp?f=jsrf_math_random)

  如何使用 random() 来返回 0 到 1 之间的随机数。

- [max()](http://www.w3school.com.cn/tiy/t.asp?f=jsrf_math_max)

  如何使用 max() 来返回两个给定的数中的较大的数。（在 ECMASCript v3 之前，该方法只有两个参数。）

- [min()](http://www.w3school.com.cn/tiy/t.asp?f=jsrf_math_min)

  如何使用 min() 来返回两个给定的数中的较小的数。（在 ECMASCript v3 之前，该方法只有两个参数。）

### 完整的 Math 对象参考手册

我们提供 [JavaScript Math 对象的参考手册](http://www.w3school.com.cn/jsref/jsref_obj_math.asp)，其中包括所有可用于算术对象的属性和方法。

该手册包含了对每个属性和方法的详细描述以及相关实例。

### Math 对象属性

| 属性                                                         | 描述                                              |
| ------------------------------------------------------------ | ------------------------------------------------- |
| [E](http://www.w3school.com.cn/jsref/jsref_e.asp)            | 返回算术常量 e，即自然对数的底数（约等于2.718）。 |
| [LN2](http://www.w3school.com.cn/jsref/jsref_ln2.asp)        | 返回 2 的自然对数（约等于0.693）。                |
| [LN10](http://www.w3school.com.cn/jsref/jsref_ln10.asp)      | 返回 10 的自然对数（约等于2.302）。               |
| [LOG2E](http://www.w3school.com.cn/jsref/jsref_log2e.asp)    | 返回以 2 为底的 e 的对数（约等于 1.414）。        |
| [LOG10E](http://www.w3school.com.cn/jsref/jsref_log10e.asp)  | 返回以 10 为底的 e 的对数（约等于0.434）。        |
| [PI](http://www.w3school.com.cn/jsref/jsref_pi.asp)          | 返回圆周率（约等于3.14159）。                     |
| [SQRT1_2](http://www.w3school.com.cn/jsref/jsref_sqrt1_2.asp) | 返回返回 2 的平方根的倒数（约等于 0.707）。       |
| [SQRT2](http://www.w3school.com.cn/jsref/jsref_sqrt2.asp)    | 返回 2 的平方根（约等于 1.414）。                 |

### Math 对象方法

| 方法                                                         | 描述                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| [abs(x)](http://www.w3school.com.cn/jsref/jsref_abs.asp)     | 返回数的绝对值。                                             |
| [acos(x)](http://www.w3school.com.cn/jsref/jsref_acos.asp)   | 返回数的反余弦值。                                           |
| [asin(x)](http://www.w3school.com.cn/jsref/jsref_asin.asp)   | 返回数的反正弦值。                                           |
| [atan(x)](http://www.w3school.com.cn/jsref/jsref_atan.asp)   | 以介于 -PI/2 与 PI/2 弧度之间的数值来返回 x 的反正切值。     |
| [atan2(y,x)](http://www.w3school.com.cn/jsref/jsref_atan2.asp) | 返回从 x 轴到点 (x,y) 的角度（介于 -PI/2 与 PI/2 弧度之间）。 |
| [ceil(x)](http://www.w3school.com.cn/jsref/jsref_ceil.asp)   | 对数进行上舍入。                                             |
| [cos(x)](http://www.w3school.com.cn/jsref/jsref_cos.asp)     | 返回数的余弦。                                               |
| [exp(x)](http://www.w3school.com.cn/jsref/jsref_exp.asp)     | 返回 e 的指数。                                              |
| [floor(x)](http://www.w3school.com.cn/jsref/jsref_floor.asp) | 对数进行下舍入。                                             |
| [log(x)](http://www.w3school.com.cn/jsref/jsref_log.asp)     | 返回数的自然对数（底为e）。                                  |
| [max(x,y)](http://www.w3school.com.cn/jsref/jsref_max.asp)   | 返回 x 和 y 中的最高值。                                     |
| [min(x,y)](http://www.w3school.com.cn/jsref/jsref_min.asp)   | 返回 x 和 y 中的最低值。                                     |
| [pow(x,y)](http://www.w3school.com.cn/jsref/jsref_pow.asp)   | 返回 x 的 y 次幂。                                           |
| [random()](http://www.w3school.com.cn/jsref/jsref_random.asp) | 返回 0 ~ 1 之间的随机数。                                    |
| [round(x)](http://www.w3school.com.cn/jsref/jsref_round.asp) | 把数四舍五入为最接近的整数。                                 |
| [sin(x)](http://www.w3school.com.cn/jsref/jsref_sin.asp)     | 返回数的正弦。                                               |
| [sqrt(x)](http://www.w3school.com.cn/jsref/jsref_sqrt.asp)   | 返回数的平方根。                                             |
| [tan(x)](http://www.w3school.com.cn/jsref/jsref_tan.asp)     | 返回角的正切。                                               |
| [toSource()](http://www.w3school.com.cn/jsref/jsref_tosource_math.asp) | 返回该对象的源代码。                                         |
| [valueOf()](http://www.w3school.com.cn/jsref/jsref_valueof_math.asp) | 返回 Math 对象的原始值。                                     |

## RegExp 正则表达式对象

**RegExp 对象用于规定在文本中检索的内容。**

### 什么是 RegExp？

RegExp 是正则表达式的缩写。

当您检索某个文本时，可以使用一种模式来描述要检索的内容。RegExp 就是这种模式。

简单的模式可以是一个单独的字符。

更复杂的模式包括了更多的字符，并可用于解析、格式检查、替换等等。

您可以规定字符串中的检索位置，以及要检索的字符类型，等等。

## RegExp 对象

RegExp 对象表示正则表达式，它是对字符串执行模式匹配的强大工具。

### 直接量语法

```
/pattern/attributes
```

### 创建 RegExp 对象的语法：

```
new RegExp(pattern, attributes);
```

### 参数

参数 *pattern* 是一个字符串，指定了正则表达式的模式或其他正则表达式。

参数 *attributes* 是一个可选的字符串，包含属性 "g"、"i" 和 "m"，分别用于指定全局匹配、区分大小写的匹配和多行匹配。ECMAScript 标准化之前，不支持 m 属性。如果 *pattern* 是正则表达式，而不是字符串，则必须省略该参数。

### 返回值

一个新的 RegExp 对象，具有指定的模式和标志。如果参数 *pattern* 是正则表达式而不是字符串，那么 RegExp() 构造函数将用与指定的 RegExp 相同的模式和标志创建一个新的 RegExp 对象。

如果不用 new 运算符，而将 RegExp() 作为函数调用，那么它的行为与用 new 运算符调用时一样，只是当 *pattern* 是正则表达式时，它只返回 *pattern*，而不再创建一个新的 RegExp 对象。

### 抛出

SyntaxError - 如果 *pattern* 不是合法的正则表达式，或 *attributes* 含有 "g"、"i" 和 "m" 之外的字符，抛出该异常。

TypeError - 如果 *pattern* 是 RegExp 对象，但没有省略 *attributes* 参数，抛出该异常。

### 定义 RegExp

RegExp 对象用于存储检索模式。

通过 new 关键词来定义 RegExp 对象。以下代码定义了名为 patt1 的 RegExp 对象，其模式是 "e"：

```
var patt1=new RegExp("e");
```

当您使用该 RegExp 对象在一个字符串中检索时，将寻找的是字符 "e"。

## RegExp 对象的方法

RegExp 对象有 3 个方法：test()、exec() 以及 compile()。

### test()

test() 方法检索字符串中的指定值。返回值是 true 或 false。

**例子**：

```
var patt1=new RegExp("e");

document.write(patt1.test("The best things in life are free")); 
```

由于该字符串中存在字母 "e"，以上代码的输出将是：

```
true
```

[TIY](http://www.w3school.com.cn/tiy/t.asp?f=jseg_regexp_test)

### exec()

exec() 方法检索字符串中的指定值。返回值是被找到的值。如果没有发现匹配，则返回 null。

**例子 1：**

```
var patt1=new RegExp("e");

document.write(patt1.exec("The best things in life are free")); 
```

由于该字符串中存在字母 "e"，以上代码的输出将是：

```
e
```

[TIY](http://www.w3school.com.cn/tiy/t.asp?f=jseg_regexp_exec)

**例子 2：**

您可以向 RegExp 对象添加第二个参数，以设定检索。例如，如果需要找到所有某个字符的所有存在，则可以使用 "g" 参数 ("global")。

如需关于如何修改搜索模式的完整信息，请访问我们的 [RegExp 对象参考手册](http://www.w3school.com.cn/jsref/jsref_obj_regexp.asp)。

在使用 "g" 参数时，exec() 的工作原理如下：

- 找到第一个 "e"，并存储其位置
- 如果再次运行 exec()，则从存储的位置开始检索，并找到下一个 "e"，并存储其位置

```
var patt1=new RegExp("e","g");
do
{
result=patt1.exec("The best things in life are free");
document.write(result);
}
while (result!=null) 
```

由于这个字符串中 6 个 "e" 字母，代码的输出将是：

```
eeeeeenull
```

[TIY](http://www.w3school.com.cn/tiy/t.asp?f=jseg_regexp_exec_2)

### compile()

compile() 方法用于改变 RegExp。

compile() 既可以改变检索模式，也可以添加或删除第二个参数。

**例子：**

```
var patt1=new RegExp("e");

document.write(patt1.test("The best things in life are free"));

patt1.compile("d");

document.write(patt1.test("The best things in life are free"));
```

由于字符串中存在 "e"，而没有 "d"，以上代码的输出是：

```
truefalse
```

[TIY](http://www.w3school.com.cn/tiy/t.asp?f=jseg_regexp_compile)

### 完整的 RegExp 对象参考手册

如需可与 RegExp 对象一同使用所有属性和方法的完整信息，请访问我们的 [RegExp 对象参考手册](http://www.w3school.com.cn/jsref/jsref_obj_regexp.asp)。

这个参考手册包含了对 RegExp 对象中每个属性和方法的详细描述，以及使用的例子。

### 修饰符

| 修饰符                                                   | 描述                                                     |
| -------------------------------------------------------- | -------------------------------------------------------- |
| [i](http://www.w3school.com.cn/jsref/jsref_regexp_i.asp) | 执行对大小写不敏感的匹配。                               |
| [g](http://www.w3school.com.cn/jsref/jsref_regexp_g.asp) | 执行全局匹配（查找所有匹配而非在找到第一个匹配后停止）。 |
| m                                                        | 执行多行匹配。                                           |

### 方括号

方括号用于查找某个范围内的字符：

| 表达式                                                       | 描述                               |
| ------------------------------------------------------------ | ---------------------------------- |
| [[abc\]](http://www.w3school.com.cn/jsref/jsref_regexp_charset.asp) | 查找方括号之间的任何字符。         |
| [[^abc\]](http://www.w3school.com.cn/jsref/jsref_regexp_charset_not.asp) | 查找任何不在方括号之间的字符。     |
| [0-9]                                                        | 查找任何从 0 至 9 的数字。         |
| [a-z]                                                        | 查找任何从小写 a 到小写 z 的字符。 |
| [A-Z]                                                        | 查找任何从大写 A 到大写 Z 的字符。 |
| [A-z]                                                        | 查找任何从大写 A 到小写 z 的字符。 |
| [adgk]                                                       | 查找给定集合内的任何字符。         |
| [^adgk]                                                      | 查找给定集合外的任何字符。         |
| (red\|blue\|green)                                           | 查找任何指定的选项。               |

### 元字符

元字符（Metacharacter）是拥有特殊含义的字符：

| 元字符                                                       | 描述                                        |
| ------------------------------------------------------------ | ------------------------------------------- |
| [.](http://www.w3school.com.cn/jsref/jsref_regexp_dot.asp)   | 查找单个字符，除了换行和行结束符。          |
| [\w](http://www.w3school.com.cn/jsref/jsref_regexp_wordchar.asp) | 查找单词字符。                              |
| [\W](http://www.w3school.com.cn/jsref/jsref_regexp_wordchar_non.asp) | 查找非单词字符。                            |
| [\d](http://www.w3school.com.cn/jsref/jsref_regexp_digit.asp) | 查找数字。                                  |
| [\D](http://www.w3school.com.cn/jsref/jsref_regexp_digit_non.asp) | 查找非数字字符。                            |
| [\s](http://www.w3school.com.cn/jsref/jsref_regexp_whitespace.asp) | 查找空白字符。                              |
| [\S](http://www.w3school.com.cn/jsref/jsref_regexp_whitespace_non.asp) | 查找非空白字符。                            |
| [\b](http://www.w3school.com.cn/jsref/jsref_regexp_begin.asp) | 匹配单词边界。                              |
| [\B](http://www.w3school.com.cn/jsref/jsref_regexp_begin_not.asp) | 匹配非单词边界。                            |
| \0                                                           | 查找 NUL 字符。                             |
| [\n](http://www.w3school.com.cn/jsref/jsref_regexp_newline.asp) | 查找换行符。                                |
| \f                                                           | 查找换页符。                                |
| \r                                                           | 查找回车符。                                |
| \t                                                           | 查找制表符。                                |
| \v                                                           | 查找垂直制表符。                            |
| [\xxx](http://www.w3school.com.cn/jsref/jsref_regexp_octal.asp) | 查找以八进制数 xxx 规定的字符。             |
| [\xdd](http://www.w3school.com.cn/jsref/jsref_regexp_hex.asp) | 查找以十六进制数 dd 规定的字符。            |
| [\uxxxx](http://www.w3school.com.cn/jsref/jsref_regexp_unicode_hex.asp) | 查找以十六进制数 xxxx 规定的 Unicode 字符。 |

### 量词

| 量词                                                         | 描述                                        |
| ------------------------------------------------------------ | ------------------------------------------- |
| [n+](http://www.w3school.com.cn/jsref/jsref_regexp_onemore.asp) | 匹配任何包含至少一个 n 的字符串。           |
| [n*](http://www.w3school.com.cn/jsref/jsref_regexp_zeromore.asp) | 匹配任何包含零个或多个 n 的字符串。         |
| [n?](http://www.w3school.com.cn/jsref/jsref_regexp_zeroone.asp) | 匹配任何包含零个或一个 n 的字符串。         |
| [n{X}](http://www.w3school.com.cn/jsref/jsref_regexp_nx.asp) | 匹配包含 X 个 n 的序列的字符串。            |
| [n{X,Y}](http://www.w3school.com.cn/jsref/jsref_regexp_nxy.asp) | 匹配包含 X 至 Y 个 n 的序列的字符串。       |
| [n{X,}](http://www.w3school.com.cn/jsref/jsref_regexp_nxcomma.asp) | 匹配包含至少 X 个 n 的序列的字符串。        |
| [n$](http://www.w3school.com.cn/jsref/jsref_regexp_ndollar.asp) | 匹配任何结尾为 n 的字符串。                 |
| [^n](http://www.w3school.com.cn/jsref/jsref_regexp_ncaret.asp) | 匹配任何开头为 n 的字符串。                 |
| [?=n](http://www.w3school.com.cn/jsref/jsref_regexp_nfollow.asp) | 匹配任何其后紧接指定字符串 n 的字符串。     |
| [?!n](http://www.w3school.com.cn/jsref/jsref_regexp_nfollow_not.asp) | 匹配任何其后没有紧接指定字符串 n 的字符串。 |

### RegExp 对象属性

| 属性                                                         | 描述                                     | FF   | IE   |
| ------------------------------------------------------------ | ---------------------------------------- | ---- | ---- |
| [global](http://www.w3school.com.cn/jsref/jsref_regexp_global.asp) | RegExp 对象是否具有标志 g。              | 1    | 4    |
| [ignoreCase](http://www.w3school.com.cn/jsref/jsref_regexp_ignorecase.asp) | RegExp 对象是否具有标志 i。              | 1    | 4    |
| [lastIndex](http://www.w3school.com.cn/jsref/jsref_lastindex_regexp.asp) | 一个整数，标示开始下一次匹配的字符位置。 | 1    | 4    |
| [multiline](http://www.w3school.com.cn/jsref/jsref_multiline_regexp.asp) | RegExp 对象是否具有标志 m。              | 1    | 4    |
| [source](http://www.w3school.com.cn/jsref/jsref_source_regexp.asp) | 正则表达式的源文本。                     | 1    | 4    |

### RegExp 对象方法

| 方法                                                         | 描述                                               | FF   | IE   |
| ------------------------------------------------------------ | -------------------------------------------------- | ---- | ---- |
| [compile](http://www.w3school.com.cn/jsref/jsref_regexp_compile.asp) | 编译正则表达式。                                   | 1    | 4    |
| [exec](http://www.w3school.com.cn/jsref/jsref_exec_regexp.asp) | 检索字符串中指定的值。返回找到的值，并确定其位置。 | 1    | 4    |
| [test](http://www.w3school.com.cn/jsref/jsref_test_regexp.asp) | 检索字符串中指定的值。返回 true 或 false。         | 1    | 4    |

### 支持正则表达式的 String 对象的方法

| 方法                                                         | 描述                             | FF   | IE   |
| ------------------------------------------------------------ | -------------------------------- | ---- | ---- |
| [search](http://www.w3school.com.cn/jsref/jsref_search.asp)  | 检索与正则表达式相匹配的值。     | 1    | 4    |
| [match](http://www.w3school.com.cn/jsref/jsref_match.asp)    | 找到一个或多个正则表达式的匹配。 | 1    | 4    |
| [replace](http://www.w3school.com.cn/jsref/jsref_replace.asp) | 替换与正则表达式匹配的子串。     | 1    | 4    |
| [split](http://www.w3school.com.cn/jsref/jsref_split.asp)    | 把字符串分割为字符串数组。       | 1    | 4    |



# Window - 浏览器对象模型

## Window - 浏览器对象模型简介

**浏览器对象模型 (BOM) 使 JavaScript 有能力与浏览器“对话”。**

### 浏览器对象模型 (BOM)

浏览器对象模型（Browser Object Model）尚无正式标准。

由于现代浏览器已经（几乎）实现了 JavaScript 交互性方面的相同方法和属性，因此常被认为是 BOM 的方法和属性。

### Window 对象

所有浏览器都支持 *window* 对象。它表示浏览器窗口。

所有 JavaScript 全局对象、函数以及变量均自动成为 window 对象的成员。

全局变量是 window 对象的属性。

全局函数是 window 对象的方法。

甚至 HTML DOM 的 document 也是 window 对象的属性之一：

```
window.document.getElementById("header");
```

与此相同：

```
document.getElementById("header");
```

### Window 尺寸

有三种方法能够确定浏览器窗口的尺寸（浏览器的视口，不包括工具栏和滚动条）。

对于Internet Explorer、Chrome、Firefox、Opera 以及 Safari：

- window.innerHeight - 浏览器窗口的内部高度
- window.innerWidth - 浏览器窗口的内部宽度

对于 Internet Explorer 8、7、6、5：

- document.documentElement.clientHeight
- document.documentElement.clientWidth

或者

- document.body.clientHeight
- document.body.clientWidth

实用的 JavaScript 方案（涵盖所有浏览器）：

**实例**

```
var w=window.innerWidth
|| document.documentElement.clientWidth
|| document.body.clientWidth;

var h=window.innerHeight
|| document.documentElement.clientHeight
|| document.body.clientHeight;
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_window_innerwidth_innerheight)

该例显示浏览器窗口的高度和宽度：（不包括工具栏/滚动条）

### 其他 Window 方法

一些其他方法：

- window.open() - 打开新窗口
- window.close() - 关闭当前窗口
- window.moveTo() - 移动当前窗口
- window.resizeTo() - 调整当前窗口的尺寸

##  Window Screen



**window.screen 对象包含有关用户屏幕的信息。**

### Window Screen

*window.screen* 对象在编写时可以不使用 window 这个前缀。

一些属性：

- screen.availWidth - 可用的屏幕宽度
- screen.availHeight - 可用的屏幕高度

### Window Screen 可用宽度

screen.availWidth 属性返回访问者屏幕的宽度，以像素计，减去界面特性，比如窗口任务栏。

**实例**

返回您的屏幕的可用宽度：

```
<script>

document.write("可用宽度：" + screen.availWidth);

</script>
```

以上代码输出为：

```
可用宽度：1536
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_window_screen_availwidth)

### Window Screen 可用高度

screen.availHeight 属性返回访问者屏幕的高度，以像素计，减去界面特性，比如窗口任务栏。

**实例**

返回您的屏幕的可用高度：

```
<script>

document.write("可用高度：" + screen.availHeight);

</script>
```

以上代码输出为：

```
可用高度：834
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_window_screen_availheight)

## Window Location



window.location 对象用于获得当前页面的地址 (URL)，并把浏览器重定向到新的页面。

### Window Location

*window.location* 对象在编写时可不使用 window 这个前缀。

一些例子：

- location.hostname 返回 web 主机的域名
- location.pathname 返回当前页面的路径和文件名
- location.port 返回 web 主机的端口 （80 或 443）
- location.protocol 返回所使用的 web 协议（http:// 或 https://）

### Window Location Href

location.href 属性返回当前页面的 URL。

**实例**

返回（当前页面的）整个 URL：

```
<script>

document.write(location.href);

</script>
```

以上代码输出为：

```
http://www.w3school.com.cn/js/js_window_location.asp
```

### Window Location Pathname

location.pathname 属性返回 URL 的路径名。

**实例**

返回当前 URL 的路径名：

```
<script>

document.write(location.pathname);

</script>
```

以上代码输出为：

```
/js/js_window_location.asp
```

### Window Location Assign

location.assign() 方法加载新的文档。

**实例**

加载一个新的文档：

```
<html>
<head>
<script>
function newDoc()
  {
  window.location.assign("http://www.w3school.com.cn")
  }
</script>
</head>
<body>

<input type="button" value="加载新文档" onclick="newDoc()">

</body>
</html>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_location_assign)

## Window Navigator



window.navigator 对象包含有关访问者浏览器的信息。

### Window Navigator

window.navigator 对象在编写时可不使用 window 这个前缀。

**实例**

```
<div id="example"></div>

<script>

txt = "<p>Browser CodeName: " + navigator.appCodeName + "</p>";
txt+= "<p>Browser Name: " + navigator.appName + "</p>";
txt+= "<p>Browser Version: " + navigator.appVersion + "</p>";
txt+= "<p>Cookies Enabled: " + navigator.cookieEnabled + "</p>";
txt+= "<p>Platform: " + navigator.platform + "</p>";
txt+= "<p>User-agent header: " + navigator.userAgent + "</p>";
txt+= "<p>User-agent language: " + navigator.systemLanguage + "</p>";

document.getElementById("example").innerHTML=txt;

</script>
```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=js_navigator_all)

警告：来自 navigator 对象的信息具有误导性，不应该被用于检测浏览器版本，这是因为：

- navigator 数据可被浏览器使用者更改
- 浏览器无法报告晚于浏览器发布的新操作系统

### 浏览器检测

由于 navigator 可误导浏览器检测，使用对象检测可用来嗅探不同的浏览器。

由于不同的浏览器支持不同的对象，您可以使用对象来检测浏览器。例如，由于只有 Opera 支持属性 "window.opera"，您可以据此识别出 Opera。

例子：if (window.opera) {...some action...}

## JavaScript 消息框



**可以在 JavaScript 中创建三种消息框：警告框、确认框、提示框。**

### 实例参考

- [警告框](http://www.w3school.com.cn/tiy/t.asp?f=jseg_alert)
- [带有折行的警告框](http://www.w3school.com.cn/tiy/t.asp?f=jseg_alert2)
- [确认框](http://www.w3school.com.cn/tiy/t.asp?f=jseg_confirm)
- [提示框](http://www.w3school.com.cn/tiy/t.asp?f=jseg_prompt)

### 警告框

警告框经常用于确保用户可以得到某些信息。

当警告框出现后，用户需要点击确定按钮才能继续进行操作。

**语法**：

```
alert("文本")
```

### 确认框

确认框用于使用户可以验证或者接受某些信息。

当确认框出现后，用户需要点击确定或者取消按钮才能继续进行操作。

如果用户点击确认，那么返回值为 true。如果用户点击取消，那么返回值为 false。

**语法**：

```
confirm("文本")
```

### 提示框

提示框经常用于提示用户在进入页面前输入某个值。

当提示框出现后，用户需要输入某个值，然后点击确认或取消按钮才能继续操纵。

如果用户点击确认，那么返回值为输入的值。如果用户点击取消，那么返回值为 null。

**语法**：

```
prompt("文本","默认值")
```

## JavaScript 计时



**通过使用 JavaScript，我们有能力做到在一个设定的时间间隔之后来执行代码，而不是在函数被调用后立即执行。我们称之为计时事件。**

### 实例参考

- [简单的计时](http://www.w3school.com.cn/tiy/t.asp?f=jseg_timing1)

  单击本例中的按钮后，会在 5 秒后弹出一个警告框。

- [另一个简单的计时](http://www.w3school.com.cn/tiy/t.asp?f=jseg_timing2)

  本例中的程序会执行 2 秒、4 秒和 6 秒的计时。

- [在一个无穷循环中的计时事件](http://www.w3school.com.cn/tiy/t.asp?f=jseg_timing_infinite)

  在本例中，单击开始计时按钮后，程序开始从 0 以秒计时。

- [带有停止按钮的无穷循环中的计时事件](http://www.w3school.com.cn/tiy/t.asp?f=jseg_timing_stop)

  在本例中，点击计数按钮后根据用户输入的数值开始倒计时，点击停止按钮停止计时。

- [使用计时事件制作的钟表](http://www.w3school.com.cn/tiy/t.asp?f=jseg_timing_clock)

  一个 JavaScript 小时钟

### JavaScript 计时事件

通过使用 JavaScript，我们有能力作到在一个设定的时间间隔之后来执行代码，而不是在函数被调用后立即执行。我们称之为计时事件。

在 JavaScritp 中使用计时事件是很容易的，两个关键方法是:

- setTimeout()

  未来的某时执行代码

- clearTimeout()

  取消setTimeout()

### setTimeout()

**语法**

```
var t=setTimeout("javascript语句",毫秒)
```

setTimeout() 方法会返回某个值。在上面的语句中，值被储存在名为 t 的变量中。假如你希望取消这个 setTimeout()，你可以使用这个变量名来指定它。

setTimeout() 的第一个参数是含有 JavaScript 语句的字符串。这个语句可能诸如 "alert('5 seconds!')"，或者对函数的调用，诸如 alertMsg()"。

第二个参数指示从当前起多少毫秒后执行第一个参数。

提示：1000 毫秒等于一秒。

**实例**

当下面这个例子中的按钮被点击时，一个提示框会在5秒中后弹出。

```
<html>
<head>
<script type="text/javascript">
function timedMsg()
 {
 var t=setTimeout("alert('5 seconds!')",5000)
 }
</script>
</head>

<body>
<form>
<input type="button" value="Display timed alertbox!" onClick="timedMsg()">
</form>
</body>
</html>
```

### 实例 - 无穷循环

要创建一个运行于无穷循环中的计时器，我们需要编写一个函数来调用其自身。在下面的例子中，当按钮被点击后，输入域便从 0 开始计数。

```
<html>

<head>
<script type="text/javascript">
var c=0
var t
function timedCount()
 {
 document.getElementById('txt').value=c
 c=c+1
 t=setTimeout("timedCount()",1000)
 }
</script>
</head>

<body>
<form>
<input type="button" value="Start count!" onClick="timedCount()">
<input type="text" id="txt">
</form>
</body>

</html>
```

### clearTimeout()

**语法**

```
clearTimeout(setTimeout_variable)
```

**实例**

下面的例子和上面的无穷循环的例子相似。唯一的不同是，现在我们添加了一个 "Stop Count!" 按钮来停止这个计数器：

```
<html>

<head>
<script type="text/javascript">
var c=0
var t

function timedCount()
 {
 document.getElementById('txt').value=c
 c=c+1
 t=setTimeout("timedCount()",1000)
 }

function stopCount()
 {
 clearTimeout(t)
 }
</script>
</head>

<body>
<form>
<input type="button" value="Start count!" onClick="timedCount()">
<input type="text" id="txt">
<input type="button" value="Stop count!" onClick="stopCount()">
</form>
</body>

</html>
```

## JavaScript Cookies

**cookie 用来识别用户。**

**实例**

- [创建一个欢迎 cookie](http://www.w3school.com.cn/tiy/t.asp?f=jseg_cookie_username)

  利用用户在提示框中输入的数据创建一个 JavaScript Cookie，当该用户再次访问该页面时，根据 cookie 中的信息发出欢迎信息。

### 什么是cookie?

cookie 是存储于访问者的计算机中的变量。每当同一台计算机通过浏览器请求某个页面时，就会发送这个 cookie。你可以使用 JavaScript 来创建和取回 cookie 的值。

### 有关cookie的例子：

- 名字 cookie

  当访问者首次访问页面时，他或她也许会填写他/她们的名字。名字会存储于 cookie 中。当访问者再次访问网站时，他们会收到类似 "Welcome John Doe!" 的欢迎词。而名字则是从 cookie 中取回的。

- 密码 cookie

  当访问者首次访问页面时，他或她也许会填写他/她们的密码。密码也可被存储于 cookie 中。当他们再次访问网站时，密码就会从 cookie 中取回。

- 日期 cookie

  当访问者首次访问你的网站时，当前的日期可存储于 cookie 中。当他们再次访问网站时，他们会收到类似这样的一条消息："Your last visit was on Tuesday August 11, 2005!"。日期也是从 cookie 中取回的。

### 创建和存储 cookie

在这个例子中我们要创建一个存储访问者名字的 cookie。当访问者首次访问网站时，他们会被要求填写姓名。名字会存储于 cookie 中。当访问者再次访问网站时，他们就会收到欢迎词。

首先，我们会创建一个可在 cookie 变量中存储访问者姓名的函数：

```
function setCookie(c_name,value,expiredays)
{
var exdate=new Date()
exdate.setDate(exdate.getDate()+expiredays)
document.cookie=c_name+ "=" +escape(value)+
((expiredays==null) ? "" : ";expires="+exdate.toGMTString())
}
```

上面这个函数中的参数存有 cookie 的名称、值以及过期天数。

在上面的函数中，我们首先将天数转换为有效的日期，然后，我们将 cookie 名称、值及其过期日期存入 document.cookie 对象。

之后，我们要创建另一个函数来检查是否已设置 cookie：

```
function getCookie(c_name)
{
if (document.cookie.length>0)
  {
  c_start=document.cookie.indexOf(c_name + "=")
  if (c_start!=-1)
    { 
    c_start=c_start + c_name.length+1 
    c_end=document.cookie.indexOf(";",c_start)
    if (c_end==-1) c_end=document.cookie.length
    return unescape(document.cookie.substring(c_start,c_end))
    } 
  }
return ""
}
```

上面的函数首先会检查 document.cookie 对象中是否存有 cookie。假如 document.cookie 对象存有某些 cookie，那么会继续检查我们指定的 cookie 是否已储存。如果找到了我们要的 cookie，就返回值，否则返回空字符串。

最后，我们要创建一个函数，这个函数的作用是：如果 cookie 已设置，则显示欢迎词，否则显示提示框来要求用户输入名字。

```
function checkCookie()
{
username=getCookie('username')
if (username!=null && username!="")
  {alert('Welcome again '+username+'!')}
else 
  {
  username=prompt('Please enter your name:',"")
  if (username!=null && username!="")
    {
    setCookie('username',username,365)
    }
  }
}
```

这是所有的代码：

```
<html>
<head>
<script type="text/javascript">
function getCookie(c_name)
{
if (document.cookie.length>0)
  {
  c_start=document.cookie.indexOf(c_name + "=")
  if (c_start!=-1)
    { 
    c_start=c_start + c_name.length+1 
    c_end=document.cookie.indexOf(";",c_start)
    if (c_end==-1) c_end=document.cookie.length
    return unescape(document.cookie.substring(c_start,c_end))
    } 
  }
return ""
}

function setCookie(c_name,value,expiredays)
{
var exdate=new Date()
exdate.setDate(exdate.getDate()+expiredays)
document.cookie=c_name+ "=" +escape(value)+
((expiredays==null) ? "" : ";expires="+exdate.toGMTString())
}

function checkCookie()
{
username=getCookie('username')
if (username!=null && username!="")
  {alert('Welcome again '+username+'!')}
else 
  {
  username=prompt('Please enter your name:',"")
  if (username!=null && username!="")
    {
    setCookie('username',username,365)
    }
  }
}
</script>
</head>

<body onLoad="checkCookie()">
</body>
</html>
```

- 
    