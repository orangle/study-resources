MySQL
======

>  MySQL也有了几年了，说不出来个所以然，认知比较肤浅。所以需要加深学习呀，这里是学习过程中收集的一些好的资源，希望大家共同进步了。不是很系统的整理，看到了就记录了下来。

官方文档必须要优先看滴呀！[本文Github地址](https://github.com/orangle/study-resources)

## 博客
前辈们的博客就是他们成长的足迹。

* [DimitriK's (dim)](http://dimitrik.free.fr/blog/archives/cat_mysql.html)
* [MATSUNOBU Yoshinori](http://yoshinorimatsunobu.blogspot.ca/) MHA作者
* [玄惭](http://hidba.org/) 阿里
* [何登成](http://hedengcheng.com/) 阿里
* [叶金荣](http://imysql.com/) 知数堂
* [姜成尧](http://www.innomysql.com/) 网易
* [杨奇龙](http://blog.itpub.net/22664653/) 支付宝
* [penglixun](http://www.penglixun.com/) 阿里
* [王朝阳](http://www.royalwzy.com/)
* [大师兄](http://www.cnblogs.com/gomysql)
* [吴老师](http://wubx.net)  知数堂
* [黄杉](http://blog.csdn.net/mchdba)
* [周振兴](http://www.orczhou.com)  一个故事@MySQL DBA
* [for dba](http://fordba.com/category/mysql)
* [那海蓝蓝的博客](http://blog.163.com/li_hx/)  Oracle 对mysql，pg都比较多
* [四爷](http://blog.csdn.net/yueliangdao0608) msyql，pg很多对比
* [smalldatum](http://smalldatum.blogspot.com) facebook， 很多myrocks文章
* [宋利兵老师公众号](http://mp.weixin.qq.com/profile?src=3&timestamp=1485068751&ver=1&signature=97zp7qqm-wQSzWOAuHTac-wiNLUHTJMLOPyDgtnGluclBugccyOmXRDaBn2vTZ1pit9I9gfD5*T*dmzlHojIKw==) 宋利兵老师公众号 Oracle， innodb原理分析
* [Jean-François Gagné](http://jfg-mysql.blogspot.ca/) Booking.com 的数据库工程师

* [淘宝数据库内核月报](http://mysql.taobao.org/monthly/)
* [planet mysql 中文](https://planet.mysql.com/zh/)
* [awesome-mysql](https://github.com/shlomi-noach/awesome-mysql/blob/gh-pages/index.md)
* [db ranking](http://db-engines.com/en/ranking) 数据库排名
* [mariadb 官方整理的MySQL知识库](https://mariadb.com/kb/en/mariadb/optimization-and-tuning/)
* [Percona Database Performance Blog](https://www.percona.com/blog/) 貌似每个dba对这个博客都特熟悉，没事多看看


## 文章
经验分享，或者是针对一些问题的分析，解答

* [大众点评订单分库分表](http://tech.meituan.com/dianping_order_db_sharding.html) 200g订单表开始做水平拆分的一些记录
* [MySQL 排序内部原理](https://mp.weixin.qq.com/s/oVl0Ih86CWT77npdS5cF1g)
* [MySQL备份经验](https://mp.weixin.qq.com/s/TxveGZK9o2QBEJbx1Vd9MA) 线上紧急备份等的操作
* [Mysql操作规范](http://blog.itpub.net/29320885/viewspace-1716164/)
* [阿里云DBA专家门诊](https://bbs.aliyun.com/read/189202.html)  问题比较基础，特意提了下不要使用外键的事（当然也是看场景)
* [阿里云DBA专家门诊](https://bbs.aliyun.com/read/241176.html) 主要集中在覆盖索引
* [MySQL5.6新特性之Muti-Range Read](http://blog.itpub.net/22664653/viewspace-1673682/) 当看到执行计划中有 mrr的时候就是它了
* [为什么不建议innodb使用亿级大表](http://xiaorui.cc/2016/12/08/为什么不建议innodb使用亿级大表/) innodb的存储方式和索引方式
* [MySQL大数据场景的优化和运维-美团DBA](https://mp.weixin.qq.com/s?__biz=MzAwMDU1MTE1OQ==&mid=209403337&idx=1&sn=f99429e24e8c591111a355e072f93e05) 非常多的可以参考和操作的内容，可以作为手册使用， 建议多看几遍
* [联合查询中的驱动表问题](http://www.cnblogs.com/zhengyun_ustc/p/slowquery1.html)  不同的写法可能造成查询优化器无法选择正确的驱动表，从而整个查询的扫描范围增加，最后的目的就是用 `小结果集驱动大结果集`
* [MySQL 加锁处理分析](http://hedengcheng.com/?p=771)  完美的串联了mvcc 锁机制 隔离级别的知识
* [innodb锁机制 Next-Key Lock 浅谈](http://www.cnblogs.com/zhoujinyi/p/3435982.html) 从小案例的角度来说明 Next-Key Lock算法在RR隔离级别下解决幻读问题的原理
* [MySQL · 答疑解惑 · MySQL 优化器 range 的代价计算](http://mysql.taobao.org/monthly/2015/11/07/) 使用 optimizer trace 来分析一个代价计算的案例
* [MySQL 5.7的新增功能白皮书（中文版）](https://mp.weixin.qq.com/s/pmycCxLM_9vzrMsX4eDFFQ) MySQL5.7 版本特性全面的介绍，如果还没有正式使用5.7版本，请仔细阅读阅读。
* [MySQL Join算法与调优白皮书（四）](https://mp.weixin.qq.com/s/vt7YjxaikJh14pnY2FAWvg) 姜老师的系列文章，深入浅出的讲解了 MySQL join算法的原理和使用中需要注意的细节
* [MySQL高可用浅析](http://www.jianshu.com/p/cc6746ac4fc2) 唐刘老师的对mysql复制部分的总结
* [MySQL半同步复制的数据一致性探讨](https://mp.weixin.qq.com/s/3DeXEd2ZjjutxRyo_3coaQ)


### 案例分析

[How to deal with MySQL deadlocks](https://www.percona.com/blog/2014/10/28/how-to-deal-with-mysql-deadlocks/) 遇到mysql死锁问题时候怎么查询，还有避免死锁的几种思路。第一个通过 ` SHOW ENGINE INNODB STATUS` 查找死锁信息，第二个回忆GAP锁知识


## slides

* [一步步深入MySQL源码](http://hotpu-meeting.b0.upaiyun.com/2014dtcc/post_pdf/hedengcheng.pdf) 何登成，怎么深入的学习Mysql的一些经验和建议
* [RDS最佳实践](https://bbs.aliyun.com/read/168647.html) 玄惭， 问题查询和数据库设计方面的建议
* [MySQL索引和SQL调优](https://bbs.aliyun.com/read/189202.html?displayMode=1&page=3#601628)   玄惭，innodb索引的原理以及案例分析
* [MySQL数据库开发的三十六条军规-石展](http://wenku.baidu.com/view/3e294a52f01dc281e53af0f1.html) 数据库开发中的一些经验规则总结，非常有参考性
* [MySQL基础技能与原理--基础技能](http://www.slideshare.net/plinux/mysql1-5066095)  彭立勋老师, 一个系列 MySQL，Oracle都有涉及 （基于5.1版本）
* [MySQL基础技能与原理--高级应用](http://www.slideshare.net/plinux/mysql2-5066096)
* [MySQL基础技能与原理--基本原理](http://www.slideshare.net/plinux/mysql3)
* [MySQL培训优化篇](http://www.slideshare.net/sunmonth/mysql-24283118)  东西比较多，几乎所有方面
* [MySQL Explain 解读](http://www.slideshare.net/sky000/mysql-explain) 简朝阳大师， 结合例子说明的非常详细了
* [MySQL查询优化浅析](http://hedengcheng.com/?p=372) 代价模型，了解mysql索引选择原理
* [Query Optimization with MySQL 5.6: Old and New Tricks](https://www.slideshare.net/jynus/query-optimization56)
* [Advanced MySQL Query Tuning](https://www.slideshare.net/AlexanderRubin1/meetup-tour-queryoptimizationnew)
* [Mysql query optimization](https://www.slideshare.net/caibaohua/mysql-query-optimization-4719028)
* [MySQL秒杀场景优化--杨德华](https://github.com/ThinkDevelopers/PHPConChina/blob/master/PHPCON2017/MySQL%E7%A7%92%E6%9D%80%E5%9C%BA%E6%99%AF%E4%BC%98%E5%8C%96--%E6%9D%A8%E5%BE%B7%E5%8D%8E%40PHPCON2017.pdf) phpconchina2017的一个演讲，视频地址是[这里](http://www.itdks.com/dakalive/detail/2291), 通过秒杀场景中的库存问题来说明线程池和死锁问题的知识


## videos

* [IT大咖说](http://www.itdks.com/dakashuo/index) 里面有一些mysql的分享，不过需要自己找下了。（还需要注册）

## 在线学习

* [sqlzoo](https://sqlzoo.net/) 在线的sql练习，比较适合入门
* [oracle live sql](https://livesql.oracle.com/apex/livesql/file/toc.html#A7) oracle 官方的sql案例，都是oracle的案例，不过也可以参考下。。


## 工具

* [binlog2sql](https://github.com/danfengcao/binlog2sql) 大众点评，闪回和binlog解析sql,  还不错哦
* [python-mysql-replication](https://github.com/noplay/python-mysql-replication) Mysql复制工具库，可以基于它开发很多东西了
* [innotop](https://github.com/innotop/innotop) innodb引擎监控工具，perl语言的一个脚本
* [orchestrator](https://github.com/github/orchestrator)


## 项目

* [phxsql](https://github.com/Tencent/phxsql/wiki) 微信开源的集群方案
* [MyRocks](https://github.com/facebook/mysql-5.6/wiki) 使用rocksdb做为底层存储，上层实现sql引擎，思路很棒
* [AliSQL](https://github.com/alibaba/AliSQL/wiki) 阿里开源，对mysql官方版本的增强版本

## 书籍 or doc

* 《高性能MySQL》  必读，多读几遍
* 《MySQL技术内幕:InnoDB存储引擎》 姜老师的书，多读几遍
*  [MySQL Internals Manual](https://dev.mysql.com/doc/internals/en/) MySQL 内幕，官方开发团队维护，了解mysql内部机制的有效资料

## 经典文献
*  [Architecture of a Database System 中英文版](http://dblab.xmu.edu.cn/post/architecture-of-a-database-system/) 中文版由厦门大学数据库实验室翻译

* [ARIES: A Transaction Recovery Method Supporting Fine-Granularity Locking and Partial Rollbacks Using Write-Ahead Logging](https://people.eecs.berkeley.edu/~brewer/cs262/Aries.pdf) 很多年前（1992）IBM关于 wal log的论文，现代数据库事务恢复机制很多基于此。再来几个相关的slides [ARIES Recovery Algorithm](http://codex.cs.yale.edu/avi/db-book/db4/slide-dir/Aries.pdf) , [ARIES (& Logging)](http://odin.cse.buffalo.edu/teaching/cse-462/slides/18-Logging.pdf) , [(Database) Techiques Everyone Should Know](https://blog.acolyer.org/2016/01/03/database-techiques-everyone-should-know/)
