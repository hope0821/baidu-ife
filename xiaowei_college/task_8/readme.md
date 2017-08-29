## [任务描述](http://ife.baidu.com/course/detail/id/104)

## 笔记

### Q1: 响应式网格布局
- 将页面等分成12栏，利用百分比表示长度
- 利用@media查询，根据页面宽度选择相应的class
- `.container`的正`padding`和`.row`的负`margin`可以抵消
- 所有`col-x`要浮动，并设置`min-height`
- 在`.row`这层要清除浮动
