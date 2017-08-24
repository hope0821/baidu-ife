## [任务描述](http://ife.baidu.com/course/detail/id/94)

## 笔记

### Q1: `<div>`里面包`<img>`时，图片下方会多出大约4px的间隙
因为`<img>`标签属于`inline`元素，默认的对齐方式是`baseline`，以下几种方式可以解决这个问题
```css
#方法一：将图片的vertical-align属性设置为[top、middle、bottom]中的任意一个值
img {
  vertical-align: middle;
}

#方法二：设置父元素的font-size属性
div {
  font-size: 0;
}

#方法三：将图片转化为块级元素
img {
  display: block;
}

```

### Q2: 左右定宽中间自适应的三栏布局
- [flex](https://codepen.io/hope0821/pen/yoqVbZ?editors=1100#0)
	- 设置父容器`container`的`display`属性为`flex`
	- 三栏在`html`结构里的顺序分别为[left、main、right]
	- `left和right`设置定宽，`main`设置属性`flex`的值为1
- [float+BFC](https://codepen.io/hope0821/pen/NvBbLO)
	- 三栏在`html`结构里的顺序分别为[left、right、main]
	- `left`向左浮动，`right`向右浮动，`main`设置`overflow`属性值为`hidden`
	- 对父容器进行浮动清除
- [圣杯](https://codepen.io/hope0821/pen/JyBbQE)
	- 三栏在`html`结构里的顺序分别为[main、left、right]
	- 三栏同时向左浮动
	- 设置`main`的宽度为`100%`
	- 利用负margin将`left`(等于main的width)和`right`(等于自身的width)拉上来，这时候`left`和`right`重叠在`main`上
	- 父容器设置左右`padding`值分别等于`left`和`right`的`width`,使整体往中间压缩
	- 利用相对定位(`position: relative`)，将`left`(left=负的自身宽度)和`right`(right=负的自身宽度)拉出来