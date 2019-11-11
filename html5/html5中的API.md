# 1 获取页面元素及类名属性和自定义属性

## 1.1 获取页面元素

- document.querySelector("选择器")
  - 这里是任何选择器，在 css 中可以使用的选择器都可以使用
  - 只返回匹配到的第一个
- document.querySelectorAll("选择器")
  - 这里是任何选择器，在 css 中可以使用的选择器都可以使用
  - 匹配符合条件的所有并返回集合

```html
<!-- 示例1： -->
<body>
  <ul>
    <li>
      <p>
        <span>111</span>
      </p>
    </li>

    <li>
      <span>222</span>
    </li>
  </ul>
  <script>
    document.querySelector("li p span").style.color = "red";
    document.querySelectorAll("li span")[0].style.color = "blue";
    document.querySelectorAll("li span")[1].style.color = "blue";
  </script>
</body>
```

## 1.2 操作类名属性

- 背景：jquery 也提供增加类名删除类名的方法；但是需要引入 jquery 库；所以 h5 提供的操作类名的不需要引入额外的库
- 具体方法如下：
  - domObj.classList.add("类名")：添加类名
  - domObj.classList.remove("类名")：移除类名
  - domObj.classList.contains("类名")：是否包含类名
  - domObj.classList.toggle("类名")：在添加和移除类名间切换
- 注意点：以上方法都是针对一个 dom 元素对象而言，所以注意只能使用 getElementById 和 querySelector 返回才是唯一的元素对象而不是集合对象

```html
<!-- 示例1： -->
<style>
  .pColor {
    color: red;
  }
</style>
<body>
  <p id="pid">你好吗</p>
  <input type="button" value="ok" />
  <script>
    // 方式1采用getElementById
    var pObj = document.getElementById("pid");
    pObj.classList.add("pColor");

    //  方式2：采用querySelector
    // var iObj = document.querySelector("input");
    // iObj.onclick = function (){
    // 	pObj.classList.add("pColor");
    // };
  </script>
</body>
```

## 1.3 自定义属性

- 背景：标签都是可以自定义属性的，但是命名不规范，h5 帮我们规范了命名
- 自定义属性命名：以`data-` 开头；注意属性名不包含`data-`
- 自定义属性获取：obj.dataset —— 返回标签对象的自定义属性列表对象
- 自定义属性设置：obj.dataset.自定义属性名 —— 进行设置

```html
<!-- 示例1： -->
<script>
  // 自定义属性获取：
  // 注意：1. "data-"是命名规范格式并不是属性名 2. 获取到的自定义属性会自动变成驼峰式
  var objs = document.querySelector(".one").dataset;
  console.log(objs.testName);

  // 自定义属性设置: age	——> data-age;
  objs.age = "18";
  // testHeight ——> data-test-height
  objs.testHeight = "170";
</script>
```

# 2 文件读取




# 3 获取网络状态

- 获取当前网络状态
  - `window.navigator.onLine` 返回布尔值判断网络状态连网或者断网
- 网络状态事件
  - `window.ononline` 网络联通事件
  - `window.onoffline` 网络断开事件

```js
// 示例1：
var rst = window.navigator.onLine;
if (rst) {
  alert("当前处于连网状态");
} else {
  alert("当前处于断网状态");
}

// 示例2：
// 当网络连通时触发
window.ononline = () => {
  alert("网络连接在线");
};

//   当网络断开时触发
window.onoffline = () => {
  alert("网络连接断开");
};
```

# 4 获取地理定位

- 获取一次当前位置
  - `window.navigator.geolocation.getCurrentPosition(successCallBack, errorCallBack);`
  - coords.latitude 纬度
  - coords.longitude 经度
  - 获取一次定位不可靠
- 获取实时定位
  - `window.navigator.geolocation.watchPosition(successCallBack, errorCallBack);`
  - coords.latitude 纬度
  - coords.longitude 经度

```js
//   示例1：获取一次定位
window.navigator.geolocation.getCurrentPosition(successCallBack, errorCallBack);
function successCallBack(position) {
  //  position位置对象
  console.log(position);
  // 纬度
  console.log(position.coords.latitude);
  // 经度
  console.log(position.coords.longitude);
}
function errorCallBack(error) {
  // 错误信息对象
  console.log(error);
}

// 示例2：获取实时定位
window.navigator.geolocation.watchPosition(
  position => {
    console.log(position);
    console.log(position.coords.latitude);
    console.log(position.coords.longitude);
  },
  error => {
    console.log(error);
  }
);
```

# 5 本地存储

## 5.1 localStorage

- 特点：
  - 永久生效（关闭窗口依然存在）
  - 多窗口共享
  - 容量大约 20M
- 使用：
  - 设置：window.localStorage.setItem(key, value);
  - 获取：window.localStorage.getItem(key);
  - 移除：window.localStorage.removeItem(key);
  - 清空：window.localStorage.clear();

```js
// 示例1：
var list = '[{"1": "11","2": "22"},{"1": "11","2": "22"}]';
window.localStorage.setItem("age", 20);
window.localStorage.setItem("list", list);
//   window.localStorage.getItem("age");
//   window.localStorage.removeItem("age");
window.localStorage.clear();
```

## 5.2 sessionStorage

- 特点：
  - 窗口关闭则失效
  - 容量大约 5M
- 使用：
  - window.sessionStorage.setItem(key, value);
  - window.sessionStorage.getItem(key);
  - window.sessionStorage.removeItem(key);
  - window.sessionStorage.clear();

# 6 操作多媒体
+ 作业：音乐播放器或者视频播放器