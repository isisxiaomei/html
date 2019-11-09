> 备注： 优酷上分享拿到链接
# 1 embed（忽略）
+ 标签定义嵌入的内容（需要兼容性，以后会像audio和video过渡）
# 2 audio
## 2.1 使用
- 音频格式mp3 ogg wav
- autoplay：默认打开网页是不播放的，设置autoplay属性会自动播放
- controls：默认是看不到音频进度条，设置controls可显示播放进度条
- loop：默认只播放一边，设置2循环两次，不设置一直循环下去
```html
<!-- 示例1： -->
<audio src="音频链接" autoplay="autoplay" controls loop="2"></audio>
```
## 2.2 兼容问题
+ 兼容问题：音频的mp3格式不是每个浏览器都支持的，一般选择把几种格式都放进去
+ `source`：规定了音频或者视频的链接
```html
<!-- 示例1：音频浏览器兼容解决 -->
<audio controls>
    <source src="music.mp3">
    <source src="music.ogg">
    <source src="music.mav">
    如果以上3中格式浏览器都不支持，显示您的浏览器不支持
</audio>
```

# 3 video
## 3.1 使用
- 视频格式mp4 ogg webM
- autoplay：默认打开网页是不播放的，设置autoplay属性会自动播放
- controls：默认是看不到进度条，设置controls可显示播放进度条
- loop：默认只播放一边，设置2循环两次，不设置一直循环下去

```html
<!-- 示例1： -->
<video src="视频连接" autoplay="autoplay" controls loop></video>
```
## 3.2 兼容问题
```html
<!-- 示例1：浏览器兼容写法 -->
<video controls>
    <source src="movie.mp4">
    <source src="movie.ogg">
    <source src="movie.webM">
    您的浏览器不支持
</video>
```