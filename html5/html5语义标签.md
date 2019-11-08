# html5新特性

```
这里只简单写了几个，还有很多
<body>
    <header>语义：定义网页头部</header>
    <nav>语义：定义网页导航栏</nav>
    <footer>语义：定义网页底部</footer>
    <article>语义：定义文章</article>
    <section>语义：定义区域</section>
    <aside>语义：定义侧边</aside>
</body>
```
#### datalist标签
- 选项列表
- datalist一般和input连用(在input中使用list属性关联dalaist的id)
- datalist标签比起select标签更好的是输入的时候有提示，参考百度输入

```
<input type="text" list="dataListId">
    <datalist id="dataListId">
        <option>刘德华</option>
        <option>刘若英</option>
        <option>张学友</option>
        <option>王菲</option>
    </datalist>
```
#### fieldset标签
- 对表单控件分组打包
- 一般和legend标签搭配使用

```
<fieldset>
    <legend>登录</legend>
    用户名：<input type="text"> <br>
    密码：<input type="password">
</fieldset>
```
#### input标签h5新增type属性
- email：邮箱格式
- tel：电话格式
- url：链接格式
- number：数字格式
- search：搜索格式，和普通输入框的区别，有叉号
- range：自由拖滑动
- time：小时分钟格式
- date：年月日
- datetime：时间
- month：年月格式
- week：年星期格式
- color：颜色

#### h5常用新属性
```
<input type="text" placeholder="请输入">
```

```
autofocus：刷新网页输入框光标出现
<input type="text" autofocus="autofocus">
```

```
multiple：文件上传时，可以多文件上传file默认只是单文件
<input type="file" multiple="multiple">
```

```
autocomplete：记录表单输入，下次提醒
注意点：
- 必须提交时候，再输入的时候才会有记录提示
- 表单必须有name属性名
- autocomplete有两个属性值on和off，off是提示关闭
<form action="">
    姓名：<input type="text" autocomplete="autocomplete" name="userName">
    <input type="submit" value="提交">
</form>
```

```
required：必填项
昵称<input type="text" required="required">
```

```
accesskey：设置快捷键定位光标到输入栏，这里alt+s就会聚焦
昵称<input type="text" required="required" accesskey="s">
```

#### 多媒体标签
>优酷上分享拿到链接
- embed：标签定义嵌入的内容（需要兼容性，以后会像audio和video过渡）
- audio：
    - 音频格式mp3 ogg wav 
    - autoplay：默认打开网页是不播放的，设置autoplay属性会自动播放
    - controls：默认是看不到音频进度条，设置controls可显示播放进度条
    - loop：默认只播放一边，设置2循环两次，不设置一直循环下去

```
<audio src="音频链接" autoplay="autoplay" controls loop="2"></audio>
```
>>音频的mps格式不是每个浏览器都支持的，一般选择把几种格式都放进去

```
- 音频浏览器兼容解决
<audio controls>
    <source src="music.mp3">
    <source src="music.ogg">
    <source src="music.mav">
    如果以上3中格式浏览器都不支持，显示您的浏览器不支持
</audio>
```


- video：
    - 视频格式mp4 ogg webM
    - autoplay：默认打开网页是不播放的，设置autoplay属性会自动播放
    - controls：默认是看不到进度条，设置controls可显示播放进度条
    - loop：默认只播放一边，设置2循环两次，不设置一直循环下去

```

<video src="视频连接" autoplay="autoplay" controls loop></video>

- 浏览器兼容写法
<video controls>
    <source src="movie.mp4">
    <source src="movie.ogg">
    <source src="movie.webM">
    您的浏览器不支持
</video>
```
