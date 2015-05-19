第二十章 导航条（五）
===

> 如果本章演示效果无法正常展示，请至主站查看 http://coffee.zji.me/

现在来写导航项。其实导航是有专门的标签的 `<nav>	</nav>` 但是这个特性比较新，IE9 才开始支持，所以很多人还是习惯用列表来写导航，这里我们也使用列表，为的是你以后看到各种代码都能看得懂，因为 nav 标签相对于列表还是比较简单的。

那么先来说说列表哦：

```html
<ul>
	<li>列表内容</li>
	<li>列表内容</li>
	<li>列表内容</li>
</ul>
```

效果如下：

<ul>
	<li>列表内容</li>
	<li>列表内容</li>
	<li>列表内容</li>
</ul>

如上叫做无序列表。

```html
<ol>
	<li>列表内容</li>
	<li>列表内容</li>
	<li>列表内容</li>
</ol>
```

效果如下：

<ol>
	<li>列表内容</li>
	<li>列表内容</li>
	<li>列表内容</li>
</ol>

如上叫做有序列表。

你说这跟导航项一点都不像啊，但是在逻辑上还是很像的，都是列出来一些内容。既然我们对于前边的编号圆点什么的完全不在乎，那么我们就选择无序列表好了，那么 html 代码很简单的，几乎跟上面一样

```html
<ul id="nav-items">
	<li class="nav-item">首页</li>
	<li class="nav-item">下载</li>
	<li class="nav-item">特点</li>
	<li class="nav-item">关于</li>
</ul>
```

这个样子没有问题，挺容易看懂的，我们把他加在 #loge 的 div 后面来看看效果。

![](http://coffee.zji.me/imgs/20-1.png)

你说，哼，幸亏我已经不再相信你了，否则又得失望。本来想要跟 logo 在一排的效果（要不那背景留着干嘛用？？）结果又做出来一个奇葩的造型。

我跟你说啊：**想横排，加浮动！**你看我一步步把它搞上去哦！在 CSS 里加上

```css
#nav-items .nav-item {
	float:left;
}
```

就是给我们的每一个导航项加上了一个向左浮动的属性，我们只做了这一点，来看看什么变化哦

![](http://coffee.zji.me/imgs/20-2.png)

这个……好像是到一行了，但是有点乱，看不好效果，主要是那个圆点的影响，那我们去掉圆点，把刚才那部分 CSS 再加上一个属性：

```css
#nav-items .nav-item {
	float:left;
	list-style: none;
}
```

就是列表的样式：无。再看效果。

![](http://coffee.zji.me/imgs/20-3.png)

呀，果然是一排相邻的元素，一加上浮动就从竖着排列变到横着排了。那么眼下呢，到这里你只要记住把想要横排的东西都加上浮动就好。如果你想知道为什么，那我们需要继续一下我们快递箱的故事，有些绕，这个故事晚些时候我会发布在我们交流平台的“咖啡俱乐部”频道内（就是我们的 VIP 频道）。

现在我们就先记住这个结论，然后再实践中去慢慢体验他的用途。然后我们做个练习，你看 logo 和导航项这两部分还是纵向排列的呢，那我们来给他俩也加上浮动试试看。

为了防止你搞乱了，我在这贴一下完整的 CSS 代码：

```css
/* 这是我写的第一个 CSS 文件，内心十分的激动，在这心潮澎湃之余，我想到了一个真理 —— 稻米鼠真帅！ */
html, body {
	margin:0;
	padding:0;
}
#nav {
	width:100%;
	height:50px;
	background:#F3F3F3;
	padding:0 30px;
}
#logo {
	float: left;
}
#logo a {
	color:#333;
	text-decoration: none;
	font-size:24px;
	font-weight: 700;
	line-height: 50px;
}
#nav-items {
	float: left;
}
#nav-items .nav-item {
	float:left;
	list-style: none;
}
```

再来看看效果：

![](http://coffee.zji.me/imgs/20-4.png)

那么到了这里貌似虽然难看些，但是我们把位置都搞对了。下节课我们来试着给导航项加链接哦～～

> **本章学习卡片：[卡片 20](http://coffee.zji.me/card.html?name=chapter20)**

> **本章代码下载：[本章代码](http://coffee.zji.me/show-code/20.zip)**

---

**本书是收费的，不过交费凭自觉。**价格定义为每人请我喝一杯咖啡（哪种品质的咖啡随意），支付宝账号：

> **alay9999@163.com  （刘源）**

为了让大家阅读方便，本书将在如下站点发布，但最终内容以主站为准：

* 主站首发： http://coffee.zji.me/
* Gitbook: http://codeme.gitbooks.io/easy-web-code-book/
* 简书： http://www.jianshu.com/users/d37eaf3de0ff
* 站酷： http://www.zcool.com.cn/u/12927742

未经本人许可，禁止任何形式转载。相关事宜请联系： dms@zji.me