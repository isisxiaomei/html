# 表单
>```空格表示：在密码之间插入2个空格——>密&nbsp;&nbsp;码" >```
#### 表单控件
>表单中的控件可以通过type（类型）属性来变化形状颜色

1. input标签

```
用户名：<input type="text" >
密&nbsp;&nbsp;&nbsp;码：<input type="password" >
```
2. type属性
```
单选框：
性别：女<input type="radio" name="sex"> 男 <input type="radio" name="sex">
```
```
复选框：
爱好：足球<input type="checkbox" name="hobby" > 游泳<input type="checkbox" name="hobby" > 网球<input type="checkbox" name="hobby" >
```
```
普通按钮：
<input type="button" value="普通按钮" > <br>
```
```
提交按钮：
<input type="submit" value="提交按钮" > <br>
```
```
重置按钮：
<input type="reset" value="重置按钮" > <br>
```
```
图像按钮：
<input type="image" src="testFunction.html" > <br>
```
```
文件按钮：
<input type="file" value="上传文件按钮" > <br>
```
3. 其他属性
- name：设置控件名称为一组
- checked="checked"：默认选择
- value：设置文本
- size：设置控件宽度
- maxlength：允许输入的最大字符数

4. lable标签
>当鼠标点文字上时，对应的输入框光标提示输入

```
<label>用户名：<input type="text" > <br /></label>
```

```
当lable包裹多个表单时，想定位到某一个，可以通过for=“id”定位
<label for="two">用户名:<input type="text" > 密码:<input type="text" id="two"></label>
```
5. textarea标签

```
多文本，并且可以多行输入
<textarea></textarea>
```
6. select标签
- select中至少包含一个option
- 在option中定义selected="selected"时，当前项为默认项
```
<select>
    <option>北京</option>
    <option>陕西</option>
    <option>广东</option>
    <option selected="selected">云南</option>
</select>
```


>#### 控件属性

属性        | 属性值 | 描述
---         | ---    | :---:
type        | row 1 col 2 | 
name        | row 2 col 2 |
value       | row 2 col 2|
size        | row 1 col 2 | 
checked     | row 1 col 2 | 
maxlength   | row 1 col 2 | 



#### 表单域
>收集表单控件信息，并且提交

```
- form表单通过name属性区分不同form
http://localhost:63342/testjs/要提交的后端地址.html?username=sss&passwd=sss

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
***
上面学的都是html通过特性，下面介绍只有html5版本才认识的
***