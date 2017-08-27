## [任务描述](http://ife.baidu.com/course/detail/id/99)

## 笔记

### Q1: CSS实现文字下划线
```css
.underline {
  text-decoration: underline;
}
```

### Q2: 实现图片中的文字效果([demo](https://codepen.io/hope0821/pen/MvqzWd))
![](http://7xrwo9.com1.z0.glb.clouddn.com/font-variant.jpg)
```css
.small-caps {
  font-variant: small-caps;
}
```

### Q3: 如何画三角形([demo](https://codepen.io/hope0821/pen/VzxaPr))
- 设置`width`和`height`的值为`0`
- 设置[上、右、下、左]四条边中的三条边的`border`属性
- 如果要得到一个箭头朝上的三角形，则设置[左，下，右]三边的`border`，其中[左、右]`border`的颜色设置为`transparent`
- 可以控制三边`border`的长度，得到不同的三角形
```css
.trangle {
  width: 0;
  height: 0;
  border-left: 20px solid transparent;
  border-right: 20px solid transparent;
  border-bottom: 30px solid #000;
}
```
