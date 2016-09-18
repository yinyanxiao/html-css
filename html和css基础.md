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
+表单标签 form

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
+  **注意：**可独立成行的想在一行，每个标签的CSS样式都加 float:left.不独立成行的想独立成行，标签的CSS样式加 display:block.

#### 标签的属性
+ id class src alt href type 
**注:**属性是用来描述标签的，人的属性有身高，体重...

##样式(CSS)

#### 　定义CSS样式 (三种方式)

+ 外部样式(使用link引入)
```html
<head>
<link rel="stylesheet" type="text/css" href="mystyle.css">
</head>
```
+内部样式
```html
<head>
	<style type="text/css">
		p{margin-left: 20px}
	</style>	
</head>
```
+内联样式
```html
<p style="color:red; margin-left: 20px">This is a paragraph</p>
```

































