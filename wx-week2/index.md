# 微信小程序第二周周报


# 微信小程序—尝试开发第二周

## 上周实现了一些基本的图片处理,这周继续页面进行改进。同时，和老师讨论之后，决定新增加社交功能以及自己搭配配方等功能。

 - **微信小程序轮播图的实现**
 如果对之前js的轮播图掌握较好的话，那么对照小程序官方文档应该是容易掌握的。下面直接贴代码了。
index. js:

```
 data: {
    indicatorDots: false,
    autoplay: false,    //是否自动切换
    interval: 3000,   //自动切换时间间隔
    duration: 800,  //滑动动画时常
  },
```

  index. wxml
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
然后在.wxss文件里设置需要的高度和宽度即可。

 - json文件中   一些小细节
 开发过程中"navigationBarTextStyle": 后面填写颜色的十六进制码会报错 ，提示应该为“black”或“white”。  查阅文档发现，仅支持白和黑，我又一次弱智了?。

 - 分类界面设计

js文件
```

Page({
    data: {
        category: [
            {name:'面包',id:'guowei'},
            {name:'饼干',id:'shucai'},
            {name:'蛋糕',id:'chaohuo'},
            {name:'冰淇淋',id:'dianxin'},
            {name:'饮料',id:'cucha'},
            {name:'原料管理',id:'danfan'}, //各类的名字以及id ，id方便后面使用。
        ],
        detail:[],
        curIndex: 0,
        isScroll: true,
        toView: 'guowei'  //第一个界面的类目
    },
    onReady(){
        
                this.setData({
                  detail: mockData.catelists
                })
         
        
    },
    switchTab(e){
      const self = this;
      this.setData({
        isScroll: true   //局部滚动，tab栏切换
      })
      setTimeout(function(){    //定时器
        self.setData({
          toView: e.target.dataset.id,
          curIndex: e.target.dataset.index
        })
      },0)
      setTimeout(function () {
        self.setData({
          isScroll: false
        })
      },1)
        
    }
    
})
```
之后在wxss设置自己想要的样式就可以啦！

## 下周开发计划

打算把 社交以及配料表和更改配方界面写完，云开发暂未提上日程。

