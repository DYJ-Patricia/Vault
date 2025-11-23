---
url: https://www.zhihu.com/question/11379810074/answer/1939628372922708504?share_code=1f4NgqM1E2bLd&utm_psn=1976084020136780302
title: 大一计算机新生怎么合理利用 github？
author: zhihu.com
aliases: 
 - 大一计算机新生怎么合理利用 github？
date: 2025-11-24 00:29:04
tags:

banner: "https://picx.zhimg.com/v2-6d4a21f9ecc355ba182a68916acdd3c7_l.jpg?source=2c26e567"
banner_icon: 🔖
---
![](https://picx.zhimg.com/v2-6d4a21f9ecc355ba182a68916acdd3c7_l.jpg?source=2c26e567)

CodeCrafter​

谢邀。。

看到这个问题，真是感慨万千。那个时候国内几乎没人认真玩 [GitHub](https://zhida.zhihu.com/search?content_id=742279157&content_type=Answer&match_order=1&q=GitHub&zd_token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJ6aGlkYV9zZXJ2ZXIiLCJleHAiOjE3NjQwODc5OTksInEiOiJHaXRIdWIiLCJ6aGlkYV9zb3VyY2UiOiJlbnRpdHkiLCJjb250ZW50X2lkIjo3NDIyNzkxNTcsImNvbnRlbnRfdHlwZSI6IkFuc3dlciIsIm1hdGNoX29yZGVyIjoxLCJ6ZF90b2tlbiI6bnVsbH0.Gp5U-xIOJZ3sq3T_5oC_Gvk7mNH6zfpeB0ZeSzhjzm8&zhida_source=entity)，老师讲课还在用 U 盘传代码，后缀名从 “最终版” 到“最终版 - 改 1”再到“打死也不改了版”，现在想想，简直是石器时代。。到后来工作做算法和数据科学，GitHub 直接成了我的半个办公室——查代码、看别人项目、跟开源社区扯皮提 issue、远程协作写代码都离不开它。

如今的学弟学妹们，能在一进大学就知道 GitHub，已经领先了我们那一代人太多。但知道归知道，怎么把它用到实处，用到能让你在未来找工作时脱颖而出，这里面门道还挺多。

大一同学刚接触的时候，很容易被它搞懵，“我又不是做开源的，甚至 C 语言语法都没掌握好，GitHub 有啥用啊”。但其实，越早把 GitHub 用到日常学习里，你的学习速度会比同龄人快一截——不是那种虚假的 “我会了” 的感觉，而是真的能在项目里打出来的能力。

我按自己的经历分几个方向聊，里面有一些你大一就能用的具体做法。

我也不整那些虚头巴脑的，就跟你唠唠嗑，分几个阶段，讲讲一个普通计算机学生，怎么把 GitHub 这东西从一个 “听说很牛逼的网站” 变成你自己的个人名片，打造个人的影响力。

### **第一阶段：大一上学期 —— 把它当成专门放你的代码的移动硬盘**

你现在刚上大一，估计 C 语言的指针还没盘明白，数据结构刚讲到链表，操作系统更是天书。这时候跟你讲什么开源贡献、持续集成，纯属扯淡。

现阶段，GitHub 对你来说，功能就一个，而且无比重要：**防止代码丢失，记录你的学习轨迹。**

你一定会经历这种事：辛辛苦苦写了一周的课程设计，电脑突然蓝屏，硬盘直接报废。或者 U 盘拷代码，结果 U 盘丢了、坏了。那感觉，比失恋还难受。过来人告诉你，这几乎是每个程序员都踩过的坑。

所以，你现在要做的，就是把 GitHub 当成一个不要钱，还超级稳定的云端硬盘。

**具体怎么做？**

1.  **装个 Git。** 别用那些花里胡哨的客户端，直接官网下载 Git，装好。学会在命令行里敲 `git` 命令。为啥？因为这东西是基本功，以后工作环境大概率是 Linux 服务器，黑乎乎的命令行就是你的全部。你现在用客户端偷的懒，以后都要加倍还回来。
2.  **学五个命令就够了。** 真的，现阶段就这五个：

*   `git init` (在你本地的文件夹里，说 “这地方归我管了！”)
*   `git add .` (把文件夹里所有改动的东西都打包，准备寄快递)
*   `git commit -m "我今天写了xxx功能"` (给你的快递写个备注，不然以后鬼知道你寄了啥)
*   `git remote add origin [你的仓库链接]` (告诉你这个快递要寄到哪儿)
*   `git push origin master` (点击 “发送” 按钮，把快递寄出去)

就这几步，每天你写完作业，或者一个功能写得差不多了，就敲一遍。把你的 C 语言作业、数据结构练习，哪怕是写了一半的垃圾代码，都扔上去。

很多人一上来就想做 Open Source Contributor，然后发现自己连 Issue 都看不懂。大一阶段，你可以先做这几类 “小积累”：

1.  **刷题仓库**：刷的 [LeetCode](https://zhida.zhihu.com/search?content_id=742279157&content_type=Answer&match_order=1&q=LeetCode&zd_token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJ6aGlkYV9zZXJ2ZXIiLCJleHAiOjE3NjQwODc5OTksInEiOiJMZWV0Q29kZSIsInpoaWRhX3NvdXJjZSI6ImVudGl0eSIsImNvbnRlbnRfaWQiOjc0MjI3OTE1NywiY29udGVudF90eXBlIjoiQW5zd2VyIiwibWF0Y2hfb3JkZXIiOjEsInpkX3Rva2VuIjpudWxsfQ.MSrfu4SkDx8i-lz50zTrB36CLcy3vuko-e95Qqo9xHU&zhida_source=entity) 题，不要散落在本地文件夹，建个 repo 分类存。未来找实习可以直接甩仓库给面试官。
2.  **课堂代码笔记**：比如学《数据结构》，你写的链表、队列、树的实现都集中在一个 repo，配上简单的 README，说清楚实现原理。
3.  **读书笔记 / 课件**：可以用 Markdown + GitHub 管理，顺便熟悉 Markdown 语法（这个你以后天天用）。

关键是——不要觉得这些很 low，很多大牛也是这么开始的。等你回过头看大一的 commit，就能看到自己的进步曲线。

此外，我再可以给你一些实践灵感。

1.  **课程作业协同调试** 你和同学做一个 C 程序课设，把仓库设私有，互相 fork 开发，push 后看 diff。这样比 QQ 传压缩包高效多了，还能看到每个人写了哪些部分。
2.  **自学项目成长记录** 学 Python 的时候，你可以开个 “Python-100-days” 仓库，每天写一个练习脚本（爬虫、数据分析、小游戏），坚持 100 天。到大二找实习时，这个 repo 会很有说服力，不比 “我学过 Python” 空口白话强？

**这么做有啥好处？**

**安全感。** 电脑炸了？没事，换台电脑，`git clone` 一下，代码全回来了。

**养成好习惯。** 让你从一开始就习惯版本控制，这比你学 100 个算法都有用。我见过太多工作好几年的人，git 用得一塌糊涂。

**一个不经意的 “简历”。** 等你大四找工作时，面试官点开你的 GitHub，看到你从大一开始，就有代码提交记录，哪怕代码写的在烂，他都会觉得：“这小伙子，有想法，有毅力，是个好苗子。” 这就是所谓的 “持续学习能力的证明”。

**推荐资源**

*   **[《Pro Git》](https://zhida.zhihu.com/search?content_id=742279157&content_type=Answer&match_order=1&q=%E3%80%8APro+Git%E3%80%8B&zd_token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJ6aGlkYV9zZXJ2ZXIiLCJleHAiOjE3NjQwODc5OTksInEiOiLjgIpQcm8gR2l044CLIiwiemhpZGFfc291cmNlIjoiZW50aXR5IiwiY29udGVudF9pZCI6NzQyMjc5MTU3LCJjb250ZW50X3R5cGUiOiJBbnN3ZXIiLCJtYXRjaF9vcmRlciI6MSwiemRfdG9rZW4iOm51bGx9.p9OcDc2FrJsH-KJmHuoehNlNfyNpcpKJM-0Lb3ZKW0M&zhida_source=entity)**：别看书名吓人，这书写得巨好，而且免费。你不用全看，看前几章，把基本概念和常用命令搞懂就行。
*   **廖雪峰的 Git 教程**：网站形式，中文的，非常适合入门。

[（持续更新中）技术总监收藏夹的学习资源汇总：计算机基础、语言类、大数据、数据分析、数据科学、AI、大模型](https://zhuanlan.zhihu.com/p/1918954720678098873)

新人一大毛病就是怕自己的代码不上档次，不敢放出来。其实没人会在意你大一的项目是不是优雅到极致，比起 “完美代码”，程序员更关注一个人是不是坚持更新、有没有持续学习。 甚至你可以开一个叫 learning-notes 的仓库，里面就是笔记、学习心路、踩坑记录。我比起只会在朋友圈截图“刷题 100 天” 的人，更尊重能把过程摆在 GitHub 上的同学——因为这才是可验证的。

我见过身边好多牛人，GitHub 账户的第一年全是乱七八糟的小玩意儿，但这些小玩意儿拼起来，就是他们的技术轨迹。

这个阶段，英语要过关，至少能看懂 README 和 issue 讨论，不然 GitHub 只能当图床用，不要觉得 star 越多越好，热门项目往往对新人不友好，先找小而美的入手，你需要懂点 Markdown，写 README 不会太丑，这直接影响别人对你项目的观感，别老想着把 GitHub 当硬盘，“上传即备份” 没问题，但别太乱，过几个月你自己也找不到文件。

几乎每个新人都有过类似经历：命令都记得，Git 也天天在用，但只要一出问题就完全不知道发生了什么。 因为大多数教程教的是命令，而不是机制。 Git 是分布式版本控制系统，它的每个操作背后都有一套指针逻辑。 当你知道 HEAD、commit tree、index、branch ref 是怎么关联的，才会发现 rebase、merge、reset、cherry-pick 其实都很优雅。

所以如果你真的想彻底搞懂 git，强烈推荐这份字节内部的 git 手册，免费下载：[Git 零基础实战手册. pdf](https://link.zhihu.com/?target=https%3A//mp.weixin.qq.com/s/YgN9lWGwcPw2qk9YJr7ngw)，结合了大厂协作流程和真实事故案例写成的系统教程。 比如它会告诉你：为什么有时候 pull 等于 “灾难按钮”；团队为什么要禁用 force push；怎么用 rebase 保证主干干净；以及遇到冲突时的最佳修复流程。

### **第二阶段：大一下到大二 —— 从 “用户” 变成一个“逛街的”**

等你代码写多一点了，不满足于只把 GitHub 当仓库了。这时候，你要开始 “逛”GitHub。

GitHub 是世界上最大的程序员同性交友社区，啊不，是开源社区。这里有无数的宝藏。

**怎么逛**

**用好搜索。** 比如你在学 Python 写爬虫，你就直接在 GitHub 搜 “[Python spider](https://zhida.zhihu.com/search?content_id=742279157&content_type=Answer&match_order=1&q=Python+spider&zd_token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJ6aGlkYV9zZXJ2ZXIiLCJleHAiOjE3NjQwODc5OTksInEiOiJQeXRob24gc3BpZGVyIiwiemhpZGFfc291cmNlIjoiZW50aXR5IiwiY29udGVudF9pZCI6NzQyMjc5MTU3LCJjb250ZW50X3R5cGUiOiJBbnN3ZXIiLCJtYXRjaF9vcmRlciI6MSwiemRfdG9rZW4iOm51bGx9.wA_ney_8xsHljv5Kb5OaYap9dP8ac29-ZVXQK1x1KkY&zhida_source=entity)”，按 Star 数排序，看看别人写的项目。看不懂没关系，先看，感受一下。

**关注 “[Awesome](https://zhida.zhihu.com/search?content_id=742279157&content_type=Answer&match_order=1&q=Awesome&zd_token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJ6aGlkYV9zZXJ2ZXIiLCJleHAiOjE3NjQwODc5OTksInEiOiJBd2Vzb21lIiwiemhpZGFfc291cmNlIjoiZW50aXR5IiwiY29udGVudF9pZCI6NzQyMjc5MTU3LCJjb250ZW50X3R5cGUiOiJBbnN3ZXIiLCJtYXRjaF9vcmRlciI6MSwiemRfdG9rZW4iOm51bGx9.sDer-yI6g5DNdcwBpH6NgB8FZ55fSXutowC0TtzIee0&zhida_source=entity)” 系列。** 这是一个神奇的关键词。比如你想学计算机科学，就去搜 `Awesome Computer Science`；想学 Python，就搜 `Awesome Python`。这些仓库都是别人整理好的学习资源、工具、项目的清单，质量极高，能帮你省下无数到处找资料的时间。比如这个 `awesome-cs-courses`，里面全是世界名校的计算机公开课，还带课程资料，简直是作弊神器。

**读别人的代码。** 这是提升最快的方式，没有之一。找一个你感兴趣的，代码量不大的小项目（比如几百行、一千行），Star 多一点的。先 `git clone` 下来，在本地跑起来。然后看它的 `README.md` 文件，这是项目的说明书。然后，从它的主程序（比如 `main.py`）开始读，一行一行看，一个函数一个函数地跟。遇到不认识的库，就去搜。

这一步比较重要，不是为了抄，而是学会怎么拆别人代码。你会看到不同人怎么组织文件结构、怎么写 README、训练脚本放哪，参数怎么配置。

这个过程很痛苦，但只要你完整读懂了一个项目，你的水平会瞬间上一个台阶。

我当年学机器学习的时候，对推荐系统很感兴趣。在 GitHub 上搜到了一个叫 `[Surprise](https://zhida.zhihu.com/search?content_id=742279157&content_type=Answer&match_order=1&q=Surprise&zd_token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJ6aGlkYV9zZXJ2ZXIiLCJleHAiOjE3NjQwODc5OTksInEiOiJTdXJwcmlzZSIsInpoaWRhX3NvdXJjZSI6ImVudGl0eSIsImNvbnRlbnRfaWQiOjc0MjI3OTE1NywiY29udGVudF90eXBlIjoiQW5zd2VyIiwibWF0Y2hfb3JkZXIiOjEsInpkX3Rva2VuIjpudWxsfQ.AeIkNBSRlXFYwWztrcgjG7wftS74mjumJp70kL6EWok&zhida_source=entity)` 的 Python 库，专门做推荐算法的。代码量不大，文档也全。我就把它 clone 下来，先跑官方的 demo，然后去看它实现`SVD`（一种推荐算法）的那部分源码。里面大量的`numpy`操作和矩阵运算，一开始看得我头皮发麻。我就一边查`numpy`的文档，一边在纸上画矩阵，硬是把那个流程给啃下来了。等我啃完，不仅算法原理懂了，`numpy`的骚操作也学了不少，后来面试的时候，跟面试官聊这个项目，对方明显对我刮目相看。

### **第三阶段：大二下到大三 —— 从 “围观” 到“搭把手”**

逛得多了，看得多了，你可能会手痒，想自己也参与一下。这就是 “开源贡献”。

很多人觉得这事儿高不可攀，感觉自己得是大牛才能给项目贡献代码。

**完全是误解！**

你的第一次贡献，可以非常非常简单。

这一步很多人拖到研究生才做，我觉得没必要等。参与开源不等于你一上来就要给 [Linux kernel](https://zhida.zhihu.com/search?content_id=742279157&content_type=Answer&match_order=1&q=Linux+kernel&zd_token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJ6aGlkYV9zZXJ2ZXIiLCJleHAiOjE3NjQwODc5OTksInEiOiJMaW51eCBrZXJuZWwiLCJ6aGlkYV9zb3VyY2UiOiJlbnRpdHkiLCJjb250ZW50X2lkIjo3NDIyNzkxNTcsImNvbnRlbnRfdHlwZSI6IkFuc3dlciIsIm1hdGNoX29yZGVyIjoxLCJ6ZF90b2tlbiI6bnVsbH0.jOXgi0YQj--O5cActWvXmxDcx2dItZP5zjAYtflpGSk&zhida_source=entity) 提交补丁，甚至可以是帮忙修 typo、补 README，翻译一段文档。

我带过的一个学弟，当时就是在大一时帮一个 Python 爬虫库补了两个中文文档的例子，结果 maintainer 很高兴，直接拉他进了 contributors 列表。后来这个经历在他的校外比赛简历里直接生效——因为这说明他有团队协作意识和实际贡献。

**怎么开始第一次贡献（Pull Request）？**

1.  **找个 “软柿子” 捏。** 很多大型项目都有一个叫 `good first issue` 的标签。这是项目维护者专门给新手准备的，难度很低，比如改个文档里的错别字、翻译一小段文档、修复一个非常简单的 bug。
2.  **改错别字。** 我跟你说，给知名项目的`README.md`改个错别字，是你开启开源之旅的最佳方式。流程简单，基本不会被拒绝，而且能让你完整体验一遍 `Fork` -> `Clone` -> `Create Branch` -> `Commit` -> `Push` -> `Pull Request` 的全过程。
3.  **提 Issue 也是贡献。** 你在使用某个库的时候，发现一个 bug，或者觉得某个功能可以改进。别害羞，去项目的 “Issues” 页面，把你的发现清清楚楚地写下来。怎么复现这个 bug？你期望的结果是什么？实际结果又是什么？这同样是一种非常有价值的贡献。

完成你的第一个 PR，哪怕只是改了个标点符号，当它被合并（merge）进主分支的那一刻，你的 GitHub 主页上就会出现一条 “XXX merged a pull request in YYY repository” 的动态。你可以亲自实践下，很爽的。

### **第四阶段：大三到大四 —— 打造你的 “技术名片”**

到了这个阶段，你已经是个老手了。GitHub 对你的意义，变成了你的另一张简历，一张比你简历上写 “精通 C++” 要可信一万倍的“技术名片”。

这时候，你要开始有意识地去维护自己的 GitHub 主页了。

**怎么做？**

**1、做一个拿得出手的项目。** 把你的课程设计、毕业设计，或者自己做的小玩意儿（比如一个贪吃蛇游戏、一个简单的网站、一个数据分析报告），认认真真地整理好，放到 GitHub 上。

**2、求求了，一定把 README 写好！** 这玩意儿就是你的脸！面试官点进你的项目，第一眼看的就是这个。一个好的`README.md`应该包括：

*   这个项目是干嘛的？（一两句话说清楚）
*   有效果图或者动图展示吗？（一张图胜过千言万语）
*   用了哪些技术？（比如 Python, Flask, PyTorch…）
*   怎么把它跑起来？（提供清晰的步骤，最好一行命令就能搞定）

**3、保持你的 “绿格子” 好看。** 你的 GitHub 主页有个贡献日历，提交了代码就会变绿。这东西不要求你天天刷，但至少别让它几个月都是一片空白。这代表了你的学习热情和持续性。哪怕是每天上去改个文档，写个学习笔记，都能点亮一格。断断续续，但一直在，这就是最好的状态。

4、**Pin 几个你的得意之作。** GitHub 主页可以把 6 个项目钉在最上面。把你觉得做得最好、文档最完善、最有代表性的项目钉上去，让别人一眼就能看到你的亮点。

我之前招实习生，收到两份简历。A 同学简历上写着 “熟悉深度学习，参与过 XX 项目”，B 同学也这么写。但我点开 B 同学的 GitHub，发现他 Pin 了一个项目，是一个用 PyTorch 实现的图像风格迁移的小应用。README 里不仅有效果对比图，还有详细的运行指南和对核心代码的解释。他甚至还把自己调参的过程和遇到的坑写成了一个笔记放在项目里。

我当时几乎没怎么犹豫，就让 HR 约了 B 同学。因为他的 GitHub 已经替他证明了：他不是 “了解”，他是真的 “做过”，而且有总结、有思考。

**最后，说几句掏心窝子的话。**

大一用 GitHub，别指望你能马上写出爆款开源库。先让它成为你 “学习、积累、交流” 的工具，你能熟练到不带脑子就能用 git 操作，那到大二大三做团队项目、科研、甚至兼职开发的时候，你会发现自己无形中多了很多优势。

在大一，用它来备份你的无知和探索；  
在大二，用它来窥探大神们的智慧；  
在大三，用它来小试牛刀，发出你自己的声音；  
在大四，用它来向世界展示你的积累和才华。

坚持下去，几年后，当你回头看你的 GitHub 主页，你会看到一条清晰的、由无数绿色格子铺成的成长之路。

这，就是对你大学四年，最好的交代。

![](https://pic1.zhimg.com/v2-8446e2859bf30d888c1f3109994ac0e0_l.jpg?source=1def8aca)

Seeridia

我自己不会像其他回答或是 b 站的视频那样一口气把 GitHub 讲透彻，我想按照一个循序渐进的方式讲，能让人很舒服地适应 GitHub，同时能够从中学到不少。

部分地方可能我不会教你，因为本篇内容是教 GitHub，其他你需要我会给你提供一个学习路径让你去了解（即便如此，我提供的内容也都是面向没有基础的人）

同时我也会在其中穿插一些 GitHub 的 “礼貌”，并在文中着重展示，请务必注意

（我跳过 GitHub 注册、流畅打开等的这方面的描述，这个自己看看就好）

（为了方便理解，部分用词可能、故意不会很标准）

如果你已经是个 GitHub 的 “专业” 使用者了，也可以在评论中留下想要告诉别人的话、自己踩过的坑，我也会放进去的

* * *

小小的扩列：1034670217（QQ 群）

* * *

首先，不要害怕，GitHub 并不是你想象中的那么遥远，更别一看到全英文的界面就关了，是英文不喜欢就开翻译嘛，有什么。

我下面要提到的内容不会有任何生僻的地方，你大概率也不会看到某一个不懂的名词还要专门去查，而前面很多部分也不需要你知道任何代码，有任何基础

所以，往下滑吧

* * *

## 接触：如何利用 GitHub 获取自己想要的东西

25.3.26 更新

GitHub 作为世界最大的开源项目网站，你不论是不是相关专业的学生，我都很推荐掌握这个基本的内容，而且也无需注册什么的

**那什么时候你需要用 GitHub？**

**很简单，你想偷懒的时候，想找好康的，好玩的时候。**

这个就是最简单的描述

例如，你想大学刷网课，就搜下

![](https://picx.zhimg.com/v2-dcc297d991393682c291b82b368c3ddc_r.jpg?source=1def8aca)

你想下载 b 站的视频

![](https://picx.zhimg.com/v2-ddee5bcb26555fe201e6873d4d910d23_r.jpg?source=1def8aca)

你所想得到的，GitHub 基本都有，也包括漫画平台 all in one、付费音乐下载等（自己去搜搜看）

那该如何使用？你选择一个你想要的项目（仓库）点进去，例如：

[qier222/YesPlayMusic: 高颜值的第三方网易云播放器，支持 Windows / macOS / Linux](https://link.zhihu.com/?target=https%3A//github.com/qier222/YesPlayMusic)

第三方的网易云播放器，点进去如下：

![](https://picx.zhimg.com/v2-c6fc729badc96a18b3429cddcfbf3d1b_r.jpg?source=1def8aca)

点击右侧的 release 页面

![](https://pic1.zhimg.com/v2-2bf980d9d2b69d766fbcb2531093b54e_r.jpg?source=1def8aca)

下面的这个便是安装包，根据文件名选择自己的系统进行下载就行。

简单来说  
Windows 平台就直接找带有 Windows、x64、exe 等字样  
mac 平台：mac、dmg  
安卓：apk  
source code 是源代码，你可以认知：源代码你并不能直接运行，对你来说没用，你需要的是安装包

大部分的项目都是类似的步骤，但也有一部分没有 release，或者 release 中没有安装包文件

对于这些，大部分是需要你自己去构建的（这个操作偏高了一点，之后讲）

**就这样了，你已经能清楚了 GitHub 最最基本的用处——找资源**

* * *

25.3.27 更新

但是很糟糕，你喜欢上了玩崩坏：星穹铁道，但是你懒得天天打本，所以你想偷懒，于是你去 GitHub 上搜索，并找到了这样一个仓库：

[moesnow/March7thAssistant: 崩坏：星穹铁道全自动 三月七小助手](https://link.zhihu.com/?target=https%3A//github.com/moesnow/March7thAssistant)

![](https://pica.zhimg.com/v2-3097ce49018a153b5ecb06f384f1283f_r.jpg?source=1def8aca)

这也太妙了吧，所以你点开了 [Releases](https://link.zhihu.com/?target=https%3A//github.com/moesnow/March7thAssistant/releases) ，看到了如下的目录

![](https://pica.zhimg.com/v2-d8c8336766b10459c77a2078152d1f59_r.jpg?source=1def8aca)

你有点愣住了，不知道自己对应的文件该下载哪个，所以特聪明的你回去主页看了看（主页的那个描述称为 readme 文件，之后会展开讲）

![](https://picx.zhimg.com/v2-6085c0fa799ef2ad3a8df60e9a412320_r.jpg?source=1def8aca)

是的，很多项目会再首页的说明里面告诉你怎么下，但是这个项目也没说下载哪个啊！所以你又看了看

![](https://pic1.zhimg.com/v2-9008405c1e4e3e5b14a44d047421c7f7_r.jpg?source=1def8aca)

7z 和 zip 应该知道，是压缩格式不同，full 估计是完整版的意思？

你不管了，于是随便下载了一个

又根据刚刚下载说明里面写的——解压、打开 March7th Launcher.exe

![](https://pic1.zhimg.com/v2-8e7b2e2a5e26d598ade8958999bbc7d8_r.jpg?source=1def8aca)

好耶！

* * *

从下面开始正式迈入 GitHub

请自行完成注册登录

为什么我这里要你自行完成登录？  
我也不是懒，一来因为这部分没有任何难度，二来我想让你自己能够独立地去尝试、去探索这样一个你目前为止的东西，同时你自己玩着玩着，后面一些我或许没有讲清楚的内容（例如某个按钮、某个页面在哪）的部分你能意识到一点

* * *

以及：请打开 GitHub 自己试试

以及：不管是什么东西，爱折腾永远是学习的第一动力

* * *

## 入门：GitHub 界面——Dashboard

25.3.27 更新

在你完成登录后，我们正式开始了 GitHub 之旅

我们首先来认识一下 GitHub 的界面

在完成登录后，你所看到的便是——个人仪表盘 dashboard

![](https://picx.zhimg.com/v2-5c824cb4017856a14da5b85bf1f1abbf_r.jpg?source=1def8aca)

中间的 Home 即为你的 “关注列表”，这里放着你关注的人或项目（仓库）的 “动态”

左侧即为你自己的 “动态”，含有你的 issue、仓库等等

右侧一般是 “推荐列表”

（你刚注册肯定没啥东西，你都没关注什么呢）

* * *

## 入门：GitHub 界面——你做出的第一个 issue

25.3.27 更新

（该部分开始都需要注册 GitHub 并登录）

你美美的用着 GitHub 上找到的 开源软件，比如刚刚的 三月七小助手，但是不止你自己，你女朋友、男朋友你也得帮着刷，你有个大胆的想法——希望能加入切换账号自动登录功能！

但是 你代码看不懂一点！

不过没事，你可以提意见！

所以我们来解释 issue 功能

在这里打开！

![](https://picx.zhimg.com/v2-e4e3ac43c892e049fda4adf058b9cdcc_r.jpg?source=1def8aca)

issue 里面可以提出你想要的新功能，当然，更多的是反馈 bug，开发者看到后会及时跟进的

**（重要！）但是反馈前有一个礼貌！请提出前一定一定做好两件事**

1.  **当前你使用的是最新的版本**
2.  **你提的 issue 之前没人提过**
3.  **（补充）别把 issue 区当做评论区，有问题发问题，别发一些无关的东西（近些年来经常有某些在国内热门的项目，其 issue 总能被乱七八糟的东西刷爆）**

你确认你自己提出的是最新的，于是你可以用关键词搜搜 “希望能加入切换账号自动登录功能”

很可惜，别人已经提过了

![](https://pica.zhimg.com/v2-5901d3d19afdc593715800021eb3df2c_r.jpg?source=1def8aca)

好吧，于是你就静静等待开发者更新吧＞﹏＜（或者等自己成长起来再自己写！）

不过你急了！你就是想为项目做个自己的贡献！你每日每夜的帮助开发者测试软件，终于让你找到一个 bug！（以下只是我拿一个已有的 issue 举个例子）

你发现 双显示器无法正常工作，只能仅主屏幕 / 仅第二屏运行！并确认了没人提过，于是你点开了 issue 并点了 New issue

![](https://picx.zhimg.com/v2-5b0adfb00c70484f738a87ce5fd32db6_r.jpg?source=1def8aca)

![](https://picx.zhimg.com/v2-c0f291b21db5e6d001ca3d42e4c679ba_r.jpg?source=1def8aca)

当你填完后，好耶！你的问题出现在了 issue 列表上！

就等着别人修吧！

* * *

当然，很多项目提 issue 有时候没有上图的界面，可能就一个这个

![](https://picx.zhimg.com/v2-887d29945bcbe11e7cb49366ca05b17c_r.jpg?source=1def8aca)

那直接写都可以了

当你提交后，这个 issue 在一段时间都会出现在你的 Dashboard 左侧

当然，在 dashboard 的右上角

![](https://pic1.zhimg.com/v2-4a81b931fe244c13c0ff3c50c8fcf2e5_r.jpg?source=1def8aca)

第一个框起来的就是你提过的 issue，第二个就是消息列表

记得留意下你的 issue，可能开发者会向你索取更多信息帮助排查问题，如果你提的 issue 被回复、解决什么的，消息列表就会有小红点

等待一段时间后，开发者便会解决、放弃这个 issue

![](https://pic1.zhimg.com/v2-6c14a3d7f6de9322cfb19f87ac086303_r.jpg?source=1def8aca)

* * *

## 入门：GitHub 界面——除 issue 外的大部分

25.3.28 更新 [babalae/better-genshin-impact: BetterGI · 更好的原神 - 自动拾取 | 自动剧情 | 全自动钓鱼 (AI) | 全自动七圣召唤 | 自动伐木 | 自动刷本 | 自动采集 / 挖矿 / 锄地 | 一条龙 | 全连音游 - UI Automation Testing Tools For Genshin Impact](https://link.zhihu.com/?target=https%3A//github.com/babalae/better-genshin-impact)

![](https://picx.zhimg.com/v2-0a0fb22590869f85e5adaefcf2fe2413_r.jpg?source=1def8aca)

我们已经讲了 release 和 issue，这一部分我将会一口气讲讲其他的东西

是因为其他的比较简单吗，恰恰相反，一部分会更复杂，但是我想循序渐进的讲，目前还是新手章节，所以一些少接触的部分我也只是先简单介绍

先看看最上面的菜单

![](https://picx.zhimg.com/v2-1ff7024378704f9e30d84221222bd65d_r.jpg?source=1def8aca)

左上角的 “babalae/better-genshin-impact”

![](https://picx.zhimg.com/50/v2-6ba5d6b4f97307871dd151d341f922b5_720w.jpg?source=1def8aca)

前面的 “babalae” 是仓库的所有者，后面的 “better-genshin-impact” 则是该仓库的名字

而且如果你看看仓库的网址，那就直接是：[HTTPS://GitHub.com/babalae/better-genshin-impact](https://link.zhihu.com/?target=https%3A//github.com/babalae/better-genshin-impact)

![](https://pic1.zhimg.com/v2-70d7c2679258614add228fcf495de295_r.jpg?source=1def8aca)

1.  最左边是关注该仓库，如果仓库有更新，发版什么的，会在消息列表中通知你
2.  Fork 暂时不管，可以先理解成复制这个仓库到自己名下，至于这样做的原因之后会说
3.  **Starred 是点赞**

**_（重要！）star 是对一个开发者最大的鼓励，意义相当重大！请一定一定不要吝啬！你可以不给这个回答点赞，但是如果你在 GitHub 遇到喜欢的项目，请一定要点赞！_**

**_（star 的数量甚至能写进自己的简历，这样理解你就能意识到 star 的重要性）_**

如果你对一个项目 star 后，如果项目发了一个新版本，那你遍会在 dashboard 的 home 那边收到；区分于这边的 watch，watch 主要是在消息列表通知，而且 watch 不仅能收到新版本通知，也能自定义收到每个 issue、pr 等等

![](https://picx.zhimg.com/v2-662c0a03b69395468682d05f12e1bf1f_r.jpg?source=1def8aca)

### Code

主页、源代码页

该页面主要是一个仓库的源代码和描述

![](https://picx.zhimg.com/v2-f8f7170c27c36d23c400b9aaf7b1caf0_r.jpg?source=1def8aca)

![](https://picx.zhimg.com/v2-d268a1cdb344e573da57dc650980c571_r.jpg?source=1def8aca)

**我们一般把一个项目的 readme 文件 作为一个项目的描述文件，建议不管做什么前都应该先看看 readme 文件**

项目的源代码的最上一层目录中如果放下一个 readme.md 文件，那么在 GitHub 页面下面就会直接显示这个文件的内容作为对该仓库的介绍

同时你可能会在项目的 about 等等地方看到 GPL-3.0 license、MIT license 等字样，这些是该项目的开源协议，包含是否允许商用等条款，这个目前了解即可，后续在自己能够进行开发再去进一步了解

### Pull requests

（跳过 issue）

简称 PR

PR 是直接对项目贡献源代码

原意是发起合并请求，可以理解成自己写了一部分代码，请求合并到原仓库中，所以是发起合并请求

![](https://picx.zhimg.com/v2-85bab4948173441ca87e05ee2c0b88ad_r.jpg?source=1def8aca)

当然，这部分能牵扯进非常庞大的东西，我估计我也讲不动...... 不过我之后应该会放一点 b 站的视频什么的，看看要不我之后开个没用的仓库，让大家体验一下 pr

其他的部分使用非常少，**目前也无需了解**，甚至一些项目没有（部分信息非仓库所有者不可见），只是提一下

*   discussions：讨论，但是有些人会把软件问题提在这里，也不是不行，但还是放 issue 吧（其实大部分项目的 discussion 也没人说话）
*   actions：嗯~ o(*￣▽￣*)o，这个不太好说，是对项目执行自动化任务，例如，如果有人发起了一个 pr，那就在 readme 文件中放上那个人的头像表示欢迎和支持
*   projects：这个一般是来放项目的目前的进展，包含 issue、pr、发版计划等等，（但是大部分项目都不会设置 projects）
*   security：安全性，一般是 GitHub 用于管理和提升仓库代码安全性的工具集
*   Insights：对项目的数据总览，包含贡献者的提交情况，访问流量等等

* * *

回过头，我们看看我们目前接触到的名词

*   issue：提问题
*   pull requests(PR)：贡献代码，发起合并请求
*   dashboard：仪表盘页，“动态列表”
*   readme：项目的描述文件
*   repository：仓库，就是一个项目
*   star：点赞

目前需要了解的就这一点点

* * *

## 入门：GitHub 界面——个人主页

（不包含如何制作，该部分在后续会提）

你可以在 dashboard 界面点右上角的个人头像，再点 Your profile 即可进入

![](https://pic1.zhimg.com/v2-8026346aca00d2299599f3b26e4ab1ac_r.jpg?source=1def8aca)

你作为新用户估计目前蛮空的，也没事！不久就能填起来了！

先介绍下界面

![](https://picx.zhimg.com/v2-f960e203a58422e217e9efa63392a058_r.jpg?source=1def8aca)

*   Overview：首页
*   Respositories：个人仓库
*   Stars：点赞的历史

（其他两个暂时不重要）

![](https://picx.zhimg.com/v2-b75c12ddb84c31e8aea2c82ce33fb7d1_r.jpg?source=1def8aca)

左侧是你的个人信息，自己看看，没啥好说的

*   Achievements：个人成就。就像玩游戏一样，达到某一标准给你个成就
*   Organization：组织，个人可以加入组织，组织在 GitHub 是个很重要的概念，可以有组织自己的仓库，一个组织来共建什么的。但是目前没啥可说的

你也可以点其他人的头像来进去别人的主页，也可以再次关注其他人，别人的动态便会出现在你的 dashboard 的 Home 上了

俺自己是 [Seeridia (Seeridia)](https://link.zhihu.com/?target=https%3A//github.com/Seeridia)，可以偷偷关注我一下吗

![](https://pic1.zhimg.com/v2-1d878b0a5171420c4756caab64462372_r.jpg?source=1def8aca)

个人 readme

你是否记得每个项目有自己的 readme 文件作为项目概要？其实个人也有这样的东西，可以用来装饰自己的主页，这个会在不久后提到

![](https://picx.zhimg.com/v2-47b9afc0e59ca0b6e05dda8cb6c1de64_r.jpg?source=1def8aca)

GitHub 的 Contribution Graph 是最具特色的部分，每个格子是一天，每个格子的绿色的深度反应当天代码的提交量，能把格子填满便是一件很帅的事情

再下面便是自己的动态，自己发起的 issue、pr、提交的代码也会出现在这里

* * *

## 相关前提：markdown

再往下，在创建属于你自己的仓库前，我想向你介绍一下 markdown

完全不用害怕，我想如果我和你面对面坐着，我教你的话大概 15mins 你就能相当熟练的掌握，可惜，在线上，你只能多付出一点点时间，不过，markdown 相当的简单，但也是必学的

markdown 是一种文本文件，文件的后缀为. md，常用于文稿撰写，我们先前提到的 readme 文件便是使用 markdown

我想我们应该知道 txt 和 word 吧？txt 很轻量，啥都没有，word 则很庞大，提供丰富的样式。markdown 则是介于两者中间，有一定的格式，但也不多。

markdown 在相关领域运用广泛，也不仅仅在开发这种方面，很多软件上都支持 markdown，你不妨就在知乎里面随便开个文章或回答，就能看到

![](https://picx.zhimg.com/50/v2-97362cffe62b15808d1fffb9e09511f0_720w.jpg?source=1def8aca)

由于这篇回答是针对 GitHub 的，所以我不会详细的教你（虽然也很简单），我将会在下面更新 markdown 的内容，一样也是很零基础的，很通俗的语言（正在更新中）

怎么用 markdown

[怎么用 markdown 写笔记呢?](https://www.zhihu.com/question/29584213/answer/1889688115016335429)

写笔记呢?

**该内容正在更新中，但是由于比较简单，你也可以直接 b 站学学，很快就可以学会**

* * *

## GitHub 教育认证（可选）

GitHub 教育认证后可以获得一些权益，其中最重要的是 Copilot Pro 的使用资格（虽然最近缩水了一点 QwQ）

**该条目可选**，但需要是大学生身份

以下方法是我自己探索出来的（后面发现也有一些其他人也找到该方法了），目前帮了很多人去做，都 100% 通过。

以下是需要准备的东西

1.  **教育邮箱**（国内高校的邮箱一般是以 [http://edu.cn](https://link.zhihu.com/?target=http%3A//edu.cn) 结尾的，你可以想想有没有印象，当然也有部分学校不提供该邮箱或需要申请，你可以找找辅导员或是学长学姐问问）
2.  **学生证**

下面开始

1.  **配置 2FA 验证**

[GitHub](https://link.zhihu.com/?target=https%3A//github.com/settings/two_factor_authentication/setup/intro)

双因素验证

点上面链接进行配置，该项是目前刚出的规定，有时候需要有时候不用

这个 2FA 可以说下，中文可以叫 双因素验证，就相当于是国内的多加一个验证方式，虽然 GitHub 允许添加我们更熟系的手机号作为第二验证，但是他并不支持国内手机号，所以我们要采用在身份验证器应用，这个或许你们现在不是很熟悉，但是没事，在未来你遇到的业内的很多平台都会使用这种方式。

我们国内平台会要求你提供一个手机号，后续验证就是短信中的一串验证码来验证

而 GitHub 所采用的 “身份验证器应用” ，就是你打开这个应用，他上面就会出现对应的验证码。

这样讲就蛮清楚的吧？

所以我们要**在手机**下载一个 “身份验证器应用”，有很多这种应用，比如：Microsoft Authenticator、CloudOTP 等等。

大部分人可能会选择 Microsoft Authenticator，你可以试试，这个应用在应用商场就能下载，在注册微软账号后使用该应用扫描 GitHub 提供的二维码就行了，它就会被添加到你的 Microsoft Authenticator 中。

而对于安卓用户，我不想让你轻松的完成这一步，我想请你使用 CloudOTP （因为这个软件苹果设备安装困难，就算了）。而这个应用是一个大学生开发的开源项目，作为更简洁专一的身份验证器来使用。

好了，你知道他的名字了，你该如何找到这个软件的安装包？

我教过你吧？

就在上面，去看看？

嗯，没事的，你每次笨拙的尝试都是对 GitHub 的更深一步探索

对，你需要先找到这个仓库，然后呢？

再打开 Release？

再找到你需要的对应版本的安装包？

对的：

![](https://picx.zhimg.com/v2-2c0158db08ab82d81a43d4c4fb1b4016_r.jpg?source=1def8aca)

（这个图在所在的链接我不给了哈，自己想办法）

（图里框起来的就是对大部分安卓能安装的 app）

（安装过程不说了）

下面就是这个 APP

![](https://picx.zhimg.com/v2-c222b0b325849efca8a23e07f03abd2d_r.jpg?source=1def8aca)

右下角扫描屏幕上的二维码后就能添加到你自己的列表了，点击就能看到现在的验证码

把他填到屏幕上的 “Verify the code from the app” 就行了，后面你就可以用这个来验证你自己了！

（后续有一段恢复代码，是当你的验证器出了问题，这个代码就是你的救命稻草，可以把他放在某个地方？比如微信收藏？）

就完成啦！

（当然，你或许刚刚也看到了那个软件 Release 列表最下面有 Windows，或许你可以直接在电脑上就能查阅 “验证码”？ 你想尝试一下吗）

**2. 将你的 GitHub 添加你刚刚找到的教育邮箱的账号**

![](https://pic1.zhimg.com/v2-a0c114dc249659077af7ae606bd10fc1_r.jpg?source=1def8aca)

![](https://picx.zhimg.com/v2-58a9c342705e4c0c770de9a58a55fa52_r.jpg?source=1def8aca)

**3. （重要）关闭你的代理工具，最好人就身处校园，使用校园网更好！！！如果发现这样无法访问 GitHub，那就换个时间段再试试，总之网络一定要正常**

**4. 打开 Billing and licensing 页 下的 Education benefits**

![](https://picx.zhimg.com/v2-ce09997385162182de137620636e172e_r.jpg?source=1def8aca)

这个邮箱填刚刚学校的那个哈

![](https://picx.zhimg.com/v2-29d924d301bfa688f4192370d6331225_r.jpg?source=1def8aca)

然后左下角选择分享你的位置，GitHub 会通过位置判断你在不在学校，不在就之后再搞吧

5. 唔 后续验证过程没图了...

但是我会告诉你一下大概的流程会告知你需要上传一个身份凭证，这时就拿出你刚刚的学生证！翻到首页，包含头像、入学时间等等的那边

**_然后！重点来了！拍照上传照片！注意，不是上传照片，是直接拍照，然后把学生证怼摄像头上，然后点拍照上传！！！_**

**_（虽然有点滑稽，但是这样确实是 0 被拒）_**

6. 等吧，或许审核需要一段时间

然后旁边就会显示

![](https://pic1.zhimg.com/v2-393eed6a277b2ec896b6702a3f7bec69_r.jpg?source=1def8aca)

这就是通过了，但是你的权益将在几天后发放，没那么快哈

![](https://picx.zhimg.com/v2-2529576b579b4d2f98234543eea3d49e_r.jpg?source=1def8aca)

这样就是权益也发放了！！这章结束！

* * *

（之后还会更新的！）

（所以麻烦点赞收藏提醒我回来写！＞﹏＜）

* * *

非常感谢大家看到这里！（虽然还没更完）有啥子问题可以直接加 QQ 群（1034670217）！也可以来找我催更！（实则扩列）

也可以直接加我 1528926919

* * *

内容实在太太太多了 我更新速度肯定比不上大家学的 不过也没事 一方面我也会尽力更新 另一方面 你自己去捣鼓折腾虽然速度慢了点 但是你能学得更深点 用得更熟练些

* * *

这里放上我在 GitHub 最开始的故事，没啥干货，小小的故事而已

为什么程序员们愿意在 GitHub

[为什么程序员们愿意在 GitHub 上开源自己的成果给别人免费使用和学习？](https://www.zhihu.com/question/269033309/answer/101153391280)

上开源自己的成果给别人免费使用和学习？

* * *

下面是个人广告位文章：（求求了，写了那么长的文章，放点广告不要紧吧？）

大学生在我看来，最重要的一课（没有之一）：日程管理

[我有特别的日程管理技巧](https://zhuanlan.zhihu.com/p/1975629573417881939)

![](https://picx.zhimg.com/v2-2be7a09777318d97b11ba03c62a210e8_l.jpg?source=1def8aca)

Javen​​

谢邀，我来分享一下我从大一萌新一路走来用 Github 踩坑的一些经验。

先说个冷知识：GitHub 个人主页其实可以 DIY 成动态简历。在仓库里新建一个和自己账号同名的 repo，写个 README.md 文件，用 Markdown 语法加上动态图标和项目展示，这样你就拥有了一个赛博名片。如果未来找工作，面试的时候能够当着面试官介绍你在 Github 上的项目，会很加分。

Github 上有很多优秀的开源项目，要复刻或者学习开源项目，首先需要定一个目标，自己想要学会哪些东西，比如说想学习操作系统，可以复刻一个开源小型操作系统的实现，如果想自己搭建一个个人博客，可以照着开源博客实现前后端程序，或者只是想了解一点一些有意思的项目，可以确定自己想要使用的技术栈，看看有没有人做过。

Github 上的资源很丰富，所以你先得学会如何过滤信息，检索自己需要的内容，下面是一些搜索技巧：

**1. 关键词组合搜索**

*   **按技术栈**：`language:python stars:>1000`（搜索 Python 项目，星标超 1000）
*   **按主题**：`topic:machine-learning` 或 `topic:web-development`
*   **按文件名**：`filename:README.md`（找有详细文档的项目）
*   **排除词**：`NOT tutorial`（过滤教程类仓库）

**2. Awesome 系列**

*   搜索 `awesome [技术名]`，如 `awesome-react`，获取高质量资源合集。
*   直接访问 [Awesome Lists](https://link.zhihu.com/?target=https%3A//github.com/topics/awesome) 主题页。

**3. 趋势项目**

*   访问 [GitHub Trending](https://link.zhihu.com/?target=https%3A//github.com/trending)，按日 / 周 / 月查看热门项目。
*   筛选语言（如 Python、JavaScript）关注新兴技术。

学会如何检索之后，就可以开始自己的学习之路了，有个小建议是刚开始复刻开源项目的时候最好选择文档丰富，社区氛围好的来尝试，不然很容易一开始就卡死，丧失了继续学习的动力。

千里之行始于足下，如果你从大一就可以开始自己写项目做项目，相信你在毕业的时候一定会感谢大一的自己的。