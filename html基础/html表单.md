# 表单
>```空格表示：&nbsp;```

## 1 input标签
###  1.1 使用
```html
<!-- 示例1： -->
用户名：<input type="text" >
密&nbsp;&nbsp;&nbsp;码：<input type="password" >
```
### 1.2 type属性
```html
<!-- 示例1：单选框 -->
性别：女<input type="radio" name="sex"> 男 <input type="radio" name="sex">

<!-- 示例2：复选框 -->

爱好：足球<input type="checkbox" name="hobby" > 游泳<input type="checkbox" name="hobby" > 网球<input type="checkbox" name="hobby" >

<!-- 示例3：普通按钮：不会提交 -->

<input type="button" value="普通按钮" > <br>

<!-- 示例4： 提交按钮：会提交-->

<input type="submit" value="提交按钮" > <br>

<!-- 示例5：重置按钮：重置输入 -->
<input type="reset" value="重置按钮" > <br>

<!-- 示例6：图像按钮： -->
<input type="image" src="testFunction.html" > <br>

<!-- 示例7：文件按钮： -->
<input type="file" value="上传文件按钮" > <br>
```
### 1.3 其他属性
- name：设置控件名称为一组
- checked="checked"：默认选择
- value：设置文本
- size：设置控件宽度
- maxlength：允许输入的最大字符数
## 2 lable标签
>当鼠标点文字上时，对应的输入框光标提示输入
### 2.1 使用
```html
<!-- 示例1： -->
<label>用户名：<input type="text" > <br /></label>
```
### 2.2 for属性定位
+ 当lable包裹多个表单时，想定位到某一个，可以通过for=“id”定位
```html
<!-- 示例1： -->
<label for="two">用户名:<input type="text" > 密码:<input type="text" id="two"></label>
```
## 3 textarea标签
### 3.1 使用
+ 多文本，并且可以多行输入
```
<textarea></textarea>
```
## 4 select标签
- select中至少包含一个option
- 在option中定义selected="selected"时，当前项为默认项
```html
<!-- 示例1： -->
<select>
    <option>北京</option>
    <option>陕西</option>
    <option>广东</option>
    <option selected="selected">云南</option>
</select>
```


## 5 form标签
### 5.1 使用
>收集表单控件信息，并且提交
+ form表单通过name属性区分不同form
+ `http://localhost:63342/testjs/要提交的后端地址.html?username=sss&passwd=sss`
```html
<!-- 示例1： -->
<form action="要提交的后端地址.html" method="get" name="form1">
    <label>用户名：<input type="text" name="username"></label>
    <label>密  码：<input type="password" name="passwd"></label>
    <input type="submit" value="提交">
    <input type="reset" value="重置">
</form>

// 一般如果没有action则不需要submit，直接用button就行；submit表示往action的路径上提交；
<form>
    <label>用户名：<input type="text" name="username" id="username"></label>
    <label>密  码：<input type="password" name="passwd" id="passwd"></label>
    <input type="button" value="提交">
    <input type="reset" value="重置">
</form>
```
### 5.2 get VS post
+ 表象不同，get把提交的数据url可以看到，post看不到
+ 原理不同，get 是拼接 url， post 是放入http 请求体中
+ 提交数据量不同，get最多提交1k数据，浏览器的限制。post理论上无限制，受服务器限制
+ get提交的数据在浏览器历史记录中，安全性不好
+ 场景不同，get 重在 "要", post 重在"给"