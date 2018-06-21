# 路由跳转


| 路由方式   | 触发时机                                                     | 路由前页面 | 路由后页面         |
| ---------- | ------------------------------------------------------------ | ---------- | ------------------ |
| 初始化     | 小程序打开的第一个页面                                       |            | onLoad, onShow     |
| 打开新页面 | 调用 API [`wx.navigateTo`](https://developers.weixin.qq.com/miniprogram/dev/api/ui-navigate.html#wxnavigatetoobject) 或使用组件 [``](https://developers.weixin.qq.com/miniprogram/dev/component/navigator.html) | onHide     | onLoad, onShow     |
| 页面重定向 | 调用 API [`wx.redirectTo`](https://developers.weixin.qq.com/miniprogram/dev/api/ui-navigate.html#wxredirecttoobject) 或使用组件 [``](https://developers.weixin.qq.com/miniprogram/dev/component/navigator.html) | onUnload   | onLoad, onShow     |
| 页面返回   | 调用 API [`wx.navigateBack`](https://developers.weixin.qq.com/miniprogram/dev/api/ui-navigate.html#wxnavigateback) 或使用组件[``](https://developers.weixin.qq.com/miniprogram/dev/component/navigator.html)或用户按左上角返回按钮 | onUnload   | onShow             |
| Tab 切换   | 调用 API [`wx.switchTab`](https://developers.weixin.qq.com/miniprogram/dev/api/ui-navigate.html#wxswitchtab) 或使用组件 [``](https://developers.weixin.qq.com/miniprogram/dev/component/navigator.html) 或用户切换 Tab |            | 各种情况请参考下表 |
| 重启动     | 调用 API [`wx.reLaunch`](https://developers.weixin.qq.com/miniprogram/dev/api/ui-navigate.html#wxrelaunch) 或使用组件 [``](https://developers.weixin.qq.com/miniprogram/dev/component/navigator.html) | onUnload   | onLoad, onShow     |

