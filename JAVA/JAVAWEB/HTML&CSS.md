# 今日内容

1. web 概念概述
2. HTML

## web 概念概述

### JavaWeb：

- 使用 Java 语言开发基于互联网的项目

### 软件架构：

1. **C/S: Client/Server 客户端 / 服务器端**
    - 在用户本地有一个客户端程序，在远程有一个服务器端程序
    - 如：QQ，迅雷...
    - **优点**：
        - 用户体验好
    - **缺点**：
        - 开发、安装，部署，维护 麻烦
2. **B/S: Browser/Server 浏览器 / 服务器端**
    - 只需要一个浏览器，用户通过不同的网址 (URL)，客户访问不同的服务器端程序
    - **优点**：
        - 开发、安装，部署，维护 简单
    - **缺点**：
        - 如果应用过大，用户的体验可能会受到影响
        - 对硬件要求过高

### B/S 架构详解

#### 资源分类：

1. **静态资源**：
    - 使用静态网页开发技术发布的资源。
    - **特点**：
        - 所有用户访问，得到的结果是一样的。
        - 如：文本，图片，音频、视频，HTML,CSS,JavaScript
        - 如果用户请求的是静态资源，那么服务器会直接将静态资源发送给浏览器。浏览器中内置了静态资源的解析引擎，可以展示静态资源
2. **动态资源**：
    - 使用动态网页及时发布的资源。
    - **特点**：
        - 所有用户访问，得到的结果可能不一样。
        - 如：jsp/servlet,php,asp...
        - 如果用户请求的是动态资源，那么服务器会执行动态资源，转换为静态资源，再发送给浏览器

  

我们要学习动态资源，必须先学习静态资源！

#### 静态资源：

- **HTML**：用于搭建基础网页，展示页面的内容
- **CSS**：用于美化页面，布局页面
- **JavaScript**：控制页面的元素，让页面有一些动态的效果

## HTML

### 1. 概念：是最基础的网页开发语言

- **Hyper Text Markup Language 超文本标记语言**
    - **超文本**:
        - 超文本是用超链接的方法，将各种不同空间的文字信息组织在一起的网状文本.
    - **标记语言**:
        - 由标签构成的语言。<标签名称> 如 html，xml
        - 标记语言不是编程语言

### 2. 快速入门：

#### 语法：

1. html 文档后缀名 .html 或者 .htm
2. 标签分为
    - 围堵标签：有开始标签和结束标签。如 <html> </html>
    - 自闭和标签：开始标签和结束标签在一起。如  
        
3. 标签可以嵌套：
    - 需要正确嵌套，不能你中有我，我中有你
    - 错误：<a><b></a></b>
    - 正确：<a><b></b></a>
4. 在开始标签中可以定义属性。属性是由键值对构成，值需要用引号 (单双都可) 引起来
5. html 的标签不区分大小写，但是建议使用小写。

#### 代码：

html

预览

```html
<html>
    <head>
        <title>title</title>
    </head>
    <body>
        <FONT color='red'>Hello World</font><br/>
        <font color='green'>Hello World</font>
    </body>
</html>
```

### 3. 标签学习：

#### 文件标签：构成 html 最基本的标签

- **html**:html 文档的根标签
- **head**：头标签。用于指定 html 文档的一些属性。引入外部的资源
- **title**：标题标签。
- **body**：体标签
- ：html5 中定义该文档是 html 文档

#### 文本标签：和文本有关的标签

- **注释**：
- **<h1> to <h6>**：标题标签
    - h1~h6: 字体大小逐渐递减
- **<p>**：段落标签
- ：换行标签
- **<hr>**：展示一条水平线
    - **属性**：
        - **color**：颜色
        - **width**：宽度
        - **size**：高度
        - **align**：对其方式
            - **center**：居中
            - **left**：左对齐
            - **right**：右对齐
- **<b>**：字体加粗
- **<i>**：字体斜体
- **<font>**: 字体标签
- **<center>**: 文本居中
    - **属性**：
        - **color**：颜色
        - **size**：大小
        - **face**：字体

#### 属性定义：

- **color**：
    - 英文单词：red,green,blue
    - rgb (值 1，值 2，值 3)：值的范围：0~255 如 rgb (0,0,255)
    - #值 1 值 2 值 3：值的范围：00~FF 之间。如： #FF00FF
- **width**：
    - 数值：width='20' , 数值的单位，默认是 px (像素)
    - 数值 %：占比相对于父元素的比例

#### 案例：公司简介

html

预览

``` html
<!DOCTYPE html>
<html lang="ch">
<head>
    <meta charset="UTF-8">
    <title>黑马程序员简介</title>
</head>
<body>

<h1>
    公司简介
</h1>
<hr color="#ffd700">

<p>
<font color="#FF0000">"中关村黑马程序员训练营"</font>是由<b><i>传智播客</i></b>联合中关村软件园、CSDN， 并委托传智播客进行教学实施的软件开发高端培训机构，致力于服务各大软件企业，解决当前软件开发技术飞速发展， 而企业招不到优秀人才的困扰。
</p>

<p>
目前，“中关村黑马程序员训练营”已成长为行业“学员质量好、课程内容深、企业满意”的移动开发高端训练基地， 并被评为中关村软件园重点扶持人才企业。
</p>

<p>

黑马程序员的学员多为大学毕业后，有理想、有梦想，想从事 IT 行业，而没有环境和机遇改变自己命运的年轻人。 黑马程序员的学员筛选制度，远比现在 90%以上的企业招聘流程更为严格。任何一名学员想成功入学“黑马程序员”， 必须经历长达 2 个月的面试流程，这些流程中不仅包括严格的技术测试、自学能力测试，还包括性格测试、压力测试、 品德测试等等测试。毫不夸张地说，黑马程序员训练营所有学员都是精挑细选出来的。百里挑一的残酷筛选制度确 保学员质量，并降低企业的用人风险。
中关村黑马程序员训练营不仅着重培养学员的基础理论知识，更注重培养项目实施管理能力，并密切关注技术革新， 不断引入先进的技术，研发更新技术课程，确保学员进入企业后不仅能独立从事开发工作，更能给企业带来新的技术体系和理念。
</p>

<p>

一直以来，黑马程序员以技术视角关注 IT 产业发展，以深度分享推进产业技术成长，致力于弘扬技术创新，倡导分享、 开放和协作，努力打造高质量的 IT 人才服务平台。
</p>

<hr color="#ffd700">

<font color="gray" size="2">
    <center>
        江苏传智播客教育科技股份有限公司<br>
        版权所有Copyright 2006-2018©, All Rights Reserved 苏ICP备16007882
    </center>
</font>


</body>
</html>
```

#### 4. 图片标签：

- **img**：展示图片
    - **属性**：
        - **src**：指定图片的位置

#### 代码：

html

预览

```html
<!--展示一张图片 img-->
<img src="image/jingxuan_2.jpg" align="right" alt="古镇" width="500" height="500"/>

<!--
    相对路径
        * 以.开头的路径
            * ./：代表当前目录  ./image/1.jpg
            * ../:代表上一级目录
 -->
<img src="./image/jiangwai_1.jpg">
<img src="../image/jiangwai_1.jpg">
```

#### 5. 列表标签：

- **有序列表**：
    - **ol**
    - **li**
- **无序列表**：
    - **ul**
    - **li**

#### 6. 链接标签：

- **a**：定义一个超链接
    - **属性**：
        - **href**：指定访问资源的 URL (统一资源定位符)
        - **target**：指定打开资源的方式
            - **_self**: 默认值，在当前页面打开
            - **_blank**：在空白页面打开

#### 代码：

html

预览

```html
<!--超链接  a-->
<a href="http://www.itcast.cn">点我</a>
<br>

<a href="http://www.itcast.cn" target="_self">点我</a>
<br>
<a href="http://www.itcast.cn" target="_blank">点我</a>

<br>

<a href="./5_列表标签.html">列表标签</a><br>
<a href="mailto:itcast@itcast.cn">联系我们</a>

<br>
<a href="http://www.itcast.cn"><img src="image/jiangwai_1.jpg"></a>
```

#### 7. div 和 span：

- **div**：每一个 div 占满一整行。块级标签
- **span**：文本信息在一行展示，行内标签 内联标签

#### 8. 语义化标签：html5 中为了提高程序的可读性，提供了一些标签。

- **<header>**：页眉
- **<footer>**：页脚

#### 9. 表格标签：

- **table**：定义表格
    - **width**：宽度
    - **border**：边框
    - **cellpadding**：定义内容和单元格的距离
    - **cellspacing**：定义单元格之间的距离。如果指定为 0，则单元格的线会合为一条、
    - **bgcolor**：背景色
    - **align**：对齐方式
- **tr**：定义行
    - **bgcolor**：背景色
    - **align**：对齐方式
- **td**：定义单元格
    - **colspan**：合并列
    - **rowspan**：合并行
- **th**：定义表头单元格
- **<caption>**：表格标题
- **<thead>**：表示表格的头部分
- **<tbody>**：表示表格的体部分
- **<tfoot>**：表示表格的脚部分

### 案例：旅游网站首页

1. 确定使用 table 来完成布局
2. 如果某一行只有一个单元格，则使用<tr><td></td></tr>
3. 如果某一行有多个单元格，则使用

  

html

预览

```html
<tr>
    <td>
        <table></table>
    </td>
</tr>
```

  

4. 代码实现

  

html

预览

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>黑马旅游网</title>
</head>
<body>

    <!--采用table来完成布局-->
    <!--最外层的table，用于整个页面的布局-->
    <table width="100%" align="center">
       <!-- 第1行 -->
        <tr>
            <td>
                <img src="image/top_banner.jpg" width="100%" alt="">
            </td>
        </tr>

        <!-- 第2行 -->
        <tr>
            <td>
                <table width="100%" align="center">
                    <tr>
                        <td>
                            <img src="image/logo.jpg" alt="">
                        </td>
                        <td>
                            <img src="image/search.png" alt="">
                        </td>
                        <td>
                            <img src="image/hotel_tel.png" alt="">
                        </td>
                    </tr>
                </table>

            </td>
        </tr>

        <!-- 第3行 -->
        <tr>
            <td>
                <table width="100%" align="center">
                    <tr bgcolor="#ffd700" align="center" height="45" >
                        <td>
                            <a href="">首页</a>
                        </td>

                        <td>
                            门票
                        </td>

                        <td>
                            门票
                        </td>

                        <td>
                            门票
                        </td>

                        <td>
                            门票
                        </td>

                        <td>
                            门票
                        </td>

                        <td>
                            门票
                        </td>

                        <td>
                            门票
                        </td>

                        <td>
                            门票
                        </td>

                        <td>
                            门票
                        </td>
                    </tr>
                </table>
            </td>
        </tr>

        <!-- 第4行 轮播图 -->
        <tr>
            <td>
                <img src="image/banner_3.jpg" alt="" width="100%">
            </td>
        </tr>

        <!-- 第5行 黑马精选-->
        <tr>
            <td>
                <img src="image/icon_5.jpg" alt="">
                黑马精选
                <hr  color="#ffd700" >
            </td>
        </tr>

        <!-- 第6行 -->
        <tr>
            <td>
                <table align="center" width="95%">
                    <tr>
                        <td>

                            <img src="image/jiangxuan_1.jpg" alt="">
                            <p>上海飞三亚五天4晚自由行(春节销售+亲子+蜜月+自由行)</p>
                            <font color="red">¥ 899</font>
                        </td>

                        <td>

                            <img src="image/jiangxuan_1.jpg" alt="">
                            <p>上海飞三亚五天4晚自由行(春节销售+亲子+蜜月+自由行)</p>
                            <font color="red">¥ 899</font>
                        </td>

                        <td>

                            <img src="image/jiangxuan_1.jpg" alt="">
                            <p>上海飞三亚五天4晚自由行(春节销售+亲子+蜜月+自由行)</p>
                            <font color="red">¥ 899</font>
                        </td>

                        <td>

                            <img src="image/jiangxuan_1.jpg" alt="">
                            <p>上海飞三亚五天4晚自由行(春节销售+亲子+蜜月+自由行)</p>
                            <font color="red">¥ 899</font>
                        </td>
                    </tr>
                </table>
            </td>
        </tr>

        <!-- 第7行 国内游 -->
        <tr>
            <td>
                <img src="image/icon_6.jpg" alt="">
                国内游
                <hr  color="#ffd700" >
            </td>
        </tr>

        <!-- 第8行 -->
        <tr>
            <td>
                <table align="center" width="95%">
                    <tr>
                        <td rowspan="2">
                            <img src="image/guonei_1.jpg" alt="">
                        </td>

                        <td>

                            <img src="image/jiangxuan_2.jpg" alt="" height="100%">
                            <p>上海飞三亚五天4晚自由行(春节销售+亲子+蜜月+自由行)</p>
                            <font color="red">¥ 699</font>
                        </td>

                        <td>

                            <img src="image/jiangxuan_2.jpg" alt="">
                            <p>上海飞三亚五天4晚自由行(春节销售+亲子+蜜月+自由行)</p>
                            <font color="red">¥ 699</font>
                        </td>

                        <td>

                            <img src="image/jiangxuan_2.jpg" alt="">
                            <p>上海飞三亚五天4晚自由行(春节销售+亲子+蜜月+自由行)</p>
                            <font color="red">¥ 699</font>
                        </td>
                    </tr>

                    <tr>
                        <td>

                            <img src="image/jiangxuan_2.jpg" alt="">
                            <p>上海飞三亚五天4晚自由行(春节销售+亲子+蜜月+自由行)</p>
                            <font color="red">¥ 699</font>
                        </td>

                        <td>

                            <img src="image/jiangxuan_2.jpg" alt="">
                            <p>上海飞三亚五天4晚自由行(春节销售+亲子+蜜月+自由行)</p>
                            <font color="red">¥ 699</font>
                        </td>

                        <td>

                            <img src="image/jiangxuan_2.jpg" alt="">
                            <p>上海飞三亚五天
```

# 今日内容： HTML 标签：表单标签

## 表单

### 概念

用于采集用户输入的数据，并且用于和服务器进行交互。

### form

用于定义表单，可以定义一个范围，这个范围代表采集用户数据的范围。

**注意**：表单项中的数据要想被提交，必须指定其 name 属性。

#### 属性

- **action**：指定提交数据的 URL。
- **method**：指定提交方式，一共 7 种，2 种比较常用。
    - **get**：
        1. 请求参数会在地址栏中显示，会封装到请求行中（HTTP 协议后讲解）。
        2. 请求参数大小是有限制的。
        3. 不太安全。
    - **post**：
        1. 请求参数不会在地址栏中显示，会封装在请求体中（HTTP 协议后讲解）。
        2. 请求参数的大小没有限制。
        3. 较为安全。

  



## 表单项标签

### input

可以通过 type 属性值，改变元素展示的样式。

#### type 属性

- **text**：文本输入框，默认值。
    - **placeholder**：指定输入框的提示信息，当输入框的内容发生变化，会自动清空提示信息。
- **password**：密码输入框。
- **radio**：单选框。
    - **注意**：
        1. 要想让多个单选框实现单选的效果，则多个单选框的 name 属性值必须一样。
        2. 一般会给每一个单选框提供 value 属性，指定其被选中后提交的值。
        3. checked 属性，可以指定默认值。
- **checkbox**：复选框。
    - **注意**：
        1. 一般会给每一个复选框提供 value 属性，指定其被选中后提交的值。
        2. checked 属性，可以指定默认值，可以简写为checked。
- **file**：文件选择框。
- **hidden**：隐藏域，用于提交一些信息。界面上看不到，但它自己提交了。
- **按钮**：
    - **submit**：提交按钮，可以提交表单。
    - **button**：普通按钮。
    - **image**：图片提交按钮，src 属性指定图片的路径。

### label

指定输入项的文字描述信息。

#### 注意

有光标出现！好玩！

label 的 for 属性一般会和 input 的 id 属性值对应。如果对应了，则点击 label 区域，会让 input 输入框获取焦点。

![[Pasted image 20250506201308.png]]

### select

下拉列表，子元素为 option，用于指定列表项。加selected默认选中。

### textarea

文本域。

#### 属性

- **cols**：指定列数，每一行有多少个字符。
- **rows**：默认多少行。

![[Pasted image 20250506202335.png]]

``` html
<!DOCTYPE html>  
<html lang="en">  
<head>  
    <meta charset="UTF-8">  
    <title>Login</title>  
</head>  
<body>  
    <form action="#" method="post">  
        <table border="1" align="center" width="800" cellspacing="0" cellpadding="5" height="800">  
            <tr>  
                <td><label for="username">用户名</label></td>  
                <td><input type="text" name="username" id="username" placeholder="请输入用户名"></td>  
            </tr>  
  
            <tr>  
                <td><label for="password">密码</label></td>  
                <td><input type="password" name="password" id="password" placeholder="请输入密码"></td>  
            </tr>  
            <tr>  
                <td><label for="email">邮箱</label></td>  
                <td><input type="email" name="email" id="email" placeholder="请输入邮箱"></td>  
            </tr>  
            <tr>  
                <td><label for="name">姓名</label></td>  
                <td><input type="text" name="name" id="name" placeholder="请输入姓名"></td>  
            </tr>  
            <tr>  
                <td><label for="tel">电话号码</label></td>  
                <td><input type="tel" name="tel" id="tel" placeholder="请输入电话号码"></td>  
            </tr>  
            <tr>  
                <td><label for="school">学校</label></td>  
                <td>  
                    <select name="school" id="school">  
                        <option value="1">南京邮电大学</option>  
                        <option value="2">NJUPT</option>  
                        <option value="3">皇家邮电大学</option>  
                        <option value="4">南邮</option>  
                    </select>  
                </td>  
            </tr>  
            <tr>  
                <td><label>性别</label></td>  
                <td>  
                    <input type="radio" name="gender" value="female" checked>女  
                    <input type="radio" name="gender" value="male">男  
                </td>  
            </tr>  
            <tr>  
                <td><label for="birthday">出生日期</label></td>  
                <td><input type="date" name="birthday" id="birthday"></td>  
            </tr>  
            <tr>  
                <td>证件照</td>  
                <td>  
                    <input type="file" name="photo">  
                </td>  
            </tr>  
            <tr>  
                <td>请用不少于一百字赞美南邮</td>  
                <td>  
                   <textarea cols="60" rows="5" name="description"></textarea>  
                </td>  
            </tr>  
            <tr>  
                <td><label for="checkingcode" >验证码</label></td>  
                <td>  
                    <input type="text" name="checkingcode" id="checkingcode">  
                    <img src="../images/verify_code.jpg">看不清？换一张  
                </td>  
            </tr>  
            <tr>  
                <td colspan="2" align="center">  
                    <input type="submit" value="注册"><br>  
                    <input type="reset" value="重置">  
                </td>  
  
            </tr>  
        </table>  
    </form>  
</body>  
</html>
```

# CSS：页面美化和布局控制

## 概念

Cascading Style Sheets，即层叠样式表。

### 层叠

多个样式可以作用在同一个 html 的元素上，同时生效。

## 好处

1. 功能强大。
2. 将内容展示和样式控制分离：

  

- 降低耦合度，解耦。
- 让分工协作更容易。
- 提高开发效率。

## CSS 的使用：CSS 与 html 结合方式

1. **内联样式**：在标签内使用 style 属性指定 css 代码。例如：`<div style="color:red;">hello css</div>`。
2. **内部样式**：在 head 标签内，定义 style 标签，style 标签的标签体内容就是 css 代码。例如：

  

html

预览

```html
<style>
    div{
        color:blue;
    }
</style>
<div>hello css</div>
```

  

3. **外部样式**：

  

- 定义 css 资源文件。
- 在 head 标签内，定义 link 标签，(用link的时候可以写link:css然后按TAB键就自动补全)引入外部的资源文件。例如：
    - **a.css 文件**：

  

css

```css
div{
    color:green;
}
```

  

- **html 文件**：

  

html

预览

```html
<link rel="stylesheet" href="css/a.css">
<div>hello css</div>
<div>hello css</div>
```

  

**注意**：

  

- 以上 1、2、3 种方式，css 作用范围越来越大。
- 1 方式不常用，后期常用 2、3。
- 3 种格式也可以写为（不常用）：

  

html

预览

```html
<style>
    @import "css/a.css";
</style>
```

## css 语法

1. **格式**：

  

css

```css
选择器 {
    属性名1:属性值1;
    属性名2:属性值2;
   ...
}
```

  

2. **选择器**：筛选具有相似特征的元素。
3. **注意**：每一对属性需要使用；隔开，最后一对属性可以不加；。

## 选择器：筛选具有相似特征的元素

1. **分类**：

  

- **基础选择器**：
    1. **id 选择器**：选择具体的 id 属性值的元素，建议在一个 html 页面中 id 值唯一。语法：`#id属性值{}`。
    2. **元素选择器**：选择具有相同标签名称的元素。语法：`标签名称{}`。注意：id 选择器优先级高于元素选择器。
    3. **类选择器**：选择具有相同的 class 属性值的元素。语法：`.class属性值{}`。注意：类选择器选择器优先级高于元素选择器。

优先级：id>class>元素

- **扩展选择器**：
    
    1. **选择所有元素**：语法：`*{}` 。
    2. **并集选择器**：`选择器1,选择器2{}`。
    3. **子选择器**：筛选选择器 1 元素下的选择器 2 元素。语法：`选择器1 选择器2{}`。
    4. **父选择器**：筛选选择器 2 的父元素选择器 1。语法：`选择器1 > 选择器2{}`。
    5. **属性选择器**：选择元素名称，属性名 = 属性值的元素。语法：`元素名称[属性名="属性值"]{}`。
    6. **伪类选择器**：选择一些元素具有的状态。语法：`元素:状态{}`。例如`<a>`标签的状态：
    
    - **link**：初始化的状态。
    - **visited**：被访问过的状态。
    - **active**：正在访问状态。
    - **hover**：鼠标悬浮状态。

## 属性

1. **字体、文本**：

  

- **font-size**：字体大小。
- **color**：文本颜色。
- **text-align**：对齐方式。
- **line-height**：行高 。

  

2. **背景**：**background**。复合属性。后面加no-repeat就不重复了,后面也可以加center。背景图全覆盖：background-size:cover。
3. **边框**：**border**，设置边框，复合属性。
4. **尺寸**：

  

- **width**：宽度。
- **height**：高度。

  

5. **盒子模型：控制布局**：

  

- **margin**：外边距。
- **padding**：内边距。默认情况下内边距会影响整个盒子的大小，`box-sizing: border-box;`设置盒子的属性，让 width 和 height 就是最终盒子的大小。
- **float**：浮动，有**left**和**right**两个值。

网页比例若不合适，加html{width:100%;height:100%}

# 案例

html

预览

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>注册页面</title>
<style>
    *{
        margin: 0px;
        padding: 0px;
        box-sizing: border-box;
    }
    body{
        background: url("img/register_bg.png") no-repeat center;
        padding-top: 25px;
    }

   .rg_layout{
        width: 900px;
        height: 500px;
        border: 8px solid #EEEEEE;
        background-color: white;
        /*让div水平居中*/
        margin: auto;
    }

   .rg_left{
        /*border: 1px solid red;*/
        float: left;
        margin: 15px;
    }
   .rg_left > p:first-child{
        color:#FFD026;
        font-size: 20px;
    }

   .rg_left > p:last-child{
        color:#A6A6A6;
        font-size: 20px;

    }


   .rg_center{
        float: left;
       /* border: 1px solid red;*/

    }

   .rg_right{
        /*border: 1px solid red;*/
        float: right;
        margin: 15px;
    }

   .rg_right > p:first-child{
        font-size: 15px;

    }
   .rg_right p a {
        color:pink;
    }

   .td_left{
        width: 100px;
        text-align: right;
        height: 45px;
    }
   .td_right{
        padding-left: 50px ;
    }

    #username,#password,#email,#name,#tel,#birthday,#checkcode{
        width: 251px;
        height: 32px;
        border: 1px solid #A6A6A6 ;
        /*设置边框圆角*/
        border-radius: 5px;
        padding-left: 10px;
    }
    #checkcode{
        width: 110px;
    }

    #img_check{
        height: 32px;
        vertical-align: middle;
    }

    #btn_sub{
        width: 150px;
        height: 40px;
        background-color: #FFD026;
        border: 1px solid #FFD026 ;
    }

</style>

</head>
<body>

<div class="rg_layout">
    <div class="rg_left">
        <p>新用户注册</p>
        <p>USER REGISTER</p>

    </div>

    <div class="rg_center">
        <div class="rg_form">
            <!--定义表单 form-->
            <form action="#" method="post">
                <table>
                    <tr>
                        <td class="td_left"><label for="username">用户名</label></td>
                        <td class="td_right"><input type="text" name="username" id="username" placeholder="请输入用户名"></td>
                    </tr>

                    <tr>
                        <td class="td_left"><label for="password">密码</label></td>
                        <td class="td_right"><input type="password" name="password" id="password" placeholder="请输入密码"></td>
                    </tr>

                    <tr>
                        <td class="td_left"><label for="email">Email</label></td>
                        <td class="td_right"><input type="email" name="email" id="email" placeholder="请输入邮箱"></td>
                    </tr>

                    <tr>
                        <td class="td_left"><label for="name">姓名</label></td>
                        <td class="td_right"><input type="text" name="name" id="name" placeholder="请输入姓名"></td>
                    </tr>

                    <tr>
                        <td class="td_left"><label for="tel">手机号</label></td>
                        <td class="td_right"><input type="text" name="tel" id="tel" placeholder="请输入手机号"></td>
                    </tr>

                    <tr>
                        <td class="td_left"><label>性别</label></td>
                        <td class="td_right">
                            <input type="radio" name="gender" value="male"> 男
                            <input type="radio" name="gender" value="female"> 女
                        </td>
                    </tr>

                    <tr>
                        <td class="td_left"><label for="birthday">出生日期</label></td>
                        <td class="td_right"><input type="date" name="birthday" id="birthday" placeholder="请输入出生日期"></td>
                    </tr>

                    <tr>
                        <td class="td_left"><label for="checkcode ">验证码</label></td>
                        <td class="td_right"><input type="text" name="checkcode" id="checkcode" placeholder="请输入验证码">
                            <img id="img_check" src="img/verify_code.jpg">
                        </td>
                    </tr>


                    <tr>
                        <td colspan="2" align="center"><input type="submit" id="btn_sub" value="注册"></td>
                    </tr>
                </table>

            </form>


        </div>

    </div>

    <div class="rg_right">
        <p>已有账号?<a href="#">立即登录</a></p>
    </div>


</div>


</body>
</html>
```



  

  

  

  

  

  

  

  

  

  

  

  

  

  

  

  

  

  

  



