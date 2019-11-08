# 1. 图片简介
> `imag`是单标签，并且这个元素包含全局属性
## 1.1 简单使用

```html
<!-- 示例1： -->
<img
  class="fit-picture"
  src="/media/examples/grapefruit-slice-332-332.jpg"
  alt="Grapefruit slice atop a pile of other slices"
/>

<!-- 示例2：图像链接 -->
<a href="https://developer.mozilla.org/"><img src="mdn-logo-sm.png" alt="MDN"></a>
```

## 1.2 标签属性
- title: 鼠标放上去展示的展示的信息
- alt: 图片加载不出来时显示的信息
- width: 一般情况下只修改 width 或者 height 其中的一个属性就可以，另外一个会等比例缩放，如果两个都修改，图片可能会失真

# 2. 高级操作
+  HTML5 的 <figure> 和 <figcaption> 元素，它正是为此而被创造出来的：为图片提供一个语义容器
+  <figure> 可以是几张图片、一段代码、音视频、方程、表格或别的
```html
<!-- 示例1： -->
<figure>
  <img src="https://raw.githubusercontent.com/mdn/learning-area/master/html/multimedia-and-embedding/images-in-html/dinosaur_small.jpg"
     alt="一只恐龙头部和躯干的骨架，它有一个巨大的头，长着锋利的牙齿。"
     width="400"
     height="341">
  <figcaption>曼彻斯特大学博物馆展出的一只霸王龙的化石</figcaption>
</figure>
```

# 3. css背景图片
+ 如果图像对您的内容里有意义，则应使用HTML图像。 如果图像纯粹是装饰，则应使用CSS背景图片