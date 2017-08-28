## [任务描述](http://ife.baidu.com/course/detail/id/102)

## 笔记

### Q1: header导航部分垂直居中布局的解决方案
- `header`指定高度
- logo和nav垂直居中
- 可以设置`a`标签的`padding`来实现`hover`时`border-bottom`的效果
```html
<header>
    <nav class="top">
        <span>新世界</span>
        <ul>
            <li><a href="#">首页</a></li>
            <li><a href="#">最新活动</a></li>
            <li><a href="#">项目介绍</a></li>
            <li><a href="#">爱心社区</a></li>
            <li><a href="#">关于我们</a></li>
            <li><a href="#">登入</a></li>
        </ul>
    </nav>
</header>
```

```css
header {
  height: 58px;
}

.top {
  line-height: 58px;
}

.top span {
  float: left; #脱离文档流，<ul>标签上来
}

.top ul {
  text-align: right; #让导航部分的文字在header的右边显示
}
.top li {
  display: inline-block; #在一栏显示
```

### Q2: 图片导入方式
- 通过`img`标签
- 通过`background：url("xxx.png") no-repeat`

### Q3: css-sprite雪碧图
- 将小图标合成一张大图（[css-sprite](http://css.spritegen.com/)）
- 通过`background：url("xxx.png")`导入
- 设置图片的`background-position`属性
- 设置图片的`width`和`height`属性
- 可以配合`::before`或者`::after`伪元素使用
```css
.pseudo::before {
/* 创建一个内容为空的元素 */
  content: "";
/* 根据需求是否要独占一行选择inline-block或者block */
  display: inline-block;
/* 导入图片 */
  background: url('../img/sprites.png') no-repeat;
  background-position: -43px -184px;
  width: 31px;
  height: 31px;
/* 调整图片位置 */
  position: relative;
  top: 8px;
  margin-right: 6px;
}
```
### Q4: 多行元素水平垂直居中
```html
<div class='parent'>
  <div class='wrap'>
    <h1>xxx</h1>
    <h2>xxxxxx</h2>
    <div>xxxx</div>
    <p>xxxx</p>
  </div>
</div>
```
```css
.parent {
/* 实现wrap包裹下的块级元素水平垂直居中*/
  display: flex;
  justify-content: center;
  align-items: center;
/* 实现文本中间对齐 */
  text-align: center;
}

/* 如果wrap指定了长度, 则设置margin属性实现水平居中 */
.wrap {
  margin: 0 auto;
}
```

### Q5: 多行段落末尾显示省略号的css实现
```css
/* 需配合目标元素的width属性使用，指定width*/
.multi-lines-ellipsis {
  display: -webkit-box;
/* 控制多少行开始省略 */
  -webkit-line-clamp: 2; 
  -webkit-box-orient: vertical;
  overflow: hidden;
}
```