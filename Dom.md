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
* 举例：
```javascript
<script type="text/javascript"> 
    function hidetext()  
	{  
        document.getElementById("con").style.display = "none";
	}  
	function showtext()  
	{  
		document.getElementById("con").style.display = "block";
	}
</script>
<p id="con">做为一个Web开发师来说，如果你想提供漂亮的网页、令用户满意的上网体验，JavaScript是必不可少的工具。</p> 
    <form>
       <input type="button" onclick="hidetext()" value="隐藏内容" /> 
       <input type="button" onclick="showtext()" value="显示内容" /> 
    </form>
```


## 控制类名（className 属性）
* 语法：
```javascript
object.className = classname
```
作用：
1. 获取元素的class 属性
2. 为网页内的某个元素指定一个css样式来更改该元素的外观
* 举例：
```javascript
<style>
    body{ font-size:16px;}
    .one{
		border:1px solid #eee;
		width:230px;
		height:50px;
		background:#ccc;
		color:red;
    }
	.two{
		border:1px solid #ccc;
		width:230px;
		height:50px;
		background:#9CF;
		color:blue;
	}
	</style>

<p id="p1" > JavaScript使网页显示动态效果并实现与用户交互功能。</p>
    <input type="button" value="添加样式" onclick="add()"/>
	<p id="p2" class="one">JavaScript使网页显示动态效果并实现与用户交互功能。</p>
    <input type="button" value="更改外观" onclick="modify()"/>

	<script type="text/javascript">
	   function add(){
	      var p1 = document.getElementById("p1");
	      p1.className = "one";
	   }
	   function modify(){
	      var p2 = document.getElementById("p2");
	      p2.className = "two";
	   }
	</script>
```

