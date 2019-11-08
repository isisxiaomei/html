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
