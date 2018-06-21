# 模块化

每个文件都是独立的作用域，可以将一些公共的代码抽离成单独的js文件通过 `module.exports` 对外暴露

```javascript
module.exports = {
  formatTime: formatTime,
  getPermissionModal: getPermissionModal,
  normalModal: normalModal,
  checkIsStart: checkIsStart,
  getProcess: getProcess,
  getMatchDate: getMatchDate,
  showToast: showToast,
  showAppDownDialog: showAppDownDialog,
  buttonEvent: buttonEvent,
  refreshLogin: refreshLogin,
  debounce,
  showConsole,
}
```