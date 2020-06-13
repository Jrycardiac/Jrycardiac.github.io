# 微信小程序 开发第三周


# 微信小程序开发第三周
上周结合老师提出的意见对页面进行了整改，经过这一周的努力还是没有想到原料管理和焙圈（没错，我只是给它取了个名字而已）该具体怎么搞，于是我把原有不变的功能的页面改进了一下，对于一个具体烘焙作品的细节页面做了一些调整。

 - css中的animation属性
 animation是CSS3中新增的属性，它可以制作出多种酷炫的动画效果，和flash也有一定的联系。
 比如  我尝试做的是点击商品名称旁边的收藏按钮，小心心图标会向右上角的?缓慢移动。
 代码如下：
 ![在这里插入图片描述](https://img-blog.csdnimg.cn/20190330224127727.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxMjIwNDg0,size_16,color_FFFFFF,t_70)
当然animation也有其他的属性
**动画名称**

```


 /*1.name：动画名称*/
/*-webkit-animation-name: kf_play;*/
 /*-moz-animation-name: kf_play;*/
 /*-o-animation-name: kf_play;*/
 /*animation-name: kf_play;*/


```
**动画的持续时间，即播放一次动画所需的时间**

```
 /*2.duration：动画持续时间*/
 /*-webkit-animation-duration: 2s;*/
 /*-moz-animation-duration: 2s;*/
 /*-o-animation-duration: 2s;*/
 /*animation-duration: 2s;*/

 
```

**动画播放速率曲线，这个属性与transition的一样。**

```


 /*3.animation-timing-function：动画播放速率曲线*/
 /*-webkit-animation-timing-function: linear;*/
 /*-moz-animation-timing-function: linear;*/
 /*-o-animation-timing-function: linear;*/
/*animation-timing-function: linear;*/
/*其他可选值：ease | linear | ease-in | ease-out | ease-in-out*/


```
这里解释一下ease ease-in等的表示含义
这些是控制移动的方式也可以说是速度，在我的代码块中提到的是ease-out 表示的是以缓慢结束的方式移动，ease-in相反的就是以缓慢开始的方式移动。
另外animation的属性还有好多好多这里就不一一列举了。
