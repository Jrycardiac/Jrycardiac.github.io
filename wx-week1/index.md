# 微信小程序第一周周报


# 微信小程序-尝试开发第一周
## 刚开始开发小程序流的泪和犯的蠢

 - 使用tabBar建立底部导航栏时图标上传失败
导入图标的时候，一直出现...jpg文件不存在，上传失败等这样的错误(忘了截图求放过），后来仔细检查，以及阅读小程序文档发现图标大小超过40KB,无法上传，于是修改了图标大小，完美解决。小程序文档还是要仔细读一读的！
![](https://img-blog.csdnimg.cn/20190317020937476.png)
 - 逗号 以及是否支持注释
 在写.json的配置文件以及.js文件中data的配置时，要注意最后一个括号中的语句是不加逗号的。（虽然很低级的错误，但我经常犯，也真的很无奈了)还有一点就是json文件是不支持加注释的。
 ![](https://img-blog.csdnimg.cn/20190317021036909.png)
 - **在页面中添加背景图片**
 <!-- wp:paragraph -->
***前来更新 ，屡次尝试之后发现官方给的云开发的例子中的<strong>添加图片方式</strong>并不能在手机端显示（应该我尝试过程中出现了问题，但一直没有解决），所以去找文档<strong>，发现图片处理应该直接用&lt;image>来写，而且url图片路径中不能出现中文，使用本地图片的src应该使用绝对路径。</strong></p>
<!-- /wp:paragraph -->
<!-- wp:paragraph -->
**一把辛酸泪，好好读文档才是最重要的**
<!-- /wp:paragraph -->
我其实在这个方面浪费了挺长时间的，一开始在wxss文件中添加image属性，无果，后来在wxml文件的模块中尝试直接添加style="background-image= .....",问题还是没有解决。。然后百度一下，发现答案不外乎下面这几种：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190317021119161.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxMjIwNDg0,size_16,color_FFFFFF,t_70)![在这里插入图片描述](https://img-blog.csdnimg.cn/20190317021129392.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxMjIwNDg0,size_16,color_FFFFFF,t_70)![在这里插入图片描述](https://img-blog.csdnimg.cn/20190317021140172.png)但这些方法要么麻烦（比如那个base64)要么没用（比如我之前试过的），所以我还是决定去瞧瞧官方给的例子，果不其然！
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190317021200951.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxMjIwNDg0,size_16,color_FFFFFF,t_70)![在这里插入图片描述](https://img-blog.csdnimg.cn/20190317021210481.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxMjIwNDg0,size_16,color_FFFFFF,t_70)好吧，完美解决。之前尝试失败的原因居然是 url。**还有一个要注意的是，语句 background-size: cover 功能是背景图片自动缩小比例适配模块**，妈妈再也不用担心我得手动调整图片比例了：）
 - 出现错误json文件找不到
 ![在这里插入图片描述](https://img-blog.csdnimg.cn/20190317021308813.png)错误显示未找到文件，但我清楚地看到文件在那里，里面内容也没报错啊。百度无果。最后惊醒自己刚刚好像改了整个文件所在文件夹的名字...改回名字，问题解决。这一天天的都是些什么错误呀。

 - 小程序text文本换行 \n
 ![在这里插入图片描述](https://img-blog.csdnimg.cn/20190317021400546.png)
 - text文本居中 使用flex 关键性语句justify-content：center;
    ` display: flex;
 	align-items: center;
	 justify-content：center;`
	

##  尝试的第一周的学习成果

模型图、第一个界面的完成以及小程序的基本架构
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190317021704954.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxMjIwNDg0,size_16,color_FFFFFF,t_70)在这里插入图片描述![在这里插入图片描述](https://img-blog.csdnimg.cn/20190317021936847.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxMjIwNDg0,size_16,color_FFFFFF,t_70)![在这里插入图片描述](https://img-blog.csdnimg.cn/20190317021749320.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxMjIwNDg0,size_16,color_FFFFFF,t_70)
## 下周学习计划
<!-- wp:paragraph -->
<p>这周主要用来做小程序模型图和首页前端，对于真正的开发还没有开始吧。</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>下周会在界面写完学有余力的情况下学习云函数、云开发。</p>
<!-- /wp:paragraph -->
