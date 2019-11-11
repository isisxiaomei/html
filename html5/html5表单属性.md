# 1. input智能表单控件
## 1.1 背景
+ ***h5之前***：如果限制input输入栏只能输入邮箱`<input type="text">`，则需要使用正则限制输入；
+ ***h5中***：采用`<input type="email">`就可以限制用户输入必须是邮箱格式，而不需要写正则
## 1.2 type新增属性值
+ 在input的type属性中新增以下值
  - email：输入合法邮箱格式
  - tel：输入合法电话格式
  - url：链接格式
  - number：数字格式
  - search：搜索格式，和普通输入框的区别，有叉号
  - range：自由拖动滑块
  - time：小时分钟格式
  - date：年月日
  - datetime：时间
  - month：年月格式
  - week：年星期格式
  - color：拾色器

```html
<!-- 示例1： -->
<input type="email">
<input type="tel">
....
```
## 1.3 input新增属性
+ `placeholder`：占位符（提示信息）
+ `autofocus`：刷新网页输入框光标出现（自动获取焦点）
+ `list`：用于关联datalist选项列表给input提供提示功能
+ `multiple`：实现多选效果
    - 文件上传时，可以多文件上传file默认只是单文件
    - select下拉菜单中默认是单选，select设置multipe属性就可以实现多选（按住shift）
+ `autocomplete`：记录表单输入，下次提醒。（注意点如下：）
    - 必须提交时候，再输入的时候才会有记录提示
    - 表单必须有name属性名
    - autocomplete有两个属性值on和off，off是提示关闭
+ `required`：必填项
+ `accesskey`：设置快捷键定位光标到输入栏，这里alt+s就会聚焦
+ `form`：可以将不同表单域数据提交到指定表单域上

```html
<!-- 示例1： -->

<input type="text" placeholder="请输入">
<input type="text" autofocus="autofocus">

昵称<input type="text" required="required">
昵称<input type="text" autofocus required >

昵称<input type="text" required="required" accesskey="s">
<input type="file" multiple="multiple">

<!-- mutiple -->
<select multiple>
      <option>111</option>
      <option>111</option>
      <option>111</option>
</select>

<form action="">
    姓名：<input type="text" autocomplete="autocomplete" name="userName">
    <input type="submit" value="提交">
</form>
```

```html
<!-- 示例1： input的form属性用法-->
<!-- submit默认只会提交form表单内部的数据；不会提交passwd；但是使用input的form属性关联到form表单的id值，submit提交时连同关联的passwd控件值也提交 -->
    <form action="" method="get" id="ff">
      <input type="text" name="usename" >
      <input type="submit" value="提交">
    </form>
    <input type="text" name="passwd" form="ff">
```


```html
<!-- 示例1： list-->
<input type="text" list="dataListId">
    <datalist id="dataListId">
        <option>刘德华</option>
        <option>刘若英</option>
        <option>张学友</option>
        <option>王菲</option>
    </datalist>
```

# 2. form表单新属性
+ autocomplete = on | off       自动完成；记录表单输入，下次提醒
+ novalidate = true | false     规定在提交表单时是否验证 form 或 input 域

```html
<!-- 示例1：novalidate -->
<!-- 下面使用email是需要对input输入验证，但是加了novalidate就不需要验证了 -->
<form action="demo-form.php" novalidate>
 E-mail: <input type="email" name="user_email">
 <input type="submit">
</form>
```

```html
<!-- 示例1: autocomplete-->
<form action="/statics/demosource/demo-form.php" autocomplete="on">
  First name:<input type="text" name="fname" value="你好"><br>
  Last name: <input type="text" name="lname"><br>
  E-mail: <input type="email" name="email" autocomplete="off" placehder="nihao"><br>
  <input type="submit">
</form>
```

