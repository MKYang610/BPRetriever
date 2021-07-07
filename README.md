# Prgiect of Batch Paper Retriever
请文明检索,按照实际需求量下载
## 简要说明
1. 编译版exe在release里面（页面右边→），解压压缩包，双击里面的exe文件即可运行。<br>
2. 源码版中BPRetriever.py是主程序脚本，基础包需要自己安装。<br>
3. wos数据库检索可能需要校园网环境。pubmed数据库检索时需要输入一项邮箱的参数，我不确定用户增多以后用同一邮箱检索，访问量变大是否会被封IP，因此要求修改成自己的邮箱。其它的我自认为已经做到了傻瓜式GUI，应该不需要太多额外教程。
## 该项目整合了之前大神们的代码，并进行了修改，包括<br>
wos爬虫：https://github.com/tomleung1996/wos_crawler<br>
Entrez检索: https://www.cnblogs.com/xiaolan-Lin/p/14030607.html<br>
Scihub下载: https://www.bilibili.com/video/av375139410/<br>
另外还对有其它一些代码进行了参考，但一时想不起来或找不到，就不一一列出了。<br>
#### 在此对所有共享代码的作者表示感谢！
## 目前软件功能包括：
### 1.一键检索关键词下所有历史文章
一次性检索上千篇文章，支持pubmed和web of science数据库，通过输入关键词或检索式检索下载。所有文献记录会被导出到一个excel表格，包括每篇文章的标题，年份，作者，2021版的影响因子，文章被引次数（仅wos数据库），原文地址等。对于想快速了解一个新领域，或需要撰写综述及论文的使用者，通过简单的表格排序即可了解该领域的核心文章（高影响因子，高被引次数）。而我个人也在使用过程中发现了许多遗漏的文章，还是挺有用的。
### 2.一键下载所有检索到的文章
一次性可以下载上千篇文章，从scihub批量下载文献（不依赖校园网），pdf以年份标题来命名（直接从检索信息提取，不会出现乱码的情况）。由于最新1年的文章大部分都还没上scihub，这部分文章需要手动下载，excel表格会更新下载成功或下载失败的信息，点击原文链接可手动下载。
### 3.文献推送功能
设定推送间隔以及打开自动检索功能以后，在下次打开软件时，可以自动查找自上次检索时到现在这段时间新发表的文献，并弹出对话框进行推送。
## 写在最后
撰写该程序的起因是我看文献的速度可以说是受限于下文献的速度，而我是一个比较懒的人，想到要复制粘贴标题，找原文主页，下载后还要重命名，很多时候就打退堂鼓了。<br>
现有软件也能实现部分功能，但各有各的缺点，导致我使用频率不高。例如stork可以推送文献，但我隔一个月不看就要回头一封一封邮件找，相互割裂很难抓到重点。而公众号推送的文章国内占比大导致不够全面。Endnote和ScihubEVA可以批量下载文章，但检索信息导入麻烦，文件名称也是乱码。<br>
21世纪是计算机的时代，自然要发展自动化办公。本来设想的是从每周文献推送到pdf下载实现自动化一条龙，但碍于种种限制暂时还没办法实现。但对于python现学现用的我来说，实现了80%的目的，已经是很满意了。
PS.，编程小白，源码以能用为原则，不够优雅清晰，欢迎吐槽改进。<br>
另外bug可以在comment或邮件告诉我，但是佛系更新。<br>
