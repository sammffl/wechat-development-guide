# 模版

创建 wxml文件
同一个模版文件可以创建多个模版
```html
<!--
  index: int
  msg: string
-->
<template name="msgItem1">
  <view>
    <text> {{index}}: {{msg}} </text>
  </view>
</template>

<!--
  time: string
-->
<template name="msgItem2">
  <view>
    <text> Time: {{time}} </text>
  </view>
</template>
```

在需要引用模版的page中导入模版
```html
<import src="../../templates/courseList.wxml"/>

<!-- 用is来说明是哪个模版 -->
<template is="msgItem" data="{{...item}}"/>
```

#### 有待扩展
