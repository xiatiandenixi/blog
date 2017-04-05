---
title: 问题总结
date: 2017-04-01
tags: 总结
reward: true
---
# card.vue
## slot插槽
外层的div没有意义
```html
<div class="card-slot">
  <slot name="media"></slot>
</div>
```
  改正
```html
<slot name="media">
  <img class="card-slot" src="../assets/logo.png" alt="">
</slot>
```
## props传递数据
 举个例子，card组件可以选择sm/md/lg三种大小

  子组件props里设置了size、 data里设置了size_: 'sm'

  在组件created钩子函数里使this.size_ = this.size
```html
  <!--默认大小 sm-->
  <card :title="child.name">
  <!--设置大小 lg-->
  <card :title="child.name" size="lg">
```

# sideDialog.vue
* 直接引用element-ui里的el-dialog组件


* 调用el-dialog实例的open和close方法要用到ref属性拿到实例
```html
<el-dialog ref="dialog">
...
</el-dialog>
this.$refs.dialog.open()
```
* el-dialog组件不能嵌套

* el-dialog封装的一些Attributes值类型为Boolean时参数前面要加上:


# 图片资源
在template里用到的图片地址如果放到script标签里要用require()包起来


# IE显示空白问题

在webpack.base.conf.js的entry配置里加上babel-polyfill



