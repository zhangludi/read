.. _articles1256:

你用Linux命令行吗？
===================

2009年8月14日 `陈皓 <http://coolshell.cn/articles/author/haoel>`__

想一想，如果你要把一个图片的尺寸改小一点，你会怎么办？当然，我一定会启动一个图形编辑软件，然后，打开图片文件，从菜单上选择相关的工具选项，更改大小，然后保存文件。就算是在Linux下，我可能也是这么干的，比如Ubuntu下也是这样，如下图：

|photo\_gimp|

但其实，如果你用命令行来更改图片大小的话，一条语句就可以搞定了。如：

::

    convert -resize 300 profile.jpg profile_small.jpg

当然，如果你要使用这样的命令，你需要安装\ `Imagemagick <http://www.imagemagick.org/script/index.php>`__\ ，你可通过apt-get
install imagemagick来安装一下。

不管怎么说，很简单吧，下面还有几个：

**1）给图片加阴影**

给图片加阴影可以使用下面的这个命令：

::

    convert screenshot.jpg
    \( +clone -background black -shadow 60×5+0+5 \)
    +swap -background white -layers merge +repage shadow.jpg

效果如下：

|screenshot-suse|\ |shadow| 

**2）把两个MP3拼起来**

::

    cat 1.mp3 2.mp3 > combined.mp3

**3）克隆一个硬盘设备**

::

    dd if=/dev/hda of=/dev/hdb

**4）把ISO文件刻录光盘**

::

    cdrecord -v speed=8 dev=0,0,0 name_of_iso_file.iso

**5）视频格式转换**

AVI和Mpeg转换

::

    ffmpeg -i video_origine.avi video_finale.mpg
    ffmpeg -i video_origine.mpg video_finale.avi

查看这个\ `链接 <http://www.catswhocode.com/blog/19-ffmpeg-commands-for-all-needs>`__\ ，你可以看看ffmpeg可以干得更多。

**6）替换文件中的文本**

::

    sed ’s/#FF0000/#0000FF/g’ main.css

把main.css中的#FF0000(红色)替换成#0000FF（蓝色）

 

如果你非常喜欢命令行的话，那么你一定要看一下下面这本书（免费在线）

GNU/Linux命令行介绍：\ `http://en.flossmanuals.net/gnulinux <http://en.flossmanuals.net/gnulinux>`__

（全文完）

.. |photo\_gimp| image:: /coolshell/static/20140921230114033000.png
   :target: http://coolshell.cn//wp-content/uploads/2009/08/photo_gimp.png
.. |screenshot-suse| image:: /coolshell/static/20140921230114304000.jpg
   :target: http://coolshell.cn//wp-content/uploads/2009/08/screenshot-suse.jpg
.. |shadow| image:: /coolshell/static/20140921230114362000.png
   :target: http://coolshell.cn//wp-content/uploads/2009/08/shadow.png
.. |image9| image:: /coolshell/static/20140921230114486000.jpg

.. note::
    原文地址: http://coolshell.cn/articles/1256.html 
    作者: 陈皓 

    编辑: 木书架 http://www.me115.com