

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