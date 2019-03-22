# 第2节：date

上一篇我们讲到了`date`命令的简单用法，现在，让我们来深入看一下。

在**终端**中，输入下面的字符。

```
man date
```

![](F:\Code\个人项目\gitbook-linux\Chapter1\img\1552309940(1).jpg)

让我们尝试分析一下终端反馈给我们的结果。

我们需要关注的有两点，第一是`SYNOPSIS`和下方的`DESCRIPTION`，

**SYNOPSIS**告诉你怎么使用`date`命令

**DESCRIPTION**告诉你`date`命令主要有哪些参数，怎么使用

让我们来分析下，`date`的`选项`吧！

```
-d --date=STRING : display time described by STRING，not 'now'
// 用字符串描述时间，并显示出来
```

```
-f --file=DATEFILE ：once for each line of DATEFILE
//显示DATEFILE文件中的每行时间
```

```
-R ==rfc-2882 ：output date and time in RFC 2882 format. Example: Mon，14Aug 2006 02:34:56 -0600
// 以RFC-2822兼容日期格式显示时间
```

```
-rfc-3339=FMT ：output date/time in RFC 3339 format. FMT='date','seconds'，or 'ns' for date and time to the indicated prec=sin. Example:2006-08-14 02:34:56-06:00
// 以RFC-3339兼容日期格式显示时间
```

```
-r --reference=FILE ：display the last modification time or FILE
// 显示文件的最后修改时间
```

```
-s --set=STRING ： set the described by STRING
// 设置时间为string格式
```

```
-u --utc,--universal ：print or set Coordinated Universal Time (UTC)
// 显示或设定为Coordinated Universal Time时间格式
```

```
--help ：display this help and exit
// 显示帮助信息
```

```
--version ：output version information and exit
// 输出版本
```

```
FORMAT controls the output.  Interpreted sequences are:
// 对日期进行格式化
```



下面，让我们用`date`来做点事情吧！

对了，在你阅读这篇学习笔记的时候应该看一下现在是几点钟了，那么让我们用高大上的方式来看一下吧！

```
date -d 'now'
// 反馈
Web Mar 13 23:29:17 CST 2019
```

假如你的基础和我一样差的话可能会说，这***是什么鬼东西？

最基本的 `13`、`23:24:16`、`2019`我还是可以看懂的，那么其中的 `Web`、`Mar`、`CST`**是什么意思呢？**

| 我不懂的 | 我懂了                |
| -------- | --------------------- |
| Web      | Web是周三英文的简写   |
| Mar      | Mar是三月的英文的简写 |
| CST      | CST则是标准时间的意思 |

我看懂了他们的意思，可是我记不住，怎么办呢？

**我在这里将周一到周日的简写，1月份到12月份的简写记了下来。**

1. 星期日：Sunday，Sun
2. 星期一：Monday，Mon
3. 星期二：Tuesday，Tue
4. 星期三：Wednesday，Wed
5. 星期四：Thursday，Thu
6. 星期五：Friday，Fri
7. 星期六：Saturday，Sat

当然，还有**1月份到12月份**

1. 一月：January，Jan 
2. 二月：February，Feb 
3. 三月：March，March
4. 四月：April，Apr 
5. 五月：May，May 
6. 六月：June，Jun
7. 七月：July，Jul
8. 八月：August，Aug
9. 九月：September，Sep 
10. 十月：October，Oct
11. 十一月：November，Nov
12. 十二月：December，Dec 



那么，现在我们能看懂了吧？

shell给我们的反馈是:**周三 三月 13日 23：29：17 标准时间 2019年**



当然了，还有一件事！

**在15天前我女朋友给我寄了一件毛衣，我想知道是几号，我用`date`的话该怎么用呢？**

```
date -d '15 days ago'
//反馈
Tue Feb 27 00:01:45 CST 2019
```

啊！我知道了，是**周二 二月份  27号 2019年！**，还好我女朋友问我的时候我知道是哪天了...



当然了，还有一件事！

**我女朋友说，一个月零一天后她的闺蜜要过来玩，要我准备准备时间，看看那天有没有时间一起玩**

天哪！女人就是这么奇怪！一个月零一天后，哇哦，我怎么知道！！！

啊对！我还有`date`，我要问一问它！

```
date -d '1 month 1 day'
// 反馈
Mon Apr 15 00:06:11 CST 2019
```

哈哈，我知道了！是**周一 四月 15日 **



当然了，还有一件事！

**我女朋友的生日我还记得，我想从现在起每天给女朋友折一只千纸鹤，那么到我女朋友的生日我叠了多少呢？**

```
date -d '23 Oct' +%j
// 反馈
296
```

嗯...**296**只...我先懒上几个月在叠吧...



当然了，还有一件事！

**对了，我想到 一件事，我想看这些英文该怎么办呢？毕竟在我的生活中我最常见的是2019-03-13这种的，那么我们这么做？**

```
date -d 'now' +%F" "%T
//反馈
2019-03-14 00:22:38
```

这里要注意！

在我们的+号前面要添加一个空格，而我们想要拼接日期的时候，想用空格分割的时候也需要添加**字符串空格!**



**这个+号的作用则是格式化我们的时间，获得我们想要的输出结果**



在这里，我只讲到了`date`的基本用法，你可能对我在`date`中的+号后面的有些陌生，别担心，我把format的用法列了张表，你可以参考一下。

%n : 下一行 

%t : 跳格 

%H : 小时(00-23) 

%I : 小时(01-12) 

%k : 小时(0-23) 

%l : 小时(1-12) 

%M : 分钟(00-59) 

%p : 显示本地 AM 或 PM 

%r : 直接显示时间 (12 小时制，格式为 hh:mm:ss [AP]M) 

%s : 从 1970 年 1 月 1 日 00:00:00 UTC 到目前为止的秒数 

%S : 秒(00-60) 

%T : 直接显示时间 (24 小时制) 

%X : 相当于 %H:%M:%S 

%Z : 显示时区 

%a : 星期几 (Sun-Sat) 

%A : 星期几 (Sunday-Saturday) 

%b : 月份 (Jan-Dec) 

%B : 月份 (January-December) 

%c : 直接显示日期与时间 

%d : 日 (01-31) 

%D : 直接显示日期 (mm/dd/yy) 

%h : 同 %b 

%j : 一年中的第几天 (001-366) 

%m : 月份 (01-12) 

%U : 一年中的第几周 (00-53) (以 Sunday 为一周的第一天的情形) 

%w : 一周中的第几天 (0-6) 

%W : 一年中的第几周 (00-53) (以 Monday 为一周的第一天的情形) 

%x : 直接显示日期 (mm/dd/yy)

%y : 年份的最后两位数字 (00.99) 

%Y : 完整年份 (0000-9999) 



上面的例子中只展示了`date`显示时间，那么接下来，让我们一起去**设置**服务器的时间吧！

![1553180408(1)](A:\开源\linux-gitbook\Chapter1\img\1553180408(1).jpg)

这是我们当前的时间，如果我们需要将时间改为`2019-03-22`该怎么改呢？

**在终端中输入**

```
date -s "019-03-22 11:11:11
```

这条命令中的`-s`就代表着**设置**的意思。

这时候终端会反馈给我们设置的时间。

让我们在看看设置的时间吧！

![](A:\开源\linux-gitbook\Chapter1\img\1553181421(1).jpg)



这是**设置**时间的操作。

我想在把时间还原回去该怎么做呢？

不要着急，我在后面的文章中会告诉你的。





注意辣！这里只是**展示`date`命令的基本操作**更多的东西需要大家去发现！
