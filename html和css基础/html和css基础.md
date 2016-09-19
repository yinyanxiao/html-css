# 网页包括
+ 内容：html
+ 样式：css
+ 行为：js

## html:超文本标记语言

## html整体框架
```html
<!DOCTYPE html>
```
+ 解析：DOCTYPE声明文档类型，以便验证文档是否符合文档类型定义（DTD）。如果你的页面添加了<!DOCTYPE html>那么，那么就等同于开启了标准模式，那么浏览器就得老老实实的按照W3C的标准解析渲染页面，这样一来，你的页面在所有的浏览器里显示的就都是一个样子了。
+  HTML4支持的三种DOCTYPE声明分别是严格型（strict）、过渡型（transitional）和框架型（Frameset）。
+  浏览器使用两种基本的模式，怪异模式和标准模式。二者的区别在于前者不遵循CSS规范，后者遵循CSS规范。DOCTYPE声明会触发浏览器的标准模式。
```html
<html lang="en">
```
+ 解析：向搜索引擎表示该页面是html语言，并且语言为英文网站，其"lang"的意思就是“language”，语言的意思，而“en”即表示english.你的页面如果是中文页面，可将其改为<html lang="zh">,中英文对页面没有影响，只是给搜索引擎看的，这些现在都是html规范，你的页面越规范，就越容易被收录。
+ 搜索引擎（Search Engine）是指根据一定的策略、运用特定的计算机程序从互联网上搜集信息，在对信息进行组织和处理后，为用户提供检索服务，将用户检索相关的信息展示给用户的系统。
```html
<meta charset="UTF-8">
```
+ 解析：utf-8编码。当你没加这句的时候，网页中有中文字符，或许会导致浏览器的不同，使得中文字符出现

##内容(html)

#### 常用的html标签
+ 标题标签 h1、h2、h3、h4、h5、h6
+ 列表标签 ul li
+ 图片标签 img
+ 段落标签 p
+ 超链接  a
+ 表单标签 form

 ```html
<!DOCTYPE html>
<html lang="zh">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
</head>
<body>
	<h1>前端工程开发师</h1>
	<ul>
		<li>水果</li>
	</ul>
	<img src="图片路径" alt="">
	<p>这里写的是段落性的文字</p>
	<a href="http://baidu.com">跳到百度</a>
</body>
</html>	
```
#### 标签分类
+ 块元素:(可独立成行，可设宽高) h   p   ul li
+ 行内/内联/行级元素(不可设宽高，不独立成行) a span
+ 行内块元素(不独立成行，可设宽高) img input
+ **注意：**可独立成行的想在一行，每个标签的CSS样式都加 float:left.不独立成行的想独立成行，标签的CSS样式加 display:block.


#### 标签的属性
+ id class src alt href type 
** 注:**属性是用来描述标签的，人的属性有身高，体重...

##样式(CSS)

#### 　定义CSS样式 (css引入的三种方式)

+ 外部样式(使用link引入)
```html
<head>
<link rel="stylesheet" type="text/css" href="mystyle.css">
</head>
```
+ 内部样式
```html
<head>
	<style type="text/css">
		p{margin-left: 20px}
	</style>	
</head>
```
+ 内联样式
```html
<p style="color:red; margin-left: 20px">This is a paragraph</p>
```
#### CSS结构

```html
选择器{
	属性：属性值；
}
```
#### CSS2选择器
+ *（通配符选择器）代表所有的标签或元素。
+ id选择器 
+ class 选择器
+ 层级选择器（后代选择器）
+ 标签/元素选择器
+ 属性选择器
+ 子元素选择器
+ 伪类选择器
```html
<!DOCTYPE html>
<html lang="zh">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		*{
			padding:0px;
			margin:0px;
		}
		#box1{
			color:red;
		}
		.box2{
			color:blue;
		}
		ul li{
			color:yellow;
		}
		p{
			color:pink;
		}
		/*属性选择器*/
		a[href="http://baidu.com"]{
			color:red;
		}
		/*子集选择器*/	
		h1 > strong {color:red;}		
	</style>
</head>
<body>
	<div id="box1">ID选择器</div>
	<div class="box2">class选择器</div>
	<ul>
		<li>插入</li>
		<li>删除</li>
	</ul>
	<p>标签/元素选择器</p>
	<a href="http://baidu.com">百度</a>
	<a href="http://163.com">网易</a>
	<h1>This is <strong>very</strong> <strong>very</strong> important.</h1>
</body>
</html>	
```
+ 伪类选择器
```html
<!DOCTYPE html>
<html lang="zh">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
	/*鼠标移动上去时变红*/
		a:hover{
			background-color: yellow;
		}
	/*未访问过的为黄色*/
		a:link{
			color:yellow;
		}
	/*访问过的为蓝色*/	
		a:visited{
			color:pink;
		}
	/*点击时为绿色*/
		a:active{
			color:green;
			background-color: #000;
		}
	/*在h1标签前加太阳*/
		h1:before{
			content:"太阳";
			color:red;
			background-color: green;
		}	
		h1:after{content:"太阳"}	
				
				
	</style>
</head>
<body>
	<a href="http://baidu.com">百度</a>
	<a href="http://163.com">网易</a>
	<a href="http://3366.com">搜狐</a>
	<h1>我向往的</h1>
</body>
</html>	
```

#### CSS2常用属性
+ color、width、height、font-size、background-color
+ display:block(设置成块元素、显示)
+ display:none(隐藏)
+ float:left(浮动，两个块元素想在一行)
+ list-style:none(去li的点)
+ text-decoration:none(去a的下划线)
+ border 1px solid red;(solid实线，dashed虚线)
+ margin:100px 100px 100px 100px (上、右、下、左)
+ margin:100px 100px(上下[依上为主]、左右[依左为主])
+ margin:0 auto(上下边距为0，左右边距相等)
+ margin:0 auto (块元素居中,例:想让盒子距离页面左右页边距相等)
+ line-height(行高，和height的值相等时，盒内元素垂直居中)
+ text-align:center,left,right(盒内元素水平居中)
+ 清浮动：子集元素浮动，父级元素高度不可以自适应(因为浮动后不占位)，则需要清浮动（清浮动后则盒子占位）就可以把不设高的大盒子撑开。
+ <div class="clear"></div> 清浮动1
```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style type="text/css">
		.box1{
			width:100px;
			height:100px;
			border:1px solid red;
			float: left;
		}
		.box2{
			width:100px;
			height:100px;
			border:1px solid red;
			float: left;
		}
		.box3{
			height:100px;
			width: 1000px;
			background-color: #aaa;
		}

		/*清浮动*/
		.clear{
			clear:both;
		}
	</style>
</head>
<body>
	<div class="box1"></div>
	<div class="box2"></div>
	<div class="clear"></div>
	<div class="box3"></div>
</body>
</html>
```
+ .clearFix:before,.clearFix:after 清浮动2
```html
<!DOCTYPE html>
<html lang="zh">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		.big-box{
			background-color: red;
		}
		.box{
			height: 100px;
			width: 100px;
			background-color: yellow;
			float:left;
		}
		.clearFix:before,.clearFix:after{
			content: "";
			clear:both;
			display: block;
		}	
				
	</style>
</head>
<body>
	/*浮动只能放在父级*/
	<div class="big-box clearFix">
		<div class="box"></div>
		<div class="box"></div>
		<div class="box"></div>
	</div>
</body>
</html>
```
#### CSS盒模型
+ css盒模型包括：内容(content)、填充(padding)、边框(border)、边界(margin)
+ **解释：**一个木头盒子，里面的东西是content，怕东西在运输的过程中磕坏，需要一些填充物泡沫padding,木头盒子是border,摆放时每个木头盒子之间的间距是margin.一般一个盒子在计算时是content+padding+border

#### 选择器优先级

+ 1.!important是提高属性的代先级 .div{height:100px!important}
+ 2.内联样式，级别为1000。<div style="color:Red;"></div>
+ 3.!important优先级高于内联样式
+ 4.id选择器,级别为100。#myDiv{color:Red;}
+ 5.类选择器级,别为10。 .divClass{color:Red;}
+ 6.标签选择器,级别是1。  div{color:Red;}
+ 7.通配符选择器最低
+ 8.优先级算法：.divClass  span { color:Red;}   优先级别就是：10+1=11




　　
　　





















































