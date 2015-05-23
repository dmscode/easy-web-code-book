第二十二章 导航条（七）
===

现在我们来学着解决问题哦，我们还有一个遗留问题没有解决，就是页面底下的滚动条。你肯定又说了：“你还是知道解决啊？你不知道我都看着碍眼好多章了么？”这个不怨我啊，你们看看我的截图，我的系统是超细滚动条，所以我看着一点也不碍眼啊！（好了，可以扔砖头了，我好捡回家盖房子娶老婆……）

方法很简单啊，右键审查元素，然后鼠标在代码里划过每个元素，看看最可能是哪个元素引起的问题。

然后我就觉得最可能是这里出了问题，为啥啊，这么多元素，就它的宽度比我窗口宽度还大（我当前窗口的宽度为 800px）。

![](http://coffee.zji.me/imgs/22-1.png)

你看，其实查找问题也未必很难，那么究竟是出了什么问题呢？这里我们猜猜啊，我们知道他如果遵循我们设置的宽度的话，那么他的宽度应该是 100% ，当前也就是 800px（body 元素当前的宽度值）。再看看我们加的内补，左右各 30px。这要是 `800+30+30=860` ，正好是当前元素的宽度。这应该就是问题的原因了。

那么这里涉及到两个问题。第一个，我们设置的宽高到底是什么？其实我们设置的宽高，不是元素边框（边界）的宽高，倒更像是元素内可用面积的宽高。就好像我们说的不是快递箱的尺寸，是他加上填充物之后还能装多大面积的东西，理解没？

所以元素的实际尺寸（从边框开始测量），实际上是设置的宽高加上内补的尺寸。就是快递箱的尺寸等于里面的东西再加上填充物的尺寸。**说简单点就是箱子里填充物（内补，padding）的多少会影响箱子的大小（元素的实际面积），当然外面裹多少泡泡纸（外补，margin）都不会影响箱子的大小**。

这就理解了，那么内补我们并不想去掉，因为想着在左右留点空白用的。看来只能动宽度了。那宽度应该改作多少？其实去掉就可以了，因为**块元素(display:block)不浮动的情况下默认填满一行**。（这是第二个问题，详见 VIP 章节之 关于浮动的故事）

于是，去掉了 #nav 的宽度之后，我们获得了一个虽然简陋，但是确实看得过去的导航条。

![](http://coffee.zji.me/imgs/22-2.png)

回想我们学了这么多节课，其实主要在说一些基本的 CSS 知识了，真正看我们写下的代码却没有几行，再看看代码，差不多也能看懂一二了，好像也不过如此。

这是一个完整的导航了？当然不是，不过毕竟从无到有，从难看到现在看的过去，我们完成了一轮创造的过程，算得上是我们学习过程中一个重要里程碑！

如果到这里你基本都明白了，那么我来带着你做点坏事哦，挺简单的，我们把当前的 #nav 部分的 Html 代码复制一遍，修改一下 id（id 不能重复啊，而且我们也需要用他进行一些区分），这么说有点抽象，来看一下我改过之后的代码（我只粘贴 body 标签之间的喽～）

```html
<div id="nav">
	<div id="logo">
	<a href="#">代码能有多难？</a>
	</div>
	<ul id="nav-items">
		<li class="nav-item"><a href="#">首页</a></li>
		<li class="nav-item"><a href="#download">下载</a></li>
		<li class="nav-item"><a href="#feature">特点</a></li>
		<li class="nav-item"><a href="#about">关于</a></li>
	</ul>
	<ul id="nav-items-r">
		<li class="nav-item"><a href="#signin">登录</a></li>
		<li class="nav-item"><a href="#signup">注册</a></li>
	</ul>
</div>
```

第二个 ul 标签部分是新加入的内容，这挺常用的哈，虽然其实这次我们用不到，但是玩玩还是无妨的。再简单修改一下 CSS，下面是原来的 CSS 中的一部分

```css
#nav-items {
	float: left;
	margin:0;
}
#nav-items .nav-item {
	float:left;
	list-style: none;
}
#nav-items .nav-item a {
	color:#333;
	text-decoration: none;
	font-size:16px;
	line-height: 50px;
	display: block;
	height: 50px;
	padding: 0 20px;
}
```

现在第一条 `#nav-items` 不用动，但是我们要照猫画虎的给新添加的 `#nav-items-r` 加一条，只是改作向右浮动。下边两条现在明显只对第一个 ul 里的内容起作用，但是我想应用到整个 `#nav` 部分，所以把选择器中的`#nav-items` 换成 `#nav`，来看修改后的结果：

```css
#nav-items {
	float: left;
	margin:0;
}
#nav-items-r {
	float: right;
	margin:0;
}
#nav .nav-item {
	float:left;
	list-style: none;
}
#nav .nav-item a {
	color:#333;
	text-decoration: none;
	font-size:16px;
	line-height: 50px;
	display: block;
	height: 50px;
	padding: 0 20px;
}
```

去看看效果吧～

![](http://coffee.zji.me/imgs/22-3.png)

于是我们得到了一个有左右两部分导航的导航条，**现在我希望大家回过头去对整个导航部分认真的复习一下，免得学到后面把前边的忘记了，那样就容易混淆了。另外一定记得每一节课都要跟着做哦～～**

下一节课我们来美化我们的导航条。

> **本章学习卡片：[卡片 22](http://coffee.zji.me/card.html?name=chapter22)**

> **本章代码下载：[本章代码](http://coffee.zji.me/show-code/22.zip)**

---

**本书是收费的，不过交费凭自觉。**价格定义为每人请我喝一杯咖啡（哪种品质的咖啡随意），支付宝账号：

> **alay9999@163.com  （刘源）**

为了让大家阅读方便，本书将在如下站点发布，但最终内容以主站为准：

* 主站首发： http://coffee.zji.me/
* Gitbook: http://codeme.gitbooks.io/easy-web-code-book/
* 简书： http://www.jianshu.com/users/d37eaf3de0ff
* 站酷： http://www.zcool.com.cn/u/12927742

未经本人许可，禁止任何形式转载。相关事宜请联系： dms@zji.me