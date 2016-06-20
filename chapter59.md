第五十九章 见证奇迹
===

说了这么多，该动动手了，其实很简单的。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>JQuery 的第一个测试</title>
    <script type="text/javascript" src="http://cdn.bootcss.com/jquery/3.0.0/jquery.min.js"></script>
    <script>
        $(document).ready(function(){
            $("button").click(function(){
                alert("就这样被你征服~~！");
            });
        });
    </script>
</head>
<body>
    <button>点我试一下</button>
</body>
</html>
```

我就解释一点东东，`function(){}`  这个是一个函数，在这里的作用是让大括号里的语句形成一个整体，然后以这个整体来作为这个 JQ 语句的一个参数。

然后再进一步，`click` 是单击的意思。仔细读一读，试一试，想一想，是不是觉得可以看懂了？就是这么简单啊，难么？

`dblclick` 是双击，改一改，看看你想的对不对。

本节课过于简单，老师拒绝授课，并趴在讲桌上开始睡觉。

---

[**上一章**](chapter58) - [**目录**](index) - [**下一章**](chapter60)

---

**本书是收费的，不过交费凭自觉。**价格定义为每人请我喝一杯咖啡（哪种品质的咖啡随意），支付宝账号：

> **alay9999@163.com  （刘源）**

为了让大家阅读方便，本书将在如下站点发布，但最终内容以主站为准：

* 主站首发： http://coffee.zji.me/
* Gitbook: http://codeme.gitbooks.io/easy-web-code-book/
* 简书： http://www.jianshu.com/users/d37eaf3de0ff
* 站酷： http://www.zcool.com.cn/u/12927742

未经本人许可，禁止任何形式转载。相关事宜请联系： dms@zji.me