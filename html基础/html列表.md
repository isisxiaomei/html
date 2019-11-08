# 1. 无序列表
## 1.1 使用
+ `<ul> Unordered List`
```html
<!-- 示例1： -->
<ul>
    <li>苹果</li>
    <li>香蕉</li>
    <li>橘子</li>
</ul>
```
```html
<!-- 示例2：嵌套列表 -->
<p>金州勇士队的全明星球员包括：<p>
<ul>
  <li>
    斯蒂芬·库里
    <ul>
      <li>微博：<a href="http://weibo.com/u/3432945104">@StephenCurry</a></li>
      <li>Twitter: <a href="https://twitter.com/stephencurry30">@StephenCurry30</a></li>
    </ul>
  </li>
  <li>凯文·杜兰特</li>
  <li>克莱·汤普森</li>
  <li>德雷蒙德·格林</li>
</ul>
```
## 1.2 无序列表注意点
- ul标签中不要包含其他标签
- li中可以包含其他标签
- 无序列表会带自己样式属性



# 2. 有序列表
## 2.1 使用
+ `<ol> Ordered List`
```html
<!-- 示例1： -->
<h1>这里有序ol，顺序order</h1>
<ol>
    <li>苹果</li>
    <li>香蕉</li>
    <li>橘子</li>
</ol>
```

# 3. 自定义列表
## 3.1 使用
+ dl是自定义列表标签
+ dt是自定义标题（可以省略）
+ dd是围绕dt解释的
```html
<!-- 示例1： -->
<h1>dl是自定义列表标签，dt是自定义标题，dd是围绕dt解释的</h1>
<dl>
    <dt>北京</dt>
    <dd>海淀区</dd>
    <dd>昌平区</dd>
    <dd>大兴区</dd>
</dl>
```