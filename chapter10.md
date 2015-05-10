第十章 表格布局原理
===

> 如果本章演示效果无法正常展示，请至主站查看 http://coffee.zji.me/

这个吧，其实真的没有很复杂的道理，就是每个单元里放上相应的内容，靠表格控制着他规规矩矩的呆着。当然了，没东西的地方就不填写了，于是就留出了空白。

现在很少有人用表格去布局了，除了淘宝之类的特殊情况，或者……这家伙不会 CSS。因为表格不灵活，修改起来也十分的麻烦啊～在这里简单讲讲做个了解。

比如我现在有两张图片，想让他们排在一行，然后相互距离 100 像素怎么办呢？我们就做一个一行三列的表格，第一个单元格和第三个单元格分别放一张图片，而第二个单元格留空，设置宽度为 100px。代码如下：

```html
<table>
	<tr>
		<td><img src="http://coffee.zji.me/imgs/bridge.jpg" width="300" /></td>
		<td width="100"></td>
		<td><img src="http://coffee.zji.me/imgs/bridge.jpg" width="300" /></td>
	</tr>
</table>
```

来看看效果：

<table>
	<tr>
		<td><img src="http://coffee.zji.me/imgs/bridge.jpg" width="200" /></td>
		<td width="100"></td>
		<td><img src="http://coffee.zji.me/imgs/bridge.jpg" width="200" /></td>
	</tr>
</table>

那么我们只是想让一张图片距离左侧 300px 呢？

```html
<table>
	<tr>
		<td width="300"></td>
		<td><img src="http://coffee.zji.me/imgs/bridge.jpg" width="300" /></td>
	</tr>
</table>
```
效果如下：

<table>
	<tr>
		<td width="300"></td>
		<td><img src="http://coffee.zji.me/imgs/bridge.jpg" width="300" /></td>
	</tr>
</table>

所以这个东西其实很好理解，设置合适的单元格尺寸，来撑开布局而已，你用 Excel 也可以玩。然后到了布局复杂的不行了，大家又发明了表格的嵌套，就是把一个表格放到另一个表格的单元格里，乱的让人想吐……不多说，只做了解。下一章我们学习一个重点的内容哦——表单。

> **本章学习卡片：[卡片 10](http://coffee.zji.me/card.html?name=chapter10)**

---

**本书是收费的，不过交费凭自觉。**价格定义为每人请我喝一杯咖啡（哪种品质的咖啡随意），支付宝账号：

> **alay9999@163.com  （刘源）**

为了让大家阅读方便，本书将在如下站点发布，但最终内容以主站为准：

* 主站首发： http://coffee.zji.me/
* Gitbook: http://codeme.gitbooks.io/easy-web-code-book/
* 简书： http://www.jianshu.com/users/d37eaf3de0ff
* 站酷： http://www.zcool.com.cn/u/12927742

未经本人许可，禁止任何形式转载。相关事宜请联系： dms@zji.me