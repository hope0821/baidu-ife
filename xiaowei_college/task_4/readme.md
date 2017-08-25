## [任务描述](http://ife.baidu.com/course/detail/id/95)

## 笔记

### Q1: 如何实现水平垂直居中
- 利用flex布局
	- 设置父容器`display`为`flex`
	- 分别设置`justify-content`和`align-items`的值为`center`
	- 为了使元素在浏览器中水平垂直居中，还要设置[body、html、父容器]的`height`值为`100%`
- 利用绝对定位+`transform`属性
	- 设置目标元素的`position`值为`absolute`
	- 设置`left`和`top`分别为`50%`
	- 设置`transform`值为`translate(-50%,-50%)`

### Q2: [画1/4圆](https://codepen.io/hope0821/pen/QMBrxg)
- 设置元素的宽和高
- 设置元素的`border-radius: a b c d`值,[a,b,c,d]分别对应圆弧的朝向[左上、右上、右下、左下]