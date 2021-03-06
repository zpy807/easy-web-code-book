第四十四章 定位实例（五）
===

然后就是给这个按钮加装一个菜单用来弹出。这很像我们前边写二级菜单的操作，其实也没什么本质上的区别，管他几级呢，反正都是弹出菜单罢了。

所以也不过是加一个列表而已，懒惰如我，直接把上边的二级菜单复制过来了。

```
<div id="show-nav">
	<div class="button">我<br>是<br>菜<br>单</div>
	<ul>
		<li>小分类一</li>
		<li>小分类二</li>
		<li>小分类三</li>
		<li>小分类四</li>
	</ul>
</div>
```

这并不复杂，那么他的 CSS 跟上边二级导航的也差不多：

```
#show-nav ul {
	display: none;
	margin: 0;
	padding: 0;
	background:rgba(54,54,54,0.6);
	position: absolute;
	left: 20px;
	bottom: 20px;
	z-index: 50;
}
#show-nav:hover ul {
	display: block;
}
#show-nav ul>li {
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

除了定位值发生了一些变化，其他几乎没有改变，所以就不多说了。只说一个小区别：

`background:rgba(54,54,54,0.6);`，一般我们用的如 #FFFFFF 形式的颜色值，是 RGB 颜色值，第一二位表示红色的浓度，三四位是绿色，五六位是蓝色。现在我们换了一个 rgba 格式，其实就是多了一个透明度的数值，当然其他区别也是有的，#FFFFFF 用的是十六进制，而我们现在写的 rgba 后面用的是十进制，前三个数值分别表示红绿蓝三种颜色的浓度，数值为 0——255 之间的整数。而最后一位是透明度，可以是 0 到 1 之间的小数。这个办法就可以简单的设置一个透明背景。

然后注意这次设置的 `z-index:50;` 而上节课我们给 `#show-nav .button` 设置的是 99。他们数字的值并不重要，重要的是他们之间的大小关系。这样是为了让弹出的菜单显示在按钮后面，也就是按钮遮住弹出菜单的左下角，显得更美观一些。

然后来看看效果：

![](http://coffee.zji.me/imgs/44-1.png)

这几节课的案例都是很常见的一些情境，定位的用法也并不复杂，稍微认真思考一下都可以理解，然而重要的不是技术本身，而是利用技术的思路。嗯哼，多思考哦~

> **本章代码下载：[本章代码](http://coffee.zji.me/show-code/44.zip)**

**本书是收费的，不过交费凭自觉。**价格定义为每人请我喝一杯咖啡（哪种品质的咖啡随意），支付宝账号：

> **alay9999@163.com  （刘源）**

为了让大家阅读方便，本书将在如下站点发布，但最终内容以主站为准：

* 主站首发： http://coffee.zji.me/
* Gitbook: http://codeme.gitbooks.io/easy-web-code-book/
* 简书： http://www.jianshu.com/users/d37eaf3de0ff
* 站酷： http://www.zcool.com.cn/u/12927742

未经本人许可，禁止任何形式转载。相关事宜请联系： dms@zji.me