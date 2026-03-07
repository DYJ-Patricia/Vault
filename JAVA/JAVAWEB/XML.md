# XML 知识笔记

## XML 概念

1. **全称**：Extensible Markup Language，可扩展标记语言。
2. **可扩展性**：标签都是自定义的，例如 <user>、<student>。
3. **功能**
    - 用于存储数据，可作为配置文件。
    - 在网络中传输数据。
4. **与 HTML 的区别**
    - XML 标签自定义，HTML 标签预定义。
    - XML 语法严格，HTML 语法相对松散。
    - XML 主要用于存储数据，HTML 主要用于展示数据。
5. **W3C**：万维网联盟，与 XML 相关标准制定等工作有关。

## XML 语法

1. **基本语法**
    - XML 文档后缀名是 .xml。
    - 第一行必须定义文档声明。
    - 文档中有且仅有一个根标签。
    - 属性值必须使用引号（单双引号均可）引起来。
    - 标签必须正确关闭。
    - 标签名称区分大小写。
2. **示例**

  

xml

```xml
<?xml version='1.0' ?>
<users>
    <user id='1'>
        <name>zhangsan</name>
        <age>23</age>
        <gender>male</gender>
        <br/>
    </user>
    <user id='2'>
        <name>lisi</name>
        <age>24</age>
        <gender>female</gender>
    </user>
</users>
```

  

3. **组成部分**
    - **文档声明**
        - 格式：。
        - 属性列表：
            - version：版本号，是必须的属性。
            - encoding：编码方式，告知解析引擎当前文档使用的字符集，默认值是 ISO-8859-1。
            - standalone：是否独立，取值为 yes（不依赖其他文件）或 no（依赖其他文件） 。
    - **指令（了解）**：结合 css 的指令，例如 。
    - **标签**：标签名称自定义，规则如下：
        - 名称可以包含字母、数字以及其他的字符。
        - 名称不能以数字或者标点符号开始。
        - 名称不能以字母 xml（或者 XML、Xml 等等）开始。
        - 名称不能包含空格。
    - **属性**：id 属性值唯一。
    - **文本**：CDATA 区，在该区域中的数据会被原样展示，格式为 。
4. **约束**
    - 作为框架的使用者（程序员）需要能够在 xml 中引入约束文档，并能简单读懂约束文档。
    - **分类**
        - **DTD**：一种简单的约束技术。引入 dtd 文档到 xml 文档中，分为内部 dtd（将约束规则定义在 xml 文档中）和外部 dtd（将约束的规则定义在外部的 dtd 文件中，本地引入方式：，网络引入方式： ）。
        - **Schema**：一种复杂的约束技术。引入方式为填写 xml 文档的根元素，引入 xsi 前缀 xmlns:xsi="[http://www.w3.org/2001/XMLSchema-instance](http://www.w3.org/2001/XMLSchema-instance)"，引入 xsd 文件命名空间 xsi:schemaLocation="[http://www.itcast.cn/xml](http://www.itcast.cn/xml) student.xsd"，为每一个 xsd 约束声明一个前缀 xmlns="[http://www.itcast.cn/xml](http://www.itcast.cn/xml)"。

## XML 解析

1. **操作 xml 文档**
    - **解析（读取）**：将文档中的数据读取到内存中。
    - **写入**：将内存中的数据保存到 xml 文档中，实现持久化的存储。
2. **解析 xml 的方式**
    - **DOM**：将标记语言文档一次性加载进内存，在内存中形成一颗 dom 树。
        - 优点：操作方便，可以对文档进行 CRUD（增删改查）的所有操作。
        - 缺点：占内存。
    - **SAX**：逐行读取，基于事件驱动。
        - 优点：不占内存。
        - 缺点：只能读取，不能增删改。
3. **xml 常见的解析器**
    - **JAXP**：sun 公司提供的解析器，支持 dom 和 sax 两种思想。
    - **DOM4J**：一款非常优秀的解析器。
    - **Jsoup**：jsoup 是一款 Java 的 HTML 解析器，可直接解析某个 URL 地址、HTML 文本内容。它提供了一套非常省力的 API，可通过 DOM，CSS 以及类似于 jQuery 的操作方法来取出和操作数据。
    - **PULL**：Android 操作系统内置的解析器，基于 sax 方式。
4. **Jsoup 的使用**
    - **快速入门步骤**：导入 jar 包，获取 Document 对象，获取对应的标签 Element 对象，获取数据。
    - **代码示例**

  

java

```java
//2.1获取student.xml的path
String path = JsoupDemo1.class.getClassLoader().getResource("student.xml").getPath();
//2.2解析xml文档，加载文档进内存，获取dom树--->Document
Document document = Jsoup.parse(new File(path), "utf-8");
//3.获取元素对象 Element
Elements elements = document.getElementsByTag("name");

System.out.println(elements.size());
//3.1获取第一个name的Element对象
Element element = elements.get(0);
//3.2获取数据
String name = element.text();
System.out.println(name);
```

  

- **对象的使用**
    - **Jsoup**：工具类，可以解析 html 或 xml 文档，返回 Document。其中 parse 方法有多种形式，如 parse (File in, String charsetName) 用于解析 xml 或 html 文件；parse (String html) 用于解析 xml 或 html 字符串；parse (URL url, int timeoutMillis) 通过网络路径获取指定的 html 或 xml 的文档对象。
    - **Document**：文档对象，代表内存中的 dom 树。获取 Element 对象的方法有 getElementById (String id)（根据 id 属性值获取唯一的 element 对象）、getElementsByTag (String tagName)（根据标签名称获取元素对象集合）、getElementsByAttribute (String key)（根据属性名称获取元素对象集合）、getElementsByAttributeValue (String key, String value)（根据对应的属性名和属性值获取元素对象集合） 。
    - **Elements**：元素 Element 对象的集合，可以当做 ArrayList<Element>来使用。
    - **Element**：元素对象。获取子元素对象的方法同 Document 中获取 Element 对象类似；获取属性值使用 String attr (String key)（根据属性名称获取属性值）；获取文本内容使用 String text ()（获取文本内容）和 String html ()（获取标签体的所有内容，包括子标签的字符串内容） 。
    - **Node**：节点对象，是 Document 和 Element 的父类。
- **快捷查询方式**
    - **selector**：选择器，使用的方法是 Elements select (String cssQuery) ，语法参考 Selector 类中定义的语法。
    - **XPath**：XPath 即为 XML 路径语言，它是一种用来确定 XML（标准通用标记语言的子集）文档中某部分位置的语言。使用 Jsoup 的 Xpath 需要额外导入 jar 包，通过查询 w3cshool 参考手册，使用 xpath 的语法完成查询。

  

java

```java
//1.获取student.xml的path
String path = JsoupDemo6.class.getClassLoader().getResource("student.xml").getPath();
//2.获取Document对象
Document document = Jsoup.parse(new File(path), "utf-8");

//3.根据document对象，创建JXDocument对象
JXDocument jxDocument = new JXDocument(document);

//4.结合xpath语法查询
//4.1查询所有student标签
List<JXNode> jxNodes = jxDocument.selN("//student");
for (JXNode jxNode : jxNodes) {
    System.out.println(jxNode);
}

System.out.println("--------------------");

//4.2查询所有student标签下的name标签
List<JXNode> jxNodes2 = jxDocument.selN("//student/name");
for (JXNode jxNode : jxNodes2) {
    System.out.println(jxNode);
}

System.out.println("--------------------");

//4.3查询student标签下带有id属性的name标签
List<JXNode> jxNodes3 = jxDocument.selN("//student/name[@id]");
for (JXNode jxNode : jxNodes3) {
    System.out.println(jxNode);
}
System.out.println("--------------------");
//4.4查询student标签下带有id属性的name标签 并且id属性值为itcast

List<JXNode> jxNodes4 = jxDocument.selN("//student/name[@id='itcast']");
for (JXNode jxNode : jxNodes4) {
    System.out.println(jxNode);
}
```