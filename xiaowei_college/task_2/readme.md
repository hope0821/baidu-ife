## [任务描述](http://ife.baidu.com/course/detail/id/92)

## 笔记
### Q1: 有哪些垂直居中的方法
1. 利用ghost伪元素实现垂直居中
	- 使用场景：在页面的`header`部分，使logo垂直居中显示
	- [参考demo](https://codepen.io/hope0821/pen/eEKoBM)
2. 让`height`和`line-height`同时等于一个固定值
	- 使用场景：使`header`部分的导航链接垂直居中
	- 实现方式：导航链接下面的`<li>`的`height`和`line-height`同时等于`header`的高度，注意去掉`<li>`的上下`margin`
	- 或者可以设置`<li>`的`height`和`line-height`同时等于某一固定高度，再通过上下`padding`把高度撑起来

### Q2: 如何让容器自适应里面图片的大小
给外围的`<figure>`添加`max-width`属性并设置值为`min-content`，可以实现容器自适应内部图片大小
```html
<figure class='fig'>
  <img src="http://via.placeholder.com/100x80" alt="">
  <figcaption>这是一张图片</figcaption>
</figure>
```
```css
figure {
  border: 1px solid #000;
  padding: 10px;
}

.fig {
  max-width: min-content;
}
```
[参考demo](https://codepen.io/hope0821/pen/YxvMeP?editors=1100#0)

### Q3: 清除浮动

```css
.clearfix:after {
  content: "";
  display: table;
}

.clearfix:after {
  clear: both;
}
```
[清除浮动demo](https://codepen.io/hope0821/pen/YxvMBw?editors=1100#0)
