第三十章 首屏大海报（四）
===

> 如果本章演示效果无法正常展示，请至主站查看 http://coffee.zji.me/

你看，代码这东西认真玩起来其实还是很有意思的。不过可能有同学问了，咱不是写一个 App 的发布页面么？怎么……啊啊，是啊是啊，所以我们接下来要写一个下载按钮呢~

这个按钮的写法比较多啊，你要是只为了链接到一个文件，其实用 a 标签就可以搞定啊，你会设置背景吧，会设置文字颜色吧，会设置边框吧。然后哩？

当然，要是希望用来发生什么有趣的事情，或者为了语义明确，我们也可以选用 button（按钮）标签。这个写起来超简单的~

```html
<button>下载偶像巨幅签名照</button>
```

![](http://coffee.zji.me/imgs/30-1.png)

是挺简单的，也挺难看的，开始给他定义样式：

```css
#post .post-content button {
	padding: 12px;
	margin-top: 36px;
	background: #CCE;
	border: 5px solid #DDF;
	font-size: 18px;
	font-weight: 600;
}
```

大家应该都看得懂的，我也不多说了，看看效果吧，请原谅我这诡异的配色！

![](http://coffee.zji.me/imgs/30-2.png)

到这里，这个海报其实就做得差不多了。虽然很多细节没有去完善。不过……那不是应该你们自己去做的吗？赶紧的，每个人做一个漂亮的出来。

本来这章已经可以结束了，但是好像字数太少了，我总要对得起各位读者的票钱……虽然你们大部分没给钱。所以在下面做一些简单的补遗。

第一个问题：背景相关的还有一个属性：background-repeat 是说背景重复。默认是重复的呦，就是背景图片小于元素的话，则通过重复的方式进行填满，而我们也可以单独设置其中某个轴是否重复。

然后我来举个例子：`background-repeat: no-repeat repeat-y` 就是横向不重复，只在纵向重复。挺好理解的事情，就不多解释了。

定义背景的时候我们可以把这些属性都写在一起，为什么这么做呢？我就是图省事……

```css
background:url(miao.jpg) center -15px no-repeat;
```

然后说说 margin 这个家伙。这个家伙其实也没有想象的那么麻烦，就是纵向上两个 margin 相遇会重叠。比如：

```html
<div style="height:50px;border:3px solid #666;margin:50px;">
	
</div>
<div style="height:50px;border:3px solid #666;margin:50px;">
	
</div>
```
效果如下：

<div style="height:50px;border:3px solid #666;margin:50px;">
	
</div>
<div style="height:50px;border:3px solid #666;margin:50px;">
	
</div>

你看你看，两个元素的间隔明显不是 100px（50+50）啊。其实只有 50px ，因为两个 margin 重叠了。

然后其实上一章 h1 引起的问题也是着个问题的一个变种，当时我们已经解决掉了。这个先知道就好，剩下的到实践中去理解。

**然后留个作业吧，敢不敢独立把这个页面完成掉？而且要尽可能的完美~**

> **本章学习卡片：[卡片 30](http://coffee.zji.me/card.html?name=chapter30)**

> **本章代码下载：[本章代码](http://coffee.zji.me/show-code/30.zip)**

---

**本书是收费的，不过交费凭自觉。**价格定义为每人请我喝一杯咖啡（哪种品质的咖啡随意），支付宝账号：

> **alay9999@163.com  （刘源）**

**本书现已重写，最新版内容请查看主站更新。**本书目前除主站之外，仅授权站酷、极客学院 Wiki发布，其他站点均为无授权盗载。

* 主站（2018 新版上线）：https://dmnydn.com/

未经本人许可，禁止任何形式转载。相关事宜请联系： dms@zji.me