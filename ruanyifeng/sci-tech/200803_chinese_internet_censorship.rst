.. _200803_chinese_internet_censorship:

中国的互联网审查
===================================

`ruanyifeng.com <http://www.ruanyifeng.com/blog/2008/03/chinese_internet_censorship.html>`__

美国\ `《大西洋》 <http://www.theatlantic.com/>`__\ 月刊的驻华记者\ `James
Fallows <http://jamesfallows.theatlantic.com/>`__\ ，每个月都要发表一篇中国报道。今年1月份，他谈了中国的外汇储备，这个我已经\ `介绍 <http://www.ruanyifeng.com/blog/2008/01/why_chinese_love_saving_money.html>`__\ 过了。最新一期则是关于中国的\ `互联网审查 <http://www.theatlantic.com/doc/print/200803/chinese-firewall>`__\ ，也就是著名的GFW。

他说，今年8月份，奥运会召开的时候，会有很多外国人来到北京。这些人住进酒店后，第一件事也许就是打开电脑上网。

他们的第一印象也许是，中国的互联网很慢。这是正常的，一个原因是数据传输必须经过太平洋海底的光缆，另一个原因是所有数据都会经过自动审查，所以变慢了。中国互联网的国际出口主要有三个：北京、上海和广州。这三个出口都安装了特殊设备，会自动过滤数据。

有消息说，奥运会期间，网络管制将会放松。在外国人居住的酒店和新闻中心，将可以自由上网。不过当奥运会结束，一切又会恢复正常。

在中国上网，从输入网址到网页最终显示，有四个审查的环节：

**1.
DNS过滤。**\ DNS是域名服务器的缩写，它的作用是将域名转换成IP地址，这被称为地址解析。在中国，有些网站的IP地址是不被解析的，会显示”Site
not
found”（网站找不到）的提示。另一情况是，给出错误的IP地址，比如访问google的时候，却会显示百度。

**2.
IP地址黑名单。**\ 当你从DNS服务器得到正确的IP地址后，系统会检查这个IP地址是否在黑名单中。如果是的，那么将出现”The
connection has been reset”（连接被重置）的提示。

**3.
url过滤。**\ 鉴于某些网站会经常改变IP地址，所以会直接禁止它们的网址。当你的url中含有这些网址时，也会显示”连接被重置”。

**4.内容过滤。**\ 每一个网页的具体内容也是被审查的，一旦其中包含违禁词语，连接会立刻被重置。具体表现是，网页只显示了一半，然后突然就断了，怎么刷新也不出来。一旦出现这种情况，系统会自动将你的IP与对方IP之间的联系切断10分钟。值得注意的是，这一步过滤是双向的，从国外访问国内的网页，也会被内容过滤。另外，它对电子邮件也有效，所以Email里如果包含敏感词语，往往无法发送到国外，一定要用加密邮件才行。

违禁的IP地址都会被记录下来，那些经常违禁的地址，最后会出现在政府的名单上。

（完）

.. note::
    原文地址: http://www.ruanyifeng.com/blog/2008/03/chinese_internet_censorship.html 
    作者: 阮一峰 

    编辑: 木书架 http://www.me115.com