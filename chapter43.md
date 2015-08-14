第四十三章 定位实例（四）
===

导航我还没玩够，哼哼，我要写一个帅点的，这样我们就可以顺便学一些新鲜的玩意了。

首先左下角浮动一个按钮，哎呀，这个写起来跟右下角的一样呢~我就不多废话了，对了，区别有点，就是这次我们不用链接了。

```
<div id="show-nav"><div class="button">我<br>是<br>菜<br>单</div></div>
```

然后我们开始对它进行美化，要是还跟右侧的按钮一样，这页面岂不丑死！来来，我们来写一个长长的 CSS 样式。

```
#show-nav {
	position: fixed;
	left: 0;
	bottom: 120px;
}
#show-nav .button {
	width: 16px;
	height: 64px;
	padding: 4px;
	position: relative;
	background: #AA0000;
	border: 5px;
	border-style: solid;
	border-color: #FFF;
	border-radius: 0 16px 16px 0;
	border-left: none;
	box-shadow: 2px 2px 18px #333;
	font-size: 12px;
	color: #FCFCFC;
	line-height: 16px;
	text-align: center;
	cursor: pointer;
	z-index: 99;
}
```

呵，有点长，我们慢慢讲。#show-nav 现在只负责定位，那么他的 CSS 很容易解读了，只是简单的设置了定位方式和位置而已。

`#show-nav .button` 主要负责样式，其实大部分属性我们都是可以自己看明白的，我就不反反复复地去讲了，否则……估计有人要跟我叫“婆婆”了。

`position: relative;` 这个属性又是一个助攻，借助它使得元素可以设置 z-index 属性。而并不是用它去影响元素位置。当然也可以说他影响了元素在层级上的定位。

边框 border 这个复合属性被我拆开来写了，先完成各种边框的定义之后，又用 `border-left: none;` 把左侧的边框干掉了。其他都好理解了，然后有一个新的属性是 `border-radius`，这个设置的是边框的圆角，可以设置一个值，代表圆角的半径，四个角的圆角半径相同。现在我设置了四个值，显然是把四个角分别设置了。四个值的顺序是：左上、右上、右下、左下，依旧是顺时针旋转，所以记住从左上角开始就够了。

`box-shadow` 是指元素的阴影，属性是三个值和一个颜色，前三个值分别是 X轴偏移量，Y轴偏移量，阴影扩散大小，最后的颜色当然就是阴影的颜色值了。这个不懂就试一试，实践是最好的学习方法，改改数值，看看效果立刻就明白了。

`cursor` 是说鼠标指针样式，当然是限定鼠标在这个元素之上的时候，pointer 标识的就是那个小手的样子，不知道？拿鼠标指向一个链接，就是这个样子的。

剩下宽高，行高，文字居中这些确定了文字的位置，你可以想一想我是怎么计算的，如果想明白了就修改数值看看，看你是否可以把他搞到另外的尺寸而保证文字居中。

那么现在我们把一个简单的元素搞得复杂了，然而仔细想想，也并没有做什么很奇特的事情。CSS 也不过就是为每个元素统筹安排这点有限的属性罢了。

那么来看看我们左侧 Sao 红的按钮吧~

![](http://coffee.zji.me/imgs/43-1.png)

> **本章代码下载：[本章代码](http://coffee.zji.me/show-code/43.zip)**

**本书是收费的，不过交费凭自觉。**价格定义为每人请我喝一杯咖啡（哪种品质的咖啡随意），支付宝账号：

> **alay9999@163.com  （刘源）**

为了让大家阅读方便，本书将在如下站点发布，但最终内容以主站为准：

* 主站首发： http://coffee.zji.me/
* Gitbook: http://codeme.gitbooks.io/easy-web-code-book/
* 简书： http://www.jianshu.com/users/d37eaf3de0ff
* 站酷： http://www.zcool.com.cn/u/12927742

未经本人许可，禁止任何形式转载。相关事宜请联系： dms@zji.me