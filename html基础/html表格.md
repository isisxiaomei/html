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
- `border`：设置表格外边距的宽度(建议采用css的boder))
- `cellspacing`：设置单元格和单元格中间的距离
- `cellpadding`：设置单元格内容和单元格边框的距离
- `colspan`：表示了每单元格在列上的横向扩展数量。默认值为1 。超过1000的值被视作1000。
- `rowspan`：表示单元格在行上的纵向扩展数量默认值为1
## 2.2 注意点
+ 表格中的很多属性已经废弃，建议使用css样式设置
+ `<td>&nbsp;</td>`：表示单元格内容为空
+ 单元格文字默认是靠左对齐；`align`属性已经废弃；
    - 单元格文字水平对齐建议使用css的`text-align`
    - 单元格文字垂直对齐建议使用css的`vertical-align`

# 3. 单元格合并
## 3.1 跨列合并
- 跨列合并单元格：`colspan`
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
- 跨行合并单元格：`rowspan`
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


# 5. 为表格的列提供共同样式
+ ***背景***：如果你想让一列中的每个数据的样式都一样，那么你就要为每个数据都添加一个样式，这样的做法是令人厌烦和低效的
+ `<col> 和 <colgroup>`：可以定义整列数据的样式信息；这里`col`需要被包裹在`colgroup`中
+ 样式信息应用到每一列，我们可以只使用一个 <col> 元素，不过需要包含 span 属性
    - `<col style="background-color: yellow" span="2">`

```html
<!-- 示例1：为同一列的每个单元格分别增加样式 -->
<table>
  <tr>
    <th>Data 1</th>
    <th style="background-color: yellow">Data 2</th>
  </tr>
  <tr>
    <td>Calcutta</td>
    <td style="background-color: yellow">Orange</td>
  </tr>
  <tr>
    <td>Robots</td>
    <td style="background-color: yellow">Jazz</td>
  </tr>
</table>

<!-- 示例2：改进版 -->
<!-- 每一个<col>都会制定每列的样式，对于第一列，我们没有采取任何样式，但是我们仍然需要添加一个空的 <col> 元素，如果不这样做，那么我们的样式就会应用到第一列上 -->
<table>
  <colgroup>
    <col>
    <col style="background-color: yellow">
  </colgroup>
  <tr>
    <th>Data 1</th>
    <th>Data 2</th>
  </tr>
  <tr>
    <td>Calcutta</td>
    <td>Orange</td>
  </tr>
  <tr>
    <td>Robots</td>
    <td>Jazz</td>
  </tr>
</table>

<!-- 示例3： 应用在每列的样式-->
<table>
  <colgroup>
    <col style="background-color: yellow" span=2>
  </colgroup>
  <tr>
    <th>Data 1</th>
    <th>Data 2</th>
  </tr>
  <tr>
    <td>Calcutta</td>
    <td>Orange</td>
  </tr>
  <tr>
    <td>Robots</td>
    <td>Jazz</td>
  </tr>
</table>

```
```html
<!-- 示例1： -->
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <title>School timetable</title>
    <style>
      html {
        font-family: "Microsoft";
      }
      table {
        border-collapse: collapse;
        border: 2px solid rgb(200, 200, 200);
        letter-spacing: 1px;
        font-size: 0.8rem;
      }
      td,
      th {
        border: 1px solid rgb(190, 190, 190);
        padding: 10px 20px;
      }
      td {
        text-align: center;
      }
      caption {
          font-size: 20px;
          font-weight: bold;
          margin-bottom: 20px;
      }

    </style>
  </head>
  <body>
    <table>
      <caption>
        School timetable
      </caption>
      <colgroup>
        <col span="2">
        <col style="background-color: rgb(0, 255, 255);">
        <col>
        <col style="background-color: rgb(0, 255, 255);">
        <col style="background-color: rgb(255, 153, 0);">
        <col span="2">

    </colgroup>
      <tr>
        <td>&nbsp;</td>
        <th>Mon</th>
        <th>Tues</th>
        <th>Wed</th>
        <th>Thurs</th>
        <th>Fri</th>
        <th>Sat</th>
        <th>Sun</th>
      </tr>
      <tr>
        <th>1st period</th>
        <td>English</td>
        <td>&nbsp;</td>
        <td>&nbsp;</td>
        <td>German</td>
        <td>Dutch</td>
        <td>&nbsp;</td>
        <td>&nbsp;</td>
      </tr>
      <tr>
        <th>2nd period</th>
        <td>English</td>
        <td>English</td>
        <td>&nbsp;</td>
        <td>German</td>
        <td>Dutch</td>
        <td>&nbsp;</td>
        <td>&nbsp;</td>
      </tr>
      <tr>
        <th>3rd period</th>
        <td>&nbsp;</td>
        <td>German</td>
        <td>&nbsp;</td>
        <td>German</td>
        <td>Dutch</td>
        <td>&nbsp;</td>
        <td>&nbsp;</td>
      </tr>
      <tr>
        <th>4th period</th>
        <td>&nbsp;</td>
        <td>English</td>
        <td>&nbsp;</td>
        <td>English</td>
        <td>Dutch</td>
        <td>&nbsp;</td>
        <td>&nbsp;</td>
      </tr>
    </table>
  </body>
</html>
```

# 6 技巧
+ 默认单元格的大小是刚好包住内容；可以通过设置padding来撑开单元格
+ border是table和td都可以设置的
+ 可以通过css的`border-collapse: collapse;`决定table的border和单元格的boder是重合或者分开