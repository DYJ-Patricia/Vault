
# Day1
## 一、 Java背景知识

在正式开干之前，我们先了解一下Java的背景知识，方便以后你在和大家聊Java的时候可以说到一块去。

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D4b49deae9h69ab74731987cec086e322%26expires%3D24h%26dp_logid%3D443618247035549586%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-IPSvcXWUEjXOEajq9LjZ8%25252B9UVvE%25253D%26file_size%3D33801%26timestamp%3D1745903341%26method%3Dinfo%26fid%3D3170504070-250528-140924858986399%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day01-Java%E5%85%A5%E9%97%A8.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday01-Java%E5%85%A5%E9%97%A8%2Fday01-Java%E5%85%A5%E9%97%A8.md&fs_id=140924858986399&size=33801&uk=3170504070&from=yuanguanjia&fsid=140924858986399&clienttype=8&scence=mac_main#11-java%E8%AF%AD%E8%A8%80%E7%9A%84%E5%8E%86%E5%8F%B2)1.1 Java语言的历史

- **Java是哪家公司的产品？**
    
    Java是美国Sun（Stanford University Network，斯坦福大学网络公司）公司在1995年推出的一门计算机**高级编程语言**。但是在2009年是Sun公司被Oracle（甲骨文）公司给收购了，所以目前Java语言是Oracle公司所有产品。
    
- **Java名称的来历？**
    
    早期这门语言的名字其实不叫Java，当时称为Oak（橡树的意思），为什么叫橡树呢？原因是因为Sun公司的门口种了很多橡树，但是后来由于商标注册时，Oak商标已经其他公司注册了，所以后面改名为Java了。那么有人好奇为什么叫Java呢？Java是印度的一个岛屿，上面盛产咖啡，可能是因为他们公司的程序员喜欢喝咖啡，所以就改名为Java了。
    
- **Java的创始人是谁？**
    
- 说完Java名称的来历之后，接下来我们聊聊Java的祖师爷是谁？ Java的联合创始人有很多，但是行业普遍认可的Java的创始人 是**詹姆斯●高斯林**，被称为Java之父
    

![1660152660273](https://pan.baidu.com/wap/assets/1660152660273.png)

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D4b49deae9h69ab74731987cec086e322%26expires%3D24h%26dp_logid%3D443618247035549586%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-IPSvcXWUEjXOEajq9LjZ8%25252B9UVvE%25253D%26file_size%3D33801%26timestamp%3D1745903341%26method%3Dinfo%26fid%3D3170504070-250528-140924858986399%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day01-Java%E5%85%A5%E9%97%A8.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday01-Java%E5%85%A5%E9%97%A8%2Fday01-Java%E5%85%A5%E9%97%A8.md&fs_id=140924858986399&size=33801&uk=3170504070&from=yuanguanjia&fsid=140924858986399&clienttype=8&scence=mac_main#12-java%E8%83%BD%E5%81%9A%E4%BB%80%E4%B9%88)1.2 Java能做什么

了解了Java语言的历史之后，接下来，大家比较关心的问题可能是Java到底能做什么了？

![1660141834075](https://pan.baidu.com/wap/assets/1660141834075.png)

其实Java能做的事情非常多，它可以做桌面应用的开发、企业互联网应用开发、移动应用开发、服务器系统开发、大数据开发、游戏开发等等。

```
1.桌面应用开发：能够在电脑桌面运行的软件
	举例：财务管理软件、编写程序用的IDEA开发工具等，可以用Java语言开发
	
2.企业级应用开发：大型的互联网应用程序
	举例：淘宝、京东、大家每天都用的tlias教学管理系统等

3.移动应用开发：运行的Android手机端的软件
	举例：QQ客户端、抖音APP等

4.服务器系统：应用程序的后台（为客户端程序提供数据）
	举例：服务器系统为用户推荐那你喜爱的视频

5.大数据开发：大数据是一个互联网开发方向
	举例：目前最火的大数据开发平台是Hadoop，就是用Java语言开发的

6.游戏开发：游戏本质上是给用户提供娱乐的软件，有良好的交互感受
	举例：我的世界MineCraft就是用Java语言开发的
```

虽然Java能做的事情非常多，但并不是每一个方向都被市场认可（比如桌面应用使用Java语言开发就不太方便，而使用C#语言是比较推荐的）。**目前Java的主流开发方向是使用Java开发企业级互联网应用程序**（很多公司的OA系统，客户关系管理系统，包括传智播客使用教学实施管理系统都是用Java语言开发的）

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D4b49deae9h69ab74731987cec086e322%26expires%3D24h%26dp_logid%3D443618247035549586%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-IPSvcXWUEjXOEajq9LjZ8%25252B9UVvE%25253D%26file_size%3D33801%26timestamp%3D1745903341%26method%3Dinfo%26fid%3D3170504070-250528-140924858986399%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day01-Java%E5%85%A5%E9%97%A8.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday01-Java%E5%85%A5%E9%97%A8%2Fday01-Java%E5%85%A5%E9%97%A8.md&fs_id=140924858986399&size=33801&uk=3170504070&from=yuanguanjia&fsid=140924858986399&clienttype=8&scence=mac_main#13-java%E7%9A%84%E6%8A%80%E6%9C%AF%E4%BD%93%E7%B3%BB)1.3 Java的技术体系

说完Java语言能做什么之后，接下来我们再给同学们介绍一下Java的技术体系。所谓技术体系，就是Java为了满足不同的应用场景提供了不同的技术版本，主要有三个版本。

- Java SE（Java Standard Edition）：叫做标准版，它是后面两个版本的基础，也就是学习后面两个版本必须先学习JavaSE。**我们基础班现阶段学习的就是这个版本中的技术**。
    
- Java EE（Java Enterprise Edition）: 叫做企业版，它是为企业级应用开发提供的一套解决方案。**在后面就业班课程中主要学习这个版本中的技术**。
    
- Java ME（Java Micro Edition）：叫做小型版，它为开发移动设备的应用提供了一套解决方案。**目前已经不被市场认可（淘汰），取而代之的是基于Android系统的应用开发**。
    

---

Java语言的相关背景就给大家介绍到这里了，这些内容小伙伴们也不用刻意去记，简单了解一下就可以了。下面我们在简要回顾一下

```
1.Java是什么？
	答：Java是一门高级编程语言
	
2.Java是哪家公司的产品？
	答：Java以前是Sun公司的产品，现在Java是属于Oracle公司的产品
	
3.Java之父是谁？
	答：詹姆斯●高斯林
	
4.Java主流的开发方向是什么？
	答：企业级互联网应用开发
	
5.Java技术平台有哪些？
	答：JavaSE（标准版）、JavaEE（企业版）、JavaME（小型版）
```

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D4b49deae9h69ab74731987cec086e322%26expires%3D24h%26dp_logid%3D443618247035549586%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-IPSvcXWUEjXOEajq9LjZ8%25252B9UVvE%25253D%26file_size%3D33801%26timestamp%3D1745903341%26method%3Dinfo%26fid%3D3170504070-250528-140924858986399%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day01-Java%E5%85%A5%E9%97%A8.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday01-Java%E5%85%A5%E9%97%A8%2Fday01-Java%E5%85%A5%E9%97%A8.md&fs_id=140924858986399&size=33801&uk=3170504070&from=yuanguanjia&fsid=140924858986399&clienttype=8&scence=mac_main#%E4%BA%8C-java%E5%BF%AB%E9%80%9F%E5%85%A5%E9%97%A8)二、 Java快速入门

上一章我们给小伙伴们介绍了Java的相关背景，你们现在是不是就想马上用一下Java呀？先不着急，我们得先得安装Java的开发环境，才能使用Java语言开发程序（ps: 就像你先需要安装微信，才能使用微信和朋友聊天是一样的）。

这里所说的Java开发环境，实际上就是Java官方提供的一个软件，叫做JDK（全称是Java Develop Kit），翻译过来意思就是Java开发工具包。**我们先要到官网上去下载JDK，然后安装在自己的电脑上，才可以在自己的电脑上使用JDK来开发Java程序**

JDK的版本有很多，下图是JDK版本更新的历程图，有LTS标识的是长期支持版本（意思就是Oracle会不定期更新）。目前公司中用得最多的版本是JDK8版本，在目前这套课程中我们为了将一些新特性会使用JDK17版本。

![1660143538211](https://pan.baidu.com/wap/assets/1660143538211.png)

下面已经给小伙伴们提供了详细的JDK下载和安装过程的截图，大家只需要按照步骤操作就行。

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D4b49deae9h69ab74731987cec086e322%26expires%3D24h%26dp_logid%3D443618247035549586%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-IPSvcXWUEjXOEajq9LjZ8%25252B9UVvE%25253D%26file_size%3D33801%26timestamp%3D1745903341%26method%3Dinfo%26fid%3D3170504070-250528-140924858986399%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day01-Java%E5%85%A5%E9%97%A8.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday01-Java%E5%85%A5%E9%97%A8%2Fday01-Java%E5%85%A5%E9%97%A8.md&fs_id=140924858986399&size=33801&uk=3170504070&from=yuanguanjia&fsid=140924858986399&clienttype=8&scence=mac_main#21-jdk%E4%B8%8B%E8%BD%BD%E5%92%8C%E5%AE%89%E8%A3%85)2.1 JDK下载和安装

- **JDK的下载**

这是JDK下载的官方网址 [https://www.oracle.com/java/technologies/downloads/，你需要把该网址复制到浏览器的地址栏，敲回车](https://www.oracle.com/java/technologies/downloads/%EF%BC%8C%E4%BD%A0%E9%9C%80%E8%A6%81%E6%8A%8A%E8%AF%A5%E7%BD%91%E5%9D%80%E5%A4%8D%E5%88%B6%E5%88%B0%E6%B5%8F%E8%A7%88%E5%99%A8%E7%9A%84%E5%9C%B0%E5%9D%80%E6%A0%8F%EF%BC%8C%E6%95%B2%E5%9B%9E%E8%BD%A6)

![1660527717279](https://pan.baidu.com/wap/assets/1660527717279.png)

进入网址后，选择JDK17版本，找到Windows标签，选择x64 Installer版本。如下图所示

![1660527981411](https://pan.baidu.com/wap/assets/1660527981411.png)

下载完成之后，在你下载的目录下会出现一个JDK的安装包，如下图所示

![1660528307458](https://pan.baidu.com/wap/assets/1660528307458.png)

到这JDK的下载就完成了，接下来就需要按照下面的步骤完成JDK安装.

- **JDK的安装**

双击安装包，按照下图引导，点击下一步即可安装。**需要注意的是安装JDK后不像你安装QQ一样会在桌面上显示一个图标，JDK安装后桌面上没有图标！！！**

![1660144855615](https://pan.baidu.com/wap/assets/1660144855615.png)

**如何验证安装成功了呢？**

刚才不是让你记住安装目录吗？你记住了吗？如果你自己修改过目录，就打开你自己修改的目录（呀！！忘记了o(╥﹏╥)o，那我帮不了你了，谁让你不认真听讲的）；如果没有修改安装目录，默认在`C:\Program Files\Java\jdk-17.0.3`目录下。

在文件资源管理器打开JDK的安装目录的bin目录，会发现有两个命令工具 `javac.exe` `java.exe` ，这就是JDK提供给我们使用的**编译工具和运行工具**，如下图所示

![1660145259521](https://pan.baidu.com/wap/assets/1660145259521.png)

我们现在就使用一下 `javac.exe` `java.exe` 这两个工具，测试一下JDK是否可用

1. 第一步：在JDK的bin目录，地址栏输入cmd，回车

![1660529458474](https://pan.baidu.com/wap/assets/1660529458474.png)

输入完cmd回车后，会出现一个黑窗口，专业说法叫**命令行窗口**

![1660529493477](https://pan.baidu.com/wap/assets/1660529493477.png)

2. 第二步：在命令行窗口中输入 `javac -version`回车，然后输入`java -version`回车
    
    如果出现下面红色框框的提示正确版本号，和我们安装的JDK版本号一致，就说明JDK安装成功
    

![1660145482256](https://pan.baidu.com/wap/assets/1660145482256.png)

做完以上步骤之后，恭喜小伙伴_，你的电脑上就已经有Java的开发环境了，接下来可以开发Java程序了。

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D4b49deae9h69ab74731987cec086e322%26expires%3D24h%26dp_logid%3D443618247035549586%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-IPSvcXWUEjXOEajq9LjZ8%25252B9UVvE%25253D%26file_size%3D33801%26timestamp%3D1745903341%26method%3Dinfo%26fid%3D3170504070-250528-140924858986399%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day01-Java%E5%85%A5%E9%97%A8.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday01-Java%E5%85%A5%E9%97%A8%2Fday01-Java%E5%85%A5%E9%97%A8.md&fs_id=140924858986399&size=33801&uk=3170504070&from=yuanguanjia&fsid=140924858986399&clienttype=8&scence=mac_main#22-cmd%E5%B8%B8%E8%A7%81%E5%91%BD%E4%BB%A4)2.2 cmd常见命令

前面测试JDK是否安装成功，需要在黑窗口中输入`javac -version`和`java -version` 这其实就是JDK查看编译工具和运行工具版本号的命令。

这种输入命令的和电脑交互的方式，称之为命令行交互。也就是说，可以使用命令指挥电脑做事情。接下来我们了解几种Windows系统常见的命令，后面可能会用到。

下面是Windows系统常见的命令以及作用，小伙伴们可以自己试一试。需要注意的是，每敲完一条命令之后，马上敲回车就表示执行这条命名。

```
E:  //切换到E盘
cd [目录]        //进入指定的目录
cd ..         //退回到上一级目录
cd /         //退回到根目录
dir             //显示当前目录下所有的内容
cls             //清空屏幕
```

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D4b49deae9h69ab74731987cec086e322%26expires%3D24h%26dp_logid%3D443618247035549586%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-IPSvcXWUEjXOEajq9LjZ8%25252B9UVvE%25253D%26file_size%3D33801%26timestamp%3D1745903341%26method%3Dinfo%26fid%3D3170504070-250528-140924858986399%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day01-Java%E5%85%A5%E9%97%A8.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday01-Java%E5%85%A5%E9%97%A8%2Fday01-Java%E5%85%A5%E9%97%A8.md&fs_id=140924858986399&size=33801&uk=3170504070&from=yuanguanjia&fsid=140924858986399&clienttype=8&scence=mac_main#23-java%E5%85%A5%E9%97%A8%E7%A8%8B%E5%BA%8F)2.3 Java入门程序

上一节我们已经安装好了JDK，接下来，我们就正式开始开发第一个入门Java程序。按照国际惯例，学习任何一本编程语言第一个案例都叫做 **Hello World**，意思是向世界问好，从此开用程序和世界沟通的大门。

> **编写Java程序的步骤**

编写一个Java程序需要经过3个步骤：**编写代码，编译代码，运行代码**

![1660145843138](https://pan.baidu.com/wap/assets/1660145843138.png)

- [x]  编写代码：任何一个文本编辑器都可以些代码，如Windows系统自带的记事本
- [x]  编译代码：将人能看懂的源代码（.java文件）转换为Java虚拟机能够执行的字节码文件（.class文件）
- [x]  运行代码：将字节码文件交给Java虚拟机执行

---

> **编写第一个Java入门程序**

按照下面提供的步骤，一步一步的完成第一个Java入门程序的编写、编译和执行。

**第一步**：新建一个后缀为.java的文本文件`HelloWorld.java`，用记事本编写代码如下。

```
public class HelloWorld {
   public static void main(String[] args) {
     System.out.println(" HelloWorld ");
    }
}
```

**第二步**：进入`HelloWorld.java`文件所在目录，在地址栏输入cmd回车，即可在此处打开命令行窗口。

![1660146387184](https://pan.baidu.com/wap/assets/1660146387184.png)

编译：在命令行窗口输入编译命令`javac HelloWorld`完成编译，编译后会生成一个`HelloWorld.class`文件。

![1660146644956](https://pan.baidu.com/wap/assets/1660146644956.png)

**第三步**：再接着输入`java HelloWorld`就可以运行了，运行结果如下。

![1660146816170](https://pan.baidu.com/wap/assets/1660146816170.png)

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D4b49deae9h69ab74731987cec086e322%26expires%3D24h%26dp_logid%3D443618247035549586%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-IPSvcXWUEjXOEajq9LjZ8%25252B9UVvE%25253D%26file_size%3D33801%26timestamp%3D1745903341%26method%3Dinfo%26fid%3D3170504070-250528-140924858986399%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day01-Java%E5%85%A5%E9%97%A8.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday01-Java%E5%85%A5%E9%97%A8%2Fday01-Java%E5%85%A5%E9%97%A8.md&fs_id=140924858986399&size=33801&uk=3170504070&from=yuanguanjia&fsid=140924858986399&clienttype=8&scence=mac_main#24-java%E7%A8%8B%E5%BA%8F%E4%B8%AD%E5%B8%B8%E8%A7%81%E7%9A%84%E9%97%AE%E9%A2%98)2.4 Java程序中常见的问题

刚才小伙伴们在编写第一个HelloWorld程序的时候，是不是很容易报错啊？ 我观察过第一次写代码，90%的同学都会有些小问题的，比如单词写错了！ 括号少写一个！等等！ 我想给大家说的是，写错代码都是很正常的，**一个什么错都犯过的程序员，才是真正的程序员**。

下面我们把程序中常见的问题，总结一下。大家在写代码时注意一下这些问题就可以了

- [x]  Windows的文件扩展名没有勾选
- [x]  代码写了，但是忘记保存了
- [x]  文件名和类名不一致。
- [x]  英文大小写错误，单词拼写错误，存在中文符号，找不到main方法。
- [x]  括号不配对。
- [x]  编译或执行工具使用不当。

---

> - **文件扩展名没有打开**

下图中文件扩展名的勾勾没有勾选，就会导致你创建的文件是普通的文本文件（.txt）文件，而不是java文件。

**正确做法是把文件扩展名的勾选上**

![1660147216279](https://pan.baidu.com/wap/assets/1660147216279.png)

> - **文件名和类名不一致**

你看下图中，文件名是`HelloWorld`，但是类名是`Helloworld`看出区别了吗？一个是大写的W，一个是小写的w。 不仔细看还真看不出来。

**正确写法是文件名叫`HelloWorld`，类名也叫`HelloWorld**`

![1660531741851](https://pan.baidu.com/wap/assets/1660531741851.png)

> - **单词大小写错吴**

下图中不是string和system这两个单词都写错了， 这里是严格区分大小写的

**正确写法是String和System**

![1660531915677](https://pan.baidu.com/wap/assets/1660531915677.png)

> - **主方法写错了**

下图所示，主方法的名称写成了`mian`，这是错误的。

主方法正确写法：必须是 `public static void main(String[] args){}`，一个字母都不能错。

![1660532147208](https://pan.baidu.com/wap/assets/1660532147208.png)

> - **标点符号写错了**

下图中打印语句最后的分号，写成功中文分号`；`

**正确写法应该是英文分号** `;` 不仔细看还真看不出区别，要小心

![1660532298281](https://pan.baidu.com/wap/assets/1660532298281.png)

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D4b49deae9h69ab74731987cec086e322%26expires%3D24h%26dp_logid%3D443618247035549586%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-IPSvcXWUEjXOEajq9LjZ8%25252B9UVvE%25253D%26file_size%3D33801%26timestamp%3D1745903341%26method%3Dinfo%26fid%3D3170504070-250528-140924858986399%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day01-Java%E5%85%A5%E9%97%A8.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday01-Java%E5%85%A5%E9%97%A8%2Fday01-Java%E5%85%A5%E9%97%A8.md&fs_id=140924858986399&size=33801&uk=3170504070&from=yuanguanjia&fsid=140924858986399&clienttype=8&scence=mac_main#25-jdk%E7%9A%84%E7%BB%84%E6%88%90)2.5 JDK的组成

在前几节课中我们已经安装了JDK，并且开发了一个Java入门程序，用javac命令编译，用Java命令运行，但是对于Java程序的执行原理并没有过多的介绍。

下面我们把JDK的组成，以及跨平台原理给大家介绍一下，有利于同学们理解Java程序的执行过程。

JDK由JVM、核心类库、开发工具组成，如下图所示

![1660147531310](https://pan.baidu.com/wap/assets/1660147531310.png)

下面分别介绍一下JDK中每一个部分是用来干什么的

```
- 什么是JVM?
    答：JDK最核心的组成部分是JVM（Java Virtual Machine），它是Java虚拟机，真正运行Java程序的地方。
    
- 什么是核心类库？
	答：它是Java本身写好的一些程序，给程序员调用的。 Java程序员并不是凭空开始写代码，是要基于核心类库提供的一些基础代码，进行编程。
	
- 什么是JRE?
    答：JRE（Java Runtime Enviroment），意思是Java的运行环境；它是由JVM和核心类库组成的；如果你不是开发人员，只需要在电脑上安装JRE就可以运行Java程序。
    
- 什么是开发工具呢？
	答：Java程序员写好源代码之后，需要编译成字节码，这里会提供一个编译工具叫做javac.exe，编写好源代码之后，想要把class文件加载到内存中运行，这里需要用到运行工具java.exe。 
	除了编译工具和运行工具，还有一些其他的反编译工具、文档工具等待...
```

JDK、JRE的关系用一句话总结就是：用JDK开发程序，交给JRE运行

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D4b49deae9h69ab74731987cec086e322%26expires%3D24h%26dp_logid%3D443618247035549586%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-IPSvcXWUEjXOEajq9LjZ8%25252B9UVvE%25253D%26file_size%3D33801%26timestamp%3D1745903341%26method%3Dinfo%26fid%3D3170504070-250528-140924858986399%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day01-Java%E5%85%A5%E9%97%A8.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday01-Java%E5%85%A5%E9%97%A8%2Fday01-Java%E5%85%A5%E9%97%A8.md&fs_id=140924858986399&size=33801&uk=3170504070&from=yuanguanjia&fsid=140924858986399&clienttype=8&scence=mac_main#26-java%E7%9A%84%E8%B7%A8%E5%B9%B3%E5%8F%B0%E5%8E%9F%E7%90%86)2.6 Java的跨平台原理

学完JDK的组成后，我们知道Java程序的执行是依赖于Java虚拟机的。就是因为有了Java虚拟机所以Java程序有一个重要的特性叫做跨平台性。

- **什么是跨平台行呢？**
    
    所谓跨平台指的是用Java语言开发的程序可以在多种操作系统上运行，常见的操作系统有Windows、Linux、MacOS系统。
    
    如果没有跨平台性，同一个应用程序，想要在多种操作系统上运行，需要针对各个操作系统单独开发应用。比如微信有Windows版本、MacOS版本、Android版本、IOS版本
    
- **为什么Java程序可以跨平台呢？**
    
    跨平台性的原理是因为在**不同版本的操作系统**中安装有**不同版本的Java虚拟机**，Java程序的运行只依赖于Java虚拟机，和操作系统并没有直接关系。**从而做到一处编译，处处运行**。
    

![1660147588001](https://pan.baidu.com/wap/assets/1660147588001.png)

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D4b49deae9h69ab74731987cec086e322%26expires%3D24h%26dp_logid%3D443618247035549586%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-IPSvcXWUEjXOEajq9LjZ8%25252B9UVvE%25253D%26file_size%3D33801%26timestamp%3D1745903341%26method%3Dinfo%26fid%3D3170504070-250528-140924858986399%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day01-Java%E5%85%A5%E9%97%A8.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday01-Java%E5%85%A5%E9%97%A8%2Fday01-Java%E5%85%A5%E9%97%A8.md&fs_id=140924858986399&size=33801&uk=3170504070&from=yuanguanjia&fsid=140924858986399&clienttype=8&scence=mac_main#27-jdk%E7%8E%AF%E5%A2%83%E5%8F%98%E9%87%8F%E9%85%8D%E7%BD%AE)2.7 JDK环境变量配置

JDK安装后，接下我们来学习一个补充知识，叫做Path环境变量

- **什么是Path环境变量？**
    
    Path环境变量是让系统程序的路径，方便程序员在命令行窗口的任意目录下启动程序；
    
- **如何配置环境变量呢？**
    
    比如把QQ的启动程序，配置到Path环境变量下就可以在任意目录下启动QQ，按照一下步骤操作。
    
    **第一步：**先找到QQ启动程序所在的目录`C:\Program Files (x86)\Tencent\QQ\Bin`，复制这个路径
    
    ![1660538063180](https://pan.baidu.com/wap/assets/1660538063180.png)
    
    **第二步：**按照下面的步骤，找到Path环境变量。
    
    首先找到此电脑，右键点击属性，可以按照下面的界面；点击【高级系统设置】，再点击【环境变量】
    
    ![1660538424000](https://pan.baidu.com/wap/assets/1660538424000.png)
    
    双击Path后，点击新建，把QQ启动目录粘贴进来，不要忘记点确定哦_
    
    ![1660538760744](https://pan.baidu.com/wap/assets/1660538760744.png)
    
    **第三步：**配置好之后，检查是否配置成功
    
    ```
    1.Win+R 输入cmd回车，打开命令行窗口
    2.输入QQScLanucher，可以看到QQ启动了
    ```
    

![1660539146158](https://pan.baidu.com/wap/assets/1660539146158.png)

---

- **将JDK配置到Path路径下**
    
    上面我们配置了QQ的启动目录到Path环境变量位置，那么接下来，我们把JDK的bin目录配置到Path环境变量下，这样就可以在任意目录下启动javac和java命令来完成编译和运行了。
    
    **第一步：**找到JDK的bin目录`C:\Program Files\Java\jdk-17.0.3\bin`，复制一下
    
    **第二步：**将JDK的bin目录粘贴在Path环境变量后面
    
    ![1660539632325](https://pan.baidu.com/wap/assets/1660539632325.png)
    
    **第三步：检测否配置成功**
    
    ```
    1.按住Win+R输入cmd 回车，打开命令行创建
    2.输入javac -version 看提示信息是否显示你安装JDK的版本号
      输入java -version 看提示信息是否显示你安装JDK的版本号
    【如果显示版本号都是JDK17就表示配置安装成功】
    ```
    
    ![1660539955302](https://pan.baidu.com/wap/assets/1660539955302.png)
    

你如果按照前面的操作到这里，就说明JDK环境变量已经配置好了，后面使用JDK命令可以在任意目录下运行。

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D4b49deae9h69ab74731987cec086e322%26expires%3D24h%26dp_logid%3D443618247035549586%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-IPSvcXWUEjXOEajq9LjZ8%25252B9UVvE%25253D%26file_size%3D33801%26timestamp%3D1745903341%26method%3Dinfo%26fid%3D3170504070-250528-140924858986399%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day01-Java%E5%85%A5%E9%97%A8.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday01-Java%E5%85%A5%E9%97%A8%2Fday01-Java%E5%85%A5%E9%97%A8.md&fs_id=140924858986399&size=33801&uk=3170504070&from=yuanguanjia&fsid=140924858986399&clienttype=8&scence=mac_main#%E4%B8%89-java%E5%BC%80%E5%8F%91%E5%B7%A5%E5%85%B7)三、Java开发工具

大家刚才写代码的时候都是用记事本写的，但是有没有觉得记事本写代码不太方便啊！记事本写代码单词写错了没有提示，格式也不好调整，写代码之后还需要我们到命令行使用javac命令手动编译，然后运行。

有没有一种软件能够将写代码、编译、运行等工具集成到一起呢？ 有，这就是集成开发环境（Integrated Development Environment ，简称IDE）。除此之外，IDEA还有代码提示、检查代码错误等功能，从而提高程序员的开发效率。

IDE有很多种，常见的Eclipse、MyEclipse、Intellij IDEA、JBuilder、NetBeans等。但是这些IDE中目前比较火的是Intellij IDEA（以下简称IDEA），被众多Java程序员视为最好用的Java集成开发环境，所以我们课程中就以IDEA为开发工具来编写代码，以后大家去公司也建议用IDEA作为开发环境。

![1660150643893](https://pan.baidu.com/wap/assets/1660150643893.png)

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D4b49deae9h69ab74731987cec086e322%26expires%3D24h%26dp_logid%3D443618247035549586%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-IPSvcXWUEjXOEajq9LjZ8%25252B9UVvE%25253D%26file_size%3D33801%26timestamp%3D1745903341%26method%3Dinfo%26fid%3D3170504070-250528-140924858986399%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day01-Java%E5%85%A5%E9%97%A8.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday01-Java%E5%85%A5%E9%97%A8%2Fday01-Java%E5%85%A5%E9%97%A8.md&fs_id=140924858986399&size=33801&uk=3170504070&from=yuanguanjia&fsid=140924858986399&clienttype=8&scence=mac_main#31-idea%E4%B8%8B%E8%BD%BD%E5%92%8C%E5%AE%89%E8%A3%85)3.1 IDEA下载和安装

为了引导大家正确的完成IDEA的下载和安装，给小伙伴们单独提供了一个文档《IDEA安装、使用、配置.pdf》，文档中提供了IDEA详细的安装和使用步骤，大家只需要按照文档的步骤一步一步操作就行。

![1660541810799](https://pan.baidu.com/wap/assets/1660541810799.png)

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D4b49deae9h69ab74731987cec086e322%26expires%3D24h%26dp_logid%3D443618247035549586%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-IPSvcXWUEjXOEajq9LjZ8%25252B9UVvE%25253D%26file_size%3D33801%26timestamp%3D1745903341%26method%3Dinfo%26fid%3D3170504070-250528-140924858986399%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day01-Java%E5%85%A5%E9%97%A8.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday01-Java%E5%85%A5%E9%97%A8%2Fday01-Java%E5%85%A5%E9%97%A8.md&fs_id=140924858986399&size=33801&uk=3170504070&from=yuanguanjia&fsid=140924858986399&clienttype=8&scence=mac_main#32-idea%E7%BC%96%E5%86%99java%E7%A8%8B%E5%BA%8F)3.2 IDEA编写Java程序

上一节我们安装好了IDEA之后，接下来我们就可以使用IDEA开发一个HelloWorld程序玩一玩！目的是让大家知道在IDEA中开发Java程序的步骤。

想要在IDEA正确的写一个Java程序，必须先认识一下IDEA的管理Java程序的工程结构。

- 第一步：首先得在IDEA中创建一个Project（工程、也叫项目），后面统称为工程。
- 第二步：需要在Project中创建Module（模块），一个工程中可以包含多个模块
- 第三步：需要在Module中新建Package（包），一个模块中可以有多个包
- 第四步：需要在Package中新建Class（类），一个包中可以包含多个类

软件工程其实类似于建筑工程，我们对比建筑工程来理解。

- Project（工程）：你可以理解成小区的院子
- Module（模块）：你可以理解成小区院子里面的每一栋楼
- Package（包）：你可以理解成每一栋楼的一层
- Class（类）：你可以理解成每一层的住户

![1660542739892](https://pan.baidu.com/wap/assets/1660542739892.png)

在实际开发中比如淘宝网站这样的工程，但是由于功能很多，所以就把淘宝网站分为不同的模块，首页是一个模块、购物车是一个模块、订单也是一个模块；

![1660543086870](https://pan.baidu.com/wap/assets/1660543086870.png)

![1660544338418](https://pan.baidu.com/wap/assets/1660544338418.png)

- **创建工程Project**
    
    创建工程的步骤比较多，在《IDEA安装、使用、配置.pdf》中提供的详细的引导步骤，照着一步一步的操作就行。
    
    用浏览器打开《IDEA安装、使用、配置.pdf》点击左侧的导航栏可以定位到对应的位置，每一个部分都有截图步骤
    
    ![1660544715195](https://pan.baidu.com/wap/assets/1660544715195.png)
    

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D4b49deae9h69ab74731987cec086e322%26expires%3D24h%26dp_logid%3D443618247035549586%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-IPSvcXWUEjXOEajq9LjZ8%25252B9UVvE%25253D%26file_size%3D33801%26timestamp%3D1745903341%26method%3Dinfo%26fid%3D3170504070-250528-140924858986399%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day01-Java%E5%85%A5%E9%97%A8.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday01-Java%E5%85%A5%E9%97%A8%2Fday01-Java%E5%85%A5%E9%97%A8.md&fs_id=140924858986399&size=33801&uk=3170504070&from=yuanguanjia&fsid=140924858986399&clienttype=8&scence=mac_main#34-idea%E5%90%84%E7%A7%8D%E9%85%8D%E7%BD%AE)3.4 IDEA各种配置

刚才有同学在使用IDEA编写程序时，可能会觉得字体比较小，背景色是黑色的，注释是灰色的，看不清，长时间可能对眼睛不好。我们可以通过IDEA相关的设置，把字体调大一点，背景色调为护眼色，注释也调为绿色。

- **主题配置**

![1660150404720](https://pan.baidu.com/wap/assets/1660150404720.png)

- **字体配置**

![1660150433205](https://pan.baidu.com/wap/assets/1660150433205.png)

- **背景色配置**

把背景色的颜色值，调为204、238、200；就是豆沙绿的护眼色了

![1660545292279](https://pan.baidu.com/wap/assets/1660545292279.png)

更多配置，大家可以参考《IDEA安装、使用、配置.pdf》

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D4b49deae9h69ab74731987cec086e322%26expires%3D24h%26dp_logid%3D443618247035549586%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-IPSvcXWUEjXOEajq9LjZ8%25252B9UVvE%25253D%26file_size%3D33801%26timestamp%3D1745903341%26method%3Dinfo%26fid%3D3170504070-250528-140924858986399%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day01-Java%E5%85%A5%E9%97%A8.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday01-Java%E5%85%A5%E9%97%A8%2Fday01-Java%E5%85%A5%E9%97%A8.md&fs_id=140924858986399&size=33801&uk=3170504070&from=yuanguanjia&fsid=140924858986399&clienttype=8&scence=mac_main#35-%E5%B8%B8%E7%94%A8%E5%BF%AB%E6%8D%B7%E9%94%AE)3.5 常用快捷键

讲完IDEA相关配置之后，接下来给大家讲一个很重要的IDEA的使用技巧，这就是IDEA的快捷键，所谓快捷键就是通过键盘上的按键组合起来，就可以帮我们生成代码。使用快捷键可以大大提高我们的开发效率。

下面是几种常见的快捷键，以及他们的作用，大家可以自己试试

|**快捷键**|**功能效果**|
|---|---|
|main/psvm、sout、…|快速键入相关代码|
|Ctrl + D|复制当前行数据到下一行|
|Ctrl + Y|删除所在行，建议用Ctrl + X|
|Ctrl + ALT + L|格式化代码|
|ALT + SHIFT + ↑ , ALT + SHIFT + ↓|上下移动当前代码|
|Ctrl + / , Ctrl + Shift + /|对代码进行注释(讲注释的时候再说)|

快捷键其实有很多，这里列举的是现阶段我们用得比较多的，现在记住不也不要紧，以后经常用，用着用着就记住了。

在后面的课程中讲到一些新的知识点时，还有会继续给大家讲一些新的快捷键。

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D4b49deae9h69ab74731987cec086e322%26expires%3D24h%26dp_logid%3D443618247035549586%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-IPSvcXWUEjXOEajq9LjZ8%25252B9UVvE%25253D%26file_size%3D33801%26timestamp%3D1745903341%26method%3Dinfo%26fid%3D3170504070-250528-140924858986399%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day01-Java%E5%85%A5%E9%97%A8.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday01-Java%E5%85%A5%E9%97%A8%2Fday01-Java%E5%85%A5%E9%97%A8.md&fs_id=140924858986399&size=33801&uk=3170504070&from=yuanguanjia&fsid=140924858986399&clienttype=8&scence=mac_main#%E5%9B%9B-java%E5%9F%BA%E7%A1%80%E8%AF%AD%E6%B3%95)四. Java基础语法

前面讲到的所有内容，都是为Java程序开发做一些准备工作，我们还没有正式教大家如何编写代码。

想要编写Java代码，就必须学习Java的语法，学习语法最主要做到下面两点就可以了

- 记住语法格式
- 明确这种语法格式能达到什么效果

这里需要给大家说明一点：语法格式是Java语言的设计者规定好的，我们不用关心它为什么这么写，因为它造出来就是这么写的。

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D4b49deae9h69ab74731987cec086e322%26expires%3D24h%26dp_logid%3D443618247035549586%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-IPSvcXWUEjXOEajq9LjZ8%25252B9UVvE%25253D%26file_size%3D33801%26timestamp%3D1745903341%26method%3Dinfo%26fid%3D3170504070-250528-140924858986399%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day01-Java%E5%85%A5%E9%97%A8.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday01-Java%E5%85%A5%E9%97%A8%2Fday01-Java%E5%85%A5%E9%97%A8.md&fs_id=140924858986399&size=33801&uk=3170504070&from=yuanguanjia&fsid=140924858986399&clienttype=8&scence=mac_main#41-%E6%B3%A8%E9%87%8A)4.1 注释

我们先从最简单的语法开始学习，先来学习注释！

- 什么是注释？
    
    注释是解释说明程序的问题，方便自己和别人阅读代码
    
- 注释有哪几种？格式怎样？
    
    ```
    1.单行注释：
    	//后面根解释文字
    2.多行注释
        /*
        这里写注释文字
        可以写多行
        */
    3.文档注释
        /**
        这里写文档注释
        也可以写多行，文档注释可以利用JDK的工具生成帮助文档
        */
    ```
    
- 下面用注释解释一段代码
    
    ```
    /**
    目标：学会使用注释
         这是程序的讲解注释
    */
    public class NoteDemo{
        //这是程序的主方法，是程序的入口
        public static void main(String[] args){
            System.out.println("我开始学习Java程序，好嗨皮~~");
            /*
            窗前明月光
            疑是地上霜
            举头望明月
            低头思故乡
            */
            System.out.println("播仔");
            System.out.println("deli");
        }
    }
    ```
    

再多学一招：每次手动加注释比较麻烦，也可以使用快捷键加注释

```
Ctrl + / 	单行注释（对当前行进行注释）
Ctrl + Shift + / 	对选中的代码进行多行注释。
```

![1660546999747](https://pan.baidu.com/wap/assets/1660546999747.png)

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D4b49deae9h69ab74731987cec086e322%26expires%3D24h%26dp_logid%3D443618247035549586%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-IPSvcXWUEjXOEajq9LjZ8%25252B9UVvE%25253D%26file_size%3D33801%26timestamp%3D1745903341%26method%3Dinfo%26fid%3D3170504070-250528-140924858986399%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day01-Java%E5%85%A5%E9%97%A8.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday01-Java%E5%85%A5%E9%97%A8%2Fday01-Java%E5%85%A5%E9%97%A8.md&fs_id=140924858986399&size=33801&uk=3170504070&from=yuanguanjia&fsid=140924858986399&clienttype=8&scence=mac_main#42-%E5%AD%97%E9%9D%A2%E9%87%8F)4.2 字面量

学习完注释之后，我们来学习一个全新的知识点叫字面量。

- 什么是字面量？
    
    大家不要被这个词搞晕了，它其实很简单，我们知道计算机是来处理数据的，字面量其实就是告诉程序员数据在程序中的书写格式。下面是常用的数据在程序中的书写格式
    

![1660150925625](https://pan.baidu.com/wap/assets/1660150925625.png)

- 编写程序，在命令行打印输出各种类型的字面值

```
/*
目标：需要同学们掌握常见数据在程序中的书写格式
*/
public class LiteralDemo{
    public static void main(String[] args){
        //1.整数
        System.out.println(666);
        
        //2.小数
        System.out.println(3.66);
        
        //3.字符: 字符必须用单引号引起来
        System.out.println('a');
        System.out.println('0');
        System.out.println('中');
        System.out.println(' '); //空格也算字符
        //特殊字符：\t表示制表符 \n表示换行
        System.out.println('\t'); //这相当于一个tab键，专业叫做制表符
        System.out.println('\n'); //这是换行的意思
        
        //4.字符串：字符串是双引号引起来的
        System.out.println("我爱你中国abc");
        
        //5.布尔值：只有两个值true和false
        System.out.println(true);
        System.out.println(false);
    }
}
```

总结一下：对于字面量，大家只要能够正确写出各种数据就可以了

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D4b49deae9h69ab74731987cec086e322%26expires%3D24h%26dp_logid%3D443618247035549586%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-IPSvcXWUEjXOEajq9LjZ8%25252B9UVvE%25253D%26file_size%3D33801%26timestamp%3D1745903341%26method%3Dinfo%26fid%3D3170504070-250528-140924858986399%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day01-Java%E5%85%A5%E9%97%A8.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday01-Java%E5%85%A5%E9%97%A8%2Fday01-Java%E5%85%A5%E9%97%A8.md&fs_id=140924858986399&size=33801&uk=3170504070&from=yuanguanjia&fsid=140924858986399&clienttype=8&scence=mac_main#43-%E5%8F%98%E9%87%8F)4.3 变量

学习完字面量之后，接下来我们再来学习变量。对于变量的学习路径如下所示

1. 先认识什么是变量？
    
2. 学习为什么要用变量？
    
3. 学习变量有啥应用场景？
    

![1660548540262](https://pan.baidu.com/wap/assets/1660548540262.png)

- **什么是变量？**

变量是用来记录程序中的数据的。其本质上是内存中的一块区域，你可以把这块区域理解成一个小盒子。

![1660548847936](https://pan.baidu.com/wap/assets/1660548847936.png)

我们通过先通过一段代码演示一下，并解释变量的含义

![1660151428759](https://pan.baidu.com/wap/assets/1660151428759.png)

```
int age = 18;
System.out.println(a);
```

当执行`int age = 18;` 这句代码时，JVM会在内存中申请一块区域，在这个区域中存储了一个整数18，给这个区域取的名字叫age； 相当于在盒子中存了一个数据18，这个盒子的名字是age，当我们打印age时，就是从盒子中把盒子中的数据取出来再打印。

- **为什么要用变量呢？**

使用变量来记录数据，对于数据的管理更为灵活。比如我们有多个地方用到一个整数10,

```
//1.假设4多个地方用到整数10; 现在我想把10改为20，这时你得一条语句一条语句的修改
System.out.println(10);
System.out.println(10);
System.out.println(10);
System.out.println(10);

//2.同样这里还是在多个地方用到整数10，你可以先用一个变量记录这个整数10
int x = 10;
//然后在需要用到整数10的地方，用x代替就行；
//如果我们把x值改了，那么后面用到x的值的地方就都一起改变了
System.out.println(x);
System.out.println(x);
System.out.println(x);
System.out.println(x);
```

- **变量有应用场景?**

变量的应用场景无处不在，只要是程序中能发生变化的数据，都可以用变量存储。比如：你微信钱包中的余额，你微信的昵称，你微信的个性签名； 余额随着你花钱是不是在变少，昵称和个性签名也可以经常修改。

```
//比如：你现在有188.8元，一会要发100元，再收20元。
double money = 188.8;
//发100元
money = money - 100;
//再收20元
money = money + 20;
//再打印money记录的值是多少
System.out.println(money);


//再比如：公交车大人2元，小孩一元，公交车经过2站
//第一站：3个大人1个小孩上车
//第二站：1个大人1个小孩上车，请问一共上了多少人，一共收入多少钱？
//刚开始公交车箱子里没有钱，用money2表示箱子里的钱
int money2 = 0;
//刚开始公交车上也没有人，用count变量表示上车的人数
int count = 0;

//经过两站的人数：第一站3人，第二站1人，总的人数是3+1
count = 3+1;
//经过两站的钱数：
money2 = money2+3*2+1; //经过第一站后
money2 = money2+2+1; //经过第二站后

//打印人数和钱数
System.out.println(count);
System.out.println(money);
```

- **变量的注意事项**

在上节课已经给大家讲了变量的基本使用，变量在实际开发中用得特别多，关于变量使用注意事项需要给大家交代一下。

讲这些注意事项目的是让大家知道，有哪些写法是允许，有哪些写法是不允许的，能分辨对错，并知道为什么错。

```
1.变量定义在哪个{}范围内，就只在哪个大括号内有效。变量的有效范围称之为变量的作用域
	{
		int a = 10;
		System.out.println(a); //这是是对的
	}
	System.out.println(a); //这里会出错

2.在同一个作用域内，不能有两个同名的变量
	{
		int a = 10;
		int a = 20; //这里会出错
	}
	
3.变量没有初始化只，不能直接使用
	int a; //仅仅定义了变量，但是没有初始值
	System.out.println(a); //这里会出错

4.变量可以定义在同一行
	如：int a=10, b=20; //a和b都是int类型
```

到此有关变量的所有使用方式，以及变量需要注意的问题，就学习完了。

我们再总结一下几点

- 变量是用来记录程序中的数据的，可以把变量理解成内存中的小盒子，盒子里放的东西就是变量记录的数据
- 变量的定义格式： `数据类型 变量名 = 初始值;`
- 变量记录的数据程序运行过程中是可以发生改变的：`变量名 = 值;`

---

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D4b49deae9h69ab74731987cec086e322%26expires%3D24h%26dp_logid%3D443618247035549586%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-IPSvcXWUEjXOEajq9LjZ8%25252B9UVvE%25253D%26file_size%3D33801%26timestamp%3D1745903341%26method%3Dinfo%26fid%3D3170504070-250528-140924858986399%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day01-Java%E5%85%A5%E9%97%A8.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday01-Java%E5%85%A5%E9%97%A8%2Fday01-Java%E5%85%A5%E9%97%A8.md&fs_id=140924858986399&size=33801&uk=3170504070&from=yuanguanjia&fsid=140924858986399&clienttype=8&scence=mac_main#44-%E5%85%B3%E9%94%AE%E5%AD%97)4.4 关键字

学完变量之后，我们再来认识一下Java的关键字。

- **什么是关键字？**
    
    关键字是java语言中有特殊含义的单词。比如用int表示整数，用double表示小数，等等！
    
- **关键字有哪些？**
    
    我们学习Java的语法其本质就是学习这些关键字的含义，一共有50多个关键字，我们不是一次性把这些关键字学完，会在后续的课程中每天学一点，慢慢得你就都学会了。
    

|**abstract**|**assert**|**boolean**|**break**|**byte**|
|---|---|---|---|---|
|**case**|**catch**|**char**|**class**|**const**|
|**continue**|**default**|**do**|**double**|**else**|
|**enum**|**extends**|**final**|**finally**|**float**|
|**for**|**goto**|**if**|**implements**|**import**|
|**instanceof**|**int**|**interface**|**long**|**native**|
|**new**|**package**|**private**|**protected**|**public**|
|**return**|**strictfp**|**short**|**static**|**super**|
|**switch**|**synchronized**|**this**|**throw**|**throws**|
|**transient**|**try**|**void**|**volatile**|**while**|

- **如何识别那些单词是关键字？**

现在我们不用知道这些关键字是什么意思，主要能够根据特点识别那些是关键字就可以了

```
关键字的特点：
	1.关键字都是小写的
	2.关键字在idea中有特殊颜色标记（如果你没有修改关键字的颜色，默认是蓝色的）
```

下图中红色框住的单词都是关键字；没有框住的单词都不是关键字

![1660553031642](https://pan.baidu.com/wap/assets/1660553031642.png)

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D4b49deae9h69ab74731987cec086e322%26expires%3D24h%26dp_logid%3D443618247035549586%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-IPSvcXWUEjXOEajq9LjZ8%25252B9UVvE%25253D%26file_size%3D33801%26timestamp%3D1745903341%26method%3Dinfo%26fid%3D3170504070-250528-140924858986399%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day01-Java%E5%85%A5%E9%97%A8.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday01-Java%E5%85%A5%E9%97%A8%2Fday01-Java%E5%85%A5%E9%97%A8.md&fs_id=140924858986399&size=33801&uk=3170504070&from=yuanguanjia&fsid=140924858986399&clienttype=8&scence=mac_main#45-%E6%A0%87%E5%BF%97%E7%AC%A6)4.5 标志符

接下来我们学习一下标志符，所谓标志符其实就是我们自己取的名字。像前面我们取的类名，变量名其实都是标志符。

讲标志符的目的，是让大家知道取名字的规则，不能让我们随即便瞎取。有些规则是强制要求的，不遵守就会报错。还有一些规则是我们建议大家遵守的，这样取名字显得我们更加专业_。

```
强制要求：必须遵守，不遵守就会报错
	1.最好是字母、数字、下划线、$组成
	2.不能以数字开头
	3.不能是Java的关键字

建议遵守：按照下面的方式取名字会显得更加专业
	1.所有的名字要见名知意，便于自己和别人阅读
		举例： class Student{} //一看这个类就知道表示一个学生
			  int age =10;    //一看这个变量就知道表示年龄
		
	2.类名：首字母大写（大驼峰命名）
		举例： class Student{}
		
	3.变量名：第二个单词开始首字母大写（小驼峰命名）
		举例： double money = 6.88;  
			  double applePrice = 7.5; 
```

# Day2

## 一、数据的表示详解

昨天我们学习了变量，我们知道变量可以用来记录数据的。那么数据在计算机底层是以什么形式表示的呢？下面我们就学习一下数据在计算机中的底层原理。

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Dfa86f1806r44517a46efa163217324a7%26expires%3D24h%26dp_logid%3D443647534724268254%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-Np%25252BgDBHQpOsjzvTdzZND%25252FPZynko%25253D%26file_size%3D32991%26timestamp%3D1745903450%26method%3Dinfo%26fid%3D3170504070-250528-760086089839307%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day02-%E7%B1%BB%E5%9E%8B%E8%BD%AC%E6%8D%A2%E3%80%81%E8%BF%90%E7%AE%97%E7%AC%A6.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday02-Java%E7%B1%BB%E5%9E%8B%E8%BD%AC%E6%8D%A2%E3%80%81%E8%BF%90%E7%AE%97%E7%AC%A6%2Fday02-%E7%B1%BB%E5%9E%8B%E8%BD%AC%E6%8D%A2%E3%80%81%E8%BF%90%E7%AE%97%E7%AC%A6.md&fs_id=760086089839307&size=32991&uk=3170504070&from=yuanguanjia&fsid=760086089839307&clienttype=8&scence=mac_main#11-%E6%95%B4%E6%95%B0%E5%9C%A8%E8%AE%A1%E7%AE%97%E6%9C%BA%E4%B8%AD%E7%9A%84%E5%AD%98%E5%82%A8%E5%8E%9F%E7%90%86)1.1 整数在计算机中的存储原理

其实任何数据在计算机中都是以**二进制**表示的。那这里肯定有人问，什么是二进制啊？所谓二进制其实就是一种数据的表示形式，它的特点是逢2进1。

数据的表示形式除了二进制（逢2进1），八进制（逢8进1）、还有十进制（逢10进1）、十六进制（逢10进1）等。

对于二进制绝大多数同学，应该是非常陌生的。 没关系！来，大家跟着我的思路，你就知道二进制是怎么表示数据的了。

```
1.二进制中只有0和1两个数
	首先十进制的0和二进制的0是一样的，十进制的1和二进制的1也是 一样的。但是十进制中	  有2，但是二进制中就没有2了

2.那么二进制是如何表示十进制的2呢？
	1
+	1		
——————————	
   10	  这里两个1相加，结果为2，由于二进制满2进1，所以最终结果10
   
3.那么二进制是如何表示十进制的3呢？
	前面我们已经知道二进制10表示十进制的2，那么二进制10+1就表示十进制的3啊！
	10
+    1
—————————
    11	 十进制的3对应的二进制是11

4.那么二进制是如何表示十进制4的呢？
	前面我们已经知道二进制11表示十进制的4，那么11+1就表示十进制的5啊
	11
+    1
—————————
   100   十进制的5对应的二进制是100

你找到规律了吗？ 你能不能依次写出5的二进制、6的二进制？
```

前面每算一个二进制数据都是采用+1的方式，逢2进1，一个一个算出来的。有没有更快的算出十进制对应二进制的方法呢？ 这里学习一种方式：叫做除2取余法。

- **除2取余法**

```
1.怎么做呢？
	答：让十进制数据连续除以2，直到商为0，余数反转

2.举例1：把十进制6转换为二进制	
			商	余数
	6/2     3    0
    3/2		1	 1
    1/2		0	 1
    然后把余数反转：6对应的二进制是110
    
3.举例2： 把十进制13转换为二进制
			商	余数
	13/2	6	 1
    6/2		3	 0
    3/2	 	1 	 1
    1/2		0	 1
    然后把余数反转：10对应的二进制是1101
    
4.练习1：你能把十进制7转换为二进制吗？
	自己试试吧！

```

关于变量记录的数据在计算机中如何表示我们就先学习到这里。

- **计算机的最小存储单位**

前面我们已经知道计算机表示数据是用二进制来的， 这里我又要抛出一个问题来了！ 我现在想要在计算机中存储一个整数6，转换为二进制是110，那么计算机中只是存110吗三位数字吗？ 其实不是的，**计算机中最小的存储单位是字节（Byte），一个字节占8位（bit）**，也就是说即使这个数据不足8位也需要用8位来存储。

![1660754639238](https://pan.baidu.com/wap/assets/1660754639238.png)

我们随便找到一个文件，看文件的属性，可以看到文件的大小都是以字节为单位的。

![1660754762466](https://pan.baidu.com/wap/assets/1660754762466.png)

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Dfa86f1806r44517a46efa163217324a7%26expires%3D24h%26dp_logid%3D443647534724268254%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-Np%25252BgDBHQpOsjzvTdzZND%25252FPZynko%25253D%26file_size%3D32991%26timestamp%3D1745903450%26method%3Dinfo%26fid%3D3170504070-250528-760086089839307%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day02-%E7%B1%BB%E5%9E%8B%E8%BD%AC%E6%8D%A2%E3%80%81%E8%BF%90%E7%AE%97%E7%AC%A6.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday02-Java%E7%B1%BB%E5%9E%8B%E8%BD%AC%E6%8D%A2%E3%80%81%E8%BF%90%E7%AE%97%E7%AC%A6%2Fday02-%E7%B1%BB%E5%9E%8B%E8%BD%AC%E6%8D%A2%E3%80%81%E8%BF%90%E7%AE%97%E7%AC%A6.md&fs_id=760086089839307&size=32991&uk=3170504070&from=yuanguanjia&fsid=760086089839307&clienttype=8&scence=mac_main#12-%E5%AD%97%E7%AC%A6%E5%9C%A8%E8%AE%A1%E7%AE%97%E6%9C%BA%E4%B8%AD%E7%9A%84%E5%AD%98%E5%82%A8%E5%8E%9F%E7%90%86)1.2 字符在计算机中的存储原理

通过上一节的学习，我们知道了整数是如何在计算机中如何存储的？那么字符在计算机中是如何存储的呢？

其实字符并不是直接存储的，而是把每一个字符编为一个整数，存储的是字符对应整数的二进制形式。美国人搞了一套字符和整数的对应关系表，叫做ASCII编码表。

```
ASCII编码表中字符编码的规律：
	1.字符0对应48，后面的1,2,3,4...9 对应的十进制整数依次往后顺延
	2.字符a对应97，后面的b,c,d,e...z 对应的十进制整数依次往后顺延
	3.字符A对应65，后面的B,C,D,E...Z 对应的十进制整数依次往后顺延
```

![1660755324089](https://pan.baidu.com/wap/assets/1660755324089.png)

需要注意的是，在ASCII编码表中是不包含汉字的。汉字在其他编码表中，后面我们会单独介绍。关于字符在计算机中的存储学到这就可以了。

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Dfa86f1806r44517a46efa163217324a7%26expires%3D24h%26dp_logid%3D443647534724268254%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-Np%25252BgDBHQpOsjzvTdzZND%25252FPZynko%25253D%26file_size%3D32991%26timestamp%3D1745903450%26method%3Dinfo%26fid%3D3170504070-250528-760086089839307%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day02-%E7%B1%BB%E5%9E%8B%E8%BD%AC%E6%8D%A2%E3%80%81%E8%BF%90%E7%AE%97%E7%AC%A6.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday02-Java%E7%B1%BB%E5%9E%8B%E8%BD%AC%E6%8D%A2%E3%80%81%E8%BF%90%E7%AE%97%E7%AC%A6%2Fday02-%E7%B1%BB%E5%9E%8B%E8%BD%AC%E6%8D%A2%E3%80%81%E8%BF%90%E7%AE%97%E7%AC%A6.md&fs_id=760086089839307&size=32991&uk=3170504070&from=yuanguanjia&fsid=760086089839307&clienttype=8&scence=mac_main#13-%E5%9B%BE%E7%89%87%E8%A7%86%E9%A2%91%E5%A3%B0%E9%9F%B3%E7%9A%84%E5%AD%98%E5%82%A8%E5%8E%9F%E7%90%86)1.3 图片视频声音的存储原理

- **图片的存储**

通过上面的学习我们已经知道整数和字符是如何存储的，最终都是要转换为二进制数据的，对吧！ 那图片、声音、视频又是如何存储的呢？我们也来了解一下

我们从图片开始，如果你把一张图片不断的放大，你会看到有马赛克的效果。你会发现图片中的每一个细节是由一个一个的小方格组成的，每一个小方格中其实就是一种颜色。任何一种颜色可以使用三原色来表示，简称RGB，其中R（红色），G（绿色），B（蓝色），而RGB中每一种颜色又用一个字节的整数来表示，最小值是0最大值是255

![1660755882309](https://pan.baidu.com/wap/assets/1660755882309.png)

```
RGB（0,0,0）表示黑色
RGB（255,255,255）表示白色
RGB（255,0,0） 表示红色
RGB（255,255,0） 表示红色和绿色混合为黄色
RGB（255,0,255） 表示红色和蓝色混合为紫色
...
```

你在画图板的颜色编辑器中可以通过指定RGB的值，来调整得到任意的颜色。一张图片实际上就是有很多个小方块的颜色组成的，而每一种颜色又是由RGB三原色的整数表示的，整数最终会转换为二进制进行存储。

![1660756387308](https://pan.baidu.com/wap/assets/1660756387308.png)

- **视频的存储**

实际上视频和图片是一样的，把多张图片连续播放，在一秒钟内连续播放24张以上，由于人眼存在视觉暂留现象，人眼感受不到画面切换的时间间隔，就认为是连续的视频了。

- **声音的存储**

了解过物理的同学肯定知道，声音是以波的形式传播的。我们可以把声波在表示在一个坐标系上，然后在坐标系上取一些点，把这些点的坐标值以二进制的形式存储到计算机中，这就是声音的存储原理。

![1660757825804](https://pan.baidu.com/wap/assets/1660757825804.png)

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Dfa86f1806r44517a46efa163217324a7%26expires%3D24h%26dp_logid%3D443647534724268254%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-Np%25252BgDBHQpOsjzvTdzZND%25252FPZynko%25253D%26file_size%3D32991%26timestamp%3D1745903450%26method%3Dinfo%26fid%3D3170504070-250528-760086089839307%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day02-%E7%B1%BB%E5%9E%8B%E8%BD%AC%E6%8D%A2%E3%80%81%E8%BF%90%E7%AE%97%E7%AC%A6.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday02-Java%E7%B1%BB%E5%9E%8B%E8%BD%AC%E6%8D%A2%E3%80%81%E8%BF%90%E7%AE%97%E7%AC%A6%2Fday02-%E7%B1%BB%E5%9E%8B%E8%BD%AC%E6%8D%A2%E3%80%81%E8%BF%90%E7%AE%97%E7%AC%A6.md&fs_id=760086089839307&size=32991&uk=3170504070&from=yuanguanjia&fsid=760086089839307&clienttype=8&scence=mac_main#14-%E6%95%B0%E6%8D%AE%E7%9A%84%E5%85%B6%E4%BB%96%E8%A1%A8%E7%A4%BA%E5%BD%A2%E5%BC%8F)1.4 数据的其他表示形式

- **二进制到十进制的转换**

前面我们学习了十进制可以转二进制，采用的是除2取余法，那么我们反过来能不能把二进制转换为十进制呢？

这里给大家介绍一种计算方式叫做：**8421码**

为了便于理解，我们先在看一下十进制怎么转十进制，主要是为了让大家看到演化过程。

```
1.十进制转十进制
	比如我们把12345进行分解：
        12345 = 10000 + 2000 + 300 + 40 + 5
              = 1*10^4 + 2*10^3 + 3*10^2 + 5*10^0
	我们发现：
		在十进制中如果把十进制的每一位从右往左从0开始编一个号，假设这一位数字是a,			那么这一位数表示的值就是：a*10^n；
	
----------------------------------------------------------------------二2.二进制转十进制：
	类比十进制：
		如果把二进制的每一位从从右往左0开始编一个号用n表示，假设二进制的每一位是a，
		那么这一位表示的十进制值是：a*2^n
		
	1)假设二进制的每一位都是1：
		128	64	32	16	8	4	2	1	每一位表示的十进制：a*2^n
		7	6	5	4	3	2	1	0	编号：n
		1	1	1	1	1	1	1	1   二进制的每一位：a
	
        二进制		 十进制
        11111111 = 1*2^7  + 1*2^6 + 1*2^5 + ... + 1*2^0
                 = 128    + 64    + 32    + ... + 1
                 = 255
    
    2)假设二进制的为0010001
    	128	64	32	16	8	4	2	1	每一位表示的十进制：a*2^n
    	7	6	5	4	3	2	1	0	编号：n
    	0	0	1	0	0	0	0	1	二进制的每一位：a
    
    	二进制				十进制
    	00001101 = 0
```


# day03——程序流程控制

各位同学，今天我们学习一个全新的知识——程序流程控制。什么是流程控制呢？说白了就是控制程序的执行顺序。

先给同学们介绍一下，程序有哪些流程控制、以及Java提供了哪些方案来控制程序的执行顺序？

程序的流程控制一般分为3种：**顺序结构、分支结构、循环结构**

- 顺序结构：就是不加任何控制，代码从main方法开始自上而下执行
    
- 分支结构：就是根据条件判断是true还是false，有选择性的执行哪些代码。在Java语言中提供了两个格式if 、 switch
    
- 循环结构：就是控制某一段代码重复执行。在Java语言中提供了三种格式，for、while、do-while
    

![1661129154598](https://pan.baidu.com/wap/assets/1661129154598.png)

以上就是我们今天要学习的课程内容

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D90985e6efib4d3c363123b0827200e1a%26expires%3D24h%26dp_logid%3D443657076446953308%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-4trhQVxF0bvM0h0htGAbYawVSnw%25253D%26file_size%3D27749%26timestamp%3D1745903486%26method%3Dinfo%26fid%3D3170504070-250528-52052917322535%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6%2Fday03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6.md&fs_id=52052917322535&size=27749&uk=3170504070&from=yuanguanjia&fsid=52052917322535&clienttype=8&scence=mac_main#%E4%B8%80-%E5%88%86%E6%94%AF%E7%BB%93%E6%9E%84)一、分支结构

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D90985e6efib4d3c363123b0827200e1a%26expires%3D24h%26dp_logid%3D443657076446953308%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-4trhQVxF0bvM0h0htGAbYawVSnw%25253D%26file_size%3D27749%26timestamp%3D1745903486%26method%3Dinfo%26fid%3D3170504070-250528-52052917322535%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6%2Fday03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6.md&fs_id=52052917322535&size=27749&uk=3170504070&from=yuanguanjia&fsid=52052917322535&clienttype=8&scence=mac_main#11-if%E5%88%86%E6%94%AF)1.1 if分支

各位同学，接下来我们学习分支结构的第一种形式——if分支。

if它的作用，是用于对条件进行判断，判断的结果只可能有两个值true或者false，然后根据条件判断的结果来决定执行那段代码。

**1. if分支的应用场景有哪些呢？**

比如，在火车站、地铁站等公共场所，会对过往的旅客测体温。如果体温在37度以内，就属于正常的；如果体温在37读以上，测体温的装置就会报警。

![1661130193692](https://pan.baidu.com/wap/assets/1661130193692.png)

再比如，你在使用微信付钱时，微信内部的程序会先判断你的余额是否足够，如果足够就可以支付成功；如果余额不足，就会提示支付失败。

![1661133550463](https://pan.baidu.com/wap/assets/1661133550463.png)

**2. if分支的格式**

接下来，我们来看一看if分支在Java语言中长什么样子呢？在Java中if分支有三种格式。

![1661131177976](https://pan.baidu.com/wap/assets/1661131177976.png)

接下来我们用一些实际案例给大家演示一下if语句的应用，以及每一种if语句的执行流程。

**3. if 第一种形式**

if 第一种形式的代码格式，和执行流程如下图所示

![1661131910804](https://pan.baidu.com/wap/assets/1661131910804.png)

```
if 第一种形式执行流程如下：
    如果 条件表达式 为true，就执行下面的语句体
    如果 条件表达式 为false,就不执行
```

```
// 需求：测量用户体温，发现体温高于37度就报警。
double t = 36.9;
if(t &gt; 37){
    System.out.println("这个人的温度异常，把他赶紧带走~~");
}
```

**4. if 第二种形式**

if 第二种形式的代码格式，和执行流程如下图所示

![1661132063147](https://pan.baidu.com/wap/assets/1661132063147.png)

```
if 第二种形式执行流程如下：
    如果 条件表达式 为true,就执行下面的语句体1
    如果 条件表达式 为false,就执行else下面的语句体2
```

```
// 需求2：发红包，你的钱包余额是99元，现在要发出90元
// 如果钱够触发发红包的动作，如果钱不够，则提示：余额不足。
double money = 19;
if(money &gt;= 90){
    System.out.println("发红包成功了~");
}else {
    System.out.println("余额不足~~");
}
```

**5. if 第三种形式**

if 第三种形式的代码格式，和执行流程如下图所示

![1661132132708](https://pan.baidu.com/wap/assets/1661132132708.png)

```
if 第三种形式执行流程如下：
    如果 条件表达式1 为true,就执行下面的代码1; 
    如果 条件表达式1 为false，就继续判断条件表达式2;

    如果 条件表达式2 为true，就执行下面的语句体;
    如果 条件表达式2 为false，就继续判断条件语句体3;

    如果 条件表达式3 为true,就执行下面的语句体3
    如果 条件表达式3 为false,就继续判断后面的表达式;

    ....
    如果前面所有条件表达式判断都为false，就执行最后的else语句中的代码
```

```
// 需求3：某个公司有一个绩效系统，根据员工的打分输出对应的绩效级别。[0,60) D  [60,80) C [80,90) B [90,100] A
int score = 298;
if(score &gt;= 0 && score &lt; 60) {
    System.out.println("您的绩效级别是： D");
}else if(score &gt;= 60 && score &lt; 80){
    System.out.println("您的绩效级别是： C");
}else if(score &gt;= 80 && score &lt; 90){
    System.out.println("您的绩效级别是： B");
}else if(score &gt;= 90 && score &lt;= 100){
    System.out.println("您的绩效级别是： A");
}else {
    System.out.println("您录入的分数有毛病~~");
}
```

**6. if 使用的几个常见问题**

同学们在第一次写if 代码时，经常一不小心会出现一些问题。下面把同学们可能出现的问题给大家看一看，以后大家要避免出现这些问题。

- 第1个问题：if的()后面不能写分号`;` 否则if下面的语句与if无关

![1661132888600](https://pan.baidu.com/wap/assets/1661132888600.png)

- 第2个问题：if后面的大括号，如果只有一行代码，大括号可以省略

![1661132851560](https://pan.baidu.com/wap/assets/1661132851560.png)

**7. if 分支小结**

关于if分支结构的几种格式，以及各种格式的执行流程，还有if在什么场景下使用我们就讲完了。下面我们总结一下

- if分支有什么作用？举几个应用场景？

```
- if作用：if分支可以根据条件，选择执行某段程序
- if应用场景
    比如1：测量用户体温，发现体温高于37度就报警
    比如2:发红包，你的钱包余额是99元，现在要发出90元
    比如3:根据员工的绩效打分输出对应的绩效级别
```

- if分支的格式有几种，执行流程是什么样的？

![1661133510341](https://pan.baidu.com/wap/assets/1661133510341.png)

---

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D90985e6efib4d3c363123b0827200e1a%26expires%3D24h%26dp_logid%3D443657076446953308%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-4trhQVxF0bvM0h0htGAbYawVSnw%25253D%26file_size%3D27749%26timestamp%3D1745903486%26method%3Dinfo%26fid%3D3170504070-250528-52052917322535%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6%2Fday03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6.md&fs_id=52052917322535&size=27749&uk=3170504070&from=yuanguanjia&fsid=52052917322535&clienttype=8&scence=mac_main#12-switch%E5%88%86%E6%94%AF)1.2 switch分支

学完if 分支之后，接下来我们来学习分支结构的第二种形式——switch分支。

**1. switch分支的执行流程**

switch 分支的作用，**是通过比较值来决定执行哪条分支代码**。先看一下switch分支的格式和执行流程

![1661134120042](https://pan.baidu.com/wap/assets/1661134120042.png)

下面通过案例来演示一下

```
/*
需求：做个电子备忘录，在控制台分别输出周一到周五的工作安排
    周一：埋头苦干，解决bug              
    周二：	请求大牛程序员帮忙             
    周三：今晚啤酒、龙虾、小烧烤      
    周四：主动帮助新来的女程序解决bug
    周五：今晚吃鸡
    周六：与王婆介绍的小芳相亲
    周日：郁郁寡欢、准备上班。
*/
```

```
String week = "周三";
switch (week){
    case "周一":
        System.out.println("埋头苦干，解决bug");
        break;
    case "周二":
        System.out.println("请求大牛程序员帮忙");
        break;
    case "周三":
        System.out.println("今晚啤酒、龙虾、小烧烤");
        break;
    case "周四":
        System.out.println("主动帮助新来的女程序解决bug");
        break;
    case "周五":
        System.out.println("今晚吃鸡");
        break;
    case "周六":
        System.out.println("与王婆介绍的小芳相亲");
        break;
    case "周日":
        System.out.println("郁郁寡欢、准备上班");
        break;
    default:
        System.out.println("您输入的星期信息不存在~~~");
}
```

**2. if 、switch如何选择**

学习完switch 分支之后，有同学可能会想，已经了有if分支，为什么还有switch分支呢？感觉上面的案例用if分支也能做啊？ 那我们在具体应用场景下如何选择呢？

如果单从功能上来讲，if 分支 的功能是更加强大的，switch分支能做的事情if 分支都能做。但是具体用哪一种分支形式，也是有一些使用原则的

```
- 如果是对一个范围进行判断，建议使用if分支结构
- 如果是与一个一个的值比较的时候，建议使用switch分支结构
```

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D90985e6efib4d3c363123b0827200e1a%26expires%3D24h%26dp_logid%3D443657076446953308%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-4trhQVxF0bvM0h0htGAbYawVSnw%25253D%26file_size%3D27749%26timestamp%3D1745903486%26method%3Dinfo%26fid%3D3170504070-250528-52052917322535%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6%2Fday03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6.md&fs_id=52052917322535&size=27749&uk=3170504070&from=yuanguanjia&fsid=52052917322535&clienttype=8&scence=mac_main#13-switch-%E6%B3%A8%E6%84%8F%E4%BA%8B%E9%A1%B9)1.3 switch 注意事项

各位同学，接下来我们学习swtich的注意事项。同学们掌握这些注意事项之后，就可以避免入坑了，也可以应对一些面试笔试题。

```
- 1.表达式类型只能是byte、short、int、char
	JDK5开始支持枚举，JDK7开始支持String
	不支持double、float、double
    
- 2.case给出的值不允许重复，且只能是字面量，不能是变量。
		
- 3.正常使用switch的时候，不要忘记写break，否则会出现穿透现象。
```

**1. 演示switch语句匹配的数据类型**

各位同学，如果下图所示，可以自己分别用变量a、b放在switch语句中匹配试一试，如果遇到不支持的写法，IDEA会报错的。

![1661135813464](https://pan.baidu.com/wap/assets/1661135813464.png)

**2. 演示case后面的值，只能是字面量不能是变量**

各位同学，也可以自己试试，下图箭头指向的位置只能写字面量，不能写变量

![1661136001680](https://pan.baidu.com/wap/assets/1661136001680.png)

**3. 演示case穿透现象**

当switch语句中没有遇到break，就会直接穿透到下一个case语句执行，直到遇到break为止。

这种语法设计也是有它的用处的，当多个case语句想要执行同一段代码时，可以利用case穿透现象，提高代码复用性。

比如：我们下面程序中，想要让周二、周三、周四，都请大牛程序员来写代码。

![1661136414587](https://pan.baidu.com/wap/assets/1661136414587.png)

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D90985e6efib4d3c363123b0827200e1a%26expires%3D24h%26dp_logid%3D443657076446953308%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-4trhQVxF0bvM0h0htGAbYawVSnw%25253D%26file_size%3D27749%26timestamp%3D1745903486%26method%3Dinfo%26fid%3D3170504070-250528-52052917322535%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6%2Fday03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6.md&fs_id=52052917322535&size=27749&uk=3170504070&from=yuanguanjia&fsid=52052917322535&clienttype=8&scence=mac_main#%E4%BA%8C-%E5%BE%AA%E7%8E%AF%E7%BB%93%E6%9E%84)二、循环结构

各位同学，接下来我们学习循环结构。循环结构可以控制一段代码重复执行。循环结构有for循环、while循环、do-while循环。

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D90985e6efib4d3c363123b0827200e1a%26expires%3D24h%26dp_logid%3D443657076446953308%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-4trhQVxF0bvM0h0htGAbYawVSnw%25253D%26file_size%3D27749%26timestamp%3D1745903486%26method%3Dinfo%26fid%3D3170504070-250528-52052917322535%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6%2Fday03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6.md&fs_id=52052917322535&size=27749&uk=3170504070&from=yuanguanjia&fsid=52052917322535&clienttype=8&scence=mac_main#21-for%E5%BE%AA%E7%8E%AF%E6%A0%BC%E5%BC%8F%E5%92%8C%E6%B5%81%E7%A8%8B)2.1 for循环——格式和流程

这里首先来学习for循环，同学们重点掌握for循环的书写格式，并理解for循环的执行流程。

**1. for循环的格式和流程**

为了让大家更直观的理解for循环的执行流程，我们直接来看具体的案例代码。

比如：我们想要在控制台打印输出3个HelloWorld

```
//需求：打印3行Hello World
for(int i = 0; i &lt; 3; i++) {
    System.out.println("Hello World");
}
```

如下图所示，是按照下面的① ② ③ ④， ② ③ ④… 的顺序来执行的；

当②条件为true时，再依次执行③④代码，然后回到②继续判断

当②条件为false时，就结束循环

![1661137599188](https://pan.baidu.com/wap/assets/1661137599188.png)

具体执行的每一步可以看下面的图解

![1661138616082](https://pan.baidu.com/wap/assets/1661138616082.png)

通过上面的案例演示，最后我们再总结一下for循环的格式

```
//for循环格式：
for (初始化语句; 循环条件; 迭代语句) {
    循环体语句(重复执行的代码);
}

初始化语句：一般是定义一个变量，并给初始值
循环条件：一般是一个关系表达式，结果必须是true或者false
迭代语句：用于对条件进行控制，一般是自增或者自减
循环语句体：需要重复执行的代码
```

**2. for循环有哪些应用场景**

通过上面的学习，我们已经知道了for循环怎么编写，并且也知道了它的执行流程。

那么具体在哪些实际场景下使用呢？**其实只要是重复做的事情，都可以用循环语句来做**

比如：在京东的网页上展示100台手机信息，我们只需要把展示数据的代码写一份，重复执行就可以了。

![1661139301013](https://pan.baidu.com/wap/assets/1661139301013.png)

再比如：再我们教学管理系统中，有很多班级需要展示在页面上，我们没必要每一个班级都写一份展示数据代码，只需要写一份重复执行就可以了。

![1661139453144](https://pan.baidu.com/wap/assets/1661139453144.png)

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D90985e6efib4d3c363123b0827200e1a%26expires%3D24h%26dp_logid%3D443657076446953308%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-4trhQVxF0bvM0h0htGAbYawVSnw%25253D%26file_size%3D27749%26timestamp%3D1745903486%26method%3Dinfo%26fid%3D3170504070-250528-52052917322535%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6%2Fday03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6.md&fs_id=52052917322535&size=27749&uk=3170504070&from=yuanguanjia&fsid=52052917322535&clienttype=8&scence=mac_main#22-for%E5%BE%AA%E7%8E%AF%E6%A1%88%E4%BE%8B1%E6%B1%82%E5%92%8C)2.2 for循环案例1——求和

学完for循环的格式和流程之后，我们再通过案例来巩固一下。通过这个案例，主要是让同学们掌握一种使用程序来求和的思想。

```
//1.掌握使用for循环批量产生数据。
for (int i = 1; i &lt;= 100; i++) {
    System.out.println(i);
}
```

```
求和的思路分析：
	1)首先需要定义一个求和变量，一般命名为sum
	2)再遍历得到所有需要求和的数据(1~100之间的所有整数)
	3)让需要求和的数据和sum累加，
	结果：所有数据累加完之后最终sum就是所有数据的和
```

```
//2.需求：求1~100中所有整数的和
int sum = 0;
//定义一个循环，先产生1-100，这100个数
for (int i = 1; i &lt;= 100; i++) {
    //每产生一个数据，就把这个数和sum累加
    sum += i; //sum = sum  + i;
}
System.out.println("1-100的数据和：" +  sum);
```

分析上面代码的执行过程：

```
i=1时：sum=0+1; sum=1;
i=2时：sum=1+2; sum=3;
i=3时：sum=3+3; sum=6;
i=4时：sum=6+4; sum=10;
...
i=100时: sum+=99; sum=5050
```

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D90985e6efib4d3c363123b0827200e1a%26expires%3D24h%26dp_logid%3D443657076446953308%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-4trhQVxF0bvM0h0htGAbYawVSnw%25253D%26file_size%3D27749%26timestamp%3D1745903486%26method%3Dinfo%26fid%3D3170504070-250528-52052917322535%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6%2Fday03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6.md&fs_id=52052917322535&size=27749&uk=3170504070&from=yuanguanjia&fsid=52052917322535&clienttype=8&scence=mac_main#22-for%E5%BE%AA%E7%8E%AF%E6%A1%88%E4%BE%8B2%E6%B1%82%E5%A5%87%E6%95%B0%E5%92%8C)2.2 for循环案例2——求奇数和

需求：求1~100之间奇数的和

**1. 代码写法一**

```
求奇数和的思路（只是求和的数据变成了奇数，思路和前面没有变化）
	1)首先需要定义一个求和变量，这里命名为sum1
	2)再遍历得到所有需要求和的数据(1~100之间的所有奇数)
	3)让需要求和的数据和sum1累加，
	结果：所有数据累加完之后最终sum1就是所有数据的和
```

```
//1)定义一个变量用于求和
int sum1 = 0;
//2)定义一个循环产生1-100之间的奇数
for (int i = 1; i &lt; 100; i+=2) {
    // i = 1 3 5 7 ...
    //3)让需要求和的数据和sum1累加，
    sum1 += i;
}
System.out.println("1-100之间的奇数和：" +  sum1);
```

以上代码的执行流程分析

```
初始化sum1=0;

当i=1时：sum1+=1; sum1=1;
当i=3时：sum1+=3; sum1=4;
当i=5时：sum1+=5; sum1=9;
...
当i=99时：sum1+=99; sum1=2500
```

**2. 代码写法二**

```
求奇数和的思路（只是求和的数据变成了奇数，思路和前面没有变化）
	1)首先需要定义一个求和变量，这里命名为sum2
	2)再遍历得到所有需要求和的数据(1~100之间的所有整数)
	3)在求和之前先对数据判断，如果是奇数，才和sum1累加；否则什么也不干
	结果：所有数据累加完之后最终sum1就是所有数据的和
```

```
//1)首先需要定义一个求和变量，这里命名为sum2
int sum2 = 0; 
//2)再遍历得到所有需要求和的数据(1~100之间的所有整数)
for (int i = 1; i &lt;= 100; i++) {
    //i = 1 2 3 4 5 6 ... 99 100
    //3)在求和之前先对数据判断，如果是奇数，才和sum1累加；否则什么也不干
    if(i % 2 == 1){
        // i = 1 3 5 7 9 ... 99
        sum2 += i;
    }
}
System.out.println("1-100之间的奇数和：" + sum2);
```

**for循环小结**

今天关于for循环，我们学习这几个案例就够了，重点还是掌握for循环的执行流程。在以后，我们还会经常用到for循环，用多了，你就会越来越熟悉了。但是在具体场景下，还是需要具体问题具体分析。

---

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D90985e6efib4d3c363123b0827200e1a%26expires%3D24h%26dp_logid%3D443657076446953308%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-4trhQVxF0bvM0h0htGAbYawVSnw%25253D%26file_size%3D27749%26timestamp%3D1745903486%26method%3Dinfo%26fid%3D3170504070-250528-52052917322535%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6%2Fday03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6.md&fs_id=52052917322535&size=27749&uk=3170504070&from=yuanguanjia&fsid=52052917322535&clienttype=8&scence=mac_main#23-while%E5%BE%AA%E7%8E%AF%E6%A0%BC%E5%BC%8F%E5%92%8C%E6%B5%81%E7%A8%8B)2.3 while循环——格式和流程

各位同学，接下来我们学习第二种循环结构——while循环。

我们先来认识一下while循环长什么样子，然后按照格式写一个while循环的基础案例

![1661141338265](https://pan.baidu.com/wap/assets/1661141338265.png)

```
// 需求：打印5行Hello World
int i = 0;
while (i &lt; 5) {
    // i = 0 1 2 3 4
    System.out.println("Hello World");
    i++;
}
```

代码的执行流程如下图所示：按照① ②③④ ②③④ … 的流程执行

如果②步骤为true，才循环执行③④步骤

如果②步骤为false，则循环结束

![1661141996444](https://pan.baidu.com/wap/assets/1661141996444.png)

![1661141867092](https://pan.baidu.com/wap/assets/1661141867092.png)

**for、while如何选择**

学到这里，细心的同学可能会发现while循环和for循环的执行流程是一样的。那他们是不是可以通用呢？

- 从功能来说：能够用for循环做的，都能用while循环做。
    
- 使用规范上来说：知道循环几次，建议使用for；不知道循环几次建议使用while
    

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D90985e6efib4d3c363123b0827200e1a%26expires%3D24h%26dp_logid%3D443657076446953308%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-4trhQVxF0bvM0h0htGAbYawVSnw%25253D%26file_size%3D27749%26timestamp%3D1745903486%26method%3Dinfo%26fid%3D3170504070-250528-52052917322535%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6%2Fday03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6.md&fs_id=52052917322535&size=27749&uk=3170504070&from=yuanguanjia&fsid=52052917322535&clienttype=8&scence=mac_main#23-while%E5%BE%AA%E7%8E%AF%E6%A1%88%E4%BE%8B%E6%8A%98%E7%BA%B8%E6%A1%88%E4%BE%8B)2.3 while循环案例——折纸案例

各位同学，上一节我们已经学习了while循环的基本使用。下面我们通过一个案例再将while循环的使用巩固一下，主要目的还是想让大家知道什么使用while循环来完成需求。

案例需求如下：

```
需求：世界最高山峰珠穆朗玛峰高度是：8848.86米=8848860毫米，假如我有一张足够大的它的厚度是0.1毫米。请问：该纸张折叠多少次，可以折成珠穆朗玛峰的高度？
```

我们来分析一下该怎么做

```
分析：首先由于不知道折叠多少次，我们可以选择用while循环
	1)纸张的初始化厚度为0.1毫米，珠峰的高度为8848860毫米
		double peakHeight = 8848860;
		double paperThickness = 0.1;
	2)每次折叠纸张的厚度为原来的两倍，这是需要循环执行的
		while(纸张厚度&lt;8848860){
			纸张厚度*=2;
		}
	3)需要求折叠的次数，可以用一个变量来记录折叠的次数
		int 次数 = 0;
		while(纸张厚度&lt;8848860){
			纸张厚度*=2;
            次数++; //每次折叠次数累加
		}
	结果：等循环结束之后，打印记录次数的值，就是折叠多少次了。
```

按照上面分析的思路把代码写出来

```
// 1、定义变量记住珠穆朗玛峰的高度和纸张的高度。
double peakHeight = 8848860;
double paperThickness = 0.1;

// 3、定义一个变量count用于记住纸张折叠了多少次
int count = 0;

// 2、定义while循环控制纸张开始折叠
while (paperThickness &lt; peakHeight) {
    // 把纸张进行折叠，把纸张的厚度变成原来的2倍。
    paperThickness = paperThickness * 2;
    count++;
}
System.out.println("需要折叠多少次：" + count);
System.out.println("最终纸张的厚度是：" + paperThickness);
```

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D90985e6efib4d3c363123b0827200e1a%26expires%3D24h%26dp_logid%3D443657076446953308%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-4trhQVxF0bvM0h0htGAbYawVSnw%25253D%26file_size%3D27749%26timestamp%3D1745903486%26method%3Dinfo%26fid%3D3170504070-250528-52052917322535%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6%2Fday03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6.md&fs_id=52052917322535&size=27749&uk=3170504070&from=yuanguanjia&fsid=52052917322535&clienttype=8&scence=mac_main#24-do-while%E5%BE%AA%E7%8E%AF%E6%A0%BC%E5%BC%8F%E5%92%8C%E6%B5%81%E7%A8%8B)2.4 do-while循环——格式和流程

各位同学，接下来我们学习循环结构的第三种格式——do-while循环。

们先来认识一下while循环长什么样子，然后按照格式写一个while循环的基础案例。

![1661143715539](https://pan.baidu.com/wap/assets/1661143715539.png)

如下图所示：do-while循环的执行流程，是按照① ②③④ ②③④… 的顺序执行的。

我们会发现，do-while循环的特点是先执行，再判断的。即使条件不成立，也会先执行一次。

![1661143856132](https://pan.baidu.com/wap/assets/1661143856132.png)

**下面我们把三种循环的区别给同学们总结一下**

```
1. for循环 和 while循环（先判断后执行）; 
   do...while （先执行后判断）
   
2.for循环和while循环的执行流程是一模一样的，
	功能上无区别，for能做的while也能做，反之亦然。
	如果已知循环次数建议使用for循环，如果不清楚要循环多少次建议使用while循环。
	
3 for循环中控制循环的变量只在循环中使用
  while循环中，控制循环的变量在循环后还可以继续使用
```

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D90985e6efib4d3c363123b0827200e1a%26expires%3D24h%26dp_logid%3D443657076446953308%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-4trhQVxF0bvM0h0htGAbYawVSnw%25253D%26file_size%3D27749%26timestamp%3D1745903486%26method%3Dinfo%26fid%3D3170504070-250528-52052917322535%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6%2Fday03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6.md&fs_id=52052917322535&size=27749&uk=3170504070&from=yuanguanjia&fsid=52052917322535&clienttype=8&scence=mac_main#26-%E6%AD%BB%E5%BE%AA%E7%8E%AF)2.6 死循环

同学们在写代码时，可能一不小心把代码写成了死循环，所谓死循环就是停不下来的循环。

接下来，带着同学们认识几种死循环的写法。然后再说一下死循环有什么用。

```
//for死循环
for ( ; ; ){
    System.out.println("Hello World1");
}

//while死循环
while (true) {
    System.out.println("Hello World2");
}

//do-while死循环
do {
    System.out.println("Hello World3");
}while (true);
```

**死循环有什么应用场景呢？**

最典型的是可以用死循环来做服务器程序， 比如百度的服务器程序就是一直在执行的，你随时都可以通过浏览器去访问百度。如果哪一天百度的服务器停止了运行，有就意味着所有的人都永不了百度提供的服务了。

对于这样的应用我们目前了解一下就可以了。对于目前来说我们只要知道代码格式该怎么写，能达到什么效果就行。

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D90985e6efib4d3c363123b0827200e1a%26expires%3D24h%26dp_logid%3D443657076446953308%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-4trhQVxF0bvM0h0htGAbYawVSnw%25253D%26file_size%3D27749%26timestamp%3D1745903486%26method%3Dinfo%26fid%3D3170504070-250528-52052917322535%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6%2Fday03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6.md&fs_id=52052917322535&size=27749&uk=3170504070&from=yuanguanjia&fsid=52052917322535&clienttype=8&scence=mac_main#28-%E5%BE%AA%E7%8E%AF%E5%B5%8C%E5%A5%97)2.8 循环嵌套

各位同学，接下来我们学习一种在实际工作中很常用的循环形式——循环嵌套。

所谓循环嵌套，就是一个循环中又包含另一个循环（就是同学们常说的，套娃_），下面我们通过案例代码演示一下。

![1661145140910](https://pan.baidu.com/wap/assets/1661145140910.png)

循环嵌套执行流程：外部循环每循环一次，内部循环会全部执行完一轮。

```
i=0时; i&lt;3为true; 进入循环
	//j的取值从0到5,执行一轮，打印5次"我爱你"
	for(int j = 1; j &lt;= 5; j++) {
       System.out.println("我爱你：" + i);
    }
    内层循环执行完之后，执行外层的i++; i的值1
    
i=1时：i&lt;3为true; 进入循环
	//j的取值从0到5,又执行一轮，打印5次"我爱你"
	for(int j = 1; j &lt;= 5; j++) {
       System.out.println("我爱你：" + i);
    }
    内层循环执行完之后，执行外层的i++; i的值2
    
i=2时：i&lt;3为true; 进入循环
	//j的取值从0到5,再执行一轮，打印5次"我爱你"
	for(int j = 1; j &lt;= 5; j++) {
       System.out.println("我爱你：" + i);
    }
    内层循环执行完之后，执行外层的i++; i的值3
    
i=3时：i&lt;3为false; 外层循环结束
```

理解问循环嵌套的执行流程之后，我们再写一个案例来巩固一下

```
需求：在控制台使用 * 打印出4行5列的矩形
    ****
    ****
    ****
    ****
```

```
//1)先写一个循环用来在一行中打印5个"*"
for (int j = 1; j &lt;= 5; j++) {
    System.out.print("*"); // 不换行
}
System.out.println(); //换行


System.out.println("-----------------");

//2)再将第一步的代码套一层循环，执行4次，就可以打印4行
for (int i = 1; i &lt;= 4; i++) {
    for (int j = 1; j &lt;= 5; j++) {
        System.out.print("*"); // 不换行
    }
    System.out.println(); //换行
}
```

总结一下，对于嵌套循环重点理解这句话：**外部循环每循环一次，内部循环会全部执行完一轮。**

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D90985e6efib4d3c363123b0827200e1a%26expires%3D24h%26dp_logid%3D443657076446953308%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-4trhQVxF0bvM0h0htGAbYawVSnw%25253D%26file_size%3D27749%26timestamp%3D1745903486%26method%3Dinfo%26fid%3D3170504070-250528-52052917322535%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6%2Fday03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6.md&fs_id=52052917322535&size=27749&uk=3170504070&from=yuanguanjia&fsid=52052917322535&clienttype=8&scence=mac_main#29-%E8%B7%B3%E8%BD%AC%E8%AF%AD%E5%8F%A5-break-continue)2.9 跳转语句 break 、continue

前面我们学习了循环结构，在中间我们还接触了死循环的一些形式，那么我想要在循环过程中提前跳出循环怎么做呢？

这里就需要用到跳转语句，需要用到**break**和**continue**两个关键字。我们先来认识一下这两个关键字的作用

- break作用：跳出并结束当前所在循环的执行
- continue作用：结束本次循环，进入下一次循环

案例1：演示break的使用，提前终止循环的执行

```
// 1、break:跳出并结束当前所在循环的执行。
// 场景：假如你又有老婆了，你犯错了，你老婆罚你说：5句我爱你
// 说到第三句的时候心软了，让你别再说了。
for (int i = 1; i &lt;= 5; i++) {
    System.out.println("我爱你：" + i);
    if(i == 3){
        // 说明已经说完了第三句了，心软了。
        break; // 跳出并结束当前所在循环的执行。
    }
}
```

案例2：演示continue的使用，结束循环中的一次，继续下一次循环

```
// 2、continue:跳出当前循环的当次执行，直接进入循环的下一次执行。
// 场景: 假如你有老婆，你犯错了，你老婆罚你洗碗5天。
// 第三天的时候，你表现很好，第三天不用洗碗，但是不解恨，第四天还是要继续的。
for (int i = 1; i &lt;= 5; i++) {
    if(i == 3) {
        // 已经到了第三天，第三天不用洗的。
        continue;
    }
    System.out.println("洗碗：" + i);
}
```

需要注意的是**break和continue不是任何地方都可以使用的**

![1661146324812](https://pan.baidu.com/wap/assets/1661146324812.png)

![1661146405314](https://pan.baidu.com/wap/assets/1661146405314.png)

---

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D90985e6efib4d3c363123b0827200e1a%26expires%3D24h%26dp_logid%3D443657076446953308%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-4trhQVxF0bvM0h0htGAbYawVSnw%25253D%26file_size%3D27749%26timestamp%3D1745903486%26method%3Dinfo%26fid%3D3170504070-250528-52052917322535%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6%2Fday03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6.md&fs_id=52052917322535&size=27749&uk=3170504070&from=yuanguanjia&fsid=52052917322535&clienttype=8&scence=mac_main#210-%E5%BE%AA%E7%8E%AF%E7%BB%93%E6%9E%84%E6%80%BB%E7%BB%93)2.10 循环结构总结

到这里关于循环结构的所有内容就都已经学习完了，我们再把几种循环结构在什么场景下使用，再总结一下。

```
1. 什么是流程控制
	答：流程控制是用来控制程序的执行顺序的
	
2. 分支结构if和switch，如何选择？
	答：if分支：一般用于对一个范围进行判断
		switch分支：对一个一个值进行匹配
		
3. for循环和while循环、do-while如何循环
	答：知道循环次数用for、不知道循环次数用while
	   想要先执行，再判断，用do-while

```

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D90985e6efib4d3c363123b0827200e1a%26expires%3D24h%26dp_logid%3D443657076446953308%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-4trhQVxF0bvM0h0htGAbYawVSnw%25253D%26file_size%3D27749%26timestamp%3D1745903486%26method%3Dinfo%26fid%3D3170504070-250528-52052917322535%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6%2Fday03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6.md&fs_id=52052917322535&size=27749&uk=3170504070&from=yuanguanjia&fsid=52052917322535&clienttype=8&scence=mac_main#%E4%B8%89-%E7%94%9F%E6%88%90%E9%9A%8F%E6%9C%BA%E6%95%B0)三、生成随机数

各位同学，接下来我们再学习一个新的知识——生成随机数。

生成随机数其实在很多场景下都很实用，比如，在课堂上可以写一个随机点名器点同学起来回答问题；再比如公司年会可以随机抽奖等。

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D90985e6efib4d3c363123b0827200e1a%26expires%3D24h%26dp_logid%3D443657076446953308%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-4trhQVxF0bvM0h0htGAbYawVSnw%25253D%26file_size%3D27749%26timestamp%3D1745903486%26method%3Dinfo%26fid%3D3170504070-250528-52052917322535%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6%2Fday03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6.md&fs_id=52052917322535&size=27749&uk=3170504070&from=yuanguanjia&fsid=52052917322535&clienttype=8&scence=mac_main#31-%E5%A6%82%E4%BD%95%E4%BA%A7%E7%94%9F%E4%B8%80%E4%B8%AA%E9%9A%8F%E6%9C%BA%E6%95%B0)3.1 如何产生一个随机数

生成随机数的功能，其实 Java已经给我们提供了，在JDK中提供了一个类叫做Random，我们只需要调用Random这个类提供的功能就可以了。

![1661147570538](https://pan.baidu.com/wap/assets/1661147570538.png)

```
// 目标：掌握使用Random生成随机数的步骤。
// 1、导包。import java.util.Random; (idea会自动完成)
import java.util.Random;
public class RandomDemo1 {
    public static void main(String[] args) {
        // 2、创建一个Random对象，用于生成随机数。
        Random r = new Random();
        // 3、调用Random提供的功能：nextInt得到随机数。
        for (int i = 1; i &lt;= 20; i++) {
            int data = r.nextInt(10); // 0 - 9
            System.out.println(data);
        }
    }
}
```

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D90985e6efib4d3c363123b0827200e1a%26expires%3D24h%26dp_logid%3D443657076446953308%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-4trhQVxF0bvM0h0htGAbYawVSnw%25253D%26file_size%3D27749%26timestamp%3D1745903486%26method%3Dinfo%26fid%3D3170504070-250528-52052917322535%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6%2Fday03-Java%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6.md&fs_id=52052917322535&size=27749&uk=3170504070&from=yuanguanjia&fsid=52052917322535&clienttype=8&scence=mac_main#32-%E7%8C%9C%E6%95%B0%E5%AD%97%E5%B0%8F%E6%B8%B8%E6%88%8F)3.2 猜数字小游戏

各位同学，接下来我们通过一个案例把前面的流程控制、跳转语句、随机数综合运用一下；

如果能把这个案例写出来，说明你对今天的知识点掌握得挺好了。

```
需求：
	随机生成一个1-100之间的数据，提示用户猜测，猜大提示过大，猜小提示过小，直到猜中	  结束游戏

分析：
	1.先随机生成一个1-100之间的数据。
		谁可以帮你生成随机数啊？ 是不是要用到Random？
		
	2.定义一个死循环让用户可以一直猜测。
		用户猜的数据从哪里来啊？ 是不是要用到Scanner?

	3.在死循环里，每次让用户录入的数据和随机数进行比较
		如果比随机数大：提示猜大了
		如果比随机数小：提示猜小了
		如果和随机数相同：提示恭喜你猜中了
```

```
import java.util.Random;
import java.util.Scanner;

public class RandomTest2 {
    public static void main(String[] args) {
        // 1、随机产生一个1-100之间的数据，做为中奖号码。
        Random r = new Random();
        int luckNumber = r.nextInt(100) + 1;

        // 2、定义一个死循环，让用户不断的猜测数据
        Scanner sc = new Scanner(System.in);
        while (true) {
            // 提示用户猜测
            System.out.println("请您输入您猜测的数据：");
            int guessNumber = sc.nextInt();

            // 3、判断用户猜测的数字与幸运号码的大小情况
            if(guessNumber &gt; luckNumber){
                System.out.println("您猜测的数字过大~~");
            }else if(guessNumber &lt; luckNumber){
                System.out.println("您猜测的数字过小~~");
            }else {
                System.out.println("恭喜您，猜测成功了，可以买单了~~");
                break; // 结束死循环
            }
        }
    }
}
```

# day04——Java数组

各位同学，今天我们学习一个Java中非常重要的技术——数组。

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Da13e17f43h572d2b4b2b5594fdd7f59f%26expires%3D24h%26dp_logid%3D443671418237770880%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-0NHcYomV1UVRKQNUz3x8eEoTI2Y%25253D%26file_size%3D21677%26timestamp%3D1745903539%26method%3Dinfo%26fid%3D3170504070-250528-900388460159693%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day04-Java%E6%95%B0%E7%BB%84.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday04-Java%E6%95%B0%E7%BB%84%2Fday04-Java%E6%95%B0%E7%BB%84.md&fs_id=900388460159693&size=21677&uk=3170504070&from=yuanguanjia&fsid=900388460159693&clienttype=8&scence=mac_main#%E4%B8%80-%E8%AE%A4%E8%AF%86%E6%95%B0%E7%BB%84)一、认识数组

先来认识一下什么数组

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Da13e17f43h572d2b4b2b5594fdd7f59f%26expires%3D24h%26dp_logid%3D443671418237770880%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-0NHcYomV1UVRKQNUz3x8eEoTI2Y%25253D%26file_size%3D21677%26timestamp%3D1745903539%26method%3Dinfo%26fid%3D3170504070-250528-900388460159693%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day04-Java%E6%95%B0%E7%BB%84.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday04-Java%E6%95%B0%E7%BB%84%2Fday04-Java%E6%95%B0%E7%BB%84.md&fs_id=900388460159693&size=21677&uk=3170504070&from=yuanguanjia&fsid=900388460159693&clienttype=8&scence=mac_main#1-%E4%BB%80%E4%B9%88%E6%95%B0%E7%BB%84)1. 什么数组

数组就是一个容器，用来存一批同种类型的数据的。

比如：想要存储 20,10,80,60,90 这些数据。 我们可以把代码写成这样

```
int[] array = {20,10,80,60,90};
```

比如：想要存储 “牛二“,“西门“,“全蛋“ 这些数据。我们可以把代码写成这样

```
String[] names = {"牛二", "西门", "全蛋"};
```

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Da13e17f43h572d2b4b2b5594fdd7f59f%26expires%3D24h%26dp_logid%3D443671418237770880%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-0NHcYomV1UVRKQNUz3x8eEoTI2Y%25253D%26file_size%3D21677%26timestamp%3D1745903539%26method%3Dinfo%26fid%3D3170504070-250528-900388460159693%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day04-Java%E6%95%B0%E7%BB%84.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday04-Java%E6%95%B0%E7%BB%84%2Fday04-Java%E6%95%B0%E7%BB%84.md&fs_id=900388460159693&size=21677&uk=3170504070&from=yuanguanjia&fsid=900388460159693&clienttype=8&scence=mac_main#2-%E6%95%B0%E7%BB%84%E7%9A%84%E5%BA%94%E7%94%A8%E5%9C%BA%E6%99%AF)2. 数组的应用场景

有变量，为什么还要有数组呢？ 比如，我们要做一个点名器

![1661321640902](https://pan.baidu.com/wap/assets/1661321640902.png)

如果用变量来做的话，代码是这样子的

![1661321680612](https://pan.baidu.com/wap/assets/1661321680612.png)

如果用数组来做的话，代码是这样子的

![1661321716135](https://pan.baidu.com/wap/assets/1661321716135.png)

一对比我们发现数组的写法比变量的写法更加简洁，所以我们可以得出一个结论

**结论：遇到批量数据的存储和操作时，数组比变量更适合**

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Da13e17f43h572d2b4b2b5594fdd7f59f%26expires%3D24h%26dp_logid%3D443671418237770880%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-0NHcYomV1UVRKQNUz3x8eEoTI2Y%25253D%26file_size%3D21677%26timestamp%3D1745903539%26method%3Dinfo%26fid%3D3170504070-250528-900388460159693%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day04-Java%E6%95%B0%E7%BB%84.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday04-Java%E6%95%B0%E7%BB%84%2Fday04-Java%E6%95%B0%E7%BB%84.md&fs_id=900388460159693&size=21677&uk=3170504070&from=yuanguanjia&fsid=900388460159693&clienttype=8&scence=mac_main#%E4%BA%8C-%E6%95%B0%E7%BB%84%E7%9A%84%E5%AE%9A%E4%B9%89%E5%92%8C%E8%AE%BF%E9%97%AE)二、数组的定义和访问

各位同学，我们已经知道数组是用来干什么的。那么如何使用Java语言写一个数组呢？这里就需要学习一下数组的初始化格式。

数组有两种初始化的方式，一种是静态初始化、一种是动态初始化。我们先用静态初始化来学习数组的操作。

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Da13e17f43h572d2b4b2b5594fdd7f59f%26expires%3D24h%26dp_logid%3D443671418237770880%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-0NHcYomV1UVRKQNUz3x8eEoTI2Y%25253D%26file_size%3D21677%26timestamp%3D1745903539%26method%3Dinfo%26fid%3D3170504070-250528-900388460159693%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day04-Java%E6%95%B0%E7%BB%84.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday04-Java%E6%95%B0%E7%BB%84%2Fday04-Java%E6%95%B0%E7%BB%84.md&fs_id=900388460159693&size=21677&uk=3170504070&from=yuanguanjia&fsid=900388460159693&clienttype=8&scence=mac_main#21-%E6%95%B0%E7%BB%84%E7%9A%84%E9%9D%99%E6%80%81%E5%88%9D%E5%A7%8B%E5%8C%96)2.1 数组的静态初始化

所谓静态初始化指的是：在定义数组时直接给数组中的数据赋值。

**1. 静态初始化标准格式：**

```
数据类型[] 变量名 = new 数据类型[]{元素1,元素2,元素3};
```

按照格式定义int类型、double类型数组

```
//定义数组，用来存储多个年龄
int[] ages = new int[]{12, 24, 36}
//定义数组，用来存储多个成绩
double[] scores = new double[]{89.9, 99.5, 59.5, 88.0};
```

**2. 静态初始化简化格式**

Java语言的设计者为了简化定义数组的写法，还为静态初始化提供了一种简化写法

```
数据类型[] 变量名 = {元素1,元素2,元素3};
```

使用简化格式定义int类型、double类型数组

```
//定义数组，用来存储多个年龄
int[] ages = {12, 24, 36}
//定义数组，用来存储多个成绩
double[] scores = {89.9, 99.5, 59.5, 88.0};
```

**3. 注意哟！！**

- 定义数组时， `数据类型[] 数组名` 也可写成 `数据类型 数组名[]`

```
//以下两种写法是等价的。但是建议大家用第一种，因为这种写法更加普遍
int[] ages = {12, 24, 36};
int ages[] = {12, 24, 36}
```

**4. 数组在计算机中的基本原理**

我们知道数组是怎么定义的之后，那么接下来看一下数组在计算机中的基本原理。

我们以`int[] ages = {12,24,36};`这句话为例，看一下这句话到底在计算机中做了那些事情。

- 首先，左边`int[] ages` 表示定义了一个数组类型的变量，变量名叫ages
- 其次，右边`{12,24,36}`表示创建一个数组对象，你完全可以把它理解成一个能装数据的东西。这个对象在内存中会有一个地址值`[I@4c873330`，每次创建一个数组对象都会有不用的地址值。
- 然后，把右边的地址值`[I@4c873330`赋值给左边的ages变量
- 所以，ages变量就可以通过地址值，找到数组这个东西。

![1661353166416](https://pan.baidu.com/wap/assets/1661353166416.png)

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Da13e17f43h572d2b4b2b5594fdd7f59f%26expires%3D24h%26dp_logid%3D443671418237770880%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-0NHcYomV1UVRKQNUz3x8eEoTI2Y%25253D%26file_size%3D21677%26timestamp%3D1745903539%26method%3Dinfo%26fid%3D3170504070-250528-900388460159693%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day04-Java%E6%95%B0%E7%BB%84.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday04-Java%E6%95%B0%E7%BB%84%2Fday04-Java%E6%95%B0%E7%BB%84.md&fs_id=900388460159693&size=21677&uk=3170504070&from=yuanguanjia&fsid=900388460159693&clienttype=8&scence=mac_main#22-%E6%95%B0%E7%BB%84%E7%9A%84%E5%85%83%E7%B4%A0%E8%AE%BF%E9%97%AE)2.2 数组的元素访问

各位同学，通过刚才的学习，我们知道数组是用来存储数据的。那么数组中存储的数据又如何访问呢？这里所说的访问，意思就是获取中数组中数据的值、或者给数组中的数据赋值。

这里先给大家统一几个概念，数组中存储的数据我们叫做元素；而且数组中的每一个元素都有一个编号与之对应，我们把这个编号叫做索引，这个索引是从0依次递增的整数。如下图所示

![1661354056668](https://pan.baidu.com/wap/assets/1661354056668.png)

要想访问数组中的元素，格式如下

```
//数组名可以找到数组对象的地址，再通过索引就可以定位到具体的元素了
数组名[索引]
```

接下来用代码来演示一下

```
//索引：	   0   1   2
int[] arr = {12, 24, 36};
// 1、访问数组的全部数据
System.out.println(arr[0]); //12
System.out.println(arr[1]); //24
System.out.println(arr[2]); //36
//下面代码没有3索引，会出现ArrayIndexOutOfBoundsException 索引越界异常
//System.out.println(arr[3]); 

// 2、修改数组中的数据
arr[0] = 66;
arr[2] = 100;
System.out.println(arr[0]); //66
System.out.println(arr[1]); 0
System.out.println(arr[2]); //100
```

除了访问数组中的元素，我们可以获取数组中元素的个数，后面我们统称为数组的长度。

```
// 3、访问数组的元素个数：数组名.length
System.out.println(arr.length);

// 技巧：获取数组的最大索引: arr.length - 1(前提是数组中存在数据)
System.out.println(arr.length - 1);

int[] arr2 = {};
System.out.println(arr2.length - 1);
```

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Da13e17f43h572d2b4b2b5594fdd7f59f%26expires%3D24h%26dp_logid%3D443671418237770880%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-0NHcYomV1UVRKQNUz3x8eEoTI2Y%25253D%26file_size%3D21677%26timestamp%3D1745903539%26method%3Dinfo%26fid%3D3170504070-250528-900388460159693%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day04-Java%E6%95%B0%E7%BB%84.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday04-Java%E6%95%B0%E7%BB%84%2Fday04-Java%E6%95%B0%E7%BB%84.md&fs_id=900388460159693&size=21677&uk=3170504070&from=yuanguanjia&fsid=900388460159693&clienttype=8&scence=mac_main#23-%E6%95%B0%E7%BB%84%E7%9A%84%E9%81%8D%E5%8E%86)2.3 数组的遍历

各位同学，接下来我们学习一个对数组最最最常见的操作——数组遍历。所谓遍历意思就是将数组中的元素一个一个的取出来。

我们刚才学习了数组中元素的访问，访问元素必须用到索引，如下列代码。

```
int[] ages = {12, 24, 36};
System.out.println(ages[0]);
System.out.println(ages[1]);
System.out.println(ages[2]);
```

但是，如果数组中有很多很多元素，索引靠自己一个一个数肯定是不行的！我们可以使用for循环从0开始一直遍历到长度-1的位置，就可以获取所有的索引了。

当你获取到每一个索引，那么每一个元素不就获取到了吗？上代码吧

```
int[] ages = {12, 24, 36};
for (int i = 0; i &lt; ages.length; i++) {
    // i的取值 = 0,1,2
    System.out.println(ages[i]); 
}
```

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Da13e17f43h572d2b4b2b5594fdd7f59f%26expires%3D24h%26dp_logid%3D443671418237770880%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-0NHcYomV1UVRKQNUz3x8eEoTI2Y%25253D%26file_size%3D21677%26timestamp%3D1745903539%26method%3Dinfo%26fid%3D3170504070-250528-900388460159693%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day04-Java%E6%95%B0%E7%BB%84.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday04-Java%E6%95%B0%E7%BB%84%2Fday04-Java%E6%95%B0%E7%BB%84.md&fs_id=900388460159693&size=21677&uk=3170504070&from=yuanguanjia&fsid=900388460159693&clienttype=8&scence=mac_main#24-%E6%95%B0%E7%BB%84%E9%9D%99%E6%80%81%E5%88%9D%E5%A7%8B%E5%8C%96%E6%A1%88%E4%BE%8B)2.4 数组静态初始化案例

学习完数组的静态初始化之后，接下来我们做一个练习题来巩固一下。

```
需求：某部门5名员工的销售额分别是：16、26、36、6、100，请计算出他们部门的总销售额。

需求分析：
	1.看到有16、26、36、6、100这5个数据数据，而且数据值很明确;
		1)想到,可以使用数组静态初始化把这5个数据存起来
	
	2.请计算出他们部门的总销售额（这不就是求数组中数据的和吗？）
		2)必须先将数组中所有的元素遍历出来
		3)想要求和，得先有一个求和变量sum
		4)再将每一个元素和求和变量sum进行累加（求和思想）
```

按照分析的思路来写代码

```
// 1、定义一个数组存储5名员工的销售额
//索引          0   1    2  3   4
int[] money = {16, 26, 36, 6, 100};

// 3、定义一个变量用于累加求和
int sum = 0;

// 2、遍历这个数组中的每个数据。
for (int i = 0; i &lt; money.length; i++) {
    // i = 0  1  2  3  4
    sum += money[i];
}
System.out.println("员工的销售总额：" + sum);
```

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Da13e17f43h572d2b4b2b5594fdd7f59f%26expires%3D24h%26dp_logid%3D443671418237770880%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-0NHcYomV1UVRKQNUz3x8eEoTI2Y%25253D%26file_size%3D21677%26timestamp%3D1745903539%26method%3Dinfo%26fid%3D3170504070-250528-900388460159693%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day04-Java%E6%95%B0%E7%BB%84.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday04-Java%E6%95%B0%E7%BB%84%2Fday04-Java%E6%95%B0%E7%BB%84.md&fs_id=900388460159693&size=21677&uk=3170504070&from=yuanguanjia&fsid=900388460159693&clienttype=8&scence=mac_main#25-%E6%95%B0%E7%BB%84%E7%9A%84%E5%8A%A8%E6%80%81%E5%88%9D%E5%A7%8B%E5%8C%96)2.5 数组的动态初始化

各位同学，刚才我们初始化数组时，都是直接将元素写出来。但是还有另一个初始化数组的方式叫 **动态初始化**。

动态初始化不需要我们写出具体的元素，而是指定元素类型和长度就行。格式如下

```
//数据类型[]  数组名 = new 数据类型[长度];
int[] arr = new int[3];
```

下面是动态初始化数组的原理图。我们发现`int[] arr` 其实就是一个变量，它记录了数组对象的地址值，而且数组中的元素默认值是0。

![1661356063895](https://pan.baidu.com/wap/assets/1661356063895.png)

**注意：**

使用动态初始化定义数组时，根据元素类型不同，默认值也有所不同。

![1661417981361](https://pan.baidu.com/wap/assets/1661417981361.png)

关于数组动态初始化的格式和原理，咱们就先学习到这里。

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Da13e17f43h572d2b4b2b5594fdd7f59f%26expires%3D24h%26dp_logid%3D443671418237770880%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-0NHcYomV1UVRKQNUz3x8eEoTI2Y%25253D%26file_size%3D21677%26timestamp%3D1745903539%26method%3Dinfo%26fid%3D3170504070-250528-900388460159693%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day04-Java%E6%95%B0%E7%BB%84.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday04-Java%E6%95%B0%E7%BB%84%2Fday04-Java%E6%95%B0%E7%BB%84.md&fs_id=900388460159693&size=21677&uk=3170504070&from=yuanguanjia&fsid=900388460159693&clienttype=8&scence=mac_main#26-%E6%95%B0%E7%BB%84%E5%8A%A8%E6%80%81%E5%88%9D%E5%A7%8B%E5%8C%96%E6%A1%88%E4%BE%8B)2.6 数组动态初始化案例

各位同学，接下来我们做一个数组动态初始化的案例。

```
案例需求：
	某歌唱比赛，需要开发一个系统：可以录入6名评委的打分，录入完毕后立即输出平均分做
	选手得分

需求分析：
	1.需要录入6名评委的分数，可以用一个数组来保存。
	   因为在评委没有录入分数之前，还不确定数组中应该存哪些数据。
	   所以可以使用数组的动态初始化
	2.遍历数组中的每一个位置，并录入分数，将分数存入数组中
	3.遍历数组中的每一个元素，对元素求和
```

代码如下

```
// 1、定义一个动态初始化的数组，负责后期存储6个评委的打分。
double[] scores = new double[6];

Scanner sc  = new Scanner(System.in);

// 2、遍历数组中的每个位置，录入评委的分数，存入到数组中去
for (int i = 0; i &lt; scores.length; i++) {
    // i = 0 1 2 3 4 5
    System.out.println("请您输入当前第" + (i + 1) +"个评委的分数：");
    double score = sc.nextDouble();
    scores[i] = score;
}

// 3、遍历数组中的每个元素进行求和
double sum  = 0;
for (int i = 0; i &lt; scores.length; i++) {
    sum += scores[i];
}
System.out.println("选手最终得分是：" + sum / scores.length);
```

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Da13e17f43h572d2b4b2b5594fdd7f59f%26expires%3D24h%26dp_logid%3D443671418237770880%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-0NHcYomV1UVRKQNUz3x8eEoTI2Y%25253D%26file_size%3D21677%26timestamp%3D1745903539%26method%3Dinfo%26fid%3D3170504070-250528-900388460159693%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day04-Java%E6%95%B0%E7%BB%84.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday04-Java%E6%95%B0%E7%BB%84%2Fday04-Java%E6%95%B0%E7%BB%84.md&fs_id=900388460159693&size=21677&uk=3170504070&from=yuanguanjia&fsid=900388460159693&clienttype=8&scence=mac_main#%E4%B8%89-%E6%95%B0%E7%BB%84%E5%9C%A8%E8%AE%A1%E7%AE%97%E6%9C%BA%E4%B8%AD%E7%9A%84%E6%89%A7%E8%A1%8C%E5%8E%9F%E7%90%86)三、数组在计算机中的执行原理

好的各位同学，在前面我们已经学习了数组的基本使用，也理解了数组的基本原理。由于数组是一个容器，变量也是一个容器，在理解他们执行原理的时候，有些同学就容易搞混，现在我把他们放在一起带着大家回顾一下他们的会执行原理，顺便带着大家详细理解一下Java程序的执行的内存原理。

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Da13e17f43h572d2b4b2b5594fdd7f59f%26expires%3D24h%26dp_logid%3D443671418237770880%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-0NHcYomV1UVRKQNUz3x8eEoTI2Y%25253D%26file_size%3D21677%26timestamp%3D1745903539%26method%3Dinfo%26fid%3D3170504070-250528-900388460159693%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day04-Java%E6%95%B0%E7%BB%84.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday04-Java%E6%95%B0%E7%BB%84%2Fday04-Java%E6%95%B0%E7%BB%84.md&fs_id=900388460159693&size=21677&uk=3170504070&from=yuanguanjia&fsid=900388460159693&clienttype=8&scence=mac_main#31-%E6%95%B0%E7%BB%84%E7%9A%84%E6%89%A7%E8%A1%8C%E5%8E%9F%E7%90%86java%E7%A8%8B%E5%BA%8F%E7%9A%84%E6%89%A7%E8%A1%8C%E5%8E%9F%E7%90%86)3.1 数组的执行原理，Java程序的执行原理

我们以下面的代码，来讲解变量、数组的执原理。

```
public class ArrayDemo1 {
    public static void main(String[] args) {
        int a = 10;
        System.out.println(a);

        int[] arr = new int[]{11, 22, 33};
        System.out.println(arr);

        System.out.println(arr[1]);

        arr[0] = 44;
        arr[1] = 55;
        arr[2] = 66;

        System.out.println(arr[0]);
        System.out.println(arr[1]);
        System.out.println(arr[2]);
    }
}
```

前面我们给大家讲过，程序是在内存中执行的。实际上Java程序是把编译后的字节码加载到Java虚拟机中执行的。

![1661437717797](https://pan.baidu.com/wap/assets/1661437717797.png)

Java为了便于虚拟机执行Java程序，将虚拟机的内存划分为 方法区、栈、堆、本地方法栈、寄存器 这5块区域。同学们需要重点关注的是 **方法区、栈、堆**。

下面把每一个块内存区域作用介绍一下，我们大致只需要知道每一部分存储什么内容就行。

- **方法区**：字节码文件先加载到这里
- **栈**：方法运行时所进入的内存区域，由于变量在方法中，所以变量也在这一块区域中
- **堆**：存储new出来的东西，并分配地址。由于数组是new 出来的，所以数组也在这块区域。

下面是上面案例执行的内存原理如下图所示，按照① ② ③ ④ ⑤ ⑥ 的标记的顺序来看

![1661438278304](https://pan.baidu.com/wap/assets/1661438278304.png)

**总结一下`int a = 10`与 `int[] arr = new int[]{11,22,33}的区别`**

- **a**是一个变量，在栈内存中，**a**变量中存储的数据就是**10**这个值。
- **arr**也是一个变量，在栈中，存储的是数组对象在堆内存中的地址值

```
// 这里的int a是一个基本类型变量，存储的是一个数值
int a = 10 ; 
//这里的int[] arr是一个引用类型的变量，存储的是一个地址值
int[] arr = new int[]{44,55,66};
```

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Da13e17f43h572d2b4b2b5594fdd7f59f%26expires%3D24h%26dp_logid%3D443671418237770880%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-0NHcYomV1UVRKQNUz3x8eEoTI2Y%25253D%26file_size%3D21677%26timestamp%3D1745903539%26method%3Dinfo%26fid%3D3170504070-250528-900388460159693%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day04-Java%E6%95%B0%E7%BB%84.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday04-Java%E6%95%B0%E7%BB%84%2Fday04-Java%E6%95%B0%E7%BB%84.md&fs_id=900388460159693&size=21677&uk=3170504070&from=yuanguanjia&fsid=900388460159693&clienttype=8&scence=mac_main#32-%E5%A4%9A%E4%B8%AA%E5%8F%98%E9%87%8F%E6%8C%87%E5%90%91%E5%90%8C%E4%B8%80%E4%B8%AA%E6%95%B0%E7%BB%84%E7%9A%84%E9%97%AE%E9%A2%98)3.2 多个变量指向同一个数组的问题

各位同学，我们了解了数组在内存中的执行原理。我们知道数组类型的变量，指向的是堆内存中数组对象的地址。但是在实际开发中可能存在一种特殊情况，就是多个变量指向同一个数组对象的形式。

讲解这个知识点的目的，是让同学们注意多个变量指向同一个数组对象存在什么问题？

我们先看一段代码

```
public class ArrayDemo2 {
    public static void main(String[] args) {
        // 目标：认识多个变量指向同一个数组对象的形式，并掌握其注意事项。
        int[] arr1 = {11, 22, 33};

        // 把int类型的数组变量arr1赋值给int类型的数组变量arr2
        int[] arr2 = arr1;

        System.out.println(arr1);
        System.out.println(arr2);

        arr2[1] = 99;
        System.out.println(arr1[1]);

        arr2 = null; // 拿到的数组变量中存储的值是null
        System.out.println(arr2);

        //System.out.println(arr2[0]);
        //System.out.println(arr2.length);
    }
}
```

我们重点关注这一段代码

![1661439843879](https://pan.baidu.com/wap/assets/1661439843879.png)

刚执行完`int[] arr1 = {11,22,33};`时，内存原理如下

![1661439986204](https://pan.baidu.com/wap/assets/1661439986204.png)

当执行完`int[] arr2 = arr1;`后，内存原理如下

![1661440179341](https://pan.baidu.com/wap/assets/1661440179341.png)

当执行到`arr2[1]=99;时`，内存原理如下

![1661440425901](https://pan.baidu.com/wap/assets/1661440425901.png)

**总结一下：**

- 两个变量指向同一个数组时，两个变量记录的是同一个地址值。
    
- 当一个变量修改数组中的元素时，另一个变量去访问数组中的元素，元素已经被修改过了。
    

到这里有关数组的基本操作，和内存原理我们就全部学习完了。

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Da13e17f43h572d2b4b2b5594fdd7f59f%26expires%3D24h%26dp_logid%3D443671418237770880%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-0NHcYomV1UVRKQNUz3x8eEoTI2Y%25253D%26file_size%3D21677%26timestamp%3D1745903539%26method%3Dinfo%26fid%3D3170504070-250528-900388460159693%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day04-Java%E6%95%B0%E7%BB%84.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday04-Java%E6%95%B0%E7%BB%84%2Fday04-Java%E6%95%B0%E7%BB%84.md&fs_id=900388460159693&size=21677&uk=3170504070&from=yuanguanjia&fsid=900388460159693&clienttype=8&scence=mac_main#%E5%9B%9B-%E6%95%B0%E7%BB%84%E4%B8%93%E9%A1%B9%E7%BB%83%E4%B9%A0)四、数组专项练习

接下来我们做一些专项练习题，把数组的常见操作练习一下。在学习这个案例时，重点掌握数组求最值的思路，代码只是用来表达你的思路的。

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Da13e17f43h572d2b4b2b5594fdd7f59f%26expires%3D24h%26dp_logid%3D443671418237770880%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-0NHcYomV1UVRKQNUz3x8eEoTI2Y%25253D%26file_size%3D21677%26timestamp%3D1745903539%26method%3Dinfo%26fid%3D3170504070-250528-900388460159693%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day04-Java%E6%95%B0%E7%BB%84.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday04-Java%E6%95%B0%E7%BB%84%2Fday04-Java%E6%95%B0%E7%BB%84.md&fs_id=900388460159693&size=21677&uk=3170504070&from=yuanguanjia&fsid=900388460159693&clienttype=8&scence=mac_main#41-%E6%95%B0%E7%BB%84%E6%B1%82%E6%9C%80%E5%80%BC)4.1 数组求最值

```
需求：定义一个int类型数组，求数组中元素的最大值，并打印最大值
```

我们先看一下选美比赛，是怎么选出颜值最高的人的。然后再以此思路，来写代码找出数组中元素的最大值。

![1661441712915](https://pan.baidu.com/wap/assets/1661441712915.png)

```
数组求最大值思路：
	1)先找出数组中0索引的元素，假设为最大值，用max表示【擂主】
	2)遍历后面的每一个元素和max比较，把较大的元素值重新赋值给max(擂主换人)
    3)最后max就是所有元素的最大值(最后站在台上的擂主)
```

```
public class Test1 {
    public static void main(String[] args) {
        // 1、把颜值数据拿到程序中来，用数组装起来
        int[] faceScores = {15, 9000, 10000, 20000, 9500, -5};

        // 2、定义一个变量用于最终记住最大值。
        int max = faceScores[0];

        // 3、从数组的第二个位置开始遍历。
        for (int i = 1; i &lt; faceScores.length; i++) {
            // i = 1  2  3  4  5
            // 判断一下当前遍历的这个数据，是否大于最大值变量max存储的数据，
            //如果大于，当前遍历的数据需要赋值给max
            if(faceScores[i] &gt; max ){
                max = faceScores[i];
            }
        }
        System.out.println("最高颜值是：" + max);
    }
}
```

**总结一下：**

通过这个案例，我们主要掌握求最值的思路，以后不管遇到求最大值还是最小值，编程思路都是一样的，不同的可能是数据不同。

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Da13e17f43h572d2b4b2b5594fdd7f59f%26expires%3D24h%26dp_logid%3D443671418237770880%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-0NHcYomV1UVRKQNUz3x8eEoTI2Y%25253D%26file_size%3D21677%26timestamp%3D1745903539%26method%3Dinfo%26fid%3D3170504070-250528-900388460159693%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day04-Java%E6%95%B0%E7%BB%84.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday04-Java%E6%95%B0%E7%BB%84%2Fday04-Java%E6%95%B0%E7%BB%84.md&fs_id=900388460159693&size=21677&uk=3170504070&from=yuanguanjia&fsid=900388460159693&clienttype=8&scence=mac_main#42-%E6%95%B0%E7%BB%84%E5%85%83%E7%B4%A0%E5%8F%8D%E8%BD%AC)4.2 数组元素反转

```
需求：某个数组有5个数据：10,20,30,40,50，请将这个数组中的数据进行反转。
      [10, 20, 30, 40, 50]  反转后 [50, 40, 30, 20, 10]
```

数组元素反转的核心，其实是数组中两个数据的交换。我们可以认为两个数据分别存储在两个水杯中。想要交换两个水杯中的东西，我们得借助第三个水杯，如下图所示

![1661442733592](https://pan.baidu.com/wap/assets/1661442733592.png)

![1661442758553](https://pan.baidu.com/wap/assets/1661442758553.png)

数组中元素交换，就是用的借用第三方变量的思想。 我们把数组中的每一个元素当做一个水杯，然后索引控制哪两个元素互换位置。

怎么样，才能达到元素反转的效果呢？我们只需将第一个和最后一个元素互换、第二个和倒数第二个互换、依次内推… 如下图所示

![1661443189060](https://pan.baidu.com/wap/assets/1661443189060.png)

怎么样写代码，才能达到上面的效果呢？我们继续分析

```
1.每次交换，需要有左右两边的两个索引，我们可以用i和j表示
	刚开始i=0，j=数组长度-1;
2.每次让i和j索引位置的两个元素互换位置
	arr[i]和arr[j]互换位置
3.每次还完位置之后，让i往右移动一位，让j往前移动一位
```

具体代码如下

```
public class Test2 {
    public static void main(String[] args) {
        // 目标：完成数组反转。
        // 1、准备一个数组
        int[] arr = {10, 20, 30, 40, 50};  

        // 2、定义一个循环，设计2个变量，一个在前，一个在后
        for (int i = 0, j = arr.length - 1; i &lt; j; i++, j--) {
            // arr[i]   arr[j]
            // 交换
            // 1、定义一个临时变量记住后一个位置处的值
            int temp = arr[j];
            // 2、把前一个位置处的值赋值给后一个位置了
            arr[j] = arr[i];
            // 3、把临时变量中记住的后一个位置处的值赋值给前一个位置处
            arr[i] = temp;
        }

        // 3、遍历数组中的每个数据，看是否反转成功了
        for (int i = 0; i &lt; arr.length; i++) {
            System.out.print(arr[i] + " ");
        }
    }
}
```

**总结一下：**

通过上面的案例，需要我们掌握元素互换位置的编程思路；以后遇到数据互换问题，都这样做。

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Da13e17f43h572d2b4b2b5594fdd7f59f%26expires%3D24h%26dp_logid%3D443671418237770880%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-0NHcYomV1UVRKQNUz3x8eEoTI2Y%25253D%26file_size%3D21677%26timestamp%3D1745903539%26method%3Dinfo%26fid%3D3170504070-250528-900388460159693%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day04-Java%E6%95%B0%E7%BB%84.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday04-Java%E6%95%B0%E7%BB%84%2Fday04-Java%E6%95%B0%E7%BB%84.md&fs_id=900388460159693&size=21677&uk=3170504070&from=yuanguanjia&fsid=900388460159693&clienttype=8&scence=mac_main#43-%E9%9A%8F%E6%9C%BA%E6%8E%92%E5%90%8D)4.3 随机排名

各位同学，通过数组元素反转的案例，我们学会了如何对两个数据进行交换。接下来，我们再学习随机排名案例，将数据交换的思路再巩固一下。

先来看一下需求

```
需求：某公司开发部5名开发人员，要进行项目进展汇报演讲，现在采取随机排名后进行汇报。请先依次录入5名员工的工号，然后展示出一组随机的排名顺序。
```

分析一下随机排名的思路

```
1.在程序中录入5名员工的工号存储起来 ---&gt; 使用动态初始化数组的方式。
2.依次遍历数组中的每个数据。
3.每遍历到一个数据，都随机一个索引值出来，让当前数据与该索引位置处的数据进行交换。
```

如下图所示，每次遍历到一个元素，随机将当前位置元素和随机索引元素换位置。

![1661444407716](https://pan.baidu.com/wap/assets/1661444407716.png)

代码如下

```
public class Test3 {
    public static void main(String[] args) {
        // 目标：完成随机排名
        // 1、定义一个动态初始化的数组用于存储5名员工的工号
        int[] codes = new int[5];

        // 2、提示用户录入5名员工的工号。
        Scanner sc = new Scanner(System.in);
        for (int i = 0; i &lt; codes.length; i++) {
            // i = 0 1 2 3 4
            System.out.println("请您输入第" + (i + 1) +"个员工的工号：");
            int code = sc.nextInt();
            codes[i] = code;
        }

        // 3、打乱数组中的元素顺序。
        // [12, 33, 54, 26, 8]
        //  i       index
        Random r =  new Random();
        for (int i = 0; i &lt; codes.length; i++) {
            // codes[i]
            // 每遍历到一个数据，都随机一个数组索引范围内的值。
            //然后让当前遍历的数据与该索引位置处的值交换。
            int index = r.nextInt(codes.length); // 0 - 4
            // 定义一个临时变量记住index位置处的值
            int temp = codes[index];
            // 把i位置处的值赋值给index位置处
            codes[index] = codes[i];
            // 把index位置原来的值赋值给i位置处
            codes[i] = temp;
        }

        // 4、遍历数组中的工号输出即可
        for (int i = 0; i &lt; codes.length; i++) {
            System.out.print(codes[i] + " ");
        }
    }
}
```

到这有关数组的常见练习题我们就讲完了，待会我们在给同学们讲一个开发中用得比较多的工具叫做Debug调试。

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Da13e17f43h572d2b4b2b5594fdd7f59f%26expires%3D24h%26dp_logid%3D443671418237770880%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-0NHcYomV1UVRKQNUz3x8eEoTI2Y%25253D%26file_size%3D21677%26timestamp%3D1745903539%26method%3Dinfo%26fid%3D3170504070-250528-900388460159693%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day04-Java%E6%95%B0%E7%BB%84.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday04-Java%E6%95%B0%E7%BB%84%2Fday04-Java%E6%95%B0%E7%BB%84.md&fs_id=900388460159693&size=21677&uk=3170504070&from=yuanguanjia&fsid=900388460159693&clienttype=8&scence=mac_main#%E4%BA%94-debug%E8%B0%83%E8%AF%95%E5%B7%A5%E5%85%B7)五、Debug调试工具

各位同学，为了让大家更好的理解代码的执行流程，这里给大家讲一个在开发中非常重要的工具——叫做Debug调试。

通过Debug调试，我们可以查看代码的执行流程。当你代码中有Bug但是又发现不了的时候，你就可以用Debug调试工具，查看执行流程，逐步分析是哪一行出现了问题。

Debug调试工具的使用步骤如下：

```
第一步：打断点，如下图的红色小圆点
第二步：右键Debug方式启动程序，如下图右键菜单
	  启动后，代码会停留在打断点的这一行
第三步：点击箭头按钮，一行一行往下执行
```

# day05——方法

各位同学，今天我们学习的内容是方法。方法也是Java语言中一个很重要的组成部分，在实际开发中几乎每时每刻都在使用方法。所以对于今天的课程一定要搞清楚。

我们先来学习一下方法是什么

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Dcdf3a2f4bu41dec240c4577597ec87f2%26expires%3D24h%26dp_logid%3D443680584437481592%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-CbOeAXqiHL%25252F3h3%25252FGJ297Fmm6H0Q%25253D%26file_size%3D21318%26timestamp%3D1745903573%26method%3Dinfo%26fid%3D3170504070-250528-297473334833912%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day05-%E6%96%B9%E6%B3%95.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday05-Java%E6%96%B9%E6%B3%95%2Fday05-%E6%96%B9%E6%B3%95.md&fs_id=297473334833912&size=21318&uk=3170504070&from=yuanguanjia&fsid=297473334833912&clienttype=8&scence=mac_main#%E4%B8%80-%E6%96%B9%E6%B3%95%E6%A6%82%E8%BF%B0)一、方法概述

**1.1 方法是什么**

**方法是一种语法结构，它可以把一段代码封装成一个功能，以便重复调用。**这句话什么意思呢？意思是，把一段功能代码围在一起，别人都可以来调用它。

下图是方法的完整格式

![1661667297650](https://pan.baidu.com/wap/assets/1661667297650.png)

我们看一个需求，比如现在张工、李工两个人都需要求两个整数的和。不使用方法，代码如下。

```
// 1、李工。
int a = 10;
int b = 20;
int c = a+b;
System.out.println("和是：" + c);


// 2、张工。
int a1 = 10;
int b1 = 20;
int c1 = a1+b1;
System.out.println("和是：" + c1);
```

阅读上面的代码，我们不难发现。两次求和的代码中，除了求和的数据不一样，代码的组织结构完全一样。

**像这种做相同事情的代码，就可以用方法进行封装**。需要用到这段代码功能时，让别人调用方法就行。代码如下

```
//目标：掌握定义方法的完整格式，搞清楚使用方法的好处。
public class MethodDemo1 {
    public static void main(String[] args) {
        // 需求：假如现在很多程序员都要进行2个整数求和的操作。
        // 1、李工。
        int rs = sum(10, 20);
        System.out.println("和是：" + rs);

        // 2、张工。
        int rs2 = sum(30, 20);
        System.out.println("和是：" + rs2);
    }

    public static int sum(int a,int b) {
        int c = a + b;
        return c;
    }
}
```

**1.2 方法的执行流程**

当调用一个方法时，执行流程，按照下图中标注的序号执行。

​ ① 通过sum方法名找到sum方法

​ ② 把10传递给方法中的参数a

​ ③ 把20传递给方法中的参数b；

​ ④ 执行方法中的代码，此时`int c=a+b;`; 相当于 `int c = 10+20`; c的值为30

​ `return c` 的含义是，把c的结果返回给调用处。 也就是调用sum方法的结果为30,

![1661668878007](https://pan.baidu.com/wap/assets/1661668878007.png)

学习完方法的执行流程之后，下面有几个注意事项需要我们写代码时注意一下。

**1.3 定义方法的注意点**

![1661680196574](https://pan.baidu.com/wap/assets/1661680196574.png)

1. 方法的修饰符：暂时都使用public static 修饰。（目前看做是固定写法，后面是可以改动的）
    
2. 方法申明了具体的返回值类型，内部必须使用return返回对应类型的数据。
    
3. 形参列表可以有多个，甚至可以没有； 如果有多个形参，多个形参必须用“，”隔开，且不能给初始化值。
    

**1.4 使用方法的好处**

最好，我们总结一下，用方法有什么好处，可以归纳为下面2点：

1. 提高了代码的复用性，提高了开发效率。
2. 让程序的逻辑更清晰。

如下图所示：写好一个方法之后，每一个人都可以直接调用，而不用再重复写相同的代码。所以是提高了代码的复用性，不用写重复代码，自然也提高了开发效率。

![1661680445407](https://pan.baidu.com/wap/assets/1661680445407.png)

那么让程序的逻辑更加清晰，是如何体现的呢？ 比如，我们后期会用所学习的技术，做一个ATM系统，ATM系统中有查看账户、存钱、取钱、修改密码等功能，到时候我们可以把每一个功能都写成一个方法。如下图所示，这样程序的逻辑就更加清晰了。

![1661680833652](https://pan.baidu.com/wap/assets/1661680833652.png)

好了，关于方法是什么，以及方法的基本使用就学习到这里。

**总结一下**

```
1.什么是方法？
	答：方法是一种语法结构，它可以把一段代码封装成一个功能，以便重复调用
2.方法的完整格式是什么样的？
	//格式如下：
	修饰符  返回值类型  方法名( 形参列表 ){
    	方法体代码(需要执行的功能代码)
       	return 返回值;
    }
3.方法要执行必须怎么办？
	必须调用才执行; 
	//调用格式:
	方法名(...);

4.使用方法有什么好处？
	答：提高代码的复用性，提高开发效率，使程序逻辑更清晰。
```

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Dcdf3a2f4bu41dec240c4577597ec87f2%26expires%3D24h%26dp_logid%3D443680584437481592%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-CbOeAXqiHL%25252F3h3%25252FGJ297Fmm6H0Q%25253D%26file_size%3D21318%26timestamp%3D1745903573%26method%3Dinfo%26fid%3D3170504070-250528-297473334833912%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day05-%E6%96%B9%E6%B3%95.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday05-Java%E6%96%B9%E6%B3%95%2Fday05-%E6%96%B9%E6%B3%95.md&fs_id=297473334833912&size=21318&uk=3170504070&from=yuanguanjia&fsid=297473334833912&clienttype=8&scence=mac_main#%E4%BA%8C-%E6%96%B9%E6%B3%95%E7%9A%84%E5%85%B6%E4%BB%96%E5%BD%A2%E5%BC%8F)二、方法的其他形式

各位同学，刚才我们学习了定义完整格式的方法。但是实际开发中，需要按照方法解决的实际业务需求，设计出合理的方法形式来解决问题。

实际上设计一个合理的方法，需要重点关注下面两点

![1661685360525](https://pan.baidu.com/wap/assets/1661685360525.png)

![1661685287374](https://pan.baidu.com/wap/assets/1661685287374.png)

设计一个合理的方法的原则如下：

- 如果方法不需要返回数据，返回值类型必须申明成void（无返回值申明）, 此时方法内部不可以使用return返回数据。
- 方法如果不需要接收外部传递进来的数据，则不需要定义形参，且调用方法时也不可以传数据给方法。
- 没有参数，且没有返回值类型（void）的方法，称为值无参数、无返回值方法。此时调用方法时不能传递数据给方法。

接下来我们看几个案例代码，练习根据实际需求定义出合理的方法

**需求1：写一个方法，打印3个"Hello World"**

分析：需求已经非常明确，打印的是3个HelloWorld，在方法中直接循环3次就可以完成需求。不需要外部给方法传递数据，所以不需要参数。

![1661686972979](https://pan.baidu.com/wap/assets/1661686972979.png)

**需求2：写一个方法，打印若干个"Hello World"，具体多少个，有调用者指定**

分析：需求不明确打印HelloWorld的个数，而是需要调用者指定。也就是说，调用者调用方法时需要给方法传递打印HelloWorld的个数。那么定义方法时，就需要写一个参数，来接收调用者传递过来的个数。

![1661687241729](https://pan.baidu.com/wap/assets/1661687241729.png)

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Dcdf3a2f4bu41dec240c4577597ec87f2%26expires%3D24h%26dp_logid%3D443680584437481592%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-CbOeAXqiHL%25252F3h3%25252FGJ297Fmm6H0Q%25253D%26file_size%3D21318%26timestamp%3D1745903573%26method%3Dinfo%26fid%3D3170504070-250528-297473334833912%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day05-%E6%96%B9%E6%B3%95.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday05-Java%E6%96%B9%E6%B3%95%2Fday05-%E6%96%B9%E6%B3%95.md&fs_id=297473334833912&size=21318&uk=3170504070&from=yuanguanjia&fsid=297473334833912&clienttype=8&scence=mac_main#%E4%B8%89-%E6%96%B9%E6%B3%95%E4%BD%BF%E7%94%A8%E5%B8%B8%E8%A7%81%E7%9A%84%E9%97%AE%E9%A2%98)三、方法使用常见的问题

各位同学，自己第一次写方法时，或多或少会可能会出现一些问题。下面把使用方法时，常见的问题整理一下。

目的是让同学们，以后写方法时避免出现这些问题。一旦出现这些问题，要知道是什么原因。

```
- 1. 方法在内种没有先后顺序，但是不能把一个方法定义在另一个方法中。

- 2. 方法的返回值类型写void（无返回申明）时，方法内不能使用return返回数据，
	如果方法的返回值类型写了具体类型，方法内部则必须使用return返回对应类型的数据。

- 3. return语句的下面，不能编写代码，属于无效的代码，执行不到这儿。

- 4. 方法不调用就不会执行,  调用方法时，传给方法的数据，必须严格匹配方法的参数情况。

- 5. 调用有返回值的方法，有3种方式：
     ① 可以定义变量接收结果 
     ② 或者直接输出调用，
     ③ 甚至直接调用；

- 6. 调用无返回值的方法，只有1种方式： 只能直接调用。
```

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Dcdf3a2f4bu41dec240c4577597ec87f2%26expires%3D24h%26dp_logid%3D443680584437481592%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-CbOeAXqiHL%25252F3h3%25252FGJ297Fmm6H0Q%25253D%26file_size%3D21318%26timestamp%3D1745903573%26method%3Dinfo%26fid%3D3170504070-250528-297473334833912%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day05-%E6%96%B9%E6%B3%95.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday05-Java%E6%96%B9%E6%B3%95%2Fday05-%E6%96%B9%E6%B3%95.md&fs_id=297473334833912&size=21318&uk=3170504070&from=yuanguanjia&fsid=297473334833912&clienttype=8&scence=mac_main#%E5%9B%9B-%E6%96%B9%E6%B3%95%E7%9A%84%E6%A1%88%E4%BE%8B)四、方法的案例

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Dcdf3a2f4bu41dec240c4577597ec87f2%26expires%3D24h%26dp_logid%3D443680584437481592%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-CbOeAXqiHL%25252F3h3%25252FGJ297Fmm6H0Q%25253D%26file_size%3D21318%26timestamp%3D1745903573%26method%3Dinfo%26fid%3D3170504070-250528-297473334833912%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day05-%E6%96%B9%E6%B3%95.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday05-Java%E6%96%B9%E6%B3%95%2Fday05-%E6%96%B9%E6%B3%95.md&fs_id=297473334833912&size=21318&uk=3170504070&from=yuanguanjia&fsid=297473334833912&clienttype=8&scence=mac_main#41-%E6%96%B9%E6%B3%95%E6%A1%88%E4%BE%8B1)4.1 方法案例1

![1661687914420](https://pan.baidu.com/wap/assets/1661687914420.png)

按照需求：定义方法如下

```
/*
分析：
	需要求1~n的和，由于n不确定是多少，所以就把n写成形式参数，n的具体值由调用者指定。
	在方法中把n当做一个确定的数据来使用就行。
*/
public static int add(int n){
    int sum = 0;
    for (int i = 1; i &lt;= n; i++) {
        // i = 1 2 3 ... n
        sum += i;
    }
    return sum;
}
```

定义好方法之后，在main方法中调用

```
public static void main(String[] args) {
    int rs = add(5);
    System.out.println("1-5的和是：" + rs); //15
    
    int rs = add(6);
    System.out.println("1-6的和是：" + rs); //21
}
```

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Dcdf3a2f4bu41dec240c4577597ec87f2%26expires%3D24h%26dp_logid%3D443680584437481592%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-CbOeAXqiHL%25252F3h3%25252FGJ297Fmm6H0Q%25253D%26file_size%3D21318%26timestamp%3D1745903573%26method%3Dinfo%26fid%3D3170504070-250528-297473334833912%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day05-%E6%96%B9%E6%B3%95.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday05-Java%E6%96%B9%E6%B3%95%2Fday05-%E6%96%B9%E6%B3%95.md&fs_id=297473334833912&size=21318&uk=3170504070&from=yuanguanjia&fsid=297473334833912&clienttype=8&scence=mac_main#42-%E6%96%B9%E6%B3%95%E6%A1%88%E4%BE%8B2)4.2 方法案例2

![1661687941843](https://pan.baidu.com/wap/assets/1661687941843.png)

按照需求：定义方法如下

```
/*
分析：
	需求中，是要判断一个数是奇数还是偶数，但是并没有明确说，是哪一个数。
	也就是说这个数可能是奇数，也可以能是偶数，是一个能够变化的数。
	把这个数写成方法的形式参数，就可以达到这个目的。因为调用方法时，调用者可以给传递 	 奇数，也可以传递偶数。
*/
public static void judge(int number){
    if(number % 2 == 0){
        System.out.println(number + "是一个偶数！");
    }else {
        System.out.println(number + "是一个奇数！");
    }
}
```

定义好方法之后，在main方法中调用

```
public static void main(String[] args) {
    judge(7); //调用后打印：7是一个奇数
    judge(8); //调用后打印：8是一个偶数
}
```

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Dcdf3a2f4bu41dec240c4577597ec87f2%26expires%3D24h%26dp_logid%3D443680584437481592%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-CbOeAXqiHL%25252F3h3%25252FGJ297Fmm6H0Q%25253D%26file_size%3D21318%26timestamp%3D1745903573%26method%3Dinfo%26fid%3D3170504070-250528-297473334833912%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day05-%E6%96%B9%E6%B3%95.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday05-Java%E6%96%B9%E6%B3%95%2Fday05-%E6%96%B9%E6%B3%95.md&fs_id=297473334833912&size=21318&uk=3170504070&from=yuanguanjia&fsid=297473334833912&clienttype=8&scence=mac_main#%E4%BA%94-%E6%96%B9%E6%B3%95%E5%9C%A8%E8%AE%A1%E7%AE%97%E6%9C%BA%E4%B8%AD%E7%9A%84%E6%89%A7%E8%A1%8C%E5%8E%9F%E7%90%86)五、方法在计算机中的执行原理

各位同学，刚才我们已经写了好几个方法并成功调用了。但是不知道同学们奇不奇怪一个问题。方法在计算机的内存中到底是怎么干的呢？

为了让大家更加深刻的理解方法的执行过程，接下来，给同学们讲一下方法在计算机中的执行原理。理解方法的执行原理，对我们以后知识的学习也是有帮助的。

我们知道Java程序的运行，都是在内存中执行的，而内存区域又分为栈、堆和方法区。那Java的方法是在哪个内存区域中执行呢？

答案是栈内存。 **每次调用方法，方法都会进栈执行；执行完后，又会弹栈出去。**

方法进栈和弹栈的过程，就类似于手枪子弹夹，上子弹和击发子弹的过程。最后上的一颗子弹是，第一个打出来的；第一颗上的子弹，是最后一个打出来的。

![1661689511649](https://pan.baidu.com/wap/assets/1661689511649.png)

假设在main方法中依次调用A方法、B方法、C方法，在内存中的执行流程如下：

- 每次调用方法，方法都会从栈顶压栈执行没执行
- 每个方法执行完后，会从栈顶弹栈出去

![1661692070922](https://pan.baidu.com/wap/assets/1661692070922.png)

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Dcdf3a2f4bu41dec240c4577597ec87f2%26expires%3D24h%26dp_logid%3D443680584437481592%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-CbOeAXqiHL%25252F3h3%25252FGJ297Fmm6H0Q%25253D%26file_size%3D21318%26timestamp%3D1745903573%26method%3Dinfo%26fid%3D3170504070-250528-297473334833912%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day05-%E6%96%B9%E6%B3%95.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday05-Java%E6%96%B9%E6%B3%95%2Fday05-%E6%96%B9%E6%B3%95.md&fs_id=297473334833912&size=21318&uk=3170504070&from=yuanguanjia&fsid=297473334833912&clienttype=8&scence=mac_main#51-%E6%9C%89%E8%BF%94%E5%9B%9E%E5%80%BC%E7%9A%84%E6%96%B9%E6%B3%95%E5%86%85%E5%AD%98%E5%88%86%E6%9E%90)5.1 有返回值的方法，内存分析

下面我们分析一下，求两个整数和的代码，在内存中的执行原理。

```
public class MethodDemo {
    public static void main(String[] args) {
        int rs = sum(10, 20);
        System.out.println(rs);
	}
    public static int sum(int a, int b ){
        int c = a + b; 
        return c;  
    }
}
```

如下图所示：以上代码在内存中的执行过程，按照①②③④⑤⑥⑦的步骤执行.

![1661694127049](https://pan.baidu.com/wap/assets/1661694127049.png)

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Dcdf3a2f4bu41dec240c4577597ec87f2%26expires%3D24h%26dp_logid%3D443680584437481592%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-CbOeAXqiHL%25252F3h3%25252FGJ297Fmm6H0Q%25253D%26file_size%3D21318%26timestamp%3D1745903573%26method%3Dinfo%26fid%3D3170504070-250528-297473334833912%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day05-%E6%96%B9%E6%B3%95.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday05-Java%E6%96%B9%E6%B3%95%2Fday05-%E6%96%B9%E6%B3%95.md&fs_id=297473334833912&size=21318&uk=3170504070&from=yuanguanjia&fsid=297473334833912&clienttype=8&scence=mac_main#52-%E6%97%A0%E8%BF%94%E5%9B%9E%E5%80%BC%E7%9A%84%E6%96%B9%E6%B3%95%E5%86%85%E5%AD%98%E5%88%86%E6%9E%90)5.2 无返回值的方法，内存分析

刚才我们分析的是有有参数有返回值的方法内存原理。下面再分析一个无返回值、无参数的内存原理。

```
public class Demo2Method {
    public static void main(String[] args) {
        study();
    }

    public static void study(){
		eat();
		System.out.println("学习");
		sleep();
	}
    public static void eat(){
        System.out.println("吃饭");
    }
    
    public static void sleep(){
        System.out.println("睡觉");
    }
}
```

![1661696067585](https://pan.baidu.com/wap/assets/1661696067585.png)

**总结一下**

```
1.方法的运行区域在哪里？
	答：栈内存。
	
2.栈有什么特点？方法为什么要在栈中运行自己？
	答：先进后出。保证一个方法调用完另一个方法后，可以回来继续执行。
```

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Dcdf3a2f4bu41dec240c4577597ec87f2%26expires%3D24h%26dp_logid%3D443680584437481592%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-CbOeAXqiHL%25252F3h3%25252FGJ297Fmm6H0Q%25253D%26file_size%3D21318%26timestamp%3D1745903573%26method%3Dinfo%26fid%3D3170504070-250528-297473334833912%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day05-%E6%96%B9%E6%B3%95.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday05-Java%E6%96%B9%E6%B3%95%2Fday05-%E6%96%B9%E6%B3%95.md&fs_id=297473334833912&size=21318&uk=3170504070&from=yuanguanjia&fsid=297473334833912&clienttype=8&scence=mac_main#%E5%85%AD-%E6%96%B9%E6%B3%95%E5%8F%82%E6%95%B0%E7%9A%84%E4%BC%A0%E9%80%92%E6%9C%BA%E5%88%B6)六、方法参数的传递机制

各位同学，刚才我们学习了方法运行的原理，相信大家对方法的运行过程有更加深刻的认识。但是方法参数的传递过程还需要，还需要进一步学习一下。

因为我们刚才演示的一些方法中传递的参数都是基本类型，实际上参数还可以是传递引用类型。接下来，学习一下当参数是基本类型时、和参数是引用类型时的区别。

先记住一个结论：**Java的参数传递机制都是：值传递**

所谓值传递：指的是在传递实参给方法的形参的时候，传递的是实参变量中存储的值的副本。 同学们肯定想知道，形参是什么？实参又是什么呢？ 请看下面这个张图

![1661725157681](https://pan.baidu.com/wap/assets/1661725157681.png)

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Dcdf3a2f4bu41dec240c4577597ec87f2%26expires%3D24h%26dp_logid%3D443680584437481592%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-CbOeAXqiHL%25252F3h3%25252FGJ297Fmm6H0Q%25253D%26file_size%3D21318%26timestamp%3D1745903573%26method%3Dinfo%26fid%3D3170504070-250528-297473334833912%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day05-%E6%96%B9%E6%B3%95.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday05-Java%E6%96%B9%E6%B3%95%2Fday05-%E6%96%B9%E6%B3%95.md&fs_id=297473334833912&size=21318&uk=3170504070&from=yuanguanjia&fsid=297473334833912&clienttype=8&scence=mac_main#61-%E5%8F%82%E6%95%B0%E4%BC%A0%E9%80%92%E7%9A%84%E5%9F%BA%E6%9C%AC%E7%B1%BB%E5%9E%8B%E6%95%B0%E6%8D%AE)6.1 参数传递的基本类型数据

接下来，看一下方法参数传递是基本类型数据时，内存中是怎么执行的。

![1661725470322](https://pan.baidu.com/wap/assets/1661725470322.png)

我们把参数传递的结论再复习一下：**Java的参数传递机制都是：值传递，传递的是实参存储的值的副本。**

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Dcdf3a2f4bu41dec240c4577597ec87f2%26expires%3D24h%26dp_logid%3D443680584437481592%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-CbOeAXqiHL%25252F3h3%25252FGJ297Fmm6H0Q%25253D%26file_size%3D21318%26timestamp%3D1745903573%26method%3Dinfo%26fid%3D3170504070-250528-297473334833912%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day05-%E6%96%B9%E6%B3%95.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday05-Java%E6%96%B9%E6%B3%95%2Fday05-%E6%96%B9%E6%B3%95.md&fs_id=297473334833912&size=21318&uk=3170504070&from=yuanguanjia&fsid=297473334833912&clienttype=8&scence=mac_main#63-%E5%8F%82%E6%95%B0%E4%BC%A0%E9%80%92%E7%9A%84%E6%98%AF%E5%BC%95%E7%94%A8%E6%95%B0%E6%8D%AE%E7%B1%BB%E5%9E%8B)6.3 参数传递的是引用数据类型

接下来，看一下方法的参数是引用类型的数据时，内存中是怎么执行的。

![1661728059814](https://pan.baidu.com/wap/assets/1661728059814.png)

我们发现调用change方法时参数是引用类型，**实际上也是值传递，只不过参数传递存储的地址值**。此时change方法和main方法中两个方法中各自有一个变量arrs，这两个变量记录的是同一个地址值[I@4c873330，change方法把数组中的元素改了，main方法在访问时，元素已经被修改了。

**总结一下：**

```
1.基本类型和引用类型的参数在传递的时候有什么不同？
	= 都是值传递
	- 基本类型的参数传递存储的数据值。
    - 引用类型的参数传递存储的地址值。
```

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Dcdf3a2f4bu41dec240c4577597ec87f2%26expires%3D24h%26dp_logid%3D443680584437481592%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-CbOeAXqiHL%25252F3h3%25252FGJ297Fmm6H0Q%25253D%26file_size%3D21318%26timestamp%3D1745903573%26method%3Dinfo%26fid%3D3170504070-250528-297473334833912%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day05-%E6%96%B9%E6%B3%95.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday05-Java%E6%96%B9%E6%B3%95%2Fday05-%E6%96%B9%E6%B3%95.md&fs_id=297473334833912&size=21318&uk=3170504070&from=yuanguanjia&fsid=297473334833912&clienttype=8&scence=mac_main#%E4%B8%83-%E6%96%B9%E6%B3%95%E5%8F%82%E6%95%B0%E4%BC%A0%E9%80%92%E6%A1%88%E4%BE%8B)七、方法参数传递案例

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Dcdf3a2f4bu41dec240c4577597ec87f2%26expires%3D24h%26dp_logid%3D443680584437481592%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-CbOeAXqiHL%25252F3h3%25252FGJ297Fmm6H0Q%25253D%26file_size%3D21318%26timestamp%3D1745903573%26method%3Dinfo%26fid%3D3170504070-250528-297473334833912%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day05-%E6%96%B9%E6%B3%95.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday05-Java%E6%96%B9%E6%B3%95%2Fday05-%E6%96%B9%E6%B3%95.md&fs_id=297473334833912&size=21318&uk=3170504070&from=yuanguanjia&fsid=297473334833912&clienttype=8&scence=mac_main#71-%E6%96%B9%E6%B3%95%E5%8F%82%E6%95%B0%E4%BC%A0%E9%80%92%E6%A1%88%E4%BE%8B1)7.1 方法参数传递案例1

```
需求：输出一个int类型的数组内容，要求输出格式为：[11, 22, 33, 44, 55]。

分析：
	 1.方法是否需要接收数据进行处理？
	 	方法要打印int类型数组中的元素，打印哪一个数组需求并不明确；
        所以可以把int数组写成参数，让调用者指定
        
	 2.方法是否需要返回数据？
	 	方法最终的目的知识打印数组中的元素。
	 	不需要给调用者返回什么，所以不需要返回值，返回值类型写void
	 
	 3.方法内部的业务：遍历数组，并输出相应的内容
```

代码如下

```
public class MethodTest3 {
    public static void main(String[] args) {
        // 目标：完成打印int类型的数组内容。
        int[] arr = {10, 30, 50, 70};
        printArray(arr);

        int[] arr2 = null;
        printArray(arr2);

        int[] arr3 = {};
        printArray(arr3);
    }

    /*
    	参数：int[] arr表示要被打印元素的数组，需要调用者传递
    */
    public static void printArray(int[] arr){
        if(arr == null){
            System.out.println(arr); // null
            return; // 跳出当前方法
        }

        System.out.print("[");
        // 直接遍历接到的数组元素
        for (int i = 0; i &lt; arr.length; i++) {
            if(i == arr.length - 1){
                System.out.print(arr[i]);
            }else {
                System.out.print(arr[i] + ", ");
            }
        }
        System.out.println("]");
    }
}
```

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Dcdf3a2f4bu41dec240c4577597ec87f2%26expires%3D24h%26dp_logid%3D443680584437481592%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-CbOeAXqiHL%25252F3h3%25252FGJ297Fmm6H0Q%25253D%26file_size%3D21318%26timestamp%3D1745903573%26method%3Dinfo%26fid%3D3170504070-250528-297473334833912%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day05-%E6%96%B9%E6%B3%95.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday05-Java%E6%96%B9%E6%B3%95%2Fday05-%E6%96%B9%E6%B3%95.md&fs_id=297473334833912&size=21318&uk=3170504070&from=yuanguanjia&fsid=297473334833912&clienttype=8&scence=mac_main#72-%E6%96%B9%E6%B3%95%E5%8F%82%E6%95%B0%E4%BC%A0%E9%80%92%E6%A1%88%E4%BE%8B2)7.2 方法参数传递案例2

```
需求：比较两个int类型的数组是否一样，返回true或者false

分析：
	1.方法是否需要接收数据进行处理？
		因为，方法中需要两个int数组比较，但是需求并不明确是哪两个数组；
		所以，需要接收两个int类型的数组，形参声明为：int[] arr1，int[] arr2 

 	2.方法是否需要返回数据？
 		因为,方法最终的结果需要true或者false;
		所以，返回值类型是boolean
 		
	3. 方法内部的业务：判断两个数组内容是否一样。
```

代码如下

```
public class MethodTest4 {
    public static void main(String[] args) {
        // 目标：完成判断两个int类型的数组是否一样。
        int[] arr1 = {10, 20, 30};
        int[] arr2 = {10, 20, 30};
        System.out.println(equals(arr1, arr2));
    }

    /*
    	参数：
    		int[] arr1, 参与比较的第一个int数组
    		int[] arr2  参与比较的第二个int数组
    	返回值:
    		返回比较的结果true或者false
    */
    public static boolean equals(int[] arr1, int[] arr2){
        // 1、判断arr1和arr2是否都是null.
        if(arr1 == null && arr2 == null){
            return true; // 相等的
        }

        // 2、判断arr1是null，或者arr2是null.
        if(arr1 == null || arr2 == null) {
            return false; // 不相等
        }

        // 3、判断2个数组的长度是否一样，如果长度不一样，直接返回false.
        if(arr1.length != arr2.length){
            return false; // 不相等
        }

        // 4、两个数组的长度是一样的，接着比较它们的内容是否一样。
        // arr1 = [10, 20, 30]
        // arr2 = [10, 20, 30]
        for (int i = 0; i &lt; arr1.length; i++) {
            // 判断当前位置2个数组的元素是否不一样，不一样直接返回false
            if(arr1[i] != arr2[i]){
                return false; // 不相等的
            }
        }
        return true; // 两个数组是一样的。
    }
}

```

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Dcdf3a2f4bu41dec240c4577597ec87f2%26expires%3D24h%26dp_logid%3D443680584437481592%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-CbOeAXqiHL%25252F3h3%25252FGJ297Fmm6H0Q%25253D%26file_size%3D21318%26timestamp%3D1745903573%26method%3Dinfo%26fid%3D3170504070-250528-297473334833912%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day05-%E6%96%B9%E6%B3%95.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday05-Java%E6%96%B9%E6%B3%95%2Fday05-%E6%96%B9%E6%B3%95.md&fs_id=297473334833912&size=21318&uk=3170504070&from=yuanguanjia&fsid=297473334833912&clienttype=8&scence=mac_main#%E5%85%AB-%E6%96%B9%E6%B3%95%E9%87%8D%E8%BD%BD)八、方法重载

接下来，我们学习一个开发中很重要的一个方法的形式——叫方法重载。

所谓方法重载指的是：一个类中，出现多个相同的方法名，但是它们的形参列表是不同的，那么这些方法就称为方法重载了。

我们在这里要能够认识，哪些是重载的方法。

下面案例中有多个test方法，但是参数列表都不一样，它们都是重载的方法。调用时只需要通过参数来区分即可。

```
public class MethodOverLoadDemo1 {
    public static void main(String[] args) {
        // 目标：认识方法重载，并掌握其应用场景。
        test();
        test(100);
    }

    public static void test(){
        System.out.println("===test1===");
    }

    public static void test(int a){
        System.out.println("===test2===" + a);
    }

    void test(double a){

    }

    void test(double a, int b){
    }

    void test(int b, double a){
    }

    int test(int a, int b){
        return a + b;
    }
}
```

我们认识了方法重载，那么方法重载有哪些应用场景呢？

一般在开发中，我们经常需要为处理一类业务，提供多种解决方案，此时用方法重载来设计是很专业的。

比如，我们现在看一个案例

```
需求：开发武器系统，功能需求如下：
    可以默认发一枚武器。
    可以指定地区发射一枚武器。
    可以指定地区发射多枚武器。

```

上面的几个需求中，不管以什么样的方式发武器，其实最终的目的都是发武器。

所以我们可以设计几个名称相同的方法，这样调用者调用起来就不用记那么多名字了

代码如下：

```
public class MethodTest2 {
    public static void main(String[] args) {
        // 目标：掌握方法重载的应用场景。
        fire();
        fire("岛国2");
        fire("米国", 999);
    }

    public static void fire(){
        fire("岛国");
    }

    public static void fire(String country){
        fire(country, 1);
    }

    public static void fire(String country, int number){
        System.out.println("发射了" + number + "枚武器给" + country);
    }
}
```

**总结一下：**

```
1.什么是方法重载？
	答：一个类中，多个方法的名称相同，但它们形参列表不同。
2.方法重载需要注意什么？
	- 一个类中，只要一些方法的名称相同、形参列表不同，那么它们就是方法重载了，
	  其它的都不管（如：修饰符，返回值类型是否一样都无所谓）。
	
	- 形参列表不同指的是：形参的个数、类型、顺序不同，不关心形参的名称。
	
3、方法重载有啥应用场景？
	答：开发中我们经常需要为处理一类业务，提供多种解决方案，此时用方法重载来设计是很	专业的。
```

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Dcdf3a2f4bu41dec240c4577597ec87f2%26expires%3D24h%26dp_logid%3D443680584437481592%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-CbOeAXqiHL%25252F3h3%25252FGJ297Fmm6H0Q%25253D%26file_size%3D21318%26timestamp%3D1745903573%26method%3Dinfo%26fid%3D3170504070-250528-297473334833912%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day05-%E6%96%B9%E6%B3%95.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday05-Java%E6%96%B9%E6%B3%95%2Fday05-%E6%96%B9%E6%B3%95.md&fs_id=297473334833912&size=21318&uk=3170504070&from=yuanguanjia&fsid=297473334833912&clienttype=8&scence=mac_main#%E4%B9%9D-return%E5%8D%95%E7%8B%AC%E4%BD%BF%E7%94%A8)九、return单独使用

各位同学，关于方法的定义，我们还剩下最后一种特殊用法，就是在方法中单独使用return语句，可以用来提前结束方法的执行。

如，下面的chu方法中，当除数为0时，就提前结束方法的执行。

```
public class Test {
    public static void main(String[] args) {
        System.out.println("开始");
        chu(10 , 0);
        System.out.println("结束");
    }
    
    public static void chu(int a , int b){
        if(b == 0){
            System.err.println(“您的数据有误！！不执行！！”);
            return; // 直接跳出并结束当前chu方法的执行
        }
        int c = a / b;
        System.out.println("除法结果是："+c); 
    }
}
```


# day06——Java编程案例（专题）

各位同学，前面我们已经学习过很多Java的基础知识了，主要有**变量、数组、运算符、流程控制、方法等**。但是对于这些知识点的运用，掌握得还不是很熟练，所以今天我们专门花一天时间，给同学们讲几个专项练习题，把前面所学习的知识巩固一下。

同时通过这些专项练习题，**积攒大家的代码量，以便提升大家的编程能力和编程思维**。这里所说的编程思维就是使用Java技术解决问题的思维方式；编程能力就是按照编程思维编写代码的能力。

想要提升编程思维和编程能力，在这里给同学们一些学习上的建议：

- 编程思维、编程能力不是一朝一夕形成的，需要大量思考，练习和时间的沉淀。
- 具体措施：前期，建议先模仿；后期，自然就能创新了； 勤于练习代码，勤于思考，孰能生巧。

中国的航空母舰、战斗机，这些技术都是先模仿，再创新的，而且的模仿的周期是非常长的。所以同学们在使用Java技术解决问题时，也是先模仿一些特定问题的解决思路，以后遇到同类型的问题，就采用同一种思维模式来做就行。

![1661995636689](https://pan.baidu.com/wap/assets/1661995636689.png)

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D5806795d1s8c0dc82c71c4d405ffed5a%26expires%3D24h%26dp_logid%3D443688099758720577%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-iKFD3oNXQNH0c1Krc%25252FO%25252BCncmQew%25253D%26file_size%3D33040%26timestamp%3D1745903601%26method%3Dinfo%26fid%3D3170504070-250528-415965395079469%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day06-Java%E7%BC%96%E7%A8%8B%E6%A1%88%E4%BE%8B%EF%BC%88%E4%B8%93%E9%A2%98%EF%BC%89.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday06-Java%E7%BC%96%E7%A8%8B%E6%A1%88%E4%BE%8B%EF%BC%88%E4%B8%93%E9%A2%98%EF%BC%89%2Fday06-Java%E7%BC%96%E7%A8%8B%E6%A1%88%E4%BE%8B%EF%BC%88%E4%B8%93%E9%A2%98%EF%BC%89.md&fs_id=415965395079469&size=33040&uk=3170504070&from=yuanguanjia&fsid=415965395079469&clienttype=8&scence=mac_main#%E6%A1%88%E4%BE%8B%E4%B8%80%E4%B9%B0%E9%A3%9E%E6%9C%BA%E7%A5%A8)案例一：买飞机票

各位同学，我们先来学习第一个案例《飞机买票》，先仔细阅读一下案例需求

![1661996140214](https://pan.baidu.com/wap/assets/1661996140214.png)

我们来分析一下，这个需求该如何实现。前面我跟同学们讲过，将来我们去做一些需求，都是一个一个方法来实现的，所以在这里我们也采用方法来编写。

这个方法如何编写呢？采用下面的方式来思考

```
1.首先，考虑方法是否需要接收数据处理？
	阅读需求我们会发现，不同月份、不同原价、不同舱位类型优惠方案都不一样；
	所以，可以将原价、月份、舱位类型写成参数
	
2.接着，考虑方法是否有返回值？
	阅读需求我们发现，最终结果是求当前用户的优惠票价
	所以，可以将优惠票价作为方法的返回值。
	
3.最后，再考虑方法内部的业务逻辑
	先使用if判断月份是旺季还是淡季，然后使用switch分支判断是头等舱还是经济舱，计算		票价
```

代码如下

```
public class Test1 {
    public static void main(String[] args) {
        // 目标：完成买飞机票的案例。
        double price = calculate(1000, 11, "头等舱");
        System.out.println("优惠价是：" + price);
    }

    public static double calculate(double price,int month,String type){
        // 1、判断当前月份是淡季还是旺季
        if(month &gt;= 5 && month &lt;= 10) {
            // 旺季
            // 2、判断仓位类型。
            switch (type){
                case "头等舱":
                    price *= 0.9; // price = price * 0.9;
                    break;
                case "经济舱":
                    price *= 0.85;
                    break;
            }
        }else {
            // 淡季
            switch (type){
                case "头等舱":
                    price *= 0.7; // price = price * 0.7;
                    break;
                case "经济舱":
                    price *= 0.65;
                    break;
            }
        }
        return price;
    }
}
```

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D5806795d1s8c0dc82c71c4d405ffed5a%26expires%3D24h%26dp_logid%3D443688099758720577%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-iKFD3oNXQNH0c1Krc%25252FO%25252BCncmQew%25253D%26file_size%3D33040%26timestamp%3D1745903601%26method%3Dinfo%26fid%3D3170504070-250528-415965395079469%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day06-Java%E7%BC%96%E7%A8%8B%E6%A1%88%E4%BE%8B%EF%BC%88%E4%B8%93%E9%A2%98%EF%BC%89.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday06-Java%E7%BC%96%E7%A8%8B%E6%A1%88%E4%BE%8B%EF%BC%88%E4%B8%93%E9%A2%98%EF%BC%89%2Fday06-Java%E7%BC%96%E7%A8%8B%E6%A1%88%E4%BE%8B%EF%BC%88%E4%B8%93%E9%A2%98%EF%BC%89.md&fs_id=415965395079469&size=33040&uk=3170504070&from=yuanguanjia&fsid=415965395079469&clienttype=8&scence=mac_main#%E6%A1%88%E4%BE%8B%E4%BA%8C%E5%BC%80%E5%8F%91%E9%AA%8C%E8%AF%81%E7%A0%81)案例二：开发验证码

各位同学，接下来，我们学习第二个案例《开发验证码》，同样先阅读一下案例需求

![1661996187012](https://pan.baidu.com/wap/assets/1661996187012.png)

分析一下，需求是要我们开发一个程序，生成指定位数的验证码。考虑到实际工作中生成验证码的功能很多地方都会用到，为了提高代码的复用性，我们还是把生成验证码的功能写成方法比较好。

那生成验证码的方法该怎么写呢？按照下面的三个步骤进行思考

```
1.首先，考虑方法是否需要接收数据处理？
	要求生成指定位数的验证码，到底多少位呢？让调用者传递即可
	所以，需要一个参数，用来表示验证码的位数

2.接着，考虑方法是否需要有返回值？
	该方法的结果，就是为了得到验证码
	所以，返回值就是验证码；

3.最后，再考虑方法内部的业务逻辑
	1)先按照方法接收的验证码位数n,循环n次
	2)每次循环，产生一个字符，可以是数字字符、或者大小写字母字符
	3)定义一个String类型的变量用于记住产生的每位随机字符
```

按照思路，编写代码如下

```
public class Test2 {
    public static void main(String[] args) {
        // 目标：完成生成随机验证码。
        System.out.println(createCode(8));
    }

    public static String createCode(int n){
        //1)先按照方法接收的验证码位数n,循环n次
        Random r = new Random();
        //3)定义一个String类型的变量用于记住产生的每位随机字符
        String code = "";
        for (int i = 1; i &lt;= n; i++) {
            // i = 1 2 3 4 5
            //2)每次循环，产生一个字符，可以是数字字符、或者大小写字母字符
            // 思路：随机一个0 1 2之间的数字出来，0代表随机一个数字字符，1、2代表随机大写字母，小写字母。
            int type = r.nextInt(3); // 0 1 2
            switch (type) {
                case 0:
                    // 随机一个数字字符
                    code += r.nextInt(10); // 0 - 9  code = code + 8
                    break;
                case 1:
                    // 随机一个大写字符 A 65   Z 65+25    (0 - 25) + 65
                    char ch1 = (char) (r.nextInt(26) + 65);
                    code += ch1;
                    break;
                case 2:
                    // 随机一个小写字符 a 97   z 97+25    (0 - 25) + 97
                    char ch2 = (char) (r.nextInt(26) + 97);
                    code += ch2;
                    break;
            }
        }
        return code;
    }
}
```

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D5806795d1s8c0dc82c71c4d405ffed5a%26expires%3D24h%26dp_logid%3D443688099758720577%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-iKFD3oNXQNH0c1Krc%25252FO%25252BCncmQew%25253D%26file_size%3D33040%26timestamp%3D1745903601%26method%3Dinfo%26fid%3D3170504070-250528-415965395079469%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day06-Java%E7%BC%96%E7%A8%8B%E6%A1%88%E4%BE%8B%EF%BC%88%E4%B8%93%E9%A2%98%EF%BC%89.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday06-Java%E7%BC%96%E7%A8%8B%E6%A1%88%E4%BE%8B%EF%BC%88%E4%B8%93%E9%A2%98%EF%BC%89%2Fday06-Java%E7%BC%96%E7%A8%8B%E6%A1%88%E4%BE%8B%EF%BC%88%E4%B8%93%E9%A2%98%EF%BC%89.md&fs_id=415965395079469&size=33040&uk=3170504070&from=yuanguanjia&fsid=415965395079469&clienttype=8&scence=mac_main#%E6%A1%88%E4%BE%8B%E4%B8%89%E8%AF%84%E5%A7%94%E6%89%93%E5%88%86)案例三：评委打分

各位同学，接下来，我们学习第三个案例《评委打分》，同样先阅读一下案例需求

![1661996204673](https://pan.baidu.com/wap/assets/1661996204673.png)我们把上面的需求还是用方法来编写。

```
1.首先，考虑方法是否需要接收数据来处理？
	需求中说，有多个评委的打分，但是到底多少个评委呢？ 可以由调用者传递
	所以，我们可以把评委的个数写成参数；

2.接着，考虑方法是否需要有返回值？
	需求中，想要的最终结果是平均分
	所以，返回值就是平均分；

3.最后，再考虑方法内部的业务逻辑
	1)假设评委的个位为n个，那么就需要n个评委的分数，首先可以新建一个长度为n的数组，		用来存储每一个评委的分数
	
	2)循环n次，使用Scanner键盘录入n个1~100范围内的整数，并把整数存储到数组中
	
	3)求数组中元素的总和、最大值、最小值
	
	4)最后再计算平均值； 平均值 = (和-最大值-最小值)/(数组.length-2);
```

代码如下

```
public class Test3 {
    public static void main(String[] args) {
        // 目标：完成评委打分案例。
        System.out.println("当前选手得分是：" + getAverageScore(6));
    }

    public static double getAverageScore(int n){
        // 1、定义一个动态初始化的数组，负责后期存入评委的打分
        int[] scores = new int[n]; // 6
        // scores = [0, 0, 0, 0, 0, 0]

        // 2、遍历数组的每个位置，依次录入评委的分数
        Scanner sc = new Scanner(System.in);
        for (int i = 0; i &lt; scores.length; i++) {
            // i = 0 1 2 3 4 5
            System.out.println("请您录入第"+ (i + 1) +"个评委的分数：");
            int score = sc.nextInt();
            scores[i] = score;
        }

        // 3、从数组中计算出总分，找出最高分，最低分。
        int sum = 0; // 求总分用的变量
        int max = scores[0]; // 求最大值的
        int min = scores[0]; // 求最小值的。

        // 遍历数组找出这些数据的。
        for (int i = 0; i &lt; scores.length; i++) {
            // i = 0 1 2 3 4 5
            int score = scores[i];
            // 求和
            sum += score;
            // 求最大值
            if(score &gt; max){
                max = score;
            }
            // 求最小值
            if(score &lt; min){
                min = score;
            }
        }
        // 4、计算出平均分并返回
        return 1.0 * (sum - min - max) / (number - 2);
    }
}
```

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D5806795d1s8c0dc82c71c4d405ffed5a%26expires%3D24h%26dp_logid%3D443688099758720577%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-iKFD3oNXQNH0c1Krc%25252FO%25252BCncmQew%25253D%26file_size%3D33040%26timestamp%3D1745903601%26method%3Dinfo%26fid%3D3170504070-250528-415965395079469%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day06-Java%E7%BC%96%E7%A8%8B%E6%A1%88%E4%BE%8B%EF%BC%88%E4%B8%93%E9%A2%98%EF%BC%89.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday06-Java%E7%BC%96%E7%A8%8B%E6%A1%88%E4%BE%8B%EF%BC%88%E4%B8%93%E9%A2%98%EF%BC%89%2Fday06-Java%E7%BC%96%E7%A8%8B%E6%A1%88%E4%BE%8B%EF%BC%88%E4%B8%93%E9%A2%98%EF%BC%89.md&fs_id=415965395079469&size=33040&uk=3170504070&from=yuanguanjia&fsid=415965395079469&clienttype=8&scence=mac_main#%E6%A1%88%E4%BE%8B%E5%9B%9B%E6%95%B0%E5%AD%97%E5%8A%A0%E5%AF%86)案例四：数字加密

各位同学，接下来我们学习第四个案例《数字加密》，我们还是先阅读一下案例需求

![1661996239984](https://pan.baidu.com/wap/assets/1661996239984.png)

仔细阅读需求后发现，简答来说该需求要做的事情，就是把一个4位数的整数，经过一系列的加密运算（至于怎么运算，待会再详细分析），得到一个新的整数。

我们还是把这个需求用方法来实现，按照下面的思维模式进行分析

```
1.首先，考虑方法是否需要接收数据处理？
	需要一个4位数，至于是哪一个数，让方法的调用者传递。
	所以，方法的参数，就是这个需要加密的四位数

2.接着，考虑方法是否需要有返回值？
	方法最终的结果是一个加密后的数据
	所以，返回值就表示为加密后的数据。

3.最后，再考虑方法内部的业务逻辑，这里的业务逻辑就是那一系列的加密运算
	1)先要把4位数整数拆分为，4个数字，用一个数组保存起来
	2)再将数组中的每一个元素加5，再对10取余
	3)最后将数组中的元素反转，
	
```

```
public class Test4 {
    public static void main(String[] args) {
        // 目标：完成数字加密程序的开发。
        System.out.println("加密后的结果是：" + encrypt(8346));
    }

    public static String encrypt(int number){
        // number = 1983
        // 1、把这个密码拆分成一个一个的数字，才可以对其进行加密啊。
        int[] numbers = split(number);
        // numbers = [1, 9, 8, 3]

        // 2、遍历这个数组中的每个数字，对其进行加密处理。
        for (int i = 0; i &lt; numbers.length; i++) {
            // i = 0 1 2 3
            numbers[i] = (numbers[i] + 5) % 10;
        }
        // numbers = [6, 4, 3, 8]

        // 3、对数组反转，把对数组进行反转的操作交给一个独立的方法来完成
        reverse(numbers);
        // numbers = [8, 3, 4, 6]

        // 4、把这些加密的数字拼接起来做为加密后的结果返回即可。
        String data = "";
        for (int i = 0; i &lt; numbers.length; i++) {
            data += numbers[i];
        }
        return data;
    }

    public static void reverse(int[] numbers) {
        // 反转数组的
        // numbers = [6, 4, 3, 8]
        //            i        j
        for (int i = 0, j = numbers.length - 1; i &lt; j; i++,j--) {
            // 交换i和j位置处的值。
            // 1、把后一个位置处的值交给一个临时变量先存起来
            int temp = numbers[j];
            // 2、把前一个位置处的值赋值给后一个位置处
            numbers[j] = numbers[i];
            // 3、把后一个位置处原来的值（由临时变量记住着）赋值给前一个位置
            numbers[i] = temp;
        }
    }

    public static int[] split(int number) {
        // number = 1983
        int[] numbers = new int[4];
        numbers[0] = number / 1000;
        numbers[1] = (number / 100) % 10;
        numbers[2] = (number / 10) % 10;
        numbers[3] = number % 10;
        return numbers;
    }
}
```

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D5806795d1s8c0dc82c71c4d405ffed5a%26expires%3D24h%26dp_logid%3D443688099758720577%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-iKFD3oNXQNH0c1Krc%25252FO%25252BCncmQew%25253D%26file_size%3D33040%26timestamp%3D1745903601%26method%3Dinfo%26fid%3D3170504070-250528-415965395079469%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day06-Java%E7%BC%96%E7%A8%8B%E6%A1%88%E4%BE%8B%EF%BC%88%E4%B8%93%E9%A2%98%EF%BC%89.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday06-Java%E7%BC%96%E7%A8%8B%E6%A1%88%E4%BE%8B%EF%BC%88%E4%B8%93%E9%A2%98%EF%BC%89%2Fday06-Java%E7%BC%96%E7%A8%8B%E6%A1%88%E4%BE%8B%EF%BC%88%E4%B8%93%E9%A2%98%EF%BC%89.md&fs_id=415965395079469&size=33040&uk=3170504070&from=yuanguanjia&fsid=415965395079469&clienttype=8&scence=mac_main#%E6%A1%88%E4%BE%8B%E4%BA%94%E6%95%B0%E7%BB%84%E6%8B%B7%E8%B4%9D)案例五：数组拷贝

各位同学，接下来我们学习第五个案例《数组拷贝》，我们还是先阅读一下案例需求

![1661996258614](https://pan.baidu.com/wap/assets/1661996258614.png)

仔细阅读需求发现，想要实现的效果就是：给定一个数组，然后经过我们编写的程序，得到一个和原数组一模一样的数组。

我们也采用一个方法来编写，按照下面的思维模式来思考

```
1.首先，考虑方法是否需要接收数据处理？
	该方法的目的是拷贝数组，拷贝哪一个数组呢？ 需要调用者传递
	所以，参数应该是一个数组

2.接着，考虑方法是否需要有返回值？
	该方法最终想要得到一个新数组
	所以，返回值是拷贝得到的新数组

3.最后，考虑方法内部的业务逻辑？
	1)创建一个新的数组，新数组的长度和元素数组一样
	2)遍历原数组，将原数组中的元素赋值给新数组
	3)最终将新数组返回
```

```
public class Test5 {
    public static void main(String[] args) {
        // 目标：掌握数组拷贝。
        int[] arr = {11, 22, 33};
        int[] arr2 = copy(arr);
        printArray(arr2);

        // 注意：这个不是拷贝数组，叫把数组变量赋值给另一个数组变量。
        //        int[] arr3 = arr;
        //        arr3[1] = 666;
        //        System.out.println(arr[1]);

        arr2[1] = 666;
        System.out.println(arr[1]);
    }

    public static int[] copy(int[] arr){
        // arr = [11, 22, 33]
        //        0    1   2

        // 1、创建一个长度一样的整型数组出来。
        int[] arr2 = new int[arr.length];
        // arr2 = [0, 0, 0]
        //         0  1  2

        // 2、把原数组的元素值对应位置赋值给新数组。
        for (int i = 0; i &lt; arr.length; i++) {
            // i = 0 1 2
            arr2[i] = arr[i];
        }

        return arr2;
    }

    public static void printArray(int[] arr){
        System.out.print("[");
        for (int i = 0; i &lt; arr.length; i++) {
            System.out.print(i==arr.length-1 ? arr[i] : arr[i] + ", ");
        }
        System.out.println("]");
    }
}
```

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D5806795d1s8c0dc82c71c4d405ffed5a%26expires%3D24h%26dp_logid%3D443688099758720577%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-iKFD3oNXQNH0c1Krc%25252FO%25252BCncmQew%25253D%26file_size%3D33040%26timestamp%3D1745903601%26method%3Dinfo%26fid%3D3170504070-250528-415965395079469%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day06-Java%E7%BC%96%E7%A8%8B%E6%A1%88%E4%BE%8B%EF%BC%88%E4%B8%93%E9%A2%98%EF%BC%89.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday06-Java%E7%BC%96%E7%A8%8B%E6%A1%88%E4%BE%8B%EF%BC%88%E4%B8%93%E9%A2%98%EF%BC%89%2Fday06-Java%E7%BC%96%E7%A8%8B%E6%A1%88%E4%BE%8B%EF%BC%88%E4%B8%93%E9%A2%98%EF%BC%89.md&fs_id=415965395079469&size=33040&uk=3170504070&from=yuanguanjia&fsid=415965395079469&clienttype=8&scence=mac_main#%E6%A1%88%E4%BE%8B%E5%85%AD%E6%8A%A2%E7%BA%A2%E5%8C%85)案例六：抢红包

各位同学，接下来我们学习第六个案例《抢红包》，我们还是先阅读一下案例需求

![1661996292796](https://pan.baidu.com/wap/assets/1661996292796.png)

![1662022389872](https://pan.baidu.com/wap/assets/1662022389872.png)

我们还是把这个案例用一个方法来编写，同样按照下面的模式来分析

```
1.首先，考虑方法是否需要接收数据处理？
	需要接收5个红包，至于是哪5个红包，可以有调用者传递；把5个红包的数值，用数组来存	 储。
	所以，参数就是一个数组
	
2.接着，考虑方法是否需要有返回值？
	按照需求的效果，抢完红包就直接打印了，不需要返回值

3.最后，考虑方法内部的业务逻辑是怎么的？
	思考：红包实际上是数组中的元素，抢红包实际上随机获取数组中的元素；而且一个红包只能抢一次，怎么做呢？我们可以把数组中获取到元素的位置，置为0,下次再或者这个位置的元素一判断为0，再重新获取新的元素，依次内推，直到把数组中所有的元素都获取完。
	
	我们我们把抽红包的思路再整理一下：
		1)首先，写一个循环，循环次数为数组的长度
		2)每次循环，键盘录入，提示"用户录入任意键抽奖："
    	3)随机从数组中产生一个索引，获取索引位置的元素，这个元素就表示抽的红包
			如果值不为0，则打印如："恭喜您，您抽中了520元",把这个位置元素置为0
    		如果值为0，则说明这个红包被抽过，重新循环到第2步，重新抽奖
    		【注意：如果当前这一次没有抽中，这一次抽奖机会被浪费掉了，我们可以把控				制循环的次数自减一下】	
```

```
public class Test6 {
    public static void main(String[] args) {
        int[] moneys = {100,999,50,520,1314};
        start(moneys);
    }
    //开始抽奖
    public static void start(int[] moneys){
        //1)首先，写一个循环，循环次数为数组的长度
        for (int i = 0; i &lt; moneys.length; i++) {
            //2)每次循环，键盘录入，提示"用户录入任意键抽奖："
            while (true){
                Scanner sc = new Scanner(System.in);
                System.out.print("用户录入任意键抽奖：");
                String msg = sc.next();
                //3)随机从数组中产生一个索引，获取索引位置的元素，这个元素就表示抽的红包
                Random r = new Random();
                int index = r.nextInt(moneys.length);
                int money = moneys[index];
                if(money!=0){
                    //如果值不为0，则打印如："恭喜您，您抽中了520元"
                    System.out.println("恭喜您，您抽中了"+money+"元");
                    moneys[index] = 0;
                    break;
                }else {
                    //如果值为0，则说明这个红包被抽过，重新循环到第2步，重新抽奖
                    //此时这一次抽奖机会被浪费掉了，可以把控制循环的次数自减一下
                    i--;
                }
            }
        }
    }
}
```

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D5806795d1s8c0dc82c71c4d405ffed5a%26expires%3D24h%26dp_logid%3D443688099758720577%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-iKFD3oNXQNH0c1Krc%25252FO%25252BCncmQew%25253D%26file_size%3D33040%26timestamp%3D1745903601%26method%3Dinfo%26fid%3D3170504070-250528-415965395079469%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day06-Java%E7%BC%96%E7%A8%8B%E6%A1%88%E4%BE%8B%EF%BC%88%E4%B8%93%E9%A2%98%EF%BC%89.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday06-Java%E7%BC%96%E7%A8%8B%E6%A1%88%E4%BE%8B%EF%BC%88%E4%B8%93%E9%A2%98%EF%BC%89%2Fday06-Java%E7%BC%96%E7%A8%8B%E6%A1%88%E4%BE%8B%EF%BC%88%E4%B8%93%E9%A2%98%EF%BC%89.md&fs_id=415965395079469&size=33040&uk=3170504070&from=yuanguanjia&fsid=415965395079469&clienttype=8&scence=mac_main#%E6%A1%88%E4%BE%8B%E4%B8%83%E6%89%BE%E7%B4%A0%E6%95%B0)案例七：找素数

各位同学，接下来我们学习第七个案例《找素数》，我们还是先阅读一下案例需求

![1661996325454](https://pan.baidu.com/wap/assets/1661996325454.png)

首先我们得统一认识一下什么是素数：**只能被1和本身整除的数是素数**，比如：3、7是素数，9,21不是素数（因为9可以被3整除，21可以被3和7整除）

再思考题目需求该怎么做？**打印输出101~200之间的素数，并求有多少个？**，我们也是把这个需求写成一个方法，还是按照三个步骤分析方法如何编写。

```
1.首先，考虑方法是否需要接收数据处理？
	该方法是求一个范围内的素数，一个范围需要两个数据来确定，比如：101~200
	所以，方法需要两个参数来接收范围的开始值start，和范围的结束值end
	
2.接着，考虑方法是否需要返回值？
	该方法需要求一个范围内的素数的个数
	所以，返回值就是素数的个数

3.最后，考虑方法内部的业务逻辑
	思考：怎么判断一个数是素数呢？要仅仅抓住，素数的要求:“只能被1和本身整除的数是素数”。我们可以从反向思考，如果这个数只要能被除了1和本身以外的数整除，那么这个数就不是素数。
	//比如1：判断9是否为素数
	int num = 9;
	boolean flag = true; //规定flag等于true表示num是素数；否则表示num不是素数
	//如果这个数num只要能被除了1和本身以外的数整除，那么这个数就不是素数。
	for(int j=2; j&lt;9-1; j++){
        //当j=3时，num%j == 9%3 == 0; 
		if(num%j==0){
            //说明num=9; 表示一个素数。把flag改为false; 
            flag = false;
		}
	}

	把上面的代码循环执行，每次循环然后把num换成start~end之间的整数即可。
```

编写代码如下

```
public class Test7 {
    public static void main(String[] args) {
        // 目标：完成找素数。
        System.out.println("当前素数的个数是：" + search(101, 200));
    }

    public static int search(int start, int end){
        int count = 0;
        // start = 101   end = 200
        // 1、定义一个for循环找到101到200之间的每个数据
        for (int i = start; i &lt;= end ; i++) {
            // i = 101 102 103 ... 199 200

            // 信号位思想
            boolean flag = true; // 假设的意思：默认当前i记住的数据是素数。
            // 2、判断当前i记住的这个数据是否是素数。
            for (int j = 2; j &lt;= i / 2; j++) {
                if(i % j == 0){
                    // i当前记住的这个数据不是素数了
                    flag = false;
                    break;
                }
            }
            // 3、根据判定的结果决定是否输出i当前记住的数据：是素数才输出展示。
            if(flag){
                System.out.println(i);
                count++;
            }
        }
        return count;
    }
}
```

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D5806795d1s8c0dc82c71c4d405ffed5a%26expires%3D24h%26dp_logid%3D443688099758720577%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-iKFD3oNXQNH0c1Krc%25252FO%25252BCncmQew%25253D%26file_size%3D33040%26timestamp%3D1745903601%26method%3Dinfo%26fid%3D3170504070-250528-415965395079469%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day06-Java%E7%BC%96%E7%A8%8B%E6%A1%88%E4%BE%8B%EF%BC%88%E4%B8%93%E9%A2%98%EF%BC%89.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday06-Java%E7%BC%96%E7%A8%8B%E6%A1%88%E4%BE%8B%EF%BC%88%E4%B8%93%E9%A2%98%EF%BC%89%2Fday06-Java%E7%BC%96%E7%A8%8B%E6%A1%88%E4%BE%8B%EF%BC%88%E4%B8%93%E9%A2%98%EF%BC%89.md&fs_id=415965395079469&size=33040&uk=3170504070&from=yuanguanjia&fsid=415965395079469&clienttype=8&scence=mac_main#%E6%A1%88%E4%BE%8B%E5%85%AB%E6%A8%A1%E6%8B%9F%E5%8F%8C%E8%89%B2%E7%90%83%E6%8B%93%E5%B1%95%E6%A1%88%E4%BE%8B)案例八：模拟双色球[拓展案例]

各位同学，接下来我们学习第八个案例《模拟双色球》，我们还是先阅读一下案例需求

![1661996916834](https://pan.baidu.com/wap/assets/1661996916834.png)

这个案例我们可以采用方法方法来完成

1. 第一个方法，让用户手动投注，产生一注双色球彩票

![1662026373775](https://pan.baidu.com/wap/assets/1662026373775.png)

2. 第二个方法，由系统随机产生一注双色球彩票开奖号码

![1662026388626](https://pan.baidu.com/wap/assets/1662026388626.png)

3. 第三个方法，判断传入两组号码，用于判断彩票的中奖情况

![1662026410363](https://pan.baidu.com/wap/assets/1662026410363.png)

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D5806795d1s8c0dc82c71c4d405ffed5a%26expires%3D24h%26dp_logid%3D443688099758720577%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-iKFD3oNXQNH0c1Krc%25252FO%25252BCncmQew%25253D%26file_size%3D33040%26timestamp%3D1745903601%26method%3Dinfo%26fid%3D3170504070-250528-415965395079469%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day06-Java%E7%BC%96%E7%A8%8B%E6%A1%88%E4%BE%8B%EF%BC%88%E4%B8%93%E9%A2%98%EF%BC%89.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday06-Java%E7%BC%96%E7%A8%8B%E6%A1%88%E4%BE%8B%EF%BC%88%E4%B8%93%E9%A2%98%EF%BC%89%2Fday06-Java%E7%BC%96%E7%A8%8B%E6%A1%88%E4%BE%8B%EF%BC%88%E4%B8%93%E9%A2%98%EF%BC%89.md&fs_id=415965395079469&size=33040&uk=3170504070&from=yuanguanjia&fsid=415965395079469&clienttype=8&scence=mac_main#81-%E6%89%8B%E5%8A%A8%E6%8A%95%E6%B3%A8)8.1 手动投注

编写一个方法，让用户手动投注，产生一注双色球彩票，思路分析

```
1.首先，考虑方法是否需要接收数据处理？
	双色球彩票的规则非常明确，没有什么数据需要传递给方法。
	所以，不需要参数

2.接着，考虑方法是否需要返回值？
	方法最终的结果是需要一注双色球彩票的号码，一注彩票有7个号码，可以用一个数组来存
	所以，返回值是一个数组

3.最后，考虑方法内部的业务逻辑怎么编写？
	1)首先需要准备一个int类型数组，长度为7; 用于存储产生的投注号码
	2)循环遍历数组的前6个元素，采用键盘录入的方式，给前区6个红球赋值
		要求录入的整数在1~33范围内，同时录入的整数在数组中不能已存在，否则重新录入
	3)最后再录入一个整数，给后区一个蓝球赋值
		要求整数必须在1~16范围内
```

- 手动投注代码如下

```
/** 1、设计一个方法，用于让用户投注一组号码并返回（前6个是红球号码，最后1个是蓝球号码 ）*/
public static int[] userSelectNumbers(){
    // 2、创建一个整型数组，用于存储用户投注的7个号码（前6个是红球号码，最后1个是蓝球号码 ）
    int[] numbers =  new int[7];
    // numbers = [0, 0, 0, 0, 0, 0, 0]
    //            0  1  2  3  4  5  6

    Scanner sc = new Scanner(System.in);
    // 3、遍历前6个位置，让用户依次投注6个红球号码，存入
    for (int i = 0; i &lt; numbers.length - 1; i++) {
        // i = 0 1 2 3 4 5

        while (true) {
            // 4、开始让用户为当前位置投注一个红球号码（1-33之间，不能重复）
            System.out.println("请您输入第" + (i + 1) + "个红球号码（1-33之间，不能重复）：");
            int number = sc.nextInt();

            // 5、先判断用户输入的红球号码是否在1-33之间
            if(number &lt; 1 || number &gt; 33){
                System.out.println("对不起，您输入的红球号码不在1-33之间，请确认！");
            }else {
                // 号码是在1-33之间了，接着还要继续判断这个号码是否重复，不重复才可以使用。
                if(exist(numbers, number)){
                    // number当前这个红球号码是重复了。
                    System.out.println("对不起，您当前输入的红球号码前面选择过，重复了，请确认！");
                }else {
                    // number记住的这个号码没有重复了，就可以使用了。
                    numbers[i] = number;
                    break; // 结束当次投注，结束了当前死循环。
                }
            }
        }
    }

    // 6、投注最后一个蓝球号码。
    while (true) {
        System.out.println("请您输入最后1个蓝球号码（1-16）：");
        int number = sc.nextInt();
        if(number &lt; 1 || number &gt; 16){
            System.out.println("对不起，您输入的蓝球号码范围不对！");
        }else {
            numbers[6] = number;
            break; // 蓝球号码录入成功，结束死循环
        }
    }

    return numbers;
}
```

每键盘录入一个号码，需要判断这个号码在数组中是否存在，存在返回true；不存在返回false

```
private static boolean exist(int[] numbers, int number) {
    // 需求：判断number这个数字是否在numbers数组中存在。
    // numbers = [12, 25, 18, 0, 0, 0, 0]
    // number = 12
    for (int i = 0; i &lt; numbers.length; i++) {
        if(numbers[i] == 0){
            break;
        }
        if(numbers[i] == number){
            return true;
        }
    }
    return false;
}
```

为了打印一注彩票的号码（数组中的元素），把打印数组中的元素也写成方法。

```
public static void printArray(int[] arr) {
    System.out.print("[");
    for (int i = 0; i &lt; arr.length; i++) {
        System.out.print(i == arr.length - 1 ? arr[i] : arr[i] + ", ");
    }
    System.out.println("]");
}
```

在main方法中测试，运行看能不能产生一注彩票号码

```
public class Test8 {
    public static void main(String[] args) {
        // 目标：完成双色球系统的开发。
        int[] userNumbers = userSelectNumbers();
        System.out.println("您投注的号码：");
        printArray(userNumbers);
    }
}
```

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D5806795d1s8c0dc82c71c4d405ffed5a%26expires%3D24h%26dp_logid%3D443688099758720577%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-iKFD3oNXQNH0c1Krc%25252FO%25252BCncmQew%25253D%26file_size%3D33040%26timestamp%3D1745903601%26method%3Dinfo%26fid%3D3170504070-250528-415965395079469%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day06-Java%E7%BC%96%E7%A8%8B%E6%A1%88%E4%BE%8B%EF%BC%88%E4%B8%93%E9%A2%98%EF%BC%89.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday06-Java%E7%BC%96%E7%A8%8B%E6%A1%88%E4%BE%8B%EF%BC%88%E4%B8%93%E9%A2%98%EF%BC%89%2Fday06-Java%E7%BC%96%E7%A8%8B%E6%A1%88%E4%BE%8B%EF%BC%88%E4%B8%93%E9%A2%98%EF%BC%89.md&fs_id=415965395079469&size=33040&uk=3170504070&from=yuanguanjia&fsid=415965395079469&clienttype=8&scence=mac_main#82-%E9%9A%8F%E6%9C%BA%E5%BC%80%E5%A5%96%E5%8F%B7%E7%A0%81)8.2 随机开奖号码

编写一个方法，让用户自动机选投注，产生一注双色球彩票，思路分析

```
1.首先，考虑方法是否需要接收数据处理？
	双色球彩票的规则非常明确，没有什么数据需要传递给方法。
	所以，不需要参数

2.接着，考虑方法是否需要返回值？
	方法最终的结果是需要一注双色球彩票的号码，一注彩票有7个号码，可以用一个数组来存
	所以，返回值是一个数组

3.最后，考虑方法内部的业务逻辑怎么编写？
	1)首先需要准备一个int类型数组，长度为7; 用于存储产生的投注号码
	2)循环遍历数组的前6个元素，采用生成随机数的的方式，给前区6个红球赋值
		要求生成的随机数在1~33范围内，同时随机的整数数组中不能已存在，否则重新生产
	3)最后再随机一个整数，给后区一个蓝球赋值
		要求随机整数必须在1~16范围内
```

机选号码，代码如下

```
/** 2、设计一个方法：随机一组中奖号码出来（6个红球号码，1个蓝球号码 ）*/
public static int[] createLuckNumbers(){
    // 1、创建一个整型数组，用于存储这7个号码
    int[] numbers = new int[7];

    Random r  = new Random();
    // 2、遍历前6个位置处，依次随机一个红球号码存入（1-33 不重复）
    for (int i = 0; i &lt; numbers.length - 1; i++) {
        // i = 0 1 2 3 4 5
        while (true) {
            // 3、为当前这个位置随机一个红球号码出来存入。
            //1 - 33 ==&gt; -1 ===&gt; (0 , 32) + 1
            int number = r.nextInt(33) + 1;

            // 4、判断这个号码是否之前出现过（红球号码不能重复）。
            if(!exist(numbers, number)){
                // number不重复。
                numbers[i] = number;
                //结束死循环，代表找到了当前这个位置的一个不重复的红球号码了。
                break; 
            }
        }
    }

    // 3、录入一个蓝球号码。 1-16
    numbers[6] = r.nextInt(16) + 1;
    return numbers;
}
```

在main方法中测试，看是否能够产生一注彩票

```
public class Test8 {
    public static void main(String[] args) {
        // 目标：完成双色球系统的开发。
        //用户手动投注
        int[] userNumbers = userSelectNumbers();
        System.out.println("您投注的号码：");
        printArray(userNumbers);
        
        //生成中奖号码
        int[] luckNumbers = createLuckNumbers();
        System.out.println("中奖的号码：");
        printArray(luckNumbers);
    }
}
```

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D5806795d1s8c0dc82c71c4d405ffed5a%26expires%3D24h%26dp_logid%3D443688099758720577%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-iKFD3oNXQNH0c1Krc%25252FO%25252BCncmQew%25253D%26file_size%3D33040%26timestamp%3D1745903601%26method%3Dinfo%26fid%3D3170504070-250528-415965395079469%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day06-Java%E7%BC%96%E7%A8%8B%E6%A1%88%E4%BE%8B%EF%BC%88%E4%B8%93%E9%A2%98%EF%BC%89.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday06-Java%E7%BC%96%E7%A8%8B%E6%A1%88%E4%BE%8B%EF%BC%88%E4%B8%93%E9%A2%98%EF%BC%89%2Fday06-Java%E7%BC%96%E7%A8%8B%E6%A1%88%E4%BE%8B%EF%BC%88%E4%B8%93%E9%A2%98%EF%BC%89.md&fs_id=415965395079469&size=33040&uk=3170504070&from=yuanguanjia&fsid=415965395079469&clienttype=8&scence=mac_main#83-%E5%88%A4%E6%96%AD%E6%98%AF%E5%90%A6%E4%B8%AD%E5%A5%96)8.3 判断是否中奖

编写一个方法，判断用户的彩票号码是否中奖，具体中奖规则如下

- 6个红球+1个蓝球 ，奖金1000万
    
- 6个红球+0个蓝球，奖金500万
    
- 5个红球+1个蓝球，奖金3000块
    
- 5个红球+0个蓝球，或者4个红球+1个蓝球，奖金200块
    
- 4个红球+0个蓝球，或者3个红球+1个蓝球，奖金10块
    
- 小于3个红球+1个蓝球，奖金5块
    
- 如果前面的都不成立，就中奖，算你为福利事业做贡献了。
    

编写方法的思路如下

```
1.首先，考虑方法是否需要接收数据处理？
	判断彩票是否中奖，需要有两组号码；一组号码是彩票号码，一组号码是开奖号码
	所以，参数需要有两个数组

2.接着，考虑方法是否需要返回值？
	方法不需要返回结果，中了奖，直接将奖项打印输出就行了。
	【注意：这只是提供一种代码的编写方案，你将中奖的金额返回也行】

3.最后，考虑方法内部的业务逻辑怎么编写？
	1)定义两个变量redCount和blueCount用来记录，红球的个数和蓝球的个数
	2)遍历两个数组中前6个元素(红球)，判断两个数组中有没有相同元素
		如果找到一个相同元素，则redCount++
    3)比较两个数组中最后一个元素(蓝球)是否相同
    	如果相同，则blueCount++
	4)根据红球和蓝球的命中个数，打印输出对应的奖项
```

代码如下

```
/** 3、设计一个方法，用于判断用户的中奖情况 */
public static void judge(int[] userNumbers,int[] luckNumbers){
    // userNumbers = [12, 14, 16, 18, 23, 26, 8]
    // luckNumbers = [16, 17, 18, 19, 26, 32, 8]

    // 2、分别定义2个变量用于记住红球命中了几个以及蓝球命中了几个
    int redCount = 0;
    int blueCount = 0;

    // 先判断红球命中的数量。
    // 遍历用户投注的号码的前6个红球
    for (int i = 0; i &lt; userNumbers.length - 1; i++) {
        // userNumbers[i]
        // 开始遍历中奖号码的前6个红球号码，看用户当前选择的这个号码是否命中了
        for (int j = 0; j &lt; luckNumbers.length - 1; j++) {
            if(userNumbers[i] == luckNumbers[j]){
                redCount++;
                break;
            }
        }
    }

    // 3、判断蓝球是否命中了
    blueCount = userNumbers[6] == luckNumbers[6] ? 1 : 0;

    System.out.println("您命中的红球数量是：" + redCount);
    System.out.println("您命中的蓝球数量是：" + blueCount);

    // 4、判断中奖详情，并输出结果
    if(redCount == 6 && blueCount == 1){
        System.out.println("恭喜您，中奖1000万，可以开始享受人生了~~~");
    }else if(redCount == 6 && blueCount == 0){
        System.out.println("恭喜您，中奖500万，可以稍微开始享受人生了~~~");
    }else if(redCount == 5 && blueCount == 1){
        System.out.println("恭喜您，中奖3000元，可以出去吃顿小龙虾了~");
    }else if(redCount == 5 && blueCount == 0 || redCount == 4 && blueCount == 1){
        System.out.println("恭喜您，中了小奖：200元~");
    }else if(redCount == 4 && blueCount == 0 || redCount == 3 && blueCount == 1){
        System.out.println("中了10元~");
    }else if( redCount &lt; 3 && blueCount == 1){
        System.out.println("中了5元~");
    }else {
        System.out.println("感谢您对福利事业做出的巨大贡献~~~");
    }
}
```

在main方法中测试，检测是否中奖的方法是否正确

```
public class Test8 {
    public static void main(String[] args) {
        // 目标：完成双色球系统的开发。
        //用户投注
        int[] userNumbers = userSelectNumbers();
        System.out.println("您投注的号码：");
        printArray(userNumbers);
		
        //随机产生一个中奖号码
        int[] luckNumbers = createLuckNumbers();
        System.out.println("中奖的号码：");
        printArray(luckNumbers);

        //判断用户投注的号码是否中奖
        judge(userNumbers, luckNumbers);
    }
}
```

# Day7
接下来，我们要学习的是Java中最核心的课程——**面向对象编程**。

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Dacb70693aqcaa2ebdce65a05afd0ed54%26expires%3D24h%26dp_logid%3D443696390879258317%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-M6UpRuIuNhAgR%25252BHtFoVwq%25252Bk7kSI%25253D%26file_size%3D23921%26timestamp%3D1745903632%26method%3Dinfo%26fid%3D3170504070-250528-195455261105656%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80%2Fday07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80.md&fs_id=195455261105656&size=23921&uk=3170504070&from=yuanguanjia&fsid=195455261105656&clienttype=8&scence=mac_main#%E4%B8%80-%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%85%A5%E9%97%A8)一、面向对象入门

各位同学，为什么说面向对象是Java最核心的课程呢？因为写Java程序是有套路的，而面向对象就是写Java程序的套路；你如果不知道面向对象编程，那么你Java语言就算白学了。

那这种编程套路是咋回事呢？ 接下来，我们通过一个案例快速的认识一下。

现在假设我们需要处理的是学生的姓名、语文成绩、数学成绩这三个数据，要求打印输出这个学生的总成绩，和平均成绩。

![1662209848898](https://pan.baidu.com/wap/assets/1662209848898.png)

遇到这样的需求，我们以前都会定义方法来做，如下图所示

注意：这里每一个方法有**三个参数**

![1662209886046](https://pan.baidu.com/wap/assets/1662209886046.png)

![1662209899008](https://pan.baidu.com/wap/assets/1662209899008.png)

定义好方法之后，我们调用方法的时候，需要给每一个方法**传递三个实际参数**

![1662210110729](https://pan.baidu.com/wap/assets/1662210110729.png)

在上面案例中，这种编程方式是一种面向过程的编程方式。所谓面向过程，就是编写一个的方法，有数据要进行处理就交给方法来处理。

但是实际上**姓名、语文成绩、数学成绩三个数据可以放在一起，组合成一个对象**，然后让对象提供方法对自己的数据进行处理。这种方式称之为面向对象编程。

![1662210587156](https://pan.baidu.com/wap/assets/1662210587156.png)

**总结一些：所谓编写对象编程，就是把要处理的数据交给对象，让对象来处理。**

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Dacb70693aqcaa2ebdce65a05afd0ed54%26expires%3D24h%26dp_logid%3D443696390879258317%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-M6UpRuIuNhAgR%25252BHtFoVwq%25252Bk7kSI%25253D%26file_size%3D23921%26timestamp%3D1745903632%26method%3Dinfo%26fid%3D3170504070-250528-195455261105656%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80%2Fday07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80.md&fs_id=195455261105656&size=23921&uk=3170504070&from=yuanguanjia&fsid=195455261105656&clienttype=8&scence=mac_main#%E4%BA%8C-%E6%B7%B1%E5%88%BB%E8%AE%A4%E8%AF%86%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1)二、深刻认识面向对象

好的各位同学，在上一节课我们已经用面向对象的编程套路，处理了学生数据。接下来我们就要搞清楚，面向对象的几个最核心问题了。

![1662211382446](https://pan.baidu.com/wap/assets/1662211382446.png)

我们把这三个问题搞明白，那么你对面向对象的理解就很到位。

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Dacb70693aqcaa2ebdce65a05afd0ed54%26expires%3D24h%26dp_logid%3D443696390879258317%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-M6UpRuIuNhAgR%25252BHtFoVwq%25252Bk7kSI%25253D%26file_size%3D23921%26timestamp%3D1745903632%26method%3Dinfo%26fid%3D3170504070-250528-195455261105656%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80%2Fday07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80.md&fs_id=195455261105656&size=23921&uk=3170504070&from=yuanguanjia&fsid=195455261105656&clienttype=8&scence=mac_main#21-%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E7%BC%96%E7%A8%8B%E6%9C%89%E4%BB%80%E4%B9%88%E5%A5%BD%E5%A4%84)2.1 面向对象编程有什么好处？

先来看第一个问题，面向对象编程到底有什么好处呢？ 那就不得不谈，Java的祖师爷对这个世界的理解了。

Java的祖师爷，詹姆斯高斯林认为，在这个世界中 **万物皆对象！**任何一个对象都可以包含一些数据，数据属于哪个对象，就由哪个对象来处理。

这样的话，只要我们找到了对象，其实就找到了对数据的处理方式。

![1662211620054](https://pan.baidu.com/wap/assets/1662211620054.png)

所以面向对象编程的好处，用一句话总结就是：面向对象的开发更符合人类的思维习惯，让编程变得更加简单、更加直观。

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Dacb70693aqcaa2ebdce65a05afd0ed54%26expires%3D24h%26dp_logid%3D443696390879258317%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-M6UpRuIuNhAgR%25252BHtFoVwq%25252Bk7kSI%25253D%26file_size%3D23921%26timestamp%3D1745903632%26method%3Dinfo%26fid%3D3170504070-250528-195455261105656%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80%2Fday07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80.md&fs_id=195455261105656&size=23921&uk=3170504070&from=yuanguanjia&fsid=195455261105656&clienttype=8&scence=mac_main#22-%E7%A8%8B%E5%BA%8F%E4%B8%AD%E5%AF%B9%E8%B1%A1%E5%88%B0%E5%BA%95%E6%98%AF%E4%B8%AA%E5%95%A5)2.2 程序中对象到底是个啥？

说完面向对象编程有什么好处之后，这里有同学可能会有问题了，你刚才举的例子中，“汽车”、“手机”、“蔡徐坤”是一个实实在在的东西，你说是一个对象好理解。那我们程序中的对象到底是个啥呢？

**对象实质上是一种特殊的数据结构**。这种结构怎么理解呢？

你可以把对象理解成一张表格，表当中记录的数据，就是对象拥有的数据。

![1662212402342](https://pan.baidu.com/wap/assets/1662212402342.png)

这就是程序中的对象到底是个啥！ **一句话总结，对象其实就是一张数据表，表当中记录什么数据，对象就处理什么数据。**

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Dacb70693aqcaa2ebdce65a05afd0ed54%26expires%3D24h%26dp_logid%3D443696390879258317%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-M6UpRuIuNhAgR%25252BHtFoVwq%25252Bk7kSI%25253D%26file_size%3D23921%26timestamp%3D1745903632%26method%3Dinfo%26fid%3D3170504070-250528-195455261105656%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80%2Fday07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80.md&fs_id=195455261105656&size=23921&uk=3170504070&from=yuanguanjia&fsid=195455261105656&clienttype=8&scence=mac_main#23-%E5%AF%B9%E8%B1%A1%E6%98%AF%E6%80%8E%E4%B9%88%E5%87%BA%E6%9D%A5%E7%9A%84)2.3 对象是怎么出来的？

刚刚我们讲到对象就是一张数据表，那么这个数据表是怎么来的呢？这张表是不会无缘无故存在的，因为Java也不知道你这个对象要处理哪些数据，所以这张表需要我们设计出来。

用什么来设计这张表呢？就是类（class），**类可以理解成对象的设计图**，或者对象的模板。

![1662213156309](https://pan.baidu.com/wap/assets/1662213156309.png)

我们需要按照对象的设计图创造一个对象。**设计图中规定有哪些数据，对象中就只能有哪些数据。**

![1662213268590](https://pan.baidu.com/wap/assets/1662213268590.png)

**一句话总结：对象可以理解成一张数据表，而数据表中可以有哪些数据，是有类来设计的。**

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Dacb70693aqcaa2ebdce65a05afd0ed54%26expires%3D24h%26dp_logid%3D443696390879258317%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-M6UpRuIuNhAgR%25252BHtFoVwq%25252Bk7kSI%25253D%26file_size%3D23921%26timestamp%3D1745903632%26method%3Dinfo%26fid%3D3170504070-250528-195455261105656%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80%2Fday07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80.md&fs_id=195455261105656&size=23921&uk=3170504070&from=yuanguanjia&fsid=195455261105656&clienttype=8&scence=mac_main#%E4%B8%89-%E5%AF%B9%E8%B1%A1%E5%9C%A8%E8%AE%A1%E7%AE%97%E6%9C%BA%E4%B8%AD%E7%9A%84%E6%89%A7%E8%A1%8C%E5%8E%9F%E7%90%86)三、对象在计算机中的执行原理

各位同学，前面我们已经带同学写了面向对象的代码，也知道对象到底是咋回事。如果我们再搞清楚对象在计算机中的执行原理，那我们对面向对象的理解就更加专业了。

按照我们之前讲的数组的执行原理，数组变量记录的其实数数组在堆内存中的地址。其实面向对象的代码执行原理和数组的执行原理是非常类似的。

其实`Student s1 = new Student();`这句话中的原理如下

- `Student s1`表示的是在栈内存中，创建了一个Student类型的变量，变量名为s1
    
- 而`new Student()`会在堆内存中创建一个对象，而对象中包含学生的属性名和属性值
    
    同时系统会为这个Student对象分配一个地址值0x4f3f5b24
    
- 接着把对象的地址赋值给栈内存中的变量s1，通过s1记录的地址就可以找到这个对象
    
- 当执行`s1.name=“播妞”`时，其实就是通过s1找到对象的地址，再通过对象找到对象的name属性，再给对象的name属性赋值为`播妞`;
    

搞明白`Student s1 = new Student();`的原理之后，`Student s2 = new Student();`原理完全一样，只是在堆内存中重新创建了一个对象，又有一个新的地址。`s2.name`是访问另对象的属性。

![1662213744520](https://pan.baidu.com/wap/assets/1662213744520.png)

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Dacb70693aqcaa2ebdce65a05afd0ed54%26expires%3D24h%26dp_logid%3D443696390879258317%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-M6UpRuIuNhAgR%25252BHtFoVwq%25252Bk7kSI%25253D%26file_size%3D23921%26timestamp%3D1745903632%26method%3Dinfo%26fid%3D3170504070-250528-195455261105656%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80%2Fday07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80.md&fs_id=195455261105656&size=23921&uk=3170504070&from=yuanguanjia&fsid=195455261105656&clienttype=8&scence=mac_main#%E5%9B%9B-%E7%B1%BB%E5%92%8C%E5%AF%B9%E8%B1%A1%E7%9A%84%E4%B8%80%E4%BA%9B%E6%B3%A8%E6%84%8F%E4%BA%8B%E9%A1%B9)四、类和对象的一些注意事项

各位同学，前面几节课我们已经入门了。接下来，关于面向对象有一些细枝末节的东西需要给大家交代一下。

我把这些注意事项已经列举在下面了，我们把几个不好理解的解释一下就可以了（标记方框），其他的大大家一看就能理解。

![1662213891968](https://pan.baidu.com/wap/assets/1662213891968.png)

> **第一条**：一个代码文件中，可以写多个class类，但是只能有一个是public修饰，且public修饰的类必须和文件名相同。

假设文件名为`Demo1.java`，这个文件中假设有两个类`Demo1类和Student类`，代码如下

```
//public修饰的类Demo1，和文件名Demo1相同
public class Demo1{
    
}

class Student{
    
}
```

> **第二条：**对象与对象之间的数据不会相互影响，但是多个变量指向同一个对象会相互影响。

如下图所示，s1和s2两个变量分别记录的是两个对象的地址值，各自修改各自属性值，是互不影响的。

![1662214650611](https://pan.baidu.com/wap/assets/1662214650611.png)

如下图所示，s1和s2两个变量记录的是同一个对象的地址值，s1修改对象的属性值，再用s2访问这个属性，会发现已经被修改了。

![1662215061486](https://pan.baidu.com/wap/assets/1662215061486.png)

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Dacb70693aqcaa2ebdce65a05afd0ed54%26expires%3D24h%26dp_logid%3D443696390879258317%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-M6UpRuIuNhAgR%25252BHtFoVwq%25252Bk7kSI%25253D%26file_size%3D23921%26timestamp%3D1745903632%26method%3Dinfo%26fid%3D3170504070-250528-195455261105656%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80%2Fday07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80.md&fs_id=195455261105656&size=23921&uk=3170504070&from=yuanguanjia&fsid=195455261105656&clienttype=8&scence=mac_main#%E4%BA%94-this%E5%85%B3%E9%94%AE%E5%AD%97)五、this关键字

各位同学，接下来我们学习几个面向对象的小知识点，这里我们先认识一下this关键字是什么含义，再说一下this的应用场景。

**this是什么呢？**

this就是一个变量，用在方法中，可以拿到当前类的对象。

我们看下图所示代码，通过代码来体会这句话到底是什么意思。**哪一个对象调用方法方法中的this就是哪一个对象**

![1662301823320](https://pan.baidu.com/wap/assets/1662301823320.png)

上面代码运行结果如下

![1662302089326](https://pan.baidu.com/wap/assets/1662302089326.png)

**this有什么用呢？**

通过this在方法中可以访问本类对象的成员变量。我们看下图代码，分析打印结果是多少

![1662303254161](https://pan.baidu.com/wap/assets/1662303254161.png)

分析上面的代码`s3.score=325`，调用方法printPass方法时，方法中的`this.score`也是325； 而方法中的参数score接收的是250。执行结果是

![1662303676092](https://pan.baidu.com/wap/assets/1662303676092.png)

关于this关键字我们就学习到这里，重点记住这句话：**哪一个对象调用方法方法中的this就是哪一个对象**

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Dacb70693aqcaa2ebdce65a05afd0ed54%26expires%3D24h%26dp_logid%3D443696390879258317%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-M6UpRuIuNhAgR%25252BHtFoVwq%25252Bk7kSI%25253D%26file_size%3D23921%26timestamp%3D1745903632%26method%3Dinfo%26fid%3D3170504070-250528-195455261105656%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80%2Fday07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80.md&fs_id=195455261105656&size=23921&uk=3170504070&from=yuanguanjia&fsid=195455261105656&clienttype=8&scence=mac_main#%E5%85%AD-%E6%9E%84%E9%80%A0%E5%99%A8)六、构造器

好同学们，接下来我们学习一个非常实用的语法知识——叫做构造器。

关于构造器，我们掌握下面几个问题就可以了：

1. 什么是构造器？
2. 掌握构造器的特点？
3. 构造器的应用场景？
4. 构造器有哪些注意事项？

我们一个问题一个问题的来学习，先来学习什么是构造器？

- **什么是构造器？**
    
    构造器其实是一种特殊的方法，但是这个方法没有返回值类型，方法名必须和类名相同。
    
    如下图所示：下面有一个Student类，构造器名称也必须叫Student；也有空参数构造器，也可以有有参数构造器。
    

![1662304435504](https://pan.baidu.com/wap/assets/1662304435504.png)

认识了构造器之后，接着我们看一下构造器有什么特点。

- **构造器的特点？**
    
    在创建对象时，会调用构造器。
    
    也就是说 `new Student()`就是在执行构造器，当构造器执行完了，也就意味着对象创建成功。
    
    ![1662304779863](https://pan.baidu.com/wap/assets/1662304779863.png)
    
    当执行`new Student("播仔",99)`创建对象时，就是在执行有参数构造器，当有参数构造器执行完，就意味着对象创建完毕了。
    
    ![1662304859276](https://pan.baidu.com/wap/assets/1662304859276.png)
    

关于构造器的特点，我们记住一句话：**new 对象就是在执行构造方法**

- **构造器的应用场景？**
    
    其实构造器就是用来创建对象的。可以在创建对象时给对象的属性做一些初始化操作。如下图所示：
    

![1662305406056](https://pan.baidu.com/wap/assets/1662305406056.png)

- **构造器的注意事项？**
    
    学习完构造器的应用场景之后，接下来我们再看一下构造器有哪些注意事项。
    
    ```
    1.在设计一个类时，如果不写构造器，Java会自动生成一个无参数构造器。
    2.一定定义了有参数构造器，Java就不再提供空参数构造器，此时建议自己加一个无参数构造器。
    ```
    

关于构造器的这几个问题我们再总结一下。掌握这几个问题，构造方法就算完全明白了。

```
1.什么是构造器？
	答：构造器其实是一种特殊的方法，但是这个方法没有返回值类型，方法名必须和类名相			同。
	
2.构造器什么时候执行？
	答：new 对象就是在执行构造方法；

3.构造方法的应用场景是什么？
	答：在创建对象时，可以用构造方法给成员变量赋值

4.构造方法有哪些注意事项？
	1)在设计一个类时，如果不写构造器，Java会自动生成一个无参数构造器。
	2)一定定义了有参数构造器，Java就不再提供空参数构造器，此时建议自己加一个无参数构		造器。
```

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Dacb70693aqcaa2ebdce65a05afd0ed54%26expires%3D24h%26dp_logid%3D443696390879258317%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-M6UpRuIuNhAgR%25252BHtFoVwq%25252Bk7kSI%25253D%26file_size%3D23921%26timestamp%3D1745903632%26method%3Dinfo%26fid%3D3170504070-250528-195455261105656%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80%2Fday07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80.md&fs_id=195455261105656&size=23921&uk=3170504070&from=yuanguanjia&fsid=195455261105656&clienttype=8&scence=mac_main#%E4%B8%83-%E5%B0%81%E8%A3%85%E6%80%A7)七、封装性

各位同学，接下来我们再学习一个面向对象很重要的特征叫做——封装性。

**1. 什么是封装呢？**

所谓封装，就是用类设计对象处理某一个事物的数据时，应该把要处理的数据，以及处理数据的方法，都设计到一个对象中去。

比如：在设计学生类时，把学生对象的姓名、语文成绩、数学成绩三个属性，以及求学生总分、平均分的方法，都封装到学生对象中来。

![1662305928023](https://pan.baidu.com/wap/assets/1662305928023.png)

现在我们已经知道什么是封装了。那我们学习封装，学习个啥呢？ 其实在实际开发中，在用类设计对事处理的数据，以及对数据处理的方法时，是有一些设计规范的。

封装的设计规范用8个字总结，就是：**合理隐藏、合理暴露**

比如，设计一辆汽车时，汽车的发动机、变速箱等一些零件并不需要让每一个开车的知道，所以就把它们隐藏到了汽车的内部。

把发动机、变速箱等这些零件隐藏起来，这样做其实更加安全，因为并不是所有人都很懂发动机、变速箱，如果暴露在外面很可能会被不懂的人弄坏。

![1662306602412](https://pan.baidu.com/wap/assets/1662306602412.png)

在设计汽车时，除了隐藏部分零件，但是还是得合理的暴露一些东西出来，让司机能够操纵汽车，让汽车跑起来。比如：点火按钮啊、方向盘啊、刹车啊、油门啊、档把啊… 这些就是故意暴露出来让司机操纵汽车的。

![1662306879230](https://pan.baidu.com/wap/assets/1662306879230.png)

好了，到现在我们已经理解什么是封装的一些规范了。就是：**合理暴露、合理隐藏**

**2. 封装在代码中的体现**

知道什么是封装之后，那封装在代码中如何体现呢？一般我们在设计一个类时，会将成员变量隐藏，然后把操作成员变量的方法对外暴露。

这里需要用到一个修饰符，叫private，**被private修饰的变量或者方法，只能在本类中被访问。**

如下图所示，`private double score;` 就相当于把score变量封装在了Student对象的内部，且不对外暴露，你想要在其他类中访问score这个变量就，就不能直接访问了；

如果你想给Student对象的score属性赋值，得调用对外暴露的方法`setScore(int score)`，在这个方法中可以对调用者传递过来的数据进行一些控制，更加安全。

![1662307191295](https://pan.baidu.com/wap/assets/1662307191295.png)

当你想获取socre变量的值时，就得调用对外暴露的另一个方法 `getScore()`

关于封装我们就学习到这里了。

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Dacb70693aqcaa2ebdce65a05afd0ed54%26expires%3D24h%26dp_logid%3D443696390879258317%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-M6UpRuIuNhAgR%25252BHtFoVwq%25252Bk7kSI%25253D%26file_size%3D23921%26timestamp%3D1745903632%26method%3Dinfo%26fid%3D3170504070-250528-195455261105656%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80%2Fday07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80.md&fs_id=195455261105656&size=23921&uk=3170504070&from=yuanguanjia&fsid=195455261105656&clienttype=8&scence=mac_main#%E5%85%AB-%E5%AE%9E%E4%BD%93javabean)八、实体JavaBean

接下来，我们学习一个面向对象编程中，经常写的一种类——叫实体JavaBean类。我们先来看什么是实体类？

**1. 什么是实体类？**

实体类就是一种特殊的类，它需要满足下面的要求：

![1662335204398](https://pan.baidu.com/wap/assets/1662335204398.png)

接下来我们按照要求，写一个Student实体类；

![1662335451401](https://pan.baidu.com/wap/assets/1662335451401.png)

写完实体类之后，我们看一看它有什么特点？ 其实我们会发现实体类中除了有给对象存、取值的方法就没有提供其他方法了。所以实体类仅仅只是用来封装数据用的。

知道实体类有什么特点之后，接着我们看一下它有哪些应用场景？

**2. 实体类的应用场景**

在实际开发中，实体类仅仅只用来封装数据，而对数据的处理交给其他类来完成，以实现数据和数据业务处理相分离。如下图所示

![1662336287570](https://pan.baidu.com/wap/assets/1662336287570.png)

在实际应用中，会将类作为一种数据类型使用。如下图所示，在StudentOperator类中，定义一个Student类型的成员变量student，然后使用构造器给student成员变量赋值。

然后在Student的printPass()方法中，使用student调用Student对象的方法，对Student对象的数据进行处理。

![1662337507608](https://pan.baidu.com/wap/assets/1662337507608.png)

到这里，我们已经学习了JavaBean实体类的是什么，以及它的应用场景，我们总结一下

```
1.JavaBean实体类是什么？有啥特点
	JavaBean实体类，是一种特殊的；它需要私有化成员变量，有空参数构造方法、同时提供		getXxx和setXxx方法；
	
	JavaBean实体类仅仅只用来封装数据，只提供对数据进行存和取的方法
 
2.JavaBean的应用场景？
	JavaBean实体类，只负责封装数据，而把数据处理的操作放在其他类中，以实现数据和数		据处理相分离。
```

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Dacb70693aqcaa2ebdce65a05afd0ed54%26expires%3D24h%26dp_logid%3D443696390879258317%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-M6UpRuIuNhAgR%25252BHtFoVwq%25252Bk7kSI%25253D%26file_size%3D23921%26timestamp%3D1745903632%26method%3Dinfo%26fid%3D3170504070-250528-195455261105656%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80%2Fday07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80.md&fs_id=195455261105656&size=23921&uk=3170504070&from=yuanguanjia&fsid=195455261105656&clienttype=8&scence=mac_main#%E4%B9%9D-%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E7%BB%BC%E5%90%88%E6%A1%88%E4%BE%8B)九、面向对象综合案例

学习完面向对象的语法知识之后。接下来，我们做一个面向对象的综合案例——模仿电影信息系统。

需求如下图所示

```
1. 想要展示系统中全部的电影信息（每部电影：编号、名称、价格）
2. 允许用户根据电影的编号（id），查询出某个电影的详细信息。
```

![1662351774659](https://pan.baidu.com/wap/assets/1662351774659.png)

运行程序时，能够根据用户的选择，执行不同的功能，如下图所示

![1662351990387](https://pan.baidu.com/wap/assets/1662351990387.png)

按照下面的步骤来完成需求

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Dacb70693aqcaa2ebdce65a05afd0ed54%26expires%3D24h%26dp_logid%3D443696390879258317%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-M6UpRuIuNhAgR%25252BHtFoVwq%25252Bk7kSI%25253D%26file_size%3D23921%26timestamp%3D1745903632%26method%3Dinfo%26fid%3D3170504070-250528-195455261105656%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80%2Fday07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80.md&fs_id=195455261105656&size=23921&uk=3170504070&from=yuanguanjia&fsid=195455261105656&clienttype=8&scence=mac_main#1-%E7%AC%AC%E4%B8%80%E6%AD%A5%E5%AE%9A%E4%B9%89%E7%94%B5%E5%BD%B1%E7%B1%BB)1. 第一步：定义电影类

首先每一部电影，都包含这部电影的相关信息，比如：电影的编号（id）、电影的名称（name）、电影的价格（price）、电影的分数（score）、电影的导演（director）、电影的主演（actor）、电影的简介（info）。

为了去描述每一部电影，有哪些信息，我们可以设计一个电影类（Movie），电影类仅仅只是为了封装电影的信息，所以按照JavaBean类的标准写法来写就行。

```
public class Movie {
    private int id;
    private String name;
    private double price;
    private double score;
    private String director;
    private String actor;
    private String info;

    public Movie() {
    }

    public Movie(int id, String name, double price, double score, String director, String actor, String info) {
        this.id = id;
        this.name = name;
        this.price = price;
        this.score = score;
        this.director = director;
        this.actor = actor;
        this.info = info;
    }

    public int getId() {
        return id;
    }

    public void setId(int id) {
        this.id = id;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public double getPrice() {
        return price;
    }

    public void setPrice(double price) {
        this.price = price;
    }

    public double getScore() {
        return score;
    }

    public void setScore(double score) {
        this.score = score;
    }

    public String getDirector() {
        return director;
    }

    public void setDirector(String director) {
        this.director = director;
    }

    public String getActor() {
        return actor;
    }

    public void setActor(String actor) {
        this.actor = actor;
    }

    public String getInfo() {
        return info;
    }

    public void setInfo(String info) {
        this.info = info;
    }
}
```

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Dacb70693aqcaa2ebdce65a05afd0ed54%26expires%3D24h%26dp_logid%3D443696390879258317%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-M6UpRuIuNhAgR%25252BHtFoVwq%25252Bk7kSI%25253D%26file_size%3D23921%26timestamp%3D1745903632%26method%3Dinfo%26fid%3D3170504070-250528-195455261105656%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80%2Fday07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80.md&fs_id=195455261105656&size=23921&uk=3170504070&from=yuanguanjia&fsid=195455261105656&clienttype=8&scence=mac_main#2-%E7%AC%AC%E4%BA%8C%E6%AD%A5%E5%AE%9A%E4%B9%89%E7%94%B5%E5%BD%B1%E6%93%8D%E4%BD%9C%E7%B1%BB)2. 第二步：定义电影操作类

前面我们定义的Movie类，仅仅只是用来封装每一部电影的信息。为了让电影数据和电影数据的操作相分离，我们还得有一个电影操作类（MovieOperator）。

因为系统中有多部电影，所以电影操作类中MovieOperator，需要有一个`Movie[] movies;` 用来存储多部电影对象；

同时在MovieOperator类中，提供对外提供，对电影数组进行操作的方法。如`printAllMovies()`用于打印数组中所有的电影信息，`searchMovieById(int id)`方法根据id查找一个电影的信息并打印。

```
public class MovieOperator {
    //因为系统中有多部电影，所以电影操作类中，需要有一个Movie的数组
    private Movie[] movies;
    public MovieOperator(Movie[] movies){
        this.movies = movies;
    }

    /** 1、展示系统全部电影信息 movies = [m1, m2, m3, ...]*/
    public void printAllMovies(){
        System.out.println("-----系统全部电影信息如下：-------");
        for (int i = 0; i &lt; movies.length; i++) {
            Movie m = movies[i];
            System.out.println("编号：" + m.getId());
            System.out.println("名称：" + m.getName());
            System.out.println("价格：" + m.getPrice());
            System.out.println("------------------------");
        }
    }

    /** 2、根据电影的编号查询出该电影的详细信息并展示 */
    public void searchMovieById(int id){
        for (int i = 0; i &lt; movies.length; i++) {
            Movie m = movies[i];
            if(m.getId() == id){
                System.out.println("该电影详情如下：");
                System.out.println("编号：" + m.getId());
                System.out.println("名称：" + m.getName());
                System.out.println("价格：" + m.getPrice());
                System.out.println("得分：" + m.getScore());
                System.out.println("导演：" + m.getDirector());
                System.out.println("主演：" + m.getActor());
                System.out.println("其他信息：" + m.getInfo());
                return; // 已经找到了电影信息，没有必要再执行了
            }
        }
        System.out.println("没有该电影信息~");
    }
}
```

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Dacb70693aqcaa2ebdce65a05afd0ed54%26expires%3D24h%26dp_logid%3D443696390879258317%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-M6UpRuIuNhAgR%25252BHtFoVwq%25252Bk7kSI%25253D%26file_size%3D23921%26timestamp%3D1745903632%26method%3Dinfo%26fid%3D3170504070-250528-195455261105656%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80%2Fday07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80.md&fs_id=195455261105656&size=23921&uk=3170504070&from=yuanguanjia&fsid=195455261105656&clienttype=8&scence=mac_main#3-%E7%AC%AC%E4%B8%89%E6%AD%A5%E5%AE%9A%E4%B9%89%E6%B5%8B%E8%AF%95%E7%B1%BB)3. 第三步：定义测试类

最后，我们需要在测试类中，准备好所有的电影数据，并用一个数组保存起来。每一部电影的数据可以封装成一个对象。然后把对象用数组存起来即可。

```
public class Test {
    public static void main(String[] args) {
        //创建一个Movie类型的数组
        Movie[] movies = new Movie[4];
        //创建4个电影对象，分别存储到movies数组中
        movies[0] = new Movie(1,"水门桥", 38.9, 9.8, "徐克", "吴京","12万人想看");
        movies[1] = new Movie(2, "出拳吧", 39, 7.8, "唐晓白", "田雨","3.5万人想看");
        movies[2] = new Movie(3,"月球陨落", 42, 7.9, "罗兰", "贝瑞","17.9万人想看");
        movies[3] = new Movie(4,"一点就到家", 35, 8.7, "许宏宇", "刘昊然","10.8万人想看");
        
    }
}
```

准备好测试数据之后，接下来就需要对电影数据进行操作。我们已经把对电影操作先关的功能写到了MovieOperator类中，所以接下来，创建MovieOperator类对象，调用方法就可以完成相关功能。

继续再main方法中，接着写下面的代码。

```
// 4、创建一个电影操作类的对象，接收电影数据，并对其进行业务处理
MovieOperator operator = new MovieOperator(movies);
Scanner sc = new Scanner(System.in);
while (true) {
    System.out.println("==电影信息系统==");
    System.out.println("1、查询全部电影信息");
    System.out.println("2、根据id查询某个电影的详细信息展示");
    System.out.println("请您输入操作命令：");
    int command = sc.nextInt();
    switch (command) {
        case 1:
            // 展示全部电影信息
            operator.printAllMovies();
            break;
        case 2:
            // 根据id查询某个电影的详细信息展示
            System.out.println("请您输入查询的电影id:");
            int id = sc.nextInt();
            operator.searchMovieById(id);
            break;
        default:
            System.out.println("您输入的命令有问题~~");
    }
}
```

到这里，电影信息系统就完成了。 小伙伴们，自己尝试写一下吧！！

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3Dacb70693aqcaa2ebdce65a05afd0ed54%26expires%3D24h%26dp_logid%3D443696390879258317%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-M6UpRuIuNhAgR%25252BHtFoVwq%25252Bk7kSI%25253D%26file_size%3D23921%26timestamp%3D1745903632%26method%3Dinfo%26fid%3D3170504070-250528-195455261105656%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80%2Fday07-Java%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%9F%BA%E7%A1%80.md&fs_id=195455261105656&size=23921&uk=3170504070&from=yuanguanjia&fsid=195455261105656&clienttype=8&scence=mac_main#%E5%8D%81-%E6%88%90%E5%91%98%E5%8F%98%E9%87%8F%E5%92%8C%E5%B1%80%E9%83%A8%E5%8F%98%E9%87%8F%E7%9A%84%E5%8C%BA%E5%88%AB)十、成员变量和局部变量的区别

各位同学，面向对象的基础内容咱们已经学习完了。同学们在面向对象代码时，经常会把成员变量和局部变量搞混。所以现在我们讲一讲他们的区别。

![1662371089114](https://pan.baidu.com/wap/assets/1662371089114.png)

如下图所示，成员变量在类中方法外，而局部变量在方法中。

![1662353340190](https://pan.baidu.com/wap/assets/1662353340190.png)

---

到这里，我们关于面向对象的基础知识就学习完了。**面向对象的核心点就是封装，将数据和数据的处理方式，都封装到对象中； 至于对象要封装哪些数据？对数据进行怎样的处理？ 需要通过类来设计。**

需要注意的是，不同的人，对同一个对象进行设计，对象封装那些数据，提供哪些方法，可能会有所不同；只要能够完成需求，符合设计规范，都是合理的设计。



- 如果当前程序中，要调用自己所在包下的其他程序，可以直接调用。（同一个包下的类，互相可以直接调用）
    
- 如果当前程序中，要调用其他包下的程序，则必须在当前程序中导包, 才可以访问！
    
    导包格式： `import 包名.类名`
    
- 如果当前程序中，要调用Java.lang包下的程序，不需要我们导包的，可以直接使用。
    
- 如果当前程序中，要调用多个不同包下的程序，而这些程序名正好一样，此时默认只能导入一个程序，另一个程序必须带包名访问。
    

## [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D6a9b44abfrf69adbba828b3271bda20b%26expires%3D24h%26dp_logid%3D443709929040815351%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-jOZC0bHS%25252BupMZYq%25252F3Bm07jgS3pE%25253D%26file_size%3D32000%26timestamp%3D1745903682%26method%3Dinfo%26fid%3D3170504070-250528-971560969751281%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day08-Java%E5%B8%B8%E7%94%A8API.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday08-Java%E5%B8%B8%E7%94%A8API%2Fday08-Java%E5%B8%B8%E7%94%A8API.md&fs_id=971560969751281&size=32000&uk=3170504070&from=yuanguanjia&fsid=971560969751281&clienttype=8&scence=mac_main#%E4%B8%89-string%E7%B1%BB)
按照面向对象的编程思想，对于字符串的操作，只需要创建字符串对象，用字符串对象封装字符串数据，然后调用String类的方法就可以了。

![1662607669465](https://pan.baidu.com/wap/assets/1662607669465.png)

---

### [](https://pan.baidu.com/wap/markdown?picdocpreview=https%3A%2F%2Fpcsdata.baidu.com%2Frest%2F2.0%2Fdocview%2Ftext%3Fobject%3D6a9b44abfrf69adbba828b3271bda20b%26expires%3D24h%26dp_logid%3D443709929040815351%26rt%3Dpr%26sign%3DFOTRE-DCb740ccc5511e5e8fedcff06b081203-jOZC0bHS%25252BupMZYq%25252F3Bm07jgS3pE%25253D%26file_size%3D32000%26timestamp%3D1745903682%26method%3Dinfo%26fid%3D3170504070-250528-971560969751281%26client_type%3Dpcygj%26file_type%3Dmd&server_filename=day08-Java%E5%B8%B8%E7%94%A8API.md&path=%2F%E8%87%AA%E5%AD%A6%2F2025%E6%9C%80%E6%96%B0%E7%89%88-Java%E5%AD%A6%E4%B9%A0%E8%B7%AF%E7%BA%BF%E5%9B%BE%2F%E7%AC%AC1%E9%98%B6%E6%AE%B5%E2%80%94Java%E5%9F%BA%E7%A1%80%2F1%E3%80%81Java%E5%9F%BA%E7%A1%80-20%E5%A4%A9%E5%AD%A6%E4%BC%9AJava%2F%E7%AC%AC%E4%B8%80%E9%98%B6%E6%AE%B5%EF%BC%9A%E5%9F%BA%E7%A1%80%E5%85%A5%E9%97%A89%E5%A4%A9%E8%AF%BE%E7%A8%8B%EF%BC%88%E8%B5%84%E6%96%99%EF%BC%89%2F%E5%85%A8%E9%83%A8%E8%AE%B2%E4%B9%89%2Fday08-Java%E5%B8%B8%E7%94%A8API%2Fday08-Java%E5%B8%B8%E7%94%A8API.md&fs_id=971560969751281&size=32000&uk=3170504070&from=yuanguanjia&fsid=971560969751281&clienttype=8&scence=mac_main#2-string%E5%88%9B%E5%BB%BA%E5%AF%B9%E8%B1%A1)2. String创建对象

接下来我们打开String类的API，看一下String类的对象如何创建。如下图所示

![1662607801186](https://pan.baidu.com/wap/assets/1662607801186.png)

String类的API中，有这么一句话：“Java程序中的所有字符串字面值（如"abc"）都是字符串的实例实现”。这里所说的实例实现，其实指的就是字符串对象。

意思就是：**所有Java的字符串字面值，都是字符串对象。**

- 所以创建String对象的第一种方式就有了

```
String s1 = "abc"; //这里"abc"就是一个字符串对象，用s1变量接收

String s2 = "黑马程序员"; //这里的“黑马程序员”也是一个字符串对象，用s2变量接收
```

- 创建String对象还有第二种方式，就是利用String类的构造方法创建String类的对象。

![1662608166502](https://pan.baidu.com/wap/assets/1662608166502.png)

我们前面学习过类的构造方法，执行构造方法需要用到new关键字。`new String(参数)`就是在执行String类的构造方法。

下面我们演示通过String类的构造方法，创建String类的对象

```
// 1、直接双引号得到字符串对象，封装字符串数据
String name = "黑马666";
System.out.println(name);

// 2、new String创建字符串对象，并调用构造器初始化字符串
String rs1 = new String();
System.out.println(rs1); // ""

String rs2 = new String("itheima");
System.out.println(rs2);

char[] chars = {'a', '黑', '马'};
String rs3 = new String(chars);
System.out.println(rs3);

byte[] bytes = {97, 98, 99};
String rs4 = new String(bytes);
System.out.println(rs4);
```

关于String类是用来干什么的，
![1661444896100](https://pan.baidu.com/wap/assets/1661444896100.png)