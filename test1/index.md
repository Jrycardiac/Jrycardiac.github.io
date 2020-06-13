# SQL安装总结


# SQL server 2017  安装过程问题总结




 - ## 首先推荐一个非常好用的公众号——软件安装管家。
 大部分我们常用的软件破解版都可以在这里找到。当然我安装SQL server 2017
   安装包以及教程都是在这个公众号找到的。[在此附上连接](https://mp.weixin.qq.com/s?__biz=MzIwMjE1MjMyMw==&mid=2650199061&idx=1&sn=5b8a140237d95929fbcaed26800c3ef5&chksm=8ee174f9b996fdef42a525a844a83864dad22ec741302a0d3ddd0d58c29d0b5b70c2671102bb&mpshare=1&scene=23&srcid=0319EtNegXdmVgb6IZEHlmUZ#rd)

   

 - ## 之后按照安装教程一步一步进行，有几个重要的步骤需要注意。

   

 1. 在你想要安装的盘中新建文件夹jre 1.8，可将软件更改安装位置，这个对于之前安装位置错误还是有很大的帮助的。

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190416113158120.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxMjIwNDg0,size_16,color_FFFFFF,t_70)

   

 2. 修改path环境变量时，发现我的电脑中弹出的并非一条属性值，而是多条，这样就不知道该如何修改了。

       **解决办法**：可将教程中需要修改的直接添加，然后将刚添加的属性值直接移到开头，便可以解决问题啦。（JDK的安装应该在之前学JAVA的时候就已经安装好了，后来出现问题，在命令行窗口中 执行 “java”命令即可验证。）

 3. 安装SQL server ,在进行这一步时不能安装教程来勾选全选，这样后面的步骤中会出现错误提示: R服务相关未完成之类的。

       **解决办法**： 带有‘R’的选项全部不选。

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190416114013198.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxMjIwNDg0,size_16,color_FFFFFF,t_70)

 4. 接下来按照教程一步步进行就没问题啦。但是SQL server 安装成功之后，并不是我们课上使用的工具。我们需要的是SQL的manage
    工具。所以打开一开始的安装中心界面点击第二条安装即可。
## 其实有了上面的安装包和安装教程就已经成功了90%，只需要注意我上面提到的几点再结合教程认真一步一步来，安装还是很容易的.

   

  
