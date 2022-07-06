# 一、HTML编程语言介绍:
1. HTML编程语言是一种在浏览器中编译与执行的编程语言，用于控制浏览器
2. HTML编程全名是【超文本标记性编程语言】
	- 新的数据描述形式  像素/帧
	- 例子：大多数编程语言都是以【命令行】方式表达含义
3. HTML所有的命令都是写在标签，比如 < br/>
# 二、HTML具体作用---控制浏览器
1. HTML命令可以要求浏览器将接收的数据以指定的形态展示-----【美工工作任务】
2. HTML命令向浏览器提供要请求的资源文件的请求信息----------【学习重点】
# 三、HTML命令书写特点
1. 所有的HTML命令都必须书写在标签中，比如< br/ >,< p >
2. 所有的HTML命令在书写时不区分英文字母大小写。（java区分大小写，sql,html不区分大小写）。
	- 比如< br/ >合法，< BR/ > 合法  < bR/ > 合法
3. 所有的HTML命令在分类上分为【双目标签】和【单目标签】
4. [双目标签]指的是命令书写在【开始标签】与【结束标签】之内。
	- 比如< tr >< /tr >,是一个命令。【双目标签】书写时其【结束标签】是不能省略，否则浏览器中HTML编译器将无法识别命令
	- < tr >< /tr >------合法
	- < tr >< tr >-------有的浏览器认为非法，有的浏览器认为这是两个命令
5. [单目标签]指的是命令所在的标签既是开始标签又是结束标签
	- 比如 < br />,是一个命令。单目标签的结束标志" / "可以省略的。
	- < br/ >------------标准的单目标签命令，合法
	- < br >-------------非标准的单目标签命令，合法
# 四、简单展示标签
代码：[Test01](00-resource/Code/HTML/标签命令/web/Test01.html)
![](00-resource/assets/JavaWeb/Pasted%20image%2020220706154907.png)
## 1.文字水平居中
```html
<center>Hello World!</center>
```
![](00-resource/assets/JavaWeb/Pasted%20image%2020220706155344.png)
## 2.自定义字体标签< font >
```html
<!--棕色、40像素-->
<font style="color: brown;font-size: 40px">  
    Hello World!  
</font>
```
![](00-resource/assets/JavaWeb/Pasted%20image%2020220706155809.png)
代码：[Test02](00-resource/Code/HTML/标签命令/web/Test02.html)
## 3.段落标签< p >
```html
<p>  
中华人民共和国国庆节又称“十一”、“国庆节”、“国庆日”、“中国国庆节”、“国庆黄金周”。中华人民共和国中央人民政府宣布自1949年起，以每年的10月1日，即中华人民共和国宣告成立的日子，即国庆日。  
</p>
```
![](00-resource/assets/JavaWeb/Pasted%20image%2020220706161003.png)
## 4.标题标签< h1 > ~ < h6 >
```html
<h1>国庆节</h1>
```
![](00-resource/assets/JavaWeb/Pasted%20image%2020220706161236.png)
## 5.插入图片
```html
<img src="CN.jpg">
```
![](00-resource/assets/JavaWeb/Pasted%20image%2020220706161715.png)

代码：[Test03](00-resource/Code/HTML/标签命令/web/Test03.html)
## 6.表格标签
```html
<!--aligns居中表格-->
<!--border表格线宽-->
<table align="center" border="2">  
    <!--行-->  
    <tr>  
        <!--字段-->  
        <td>部门编号</td>  
        <td>职员姓名</td>  
        <td>职员工资</td>  
    </tr>  
</table>
```
![](00-resource/assets/JavaWeb/Pasted%20image%2020220706163457.png)
### rowspan
使当前单元格的宽度变为原来的n倍（向下）。实现了单元格合并的效果。
```html
<tr>  
    <td rowspan="2">001</td>  
    <td>Smith</td>  
    <td>5000</td>  
</tr>  
<tr>  
    <td>Curry</td>  
    <td>5000</td>  
</tr>
```
![](00-resource/assets/JavaWeb/Pasted%20image%2020220706163548.png)
### colspan
使当前单元格的长度变为原来的n倍（向右）。实现了单元格合并的效果。
```html
<tr>  
    <!--字段-->  
    <td>部门编号</td>  
    <td colspan="2">职员姓名和工资</td>  
</tr>
```
![](00-resource/assets/JavaWeb/Pasted%20image%2020220706164017.png)

代码：[Test04](00-resource/Code/HTML/标签命令/web/Test04.html)
## 7.列表标签
### 有序列表
```html
<ol>  
    <li>香蕉</li>  
    <li>苹果</li>  
</ol>
```
![](00-resource/assets/JavaWeb/Pasted%20image%2020220706164342.png)
### 无序列表
```html 
<ul>  
    <li>香蕉</li>  
    <li>苹果</li>  
</ul>
```
![](00-resource/assets/JavaWeb/Pasted%20image%2020220706164432.png)

# 五、考试系统DEMO
![](00-resource/assets/JavaWeb/Pasted%20image%2020220706184339.png)
**源码：00-resource/Code/HTML/Demo**
# 六、请求文件信息标签（重点）⭐
[Test01](00-resource/Code/HTML/请求文件信息/web/Test01.html)
## 1.超链接标签命令
```html
<a href="地址">提示信息</a>
```
![](00-resource/assets/JavaWeb/Pasted%20image%2020220706190918.png)
## 2.表单标签命令
```html
<form action="地址">
	<input type='submit' value='提示信息'/>
</form>
```
![](00-resource/assets/Pasted%20image%2020220706191139.png)
