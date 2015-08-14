第四十五章 无聊的写个小游戏吧
===

当然了，没有 JS 这种灵活的东东，我们不可能做很复杂的动态游戏。但是如果你肯开发思路的话，确实可以实现一些完整的游戏过程，虽然确实很简单，但是可玩性，以及游戏体验却也未必很差。

那么今天我们来做一个猫咪抓老鼠的小游戏。你看说的好听，其实就是不断把鼠标移动到一个小小的红色方块的过程，你把它当成鼠标走迷宫也可以，总之鼠标要是没有能够准确的移动到下一个预定位置就算失败。如果我们把目标点设置的小一些，那么难度还是很大的。

首先我们给游戏写一个起点，Start：

```
<div id="start">Start</div>
```

至于 CSS，我就把上节课那只红色按钮简单修改了一下，所以不解释喽~

```
#start {
	width: 64px;
	height: 64px;
	padding: 4px;
	position: relative;
	background: #CC0000;
	border: 5px solid #CCCCFF;
	border-radius: 40px;
	font-size: 16px;
	color: #FCFCFC;
	line-height: 64px;
	text-align: center;
}
```

![](http://coffee.zji.me/imgs/45-1.png)

然后我们在刚才的标签里面写一个 div 当作老鼠，于是就变成了：

```
<div id="start">Start
	<div class="mouse"></div>
</div>
```

我再给它一个简单的样式：

```
.mouse {
	display: none;
	width: 10px;
	height: 10px;
	background: #CC0000;
	position: absolute;
	left: 10px;
	top:0;
}
```

写到这里你就发现了，这跟弹出菜单很像啊。对啊，我就是让鼠标放在一个元素上，就会弹出它的内部元素，再放到弹出的元素上，又弹出内部元素……如此玩下去，鼠标一旦位置放错，这些弹出就都隐藏了，于是……游戏失败。

那么显然的我就写下了如下的触发动作：

```
#start:hover {
	background: #CCCCFF;
}
#start>.mouse {
	left: 74px;
	top: 35px;
}
#start:hover>.mouse {
	display: block;
}
.mouse:hover {
	background: #CCCCFF;
}
.mouse:hover>.mouse {
	display: block;
}
```

当然其中包含一些为了视觉舒服而做的小变化。另外就是这个 `#start>.mouse` 是特意规定了一下第一个 .mouse 的位置，因为这个跟别的有点区别。

现在的问题就是 .mouse 里面嵌套 .mouse 了，就像下面这样：

```
<div id="start">Start
	<div class="mouse">
		<div class="mouse">
			<div class="mouse">
				<div class="mouse">
					<div class="mouse">
						<div class="mouse">
							<div class="mouse"></div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</div>
```

![](http://coffee.zji.me/imgs/45-2.png)

你可以试一下，随着你鼠标的滑动，逐渐显示出了一条直线，因为每一只 mouse 都相对于前一只向后偏移了，所以是一条水平的直线，但是这样没有变化就显得毫无趣味了。那么所谓的变化也就是换个偏移的方向而已，实际上就涉及到了两个属性——left 和 top。

于是我再定义几个类，产生一些变化。

```
.md {
	left: 0;
	top: 10px;
}
.ml {
	left: -10px;
	top: 0;
}
.mu {
	left: 0;
	top: -10px;
}
```

.md 是向下偏移，.ml 向左，.mu 向上，至于向右，.mouse 不就是么？然后这么写：

```
<div id="start">Start
	<div class="mouse">
		<div class="mouse">
			<div class="mouse md">
				<div class="mouse md">
					<div class="mouse md">
						<div class="mouse ml">
							<div class="mouse ml"></div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</div>
```

![](http://coffee.zji.me/imgs/45-3.png)

我就不多写了，你可以自由组合着玩，最后在里面再写一个 #end 来作为结束，就算大功告成。我写了一个案例，你可以下载来玩，当然也要认真想想都是为什么，然后你能想出什么有趣的玩法吗？

我的案例玩起来是这个样子的：

![](http://coffee.zji.me/imgs/45-4.png)

> **本章代码下载：[本章代码](http://coffee.zji.me/show-code/45.zip)**

**本书是收费的，不过交费凭自觉。**价格定义为每人请我喝一杯咖啡（哪种品质的咖啡随意），支付宝账号：

> **alay9999@163.com  （刘源）**

为了让大家阅读方便，本书将在如下站点发布，但最终内容以主站为准：

* 主站首发： http://coffee.zji.me/
* Gitbook: http://codeme.gitbooks.io/easy-web-code-book/
* 简书： http://www.jianshu.com/users/d37eaf3de0ff
* 站酷： http://www.zcool.com.cn/u/12927742

未经本人许可，禁止任何形式转载。相关事宜请联系： dms@zji.me