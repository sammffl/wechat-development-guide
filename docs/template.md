# 模板引擎 初始化数据

```html
    <view>{{text}}</view>
    <view>{{array[0].msg}}</view>
```

```javascript
Page({
  data: {
    text: 'init data',
    array: [{msg: '1'}, {msg: '2'}]
  }
})
```