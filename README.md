#### 我为什么要学习Linux的命令行？

​	在我小时候看过一部电影，电影的名字叫[《我是谁：没有绝对安全的系统》](www.naidu.com)，年轻的黑客坐在笔记前对着黑洞洞的CMD窗口快速敲出几行命令就将公寓的供电系统断电，公寓瞬间黑暗暗了下来，同时我对技术的向往也被如黑洞般的CMD吸引。

![](F:\Code\个人项目\gitbook-linux\IMG\p2317421915.jpg)

​	后来才得知这是C语言的代码...



​	由于我的职业为[前端工程师](https://baike.baidu.com/item/%E5%89%8D%E7%AB%AF%E5%BC%80%E5%8F%91%E5%B7%A5%E7%A8%8B%E5%B8%88)，工作中鲜有接触到[命令行](https://baike.baidu.com/item/%E5%91%BD%E4%BB%A4%E6%8F%90%E7%A4%BA%E7%AC%A6/998728?fromtitle=%E5%91%BD%E4%BB%A4%E8%A1%8C&fromid=196110)，最多执行的是前端的老三套，webpack、node、Vue...，业余时间虽然也有接触，但局限于用到的时候查，不用了就丢在一边，令我想要重新学习Linux命令行的原因是因为公司内的项目跑在Linux机器上，看着其他部门的同事熟练的敲出命令行，我仿佛又回到了电影中，所以我打算写一个关于学习Linux命令行的文档，送给想要学习的人。

### Linux是什么？



​	Linux是一个开放源代码的类[UNIX](https://zh.wikipedia.org/wiki/UNIX)操作系统。该操作系统的内核是由林纳斯·托瓦兹于1991 年 10 月 5 日首次发布。



​	![png](F:\Code\个人项目\gitbook-linux\IMG\LinuxCon_Europe_Linus_Torvalds_03.jpg)



​        老外通常用自己的名字命名....

​	如果严格来讲，Linux只是单纯的指的是Linux操作系统的内核，因为操作系统中包含了其他的东西，比如：桌面环境和各种各样的工具。现在，很多人经常说“欸，你用的Linux系统吖”，但其实是使用的基于Linux内核的操作系统。

​        Linux可以跑在各种各样的设备上，比如平板、PC、手机、路由器、电视，而我们经常使用的Android手机也是创建在Linux内核上面的。

​	通常情况下，我们使用的Linux系统是使用Linux内核和其他的程序打包成Linux发行版，就像我之前使用的[Ubuntu](https://www.ubuntu.com/)(但是因为我需要接触到微信开发，并在一次删除软件的时候误操作删掉了某些东西，导致系统的桌面无法启动，还好我可以使用Linux命令行的方式将我的文件导出，但是！！！由于Linux命令行中的中文乱码，我只能将最外部的文件夹导出，所以...在Linux中不要用中文创建文件夹是正确的事情....)，还有其他的Linux发行版，比如[Centos](https://www.centos.org/)、[Debian](https://www.debian.org/)...还有其他的发行版，根据主要提供的功能不同打包成不同的Linux操作系统，比如黑客经常使用的[Kali Linux](https://www.kali.org/) (我只知道这一个)...

#### 我将怎么学习Linux命令

​	我会从最基本`cd`命令开始，由浅入深的学习，实际上我也不知道我会学习到哪种深度，我只能走一步看一步。