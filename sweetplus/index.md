# 微信小程序开发总结


<h2>产品简介</h2>
<p>SweetPlus是一款基于烘焙蛋糕类食品的菜谱查找的微信小程序。旨在让喜爱做烘焙的用户可以快速查找到想要的菜谱，同时我还增加了节日的分类目录，让烘焙也变成一种有仪式感的事情。因为做烘焙的过程是甜甜的，做出的成品是甜甜的，那么查找做法的过程必然是更加甜的，所以我将这款小程序命名为SweetPlus。甜一点，再甜一点，更甜一点！<br></p>

<h2>目标用户</h2>


<p>任何可能想要做烘焙或者其他菜的人</p>

<h2>主要功能</h2>

<p>查询任何想要的做的甜品或者菜肴，以及在对应节日中通过节日分类查询到相应的食物的做法。对自己喜爱的菜谱进行收藏以及对现有的菜品的做法进行改进并上传发布给开发者。</p>

<h2>开发过程</h2>

<p>这款微信小程序是用云开发实现的，使用云开发数据库调用聚合数据中的菜谱大全的api对数据进行调用，通过wxss的样式改变将菜谱展示出来。</p>

<p>增加收藏按钮，点击按钮，自动将当前事物的id存入collectlist收藏列表中，通过对数据库food集合的查询从而将已经收藏过的食物做法展现在页面上。</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>增加改良按钮，点击按钮，跳转到发表页面，发表文字和图片，成功存入云开发数据库中。</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>以下是部分调用数据库的代码截图</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":90} -->
<figure class="wp-block-image"><img src="http://ycardiac.cn/wp-content/uploads/2019/06/图片.png" alt="" class="wp-image-90"/></figure>
<!-- /wp:image -->

<!-- wp:image {"id":91} -->
<figure class="wp-block-image"><img src="http://ycardiac.cn/wp-content/uploads/2019/06/图片-1.png" alt="" class="wp-image-91"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p><br></p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2>开发成果</h2>
<!-- /wp:heading -->

<!-- wp:image {"id":93,"width":284,"height":476} -->
<figure class="wp-block-image is-resized"><img src="http://ycardiac.cn/wp-content/uploads/2019/06/JN5U@V8GZL87D1EMO4.png" alt="" class="wp-image-93" width="284" height="476"/></figure>
<!-- /wp:image -->

<!-- wp:image {"id":92,"width":257,"height":410} -->
<figure class="wp-block-image is-resized"><img src="http://ycardiac.cn/wp-content/uploads/2019/06/YRH4FXVRK9MEJ4G.png" alt="" class="wp-image-92" width="257" height="410"/></figure>
<!-- /wp:image -->

<!-- wp:image {"id":94,"width":301,"height":302} -->
<figure class="wp-block-image is-resized"><img src="http://ycardiac.cn/wp-content/uploads/2019/06/Q3ZARZGCK6LJ4IL2P.png" alt="" class="wp-image-94" width="301" height="302"/></figure>
<!-- /wp:image -->

<!-- wp:image {"id":95,"width":306,"height":481} -->
<figure class="wp-block-image is-resized"><img src="http://ycardiac.cn/wp-content/uploads/2019/06/D5J09U_Z__LQ5QRDMYV.png" alt="" class="wp-image-95" width="306" height="481"/></figure>
<!-- /wp:image -->

<!-- wp:image {"id":96,"width":288,"height":501} -->
<figure class="wp-block-image is-resized"><img src="http://ycardiac.cn/wp-content/uploads/2019/06/15UJXE3WXHM67W2X1V0KQ.png" alt="" class="wp-image-96" width="288" height="501"/></figure>
<!-- /wp:image -->

<!-- wp:heading -->
<h2>开发心得<br></h2>
<!-- /wp:heading -->

<!-- wp:list -->
<ul><li>一定要养成良好的代码备份的习惯，充分利用git,不然泪水是流也流不完的。</li><li>做不论是微信小程序还是其他项目的开发，一定要确定好需求，所有界面的逻辑，界面UI设计等等基本设定好之后动手去写代码，不然写的过程真的挺迷茫的，效率又不高。</li><li>开发过程中出现了挺多语法和逻辑错误，最好的解决办法就是啃官方文档，一遍一遍的仔细读微信小程序官方文档api调用的例子，问题总会迎刃而解的。</li></ul>
<!-- /wp:list -->
