.. _201005_the_first_view_of_vp8:

Vp8视频格式初探
==================================

`ruanyifeng.com <http://www.ruanyifeng.com/blog/2010/05/the_first_view_of_vp8.html>`__

昨天，Google发布了一个开源项目\ `WebM <http://www.webmproject.org/>`__\ 。

这个项目的目的，是在文件格式方面，为制作和发布互联网视频提供了一个开源的解决方案。

WebM采用MKV作为封装格式，里面的音频编码用Vorbis格式，视频编码用VP8格式。

MKV和Vorbis都是早就存在的开源格式，而VP8本来属于On2公司的封闭格式，是不开源的。去年8月，Google花了1亿美元收购On2，才有了今天。

这个决定轰动了业界，因为这意味着，我们终于有了一个没有专利约束、并且获得大公司支持的免费视频编码格式VP8（详见我翻译的\ `《HTML5视频格式之争》 <http://www.ruanyifeng.com/blog/2010/05/html5_codec_fight.html>`__\ 一文）。

但是，VP8其实只是一种规格，以前从来没有公开过，也没有任何基于它的产品问世。所以，外界一直不知道VP8的性能究竟如何。

开源视频转换程序ffmpeg的开发者之一Jason
Garrett-Glaser，有机会提前接触到了VP8。他写了一篇很详细的\ `评估 <http://x264dev.multimedia.cx/?p=377>`__\ ，说出了自己对VP8的印象，并将VP8与专利格式H.264做了比较。

下面就是这篇评估的简单翻译，删去了讨论技术细节的部分。


=======================

**VP8视频格式初探（精简版）**

作者：Jason Garrett-Glaser

译者：阮一峰

原文网址：\ `http://x264dev.multimedia.cx/?p=377 <http://x264dev.multimedia.cx/?p=377>`__

| 
| **一、On2是一家怎样的公司？**

在开始讨论VP8之前，我想先谈谈对On2公司的印象。

它曾经宣称，VP8比H.264的性能高出50%。但是，它的话是不可信的。因为它也说过，VP7比H.264的性能高出15%。但是后来人们发现，VP7远远不如H.264。

2003年，On2宣布VP3开源。表面上，它好像为开源事业做出了贡献。但是实际上，它的目的是，希望开源社区为它修正错误。Theora项目上了当，选择VP3作为自己的代码基础，结果修改代码的时间用去了6年，做出来的产品性能还是不如H.264。

**二、VP8的规格**

这份规格文件令人很不满意。很多技术细节，不是写得太简单，就是写得太模糊。大部分地方都是直接张贴C代码，而不是用文字表述。要知道C代码和格式规格，完全是两回事，根本不能替代。

我曾经觉得，H.264的规格写得太啰嗦，但它至少是准确的。VP8的规格根本就是不清晰，不准确，太简短，很多细节没有解释清楚。老实说，仅仅根据这份规格，地球上根本不可能有人能够写出VP8的解码器。

更令人惊奇的是，根据代码中的注释，VP8有些部分写于2004年初，比H.264还要古老！On2在此后6年的时间中，都不做修改，这是说不过去的。

**三、VP8编码器（Encoder）**

首先要明确一件事情。格式规格和它的具体实现，是两回事。一个很好的编码程序，可能是基于一个很烂的规格；而一个很好的规格，也可能会产生出一个很烂的编码程序。

原厂提供的解码器，生成的图像质量虽然大大好于VP3，但是并没有明显胜过H.264的地方。

这个编码器的编码速度要慢于H.264。我的机器是1.6Ghz的Core
i7，编码1080p时速度为26fps；而用H.264编码器，选择”最快速度”选项时，可以达到101fps。

在压缩性能方面，VP8也不如H.264。

**四、VP8解码器（Decoder）**

原厂提供的VP8解码器，比ffmpeg的H.264解码器慢了16%，更不要说其他更先进的H.264解码器了。

就算最终通过各种优化，VP8解码器可以达到H.264的同样水平。但是，H.264有众多硬件支持，而VP8只能靠软解码，所以谁快谁慢不言而喻。

**五、专利问题**

VP8的一大卖点，就是没有专利权问题。但是，它的某些细节与H.264太像，我觉得已经很难用巧合解释了，将来肯定会出现专利纠纷。

在没有明确证据表明VP8通过专利检验之前，我建议使用时一定要非常谨慎。

**[附录]**

Youtube已经开始提供WebM视频了，不过只有最新的浏览器才支持。具体的观看方法请查看\ `http://www.ghacks.net/2010/05/20/webm-video/ <http://www.ghacks.net/2010/05/20/webm-video/>`__\ （英文）。

（完）

.. note::
    原文地址: http://www.ruanyifeng.com/blog/2010/05/the_first_view_of_vp8.html 
    作者: 阮一峰 

    编辑: 木书架 http://www.me115.com