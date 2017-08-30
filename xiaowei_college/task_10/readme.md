## [任务描述](http://ife.baidu.com/course/detail/id/114)

## 笔记

### Q1: flex布局
![](http://www.ruanyifeng.com/blogimg/asset/2015/bg2015071004.png)

- flex容器(flex container)
	- 如何变成一个弹性容器`display: flex`or`display: inline-flex`(内联元素也可以设置)
	- 设为flex布局后，子元素的`float`,`clear`,`vertical-align`属性将失效
	- flex容器属性
		- flex-direction
			- `flex-direction: row | row-reverse | column | column-reverse`
			- row(默认值)：延主轴方向，起点在左端(12345)
			- row-reverse：延主轴方向，起点在右端(54321)
			- column：延交叉轴方向，起点在上端
			- column-reverse：延交叉轴方向，起点在下端
		- flex-wrap
			- `flex-wrap: nowrap | wrap | wrap-reverse`
			- nowrap(默认值)：不换行
			- wrap：在空间不够的情况下可以换行，第一行在上面
			- wrap-reverse：在空间不够的情况下可以换行，第一行在下面
		- `flex-flow`
			- 是`flex-direction`和`flex-wrap`属性的简写
			- 默认值是`flex-flow: row nowrap`
		- justify-content(主轴方向上)
			- `justify-content: flex-start | flex-end | center | space-between | space-around`
			- flex-start(默认值)：左对齐
			- flex-end：右对齐
			- center：居中对齐
			- space-between：两端对齐，每个项目之间的距离相等
			- space-around：每个项目之间的距离相等，所以项目与项目之间的距离比项目与边框之间的距离大一倍
			- space-evenly：任何两个项目以及项目与边框的距离均相等
			![](https://cdn.css-tricks.com/wp-content/uploads/2013/04/justify-content-2.svg)
		- align-items(交叉轴方向上,针对flex items)
			- `align-items: flex-start | flex-end | center | baseline | stretch`
			- flex-start：交叉轴起点对齐
			- flex-end：交叉轴终点对齐
			- center：交叉轴居中对齐
			- baseline：项目第一行文字的基线对齐
			- stretch(默认值)：如果项目**没有**设置高度或者高度为**auto**，则拉伸占满整个容器的高度
			![](http://upload-images.jianshu.io/upload_images/5138806-ec26abbafb5f9156.gif?imageMogr2/auto-orient/strip)
		- align-content(针对flex lines)
			- 交叉轴版的`justify-content`,需交叉轴方向上有多行项目，如果只有1行则不起作用
			- `align-content: flex-start | flex-end | center | space-between | space-around | stretch`
			- flex-start:交叉轴的起点对齐
			- flex-end:交叉轴的终点对齐
			- center:交叉轴的居中对齐
			- space-between:交叉轴两端对齐，各行之间的距离相等
			- space-around:各行之间的距离相等
			- stretch(默认值):各行占满整个交叉轴
			![](http://www.ruanyifeng.com/blogimg/asset/2015/bg2015071012.png)
- flex项目(flex item, flex容器下的所有子元素)
	- order
		- 属性值越小，排列越靠前，默认是0，可以设负值
	- flex-grow
		- 定义项目的放大比例，默认是`0`，即如果存在剩余空间也不放大
		- 如果所有项目的`flex-grow`值都为`1`，则等分剩余空间，如果某一个项目是2，其他都是1，则`2`占2倍空间
		![](http://upload-images.jianshu.io/upload_images/5138806-f35c86e614a3d80b.gif?imageMogr2/auto-orient/strip)
	- flex-shrink
		- 定义了项目的缩小比例，默认值为`1`，随容器缩小而缩小
		- 如果将值设为`0`，则该项目将不随容器缩小而缩小,负值无效
		![](http://upload-images.jianshu.io/upload_images/5138806-9dc8e0053f71c01f.gif?imageMogr2/auto-orient/strip)
	- flex-basis
		- 定义项目占据主轴空间(main size)，默认值为auto,即项目本来的大小
		- `flex-basis: <length> | auto /* default auto */`
		- 可以设为跟`width`和`height`属性一样的值(比如350px)，则项目占据固定空间
		- `flex-basis`根据`flex-direction`的不同会影响到`width` 或者`height`
		![](http://upload-images.jianshu.io/upload_images/5138806-6155698a8e2b0f1d.gif?imageMogr2/auto-orient/strip)
	- `flex`
		- `flex-grow`,`flex-shrink`,`flex-basis`三者的缩写，推荐使用缩写
		- 默认值`flex: 0 1 auto`, 后两个属性可选
		- 设置为`auto`等价于`1 1 auto`
		- 设置为`none`等价于`0 0 auto`
	- align-self
		- 定义单个项目在交叉轴的对齐方式，可以覆盖`align-items`的属性
		- 默认值是`auto`，继承父元素的`align-items`属性
		- `align-self: auto | flex-start | flex-end | center | baseline | stretch` 其他值同`align-items`


### Q2: flex布局实战
- [flex实现响应式导航栏](https://codepen.io/hope0821/pen/brmPpv?editors=1100#0)

- [flex实现响应式圣杯布局](https://codepen.io/hope0821/pen/YxRXxK?editors=1100)

- [flex布局](https://www.w3schools.com/css/tryit.asp?filename=trycss3_flexbox_website)