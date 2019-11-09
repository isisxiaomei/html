# 1. 文档结构新语义
## 1.1 文档结构语义标签
> 以下结果语义都是块元素
+ `<header>`：定义网页头部`</header>`
+ `<nav>`：定义网页导航栏`</nav>`
+ `<footer>`：定义网页底部`</footer>`
+ `<article>`：定义内容`</article>`
+ `<section>`：定义区段`</section>`
+ `<aside>`：定义侧边`</aside>`
```html
<!-- 示例1：如图 -->
<img title="HTML5 语义元素" src="https://7n.w3cschool.cn/statics/images/course/img_sem_elements.gif" alt="" height="207" width="174">
```
## 1.2 结构语义标签和div的区别
+ 主要的区别在于div是没有语义的
```html
<!-- 示例1： -->
<!-- 其他语义结构同下 -->
<header></header>   ==>  <div class="header"></div>
<nav></nav>         ==>  <div class="nav"></div>
```
## 1.3 优点
+ 选择合适的标签、使用合理的代码结构，便于开发者和视觉障碍人士阅读，同时让浏览器的爬虫和机器很好地解析

## 1.4 新语义浏览器兼容性
+ 背景：有的低版本浏览器不支持html5；所以需要插件
+ 注意点：下面的语义插件必须放在<head> 元素中
```html
<!-- 示例1：h5解决语义浏览器支持 -->
<!-- 下面代码只有IE认识，在IE中会执行 -->
<!-- 按cc:ie 就会出来 -->
<!--[if lte IE 8]>
    <script src="html5shiv.js"></script>
<![endif]-->
```

# 2. 语义标签描述
+ `<figure>`：规定独立内容
+ `<figcaption>`：描述内容；figcaption不是块元素
+ `<figcaption>`元素应该被置于 "figure" 元素的第一个或最后一个子元素的位置。
```html
<!-- 示例1：figcaption描述img图片的内容 -->
<figure>
  <img src="img_pulpit.jpg" alt="The Pulpit Rock" width="304" height="228">
  <figcaption>Fig1. - The Pulpit Pock, Norway.</figcaption>
</figure>
```



























