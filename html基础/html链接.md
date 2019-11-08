# 1 链接标签

## 1.1 内外链接

```html
<!-- 示例1： -->
<!-- 内连接注意写上后缀名 -->
<a href="testFunction.html"> 本地内连接</a>
<a href="http://www.baidu.com">外链接</a>
```

## 1.2 a 标签属性
- title 属性：当鼠标放在图片上，看到的文字
- target 属性：将 target 设置成 `_blank` 时，点击链接浏览器会新开一个 Tab 打开该网页


```html
<!-- 示例1： -->
<!-- 鼠标放在 FE 13 上会展示title的文字内容 -->
<a href="https://github.com/fe13" title="可能是未来中国最火的前端工程师的聚集地"
  >FE 13</a
>

<!-- 跳转到新窗口打开链接 -->
<a
  href="https://github.com/fe13"
  title="可能是未来中国最火的前端工程师的聚集地"
  target="_blank"
  >FE 13</a
>
```

# 2 链接

## 2.1 返回顶部链接

```html
<!-- 示例1：返回顶部链接 -->
<a href="#">返回页面顶部链接</a>
```

## 2.2 外部链接

```html
<!-- 示例1：跳转到新窗口打开链接 -->
<a
  href="https://github.com/fe13"
  title="可能是未来中国最火的前端工程师的聚集地"
  target="_blank"
  >FE 13</a
>
```

## 2.3 内部锚点定位

```html
<!-- 示例1： -->
<a href="#标签id"> 生活经历</a>
<p id="标签id">生活相关事情</p>
```

## 2.4 图片链接

```html
<!-- 示例1： -->
<a href="https://www.mozilla.org/en-US/">
  <img
    src="mozilla-image.png"
    alt="mozilla logo that links to the mozilla homepage"
  />
</a>
```

## 2.5 下载链接

- 当您链接到要下载的资源而不是在浏览器中打开时，您可以使用 download 属性来提供一个默认的保存文件名

```html
<!-- 示例1： -->
<a
  href="https://download.mozilla.org/?product=firefox-latest-ssl&os=win64&lang=en-US"
  download="firefox-latest-64bit-installer.exe"
>
  Download Latest Firefox for Windows (64-bit) (English, US)
</a>
```

## 2.6 电话链接

```html
<!-- 示例1 -->
<a href="tel:+8613701234567">+86 13701234567</a>
```

## 2.7 email 链接

- 注意: 每个字段的值必须是 URL 编码的。 也就是说，不能有非打印字符（不可见字符比如制表符、换行符、分页符）和空格

```html
<!-- 示例1： -->
<a href="mailto:xumeihong@2008.sina.com">Send email to nowhere</a>

<!-- 示例2： -->
<!-- cc：抄送   subject：主题  body：内容-->
<a
  href="mailto:nowhere@mozilla.org?cc=name2@rapidtables.com&bcc=name3@rapidtables.com&subject=The%20subject%20of%20the%20email&body=The%20body%20of%20the%20email"
>
  Send mail with cc, bcc, subject and body
</a>
```

# 3. 案例

```html
<style>
  a[href^="https"]::before {
    content: "🔗 ";
  }

  a[href^="mailto"]::before {
    content: "📧 ";
  }

  a[href^="tel"]::before {
    content: "📞 ";
  }

  li {
    margin-bottom: 0.5rem;
  }
</style>

<p>You can reach Michael at:</p>

<ul>
  <li><a href="https://example.com">Website</a></li>
  <li><a href="mailto:m.bluth@example.com">Email</a></li>
  <li><a href="tel:+123456789">Phone</a></li>
</ul>
```
