---
title: 主题切换
tags: [技巧]
---

## 基础准备

公共样式抽取、管理

内容型、宣传型

基础样式分类：

- 主题
  - Dark
  - Light
- 文字
  - 标题
  - 主要
  - 次要
  - 链接
  - 提示（渐进式）
- 辅助
  - 边框
  - 分割线
  - 阴影
  - 背景色
- 功能
  - Success
  - Warning
  - Danger
  - Info

## 版本迭代

### v1.x

```less
.dark {
  @bg: black;
  // ...
}
.light {
  @bg: white;
  // ...
}

html[data-theme="dark"] {
  // ...
}
html[data-theme="light"] {
  // ...
}
```

优点：SSR 站点刷新页面时，样式响应较快、切换主题立即响应

缺点：代码冗余

### v2.x

默认 light 主题，切换主题时，增删 dark 样式资源：

`<link id="theme" rel="stylesheet" type="text/css" href="/assets/css/theme/dark.css">`

缺点：闪屏偶发、切换时偶发延迟、重复请求资源

### v3.x-final

css 变量 var();

```css
:root {
  --bg: @bg;
}
:root[data-theme="dark"] {
  --bg: @bg;
}
```

// TODO 路由方式控制页面跳转
