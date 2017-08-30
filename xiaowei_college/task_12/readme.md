## [任务描述](http://ife.baidu.com/course/detail/id/117)

## 笔记

### Q1: 使用web fonts
```css
@font-face {
  font-family: myFirstFont; /*自定义字体名字*/
  src: url(sansation_light.woff);
}

/*使用自定义字体*/
div {
  font-family: myFirstFont;
}
```

### Q2: CSS3过渡([Transition](https://codepen.io/hope0821/pen/xLQWYw?editors=1100#0))
```css
.demo {
  height: 100px;
  width: 100px;
  background-color: skyblue;
/* 分别对高和宽进行过渡，时间为2s和3s */
  transition: height 2s, width 3s;
}

/* 当hover目标元素时触发过渡，改变宽和高 */
.demo:hover {
  width: 300px;
  height: 200px;
}
```


### Q3: CSS3动画([Animation](https://codepen.io/hope0821/pen/QMJmxJ?editors=1100))

### Q4: `<a>`标签的使用([demo](https://codepen.io/hope0821/pen/dzQmQv?editors=1100#0))
- 通过`<a>`标签的`href=“#target_id”`属性和目标元素建立钩子
- 通过点击`a`元素，触发目标元素的过渡和动画效果
```html
<div><a href="#demo">按钮</a></div>

<div id="demo"></div>
```

```css
#demo {
  width: 100px;
  height: 100px;
  background-color: skyblue;
  transition: background-color 2s;
  position: relative;
}

@keyframes demo {
  from {left: 0;}
  to {left: 100px;}
}

#demo:target {
  background-color: red;
  animation: demo 2s;
}
```

### Q5: 响应式图片
```css
/ * 针对图片 */
img {
  width: 100%;
  height: auto;
}


/* 结合媒体查询，针对图片的容器 */

.responsive {
  padding: 0 6px;
  float: left;
  width: 24.99999%;
}

@media only screen and (max-width: 700px){
  .responsive {
    width: 49.99999%;
    margin: 6px 0;
  }
}

@media only screen and (max-width: 500px){
  .responsive {
    width: 100%;
  }
}

```

### Q6: CSS伪类选择器可以叠加使用
- `a:hover:not(.active) {...}`，对没有`.active`类的对象添加hover伪类
- `li: not(:target)`，选择当前目标以外的`li`元素
- `a:not(:last-child)`，选择除了最后一个以外的`a`元素

### Q7: `resize`属性
- 允许用户自定义窗口大小，配合`overflow:auto`使用
- `resize: horizontal | vertical | both`
- [demo](https://www.w3schools.com/css/tryit.asp?filename=trycss3_resize)

### Q8: `outline`和`border`的区别
- outline是是围绕元素周围的线段，在border区域外
- outline不占据空间
- outline可能不是矩形
- outline-offset可以改变outline的位置，可以是负值
- [demo](https://www.w3schools.com/css/tryit.asp?filename=trycss3_outline-offset)

### Q9: 响应式表格([table](https://www.w3schools.com/css/tryit.asp?filename=trycss_table_responsive))
```html
<div class='table'>
  <table>...</table>
</div>
```

```css
.table {
  overflow-x: auto;
}
```

### Q10: `::selection`伪元素([demo](https://www.w3schools.com/css/tryit.asp?filename=trycss3_selection))
```css
/* 选中后高亮 */
::selection {
  color: red;
  background: yellow;
}

```

### Q11: CSS自动添加序列([demo](https://codepen.io/hope0821/pen/vJQqmX?editors=1100#0))