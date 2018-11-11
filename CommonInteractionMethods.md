# 常用互动方法

## 输出内容
* ```document.write()``` 可用于直接向 HTML 输出流写内容
* 举例，有很多输出方法：
```javascript
<script type="text/javascript">
  document.write("I love JavaScript！"); //内容用""括起来，""里的内容直接输出。

  var mystr="hello world!";
  document.write(mystr);  //直接写变量名，输出变量存储的内容。

  document.write(mystr+"I love JavaScript"); //多项内容之间用+号连接

  document.write(mystr+"<br>");//输出hello后，输出一个换行符
  document.write("JavaScript");
</script>
```


## 警告（alert 消息对话框）（弹出窗口只有确认键）
* 语法：
```
alert(字符串或变量);
```
* 举例：
```javascript
<script type="text/javascript">
   var mynum = 30;
   alert("hello!");
   alert(mynum);
</script>

```
上述代码展示过程中，当弹出了“hello！”的窗口后，点击确定，接着按顺序弹出第二个窗口显示变量```mynum```的值。


## 确认（confirm 消息对话框）（弹出窗口有确认键和取消键）
* 语法：
```javascript
confirm(str);
```
⚠️ 返回值为boolean值
* 举例：
```javascript
<script type="text/javascript">
    var mymessage=confirm("你喜欢JavaScript吗?");
    if(mymessage==true)
    {   document.write("很好,加油!");   }
    else
    {  document.write("JS功能强大，要学习噢!");   }
</script>
```


## 提问（prompt 消息对话框）（弹出窗口有确认键、取消键和文本输入框）
* 语法：
```javascript
prompt(str1, str2);
```
说明：str1: 要显示在消息对话框中的文本，不可修改。str2：文本框中的内容，可以修改
返回值：点击确定按钮，文本框中的内容将作为函数返回值。点击取消按钮，将返回null值
* 举例：
```javascript
var myname=prompt("请输入你的姓名:");
if(myname!=null)
  {   alert("你好"+myname); }
else
  {  alert("你好 my friend.");  }
```


## 打开新窗口（window.open）
* 语法：
```javascript
window.open([URL], [窗口名称], [参数字符串])
```
💬 说明：
1. URL：可选参数，在窗口中要显示网页的网址或路径。如果省略这个参数，或者它的值是空字符串，那么窗口就不显示任何文档。
2. 窗口名称：可选参数，被打开窗口的名称。  
   1⃣️ 该名称由字母、数字和下划线字符组成。  
   2⃣️ "_top"、"_blank"、"_self"具有特殊意义的名称。  
   _blank：在新窗口显示目标网页  
   _self：在当前窗口显示目标网页  
   _top：框架网页中在上部窗口中显示目标网页   
   3⃣️ 相同 name 的窗口只能创建一个，要想创建多个窗口则 name 不能相同。  
   4⃣️ name 不能包含有空格。
3. 参数字符串：可选参数，设置窗口参数，各参数用逗号隔开。<3434>`<2323>`


