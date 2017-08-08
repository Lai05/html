### <!DOCTYPE> 声明
< !DOCTYPE> 声明位于文档中的最前面的位置，处于 <html> 标签之前。
  
< !DOCTYPE> 声明不是一个 HTML 标签；它是用来告知 Web 浏览器页面使用了哪种 HTML 版本。

< !DOCTYPE> 标签没有结束标签

< !DOCTYPE> 声明不区分大小写
  
#### 通用声明
HTML5：
```
<!DOCTYPE html>
```

### 中文编码
目前在大部分浏览器中，直接输出中文会出现中文乱码的情况，这时候我们就需要在头部将字符声明为 UTF-8。
```
<head>
<meta charset="UTF-8">
<title>页面标题</title>
</head>
```

### HTML属性
属性值应该始终被包括在引号内,双引号是最常用的，不过使用单引号也没有问题。

在某些个别的情况下，比如属性值本身就含有双引号，那么您必须使用单引号，例如：name='John "ShotGun" Nelson'

属性和属性值对大小写不敏感

### HTML  < head> 元素
< head> 元素包含了所有的头部标签元素。在 <head>元素中你可以插入脚本（scripts）, 样式文件（CSS），及各种meta信息

可以添加在头部区域的元素标签为: <title>, <style>, <meta>, <link>, <script>, <noscript>, and <base>.
  
### HTML < base> 元素
< base> 标签为HTML文档中所有的链接标签的默认链接

### HTML < link> 元素
< link> 标签定义了文档与外部资源之间的关系。

< link> 标签通常用于链接到样式表:
```
<head>
<link rel="stylesheet" type="text/css" href="mystyle.css">
</head>
```

### HTML 图像标签
[< img >]()定义图像

[< map >]()定义图像地图

[< area >](http://www.runoob.com/tags/tag-area.html)定义图像地图中的可点击区域

  1、距形：(左上角顶点坐标为(x1,y1)，右下角顶点坐标为(x2,y2))
```
<area shape="rect" coords="x1,y1,x2,y2" href=url>
```
2、圆形：(圆心坐标为(X1,y1)，半径为r)
```
<area shape="circle" coords="x1,y1,r" href=url>
```
3、多边形：(各顶点坐标依次为(x1,y1)、(x2,y2)、(x3,y3) ......)
```
<area shape="poly" coords="x1,y1,x2,y2 ......" href=url>
```
### HTML 表格
表格由 < table> 标签来定义。每个表格均有若干行（由 < tr> 标签定义），每行被分割为若干单元格（由 < td> 标签定义）。
  
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
  
### HTML 表格表头
表格的表头使用 < th> 标签进行定义。大多数浏览器会把表头显示为粗体居中的文本
  
#### 跨行或跨列的表格单元格
单元格跨两格:
```
<table border="1">
<tr>
  <th>Name</th>
  <th colspan="2">Telephone</th>
</tr>
<tr>  
  <td>Bill Gates</td>  
  <td>555 77 854</td>  
  <td>555 77 855</td>
</tr>
</table>
```
单元格跨两列:
```
<table border="1">
<tr>
  <th>First Name:</th> 
  <td>Bill Gates</td>
</tr>
<tr>  
  <th rowspan="2">Telephone:</th>  
  <td>555 77 854</td>
</tr>
<tr>  
  <td>555 77 855</td>
</tr>
</table>
```
### HTML < span> 标签
< span> 用于对文档中的行内元素进行组合。

< span> 标签没有固定的格式表现。当对它应用样式时，它才会产生视觉上的变化。如果不对 < span> 应用样式，那么 < span> 元素中的文本与其他文本不会任何视觉上的差异。

使用 < span> 元素对文本中的一部分进行着色：

```
<p>我的母亲有 <span style="color:blue">蓝色</span> 的眼睛。</p>
```
### HTML 表单
表单是一个包含表单元素的区域。

表单元素是允许用户在表单中输入内容,比如：文本域(textarea)、下拉列表、单选框(radio-buttons)、复选框(checkboxes)等等。
##### 表单使用表单标签 < form> 来设置:
```
<form>
.
input 元素
.
</form>
```
##### HTML 表单输入元素
多数情况下被用到的表单标签是输入标签（<input>）。输入类型是由类型属性（type）定义的。

大多数经常被用到的输入类型如下：
###### 文本域（Text Fields）
文本域通过< input type="text"> 标签来设定，当用户要在表单中键入字母、数字等内容时，就会用到文本域。
```
<form>
First name: <input type="text" name="firstname">
<br>
Last name: <input type="text" name="lastname">
</form>
```
###### 密码字段
密码字段通过标签< input type="password"> 来定义:
```
<form>
Password: <input type="password" name="pwd">
</form>
```
###### 单选按钮（Radio Buttons）
< input type="radio"> 标签定义了表单单选框选项
```
<form>
  <input type="radio" name="sex" value="male">Male
  <br>
  <input type="radio" name="sex" value="female">Female
</form>
```
###### 复选框（Checkboxes）
< input type="checkbox"> 定义了复选框. 用户需要从若干给定的选择中选取一个或若干选项。
```
<form>
  <input type="checkbox" name="vehicle" value="Bike">I have a bike
  <br>
  <input type="checkbox" name="vehicle" value="Car">I have a car 
</form>
```
###### 提交按钮(Submit Button)
< input type="submit"> 定义了提交按钮.当用户单击确认按钮时，表单的内容会被传送到另一个文件。
```
<form name="input" action="html_form_action.php" method="get">
  Username: <input type="text" name="user"><input type="submit" value="Submit">
</form>
```
###### 下拉框
< select> 定义了下拉选项列表

```
<form>
<select name="cars">
<option value="volvo">Volvo</option>
<option value="saab">Saab</option>
<option value="fiat" selected>Fiat</option>
<option value="audi">Audi</option>
</select>
</form>
```
#### HTML 字符实体
###### 不间断空格(Non-breaking Space)
HTML的常用字符实体是不间断空格(&nbsp;)。浏览器总是会截短 HTML 页面中的空格。如果您在文本中写 10 个空格，在显示该页面之前，浏览器会删除它们中的 9 个。如需在页面中增加空格的数量，您需要使用 &nbsp; 字符实体。
###### 结合音标符
| à | a&#768|

| á | a&#769|

| â | a&#770|

| ã | a&#771|
#### 文本格式化（Formatting）
```
<b>粗体文本</b>
<code>计算机代码</code>
<em>强调文本</em>
<i>斜体文本</i>
<kbd>键盘输入</kbd> 
<pre>预格式化文本</pre>
<small>更小的文本</small>
<strong>重要的文本</strong>
 
<abbr> （缩写）
<address> （联系信息）
<bdo> （文字方向）
<blockquote> （从另一个源引用的部分）
<cite> （工作的名称）
<del> （删除的文本）
<ins> （插入的文本）
<sub> （下标文本）
<sup> （上标文本）
```
#### 链接（Links）
```
普通的链接：<a href="http://www.example.com/">链接文本</a>
图像链接： <a href="http://www.example.com/"><img src="URL" alt="替换文本"></a>
邮件链接： <a href="mailto:webmaster@example.com">发送e-mail</a>
书签：
<a id="tips">提示部分</a>
<a href="#tips">跳到提示部分</a>
```
### HTML5 新元素
###### < canvas> 新元素
  < canvas> 元素(画布)用于图形的绘制，通过脚本 (通常是JavaScript)来完成.
###### 使用 JavaScript 来绘制图像
canvas 元素本身是没有绘图能力的。所有的绘制工作必须在 JavaScript 内部完成：

首先，找到 < canvas> 元素:
```
var c=document.getElementById("myCanvas");
```
然后，创建 context 对象：
```
var ctx=c.getContext("2d");
```
getContext("2d") 对象是内建的 HTML5 对象，拥有多种绘制路径、矩形、圆形、字符以及添加图像的方法。
下面的两行代码绘制一个红色的矩形：
```
ctx.fillStyle="#FF0000";
ctx.fillRect(0,0,150,75);
```
设置fillStyle属性可以是CSS颜色，渐变，或图案。
fillStyle 默认设置是#000000（黑色）。fillRect(x,y,width,height) 方法定义了矩形当前的填充方式。
###### Canvas  路径
  在Canvas上画线，我们将使用以下方法：
  
  moveTo(x,y) 定义线条开始坐标
  
  lineTo(x,y) 定义线条结束坐标
 
 定义开始坐标(0,0), 和结束坐标 (200,100)。然后使用 stroke() 方法来绘制线条:
 ```
var c=document.getElementById("myCanvas");
var ctx=c.getContext("2d");
ctx.moveTo(0,0);
ctx.lineTo(200,100);
ctx.stroke();
```
在canvas中绘制圆形, 我们将使用以下方法:

arc(x,y,r,start,stop)

实际上我们在绘制圆形时使用了 "ink" 的方法, 比如 stroke() 或者 fill().
```
var c=document.getElementById("myCanvas");
var ctx=c.getContext("2d");
ctx.beginPath();
ctx.arc(95,50,40,0,2*Math.PI);
ctx.stroke();
```
##### Canvas 文本
使用 canvas 绘制文本，重要的属性和方法如下：

font - 定义字体

fillText(text,x,y) - 在 canvas 上绘制实心的文本

strokeText(text,x,y) - 在 canvas 上绘制空心的文本

使用 "Arial" 字体在画布上绘制一个高 30px 的文字（实心）：
```
var c=document.getElementById("myCanvas");
var ctx=c.getContext("2d");
ctx.font="30px Arial";
ctx.fillText("Hello World",10,50);
```
使用 "Arial" 字体在画布上绘制一个高 30px 的文字（空心）：
```
var c=document.getElementById("myCanvas");
var ctx=c.getContext("2d");
ctx.font="30px Arial";
ctx.strokeText("Hello World",10,50);
```
###### Canvas - 渐变
渐变可以填充在矩形, 圆形, 线条, 文本等等, 各种形状可以自己定义不同的颜色。

以下有两种不同的方式来设置Canvas渐变：

createLinearGradient(x,y,x1,y1) - 创建线条渐变

createRadialGradient(x,y,r,x1,y1,r1) - 创建一个径向/圆渐变

当我们使用渐变对象，必须使用两种或两种以上的停止颜色。

addColorStop()方法指定颜色停止，参数使用坐标来描述，可以是0至1.

使用渐变，设置fillStyle或strokeStyle的值为 渐变，然后绘制形状，如矩形，文本，或一条线。

使用 createLinearGradient():

创建一个线性渐变。使用渐变填充矩形:
```
var c=document.getElementById("myCanvas");
var ctx=c.getContext("2d");
 
// 创建渐变
var grd=ctx.createLinearGradient(0,0,200,0);
grd.addColorStop(0,"red");
grd.addColorStop(1,"white");
 
// 填充渐变
ctx.fillStyle=grd;
ctx.fillRect(10,10,150,80);
```
使用 createRadialGradient():

创建一个径向/圆渐变。使用渐变填充矩形：
```
var c=document.getElementById("myCanvas");
var ctx=c.getContext("2d");
 
// 创建渐变
var grd=ctx.createRadialGradient(75,50,5,90,60,100);
grd.addColorStop(0,"red");
grd.addColorStop(1,"white");
 
// 填充渐变
ctx.fillStyle=grd;
ctx.fillRect(10,10,150,80);
```
###### Canvas - 图像
把一幅图像放置到画布上, 使用以下方法:

drawImage(image,x,y)

把一幅图像放置到画布上:
```
var c=document.getElementById("myCanvas");
var ctx=c.getContext("2d");
var img=document.getElementById("scream");
ctx.drawImage(img,10,10);
```
#### HTML5 拖放（Drag 和 Drop）
HTML5 拖放实例
```
<!DOCTYPE HTML>
<html>
<head>
<meta charset="utf-8"> 
<title>菜鸟教程(runoob.com)</title>
<style type="text/css">
#div1 {width:350px;height:70px;padding:10px;border:1px solid #aaaaaa;}
</style>
<script>
function allowDrop(ev)
{
    ev.preventDefault();
}
 
function drag(ev)
{
    ev.dataTransfer.setData("Text",ev.target.id);
}
 
function drop(ev)
{
    ev.preventDefault();
    var data=ev.dataTransfer.getData("Text");
    ev.target.appendChild(document.getElementById(data));
}
</script>
</head>
<body>
 
<p>拖动 RUNOOB.COM 图片到矩形框中:</p>
 
<div id="div1" ondrop="drop(event)" ondragover="allowDrop(event)"></div>
<br>
<img id="drag1" src="/images/logo.png" draggable="true" ondragstart="drag(event)" width="336" height="69">
 
</body>
</html>
```
###### 设置元素为可拖放
首先，为了使元素可拖动，把 draggable 属性设置为 true ：
```
<img draggable="true">
```
###### 拖动什么 - ondragstart 和 setData()
然后，规定当元素被拖动时，会发生什么。

在上面的例子中，ondragstart 属性调用了一个函数，drag(event)，它规定了被拖动的数据。

dataTransfer.setData() 方法设置被拖数据的数据类型和值：
```
function drag(ev){    
  ev.dataTransfer.setData("Text",ev.target.id);
  }
```
在这个例子中，数据类型是 "Text"，值是可拖动元素的 id ("drag1")。
###### 放到何处  ondragover
ondragover 事件规定在何处放置被拖动的数据。

默认地，无法将数据/元素放置到其他元素中。如果需要设置允许放置，我们必须阻止对元素的默认处理方式。

这要通过调用 ondragover 事件的 event.preventDefault() 方法：
```
event.preventDefault()
```
###### 进行放置 ondrop
当放置被拖数据时，会发生 drop 事件。

在上面的例子中，ondrop 属性调用了一个函数，drop(event)：
```
function drop(ev){    
  ev.preventDefault();    
  var data=ev.dataTransfer.getData("Text");    
  ev.target.appendChild(document.getElementById(data));
  }
```
代码解释：

调用 preventDefault() 来避免浏览器对数据的默认处理（drop 事件的默认行为是以链接形式打开）

通过 dataTransfer.getData("Text") 方法获得被拖的数据。该方法将返回在 setData() 方法中设置为相同类型的任何数据。

被拖数据是被拖元素的 id ("drag1")

把被拖元素追加到放置元素（目标元素）中






###### 新多媒体元素


