第十三章 神一样的 CSS
===

> 如果本章演示效果无法正常展示，请至主站查看 http://coffee.zji.me/

当然这只是一个比喻，我绝没有挑起代码界圣战的意思。从 Html 进入到 CSS 世界的感觉就好像从人间一步迈进了神国，一些曾经很难做到的事情，现在变得信手拈来了。宛如我们掌握了神的力量。当然这么说下去的话后面我们要学的 JavaScript 就应该称作众神之神了……

玩笑开完了，玩代码的时间到了，我们先来简单认识一下 CSS。

首先看一下我们前边写的代码：

```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8">
		<title>Document</title>
	</head>
	<body>
		<p>Hello world！</p>
		<p>Code is so easy！</p>
	</body>
</html>
```

挺简单的代码，效果如下：

<p>Hello world！</p>
<p>Code is so easy！</p>

就是两段文字，现在我给他添加一点属性哦：

```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8">
		<title>Document</title>
	</head>
	<body>
		<p style="color:red;font-size:12px;">Hello world！</p>
		<p>Code is so easy！</p>
	</body>
</html>
```

大家看到，我就是给第一个段落加了一个属性。来看看效果：

<p style="color:red;font-size:12px;">Hello world！</p>
<p>Code is so easy！</p>

我们来分析代码哦，`style` 是样式的意思，那么很容易明白，这个属性就是给当前的元素加上一些样式。那么我们加了什么样的样式呢？`color:red;` 颜色是红色，颜色（color）是一个 CSS 属性，而红色（red）是这个属性的值。哎，着就跟 Html 有区别了，Html 是`属性=属性值`，而 CSS 是`属性:属性值`。（**特别强调：都是英文标点哦**）。然后 CSS 的每个属性结束都要用英文的分号标记出来，所以 `font-size` 就是第二个属性了，意思是字体的尺寸，属性值是 `12px` ，于是我们就看到了上边的效果。

所以看到了，CSS 也不难，不过是换个格式去写属性，属性值。说来说去也就像代数里的赋值操作，然后就没有然后了。

那你说这个 CSS 有啥好的啊？方便！来看哦，现在代码里有两个段落，那么我们假设我们有一百个段落（我不写了，就拿这两个代表了）要是我想都设置成刚才那样，咋弄？把 style 属性整个复制，然后挨个 `<p></p>` 标签里粘贴？好不容易粘完了，老板告诉你改回第一稿……

来看我怎么写：

```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8">
		<title>Document</title>
		<style>
			p {
				color:red;
				font-size:12px;
			}
		</style>
	</head>
	<body>
		<p>Hello world！</p>
		<p>Code is so easy！</p>
	</body>
</html>
```

效果如下：

<p style="color:red;font-size:12px;">Hello world！</p>
<p style="color:red;font-size:12px;">Code is so easy！</p>

好了，再来分析代码哦～

我们说了 `<head></head>` 标签是用来声明东西的，那么我在他里面声明一下这个页面的样式他应该不会有什么意见，就是本职工作啊。但是我们要把这些样式放在一起，不许他们乱跑，所以写上 `<style></style>` 标记一下，这里面的都是样式，就是都是 CSS 代码啊，你要按着 CSS 那么处理。于是这个事情明白了。

再看里边，`p` 代表标签 `<p></p>` 这个猜都能猜出来，是吧，后面是他的样式（color，font-size），我们前边也都认识过了。现在的问题是大括号，大括号就是说这部分代码都是前边 p 的啊，又是一前一后标记一下，这么简单的事情我们一想就明白了。

看到啦，我在 CSS 里说 `p {……}`，于是页面里所有的 `<p></p>`  标签就都获得了这个样式，很方便是不是？

——“老板，那一百段的文字颜色我都改好了！”

——“这么快！没骗我吧，正好我这还有点活，你就能者多劳吧……”

CSS 这么厉害的东西确实是能者多劳，现在我们一般只用 Html 写网页的框架和内容，而样式全部交给 CSS 处理，他清晰明了，便于管理和修改，而且也十分得强大。

但是能者多劳就该出问题了，你想啊，CSS 管理了整个页面的样式，有着很多内容，全放在页头，我们想看网页的 Html 结构的时候就要往下找很久。这就好像把档案管理员跟老板放在一个办公室，老板迟早要被堆积成山的档案埋没（为什么说到这里我很开心呢？）。

然后还有一个问题，你想我写一个网站，肯定很多样式是相似或者相同的，那么这部分咋整？每个页面复制一份？然后老板说了，吧所有页面的文字都换成蓝色，你又挨个页面复制粘贴……

所以我们要把 CSS 独立出来，这样他不会影响我方便的阅读 Html，还可以在多个页面里调用，谁用他就叫他，我们共用一个就好啦。是啊，公司就一个档案管理员，不是一个部门塞一个，那样机构臃肿，职能重叠，效率低下……

所以我们新建一个 css 为后缀的文件，比如叫做 `style.css`，文件名你随意啊，然后把这部分代码粘进去保存。

```css
p {
	color:red;
	font-size:12px;
}
```

这就是独立的 CSS 文件了。然后我们把我们的 Html 代码改成：

```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8">
		<title>Document</title>
		<link href="mycss/style.css" rel="stylesheet" type="text/css">
	</head>
	<body>
		<p>Hello world！</p>
		<p>Code is so easy！</p>
	</body>
</html>
```

我们发现这就是在普通的 Html 文档上加了一个 link 标签，我们来分析一下，link 是链接的意思，就是我们要把我们的 CSS 文件链接到这个文档来，要不然浏览器怎么知道你要用哪个 CSS 文件呀。所以这是一个声明，放在 head 势力范围内没错。

现在研究 link 的属性哦，href 是链接到的地址，就是我们要用的 CSS 文件地址，我这里写的是相对地址，所以你不要光是照着抄，要写你自己那个 CSS 文件的相对地址哦，否则找不到文件自然就出错了。

rel 属性是说被链接文档和当前文档之间的关系，就是样式表（stylesheet）喽，顺便说一下 CSS （Cascading Style Sheets）的中文名称是“层叠样式表”，简称“样式表”。

然后 type 是类型，text/css 说的是这是一个文本文件（text），同时也是一个 css 格式的文件。

当然这种格式也不用记，跟我一样用的时候抄一下就好了。所以呢，今天我们学习了 CSS 在 Html 文件中的三种出场方式和一些 CSS 的优点。大家可以看学习卡片中的总结再复习一下主要知识点哦～

> **本章学习卡片：[卡片 13](http://coffee.zji.me/card.html?name=chapter13)**

---

**本书是收费的，不过交费凭自觉。**价格定义为每人请我喝一杯咖啡（哪种品质的咖啡随意），支付宝账号：

> **alay9999@163.com  （刘源）**

**本书现已重写，最新版内容请查看主站更新。**本书目前除主站之外，仅授权站酷、极客学院 Wiki发布，其他站点均为无授权盗载。

* 主站（2018 新版上线）：https://dmnydn.com/

未经本人许可，禁止任何形式转载。相关事宜请联系： dms@zji.me