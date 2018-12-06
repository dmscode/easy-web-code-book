第四十章 定位实例（一）
===

讲了这么多，有点晕了？嗯，很好，很好！来我们做个练习来更加的迷糊一下，咳咳，是深入理解一下。

其实这个案例也十分的简单，本来是可以在前面所写的页面中直接添加的，不过怕大家搞乱了，所以索性新写一个好了。当然我们只写主要部分，不会再写一个完整页面的。

我们要写的是一个二级导航，和一个返回顶部的按钮。其他部分咱们就简单呵呵一下，你们要理解我在简言之。先来写个基础的结构哦~

```
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>定位练习</title>
	<style>
		html, body {
			margin: 0;
			padding: 0;
		}
		#main {
			width: 960px;
			margin: 0 auto;
		}
		#logo {
			height: 120px;
			margin: 10px 0;
			background: #F3F3F3;
		}
		#post {
			height: 300px;
			margin: 10px 0;
			background: #F3F3F3;
		}
		#footer {
			height: 160px;
			margin: 10px 0;
			background: #F3F3F3;
		}
		#nav {
			height: 36px;
			margin: 10px 0;
			background: #333;
		}
	</style>
</head>
<body>
	<div id="main"><!-- 页面内容，宽 960 Start -->
		<div id="logo"></div>
		<div id="nav">
			<!-- 后面的 Html 结构写在这里，因为我们要写一个导航 -->
		</div>
		<div id="post"></div><!-- 这是海报 -->
		<div id="post"></div>
		<div id="post"></div>
	</div><!-- 页面内容，宽 960 End -->
	<div id="footer"></div><!-- 这是一个页尾 -->
</body>
</html>
```

这些都看得懂了吧，你看，简单的几行一个基本的页面结构就出来了，难吗？理解了就真的没什么了。自己去看下效果，我不截图了，这些只是给我们今天的主角一个舞台而已。

然后来写个导航，也没啥大不了的，轻车熟路啊~

```
<ul>
	<li>首页</li>
	<li>分类 &#9660;</li>
	<li>关于</li>
	<li>联系</li>
	<li>福利</li>
</ul>
<div class="clear"></div>
```

他的 CSS 如下：

```
#nav ul {
	margin: 0;
	padding: 0;
	float: left;
}
#nav ul>li {
	margin: 0;
	padding: 0 35px;
	list-style: none;
	float: left;
	color: #FCFCFC;
	line-height: 36px;
}
.clear {
	clear: both;
}
```

这也全是前面学过的内容，我们不多说，链接我不写了，反正这也不是我们这次的重点，我们尽量写的清爽一些。

然后接是一个新的选择器 `>` 表示某元素的子元素里的什么。`#nav ul>li ` 就是说 `#nav ul` 的所有是 li 子元素。就这么说吧，以前我们说 `#nav ul li`，是说这个 ul 的所有后代，哪怕是七十八代玄孙，只要叫 li ，那就有一个算一个。现在 `#nav ul>li ` 就只说他儿子辈里面叫 li 的，跟其他辈分没有毛关系了。

你说我们写了这么半天学过的东西，没见到啥区别啊。嗯……你看到分类那一项我写了个向下的三角箭头么？我们要给他写一个下拉菜单，不过……打字打得手疼了，下节课再继续……

---

**本书是收费的，不过交费凭自觉。**价格定义为每人请我喝一杯咖啡（哪种品质的咖啡随意），支付宝账号：

> **alay9999@163.com  （刘源）**

**本书现已重写，最新版内容请查看主站更新。**本书目前除主站之外，仅授权站酷、极客学院 Wiki发布，其他站点均为无授权盗载。

* 主站（2018 新版上线）：https://dmnydn.com/

未经本人许可，禁止任何形式转载。相关事宜请联系： dms@zji.me