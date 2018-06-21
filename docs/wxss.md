# .wxss (.css)

### 尺寸单位

> **rpx**（responsive pixel）: 可以根据屏幕宽度进行自适应。规定屏幕宽为750rpx。如在 iPhone6 上，屏幕宽度为375px，共有750个物理像素，则750rpx = 375px = 750物理像素，1rpx = 0.5px = 1物理像素。


### 响应式布局

推荐使用弹性布局

```css
/* 父容器 */
.container {
    display: flex;
    flex-direction: column;
    flex-wrap: nowrap;
    justify-content: flex-start;
    align-items: center;
}

/* 子容器 */
.item {
    flex: 1;
}

```
<image src="../assets/flex.png" width="600"></image>