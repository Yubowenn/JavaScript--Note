# 文档对象模型DOM
* 定义访问和处理HTML文档的标准方法。DOM 将HTML文档呈现为带有元素、属性和文本的树结构（节点树）。ps:类似xml中dtd的赶脚
  
## 通过ID获取元素
* 语法：
```javascript
document.getElementById(“id”) 
```
* 举例：
```javascript
<p id="con">JavaScript</p>
<script type="text/javascript">
  var mychar= document.getElementById("con")          ;
  document.write("结果:"+mychar); //输出获取的P标签。 
</script>
```


## innerHTML 属性
* 语法：
```javascript
Object.innerHTML
```
⚠️ 
1. Object是获取的元素对象，如通过document.getElementById("ID")获取的元素。
2. 注意书写，innerHTML区分大小写。
* 举例：
```javascript
<h2 id="con">javascript</H2>
<script type="text/javascript">
  var mychar=  document.getElementById("con")         ;
  document.write("原标题:"+mychar.innerHTML+"<br>"); //输出原h2标签内容
  mychar.innerHTML = "Hello World";
  document.write("修改后的标题:"+mychar.innerHTML); //输出修改后h2标签内容
</script>
```
输出结果为：
```
Hello World
原标题:javascript
修改后的标题:Hello World
```
即h2中最终显示的是经过`innerHTML`修改后的内容


## 改变 HTML 样式
* 语法：
```javascript
Object.style.property=new style;
```
⚠️ Object是获取的元素对象，如通过document.getElementById("id")获取的元素。
* 基本属性表：  
![property](http://img.mukewang.com/52e4d4240001dd6c04850229.jpg)
* 举例：
```javascript
<p id="pcon">Hello World!</p>
<script>
   var mychar = document.getElementById("pcon");
   mychar.style.color="red";
   mychar.style.fontSize="20";
   mychar.style.backgroundColor ="blue";
</script>
```
结果为：  
![result_2](http://img.mukewang.com/52e4d6ae000177d203770253.jpg)


## 显示和隐藏（display属性）
* 语法：
```javascript
Object.style.display = value
```
⚠️ Object是获取的元素对象，如通过document.getElementById("id")获取的元素。  
* value取值：
![value](http://img.mukewang.com/52e4dba5000179da04110095.jpg)



