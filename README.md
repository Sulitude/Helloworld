# Markdown 语法练习

## 目录
* [标题](#标题)
* [文本](#文本)
    * [文字](#文字)
        * 斜体/粗体/高亮
        * 删除线
    * [换行](#换行)
    * [段落](#段落)
    * [文本框](#文本框)
* [链接](#链接)
* [图片](#图片)
* [列表](#列表)
* [表格](#表格)
* [块级引用](#块级引用)
* [代码引用](#代码引用)
* [数学引用](#数学引用)
* [diff语法](#diff语法)
* [锚点](#锚点)
* [分割线](#分割线)
* [表情](#表情)
* [参考文献](#参考文献)
***
### 标题

# 一级标题    `# 标题名称`
## 二级标题    `## 标题名称`
### 三级标题    `### 标题名称`
#### 四级标题    `#### 标题名称`
##### 五级标题    `##### 标题名称`
###### 六级标题    `###### 标题名称`

***
### 文本
#### 文字

|语法|效果|
|:----:|:----:|
|`_斜体_`|_斜体_|
|`*斜体*`|*斜体*|
|`**粗体**`|**粗体**|
|`__粗体__`|__粗体__|
|`***粗斜体***`|***粗斜体***|
|`___粗斜体___`|___粗斜体___|
|`` `高亮` ``|`高亮`|
|`~~删除线~~`|~~删除线~~|
#### 换行
```
1. 行尾加两个空格
2. HTML换行符<br>
3. 两行文本之间加空行
```
#### 段落
```
用```将段落内容包裹起来，符号与内容之间需换行(回车即可)，否则表现形式与文本高亮一致
```
#### 文本框
    每行开头加四个空格
    最近的'父节点'应为块级元素
***
### 链接
    [content](URL "title")
* content:链接文字
* "title":链接标题，鼠标悬停时显示`可选`
* URL：可设置引用ID。当使用引用ID时，用`[ID]`代替`(URL "title")`
> 例：[图片廊][id]
```
[图片廊][id]
[id]: https://github.com/Sulitude/Image-Gallery "title"
```
##### 定义链接标签必须另起一行
[id]:https://github.com/Sulitude/Image-Gallery/ "Image_Gallery"

### 图片
    ![alt](URL "title")
* alt:图片显示失败时的替换文本`可选`
* "title":图片标题，鼠标悬停时显示`可选`
* URL:可设置引用ID，方法与使用链接相同。
>例：绝对路径 <div align=center>![picture](https://github.com/Sulitude/Image/raw/master/Image/1.jpg "My profile picture")
```
  <div align=center>![picture](https://github.com/Sulitude/Image/raw/master/Image/1.jpg "My profile picture")
```
* 图片的大小位置等可以用HTML设置
***
    
### 列表
#### 无序列表
##### 语法
```
'*'(或'-')+'空格'+'内容'
* 选项一
* 选项二
* 选项三
    * 二级选项一
    * 二级选项二
        * 三级选项一
```
##### 效果
* 选项一
* 选项二
* 选项三
    * 二级选项一
    * 二级选项二
        * 三级选项一
#### 有序列表
##### 语法
```
'数字'+'.'+'空格'+'内容'
1. 选项一
2. 选项二
3. 选项三
    1. 二级选项一
    2. 二级选项二
        1. 三级选项一
```
##### 效果
1. 选项一
2. 选项二
3. 选项三
    1. 二级选项一
    2. 二级选项二
        1. 三级选项一
#### 复选框列表
##### 语法
```
- [x] HTML
- [x] CSS
- [x] JavaScript
- [x] JSON
- [x] JQuery
- [x] Vue.js
- [x] Node.js
- [ ] AJAX
- [ ] TypeScript
```
##### 效果
- [x] HTML
- [x] CSS
- [x] JavaScript
- [x] JSON
- [x] JQuery
- [x] Vue.js
- [x] Node.js
- [ ] AJAX
- [ ] TypeScript
> 在GitHub的**issue**中使用该语法是可以实时点击复选框来勾选或解除勾选的，而无需修改issue原文。

#### 表格
##### 语法
```
|表头|表头|
|----|----|
|单元格|单元格|
|单元格|单元格|
|单元格|单元格|

> 指定对齐方式

|表头|表头|表头|
|:----|:----:|---:|
|左对齐|居中|右对齐|
|左对齐|居中|右对齐|
|左对齐|居中|右对齐|
```
##### 效果
 
|表头|表头|
|----|----|
|单元格|单元格|
|单元格|单元格|
|单元格|单元格|

> 指定对齐方式

|表头|表头|表头|
|:----|:----:|---:|
|左对齐|居中|右对齐|
|左对|居中|对齐|
|左|居中|齐|
***
### 块级引用
#### 语法
```
> **JavaScript 是一种专为与网页交互而设计的脚本语言，由下列三个不同的部分组成：**
>> ECMAScript，由ECMA-262 定义，提供核心语言功能；

>> 文档对象模型（DOM），提供访问和操作网页内容的方法和接口；

>> 浏览器对象模型（BOM），提供与浏览器交互的方法和接口。
>>>> (JavaScript高级程序设计（第三版）)
```
#### 效果
> **JavaScript 是一种专为与网页交互而设计的脚本语言，由下列三个不同的部分组成：**
>> ECMAScript，由ECMA-262 定义，提供核心语言功能；<br>
>> 文档对象模型（DOM），提供访问和操作网页内容的方法和接口；<br>
>> 浏览器对象模型（BOM），提供与浏览器交互的方法和接口。<br>
>>>> (JavaScript高级程序设计（第三版）)
### 代码引用
#### 语法
    '```语法名称' + '换行符' + '内容' + '换行符' + '```'
> 例: <br>
\```Java <br>
public static void main(String[]args){} //Java<br>
\```<br>
\```c<br>
int main(int argc, char *argv[]) //C<br>
\```<br>
\```Bash<br>
echo "hello GitHub" #Bash<br>
\```<br>
\```javascript<br>
document.getElementById("myH1").innerHTML="Welcome to my Homepage"; //javascipt<br>
\```<br>
\```cpp<br>
string &operator+(const string& A,const string& B) //cpp<br>
\```<br>

#### 效果
```Java
public static void main(String[]args){} //Java
```
```c
int main(int argc, char *argv[]) //C
```
```Bash
echo "hello GitHub" #Bash
```
```javascript
document.getElementById("myH1").innerHTML="Welcome to my Homepage"; //javascipt
```
```cpp
string &operator+(const string& A,const string& B) //cpp
```
### 数学引用
<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=default"></script>
$\sum$
$ \sum_1^n $
$
\int_0^1x^2dx
$
有些时候我们需要输入特殊的数学符号，比如∑∑、∏∏、∫∫、x−−√x​等，可以用下面的格式：
$想要输入的公式$
如：
$\sum_1^n$→→∑n1∑1n​、$\int_0^1x^2dx$→→∫10x2dx∫01​x2dx
其中“_”表示后面是下标，“^”表示后面是上标
#### 语法
```
$$
\mathbf{V}_1 \times \mathbf{V}_2 =  \begin{vmatrix} 
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
\frac{\partial X}{\partial u} &  \frac{\partial Y}{\partial u} & 0 \\
\frac{\partial X}{\partial v} &  \frac{\partial Y}{\partial v} & 0 \\
\end{vmatrix}
$$
```
$$
\mathbf{V}_1 \times \mathbf{V}_2 =  \begin{vmatrix} 
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
\frac{\partial X}{\partial u} &  \frac{\partial Y}{\partial u} & 0 \\
\frac{\partial X}{\partial v} &  \frac{\partial Y}{\partial v} & 0 \\
\end{vmatrix}
$$

### diff语法
#### 语法
> **类似于代码引用**<br>
\```diff <br>
\+ 绿色代表新增<br>
\- 红色代表删除<br>
\! 橙色代表加重<br>
\# 灰色代表一般<br>
\```
#### 效果

```diff <br>
+ 绿色代表新增
- 红色代表删除
! 橙色橙色橙色
# 灰色灰色灰色
```

### 锚点
```
[Markdown 语法练习](#Markdown 语法练习)
```  
[Markdown 语法练习](#Markdown 语法练习)
> 不区分大小写
    
### 分割线
1. \*** 
***
2. \---
---
3. \___
___
### 表情
Github的Markdown语法支持添加emoji表情，输入不同的符号码（两个冒号包围的字符）可以显示出不同的表情。<br>
比如`:blush:`，可以显示:blush:。<br>
具体每一个表情的符号码，可以查询GitHub的官方网页[http://www.emoji-cheat-sheet.com](http://www.emoji-cheat-sheet.com)。<br>
***
### 参考文献
1.[Markdown中文文档](https://markdown-zh.readthedocs.io/en/latest/)
2.[果冻虾仁的Github](https://github.com/Sulitude/README/blob/master/README.md)
3.
4.


