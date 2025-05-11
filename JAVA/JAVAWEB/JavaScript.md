# JavaScript 基础

## JavaScript

### 概念

- 一门客户端脚本语言。
- 运行在客户端浏览器中，每一个浏览器都有 JavaScript 的解析引擎。
- 脚本语言，不需要编译，直接就可以被浏览器解析执行。

### 功能

- 可以增强用户和 html 页面的交互过程，控制 html 元素，让页面有动态效果，提升用户体验。

### JavaScript 发展史

1. 1992 年，Nombase 公司开发出第一门客户端脚本语言，用于表单校验，命名为 C--，后更名为 ScriptEase。
2. 1995 年，Netscape（网景）公司开发了 LiveScript，后请来 SUN 公司专家修改，命名为 JavaScript。
3. 1996 年，微软抄袭 JavaScript 开发出 JScript 语言。
4. 1997 年，ECMA（欧洲计算机制造商协会）制定出客户端脚本语言的标准：ECMAScript，统一了所有客户端脚本语言的编码方式。
5. JavaScript = ECMAScript + JavaScript 自己特有的东西（BOM+DOM）。

## ECMAScript：客户端脚本语言的标准

### 基本语法

#### 与 html 结合方式

1. **内部 JS**：定义`<script>`，标签体内容就是 js 代码。
2. **外部 JS**：定义`<script>`，通过 src 属性引入外部的 js 文件。
3. **注意**：
    - `<script>`可以定义在 html 页面的任何地方，但定义位置会影响执行顺序。
    - `<script>`可以定义多个。

#### 注释

1. **单行注释**：`//注释内容`
2. **多行注释**：`/*注释内容*/`

#### 数据类型

1. **原始数据类型（基本数据类型）**：
    - **number**：数字，包括整数、小数、NaN（not a number，一个不是数字的数字类型）。
    - **string**：字符串，如 "abc"、"a"、'abc'。
    - **boolean**：true 和 false。
    - **null**：一个对象为空的占位符。
    - **undefined**：未定义，如果一个变量没有初始化值，则会被默认赋值为 undefined。
2. **引用数据类型**：对象。

#### 变量

- 变量是一小块存储数据的内存空间。
- Java 语言是强类型语言，JavaScript 是弱类型语言：
    - **强类型**：开辟变量存储空间时，定义空间将来存储的数据类型，只能存储固定类型的数据。
    - **弱类型**：开辟变量存储空间时，不定义空间将来的存储数据类型，可以存放任意类型的数据。
- **语法**：`var 变量名 = 初始化值;`
- **typeof 运算符**：获取变量的类型，注：null 运算后得到的是 object。

#### 运算符

1. **一元运算符**：只有一个运算数的运算符，如`++`，`--` ，`+`（正号） 。
    - `++`，`--`：自增（自减）。
        - `++`（`--`）在前，先自增（自减），再运算。
        - `++`（`--`）在后，先运算，再自增（自减）。
    - `+`（`-`）：正负号。
    - 注意：在 JS 中，如果运算数不是运算符所要求的类型，js 引擎会自动将运算数进行类型转换。
        - 其他类型转 number：
            - string 转 number：按照字面值转换。如果字面值不是数字，则转为 NaN（不是数字的数字）。
            - boolean 转 number：true 转为 1，false 转为 0。
2. **算数运算符**：`+`，`-`，`*`，`/`，`%`等。
3. **赋值运算符**：`=`，`+=`，`-=`等。
4. **比较运算符**：`>`，`<`，`>=`，`<=`，`==`，`===`（全等于）。
    - **比较方式**：
        - 类型相同：直接比较，字符串按照字典顺序比较，按位逐一比较，直到得出大小为止。
        - 类型不同：先进行类型转换，再比较。
        - `===`：全等于，在比较之前，先判断类型，如果类型不一样，则直接返回 false。
5. **逻辑运算符**：`&&`，`||`，`!`。
    - 其他类型转 boolean(要掌握)：
        - number：0 或 NaN 为假，其他为真。
        - string：除了空字符串 ("")，其他都是 true。
        - null&undefined：都是 false。
        - 对象：所有对象都为 true。
6. **三元运算符**：`? :`表达式。
    - 语法：`表达式? 值1:值2;`，判断表达式的值，如果是 true 则取值 1，如果是 false 则取值 2。
    - 示例：`var a = 3; var b = 4; var c = a > b? 1:0;`

#### 流程控制语句

1. `if...else...`
2. `switch`：
    - 在 java 中，switch 语句可以接受的数据类型：byte，int，short，char，枚举（1.5），String（1.7），格式为`switch(变量): case 值:`。
    - 在 JS 中，switch 语句可以接受任意的原始数据类型。
3. `while`
4. `do...while`
5. `for`

#### JS 特殊语法

1. 语句以`;`结尾，如果一行只有一条语句则`;`可以省略（不建议）。
2. 变量的定义使用`var`关键字，也可以不使用：
    - 用：定义的变量是局部变量。
    - 不用：定义的变量是全局变量（不建议）。

#### 练习：99 乘法表

html

预览

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>99乘法表</title>
    <style>
        td{
            border: 1px solid;
        }

    </style>

    <script>

        document.write("<table  align='center'>");


        //1.完成基本的for循环嵌套，展示乘法表
        for (var i = 1; i <= 9 ; i++) {
            document.write("<tr>");
            for (var j = 1; j <=i ; j++) {
                document.write("<td>");

                //输出  1 * 1 = 1
                document.write(i + " * " + j + " = " + ( i*j) +"&nbsp;&nbsp;&nbsp;");

                document.write("</td>");
            }
            /*//输出换行
            document.write("<br>");*/

            document.write("</tr>");
        }

        //2.完成表格嵌套
        document.write("</table>");

    </script>
</head>
<body>

</body>
</html>
```

### 基本对象

#### Function：函数（方法）对象

1. **创建**：
    - `var fun = new Function(形式参数列表,方法体);`（忘掉吧）。
    - `function 方法名称(形式参数列表){ 方法体 }`。
    - `var 方法名 = function(形式参数列表){ 方法体 }`。
2. **方法**：（此处未详细列出具体方法，可后续补充）
3. **属性**：`length`代表形参的个数。
4. **特点**：
    - 方法定义时，形参的类型不用写，返回值类型也不写。
    - 方法是一个对象，如果定义名称相同的方法，会覆盖，不会报错。
    - 在 JS 中，方法的调用只与方法的名称有关，和参数列表无关。
    - 在方法声明中有一个隐藏的内置对象（数组），`arguments`，封装所有的实际参数。
5. **调用**：`方法名称(实际参数列表);`

#### Array: 数组对象

1. **创建**：
    - `var arr = new Array(元素列表);`。
    - `var arr = new Array(默认长度);`。
    - `var arr = [元素列表];`。
2. **方法**：
    - `join(参数)`：将数组中的元素按照指定的分隔符拼接为字符串。
    - `push()`：向数组的末尾添加一个或更多元素，并返回新的长度。
3. **属性**：`length`数组的长度。
4. **特点**：
    - JS 中，数组元素的类型可变。
    - JS 中，数组长度可变。

#### Boolean

（此处未详细展开，可后续补充相关内容，如构造函数、原型方法等）

#### Date：日期对象

1. **创建**：`var date = new Date();`
2. **方法**：
    - `toLocaleString()`：返回当前 date 对象对应的时间本地字符串格式。
    - `getTime()`：获取毫秒值，返回当前日期对象描述的时间到 1970 年 1 月 1 日零点的毫秒值差。

#### Math：数学对象

1. **创建**：特点是 Math 对象不用创建，直接使用，`Math.方法名();`。
2. **方法**：
    - `random()`：返回 0 ~ 1 之间的随机数，含 0 不含 1。
    - `ceil(x)`：对数进行上舍入。
    - `floor(x)`：对数进行下舍入。
    - `round(x)`：把数四舍五入为最接近的整数。
3. **属性**：`PI`。

#### Number

（此处未详细展开，可后续补充相关内容，如构造函数、原型方法、静态方法等）

#### String

（此处未详细展开，可后续补充相关内容，如构造函数、原型方法、字符串操作等）

#### RegExp：正则表达式对象

1. **正则表达式**：定义字符串的组成规则。
    - **单个字符**：`[]`，如`[a]`，`[ab]`，`[a-zA-Z0-9_]`。
        - 特殊符号代表特殊含义的单个字符：
            - `\d`：单个数字字符`[0-9]`。
            - `\w`：单个单词字符`[a-zA-Z0-9_]`。
    - **量词符号**：
        - `?`：表示出现 0 次或 1 次。
        - `*`：表示出现 0 次或多次。
        - `+`：出现 1 次或多次。
        - `{m,n}`：表示`m<= 数量 <= n`，`m`如果缺省：`{,n}`最多 n 次；`n`如果缺省：`{m,}`最少 m 次。
    - **开始结束符号**：
        - `^`：开始。
        - `$`：结束。
2. **正则对象**：
    - **创建**：
        - `var reg = new RegExp("正则表达式");`。
        - `var reg = /正则表达式/;`。
    - **方法**：`test(参数)`验证指定的字符串是否符合正则定义的规范。

#### Global

1. **特点**：全局对象，这个 Global 中封装的方法不需要对象就可以直接调用，`方法名();`。
2. **方法**：
    - `encodeURI()`：url 编码。
    - `decodeURI()`：url 解码。
    - `encodeURIComponent()`：url 编码，编码的字符更多。
    - `decodeURIComponent()`：url 解码。
    - `parseInt()`：将字符串转为数字，逐一判断每一个字符是否是数字，直到不是数字为止，将前边数字部分转为 number。
    - `isNaN()`：判断一个值是否是 NaN，NaN 六亲不认，连自己都不认，NaN 参与的`==`比较全部为 false。
    - `eval()`：将 JavaScript 字符串，并把它作为脚本代码来执行。
3. **URL 编码**：如传智播客 = % E4% BC% A0% E6%99% BA% E6%92% AD% E5% AE% A2


## ECMAScript

（此处未详细内容，可根据实际补充）

## BOM（Browser Object Model 浏览器对象模型）

将浏览器的各个组成部分封装成对象。

### 组成

1. **Window**：窗口对象
2. **Navigator**：浏览器对象
3. **Screen**：显示器屏幕对象
4. **History**：历史记录对象
5. **Location**：地址栏对象

### Window 窗口对象

1. **创建**：不需要创建可直接使用，`window` 使用，`window.方法名()`，`window` 引用可省略，直接 `方法名()`
2. **方法**
    - **与弹出框有关的方法**
        - `alert()`：显示带有一段消息和一个确认按钮的警告框。
        - `confirm()`：显示带有一段消息以及确认按钮和取消按钮的对话框。用户点击确定按钮返回 `true`，点击取消按钮返回 `false`。
        - `prompt()`：显示可提示用户输入的对话框，返回用户输入的值。
    - **与打开关闭有关的方法**
        - `close()`：关闭浏览器窗口，谁调用就关谁。
        - `open()`：打开一个新的浏览器窗口，返回新的 `Window` 对象。
    - **与定时器有关的方式**
        - `setTimeout()`：在指定的毫秒数后调用函数或计算表达式，参数为 `js` 代码或者方法对象和毫秒值，返回唯一标识，用于取消定时器。
        - `clearTimeout()`：取消由 `setTimeout()` 方法设置的 `timeout`。
        - `setInterval()`：按照指定的周期（以毫秒计）来调用函数或计算表达式。
        - `clearInterval()`：取消由 `setInterval()` 设置的 `timeout`。
3. **属性**
    - 获取其他 BOM 对象，如 `history`、`location`、`Navigator`、`Screen`。
    - 获取 DOM 对象，如 `document`。

### Location 地址栏对象

1. **创建 (获取)**
    - `window.location`
    - `location`
2. **方法**
    - `reload()`：重新加载当前文档，即刷新。
3. **属性**
    - `href`：设置或返回完整的 URL。

### History 历史记录对象

1. **创建 (获取)**
    - `window.history`
    - `history`
2. **方法**
    - `back()`：加载 `history` 列表中的前一个 URL。
    - `forward()`：加载 `history` 列表中的下一个 URL。
    - `go(参数)`：加载 `history` 列表中的某个具体页面，参数正数为前进几个历史记录，负数为后退几个历史记录。
3. **属性**
    - `length`：返回当前窗口历史列表中的 URL 数量。

## DOM（Document Object Model 文档对象模型）

将标记语言文档的各个组成部分，封装为对象。可以使用这些对象，对标记语言文档进行 CRUD 的动态操作。

### W3C DOM 标准被分为 3 个不同的部分

1. **核心 DOM**：针对任何结构化文档的标准模型
    - `Document`：文档对象
    - `Element`：元素对象
    - `Attribute`：属性对象
    - `Text`：文本对象
    - `Comment`：注释对象
    - `Node`：节点对象，其他 5 个的父对象
2. **XML DOM**：针对 XML 文档的标准模型
3. **HTML DOM**：针对 HTML 文档的标准模型

### 核心 DOM 模型

1. **Document 文档对象**
    - **创建 (获取)**：在 html dom 模型中可以使用 `window` 对象来获取
        - `window.document`
        - `document`
    - **方法**
        - 获取 `Element` 对象
            - `getElementById()`：根据 `id` 属性值获取元素对象，`id` 属性值一般唯一。
            - `getElementsByTagName()`：根据元素名称获取元素对象们，返回值是一个数组。
            - `getElementsByClassName()`：根据 `Class` 属性值获取元素对象们，返回值是一个数组。
            - `getElementsByName()`：根据 `name` 属性值获取元素对象们，返回值是一个数组。
        - 创建其他 DOM 对象
            - `createAttribute(name)`
            - `createComment()`
            - `createElement()`
            - `createTextNode()`
2. **Element 元素对象**
    - **获取 / 创建**：通过 `document` 来获取和创建
    - **方法**
        - `removeAttribute()`：删除属性
        - `setAttribute()`：设置属性
3. **Node 节点对象**：其他 5 个的父对象
    - **特点**：所有 dom 对象都可以被认为是一个节点
    - **方法**
        - CRUD dom 树
            - `appendChild()`：向节点的子节点列表的结尾添加新的子节点。
            - `removeChild()`：删除（并返回）当前节点的指定子节点。
            - `replaceChild()`：用新节点替换一个子节点。
    - **属性**
        - `parentNode`：返回节点的父节点。

### HTML DOM

1. 标签体的设置和获取：`innerHTML`
2. 使用 html 元素对象的属性
3. 控制元素样式
    - 使用元素的 `style` 属性来设置，示例：

  

javascript

```javascript
//修改样式方式1
div1.style.border = "1px solid red";
div1.style.width = "200px";
//font-size--> fontSize
div1.style.fontSize = "20px";
```

  

- 提前定义好类选择器的样式，通过元素的 `className` 属性来设置其 `class` 属性值。

## DOM 简单学习：为了满足案例要求

1. **功能**：控制 html 文档的内容
2. **获取页面标签 (元素) 对象**：`Element`
    - `document.getElementById("id值")`：通过元素的 `id` 获取元素对象
3. **操作 Element 对象**
    - **修改属性值**
        - 明确获取的对象是哪一个。
        - 查看 API 文档，找其中有哪些属性可以设置。
    - **修改标签体内容**
        - 属性：`innerHTML`
        - 操作步骤
            1. 获取元素对象
            2. 使用 `innerHTML` 属性修改标签体内容

## 事件简单学习

1. **功能**：某些组件被执行了某些操作后，触发某些代码的执行。造句示例：xxx 被 xxx，我就 xxx，如我方水晶被摧毁后，我就责备队友；敌方水晶被摧毁后，我就夸奖自己。
2. **如何绑定事件**
    - 直接在 html 标签上，指定事件的属性 (操作)，属性值就是 js 代码，事件如 `onclick`（单击事件）。
    - 通过 js 获取元素对象，指定事件属性，设置一个函数。
    - **代码示例**

  

html

预览

```html
<body>
    <img id="light" src="img/off.gif"  onclick="fun();">
    <img id="light2" src="img/off.gif">
    
    <script>
        function fun(){
            alert('我被点了');
            alert('我又被点了');
        }
    
        function fun2(){
            alert('咋老点我？');
        }
    
        //1.获取light2对象
        var light2 = document.getElementById("light2");
        //2.绑定事件
        light2.onclick = fun2;
    </script>
</body>
```

  

3. **案例 1：电灯开关**

  

html

预览

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>电灯开关</title>

</head>
<body>

<img id="light" src="img/off.gif">

<script>
    /*
        分析：
            1.获取图片对象
            2.绑定单击事件
            3.每次点击切换图片
                * 规则：
                    * 如果灯是开的 on,切换图片为 off
                    * 如果灯是关的 off,切换图片为 on
                * 使用标记flag来完成

     */

    //1.获取图片对象
    var light = document.getElementById("light");

    var flag = false;//代表灯是灭的。 off图片

    //2.绑定单击事件
    light.onclick = function(){
        if(flag){//判断如果灯是开的，则灭掉
            light.src = "img/off.gif";
            flag = false;

        }else{
            //如果灯是灭的，则打开

            light.src = "img/on.gif";
            flag = true;
        }


    }
</script>
</body>
</html>
```

## 事件监听机制

1. **概念**：某些组件被执行了某些操作后，触发某些代码的执行。
    - **事件**：某些操作，如单击，双击，键盘按下了，鼠标移动了。
    - **事件源**：组件，如按钮、文本输入框等。
    - **监听器**：代码。
    - **注册监听**：将事件，事件源，监听器结合在一起。当事件源上发生了某个事件，则触发执行某个监听器代码。
2. **常见的事件**
    - **点击事件**
        - `onclick`：单击事件
        - `ondblclick`：双击事件
    - **焦点事件**
        - `onblur`：失去焦点
        - `onfocus`：元素获得焦点
    - **加载事件**
        - `onload`：一张页面或一幅图像完成加载
    - **鼠标事件**
        - `onmousedown`：鼠标按钮被按下
        - `onmouseup`：鼠标按键被松开
        - `onmousemove`：鼠标被移动
        - `onmouseover`：鼠标移到某元素之上
        - `onmouseout`：鼠标从某元素移开
    - **键盘事件**
        - `onkeydown`：某个键盘按键被按下
        - `onkeyup`：某个键盘按键被松开
        - `onkeypress`：某个键盘按键被按下并松开
    - **选择和改变**
        - `onchange`：域的内容被改变
        - `onselect`：文本被选中
    - **表单事件**
        - `onsubmit`：确认按钮被点击
        - `onreset`：重置按钮被点击