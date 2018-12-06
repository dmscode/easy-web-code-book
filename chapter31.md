第三十一章 还是海报
===

报告读者，本人正在直播……直播写作，接受监督，但是我就不告诉你们在哪里直播。

以下为注释 `<!-- http://live.bilibili.com/21024 -->`

好了，今天废话不多说，开始我们的正文。你的啤酒准备好了么？

前边我们写了导航栏、写了大海报，你也许觉得这还是在入门，好简陋好简陋的，但是其实呢，这已经是我们常用知识中的大部分了。不信你看，今天的内容几乎完全是在复习的样子啊。

那么呢，作为一个 App 发布页面……额，虽然已经被我写得不伦不类的，你就当成那个样子去看好了，毕竟我这么帅，你们会原谅我的对不对？

好啦，为了展示它的特性呢，它是谁？不是你想的那个样子啦，是为了展示我们要发布的这个根本不存在的 App 的某些引人入胜的特性，我们要多加几张海报。你说把前边海报部分复制一下就 OK 啦，反正也是，但是我要是那么懒，你们还不打死我？再说了，千篇一律的版式也不方便糊弄老板啊！所以下边两个海报的样式总要变一变的。

第一张呢，左边文字，右边一张什么什么 LOGO 或者 ICO 什么的，哎呀，不说那么高大上了，放个剪切画的意思。第二张就是把这两边换换，左边剪切画，右边文字，当然啦，他们都有通栏的背景，这样显得符合潮流……其实是符合老板恶俗的审美啊。

那么开始我们的工作，第一张海报……算了，这么懒的我肯定是两张一起写了，首先是 Html ：

```html
<div id="post-a">
	<div class="post-content">
		
	</div><!-- .post-content End -->
</div><!-- #post-a End -->
<div id="post-b">
	<div class="post-content">
		
	</div><!-- .post-content End -->
</div><!-- #post-b End -->
```

然后是一些基础的 CSS 样式控制，我不用讲你也看得懂啦。你看你们老说学不会啊、看不懂啊，现在为啥就能看懂了？切，根本就没那么难嘛~

```css
#post, #post-a, #post-b  {
	width: 100%;
	height: 450px;
}
#post {
	background: url(../images/bg.jpg) center -250px;
}
#post-a {
	background: url(../images/bg-a.jpg) center 0px;
}
#post-b {
	background: url(../images/bg-b.jpg) center -250px;
}
.post-content {
	width: 960px;
	height: 100%;
	margin: 0 auto;
	overflow: hidden;
	color: #EFEFEF;
	text-align: center;
}
```
以上是我修改/添加的 CSS ，大家看看发生了什么变化？为什么捏？#post, #post-a, #post-b 三者样式区别不大，所以干脆放在一起定义一下相同部分，然后再分别设置背景好了。.post-content  样式是可以共用的，那就共用好了，所以去掉 #post 的约束。然后来看看效果，这次有点长……

![](http://coffee.zji.me/imgs/31-1.png)

现在开始填写海报里的内容，几乎跟第一张海报是一样的。什么什么？你说我偷懒？分明就是复制了第一张海报在糊弄？其实你把下两张海报的高度改低点（或者高点），然后设置个纯色背景就挺高大上的，不过好像比现在的还简单……所以我没偷懒好伐？！

现在给第一张海报加上一个图标，一段文字。Html 代码如下：

```html
<div id="post-a">
	<div class="post-content">
		<div class="post-text">
			<h3>帅的那样让人心醉</h3>
			<p>让你忍不住多看了一眼又一眼</p>
		</div>
		<div class="post-icon">
			<img src="images/icon-a.png" alt="">
		</div>
	</div><!-- .post-content End -->
</div><!-- #post-a End -->
```

我多复制了两层，所以呢，你应该可以知道这代码是写在哪里的了。首先我们去看看当前混乱的局面，然后我们再去规范他的样式。

![](http://coffee.zji.me/imgs/31-2.png)

看看，随手一放，就是这么的别有风味，现在我们开始设置一下他的样式，等设置完成就变得俗不可耐，十分讨老板欢心了。

```css
.post-content .post-text {
	float: left;
	width: 510px;
	padding-top: 165px;
	font-size: 28px;
	line-height:  60px;
}
.post-content .post-text h3 {
	margin: 0;
	font-size: 36px;
}
.post-content .post-icon {
	float: left;
	width: 256px;
	height: 256px;
	padding: 97px;
}
.post-content .post-icon img {
	width: 256px;
	height: 256px;
}
```

这些 CSS 我就不逐一的解释了啊，你们可以通过审核元素去理解他们为啥那么写。两个元素都 `float:left` 是为了横排；图片占了 450×450 的面积，左边剩下 510宽的面积给文字，通过一些属性的设置使得文字在他的位置内居中。

然后效果如下：

![](http://coffee.zji.me/imgs/31-3.png)

这基本就达到了我们的预期，当然要说严谨的话还要清除一下浮动才好，当然如果不清除其实也出不了什么问题，因为各种属性的限制，现在的布局其实不至于乱掉，当然只是表面上看起来，事实上道理并不是讲的很通，反正加不加看你喽。

现在第二张海报……其实好简单的，只要你把 Html 写一下就好。

```html
<div id="post-b">
	<div class="post-content">
		<div class="post-icon">
			<img src="images/icon-b.png" alt="">
		</div>
		<div class="post-text">
			<h3>其实做人要谦虚的</h3>
			<p>你看作者从来不说自己帅</p>
		</div>
	</div><!-- .post-content End -->
</div><!-- #post-b End -->
```

然后就行了呢，因为他要用到的 CSS 我们在前边都已经定义了呢~好啦，看一下整体的效果就可以结束这节课了哦。（其实底下还有悄悄话，我不告诉你）

![](http://coffee.zji.me/imgs/31-4.png)

你看，你看，这效果还是看得过去的……吧？

其实我就是为了把各种情况演示一下啦，所以做的不伦不类的，你们可不许这样，要认真哦！困，我先去睡会。

> **本章学习卡片：[卡片 31](http://coffee.zji.me/card.html?name=chapter31)**

> **本章代码下载：[本章代码](http://coffee.zji.me/show-code/31.zip)**

---

**本书是收费的，不过交费凭自觉。**价格定义为每人请我喝一杯咖啡（哪种品质的咖啡随意），支付宝账号：

> **alay9999@163.com  （刘源）**

**本书现已重写，最新版内容请查看主站更新。**本书目前除主站之外，仅授权站酷、极客学院 Wiki发布，其他站点均为无授权盗载。

* 主站（2018 新版上线）：https://dmnydn.com/

未经本人许可，禁止任何形式转载。相关事宜请联系： dms@zji.me