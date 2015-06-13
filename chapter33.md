第三十三章 一个页尾
===

其实写到这里，页尾大家应该都会做了的，还是那点知识而已，我都懒得写了，而且我猜性急的朋友应该也都写出来了。算了，虽然很无聊，但是还是写一遍好了。

老板说就这么多内容吧，然后你觉得如释重负啊！可是呢，就算这样也不能完啊，就算是虎头蛇尾总也是要给他一个结尾的啊。

其实结尾跟咱们的导航部分有点类似啦，都是一个通栏，然后中间一个居中的区域用来放内容啊。所以嘛，到了后面简直就是没什么新鲜的东西的啊。

来，我们先来写一个简单单的催眠一下。反正我也已经很困了啊

好啦，依旧是千篇一律的先来点 Html（糊涂妹啦）：

```html
<div id="footer">
	<ul>
		<li><a href="#">公司简介</a></li>
		<li><a href="#">关于我们</a></li>
		<li><a href="#">联系我们</a></li>
		<li><a href="#">服务条款</a></li>
		<li><a href="#">帮助中心</a></li>
	</ul>
</div><!-- #footer End -->
```

内容是我瞎写的，不用在意，这个不要我去解释了吧。其实很简单的说。然后我们去定义一些 CSS （彩色式）

```css
#footer {
	background:#F3F3F3;
	border-top: 3px solid #EFEFEF;
}
#footer ul {
	width:800px;
	margin: 0 auto;
	padding:15px 0;
	overflow: hidden;
}
#footer ul li {
	float: left;
	margin: 0;
	width: 160px;
	list-style: none;
	text-align: center;
}
#footer ul li a {
	text-decoration: none;
	color: #333;
}
```

到了这里我就不去过多的解释 CSS 了，因为我们用了很多遍了好吗？你应该差不多看懂了，否则大家该怀疑我故意占篇幅换稿费啦~（虽然并没有什么稿费……哭……）只是说一下：#footer ul  中的 `overflow: hidden;` 是用来清除浮动的，好啦，你又学了一个小小的新技能哦。来看看效果吧：

![](http://coffee.zji.me/imgs/33-1.png)

就是这么的简单，这根本就是前边的内容啊，分明作者……还是骗稿费的……（然后真的并没有稿费啊！）

当然这些都不要紧，关键是，要是老板看了这些教程，会觉得果然就是个骗工资的，于是责令整改啊，要做一个高大上的，跟那谁家小谁的网站一个样式的页尾……

不是说好不改了的嘛，哎，谁叫人家是老板捏！捏！，你懂的，说到捏，你有木有觉得很解气啊！但是还是要把工作做掉的，所以……前边的推翻重新来~

```html
<div id="footer">
	<div class="footer-content">
		<ul>
			<li><a href="#">公司简介</a></li>
			<li><a href="#">关于我们</a></li>
			<li><a href="#">联系我们</a></li>
			<li><a href="#">服务条款</a></li>
			<li><a href="#">帮助中心</a></li>
		</ul>
		<ul>
			<li><a href="#">公司简介</a></li>
			<li><a href="#">关于我们</a></li>
			<li><a href="#">联系我们</a></li>
			<li><a href="#">服务条款</a></li>
			<li><a href="#">帮助中心</a></li>
		</ul>
		<div id="qrcode">
			<img src="images/qrcode.png" alt="">
		</div>
	</div><!-- .footer-content End -->
</div><!-- #footer End -->
```

别，别在意内容，我已经比刚才更加的随意了……嘘，老板现在不在身边。

至少，内容丰富了不是？那就好了，我就是糊弄下老板，你们……可别糊弄自己哦！

然后是 CSS ，其实，还是那点东西……

```css
#footer {
	padding: 30px 0;
	background:#F3F3F3;
	border-top: 3px solid #EFEFEF;
}
#footer .footer-content {
	width: 960px;
	margin: 0 auto;
}
#footer ul {
	float: left;
	width:300px;
	margin: 0;
	padding:0;
}
#footer ul li {
	padding:10px 0;
}
#footer ul li a {
	text-decoration: none;
	color: #333;
}
#qrcode {
	float: right;
}
#qrcode img {
	width: 250px;
	height: 250px;
}
```

然后你让我给你们解释什么？哪一句没学过？你指出来，我马上就划掉！来看看效果~

![](http://coffee.zji.me/imgs/33-2.png)

然后这章就结束了哈！但是你要自己动手试试哦~我一个页面都讲完了，你们也该写出个什么页面了吧？？记得交作业哦，虽然我不看，你们先努力把自己的页面写好写漂亮，后面我会告诉你们怎么把他们发布到网上去，跟你的女盆友们炫耀……虽然她们其实更在乎怎样把自己的照片修的美美哒~

好了，下一章我们讲点新鲜玩意儿~

> **本章学习卡片：[卡片 33](http://coffee.zji.me/card.html?name=chapter33)**

> **本章代码下载：[本章代码](http://coffee.zji.me/show-code/33.zip)**

---

**本书是收费的，不过交费凭自觉。**价格定义为每人请我喝一杯咖啡（哪种品质的咖啡随意），支付宝账号：

> **alay9999@163.com  （刘源）**

为了让大家阅读方便，本书将在如下站点发布，但最终内容以主站为准：

* 主站首发： http://coffee.zji.me/
* Gitbook: http://codeme.gitbooks.io/easy-web-code-book/
* 简书： http://www.jianshu.com/users/d37eaf3de0ff
* 站酷： http://www.zcool.com.cn/u/12927742

未经本人许可，禁止任何形式转载。相关事宜请联系： dms@zji.me