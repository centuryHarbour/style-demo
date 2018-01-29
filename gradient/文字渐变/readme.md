# 文字渐变
利用css mask-\*属性实现
-

**css代码：**
```css
.font-gradient {
	position: relative;
}

.font-gradient[data-text]::after {
	content: attr(data-text);
	color: green;
	position: absolute;
	left: 0;
	z-index: 2;
	-webkit-mask-image: -webkit-gradient(linear, 0 0, 0 bottom, from(#ff0000), to(rgba(0, 0, 255, 0)));
}
```

**html代码：**
```html
<h2 class="font-gradient" data-text="mask-image来实现文字渐变">mask-image来实现文字渐变</h2>
```

* css mask-*参考链接：
	* [MDN web docs mask-\*](https://developer.mozilla.org/zh-CN/docs/Web/CSS/mask)
	* [CSS mask-image属性详细介绍](https://www.xttblog.com/?p=2349)

利用css background的linear-gradient来实现
-

**css代码：**
```css
background: -webkit-linear-gradient(left,#00c0f9, #4d8cff, #9f72ff);
background: linear-gradient(left,#00c0f9, #4d8cff, #9f72ff);
-webkit-background-clip: text;
webkit-text-fill-color: transparent;
```

**html代码：**
```html
<h1 class="title">background的linear-gradient实现文字渐变</h1>
```

利用css background-image的gradient来实现
-

**css代码：**
```css
background-image: -webkit-gradient(linear, 0 0, 0 bottom, from(rgba(0, 128, 0, 1)), to(rgba(51, 51, 51, 1)));
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;
```

**html代码：**
```html
<h2 class="text-gradient">利用css background-image的gradient来实现</h2>
```

* demo请查看 001.html