第五十四章 一万遍啊一万遍！
===

我觉得咱们里面有叛徒，谁又跟我女盆友说我作弊的事了？现在她罚我说我错了一万遍，而且不许使用 for 循环。

可是……我们还有 while 循环呀！这个其实跟 for 循环很像的，我写得出来你猜猜意思。

```
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>while 循环</title>
	<script>
		var i=0;
		while(i<10000){
			alert("我错了~第 "+i+"遍");
			i++;
		}
	</script>
</head>
<body>

</body>
</html>
```

对照着 for 循环你很容易理解吧，先判断小括号里条件是否成立，然后如果成立就执行大括号里的语句，执行完再判断小括号里的条件是否成立，如果成立再执行大括号里……

你看我完成了女朋友的苛刻条件了吧？但是作为一个优秀的男盆友怎么可以就此止步呢？所以事实上我写的程序更加的简洁：

```
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>while 循环</title>
	<script>
		while(1){
			alert("我错了~");
		}
	</script>
</head>
<body>

</body>
</html>
```

我们说过非零的数字为 true，条件成立，然后执行了大括号的语句之后，小括号里的条件依旧成立，其实这个条件永远不会发生变化，这是一个常量（常量不会变），所以条件一直成立，循环一直继续，这就是传说中可以跑到地老天荒的死循环，我们写程序的时候一定要避免写死循环。

现在女盆友还在那里一边计数一边关提示框呢。

> **本章代码下载：[本章代码](http://coffee.zji.me/show-code/54.zip)**

---

[**上一章**](chapter53) - [**目录**](index) - [**下一章**](chapter55)

---

**本书是收费的，不过交费凭自觉。**价格定义为每人请我喝一杯咖啡（哪种品质的咖啡随意），支付宝账号：

> **alay9999@163.com  （刘源）**

为了让大家阅读方便，本书将在如下站点发布，但最终内容以主站为准：

* 主站首发： http://coffee.zji.me/
* Gitbook: http://codeme.gitbooks.io/easy-web-code-book/
* 简书： http://www.jianshu.com/users/d37eaf3de0ff
* 站酷： http://www.zcool.com.cn/u/12927742

未经本人许可，禁止任何形式转载。相关事宜请联系： dms@zji.me