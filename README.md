### <!DOCTYPE> 声明
< !DOCTYPE> 声明位于文档中的最前面的位置，处于 <html> 标签之前。
  
< !DOCTYPE> 声明不是一个 HTML 标签；它是用来告知 Web 浏览器页面使用了哪种 HTML 版本。

< !DOCTYPE> 标签没有结束标签

< !DOCTYPE> 声明不区分大小写
  
#### 通用声明
HTML5：
```
<!DOCTYPE html>```

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

### HTML <head> 元素
<head> 元素包含了所有的头部标签元素。在 <head>元素中你可以插入脚本（scripts）, 样式文件（CSS），及各种meta信息

可以添加在头部区域的元素标签为: <title>, <style>, <meta>, <link>, <script>, <noscript>, and <base>.
  
### HTML <base> 元素
<base> 标签为HTML文档中所有的链接标签的默认链接

### HTML <link> 元素
<link> 标签定义了文档与外部资源之间的关系。

<link> 标签通常用于链接到样式表:
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




