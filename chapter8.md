第八章 半个标签
===

现在我们学过的标签都是一个开始，一个结束，为什么腻？因为其实我们要标记的是一个范围，所以要给出一个开始和一个结束的点。那么有没有我们只需要给出一个点的情况呢？当然有了，来看两个标签先：

> `<br />`

> `<hr />`

解释一下哦，`<br />` 是在这里换行，那么明显我们只需要指定一个位置就可以了；`<hr />` 是在这里插入一条分割线，当然也只要告诉他一个位置就够了。

既然只需要一个位置，那么写两个（一组、一对）标签就是浪费时间，所以懒惰的程序员们就把这一对标签合二为一，看看上边的写法，明白了吧。等等，不是什么标签都可以这么合并的哦，我这么说只是为了让你理解一下的，你可别光顾着撸串又把我的话当了耳旁风啊～

这个当然没什么难的，不过有个很著名的标签也是独行侠哦～～他独来独往，至今还是一只单身狗，那么他就是大名鼎鼎的图片标签 `<img src="在这里写图片地址哦～" />`

那么现在，我们来玩哦～我这有一个图片地址： `http://coffee.zji.me/imgs/bridge.jpg` ，那么我们的代码应该是：

```html
<img src="http://coffee.zji.me/imgs/bridge.jpg" />
```

效果如下哦：

![](http://coffee.zji.me/imgs/bridge.jpg)

那么看懂啦 src 属性就是要插入的图片的地址。然后我们再看看他的其他属性哦，这个开始有意思了。

```html
<img src="http://coffee.zji.me/imgs/bridge.jpg" alt="这里是图片的说明文字" />
```

alt 很像链接里的 title 属性，这个是用来说明图片的，但是他还有一个很重要的作用，要是因为网络等问题图片没能正常显示的时候，这些文字会显示在图片位置，让人们知道这里应该是什么。效果如下：

![这里本该是一张图片的，但是他今天没来上班……](no-pic.jpg)

上面的这些对照着链接都很容易理解了，但是图片还有两个常用的属性宽（width）和高（height），一般的说，我们给他们指定的值就好了，比如呢～

```html
<img src="http://coffee.zji.me/imgs/bridge.jpg" width="300" height="300" />
```

在 html 代码里，如果没写单位则默认单位是 px（像素），效果如下：

<div class="img-box"><img src="http://coffee.zji.me/imgs/bridge.jpg" width="300" height="300" /></div>

而如果你只写了其中一个属性，则图片会按比例缩放，也就是另一个属性会跟着等比例变化。比如：

```html
<img src="http://coffee.zji.me/imgs/bridge.jpg" width="300" />
```

它的效果如下：

<div class="img-box"><img src="http://coffee.zji.me/imgs/bridge.jpg" width="300" /></div>

那么我们基本了解了图片这个标签，现在我们来为图片加个链接吧～

```html
<a href="http://coffee.zji.me/">
	<img src="http://coffee.zji.me/imgs/bridge.jpg" />
</a>
```

好啦，那么这次就聊到这里，记得给我买咖啡喝哦～

> **本章学习卡片：[卡片 8](http://coffee.zji.me/card.html?name=chapter8)**

---

**本书是收费的，不过交费凭自觉。**价格定义为每人请我喝一杯咖啡（哪种品质的咖啡随意），支付宝账号：

> **alay9999@163.com  （刘源）**

为了让大家阅读方便，本书将在如下站点发布，但最终内容以主站为准：

* 主站首发： http://coffee.zji.me/
* Gitbook: http://codeme.gitbooks.io/easy-web-code-book/
* 简书： http://www.jianshu.com/users/d37eaf3de0ff
* 站酷： http://www.zcool.com.cn/u/12927742

未经本人许可，禁止任何形式转载。相关事宜请联系： dms@zji.me