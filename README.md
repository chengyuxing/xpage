# 分页控件使用说明
基于javascript ES6开发，提供灵活的配置项，后端分页数据格式可以自定义配置，主题可自由发挥，
无任何强制第三方依赖，第三方依赖仅仅作为可选项：引入<b>font-awesome</b>,则显示翻页按钮默认图标，
否则显示默认文字。

## 初始化

```html
<div id="page"></div>
```

```js
const PAGE = xpage.init('page', <setting>);
```

支持自定义配置，参考：`xpage.defaultSetting`。

## 方法

### 静态

#### objectDeepClone(obj)

对象深拷贝，避免引用的问题。

#### objectDeepAssign(target = {}, source = {})

对象深分配，类似于`Object.assign`，但可以深层分配。

#### init(containerId, setting)

初始化操作。
参数：
- 分页容器ID
- 自定义配置

### 原型

#### request(url, option)

参数：

- 请求地址
- 默认选项

ajax请求分页，支持`get`（默认）、`post`（请求头`Content-Type`支持）：

- application/json
- application/x-www-form-urlencoded（默认）

#### resource(list, option)
静态数据分页请求。

参数：

- 数组类型静态数据
- 默认选项

#### sourceFrom(from, option)

分页请求。

参数：

- url或静态数据数据
- 默认选项

#### refresh()

刷新当前页数据。

## 属性

### 静态
#### defaultOption

默认选项

#### defaultSetting

默认配置
