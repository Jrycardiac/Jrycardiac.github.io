# 微信小程序 开发第四周


## 微信小程序-开发第四周
## 用mockdata 伪造小程序后台数据
对于一个小程序小白来说，还要搭后台才能利用数据看出测试效果简直是太麻烦了，而且调用理想网站的API还经常会报错误，所以这时候建立一个伪后台就显得尤为舒服。

 1. 在小程序文件夹页面添加文件夹 data(名字当然是随便取啦）
 ![在这里插入图片描述](https://img-blog.csdnimg.cn/20190407152533402.png)
 2. 在文件夹里新建js文件添加你想要测试的数据，
    例如我想要做一个轮播图：


```
var localdata = {
  "bannerPic":[{
    pid:6,
    imgUrls: '/image/b3.jpg'
  },{
      pid: 7,
      imgUrls: '/image/b2.jpg',
  },{
      pid: 8,
      imgUrls: '/image/b1.jpg',
  }],
```
这是我们的数据文件，**pid**是对应的标号，方便后面调用。

 3. 然后在需要使用数据的对应页面文件夹下的js文件开头添加


```
var mockData= require('../../data/homedata.js');
```
就可以用我们刚刚添加的数据啦

 4. 当然wxml文件也需要写出调用：

```
<swiper indicator-dots="true" autoplay="true" interval="{{interval}}" duration="{{duration}}" circular="true">
    <block wx:for="{{productlists.bannerPic}}" wx:key="{{index}}">
      <navigator url="details/details?pid={{item.pid}}">
      <swiper-item >
       <image src="{{item.imgUrls}}" class="slide-image" width="100%" />
      </swiper-item>
       </navigator>
    </block>
  </swiper>
```
比如在实现点击跳转时，**pid**就可以派上用场啦。

 5.  这就是最后实现的效果啦，没办法上传动态图，不过轮播的效果还是想象的到的吧嘻嘻。
 ![在这里插入图片描述](https://img-blog.csdnimg.cn/20190407154542716.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxMjIwNDg0,size_16,color_FFFFFF,t_70)
 6. 这个方法一般只适合于比较少的数据量，如果需要大量数据的伪数据后台可以使用类似EasyMock的在线工具。[点我去EasyMock网站看看](http://easy-mock.com)

 关于教程应该到处都有的，我这里就不贴了。类似这样的工具应该还有蛮多，大家可以自己去发现噢！

 这周就是这样啦，我们下周再见!下周的任务要做基类继承等等的任务了。
