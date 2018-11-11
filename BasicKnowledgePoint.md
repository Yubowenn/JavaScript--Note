# JavaScipt基础知识

## 使用JS
### 插入JS
* JavaScript代码写在```<script></script>```之间  
```<script type="text/javascript">```表示在&#60;script&#62;&#60;/script&#62;之间的是文本类型(text),javascript是为了告诉浏览器里面的文本是属于JavaScript语言。
### 引入外部JS文件
* 把HTML文件和JS代码分开,并单独创建一个JavaScript文件(简称JS文件),其文件后缀通常为.js，然后将JS代码直接写在JS文件中。
* 举例：  
index.html:
```html
<!DOCTYPE HTML>
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
<title>引用JS文件</title>
<script src="script.js"></script>//在这里引用
</head>
<body>
</body>
</html>
```
script.js:
```javascript
document.write("引用JS文件！");
```


## JS放在页面中的位置
* 可以将JavaScript代码放在html文件中任何位置，但是我们一般放在网页的head或者body部分。  
1. 放在&#60;head&#62;部分  
常用的方式是在页面中head部分放置&#60;script&#62;元素，浏览器解析head部分就会执行这个代码，然后才解析页面的其余部分。
2. 放在&#60;body&#62;部分  
JavaScript代码在网页读取到该语句的时候就会执行。  
⚠️ javascript作为一种脚本语言可以放在html页面中任何位置，但是浏览器解释html时是按先后顺序的，所以前面的script就先被执行。比如进行页面显示初始化的js必须放在head里面，因为初始化都要求提前进行（如给页面body设置css等）；而如果是通过事件调用执行的function那么对位置没什么要求的


## 定义变量
* 语法如下：
```var 变量名   ```
* 变量命名规则：
1. 变量必须使用字母、下划线(_)或者美元符($)开始。

2. 然后可以使用任意多个英文字母、数字、下划线(_)或者美元符($)组成。

3. 不能使用JavaScript关键词与JavaScript保留字。


## if-else语句
* 语法如下：
```
if(条件)
{ 条件成立时执行的代码 }
else
{ 条件不成立时执行的代码 }
```


## 函数
* 语法如下：
```
function 函数名()
{
     函数代码;
}
```