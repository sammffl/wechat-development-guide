# .wxml (.html)

> 常用 `view` , `text` , `input` , `image`, `button`

列表渲染：wx:for
```html
<view wx:for="{{[1, 2, 3, 4, 5, 6, 7, 8, 9]}}" wx:for-item="i">
  <view wx:for="{{[1, 2, 3, 4, 5, 6, 7, 8, 9]}}" wx:for-item="j">
    <view wx:if="{{i <= j}}">
      {{i}} * {{j}} = {{i * j}}
    </view>
  </view>
</view>
```

条件渲染：wx:if

```html
<view wx:if="{{length > 5}}"> 1 </view>
<view wx:elif="{{length > 2}}"> 2 </view>
<view wx:else> 3 </view>
```

### button 小程序开放功能 
[api文档](https://developers.weixin.qq.com/miniprogram/dev/component/button.html)

| form-type | String | 用于 `<form/>` 组件，点击分别会触发 `<form/>` 组件的 submit/reset 事件 
| --------- | ------ | ------------------------------------------------------------ | 
| open-type | String | 微信开放能力                                                 |     


```html
<!-- 获取用户信息 -->
<button
    class="rules-confirm"
    open-type="getUserInfo"
    bindgetuserinfo="getUserInfo"
>我也要来抢流量</button>
```

```html
<!-- 小程序表单提交 （eg:服务通知） -->
<form report-submit="true" bindsubmit="formSubmit">
    <button formType="submit">Submit</button>
</form>
```

