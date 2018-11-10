# JavaScipt基础知识

## 使用JS
### 插入JS
* JavaScript代码写在```<script></script>```之间  
```<script type="text/javascript">```表示在<script></script>之间的是文本类型(text),javascript是为了告诉浏览器里面的文本是属于JavaScript语言。
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
1. 放在&60;head&62;部分