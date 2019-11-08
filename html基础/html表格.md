# 1. 表格
## 1.1 简单使用
- 表格不是用来布局的，而是用来处理数据的
- table和tr里面不要放其他标签，其他标签可以放在td里面
- tr：行
- th：表头
- td：单元格

```html
<!-- 示例1： -->
<!-- 注意：这里设置边框，table是表格的最外层框，td的boder是每个单元格的边框 -->
    <style>
      table,
      td {
        border: 1px solid #333;
      }

      thead {
        background-color: #333;
        color: #fff;
      }
    </style>
<table>
    <thead>
        <tr>
            <th colspan="2">The table header</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>The table body</td>
            <td>with two columns</td>
        </tr>
    </tbody>
</table>
```
## 1.2 表格结构
- 表格划分为caption标题、thead、tbody、tfoot；除了caption外其他3个没有实际含义，只是结构上划分

```html
<!-- 示例1： -->
<table>
    <caption>火影忍者</caption>
    <thead>
        <tr>
            <th> 姓名 </th>
            <th> 年龄</th>
        </tr>
    <thead>
    <tbody>
        <tr>
            <td>小美</td>
            <td>18</td>
        </tr>
        <tr>
            <td>张三</td>
            <td>18</td>
        </tr>
    </tbody>
</table>
```
## 1.3 表格标题
- caption：是标题标签，随着表格移动
```html
<!-- 示例1： -->
<table>
    <caption>火影忍者</caption>
    <thead>
        <tr>
            <th> 姓名 </th>
            <th> 年龄</th>
        </tr>
    <thead>
    <tbody>
        <tr>
            <td>张三</td>
            <td>18</td>
        </tr>
    </tbody>
</table>
```

# 2. 表格属性
## 2.1 常用属性
- `border`：设置表格外边距的宽度
- `cellspacing`：设置单元格和单元格中间的距离
- `cellpadding`：设置单元格内容和单元格边框的距离
- `colspan`：表示了每单元格在列上的横向扩展数量。默认值为1 。超过1000的值被视作1000。
- `rowspan`：表示单元格在行上的纵向扩展数量默认值为1
## 2.2 注意点
+ 表格中的很多属性已经废弃，建议使用css样式设置
+ 单元格文字默认是靠左对齐；`align`属性已经废弃；
    - 单元格文字水平对齐建议使用css的`text-align`
    - 单元格文字垂直对齐建议使用css的`vertical-align`

# 3. 单元格合并
## 3.1 跨列合并
- 跨列合并单元格：colspan
```html
<!-- 示例1： -->
<table width="500" height="300" border="1">
    <tr>
        <th> 姓名 </th>
        <th> 年龄</th>
        <th> 学历</th>
    </tr>
    <tr>
        <td>小美</td>
        <td>18</td>
        <td>博士</td>
    </tr>
    <tr>
        <td>张三</td>
        <td colspan="2">18博士</td>
    </tr>
</table>
```
## 3.2 跨行合并
- 跨行合并单元格：rowspan
```html
<!-- 示例1： -->
<table width="500" height="300" border="1">
    <tr>
        <th> 姓名 </th>
        <th> 年龄</th>
        <th> 学历</th>
    </tr>
    <tr>
        <td>小美</td>
        <td>18</td>
        <td rowspan="2">博士</td>
    </tr>
    <tr>
        <td>张三</td>
        <td>18</td>
    </tr>
</table>
```
# 4. 单元格拆分
https://zhidao.baidu.com/question/183699981.html


