---
category: Components
type: 反馈
title: Notification
subtitle: 通知提醒框
cover: https://gw.alipayobjects.com/zos/alicdn/Jxm5nw61w/Notification.svg
---

全局展示通知提醒信息。

## 何时使用

在系统四个角显示通知提醒信息。经常用于以下情况：

- 较为复杂的通知内容。
- 带有交互的通知，给出用户下一步的行动点。
- 系统主动推送。

## API

- `notification.success(config)`
- `notification.error(config)`
- `notification.info(config)`
- `notification.warning(config)`
- `notification.warn(config)`
- `notification.open(config)`
- `notification.close(key: String)`
- `notification.destroy()`

config 参数如下：

| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| btn | 自定义关闭按钮 | VNode | - |  |
| bottom | 消息从底部弹出时，距离底部的位置，单位像素。 | string | `24px` |  |
| class | 自定义 CSS class | string | - |  |
| description | 通知提醒内容，必选 | string \|VNode | - |  |
| duration | 默认 4.5 秒后自动关闭，配置为 null 则不自动关闭 | number | 4.5 |  |
| getContainer | 配置渲染节点的输出位置 | () => HTMLNode | () => document.body |  |
| icon | 自定义图标 | VNode | - |  |
| key | 当前通知唯一标志 | string | - |  |
| message | 通知提醒标题，必选 | string \|VNode | - |  |
| placement | 弹出位置，可选 `topLeft` `topRight` `bottomLeft` `bottomRight` | string | topRight |  |
| style | 自定义内联样式 | Object \| string | - |  |
| onClose | 点击默认关闭按钮时触发的回调函数 | Function | - |  |
| onClick | 点击通知时触发的回调函数 | Function | - |  |
| top | 消息从顶部弹出时，距离顶部的位置，单位像素。 | string | `24px` |  |
| closeIcon | 自定义关闭图标 | VNode | - |  |

还提供了一个全局配置方法，在调用前提前配置，全局一次生效。

- `notification.config(options)`

```js
notification.config({
  placement: 'bottomRight',
  bottom: '50px',
  duration: 3,
});
```

| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| bottom | 消息从底部弹出时，距离底部的位置，单位像素。 | string | `24px` |  |
| duration | 默认自动关闭延时，单位秒 | number | 4.5 |  |
| getContainer | 配置渲染节点的输出位置 | () => HTMLNode | () => document.body |  |
| placement | 弹出位置，可选 `topLeft` `topRight` `bottomLeft` `bottomRight` | string | topRight |  |
| top | 消息从顶部弹出时，距离顶部的位置，单位像素。 | string | `24px` |  |
| closeIcon | 自定义关闭图标 | VNode | - |  |
