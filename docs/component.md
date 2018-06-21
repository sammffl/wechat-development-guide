# 组件

### 基础组件
查询官方文档 [跳转](https://developers.weixin.qq.com/miniprogram/dev/component/)

### 自定义组件

#### 创建组件
<image src="../assets/component.png" width="450"></image> <br>
在json文件中会有 component
```json
{
  "component": true,
  "usingComponents": {}
}
```
```html
<!-- 这是自定义组件的内部WXML结构 -->
<view class="inner">
  {{innerText}}
</view>
<slot></slot>
```

```js
Component({
  properties: {
    // 这里定义了innerText属性，属性值可以在组件使用时指定
    innerText: {
      type: String,
      value: 'default value',
    }
  },
  data: {
    // 这里是一些组件内部数据
    someData: {}
  },
  methods: {
    // 这里是一个自定义方法
    customMethod: function(){}
  }
})
```


#### 在页面中使用组件
在页面的配置文件中进行配置
```json
{
  "usingComponents": {
    "component-tag-name": "path/to/the/custom/component"
  }
}
```
```html
<view>
  <!-- 以下是对一个自定义组件的引用 -->
  <component-tag-name inner-text="Some text"></component-tag-name>
</view>
```


#### 有待扩展