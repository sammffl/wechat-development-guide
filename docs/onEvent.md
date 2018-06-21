# 生命周期函数

| 属性                                                         | 类型     | 描述                                                         |
| ------------------------------------------------------------ | -------- | ------------------------------------------------------------ |
| [data](https://developers.weixin.qq.com/miniprogram/dev/framework/app-service/page.html#%E5%88%9D%E5%A7%8B%E5%8C%96%E6%95%B0%E6%8D%AE) | Object   | 页面的初始数据                                               |
| onLoad                                                       | Function | 生命周期函数--监听页面加载                                   |
| onReady                                                      | Function | 生命周期函数--监听页面初次渲染完成                           |
| onShow                                                       | Function | 生命周期函数--监听页面显示                                   |
| onHide                                                       | Function | 生命周期函数--监听页面隐藏                                   |
| onUnload                                                     | Function | 生命周期函数--监听页面卸载                                   |
| onPullDownRefresh                                            | Function | 页面相关事件处理函数--监听用户下拉动作                       |
| onReachBottom                                                | Function | 页面上拉触底事件的处理函数                                   |
| onShareAppMessage                                            | Function | 用户点击右上角转发                                           |
| onPageScroll                                                 | Function | 页面滚动触发事件的处理函数                                   |
| onTabItemTap                                                 | Function | 当前是 tab 页时，点击 tab 时触发                             |
| 其他                                                         | Any      | 开发者可以添加任意的函数或数据到 object 参数中，在页面的函数中用 `this` 可以访问 |



```javascript
//index.js
Page({
  data: {
    text: "This is page data."
  },
  onLoad: function(options) {
    // Do some initialize when page load.
  },
  onReady: function() {
    // Do something when page ready.
  },
  onShow: function() {
    // Do something when page show.
  },
  onHide: function() {
    // Do something when page hide.
  },
  onUnload: function() {
    // Do something when page close.
  },
  onPullDownRefresh: function() {
    // Do something when pull down.
  },
  onReachBottom: function() {
    // Do something when page reach bottom.
  },
  onShareAppMessage: function () {
   // return custom share data when user share.
  },
  onPageScroll: function() {
    // Do something when page scroll
  },
  onTabItemTap(item) {
    console.log(item.index)
    console.log(item.pagePath)
    console.log(item.text)
  },
  // Event handler.
  viewTap: function() {
    this.setData({
      text: 'Set some data for updating view.'
    }, function() {
      // this is setData callback
    })
  },
  customData: {
    hi: 'MINA'
  }
})

```