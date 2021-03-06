第四十一章 定位实例（二）
===

那么我们说了，这个要做一个二级菜单的，现在刚有了第一级的菜单，现在来写第二级。

二级菜单是什么呢？其实还是一个列表，有那么几个列表项。所以还是 ul 和 li 标签而已。那么放在哪里呢？这个问题很有意思，真正的解答是：放在哪里都可以。我来解说几种情况：

第一种：像我们这个实例这么简单的情况。一般的我们为了说明他的层级关系，都会把它放在父级导航项内；

第二种：二级甚至三级或者更多级导航很复杂，代码量很大。这时候我们一般把它放在页尾。因为，一般这些导航默认是不显示的，那么让不显示的代码在前面，打开页面的时候就会先载入这部分代码，然后再载入下面那些需要被显示的代码，就显得页面加载速度比较慢了。所以我们把这些不需要立刻显示出来的代码放在最后去加载。至于位置，当然用各种方式定位过去就是了，有的时候也可能用 JS 动态的把这部分代码再插到前面。

好啦，开始我们本次的简单任务，那么加上二级导航之后就变成了这个样子。

```
<ul>
	<li>首页</li>
	<li>分类 &#9660;
		<ul>
			<li>小分类一</li>
			<li>小分类二</li>
			<li>小分类三</li>
			<li>小分类四</li>
		</ul>
	</li>
	<li>关于</li>
	<li>联系</li>
	<li>福利</li>
</ul>
<div class="clear"></div>
```

然后我们来给二级导航写 CSS ：

```
#nav>ul>li>ul {
	margin: 0;
	padding: 0;
	background:#363636;
	position: absolute;
	top: 40px;
}
```

我们一段段的说，这里定义的是 #nav （导航）里的 ul （一级菜单）里的 li （一级菜单项）里面的 ul （二级菜单）。好了，选择器就说到这里，下次不说了，说了两遍，差不多该看懂了。

margin 和 padding 都是清除元素的原有样式，这事情我们也做过很多次了，background 是设置背景色。

position 是定位，absolute 定位什么特点？不给自己保留原来的位置，而且相对于他外面第一个不是默认定位方式的元素定位。然而他外面并没有……这时候定位变得复杂。所以我们要让它相对于它外面的那个 li 标签进行定位。那么我们要给前面的 li 标签设置一个定位 `position: relative;` ，但是并不设置定位的位置数值。这样 li 位置没有发生变化，而且也占据着原来的位置。但是它内部的 ul 就可以以它为基准进行定位了。

top 是说二级菜单相对于他外面的 li 标签，顶部的距离是 40px ，正好给一级菜单留出了位置。

然后我们定义一下二级菜单的菜单项就可以去看效果了：

```
#nav ul>li>ul>li {
	width: 80px;
	margin: 0;
	padding: 0 35px;
	list-style: none;
	float: left;
	color: #FCFCFC;
	line-height: 36px;
	border-bottom: 1px solid #666;
}
```

这部分不解释了，因为并不复杂。

然后我们就获得了如下效果的导航菜单：

![](http://coffee.zji.me/imgs/41-1.png)

那么趁着还不复杂，赶紧的思考一下这个定位是怎么实现的，把你不懂得地方都去试着修改或者删除一下，看看会发生什么样的变化。

> **本章代码下载：[本章代码](http://coffee.zji.me/show-code/41.zip)**

**本书是收费的，不过交费凭自觉。**价格定义为每人请我喝一杯咖啡（哪种品质的咖啡随意），支付宝账号：

> **alay9999@163.com  （刘源）**

**本书现已重写，最新版内容请查看主站更新。**本书目前除主站之外，仅授权站酷、极客学院 Wiki发布，其他站点均为无授权盗载。

* 主站（2018 新版上线）：https://dmnydn.com/

未经本人许可，禁止任何形式转载。相关事宜请联系： dms@zji.me