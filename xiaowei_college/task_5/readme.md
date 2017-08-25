## [任务描述](http://ife.baidu.com/course/detail/id/96)

## 笔记

### Q1: 字体单位的选择
```css
# 设置html的font-size为62.5%，这个时候1rem=10px
html {
  font-size: 62.5%;
}
```

### Q2: 实现图中的需求
![](http://7xrwo9.com1.z0.glb.clouddn.com/ife-task_5_note.jpg)
```css
.grey-bar {
  border-left: 3px solid #ccc;
/* 通过padding把竖条拉长 */
  padding: 8px;
}

.right-align {
  text-align: right;
  display: inline-block;
/* 根据实际情况调整宽度 */
  width: 33%;
}

.top-align {
  vertical-align: top;
}
``` 